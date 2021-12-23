---
title: Структура руководства по процессу
description: В этой теме приводятся сведения о структуре руководства по процессам для разработчиков, расширяющих мобильные процессы для склада в X++.
author: Mirzaab
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 6882c979ad9b37eb4f95a04259b6ac0f0a0edcdc
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902054"
---
# <a name="process-guide-framework"></a>Структура руководства по процессу

[!include [banner](../includes/banner.md)]

В этой теме приводятся сведения о структуре руководства по процессам для разработчиков, расширяющих мобильные процессы для склада в X++. Мобильные процессы склада расширяются в результате выполнения процессов, разбитых на небольшие этапы. Бизнес-логика и построение пользовательского интерфейса каждого шага были извлечены в отдельные классы, что позволяет выполнять расширяемость.

## <a name="overview-of-the-existing-design"></a>Обзор существующей структуры

Потоки мобильного выполнения склада доступны через одну настраиваемую конечную точку службы. Запрос поступает от мобильного приложения в виде XML-строки, которая содержит метаданные интерфейса пользователя, представленного в мобильном приложении, а также значения, введенные пользователем.

При получении запроса первым шагом является десериализация этого XML. Класс **WHSMobileAppServiceXMLTranslator** преобразовывает XML в контейнер, который содержит как информацию об элементе управления, так и информацию сеанса.

После этого сведения в контейнере используются для вычисления того, с каким складом работает и собирается начать работать пользователь (представлено перечислением **WHSWorkExecuteMode**), и соответствующим образом создания экземпляра производного класса **WHSWorkExecuteDisplay**. Вызывается метод **displayform()**, который выполняет следующие действия:

-   Обрабатывает данные пользователя (делегировано классу **WHSRFControlData**, но некоторые процессы реализуют определенную логику путем переопределения метода **processControl()**).

-   Выполняет бизнес-логику.

-   Увеличивает шаг.

-   Создает контейнер, представляющий новый интерфейс пользователя (обычно в методе **build…()**).

Затем контейнер возвращается в переводчик, который затем сериализует XML и отправляет его обратно в виде ответа в мобильное устройство.

Следующая схема последовательности показывает обзор потока выполнения. Обратите внимание, что диаграмма является более схематическим обзором и не является представлением фактического кода 1:1.

![Схематический обзор процесса.](media/schematic-overview.png) 

### <a name="reason-for-the-redesign"></a>Причина переработки структуры

Приведенная выше структура предлагает очень простую структуру для создания процессов, используемых в мобильных потоках. Однако, как очевидно выше, методы **displayform()** выполняют несколько обязанностей. Он делегирует их другим методам и классам, но в отсутствие обязанностей конкретных классов он выполняется в несогласованном порядке между классами. Кроме того, поскольку число поддерживаемых сценариев растет, некоторые из этих классов могут оказаться довольно сложными. Чтобы сделать события более интересным, некоторые из этих классов или методов переопределяются и повторно используются в нескольких режимах. Результатом являются очень длинные методы с высокой сложностью циклов. Это создавало сложности с обслуживанием в прошлом. Устранение ошибок в этих методах является опасной и подверженной регрессии ситуацией.
Например, метод **processWorkLine()** в классе **WhsWorkExecuteDisplay** упоминается в нескольких процессах (в основном это место, где выполняется выполнение работы).

Чтобы сделать их расширяемыми, одним из вариантов является разбиение методов **displayForm** на более мелкие методы и ввод точек расширения. Однако из-за матрицы сценариев у партнеров могут возникнуть сложности с созданием расширений и проверками на регрессию. Это объясняется не только с тем, что в связи с отсутствием структурного распределения обязанностей, что указано выше, код будет обновляться непредсказуемым образом с течением времени, что приведет к проблемам при создании качественных расширений.

В результате переработка является действенными вариантом, и цель заключается в получении четко определенных классов независимыми обязанностями. У класса должна быть одна обязанность, одна из причин для изменения и одна из причин расширения.

