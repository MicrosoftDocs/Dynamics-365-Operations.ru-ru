---
title: Приступая к работе с дополнительным компонентом электронных накладных для Бразилии
description: В этой теме приводятся сведения, которые помогут приступить к работе с дополнительным компонентом электронного выставления накладных для Бразилии в Microsoft Dynamics 365 Finance и Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6472672f5d618cc6d100298dd35939afa4c0066d
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2020
ms.locfileid: "3836027"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Приступая к работе с дополнительным компонентом электронных накладных для Бразилии 

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Дополнительный компонент электронных накладных для Бразилии в настоящее время не поддерживает все функции, доступные в интеграции финансовых документов, встроенной в Microsoft Dynamics 365 Finance и Dynamics 365 Supply Chain Management.

В этой теме приводятся сведения, которые помогут приступить к работе с дополнительным компонентом электронного выставления накладных для Бразилии. Она поможет выполнить этапы настройки, зависящие от страны или региона, в службах Regulatory Configuration Services (RCS) и в Finance и Supply Chain Management. Кроме того, в ней описывается процесс отправки финансового документа NF-e (модель электронного документа 55) через службу, а также объясняет порядок просмотра результатов обработки и статус финансовых документов.

## <a name="prerequisites"></a>Необходимые условия

Перед выполнением шагов, описанных в этой теме, необходимо выполнить шаги из раздела [Приступая к работе с дополнительным компонентом электронных накладных](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>Настройка RCS

Во время настройки RCS будут выполнены следующие задачи:

1. Импорт функции выставления электронных накладных для финансовых документов NF-e.
2. Проверка форматов файлов, необходимых для отправки финансовых документов NF-e для авторизации.
3. Проверка форматов файлов, которые необходимы для запроса отмены утвержденного NF-e.
4. Настройка события, необходимого для отправки финансовых документов NF-e для авторизации.
5. Настройка события, необходимого для запроса отмены утвержденного NF-e.
6. Назначение функции электронных накладных среде дополнения электронных накладных.
7. Опубликуйте функцию выставления накладных в электронной форме.

> [!NOTE]
> "Функция электронных накладных" — это универсальное имя для ресурса, который настраивается и публикуется для использования сервера дополнения электронных накладных. Настройка функции электронных накладных объединяет, помимо всего прочего, использование форматов конфигурации электронной отчетности для создания настраиваемых файлов экспорта и импорта и использования действий и потоков действий для разрешения создания настраиваемых правил для отправки запросов, импорта ответов и обработки содержимого ответов.

## <a name="import-the-e-invoicing-feature"></a>Импорт функции выставления накладных в электронной форме

1. Вход в учетную запись RCS
2. В рабочей области **Функции глобализации** в разделе **Функции** выберите плитку **Электронные накладные**.
3. На странице **Функции электронного выставления накладных** выберите **Импорт**, чтобы импортировать функцию электронных накладных финансовых документов NF-e из глобального репозитория.

    ![Кнопка "Импорт"](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. Выберите функцию финансовых документов NF-e, затем выберите **Импорт**.

    ![Импорт функции NF-e](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a>Создание новой версии функции финансовых документов NF-e

- На странице **Функции электронных накладных** на вкладке **Версии** выберите **Создать**.

![Добавление новой версии функции электронных накладных](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a>Обновление версии конфигурации

1. На странице **Функции электронного выставления накладных** на вкладке **Конфигурации** выберите **Добавить** или **Удалить** для управления версиями конфигураций (конфигурации формата файлов электронной отчетности).

    ![Управление конфигурациями функции электронных накладных](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - При создании новой версии функции финансовых документов NF-e все версии конфигурации (форматы файлов электронной отчетности) наследуются из последней версии.
    - Для отправки финансового документа NF-e для авторизации необходимы следующие версии конфигурации:

        - Формат экспорта отправки NF-e
        - Импорт ответного сообщения NF-e
        - Импорт журнала ошибок NF-e

    - Чтобы отправить отмену NF-e, требуется следующая версия конфигурации:

        - Формат экспорта отмены NF-e

2. В списке выберите версию конфигурации, а затем выберите **Правка** или **Просмотр**, чтобы открыть страницу **Конструктор форматов**, на которой можно изменить или просмотреть конфигурацию.

    ![Открытие страницы конструктора формата](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. Страница **Конструктор форматов** используется для изменения или просмотра конфигураций форматов файлов электронной отчетности. Дополнительные сведения см. в разделе [Создание конфигураций электронных документов](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Страница конструктора форматов](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a>Управление настройками функции электронных накладных

- На странице **Функции электронного выставления накладных** на вкладке **Настройки** выберите **Добавить** или **Удалить** для управления настройками функций электронных накладных (то есть, событий NF-e).

![Управление настройками функций электронных накладных](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

При создании новой версии функции финансового документа NF-e, которая является производной от другой функции электронных накладных, все настройки функций (событий NF-e) наследуются из последней версии.

Чтобы отправить финансовые документы NF-e для авторизации, требуется настройка функции **Отправить**.

Чтобы отправить отмену NF-e, требуется настройка функции **Отмена**.

#### <a name="configure-the-submit-feature-setup"></a>Задание настройки функции отправки

1. На странице **Функции электронного выставления накладных** на вкладке **Настройки** в столбце **Настройка функции** выберите **Отправить**.
2. Выберите **Правка**.

    ![Изменение настройки функции электронных накладных](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. На странице **Настройка версии функции** выберите вкладку **Действия** для управления списком действий.

    ![Вкладка "Действия"](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. Проверка действий, необходимых для отправки NF-e для авторизации.

    | Код действия | Имя действия                  | Описание действия                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | 1         | Преобразование документа           | Создание XML-файла NF-e для отправки.                          |
    | 2         | Подписать документ                | Применение цифрового сертификата к файлу XML.                    |
    | 3         | Вызов бразильской службы SEFAZ | Отправка подписанного файла XML в веб-службы для авторизации. |
    | 4         | Обработка ответа             | Получение ответа веб-службы.                                     |
    | 5         | Преобразование документа           | Анализ содержимого файла, полученного в качестве ответа.     |
    | 6         | Преобразование документа           | Создание XML-файла для запроса статуса отправки.    |
    | 7         | Вызов бразильской службы SEFAZ | Отправка файла XML, который запрашивает состояние отправки.          |
    | 8         | Обработка ответа             | Получение ответа веб-службы.                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>Настройка URL-адреса для веб-служб SEFAZ 

1. На странице **Настройка версии функции** на вкладке **Действия** на экспресс-вкладке **Действия** выберите **Вызов бразильской службы SEFAZ** (код действия **3**).
2. На экспресс-вкладке **Параметры** в поле **Параметр URL-адреса** введите URL-адрес веб-службы SEFAZ для отправки NF-e.
3. На экспресс-вкладке **Действия** выберите **Вызов бразильской службы SEFAZ** (код действия **7**).
4. На экспресс-вкладке **Параметры** в поле **Параметр URL-адреса** введите URL-адрес веб-службы SEFAZ для отправки NF-e.

#### <a name="configure-the-cancellation-feature-setup"></a>Задание настройки функции отмены

1. На странице **Функции электронного выставления накладных** на вкладке **Настройки** в столбце **Настройка функции** выберите **Отмена**.
2. Выберите **Правка**.
3. На странице **Настройка версии функции** выберите вкладку **Действия** для управления списком действий.
4. Проверка действий, которые необходимы для запроса отмены утвержденного NF-e.

    | Код действия | Имя действия                  | Описание действия                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | 1         | Преобразование документа           | Создание XML-файла отмены NF-e для отправки.            |
    | 2         | Подписать документ                | Применение цифрового сертификата к файлу XML.                   |
    | 3         | Вызов бразильской службы SEFAZ | Отправка подписанного файла XML в веб-службы для отмены. |
    | 4         | Обработка ответа             | Получение ответа веб-службы.                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>Настройка URL-адреса для веб-служб SEFAZ

1. На странице **Настройка версии функции** на вкладке **Действия** на экспресс-вкладке **Действия** выберите **Вызов бразильской службы SEFAZ** (код действия **3**).
2. На экспресс-вкладке **Параметры** в поле **Параметр URL-адреса** введите URL-адрес веб-службы SEFAZ для отмены утвержденного NF-e.

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a>Обеспечение доступности среды электронных накладных и назначение черновой версии

1. На странице **Функции электронных накладных** на вкладке **Среды** выберите **Включить**.
2. В поле **Среда** выберите среду.
3. В поле **Действует с** выберите дату, когда новая среда должна начать действовать.
4. Выберите **Включить**.

![Включение среды выставления накладных в электронной форме](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a>Изменение статуса на "Завершено"

1. На странице **Функции электронных накладных** на вкладке **Версии** выберите версию функции электронных накладных, имеющую статус **Черновик**.
2. Выберите **Изменить статус \> Завершено**.

### <a name="change-the-status-to-publish"></a>Изменение статуса на "Опубликовать"

1. На странице **Функции электронных накладных** на вкладке **Версии** выберите версию функции электронных накладных, имеющую статус **Завершено**.
2. Выберите **Изменить статус \> Опубликовано**.

![Публикация функции выставления накладных в электронной форме](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Настройка интеграции дополнения электронных накладных в Finance или Supply Chain Management

Во время настройки будут выполнены следующие задачи:

1. Включите федеративную функцию NF-e для Бразилии.
2. Импортируйте специфичную модель данных электронной отчетности, сопоставление модели данных электронной отчетности и форматы, которые требуются для финансовых документов NF-e.
3. Импортируйте конфигурацию электронной отчетности и настройте типы откликов, которые необходимы для обновления статуса финансового документа после возврата процесса отправки.

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a>Включение федеративной функции NF-e для Бразилии

1. Перейдите в раздел **Администрирование организации \> Настройка \> Параметры электронных документов**.
2. На вкладке **Функции** установите флажок **Включить** в строке для ссылки на функцию **BR00053**.

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a>Импорт сопоставления модели данных электронной отчетности, необходимого для финансовых документов NF-e

1. Войдите в Finance.
2. В рабочей области **Электронная отчетность** в разделе **Поставщики конфигурации** выберите плитку **Microsoft**. Убедитесь, что этот поставщик конфигурации имеет значение **Активный**. Дополнительные сведения о том, как задать для поставщика состояние **Активный** см. в разделе [Создание поставщиков конфигураций и пометка их как активных](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Выберите **Репозитории**.
4. Выберите **Глобальный ресурс \> Открыть**.
5. Импорт конфигураций **Сопоставление финансовых документов**.

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a>Импорт конфигураций электронной отчетности и настройка типов откликов для финансовых документов

1. В рабочей области **Электронная отчетность** в разделе **Поставщики конфигурации** выберите плитку **Microsoft**.
2. Выберите **Репозитории**.
3. Выберите **Глобальный ресурс \> Открыть**.
4. Импортируйте **Импорт журнала ошибок NF-e (BR)**, **Формат импорта данных ответа NF-e (BR)** и **Импорт сообщения ответа NF-e (BR)**.
5. Перейдите в раздел **Администрирование организации \> Настройка \> Параметры электронных документов**.
6. На вкладке **Электронный документ** выберите **Добавить**.
6. В поле **Имя таблицы** введите **Заголовок финансового документа**.
7. В поле **Контекст документа** выберите **Модель контекста накладной клиента — контекст финансового документа**.
8. Выберите **Типы ответов**.
9. Выберите **Создать**, затем в поле **Тип ответа** выберите **Ответ**.
10. В поле **Статус отправки** выберите **Ожидание**.
11. В поле **Сопоставление моделей** выберите **Формат импорта ответного сообщения — сопоставление модели из ответного сообщения**.
12. Нажмите **Сохранить**.
13. Выберите **Создать**, затем в поле **Тип ответа** введите **ResponseData**.
14. В поле **Статус отправки** выберите **Ожидание**.
15. В поле **Сопоставление моделей** выберите **Формат импорта данных ответа NFe — импорт данных ответов**.
16. Нажмите **Сохранить**.

## <a name="electronic-invoice-processing"></a>Обработка электронных накладных

Во время обработки в Finance будут выполнены следующие задачи:

1. Отправка финансового документа через дополнение электронных накладных.
2. Просмотр журналов выполнения отправки и просмотр результатов обработки.
3. Отправка отмены финансового документа через дополнение электронных накладных.

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a>Отправка финансовых документов NF-e для авторизации SEFAZ 

После включения функции **Настраиваемая интеграция дополнения электронных накладных** старый процесс отправки финансовых документов NF-e для авторизации (**Экспорт/импорт процесса NF-e**) больше не может использоваться. Он заменяется новым процессом с именем **Отправка электронных документов**.

> [!NOTE]
> Перед продолжением убедитесь, что имеется один или несколько финансовых документов клиентов модели 55, которые были выданы финансовым учреждением клиента. Направление для этих финансовых документов должно быть установлено в **Исходящие**, и статус должен быть **Создано**. Дополнительные сведения см. в разделе [Выпуск финансового документа клиента (Бразилия)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).

1. Перейдите в раздел **Администрирование организации \> Периодические задачи \> Электронные документы \> Отправка электронных документов**.
2. Для первой отправки любого документа обязательно установите для параметра **Повторно отправить документы** значение **Нет**. Если необходимо повторно отправить документ через службу, установите для этого параметра значение **Да**.
3. На экспресс-вкладке **Включаемые записи** выберите **Фильтр**, чтобы открыть диалоговое окно **Запрос**, в котором можно построить запрос для выбора повторно отправляемых документов.
4. На вкладке **Диапазон** выберите **Добавить**.
5. В поле **Таблица** выберите **Заголовок финансового документа**.
6. В поле **Производная таблица** выберите **Заголовок финансового документа**.
6. В поле **Поле** выберите **Номер**.
7. В поле **Критерии** введите номер финансового документа, который должен быть отправлен.
8. Выберите **ОК**, чтобы закрыть диалоговое окно **Запрос**.
8. Выберите **ОК**, чтобы отправить выбранные документы.

> [!NOTE]
> При первой попытке отправить документ через службу вам будет предложено подтвердить связь с дополнительной функцией электронных накладных. Выберите **Щелкните здесь для подключения к службе отправки электронных документов**.

### <a name="view-all-submission-logs"></a>Просмотр всех журналов отправки

После включения функции **Настраиваемая интеграция дополнения электронных накладных** будет доступна новая страница, позволяющая отслеживать процесс отправки документа. Можно использовать эту страницу, чтобы просмотреть журналы отправки для всех отправленных документов.

1. Перейдите в раздел **Администрирование организации \> Периодические задачи \> Электронные документы \> Журнал отправки электронных документов**.
2. В поле **Тип документа** выберите **Заголовок финансового документа**, чтобы отфильтровать только финансовые документы.
3. В области действий выберите **Запросы \> Сведения об отправке** для просмотра сведений о журналах выполнения отправки.

![Просмотр сведений журнала отправки](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> Для финансовых документов NF-e в столбце **Код ошибки** отображается код возврата, возвращенный веб-службами SEFAZ.

### <a name="view-submission-logs-through-the-fiscal-document-page"></a>Просмотр журналов отправки с помощью страницы финансовых документов

После включения функции **Настраиваемая интеграция дополнения электронных накладных** можно также просмотреть журналы отправки на странице финансовых документов.

1. Перейдите в раздел **Главная книга \> Запросы и отчеты \> Финансовые документы \> Все финансовые документы**.
2. Выберите финансовый документ, который ранее был отправлен с помощью дополнения электронных накладных.
3. На панели операций откройте вкладку **Федеральный NF-e** и выберите **Журнал электронных документов**.

![Просмотр журналов отправки со страницы финансовых документов](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a>Отправка утвержденных финансовых документов NF-e для отмены SEFAZ

После включения функции **Настраиваемая интеграция дополнения электронных накладных** нельзя будет использовать старый процесс отмены финансовых документов NF-e. Он заменяется новым процессом отмены, который внедрен на странице **Журнал отправки электронных документов**.

> [!NOTE]
> Убедитесь, что вы выполнили отмену финансового документа клиента для утвержденного финансового документа NF-e. Дополнительные сведения см. в разделе [Отмена финансового документа клиента (Бразилия)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).

1. Перейдите в раздел **Администрирование организации \> Периодические задачи \> Электронные документы \> Журнал отправки электронных документов**.
2. Выберите финансовый документ, затем выберите **Функции \> Отправить связанные отправки**.
3. Введите описание для соответствующей отправки, затем нажмите кнопку **ОК**.

### <a name="view-cancellation-submission-logs"></a>Просмотр журналов отправки отмены

1. Перейдите в раздел **Администрирование организации \> Периодические задачи \> Электронные документы \> Журнал отправки электронных документов**.
2. В поле **Тип документа** выберите **Заголовок финансового документа**, чтобы отфильтровать только финансовые документы.
3. Выберите финансовый документ, затем в области действий выберите **Запросы \> Связанная отправка**

    Соответствующие отправки являются отправками, которые связаны с основной отправкой, которая была произведена первой. Например, отправка, которая авторизует конкретный NF-e, — это основная отправка. Отправка, запрашивающая отмену того же NF-e в SEFAZ, является связанной отправкой. Она существует только потому, что она запрашивает отмену задания, выполненного с помощью другой отправки.

    На странице **Связанные отправки** отображаются все связанные отправки и их статус отправки для данного финансового документа. На следующем рисунке первая строка представляет собой отправку, которая запрашивала утверждение финансового документа. Вторая строка представляет собой отправку, которая отменила этот финансовый документ.

    ![Просмотр журналов отправки отмены](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. В области действий выберите **Запросы \> Сведения об отправке** для просмотра сведений о журналах выполнения отправки.

    ![Просмотр сведений журнала отправки отмены](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a>Уведомление о конфиденциальности
Для включения функции BR-00053 (Федеративная NF-e) может потребоваться отправка ограниченных данных, которые включают код налоговой регистрации организации. Они будут переданы сторонним агентствам, которые уполномочены налоговыми органами для целей отправки электронных накладных в этот налоговый орган в заранее определенном формате, требуемом для интеграции с веб-службой правительственного учреждения. Администратор может включать и отключать функцию BR-00053 (федеральная NF-e) путем перехода к разделу **Администрирование организации \> Настройка \> Параметры электронных документов**. Перейдите на вкладку **Функции**, выберите строку, содержащую функцию BR-00053, затем выполните соответствующие действия по выбору. На данные, импортируемые из этих внешних систем в данную веб-службу Dynamics 365, распространяется наше [заявление о конфиденциальности](https://go.microsoft.com/fwlink/?LinkId=512132). Дополнительные сведения см. в разделах "Уведомление о конфиденциальности" в документации по компонентам, относящимся к конкретной стране.


## <a name="additional-resources"></a>Дополнительные ресурсы

- [Обзор дополнительной функции электронных накладных](e-invoicing-service-overview.md)
- [Приступая к работе с дополнительным компонентом электронных накладных](e-invoicing-get-started.md)
- [Настройка дополнения электронных накладных](e-invoicing-setup.md)