---
title: Настройка интерфейса выполнения производственного цеха
description: В этой статье описывается, как создать одну или несколько конфигураций для интерфейса выполнения производственного цеха. При открытии интерфейса выполнения производственного цеха он автоматически загружает выбранную конфигурацию и фильтр заданий, которые относятся к браузеру и устройству. В конфигурации задаются политики, которые должны быть применимы для конкретного использования.
author: johanhoffmann
ms.date: 11/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 641b293617df608bc07b97c077dbcd05664f8e2a
ms.sourcegitcommit: 4abf9b375fed6885ea11a425c524958fea29c3b9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748695"
---
# <a name="configure-the-production-floor-execution-interface"></a>Настройка интерфейса выполнения производственного цеха

[!include [banner](../includes/banner.md)]

Сотрудники производственного цеха используют интерфейс выполнения производственного цеха для регистрации своей ежедневной работы, например, когда они начинают задание, вводят обратную связь по заданиям, регистрируют дополнительные мероприятия и регистрируют отсутствие. Эти регистрации являются основой для отслеживания хода выполнения работ и затрат на производственные заказы и для расчета базиса для оплаты работников.

При открытии интерфейса выполнения производственного цеха он автоматически загружает выбранную конфигурацию и фильтр заданий, которые относятся к браузеру и устройству. В конфигурации задаются политики, которые должны быть применимы для конкретного использования. Далее приводятся некоторые примеры использования:

- На устройстве в холле компании сотрудники регистрируют время прихода на работу, когда они приходят в офис, и регистрируют уход в течение дня.
- На устройстве в цехе операторы машин регистрируют запуск и завершение заданий. Они также регистрируют перерывы и дополнительные мероприятия.

В этой статье описываются различные параметры для настройки интерфейса выполнения производственного цеха для каждого устройства, используемого на сайте.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Включение интерфейса выполнения производственного цеха и его связанных дополнительных функций