## <a name="design-overview"></a>Обзор разработки

В переработанной структуре основная стратегия основана на двух принципах: разделение потока выполнения на отдельные компоненты с помощью правильно определенных обязанностей и создание четко заданных точек расширения в каждом из компонентов.

Имя новой платформы — "ProcessGuide". Это объясняется тем, что целью этих классов является направление пользователя через бизнес-процесс (в противоположность полному клиенту, который представляет собой взаимодействия на основе формы, когда пользователь обладает большей гибкостью взаимодействия с данными или порядком выполнения ими задач).

> [!NOTE]
> Одной из заметных особенностей является преднамеренное опущение префикса "WHS". В то время как мобильные процессы изначально были введены для складских операций, они имеют широкие возможности для поддержки различных процессов управления производством и запасами. В результате ссылка на склад исключена из названия структуры.

Для идентификации компонентов первым шагом является обзор процесса запуска производства (класс **WhsWorkExecuteDisplayProdStart**). Ниже представлена схема процесса.

![Изображение схематического процесса.](media/production-start-process-schematic.png)

Глядя на поток управления, необходимы следующие компоненты:

-   Контроллер для объединения всего бизнес-процесса.
-   Шаг, ответственный за выполнение этапа процесса.
-   Обработчик данных для обработки данных на шаге.
-   Конструктор страниц, отвечающий за создание пользовательского интерфейса для шага.
-   Агент навигации, ответственный за переход шагов.
-   Класс, отвечающий за выполнение бизнес-процесса.

На схеме потока операций выше, если начать с шага 1 и начать обработку данных с предыдущего шага, а затем завершить создание пользовательского интерфейса, данные на следующем этапе будут продолжать обрабатываться. Это обеспечивает тесную связь между последовательными шагами, в результате чего наша новая схема высокого уровня будет выглядеть следующим образом:

![Изображение высокоуровневой схематической обработки.](media/high-level-schematic.png)

Ниже перечислены ключевые компоненты переработанного процесса:

-   **ProcessGuideController** — этот класс используется для организации общего выполнения бизнес-процесса. Он определяет фабрики, которые создают экземпляр шага, и агента навигации, который, в свою очередь, составляет выполнение процесса, а также логику очистки для отмены или выхода из процесса.

-   **ProcessGuideStep** — этот класс представляет один отдельный шаг в бизнес-процессе. Этот класс содержит определение фабрик, которые создают экземпляр конструктора страниц, действий и обработчиков данных, и отвечает за их вызов в правильной последовательности.

-   **ProcessGuideNavigationAgent** — этот класс отвечает за навигацию между шагами. После завершения этапа агент навигации отвечает за определение следующего шага и передает все параметры, которые могут потребоваться для связи с следующего шага с предыдущим шагом.

-   **ProcessGuidePageBuilder** — этот класс отвечает за создание экземпляров пользовательского интерфейса.

-   **ProcessGuideAction** — этот класс представляет действие, отображаемое в качестве кнопки для пользователя.

-   **ProcessGuideDataProcessor** — этот класс отвечает за обработку данных, введенных пользователем в поле.

## <a name="execution-flow"></a>Поток выполнения

Начальная точка потока выполнения остается неизменной. Таким образом, запрос по-прежнему приходит через те же конечные точки, а затем десериализует XML в контейнер. Этот контейнер затем передается в **getNextFormState()**.

Существует три важных класса, которые необходимо отметить:

-  **ProcessGuideSessionState** — содержит информацию о состоянии сеанса: режим, проход, контроллер, выполняемый шаг и т. д.

-  **ProcessGuidePage** — содержит строго типизированное представление метаданных пользовательского интерфейса.

-  **ProcessGuideRequest** — содержит оба указанных выше как элементы и является строго типизированным представлением запроса, полученного от мобильного устройства.

Эти классы создаются с помощью сведений контейнера (состояние и введенные пользователем данные управления). Это обеспечивает способ доступа с защитой типа и управление значениями. В сравнении с повторяющимся доступом контейнера в ходе процесса это дает преимущества как для удобочитаемости, так и для повышения производительности.

