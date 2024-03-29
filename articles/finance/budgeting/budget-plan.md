---
title: Бюджетное планирование
description: Цель этой практической работы — обеспечить управляемое представление об обновлениях функций Microsoft Dynamics 365 Finance в области планирования бюджета. Смысл этой практической работы — проиллюстрировать быстрый пример настройки модуля бюджетного планирования и показать, как планирование бюджета может быть выполнено используя эта конфигурация.
author: panolte
ms.date: 06/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65ebfddb1baf39e20c22d3ed9bb26dbb33765e20
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712014"
---
# <a name="budget-planning"></a>Бюджетное планирование

[!include [banner](../includes/banner.md)]

Цель этой практической работы — обеспечить управляемое представление об обновлениях функций Microsoft Dynamics 365 Finance в области планирования бюджета. Смысл этой практической работы — проиллюстрировать быстрый пример настройки модуля бюджетного планирования и показать, как планирование бюджета может быть выполнено используя эта конфигурация.  Это практическое занятие сфокусируется специфически на следующих бизнес-процессах или задачах:
- Создание организационной иерархии для бюджетного планирования и настройка безопасности пользователей
- Определение сценариев бюджетного плана, столбцов бюджетного плана, макетов и шаблонов Excel
- Создание и активация процесс бюджетного планирования
- Создание документа бюджетного плана посредством получения фактических данных из главной книги
- Использование распределений для настройки данных документа бюджетного плана
- Редактирование данных документа бюджетного плана в Excel 

## <a name="prerequisites"></a>Необходимые условия 

В этом учебнике вы получите доступ к среде Microsoft Dynamics 365 Finance, используя демонстрационные данные Contoso, и получите роль администратора в экземпляре. Не используйте частный режим браузера для этого практического занятия. Выйдите из всех других учетных записей в браузере, если это необходимо, и войдите, используя учетные данные администратора. При входе **НЕОБХОДИМО** установить флажок "Оставаться в системе". В результате будет создан постоянный файл cookie, необходимый приложению Excel в данный момент. Если войти в приложение с помощью браузера, отличного от IE, отобразится запрос на вход в приложении Excel. При щелчке "Вход" в приложении Excel откроется всплывающее окно IE, и при входе **НЕОБХОДИМО** установить флажок "Оставаться в системе". Если при щелчке "Вход" в приложении Excel ничего не происходит, очистите кэш файлов cookie в IE.

## <a name="scenario-overview"></a>**Обзор сценария**
Julia работает менеджером по финансам в Contoso Entertainment Systems в Германии (DEMF). По мере приближения FY2016 ей нужно приступать к настройке бюджета компании на предстоящий год. Подготовка бюджета выглядит следующим образом:

1.  Julia использует фактические суммы предыдущего года как начальную точка для создания бюджета.
2.  На основании фактических сумм предыдущего года она создает оценки на 12 месяцев в предстоящем году.
3.  Julia пересматривает бюджет с финансовым директором. По завершении она вносит необходимые корректировки в бюджетный план и завершает подготовку бюджета.

Схема конфигурации бюджетного планирования для сценария выглядит следующим образом:

![Схема конфигурации планирования бюджета.](./media/screenshot1-300x152.png)

Julia использует следующий шаблон Excel для подготовки бюджета:

[![Шаблон Excel.](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

## <a name="exercise-1-configuration"></a>Упражнение 1. Конфигурация

### <a name="task-1-create-organizational-hierarchy"></a>**Задача 1. Создание организационной иерархии**
Поскольку весь процессе составления бюджета происходит в финансовом отделе, Julia должна создать очень простую организационную иерархию, состоящую только из финансового отдела. 

1.1. Перейдите в организационным иерархиям ("Администрирование организации" &gt; "Организации" &gt; "Организационные иерархии") и нажмите кнопку "Создать".

![Организационные иерархии.](./media/screenshot3.png) 

1.2. Введите имя для организационной иерархии в поле "Имя" и нажмите "Назначить цель".

1.3. Выберите цель бюджетного планирования, нажмите "Добавить" и назначьте новую организационную иерархию. 

[![Назначение цели.](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Повторите шаг выше для организационной цели "Безопасность". Закройте форму по завершении работы.

1.5. В форме "Организационные иерархии" нажмите "Просмотр". Щелкните "Правка" в конструкторе иерархии и создайте иерархию, нажав "Вставить".

[![Вставить.](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Выберите финансовый отдел для иерархии бюджетирования. 

[![Финансы.](./media/screenshot8.png)](./media/screenshot8.png)

1.7. По завершении нажмите "Опубликовать и закрыть". Выберите 1/1/2015 как дату вступления в силу для публикации иерархии.

[![Дата вступления в силу.](./media/screenshot9.png)](./media/screenshot9.png)

### <a name="task-2-configure-user-security"></a>Задача 2. Настройка безопасности пользователя
В бюджетном планировании используются специальные политики безопасности для настройки доступа к данным бюджетного плана. Julia нужно предоставить самой себе доступ к финансовым бюджетным планам. 

2.1. Переключитесь на контекст юридического лица DEMF. 


2.2. Перейдите в раздел "Бюджетирование" &gt; "Настройка" &gt; "Бюджетное планирование" &gt; "Конфигурация бюджетного планирования". На вкладке "Параметры" задайте для модели безопасности значение "На основе организаций безопасности". 

[![Параметры.](./media/screenshot11.png)](./media/screenshot11.png) 

2.3. Перейдите в раздел "Администрирование системы" &gt; "Пользователи" &gt; "Пользователи". Предоставьте пользователю "Администратор" (Julia Funderburk) роль "Менеджер бюджета". 

[![Менеджер бюджета.](./media/screenshot12.png)](./media/screenshot12.png) 

2.4. Выберите роль пользователя и щелкните "Назначить организации". 

[![Назначить организации.](./media/screenshot13.png)](./media/screenshot13.png)

2.5. Выберите "Предоставить доступ к определенным организациям". Выберите организационную иерархию, созданную на первом шаге. Выберите узел "Финансы" и нажмите кнопку "Предоставить с дочерними". 

***Важно!** _ _Убедитесь, что вы находитесь в контексте юридического лица DEMF при выполнении этой задачи, поскольку организационная безопасность применяется для юридического лица* 

### <a name="task-3-create-scenarios"></a>Задача 3. Создание сценариев
3.1. Перейдите в раздел "Бюджетирование" &gt; "Настройка" &gt; "Бюджетное планирование" &gt; "Конфигурация бюджетного планирования". В странице "Сценарии" обратите внимание на сценарии, которые мы будем использовать далее в этом практическом занятии: "Фактические показатели предыдущего года" и "Бюджетные". 

*Примечание. Вы можете создать новые сценарии для этого практического занятии при желании и использовать их.* 

[![Новые сценарии.](./media/screenshot15.png)](./media/screenshot15.png) 

*Примечание. Поскольку Julia не использует формальный процесс утверждения для подготовки бюджета, мы пропустим настройку элементов "Workflow-процессы", "Стадии" и "Стадии workflow-процесса" в этом практическом занятии и будем использовать существующую настройку для автоматического утверждения workflow-процесса. См. приложение для этой конфигурации workflow-процесса.*

### <a name="task-4-create-budget-plan-columns"></a>Задача 4. Создание столбцов бюджетного плана
Столбцы бюджетного плана основаны либо на денежной сумме, либо на количестве и могут использоваться в макете документа бюджетного плана. В нашем примере нам нужно создать столбец для фактических сумм предыдущего года и 12 столбцов для представления каждого месяца в бюджетном году. Чтобы создать столбцы, нажмите кнопку "Добавить" и заполните значение или используйте информационный объект. В этом практическом занятии мы будем использовать информационный объект для заполнения значений. 

4.1. В разделе "Бюджетирование" &gt; "Настройка" &gt; "Бюджетное планирование" &gt; "Конфигурация бюджетного планирования" откройте страницу "Столбцы". Нажмите кнопку Office в правом верхнем углу формы и выберите "Столбцы (неотфильтровано)". 

[![Столбцы не отфильтрованы.](./media/screenshot16.png)](./media/screenshot16.png) 

4.2. Система откроет книгу Excel, которая будет использоваться для заполнения значений. Если отобразится запрос, щелкните "Разрешить изменение" и "Доверять этому приложению". 

4.3. Нам потребуется больше столбцов для заполнения значений. Щелкните "Проектирование" на панели справа, чтобы добавить столбцы в сетку. 

[![Проектирование.](./media/screenshot19.png)](./media/screenshot19.png) 

4.4. Нажмите кнопку маленького карандаша рядом с PlanColumns, чтобы просмотреть доступные столбцы для добавления в сетку. 

[![Изменить.](./media/screenshot20.png)](./media/screenshot20.png) 

4.5. Дважды щелкните каждое доступное поле, чтобы добавить его в область "Выбранные поля" и нажмите кнопку "Обновить". 

4.6. В таблице Excel добавьте все столбцы, которые нужно создать. Используйте функцию AutoFill в Excel, чтобы быстро добавить строки. Убедитесь, что строки добавляются как часть таблицы (при использовании вертикальной прокрутки вверху сетки должны отображаться заголовки столбцов). 

4.7. Вернитесь в приложение и обновите страницу. Опубликованные значения отобразятся. 

[![Обновить.](./media/screenshot23.png)](./media/screenshot23.png)

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Задача 5. Создайте макеты и шаблоны документов бюджетных планов
План определяет, как будут выглядеть строки документа бюджетного плана, когда пользователь открывает документ бюджетного плана. Также можно переключить макет для документа бюджетного плана, чтобы просмотреть те же данные под разными углами. Теперь, когда Julia определила столбцы для использования с документом бюджетного плана, ей нужно создать макет документа бюджетного плана, который будет выглядеть как таблица Excel, которую она использует для создания бюджетных данных (см. раздел "Обзор сценария" в этом практическом занятии) 

5.1. В разделе "Бюджетирование" &gt; "Настройка" &gt; "Бюджетное планирование" &gt; "Конфигурация бюджетного планирования" откройте страницу "Макеты". Создайте новый макет для записи "Ежемесячный бюджет":

-   Выберите набор аналитик MA+BU, чтобы включить счета ГК и бизнес-единицы в макет.
-   Перечислите все столбцы бюджетного плана, созданные на предыдущем шаге, в разделе "Элементы". Сделайте все фактические суммы за предыдущий год редактируемыми.
-   Нажмите кнопку "Описания", чтобы выбрать, в каких финансовых аналитиках должны отображаться описания в сетке.

[![Описания.](./media/screenshot24.png)](./media/screenshot24.png) 

На основании определения макета бюджетного плана можно создать шаблон Excel для использования как альтернативный способ редактирования данных бюджета. Поскольку шаблон Excel должен соответствовать определению макета бюджетного плана, вы не сможете изменить макет бюджетного плана после создания шаблона Excel, следовательно, эту задачу следует выполнять после определения всех компонентов макета. 

5.2. Для макета, созданного на шаге 5.1, нажмите кнопку "Шаблон" &gt; "Создать". Подтвердите предупреждающее сообщение. Чтобы просмотреть шаблон, щелкните "Шаблон" &gt; "Просмотр". 

*Примечание. Убедитесь, что выбрана команда "Сохранить как", и выберите место сохранения шаблона для его редактирования. Если пользователь выбирает "Открыть" в диалоговом окне без сохранения, внесенные в файл изменения не будут сохранены после закрытия файла.* 
[![Средство просмотра шаблонов.](./media/screenshot25.png)](./media/screenshot25.png) 

5.3. &lt; Дополнительный шаг&gt; Измените шаблон Excel, чтобы упростить его для использования: добавьте формулы итога, поля заголовков, форматирование и т. д. Сохраните изменения и отправьте файл в макет бюджетного плана, щелкнув "Макет" &gt; "Отправить". 


### <a name="task-6-create-a-budget-planning-process"></a>Задача 6. Создание процесса бюджетного планирования
Julia нужно создать и активировать новый процесс бюджетного планирования, объединив все настройки выше, чтобы начать вводить бюджетные планы. Процесс бюджетного планирования определяет, какие организации бюджетирования, workflow-процесс, макеты и шаблоны будут использоваться для создания бюджетных планов. 

6.1. Перейдите в раздел "Бюджетирование" &gt; "Настройка" &gt; "Бюджетное планирование" &gt; "Процесс бюджетного планирования" и создайте новую запись.

-   Процесс бюджетного планирования — Бюджетирование DEMF в FY2016
-   Бюджетный цикл — FY2016
-   Главная книга — DEMF
-   Структура счета по умолчанию — Manufacturing P&L
-   Организационная иерархия — выберите иерархию, созданную в начале практического занятия
-   Workflow-процесс бюджетного планирования — назначьте workflow-процесс "Автоматическое утверждение" для финансового отдела
-   В правилах и шаблонах стадии бюджетного планирования для каждой стадии бюджетного планирования workflow-процесса укажите, можно ли будет добавлять и изменять строки и какой макет должен использоваться по умолчанию

*Примечание. Вы можете создать дополнительные макеты документов и назначить их как доступные на стадии workflow-процесса бюджетного планирования, нажав кнопку "Альтернативные макеты".* 

[![Альтернативные макеты.](./media/screenshot27.png)](./media/screenshot27.png) 

6.2. Выберите "Действия" &gt; "Активировать", чтобы активировать этот workflow-процесс бюджетного планирования. 

[![Активировать.](./media/screenshot28.png)](./media/screenshot28.png)

## <a name="exercise-2-process-simulation"></a>Упражнение 2. Моделирование процесса

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Задача 7. Создание исходных данных для бюджетного плана из главной книги
7.1. Перейдите в раздел "Бюджетирование" &gt; "Периодические операции" &gt; "Создать бюджетный план на основе главной книги". Заполните параметры периодического процесса и нажмите "Создать". 

7.2. Перейдите в раздел "Бюджетирование" &gt; "Бюджетные планы", чтобы найти бюджетный план, созданный в процессе создания. 

[![Бюджетный план.](./media/screenshot30.png)](./media/screenshot30.png) 

7.3. Откройте сведения о документе, перейдя по гиперссылке номера документа. Бюджетный план отобразится как определено в макете, созданном в ходе этого практического занятия. 

[![Отображение бюджетного плана.](./media/screenshot31.png)](./media/screenshot31.png)

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Задача 8. Создание бюджета на текущий год на основании фактических сумм предыдущего года
Методы распределения можно использовать в бюджетном плане для простого копирования информации для бюджетных планов из одного сценария в другой, распределения их по периодам и распределения в аналитики. Мы будем использовать распределения для создания бюджета на текущий год на основании фактических сумм предыдущего года. 

8.1. Выберите все строки в сетке документа бюджетного плана и нажмите "Распределить бюджет". 

[![Все строки.](./media/screenshot32.png)](./media/screenshot32.png) 

8.2. Выберите метод распределения, ключ периода, исходный и целевой сценарии, затем нажмите кнопку "Распределить". 

[![Распределить.](./media/screenshot33.png)](./media/screenshot33.png)

Фактические суммы за предыдущий год будут скопированы в бюджет текущего года и распределены по периодам с помощью ключа периода "Кривая продаж". 

[![Кривая продаж.](./media/screenshot34.png)](./media/screenshot34.png)

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Задача 9. Корректировка документа бюджетного плана с помощью Excel и оформление документа
9.1. Нажмите кнопку "Лист", чтоб открыть содержимое документа в Excel.

9.2. После открытия книги Excel скорректируйте числа в документе бюджетного плана и нажмите кнопку "Опубликовать".

9.3. Вернитесь в документ бюджетного плана. Нажмите "Workflow-процесс" &gt; "Отправить", чтобы автоматически утвердить документ.

[![Автоматическое утверждение.](./media/screenshot37.png)](./media/screenshot37.png) 

По завершении workflow-процесса стадия документа бюджетного плана изменится на "Утверждено". [![Одобрено.](./media/screenshot38.png)](./media/screenshot38.png)

## <a name="appendix"></a>Приложение

### <a name="auto-approve-workflow-configuration"></a>Конфигурация workflow-процесса автоматического утверждения

A. Бюджетирование &gt; Настройка &gt; Бюджетное планирование &gt; Workflow-процессы бюджетирования. Создание нового workflow-процесса с помощью шаблона "Workflow-процессы планирования бюджета":

[![Создание нового бизнес-правила.](./media/screenshot39.png)](./media/screenshot39.png)

Этот workflow-процесс содержит только одну задачу: "Бюджетный план перехода между стадиями". 

[![Бюджетный план перехода между стадиями.](./media/screenshot40.png)](./media/screenshot40.png) 

Сохраните и активируйте workflow-процесс. 

B. Перейдите в раздел "Бюджетирование" &gt; "Настройка" &gt; "Бюджетное планирование" &gt; "Конфигурация бюджетного планирования". На вкладке "Стадии" создайте 2 стадии: "Исходная" и "Отправлено". 

[![Исходная и отправлено.](./media/screenshot41.png)](./media/screenshot41.png)

C. Перейдите в раздел "Бюджетирование" &gt; "Настройка" &gt; "Бюджетное планирование" &gt; "Конфигурация бюджетного планирования". На вкладке "Стадии workflow-процесса" свяжите workflow-процесс автоматического утверждения, созданный на шаге A, со стадиями "Исходная" и "Отправлено".

[![Бюджетирование и планирование бюджета.](./media/screenshot42.png)](./media/screenshot42.png)  





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
