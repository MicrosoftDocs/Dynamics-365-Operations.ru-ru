---
title: Распределенное управление заказами (DOM)
description: В этой статье описывается функция распределенного управления заказами (DOM) в Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/16/2022
ms.topic: index-page
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.openlocfilehash: cfb89544580141ed397d27886f51fd0f1ac138d2
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785191"
---
# <a name="distributed-order-management-dom"></a>Распределенное управление заказами (DOM)

[!include [banner](includes/banner.md)]

В этой статье описывается функция распределенного управления заказами (DOM) в Microsoft Dynamics 365 Commerce.

DOM — это многоканальное решение оптимизации выполнения заказов, которое помогает максимально повысить эффективность выполнения заказов в цепочке поставок. DOM помогает гарантировать, что продукты будут доставлены клиентам в правильных количествах, из правильных источников и в правильное время. DOM также может помочь максимально увеличить прибыль, свети к минимуму затраты и выполнить требования на уровне обслуживания.

DOM использует частично-целочисленное программирование (MIP) и модели прогнозного анализа для выполнения оптимизации как на уровне партии, так и на уровне отдельных заказов. Эта возможность позволяет предприятиям розничной торговли использовать определенные правила для балансировки множества конфликтующих потребностей выполнения заказов. В современной сети поставок, в которой выполнение продуктов может осуществляться из нескольких каналов, организации должны быстро адаптироваться к изменениям заказов, проблемам с доступностью поставщиков и пиковым скачкам спроса. DOM помогает максимально повысить эффективность выполнения заказов и находить правильные источники для поставки продуктов на основе бизнес-ограничений и целей, таких как сведение к минимуму затрат путем выполнения заказов из ближайших источников. DOM использует расстояние между источниками выполнения продуктов и назначениями отгрузки, коэффициенты затрат, которые определены как цели оптимизации, а также правила, которые определены как ограничения, например запасы в узлах выполнения, для оптимизации выполнения заказов. DOM допускает определение нескольких профилей, которые позволяют компаниям выполнять различные стратегии оптимизации в зависимости от типа сегмента коммерческой деятельности или потребительского сегмента. 

На следующем рисунке показан жизненный цикл заказа на продажу в системе DOM.

![Жизненный цикл заказа на продажу в контексте DOM.](./media/flow.png "Жизненный цикл заказа на продажу в контексте DOM")

В следующем видеоролике представлен обзор возможностей DOM в Dynamics 365 Commerce.


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5bRYl]

## <a name="set-up-dom"></a>Настройка DOM