Сведения о состоянии сеанса используются для создания соответствующего класса **ProcessGuideController**. После создания экземпляра вызывается метод **createResponse()** в классе **ProcessGuideController**. Этот метод является точкой входа в логику руководства по процессам и после выполнения возвращается с ответом (представленным в классе **ProcessGuideResponse**). Ответ затем возвращается обратно в контейнер и передается обратно в традиционную логику, которая затем сериализует его в XML и отправляет ответ обратно на мобильное устройство.

Затем контроллеру нужно найти следующий шаг для выполнения. Если это начало нового процесса, контроллер выполнит вызов **initialStep()**, чтобы получить первый шаг процесса. После этого он вызовет метод **execute()** в **ProcessGuideStep**. Затем этот метод создает экземпляр класса **ProcessGuidePageBuilder** и вызывает **buildPage()**, который возвращается с объектом **ProcessGuidePage**, который является виртуальным представлением интерфейса пользователя, который будет представлен пользователю. Затем шаг отправляет результат обратно контроллеру, который затем сохраняет текущее состояние сеанса и возвращает результат обратно в **getNextFormState()** в форме класса **ProcessGuideResponse**. После этого ответ преобразовывается обратно в контейнер, а затем сериализуется в XML и отправляет ответ обратно на мобильное устройство.

Этот поток управления объясняется в следующей схеме последовательностей. Обратите внимание, что это наиболее распространенный поток управления, упрощенный для объяснения конструкции.

![Упрощенный поток управления.](media/control-flow.png)

Когда пользователь выполняет действие на мобильном устройстве нажатием кнопки (или сканируете значение — что обычно активирует действие по умолчанию) — запрос прибывает в методе **createResponse()** в классе **ProcessGuideController** по тому же самому маршруту. На этот раз, однако, контроллер знает информацию о состоянии сеанса, с которой пользователь находится на шаге. Соответственно, он создает экземпляр соответствующего класса **ProcessGuideStep** и вызывает метод выполнения. **ProcessGuideStep**, в свою очередь, считывает имя действия, вызванного пользователем, а затем создает соответствующий класс **ProcessGuideAction** и вызывает метод **execute()**.

Класс **ProcessGuideAction** отвечает за выполнение данного действия, но есть два важных исключения.

Первый из них — класс **ProcessGuideOKAction**. Это действие предполагает, что пользователь хочет подтвердить и перейти вперед в ходе процесса. В соответствии с этим данный метод фактически выполняет обратный вызов класса ProcessGuideStep, что означает, что шаг вызывает **processData()** в **ProcessGuideDataProcessor**. При этом будут обработаны данные, введенные пользователем, а затем обновлено состояние шага и отправлен результат обратно в контроллер. В зависимости от результата процессора, шаг вызывает конструктор страниц для создания соответствующего интерфейса пользователя или задает статус шага как завершенного. Это отражено в верхней половине схемы последовательностей ниже.

Другое исключение — это действие отмены, реализованное в классах **ProcessGuideCancelResetProcessAction** и **ProcessGuideCancelExitProcessAction**. Эти действия представляют собой цель отмены процесса и возврата в начало процесса или вообще завершения процесса. Аналогично действию **ОК** эти действия также выполняют обратный вызов шага, который сообщает в цели в **ProcessGuideController**. После этого контроллер выполняет необходимую очистку переменных состояния и либо переносит управление на начальный шаг процесса, либо завершает процесс совсем.

После завершения шага, если статус шага имеет значение **завершено**, контроллер создает экземпляр **ProcessGuideNavigationAgent**, который возвращает имя следующего шага. Затем контроллер создает экземпляр этого шага и вызывает метод **execute()** — и цикл продолжается. Чаще всего новый шаг вызывает соответствующий **ProcessGuidePageBuilder** для создания пользовательского интерфейса для следующего экрана, который будет представлен пользователю, который затем отправляется назад. Этот поток отражен в нижней половине схемы последовательностей ниже.