Сам интерфейс выполнения производственного цеха плюс несколько дополнительных параметров, описанных в этой статье, должны быть включены для системы, прежде чем их можно будет использовать. Используйте страницу [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для включения определенных или всех возможностей, описанных в следующих подразделах, как требуется.

### <a name="the-production-floor-execution-interface"></a>Интерфейс выполнения производственного цеха

Это основная функция, описываемая в этой статье, которая является необходимым условием для всех других функций, упоминаемых в этом разделе. В Supply Chain Management 10.0.25 она обязательна и не может быть отключена. При запуске версии, более старой, чем 10.0.25, администраторы могут включать или выключать эту функцию путем поиска функции *Выполнения производственного цеха* в рабочей области [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="generate-license-plates"></a>Создание грузомест

Эти функции делают доступными функции грузомест в интерфейсе выполнения производственного цеха. Если вы хотите использовать их, включите следующие функции в [управлении функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (в указанном порядке):

1. *Грузоместо для приемки добавлено в устройство карты задания*<br>(В Supply Chain Management версии 10.0.21 эта функция включена по умолчанию. В Supply Chain Management версии 10.0.25 эта функция обязательна.)
1. *Включение автоматического создания номерного знака при приемке на устройстве карты задания*<br>(В Supply Chain Management версии 10.0.25 эта функция обязательна.)

### <a name="print-labels"></a>Печать этикеток

Эти функции делают доступной функцию печати меток в интерфейсе выполнения производственного цеха. Если вы хотите использовать их, включите следующие функции в [управлении функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (в указанном порядке):

1. *Грузоместо для приемки добавлено в устройство карты задания*<br>(В Supply Chain Management версии 10.0.21 эта функция включена по умолчанию. В Supply Chain Management версии 10.0.25 эта функция обязательна.)
1. *Печать этикетки с устройства карты задания*<br>(В Supply Chain Management версии 10.0.25 эта функция обязательна.)

### <a name="allow-locking-the-touch-screen"></a>Разрешить блокировку сенсорного экрана

Эта функция позволяет разрешить работникам блокировать сенсорный экран, чтобы можно было выполнить его санитарную обработку.

В Supply Chain Management версии 10.0.21 эта функция включена по умолчанию. В Supply Chain Management 10.0.25 эта функция обязательна и не может быть отключена. При работе с версией, более ранней, чем 10.0.25, администраторы могут включать или выключать эту функцию путем поиска функции *Функция для блокировки устройства карты задания и терминала карты задания для дезинфекции* в рабочей области [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Функция управления активами для интерфейса выполнения производственного цеха

Эта функция добавляет вкладку управления активами в интерфейсе выполнения производственного цеха. Работники могут использовать эту вкладку для выбора актива, связанного с ресурсом оборудования, который находится в выбранном фильтре списка заданий. Для выбранного актива оборудования работник может просмотреть статус и работоспособность актива из значений счетчиков для максимум четырех выбранных счетчиков.

В Supply Chain Management версии 10.0.25 эта функция включена по умолчанию. В Supply Chain Management версии 10.0.29 эта функция обязательна и не может быть отключена. При запуске версии, более старой, чем 10.0.29, администраторы могут включать или выключать эту функцию путем поиска функции *Функция управления активами для интерфейса выполнения производственного цеха* в рабочей области [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="job-search"></a>Поиск заданий

Эта функция делает возможным добавление поля поиска в список заданий. Работники могут найти конкретное задание путем ввода кода задания или поиска всех заданий для конкретного заказа, вводя код заказа. Работники могут ввести код с помощью клавиатуры или путем сканирования штрих-кода.

В Supply Chain Management версии 10.0.25 эта функция включена по умолчанию. В Supply Chain Management версии 10.0.29 эта функция обязательна и не может быть отключена. При запуске версии, более старой, чем 10.0.29, администраторы могут включать или выключать эту функцию путем поиска функции *Поиск заданий для интерфейса выполнения производственного цеха* в рабочей области [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="report-on-co-products-and-by-products"></a>Отчет по сопутствующим и побочным продуктам

С помощью этой функции работники используют интерфейс выполнения производственного цеха для отчета о ходе выполнения заказов партий. Этот отчет включает отчетность по сопутствующим и побочным продуктам.

Чтобы использовать эту функцию, ее необходимо включить для системы. В Supply Chain Management версии 10.0.29 эта функция включена по умолчанию. Администраторы могут включать или выключать эту функцию путем поиска функции *Отчет о сопутствующих и побочных продуктах из интерфейса выполнения производственного цеха* в рабочей области [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="display-full-serial-batch-and-license-plate-numbers"></a>Отображение полных серийных номеров, номеров партий и номеров грузомест

Эта функция обеспечивает улучшенные возможности просмотра списков серийных номеров, номеров партий и грузомест в интерфейсе выполнения производственного цеха. Отображение изменяется из представления карточек, в котором отображается ограниченное число символов, на представление списка, которое обеспечивает достаточное количество свободного места для отображения всех значений. Список также предоставляет возможность поиска по указанным номерам.

Чтобы использовать эту функцию, ее необходимо включить для системы. В Supply Chain Management версии 10.0.25 эта функция включена по умолчанию. В Supply Chain Management версии 10.0.29 эта функция обязательна и не может быть отключена. Если используется версия старее 10.0.29, то администраторы могут включать или выключать эту функцию путем поиска функции *Показывать серийные номера, номера партии и номерные знаки полностью в интерфейсе выполнения производственного цеха* в рабочей области [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

В Supply Chain Management версии 10.0.25 эта функция включена по умолчанию. Администраторы могут включать или выключать эту функцию путем поиска функции *Finance or Supply Chain Management* в рабочей области [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="register-material-consumption"></a>Регистрация потребления материалов

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Эта функция позволяет сотрудникам использовать интерфейс выполнения производственного цеха для регистрации потребления материалов, номеров партий и серийных номеров. Некоторые производители, особенно в перерабатывающих отраслях, должны явным образом регистрировать количество материала, потребляемое для каждого партии или производственного заказа. Например, работники могут использовать весы для того, чтобы взвесить количество потребленного материала по мере их работы. Чтобы обеспечить полную трассировку материалов, эти организации также должны регистрировать номера партий, потребляемых для производства каждого продукта.

Существует две версии данной функции. Одна поддерживает только номенклатуры, для которых *не* включено использование процессов управления складом (WMS). Другая поддерживает номенклатуры, для которых *разрешено* использование WMS. Чтобы использовать эту функциональность, включите одну или обе из следующих функций в разделе [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (в указанном порядке), в зависимости от того, включены ли номенклатуры для WMS:

- *Регистрация потребления материалов в интерфейсе выполнения производственного цеха (без службы управления рабочими процессами)*
- *(Предварительная версия) Зарегистрировать потребление материалов в интерфейсе выполнения производственного цеха (с поддержкой службы управления рабочими процессами)*

> [!IMPORTANT]
> Можно использовать только функцию, не относящуюся к WMS. Однако при использовании WMS необходимо включить обе функции.

### <a name="report-on-catch-weight-items"></a>Отчет по номенклатурам, учитываемых в двух единицах измерения

Работники могут использовать интерфейс выполнения производственного цеха для отчета о ходе выполнения заказов партий для номенклатур, учитываемых в двух единицах измерения. Заказы партий создаются на основе формул, которые могут быть определены таким образом, чтобы они имели номенклатуры с учетом в двух единицах измерения в качестве номенклатур формул, сопутствующие продукты и побочные продукты. Формула также может быть определена для того, чтобы иметь строки формулы для ингредиентов, которые определены для учета в двух единицах измерения. Номенклатуры с учетом в двух единицах измерения используют две единицы измерения для отслеживания запасов: количество во вторичной единице измерения и количество запасов. Например, в пищевой промышленности мясо в коробках можно определить как номенклатуру с учетом в двух единицах измерения, где количество во вторичной единице измерения используется для отслеживания количества коробок, а количество запасов используется для отслеживания веса коробок.

Чтобы эта функциональность была доступна, включите следующую функцию в [управлении функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Отчеты по номенклатурам, учитываемым в двух единицах измерения, из интерфейса выполнения производственного цеха*

### <a name="the-my-day-dialog"></a>Диалоговое окно "Мой день"

Диалоговое окно **Мой день** предоставляет сотрудникам обзор ежедневных регистраций и текущих балансов для оплачиваемого времени, оплачиваемых сверхурочных, отсутствия и оплачиваемого отсутствия.

Чтобы использовать эту функцию, ее необходимо включить для системы. В Supply Chain Management версии 10.0.29 эта функция включена по умолчанию. Администраторы могут включать или выключать эту функцию путем поиска функции *Представление "Мой день" для интерфейса выполнения производственного цеха* в рабочей области [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="teams"></a>Рабочие группы

Если несколько сотрудников назначены одному производственному заданию, они могут сформировать рабочую группу. Рабочая группа может назначить одного работника в качестве руководителя. Остальные работники затем автоматически становятся помощниками для этого руководителя. Для получившейся рабочей группы только руководитель должен зарегистрировать статус задания. Записи времени применяются ко всем участникам рабочей группы.

Чтобы эта функциональность была доступна, включите следующую функцию в [управлении функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Производственные группы в интерфейсе выполнения производственного цеха*

### <a name="additional-configuration-in-the-production-floor-execution-interface"></a>Дополнительная настройка в интерфейсе выполнения производственного цеха

Эта функция добавляет параметры для следующей функциональной возможности на странице **Настроить управление производственным участком**:

- Автоматическое открытие диалогового окна **Запустить задание** после завершения поиска.
- Автоматическое открытие диалогового окна **Проверить ход выполнения** после завершения поиска.
- Предварительное заполнение оставшегося количества в диалоговом окне **Проверить ход выполнения**.
- Включение корректировок потребления материалов из диалогового окна **Проверить ход выполнения**. (Для этой функции также требуется функция *Регистрация потребления материалов в интерфейсе выполнения производственного цеха (без службы управления рабочими процессами)*.)
- Включить поиски по ИД проекта.

Сведения о том, как использовать эти параметры, приведены ниже в этой статье.

Чтобы эта функциональность была доступна, включите следующую функцию в [управлении функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Дополнительная настройка интерфейса выполнения производственного цеха*

### <a name="enable-the-my-jobs-tab"></a>Включение вкладки "Мои задания"

С помощью вкладки **Мои задания** работники могут легко просмотреть все неначатые и незаконченные задания, назначенные конкретно им. Это полезно в компаниях, где задания иногда или всегда назначаются отдельным сотрудникам (человеческим ресурсам), а не ресурсам других типов (например, машинам).

Чтобы эта функциональность была доступна, включите следующую функцию в [управлении функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Вкладка "Мои задания" в интерфейсе выполнения производственного цеха*

### <a name="enable-use-of-a-numpad-on-the-sign-in-page"></a>Включение цифровой панели на странице входа

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until 10.0.31 GA -->

Эта функция позволяет администраторам добавить элемент управления цифровой панели на страницу входа для интерфейса выполнения производственного цеха. Работники могут затем выполнять вход, используя цифровую панель для ввода кода с пропуска или личного номера.

Чтобы эта функциональность была доступна, включите следующую функцию в [управлении функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Включение цифровой панели на странице входа*

## <a name="work-with-production-floor-execution-configurations"></a>Работа с конфигурациями интерфейса выполнения производственного цеха

Для создания и настройки конфигураций выполнения производственного цеха перейдите в раздел **Управление производством \> Настройка \> Управление производством \> Настройка выполнения производства**. На странице **Настройка выполнения производственного цеха** отображается список существующих конфигураций. На этой странице можно выполнить следующие действия:

- Выберите любую конфигурацию производственного цеха, указанную в левом столбце, для просмотра и редактирования.
- На панели действий выберите **Создать**, чтобы добавить в список новую конфигурацию. Затем в поле **Конфигурация** введите имя, чтобы идентифицировать новую конфигурацию. Введенное имя должно быть уникальным для всех конфигураций, и его нельзя изменить позже. В поле **Описание** при необходимости можно ввести описание конфигурации.

Затем настройте различные параметры для выбранной конфигурации, как описано в следующих подразделах.

### <a name="the-general-fasttab"></a>Экспресс-вкладка "Общие"

На экспресс-вкладке **Общие** доступны следующие параметры:

- **Только время прихода и ухода** — установите для этого параметра значение *Да*, чтобы создать упрощенный интерфейс, обеспечивающий только функцию регистрации времени прихода и ухода. Этот параметр приведет к отключению большинства других параметров на этой странице. Прежде чем можно будет включить этот параметр, необходимо удалить все строки на экспресс-вкладке **Выбор вкладки**.
- **Включить поиск** — установите для этого параметра значение *Да*, чтобы включить поле поиска в список заданий. Работники могут найти конкретное задание путем ввода кода задания, или они могут найти все задания для конкретного заказа, введя код заказа. Работники могут ввести код с помощью клавиатуры или путем сканирования штрих-кода.
- **Включить поиск по ИД проекта** — установите для этого параметра значение *Да*, чтобы разрешить сотрудникам выполнять поиск по коду проекта (в дополнение к коду задания и коду заказа) в поле поиска в интерфейсе выполнения производственного цеха. Можно установить для этого параметра значение *Да* только в том случае, если для параметра **Включить поиск** также установлено значение *Да*.
- **Автоматически открывать диалоговое окно запуска** — если для этого параметра задано значение *Да*, диалоговое окно **Запустить задание** автоматически открывается, когда работники используют строку поиска для поиска задания.
- **Автоматически открывать диалоговое окно хода производства** — если для этого параметра задано значение *Да*, диалоговое окно **Проверить ход выполнения** автоматически открывается, когда работники используют строку поиска для поиска задания.
- **Включить корректировку материалов** — установите для этого параметра значение *Да*, чтобы включить кнопку **Корректировать материал** в диалоговом окне **Проверить ход выполнения**. Работники могут выбрать эту кнопку для корректировки потребления материалов для задания.
- **Сообщать о количестве на время ухода** — установите для этого параметра значение *Да*, чтобы сотрудникам выдавалось напоминание об указании обратной связи по выполняемым заданиям при регистрации времени ухода с работы. Если для этого параметра указано значение *Нет*, работники не будут получать запрос.
- **Блокировать сотрудника** — если этот параметр имеет значение *Нет*, работники будут выходить из системы сразу после того, как они выполняют регистрацию (например, новая должность). Затем интерфейс вернется на страницу входа. Если этот параметр задан как *Да*, работники остаются в системе на интерфейсе выполнения производственного цеха. Однако работник может выйти из системы вручную, чтобы другой работник мог войти в систему, пока интерфейс выполнения производственного цеха продолжает работать под одной и той же учетной записью пользователя системы. Для получения дополнительных сведений о учетных записей см. [Назначенные пользователи](config-job-card-device.md#assigned-users).
- **Использовать реальное время регистрации** — установите для этого параметра значение *Да*, чтобы задать время для каждой новой регистрации, равное точному времени, когда работник отправил регистрацию. Когда для этого параметра установлено значение *Нет*, вместо этого используется время входа в систему. Обычно для этого параметра устанавливается значение *Да*, если для параметра **Блокировать сотрудника** и/или **Один сотрудник** задано значение *Да*, когда работники часто остаются в системе в течение длительных периодов.
- **Один сотрудник** — установите для этого параметра значение *Да*, если только один работник использует каждый интерфейс выполнения производственного цеха, в котором активна данная конфигурация. Если для этого параметра задано значение *Да*, параметр **Блокировать сотрудника** автоматически задается как *Да*. Кроме того, этот параметр позволяет удалить требование (и возможность) для входа работника в систему с использованием кода значка работника (или аналогичного). Вместо этого работник выполняет вход в Microsoft Dynamics 365 Supply Chain Management с использованием учетной записи пользователя системы, связанной с *работником с зарегистрированным временем* (из таблицы *Работники*), и входит в интерфейс выполнения производственного цеха в качестве этого сотрудника в это же время.
- **Включить цифровую панель** — установите для этого параметра значение *Да*, чтобы добавить цифровую панель на экран входа, что позволяет сотрудникам вводить код пропуска или личный номер с помощью сенсорной цифровой панели. Установите для этого параметра значение *Нет*, чтобы скрыть цифровую панель.
- **Разрешить блокировку сенсорного экрана** — установите этот параметр как *Да*, чтобы разрешить работникам блокировать сенсорный экран интерфейса выполнения производственного цеха для санитарной обработки. Если этот параметр имеет значение *Да*, кнопка **Заблокировать экран для санитарной обработки** добавляется на страницу входа. Когда работник нажимает эту кнопку, сенсорный экран временно блокируется, чтобы исключить непредусмотренный ввод данных. Также отображается таймер обратного отсчета. После этого работник может спокойно очистить устройство и экран. После завершения обратного отсчета сенсорный экран автоматически разблокируется.
- **Длительность блокировки экрана** — когда для параметра **Разрешить блокировку сенсорного экрана** установлено значение *Да*, используйте этот параметр, чтобы задать количество секунд, в течение которого сенсорный экран должен блокироваться для санитарной обработки. Длительность должна быть в интервале от 5 до 120 секунд.
- **Создать грузоместо** — установите для этого параметра значение *Да*, чтобы создать новое грузоместо каждый раз, когда сотрудник использует интерфейс выполнения производственного цеха для приемки. Номер грузоместа создается на основе номерной серии, настроенной на странице **Параметры управления складом**. Если для этого параметра задано значение *Нет*, работники должны указать существующее грузоместо при приемке.
- **Печать этикетки** — установите этот параметр как *Да*, чтобы печатать этикетку грузоместа, когда работник использует интерфейс выполнения производственного цеха для приемки. Конфигурация метки настраивается в маршрутизации документа, как описано в разделе [Макеты этикеток маршрутизации документов](../warehousing/document-routing-layout-for-license-plates.md).

### <a name="the-tab-selection-fasttab"></a>Экспресс-вкладка "Выбор вкладки"

Параметры на экспресс-вкладке **Выбор вкладки** служат для выбора вкладок, которые должны отображаться интерфейсом выполнения производственного цеха, когда текущая конфигурация активна. Можно создать столько вкладок, сколько необходимо, а затем добавить и упорядочить их по мере необходимости с помощью кнопок на панели инструментов экспресс-вкладки. Информацию о разработке вкладок и работе с этими настройками см. в разделе [Разработка интерфейса выполнения производственного цеха](production-floor-execution-tabs.md).

### <a name="the-report-progress-fasttab"></a>Экспресс-вкладка "Проверить ход выполнения"

На экспресс-вкладке **Проверить ход выполнения** доступны следующие параметры:

- **Включить корректировку материалов** — установите для этого параметра значение *Да*, чтобы включить кнопку **Корректировать материал** в диалоговом окне **Проверить ход выполнения**. Работники могут выбрать эту кнопку для корректировки потребления материалов для задания.
- **Оставшееся количество по умолчанию** — установите для этого параметра значение *Да* для предварительного заполнения ожидаемого оставшегося количества для производственного задания в диалоговом окне **Проверить ход выполнения**.

## <a name="clean-up-job-configurations"></a>Очистка конфигураций заданий

Когда супервизор цеха настраивает интерфейс выполнения производственного цеха, он выбирает конфигурацию и фильтр заданий. Эти выбранные параметры хранятся в справочной таблице в Supply Chain Management, и браузер использует идентификатор, хранящийся в локальном файле cookie, чтобы найти правильную строку в этой таблице. В таблице также регистрируются дата и время последнего входа сотрудника в систему на каждом устройстве.

Пакетное задание периодически производит очистку записей в таблице ссылок для устройств, не зарегистрировавших каких-либо мероприятий за последние 60 дней. Можно также вручную очистить записи в любое время, выполнив следующие шаги:

1. Перейдите в раздел **Управление производством \> Настройка \> Выполнение производства \> Настройка выполнения производственного цеха**.
1. В области действий выберите **Очистить клиентские конфигурации**.
1. В диалоговом окне **Очистка конфигурации клиента** задайте в поле **Число дней** число дней отсутствия активности (до сегодняшнего дня) для рассмотрения. Будут удалены все конфигурации и записи входа для устройств, которые не были активны в течение этого времени.
1. Выберите **ОК**, чтобы очистить соответствующие конфигурации в соответствии с настройкой **Количество дней**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