1. Перейдите в раздел **Администрирование системы \> Настройка \> Конфигурация лицензии**.
2. На вкладке **Конфигурационные ключи** разверните узел **Commerce** узел, а затем установите флажок **Распределенное управление заказами**.
3. Последовательно выберите **Retail и Commerce \> Распределенное управление заказами \> Настройка \> Параметры DOM**.
4. На вкладке **Общие** установите следующие значения.

    - **Включить распределенное управление заказами** — **Да**.
    - **Подтвердить использование карт Bing для DOM** — **Да**.

        > [!NOTE]
        > Для этого параметра можно установить значение **Да**, только если параметр **Включить карты Bing** на вкладке **Карты Bing** страницы **Общие параметры Commerce** (**Retail и Commerce \> Настройка центрального офиса \> Параметры \> Общие параметры Commerce**) также имеет значение **Да** и если в поле **Ключ карт Bing** указан действующий ключ.
        >
        > Портал [Центра разработки для карт Bing](https://www.bingmapsportal.com/) позволяет ограничить доступ к вашим ключам API карт Bing до набора доменов, которые вы указали. С помощью этой функции клиенты могут определить строгий набор значений источников данных или диапазонов IP-адресов, по которым будет выполняться проверка ключа. Запросы, поступающие из списка разрешений, обрабатываются обычным образом, в то время как запросы извне будут возвращать ответ "отказано в доступе". Добавление безопасности домена к ключу API не является обязательным, и ключи, оставленные как есть, будут продолжать работать. Список разрешений для ключа не зависит от других ключей, что позволяет установить различные правила для каждого из ключей. Распределенное управление заказами не поддерживает настройку свойств, связанных с доменом.

    - **Период хранения в днях** — укажите, как долго в системе должны сохранять планы выполнения, сгенерированные при запуске модели DOM. Пакетное задание **Настройка задания удаления данных выполнения DOM** удаляет все планы выполнения, созданные ранее указанного здесь числа дней.
    - **Период отклонения (в днях)**  — укажите, сколько времени должно пройти, прежде чем отклоненную строку заказа можно будет назначить той же точке выполнения.

5. На вкладке **Решатель** установите следующие значения.

    - **Максимальное число попыток автоматического выполнения** — укажите, сколько раз система DOM будет обработать строку заказа с помощью конкретной точки выполнения. Если обработать строку заказа с помощью системы DOM за указанное число раз не удастся, эта строка будет помечена как исключение. После этого строка будет пропускаться, пока ее статус не будет изменен вручную.
    - **Радиус области локального магазина** — введите значение. Это поле помогает определить, как точки выполнения группируются, чтобы считаться одинаковыми с точки зрения расстояния. Например, если ввести в это поле значение **100**, то каждый магазин или центр распределения в пределах 100 миль от адреса выполнения, будет считаться одинаковым по расстоянию.
    - **Тип решателя** — выберите значение. В Commerce доступно два типа решателя: **Рабочий решатель** и **Упрощенный решатель**. Для всех компьютеров, которые используются DOM (все серверы, входящие в группу DOMBatch) , следует выбирать **Рабочий решатель**. Для рабочего решателя требуется специальный лицензионный ключ, который по умолчанию развертывается в производственных средах. В более новых средах уровня 2+ рабочий решатель уже будет включен. Для непроизводственных сред этот лицензионный ключ необходимо развертывать вручную. Чтобы развернуть лицензионный ключ вручную, выполните следующие действия.

        1. В Microsoft Dynamics Lifecycle Services откройте общую библиотеку активов, выберите тип актива **Модель** и загрузите файл **лицензии DOM**.
        1. Запустите диспетчер служб Microsoft IIS, щелкните правой кнопкой мыши **Веб-сайт AOSService** и выберите **Обзор**. В проводнике будет открыто окно папки **\<AOS service root\>\\webroot**. Запишите или скопируйте путь \<AOS Service root\>, поскольку он понадобится на следующем шаге.
        1. Скопируйте файл конфигурации в папку **\<AOS Service root\>\\PackagesLocalDirectory\\DOM\\bin**.
        1. Перейдите в клиент Headquarters и откройте страницу **Параметры DOM**. На вкладке **Решатель** в поле **Тип решателя** выберите **Рабочий решатель** и убедитесь, что никакие сообщения об ошибках не появляются.

        > [!NOTE]
        > Упрощенный решатель позволяет познакомиться с функциями DOM без развертывания специальной лицензии. Организации не должны использовать упрощенный решатель в рабочих средах.
        >
        > Рабочий решатель повышает производительность (например, число обрабатываемых за один раз заказов или строк заказов) и оптимальность результатов (поскольку в некоторых случаях результаты для пакета заказов могут отличаться от оптимальных). Правило **Частичных заказов** требует наличия рабочего решателя.

6. Снова выберите **Retail и Commerce \> Распределенное управление заказами \> Настройка \> Параметры модели DOM**.
7. На вкладке **Номерные серии** назначьте нужные номерные серии различным объектам DOM.

    > [!NOTE]
    > Чтобы это можно было сделать, необходимо предварительно определить номерные серии на странице **Номерные серии** (**Управление организацией \> Номерные серии \> Номерные серии**).

8. Функция DOM поддерживает определение различных типов правил DOM, и организация может несколько правил в зависимости от своих бизнес-потребностей. Правила DOM можно определить для группы точек выполнения или отдельных точек выполнения, а также для конкретных продуктов, категорий продуктов и вариантов. Чтобы создать группировку точек выполнения для правил DOM, выполните следующие действия.

    1. Выберите **Retail и Commerce \> Настройка канала \> Группы выполнения**.
    2. Выберите **Создать**, а затем введите название и описание новой группы.
    3. Нажмите **Сохранить**.
    4. Выберите **Добавить строку**, чтобы добавить в группу отдельную точку выполнения. Чтобы добавить несколько точек местонахождения, выберите **Добавить строки**.

    > [!NOTE]
    > В Commerce версии 10.0.12 и выше должна быть включена **Возможность указывать местонахождения в качестве точек "Отгрузка" или "Отправка", включенная в группе выполнения** в рабочей области **Управление функциями**.
    >
    > Эта функция позволяет добавлять новые конфигурации на странице **Группа выполнения**, чтобы можно было указать, что склад можно использовать для отгрузки или что сочетание склад/магазин можно использовать для отгрузки, отправки или и того, и другого. 
    >
    > Если эта функция включена, параметры, доступные для выбора местонахождения при создании заказов на отправку или отгрузку в POS будут обновлены.
    >
    > Включение этой функции также приводит к обновлению страниц в POS-терминале, когда выбраны операции "Отгрузить все" или "Отгрузить выбранные".

9. Чтобы определить правила, выберите **Retail и Commerce \> Распределенное управление заказами \> Настройка \> Управление правилами**. В настоящее время поддерживаются следующие правила DOM.

    - **Правило минимальных запасов** — это правило позволяет организации резервировать определенное количество продукта для целей, отличных от выполнения заказов. Например, можно сделать так, чтобы система DOM учитывала при выполнении заказов не все запасы, находящиеся на складе, чтобы часть запасов оставалась для посетителей обычных магазинов. Если используется такое правило, вы можете определить минимальные запасы для категории продуктов, конкретного продукта или варианта продукта в конкретной точке выполнения или группе точек. Также можно определить минимальное количество запасов с помощью иерархии дополнительных категорий. Если продукт входит в несколько категорий, дополнительная категория имеет наивысшую важность для всех правил, в которых можно использовать категории.
    - **Правило для приоритета точки выполнения** — это правило позволяет организации определять иерархию приоритета точек выполнения, которая будет использоваться при выполнении системой DOM заказов конкретных продуктов. Допустимый диапазон приоритетов: от 1 до 10, где 1 — самый высокий, а 10 — самый низкий приоритет. Точки выполнения с более высоким приоритетом рассматриваются в первую очередь. Если правило установлено как жесткое ограничение, заказы выполняются только из тех точек выполнения, которые заданы в правиле. DOM отдает предпочтение отгрузке заказов полностью из одного местонахождения. Таким образом, если весь заказ и его строки недоступны для отгрузки из местонахождения с приоритетом 1, DOM попытается выполнить заказ из местонахождения с приоритетом 2.
    - **Правило для частичных заказов** — в Retail версии 10.0.5 параметр **Выполнить заказ только с одного склада** был заменен на **Максимум складов для выполнения**. Старый параметр позволял пользователям указывать, могут ли заказы выполняться только из одного местонахождения или из максимально возможного количества местонахождений. Новый параметр позволяет пользователям указывать, можно ли выполнять заказы из определенного набора местонахождений (не более пяти) или из максимально возможного количества местонахождений. Для всех параметров, за исключением выполнения из одного местонахождения, DOM разделяет строку, поскольку обработка заказа выполняется по строкам. Это правило применимо только для рабочего решателя.
    - **Правило для офлайн-точки выполнения заказов** — это правило позволяет организации задать склад или группу складов в качестве офлайн-точек выполнения или сделать их недоступными для модели DOM, чтобы заказы не назначались этим складам.
    - **Правило максимального числа отклонений** — это правило позволяет организации определять порог отклонений. По достижении этого порога система DOM помечает заказ или строку заказа как исключение и больше не обрабатывает. Для обеспечения производительности DOM не будет просматривать историю всех отклонений. 

        После назначения строк заказа определенной точке выполнения эта точка выполнения может отклонить назначенную строку, если по тем или иным причинам выполнение заказа в ней невозможно. Отклоненные строки помечаются как исключения и возвращаются в общий пул для обработке при следующем запуске. При следующем запуске система DOM пытается назначить отклоненную строку другой точке. Новая точка может также отклонить назначенную строку заказа. Этот цикл назначения и отклонения может повториться несколько раз. По достижении порога отклонения система DOM пометит строку заказа ка постоянное исключение и больше не будет пытаться ее назначать. Строка может быть заново назначена, только если пользователь вручную изменит ее статус.

    - **Правило максимального расстояния** — это правило позволяет организации определить максимальное расстояние, на котором может находиться точка или группа точек выполнения. Если для точки выполнения заданы пересекающиеся правила максимального расстояния, система DOM будет использовать то из них, в котором задано меньшее расстояние.
    - **Правило максимума заказов** — это правило позволяет организации определить максимальное количество заказов, которое может быть обработано в точке или группе точек выполнения. В процессе оптимизации система будет учитывать заказы, которые не были отгружены из этих местонахождений. Эта проверка выполняется по профилям. Таким образом, если перекрывающиеся максимальные количества заказов определяются по профилям для одного и того же местонахождения, в системе будет учитываться максимальное количество заказов, определенное по всем профилям. 

    Ниже перечислены некоторые общие атрибуты, которые обычно задаются для всех описанных выше правил.

    - **Дата начала** и **Дата окончания** — с помощью этих полей можно ввести даты вступления в силу каждого правила.
    - **Отключено** — система DOM учитывает только те правила, у которых в этом поле установлено значение **Нет**.
    - **Жесткое ограничение** — правила можно определять в качестве жестких и нежестких ограничений. Каждый запуск DOM проходит через два этапа. На первом этапе каждое правило считается жестким ограничением независимо от состояния этого поля. Иными словами, применяются все правила. Единственное исключение — правило **Приоритет точки**. На втором этапе правила, которые не были выбраны в качестве жестких, исключаются, и происходит назначение ранее не назначенных заказов и строк заказов.

10. Профили выполнения служат для группировки коллекций правил, юридических лиц, происхождений заказов на продажу и режимов доставки. В каждом запуске DOM обрабатывается только один профиль выполнения. Поэтому организация может определить набор правил для отдельной группы юридических лиц, для заказов с определенным происхождением и с определенным режимом доставки. Если к разным наборам происхождений заказов на продажу или режимам доставки нужно применять разные правила, можно определить несколько профилей выполнения. Чтобы настроить профили выполнения, сделайте следующее.  

    1. Выберите **Retail и Commerce \> Распределенное управление заказами \> Настройка \> Профили выполнения**.
    2. Выберите **Создать**.
    3. Заполните поля **Профиль** и **Описание**.
    4. Задайте параметр **Результат автоматического применения**. Если задать для этого параметра значение **Да**, результаты запуска DOM для профиля будут автоматически применены к строкам заказов на продажу. Если задать значение **Нет**, результаты можно будет просматривать только в плане выполнения. Они не будут применены к строкам заказов на продажу.
    5. Если профиль DOM (распределенное управление заказами) должен применяться к заказам на продажу с любым происхождением, в том числе если происхождение не определено, установите для параметра **Обработать заказы с пустым происхождением заказа на продажу** значение **Да**. Чтобы применить профиль только к заказам с определенным происхождением, воспользуйтесь страницей **Происхождение заказов**, как описано ниже.

        > [!NOTE]
        > В выпуске Commerce версии 10.0.12 и выше должна быть включена функция **Возможность назначить группу выполнения профилю выполнения** в рабочей области **Управление функциями**. Эта функция позволяет указать список складов, которые должны учитываться в DOM при оптимизации с использованием профиля выполнения. Если этот список складов не указан, DOM будет учитывать все склады в юридических лицах, которые определены в профиле.
        >
        > Эта функция добавляет новую конфигурацию на странице **Профиль выполнения**, которая может быть связана с одной группой выполнения. 
        >
        > Если выбрана группа выполнения, правила DOM (распределенное управление заказами) для этого профиля выполнения будут эффективно выполняться на складах "Отгрузка", входящих в группу выполнения. 
        > 
        > Для эффективного использования этой функции убедитесь, что есть одна группа выполнения, содержащая все склады отгрузки, а затем свяжите эту группу выполнения с профилем выполнения.

    6. На экспресс-вкладке **Юридические лица** нажмите **Добавить**, а затем выберите юридическое лицо.
    7. На экспресс-выберите **Правила** нажмите **Добавить**, а затем выберите правило, которое нужно связать с профилем.
    8. Повторяйте эти два шага, пока в профиль не будут добавлены все нужные правила.
    9. Нажмите **Сохранить**.
    10. В области действий откройте вкладку **Настройка** и выберите **Режимы доставки**.
    11. На странице **Режимы доставки** нажмите **Создать**.
    12. В поле **Компания** выберите юридическое лицо. Вы можете выбирать только из тех компаний, которые добавили ранее.
    13. В поле **Режим доставки** выберите режим доставки, который будет связан с этим профилем. Один режим доставки невозможно связать с несколькими активными профилями.
    14. Повторяйте эти два шага, пока с профилем не будут связаны все нужные режимы доставки.
    15. Закройте страницу **Режимы доставки**.
    16. В области действий откройте вкладку **Настройка** и выберите **Происхождения заказов на продажу**.
    17. На странице **Происхождения заказов на продажу** нажмите **Создать**.
    18. В поле **Компания** выберите юридическое лицо. Вы можете выбирать только из тех компаний, которые добавили ранее.
    19. В поле **Происхождение заказа на продажу** выберите происхождение, которое нужно связать с этим профилем. Одно происхождение заказов на продажу нельзя связать с несколькими активными профилями.
    20. Повторяйте эти два шага, пока в профиль не будут добавлены все нужные происхождения заказов на продажу.
    21. Закройте страницу **Происхождения заказов на продажу**.
    22. Для параметра **Включить профиль** выберите значение **Да**. Если в конфигурации есть ошибки, появится предупреждение.

## <a name="dom-processing"></a>Обработка DOM

DOM запускается только в рамках пакетных заданий. Чтобы настроить пакетное задание для DOM, выполните следующие действия.

1. Выберите **Retail и Commerce \> Распределенное управление заказами \> Пакетная обработка \> Настройка задания обработчика DOM**.
1. На экспресс-вкладке **Параметры** в поле **Профиль выполнения** выберите профиль, для которого нужно запустить DOM.
1. На экспресс-вкладке **Выполнять в фоновом режиме** в поле **Группа пакетов** выберите настроенную группу пакетов.
1. В поле **Описание задачи** введите наименование пакетного задания.
1. Выберите **Повторение** и определите режим повторного запуска пакетного задания.
1. Нажмите **ОК**.

Во время обработки система DOM будет учитывать заказы и строки заказов, указанные ниже.

- Строки заказов, удовлетворяющие заданным в профиле DOM критериям по происхождению, режимам доставки и юридическим лицам, а также следующим критериям:

    - созданы в каналах коммерческой деятельности;
    - никогда не обрабатывались DOM;
    - ранее обрабатывались DOM, но помечены как исключения, а максимальное число попыток еще не достигнуто;
    - режим доставки: не самовывоз и не электронный;
    - не отмечены для поставки;
    - не исключены вручную.

- Заказы, которые не заблокированы.

После применения правил, ограничений по запасам и оптимизации система DOM выберет точку выполнения, которая находится ближе всего к адресу поставки. DOM преобразует адреса типа **Поставка** в значения широты и долготы. Затем DOM преобразует адрес поставки в заказе на продажу в значения широты и долготы и обновляет значения широты и долготы адреса для использования в будущем. DOM зависит от карт Bing при определении точных значений широты и долготы на основе сведений об адресе, городе и почтовом индексе.

DOM использует API карт Bing для расчета расстояния по воздуху или по дороге в зависимости от параметров. Затем эта информация используется для определения стоимости отгрузки. Модель оптимизации отдает приоритет выполнению полного заказа из одного местонахождения. Даже если часть заказа доступна в одном городе или почтовом индексе, модель была оптимизирована для уменьшения количества отгрузок. 

DOM ищет доступные запасы путем просмотра запасов в наличии в объектах склада версии V2. Во время выполнения каждого пакетного задания DOM разделяет заказы на партии в зависимости от значения параметра **Обработчик DOM** для задач, определенных в профиле. Значение этого параметра по умолчанию — **2000**. Например, если 10 000 строк заказа оптимизированы в ходе выполнения и для параметра **Обработчик DOM** задано значение по умолчанию **2000**, DOM создает пять партий, которые обрабатываются одновременно. Планы выполнения затем извлекаются из оптимизатора и применяются к строке. Если строку заказа необходимо разделить между двумя местонахождениями, DOM обеспечивает соответствующее распределение цен и налогов по строкам.

![Критерии заказов на продажу.](./media/ordercriteria.png "Критерии заказов на продажу")

## <a name="results-of-dom-runs"></a>Результаты запуска DOM

Если в профиле выполнения установлен параметр **Автоматическое применение**, результаты выполнения будут автоматически применены к строкам заказов на продажу. План выполнения можно будет посмотреть отдельно. Если же в профиле выполнения параметр **Автоматическое применение** не установлен, результаты можно будет видеть только в представлении плана выполнения. 

Чтобы открыть все сформированные планы выполнения, выполните следующие действия.

1. Выберите **Retail и Commerce \> Распределенное управление заказами \> Распределенное управление заказами**.
2. В рабочей области **Распределенное управление заказами** выберите плитку **Планы выполнений**.
3. Выберите идентификатор нужного плана выполнения заказов.

    В разделе сведений о заказе представления плана выполнения можно видеть исходные строки заказа на продажу, для которых подготовлен план. Помимо стандартных полей строк заказа на продажу, в разделе сведений также приведены следующие три поля, связанные с DOM.

    - **Тип выполнения** — это поле показывает, была строка заказа обработана полностью, частично или вообще не обработана для конкретной точки выполнения.
    - **Разбиение** — это поле показывает, была ли строка заказа на продажу разбита между несколькими точками выполнения.
    - **Число точек выполнения** — это поле показывает, сколько строк выполнения было создано для одной строки заказа на продажу (в зависимости от числа точек выполнения, между которыми была разбита исходная строка заказа на продажу).

    В разделе сведений о выполнении можно видеть назначение исходных строк заказа на продажу разным точкам выполнения, а также соответствующие количества.

## <a name="order-line-actions-and-statuses"></a>Действия и статусы строк заказов

Ниже перечислены параметры строк заказов. Чтобы открыть строку заказа, выберите **Retail и Commerce \> Клиенты \> Все заказы на продажу**.

- Если для параметра **Исключить из обработки DOM** на вкладке **Общие** строки заказа на продажу выбрано значение **Да**, заказ или строка заказа не будут обрабатываться системой DOM.
- Поле **Статус DOM** на вкладке **Общие** строки заказа на продажу может иметь одно из следующих значений.

    - **Нет** — строка заказа никогда не обрабатывалась.
    - **Выполнено** — строка заказа успешно обработана и назначена точке выполнения.
    - **Исключение** — строка заказа обработана, не ее не удалось назначить точке выполнения. У исключений есть несколько подтипов, которые доступны в рабочей области DOM:

        - **Количество недоступно** — нет доступных запасов для назначения заказа точке выполнения;
        - **Максимальное число отклонений** — для строки заказа достигнуто максимальное число отклонений;
        - **Конфликт изменения данных** — строки заказа на продажу была изменен после обработки заказа DOM. Поэтому применить к заказу план выполнения невозможно;
        - **Исключение для конкретной строки заказа** — в строке заказа есть более одного исключения.

- Во время ввода заказа на продажу система DOM может работать интерактивном режиме. При вводе строки заказа после указания продукта и количества можно выбрать команду **Обновить строку**, а затем в разделе **DOM** выбрать **Предложить точку выполнения**. Будет открыт основанный на правилах DOM список точек выполнения, в которых возможно выполнение строки заказа с нужным количеством. Этот список будет отсортирован по расстоянию. Выберите точку выполнения (объект или склад) для строки заказа на продажу. Чтобы можно было пользоваться этой функцией, должен существовать активный профиль выполнения, соответствующий происхождению и режиму доставки строки заказа на продажу.
- Чтобы открыть журналы запуска DOM для строки заказа на продажу, выберите **строку заказа на продажу**, а затем в разделе **DOM** выберите **Просмотр журналов DOM**. В журналах DOM можно видеть все события и журналы, сформированные во время выполнения DOM. С их помощью вы можете лучше понять, какие точки выполнения были назначены конкретной строке заказа, а также какие правила и ограничения при этом учитывались. На вкладке **Управление** журналы DOM также доступны на уровне заголовка заказа на продажу.

## <a name="run-a-clean-up-job-for-dom-fulfillment-plans"></a>Запуск задания очистки для планов выполнения DOM

Во время работы системы DOM создаются планы выполнения. С течением времени в системе накапливается очень большое число таких планов. Для управления хранящимися в системе планами можно настроить пакетное задание, которое будет удалять старые планы в соответствии со значением **Период хранения в днях**.

1. Выберите **Retail и Commerce \> Распределенное управление заказами \> Пакетная обработка \> Настройка задания удаления данных выполнения DOM**. 
1. В поле **Группа пакетов** выберите настроенную группу пакетов.
1. Выберите **Повторение** и определите режим повторного запуска пакетного задания.
1. Нажмите **ОК**.

## <a name="more-information"></a>Дополнительные сведения

При использовании функции DOM следует учитывать следующие обстоятельства.

- В настоящее время система DOM обрабатывает только заказы, созданные в каналах коммерческой деятельности. Заказы на продажу считаются заказами на продажу, если параметр **Коммерческие продажи** в них имеет значение **Да**.
- Корпорация Майкрософт еще не протестирована DOM с расширенными процессами управления складом. Таким образом, клиенты и партнеры должны критически оценивать совместимость DOM с расширенными процессами управления складом. Расширенные складские процессы позволяют использовать настраиваемые аналитики, такие как статус запасов, которые не позволяют точно определить доступные запасы. DOM предоставляет расширяемый метод настройки доступных запасов для реализаций, использующих расширенные складские процессы. Его можно использовать для работы с настроенными значениями статуса запасов и других аналитик.

    Расширяемость в DOM ограничена, поскольку оптимизация выполняется во встроенной модели MIP, которая учитывает оптимизацию и ее ограничения. Для настройки оптимизации запасов и последующей обработки уже существует несколько расширяемых точек. Профили DOM могут отличаться по источнику продаж и режиму доставки. Основание заказа на продажу можно задать во время приема заказа, и на основе этих значений можно использовать другие стратегии оптимизации. DOM также поддерживает создание настраиваемых пакетных заданий, которые могут использовать задачу "Процессор DOM" в качестве входных данных и разрешать передачу профиля в качестве параметра. Таким образом, одну оптимизацию можно выполнить после другой для поддержки различных бизнес-сценариев.

- Система DOM доступна только для облачной версии Commerce. Она не поддерживается в локальных развертываниях.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