![Схема последовательностей.](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a>Создание нового процесса с помощью структуры ProcessGuide

Лучшим способом объяснения потока управления является использование примера, который существует в приложении — процесс запуска производства.

## <a name="overview-of-the-production-start-process"></a>Обзор процесса начала производства

Начнем с понимания потока процесса. На первом шаге пользователю предлагается ввести код производственного заказа.

![Запрос кода производства.](media/production-id-prompt.png)

Когда пользователь вводит код производственного заказа, номер заказа проверяется. Некоторые проверки выполняются в зависимости от того, находится ли заказ на том же складе, на котором пользователь вошел в систему, и статус заказа. Если проверка завершилась ошибкой, пользователь видит сообщение об ошибке. Если проверка выполнена успешно, пользователь видит сведения о производственном заказе и номенклатуре.

Пользователь может либо отменить, чтобы вернуться к началу процесса, либо нажать **ОК** для подтверждения. В последнем случае для производственного заказа устанавливается статус **Начато**, соответствующие журналы разносятся, элемент управления перемещается назад на первый шаг, а пользователю выводится сообщение "Работа завершена".


## <a name="creating-the-controller"></a>Создание контроллера

Первый шаг в создании бизнес-процесса заключается в создании класса контроллера, расширяемого из абстрактного класса **ProcessGuideController**, в котором реализовано поведение контроллера по умолчанию. Имя нового класса — **ProdProcessGuideProductionStartController**, со значением **WHSWorkExecuteMode** **StartProdOrder**. Используется создание экземпляра на основе **SysExtension**, что и в классах **WHSWorkExecuteDisplay**, что помогает создать экземпляр контроллера при выполнении пользователем пункта меню в этом режиме.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController
```

> [!NOTE]
> Шаблон именования класса — **\<FunctionalArea\>ProcessGuide\<Businessprocessname\>Controller**. Этот шаблон используется в классах контроллеров и расширяется до других классов.


## <a name="building-the-first-step"></a>Создание первого шага

Затем, чтобы определить первый шаг, вы создаете класс **ProdProcessGuidePromptProductionIdStep**, расширяя из **ProcessGuideStep**.

Задача создания экземпляра класса делегируется фабрике шагов, которая вызывается базовым классом **ProcessGuideController**. Реализация фабрики по умолчанию создает экземпляр шага на основе имени. Таким образом, чтобы создать экземпляр **ProdProcessGuidePromptProductionIdStep** как первый шаг контроллера, необходимо выполнить две вещи:

-   Снабдите класс **ProdProcessGuidePromptProductionIdStep** атрибутом **ProcessGuideStepName**.

    ```xpp
    [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
    ```

-   В классе контроллера реализуйте абстрактный метод **initialStepName()**, чтобы вернуть имя шага.

    ```xpp
    protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
    }
    ````   
    
> [!NOTE]
> Значение в атрибуте **ProcessGuideStepName** не должно точно совпадать с именем класса, как показано выше. Однако реализация этого позволяет при использовании класса использовать единообразие и безопасную типизацию в отношении перекрестных ссылок. Рекомендуется использовать это соглашение об именах.
>
> Создание экземпляра на основе **ProcessGuideStepName** реализовано в классе **ProcessGuideStepDefaultFactory**. В редких случаях, когда требуется другая стратегия создания экземпляра шага, необходимо выполнить следующие действия:
> -   Создайте новый класс фабрики, который наследуется из **ProcessGuidStepAbstractFactory**.
> -   При необходимости создайте новый класс параметров, реализующий интерфейс **ProcessGuideIStepCreationParameters**, содержащий необходимые параметры фабрики.
> -   В классе контроллера переопределяйте методы **stepFactory()** и **stepCreationParameters()**, чтобы вернуть вышеописанную фабрику и параметры.

Следующим шагом является реализация функций класса **ProdProcessGuidePromptProductionIdStep**. Необходимо реализовать логику для создания пользовательского интерфейса, обработки вводимых пользователем данных и определения времени выполнения шага.

### <a name="building-the-user-interface-for-the-first-step"></a>Создание пользовательского интерфейса для первого шага

Пользовательский интерфейс создается с помощью класса, который наследуется из абстрактного класса **ProcessGuidePageBuilder**. Для этого шага назовите класс, чтобы представить, что он делает — **ProdProcessGuidePromptProductionIdPageBuilder**.

Механизм создания экземпляров класса схож с порядком создания экземпляров этого шага из контроллера. 

-   Снабдите класс **ProdProcessGuidePromptProductionIdPageBuilder** атрибутом **ProcessGuidePageBuilderName**.

    ```xpp
    [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
    ```

-   В классе **ProdProcessGuidePromptProductionIdStep** реализуйте абстрактный метод **pageBuilderName()**, чтобы вернуть это имя.

    ```xpp
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
    }
    ```    

> [!TIP]
> Подобно фабрике шагов, имеется также абстрактный шаблон фабрики, реализованный для фабрики страниц. Поэтому в редких случаях, когда требуется другая стратегия создания экземпляра конструктора страниц, необходимо выполнить следующие действия:
> - Создайте новый класс фабрики, который наследуется из **ProcessGuidePageBuilderAbstractFactory**.
> - При необходимости создайте новый класс параметров, реализующий интерфейс **ProcessGuideIPageBuilderCreationParameters**, содержащий необходимые параметры фабрики.
> - В классе шага переопределяйте методы **pageBuilderFactory()** и **pageBuilderCreationParameters()**, чтобы вернуть вышеописанную фабрику и параметры.

Чтобы реализовать интерфейс пользователя, требуется страница с одним текстовым полем для ввода кода производственного заказа, а также кнопки **ОК** и **Отмена**. Кнопка **Отмена** должна выходить из процесса.

Чтобы реализовать это, необходимо переопределить два метода в классе **ProdProcessGuidePromptProductionIdPageBuilder**:

-   Чтобы добавить текстовое поле, используйте метод **addDataControls()**.

    ```xpp
    protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
    }
    ```   

-   Метод **addActionControls()** используется для добавления кнопок **ОК** и **Отмена**.

    ```xpp
    protected final void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
    }
    ``` 

При этом добавляются элементы управления данными, а затем — кнопки. Однако если требуется создать экран с элементами управления и кнопками с данными, можно переопределить метод **addControls()**, чтобы обеспечить гибкость.

В качестве дополнительного сценария следует подумать, как перестроить страницу в случае сбоев проверки, например, если пользователь вводит неправильный код производственного заказа. Базовый класс **ProcessGuidePageBuilder** реализует поведение по умолчанию, которое перестраивает интерфейс пользователя, отменяет отсканированное значение и добавляет элемент управления ошибки с сообщением об ошибке. Поскольку это поведение по умолчанию, которое необходимо использовать, нет необходимости добавлять код для обработки ошибок.

> [!TIP]
> Если требуется реализовать поведение пользовательского интерфейса для ситуаций с ошибками, можно переопределить один или несколько методов **rebuildFromRequestPage()**, **isErrorState()** и **reuseRequestPageOnError()**.

### <a name="processing-the-user-entered-data-in-the-first-step"></a>Обработка вводимых пользователем данных на первом шаге

Обработка данных выполняется в классе **ProcessGuideDataProcessorDefault**, который, в свою очередь, вызывает устаревший класс **WhsRfControlData**. Изменения данного поведения по умолчанию не требуются, и **WhsRfControlData** уже имеет логику для проверки поля **ProdId**, поэтому нет необходимости выполнять написание какой-либо логики для их обработки. В случае необходимости расширения для логики проверки следует использовать механизм расширения на основе **WhsControl**.

### <a name="determine-if-the-first-step-is-complete"></a>Определение того, завершен ли первый шаг

Когда проверка выполнена успешно, шаг помечается как завершенный. Это выполняется в базовом классе, однако необходимо реализовать условие, чтобы определить завершение шага. Это делает следующий переопределенный метод.

```xpp
protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
}
```   

### <a name="step-two-view-order-details-and-confirm"></a>Шаг 2. Просмотр сведений о заказе и подтверждение

На втором шаге процесса пользователь видит экран с подробными сведениями о заказе. Пользователь может нажать кнопку **ОК**, чтобы подтвердить запуск производственного заказа, либо нажать кнопку **Отмена**, чтобы вернуться к началу процесса. Для данного примера назовите шаг **ProdProcessGuideConfirmProductionOrderStep** и класс конструктора страниц **ProdProcessGuideConfirmProductionOrderPageBuilder**.

Класс ProdProcessGuideConfirmProductionOrderStep выглядит следующим образом:

```xpp
[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
}
```     

Поскольку пользователь не вводит никаких значений, нет необходимости переопределять метод **isComplete()**. Шаг завершается, когда пользователь нажимает кнопку **OK**.

Класс конструктора страниц переопределяет метод **addDataControls()**, добавляя три метки. Первая метка отображает код производственного заказа, вторая содержит сведения о номенклатуре (например, код номенклатуры, аналитики или описание), а третья содержит количество и единицу измерения.

**addActionControls()** затем переопределяется, добавляя две кнопки — кнопку **ОК** и кнопку **Отмена**, чтобы отменить процесс и вернуться к началу процесса.

```xpp
/// <summary>
/// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
/// and then confirm.
/// </summary>
[ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
{
    protected void addDataControls(ProcessGuidePage _page)
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;
        
        _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
        _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
        _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

        if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
        {
            _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
        }
    }

    protected void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelResetProcess));
    }
```

> [!NOTE]
> Один и тот же исходный код для методов X++ в этом разделе можно найти с помощью обозревателя приложений. Выполните фильтрацию по имени класса, а затем щелкните правой кнопкой мыши имя класса и выберите пункт **Просмотреть код**.

### <a name="step-3-start-the-production-order"></a>Шаг 3. Начало производственного заказа

Третий шаг заключается в том, чтобы выполнить бизнес-логику запуска производственного заказа. Этот шаг несколько отличается от предыдущих шагов, в этом случае у этого шага нет интерфейса пользователя. Этот шаг выполняется автоматически, когда пользователь нажимает кнопку **ОК** на предыдущем шаге.

Абстрактный класс **ProcessGuideStepWithoutPrompt** реализует поведение по умолчанию для таких шагов. Поэтому текущий шаг должен расширять класс **ProcessGuideStepWithoutPrompt** и переопределять метод **doExecute()**.

В следующем примере кода показано использование класса и реализации метода **doExecute()**. Метод просто извлекает код заказа и код пользователя из состояния сеанса и вызывает метод для запуска производственного заказа.

```xpp
/// <summary>
/// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
/// </summary>
[ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
{
    protected final void doExecute()
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        WhsWorkExecute workExecute = WhsWorkExecute::construct();
        workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

        this.addProcessCompletionMessage();

        super();
    }

}
```

В случае исключения логика обработки исключений структуры позволяет вернуть процесс к предыдущему шагу.

> [!NOTE]
> При вызове **addProcessCompletionMessage()** к параметрам навигации добавляется сообщение "Работа завершена". Следующий шаг (предполагая, что он имеет интерфейс пользователя) будет выводить это сообщение. Базовые классы обрабатывают эту логику, и для достижения этого поведения не требуется добавлять какой-либо специальный код в классы процессов.


### <a name="building-the-navigation-through-the-steps"></a>Создание навигации с помощью шагов

В базовом классе **ProcessGuideController** создается экземпляр класса **ProcessGuideNavigationAgentDefault**, который основывается на заранее определенном маршруте навигации, который представляет собой простое сопоставление исходных и целевых шагов. Для сценария запуска производства, поскольку не существует условного ветвления, эта реализация будет достаточной. Поэтому требуется переопределить только метод **initializeNavigationRoute()**, чтобы определить маршрут навигации.

```xpp
    protected ProcessGuideNavigationRoute initializeNavigationRoute()
    {
        ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
        navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

        return navigationRoute;
    }
```

Существуют процессы, в которых будет выполняться условное ветвление (на основе действий пользователя или каких-либо других условий). Такие процессы должны выполнять следующие действия:

-   Реализуйте отдельные агенты навигации, наследуемые из класса **ProcessGuideNavigationAgent**.

-   Реализуйте специальную фабрику агентов навигации, унаследованную от класса **ProcessGuideNavigationAgentAbstractFactory**, которая содержит логику для создания экземпляра правильного агента навигации на основе текущего шага, состояния сеанса, действия пользователя или другой логики.

-   При необходимости переопределяет **navigationAgentCreationParameters()** в классе контроллера, чтобы передать подходящие параметры.

-   Переопределите **navigationAgentFactory()** в контроллера для создания экземпляра созданной выше фабрики агента навигации.

### <a name="action-classes"></a>Классы действий

Классы действий представляют действия пользователя, поэтому в этом примере действие **ОК** используется для отображения способа создания действий.

```xpp
[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
}
```    

Класс должен реализовывать 2 абстрактных метода:

-   **label()**, который возвращает метку, которая должна отображаться в элементе управления кнопки, привязанном к данному действию.

-   **doExecute()**, который выполняет действие. Как упоминалось ранее, кнопка **ОК** просто выполняет обратный вызов этапа. Однако в этом случае другие действия могут иметь более сложную логику.

Экземпляры действий создаются с помощью структуры **SysExtension** на основе атрибута **ProcessGuideActionName**. Аналогично созданию экземпляров конструкторов страниц, класс шага реализует фабрику действий по умолчанию, и это может быть переопределено. Конструктор страниц добавляет элемент управления кнопки, подобно этому.

```xpp
_page.addButton(step.createAction(#ActionOK), true);
```

При этом он запрашивает у шага создание класса действия для переданного имени и связывает это действие с кнопкой.

### <a name="summary"></a>Сводка

Чтобы обобщить все, что было объяснено в этом разделе, приведем подробное описание кода, необходимого для этого процесса:

1.  **ProdProcessGuideProductionStartController**

    1.  Переопределите **initialStepName()** для указания имени первого шага.
    2.  Переопределите **initializeNavigationRoute()** для создания карты навигации.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideProductionStartController</c> class is the controller class for the production order start process guide.
        /// </summary>
        [WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
        public class ProdProcessGuideProductionStartController extends ProcessGuideController
        {
            protected ProcessGuideStepName initialStepName()
            {
                return classStr(ProdProcessGuidePromptProductionIdStep);
            }

            protected ProcessGuideNavigationRoute initializeNavigationRoute()
            {
                ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
                navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

                return navigationRoute;
            }

        }
        ```

2.  **ProdProcessGuidePromptProductionIdStep**

    1.  Переопределите **isComplete()**, чтобы указать, когда этап считается завершенным.
    2.  Переопределите **pageBuilderName()** для указания используемого конструктора страниц.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdStep</c> represents a step that 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))]
        public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
        {
            protected boolean isComplete()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);

                return (prodId != '');
            }

            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuidePromptProductionIdPageBuilder**

    1.  Переопределите **addDataControls()** для добавления текстового поля **Prod ID**.
    2.  Переопределите **addActionControls()** используется для добавления кнопок **ОК** и **Отмена**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdPageBuilder</c> class builds a page 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))]
        public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelExitProcess));
            }

        }
        ```

4.  **ProdProcessGuideConfirmProductionOrderStep**

    1.  Переопределите **pageBuilderName()** для указания используемого конструктора страниц.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderStep</c> class represents the step for viewing production order
        /// details and confirming the same.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
        public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
        {    
            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuideConfirmProductionOrderPageBuilder**

    1.  Переопределите **addDataControls()**, чтобы добавить метки сведений о заказе, номенклатуре и количестве.

    2.  Переопределите **addActionControls()** используется для добавления кнопок **ОК** и **Отмена**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
        /// and then confirm.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
        public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;

                _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
                _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
                _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

                if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
                {
                    _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
                }
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelResetProcess));
            }

        ```

        > [!NOTE]
        > Метод **generateItemInfoForProdId()**, который используется для создания меток сведений о номенклатуре, исключен из этого раздела. Этот метод запрашивает несколько таблиц для получения идентификатора, описания и аналитик номенклатуры. Если вы хотите лучше понять **generateItemInfoForProdId()**, взгляните на исходный код.

4.  **ProdProcessGuideStartProductionOrderStep**

    1.  Переопределите **doExecute()** для выполнения процесса запуска производства и добавления сообщения о завершении процесса.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
        public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
        {
            protected final void doExecute()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                WhsWorkExecute workExecute = WhsWorkExecute::construct();
                workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

                this.addProcessCompletionMessage();

                super();
            }

        }
        ```

> [!NOTE]
> Обратите внимание на то, что большое количество общих шаблонов (повторное создание пользовательского интерфейса при ошибке, задание сообщения о завершении процесса, поведение **ОК** и **Отмена**) были перемещены в структуру — таким образом, разработчик приложения не будет писать шаблонный код, подверженным ошибкам, и рисковать получить несогласованное поведение в процессах. Если сценарий должен отклоняться от общего пути, но разработчик приложения предоставляет возможность перекрытия подходящих методов — но тогда это является преднамеренным отклонением, которые одновременно являются явными и отслеживаемыми.


### <a name="extending-a-business-process"></a>Расширение бизнес-процесса

На данный момент в этой теме был выделен способ создания нового процесса с помощью структуры **ProcessGuide**. В этом заключительном разделе вы увидите несколько примеров того, как можно расширить этот бизнес-процесс.

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a>Добавление шага в потоке (с помощью ProcessGuideNavigationAgentDefault)

Где можно расширить:

-   Дочерний класс **ProcessGuideController** для процесса.

Как расширить:

-   Расширьте метод **initializeNavigationRoute()** в классе контроллера и вызовите **addFollowingStep()** в классе **ProcessGuideNavigationRoute**.

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a>Добавление шага в потоке (с помощью настраиваемого агента навигации)

Где можно расширить:

-   Дочерний элемент для **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent**.

Как расширить:

-   Создайте новый дочерний класс **ProcessGuideNavigationAgent**, который возвращает имя нужного шага.

-   Создайте новый класс, производный от **ProcessGuideNavigationAgentFactory**, в котором условно возвращается созданный ранее агент навигации.

-   Расширьте метод **navigationAgentFactory()** в классе контроллера для возврата созданной выше фабрики.

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a>Добавление нового элемента управления в пользовательский интерфейс существующего шага 

Где можно расширить:

-   Дочерний элемент для **ProdProcessGuidePageBuilder** для шага.

Как расширить:

-   Расширьте метод **addDataControls()** и добавьте дополнительный элемент управления.

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a>Выполнение реконструкции пользовательского интерфейса в существующем шаге

Где можно расширить:

-   Дочерний элемент для **ProdProcessGuideStep**.

Как расширить:

-   Создайте новый дочерний класс класса **ProdProcessGuidePageBuilder** и реализуйте желаемый пользовательский интерфейс.

-   Расширьте метод **pageBuildeName()** в классе шага, чтобы возвратить **ProcessGuidePageBuilderNameAttribute** для класса, созданного ранее.

### <a name="alter-logic-when-a-step-is-considered-complete"></a>Изменить логику после того, как этап считается завершенным

Где можно расширить:

-   Дочерний элемент для **ProdProcessGuideStep**.

Как расширить:

-   Расширьте метод **isComplete()** для создания дополнительной логики.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]