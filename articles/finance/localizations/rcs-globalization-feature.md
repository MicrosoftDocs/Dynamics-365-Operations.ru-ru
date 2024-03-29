---
title: Regulatory Configuration Service (RCS) — функции глобализации
description: В этой статье объясняется, как использовать службу Microsoft Regulatory Configuration Services (RCS) и глобальный репозиторий для создания и использования функций глобализации.
author: kfend
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.custom: 97423
ms.assetid: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
ms.openlocfilehash: 5df0b37741103c7beba4cc43f0aba25a5af52be0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279781"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a>Regulatory Configuration Service (RCS) — функции глобализации

[!include [banner](../includes/banner.md)]

Для создания функции глобализации, которая может использоваться в службах глобализации, например в службе электронных накладных, можно использовать Microsoft Regulatory Configuration Service (RCS). RCS позволяет выполнять следующие задачи:

- Определение связанных компонентов функции.
- Управление жизненным циклом функции с помощью статуса функции.
- Сделать функцию доступной для указанных сред.
- Совместное использование функции с другими организациями.

Следующие процедуры показывают, как пользователь в RCS может добавить функцию глобализации и связанные компоненты, обновить статус функции и сделать функцию доступной, чтобы ее можно было использовать в службах глобализации.

Перед выполнением процедур необходимо выполнить шаги, которые относятся к следующим задачам:

- Доступ к экземпляру RCS.
- Создание и активация поставщика конфигураций. Дополнительные сведения см. в [Создание поставщиков конфигураций и пометка их как активных](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

В вашем экземпляре приложений для управления финансами и операциями выполните следующие действия.

1. Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.
2. Если у вашей компании нет среды RCS, щелкните **Regulatory Services — конфигурация** и следуйте инструкциям по подготовке среды.

> [!NOTE]
> Если среда RCS уже подготовлена для вашей компании, воспользуйтесь URL-адресом страницы для доступа к ней, выбрав параметр входа.

## <a name="turn-on-the-globalization-features"></a>Включение функций глобализации

1. В экземпляре RCS выберите плитку **Управление функциями**.
2. В рабочей области **Управление функциями** выберите **Функции глобализации** в списке и выберите **Включить**.

    ![Функции глобализации в управлении функциями.](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a>Функции глобализации

Чтобы использовать функцию глобализации, необходимо сначала импортировать ее из глобального репозитория и создать для нее свою собственную версию. Есть два способа добавления функций глобализации:

- Добавление производной функции, основанной на существующей функции, которая была опубликована или передана в общий доступ.
- Добавление новой функции, созданной с нуля.

## <a name="access-globalization-features"></a>Доступ к функциям глобализации

1. Убедитесь, что в модуле "Управление функциями" включена функция **Функции глобализации**, как описано ранее в этой статье.
2. Откройте новую рабочую область **Функции глобализации**, а затем в разделе **Функции** выберите плитку **Электронные накладные**.

    ![Рабочая область глобальных функций.](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    Открывается страница **Функции электронных накладных**.

    ![Страница функций электронных накладных.](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a>Добавление производной функции глобализации

Можно добавить новую функцию глобализации, создав производную от нее функцию, которая была опубликована или передана в общий доступ.

1. Выберите **Импорт**, чтобы открыть страницу **Импорт функции из глобального репозитория**.

    ![Страница импорта функции из глобального репозитория.](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. Выберите **Синхронизировать** для получения последних функций.

    В синхронизированном списке указаны доступные для пользователя функции, поскольку они были опубликованы корпорацией Майкрософт или для них был открыт общий доступ другим поставщиком конфигураций.

    ![Синхронизированный список функций.](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. В списке выберите функции для импортирования, а затем выберите **Импорт**. При успешном импорте выбранных функций появится сообщение.

    ![Сообщение об успешном импорте.](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. Выберите **Добавить**, а затем в раскрывающемся диалоговом окне выберите **На основе существующей версии**.
5. Введите имя и описание для функции.
6. В списке доступных функций выберите базовую версию функции, а затем выберите **Создать функцию**.

    ![Добавление производной функции.](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    Добавленная функция создается, ей присваивается статус **Черновик**.

    ![Производная функция со статусом "Черновик".](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. Просмотрите компоненты функций, чтобы определить, требуются ли обновления:

    - Просмотрите конфигурации, в случае необходимости настройки форматов электронной отчетности (ER) и их привязки к сопоставлениям форматов для версии функции.
    - Просмотрите настройки, если необходимо настроить вкладку **Действия**, **Правила применимости** или **Переменные** для версии функции.

8. На вкладке **Версии** выберите дату **Действует с** и введите описание, если поле **Описание** пустое.
9. Выберите **Изменить статус** для завершения функции. Выполненные функции могут быть доступны для определенной среды, чтобы их можно было использовать в службах глобализации, либо они могут быть опубликованы в глобальном репозитории.

> [!NOTE]
> Функции со значением **Статус версии функции** — **Опубликовано** могут использоваться совместно с внешними организациями.

## <a name="add-a-new-globalization-feature"></a>Добавление новой функции глобализации

Можно добавить новую функцию глобализации, создав ее с нуля.

1. На странице **Импорт функции из глобального репозитория** выберите **Добавить**, а затем в раскрывающемся диалоговом окне выберите параметр **Создать функцию**.
2. Введите имя и описание для функции.
3. Выберите **создать функцию**.

    ![Добавление новой функции.](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. На вкладке **Версии** выберите дату **Действует с**, а затем выберите **Изменить статус**, чтобы завершить функцию. Выполненные функции могут быть доступны для определенной среды, чтобы их можно было использовать в службах глобализации, либо они могут быть опубликованы в глобальном репозитории.

> [!NOTE]
> Функции со значением **Статус версии функции** — **Опубликовано** могут использоваться совместно с внешними организациями.

## <a name="feature-component-overview"></a>Обзор компонентов функций

Для функций глобализации есть следующие компоненты:

- **Версия** — этот компонент поддерживает управление жизненным циклом функции и позволяет пользователям управлять статусом для разных версий функции.
- **Конфигурации** — этот компонент позволяет пользователям управлять, просматривать и изменять соответствующие форматы электронной отчетности и сопоставления форматов.
- **Настройки** — этот компонент позволяет пользователям служб глобализации, например службы электронных накладных, управлять настройкой связанной версии функции. Таким образом, он поддерживает гибкое создание правил обмена данными и реакции.
- **Среда** — этот компонент позволяет пользователям служб глобализации, например службы электронных накладных, управлять средой, в которой используется настройка версии функций, и предоставлять авторизацию пользователям, которые будут иметь к ней доступ.
- **Организации** — этот компонент позволяет пользователям использовать функцию совместно с внешними организациями.

## <a name="configuring-feature-components"></a>Настройка компонентов функций

### <a name="version-and-status"></a>Версия и статус

Версия используется для управления жизненным циклом функции глобализации.

Статус можно изменить в поле **Статус** на вкладке **Версия**. Доступны следующие статусы:

- **Черновик** — функция может быть изменена только в том случае, если у нее есть этот статус.
- **Завершено** — функция и все связанные компоненты были завершены и не могут быть изменены.
- **Опубликовано** — функция и все связанные компоненты были опубликованы в глобальном репозитории.
- **Общий** — функция и все связанные компоненты являются общими для внешних организаций.
- **Включено** — функция и все связанные компоненты включены для использования в службе глобализации, такой как служба электронных накладных.

> [!NOTE]
> Для функций должны последовательно изменяться некоторые статусы. Таким образом, не все статусы могут быть доступны на каждом этапе жизненного цикла.

### <a name="configurations"></a>Конфигурации

Для конфигураций доступны следующие действия:

- **Просмотреть** — просмотр основных конфигураций функций, которые не требуют обновления.
- **Изменить** — создание черновой версии выбранной конфигурации, чтобы можно было редактировать формат или сопоставление форматов в конструкторе форматов.
- **Удалить** — удаление выбранной конфигурации из функции.
- **Повторно разместить** — повторно разместить функцию. Дополнительные сведения см. в разделе [Повторное размещение производных функций глобализации](#rebase) далее в этой статье.

### <a name="setups"></a>Настройки

Для настроек функций доступны следующие действия:

- **Добавить** — создание новой настройки функции. Эта настройка функций может быть производной из существующей настройки функции или создана с нуля.
- **Удалить** — удаление выбранной настройки функции.
- **Просмотреть** — просмотр базовой настройки функции, которая не требует каких-либо изменений.
- **Изменить** — создание, удаление или изменение атрибутов трех основных компонентов настройки функции:

    - Действия и их параметры
    - Правила применимости
    - Переменные

![Страница настройки версии функции.](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a>Среды

Для среды доступны следующие действия:

- **Включить** — для выбранной версии функции выберите опубликованную среду и выберите дату **Действует с**, когда она должна быть доступна. Дополнительные сведения см. в разделе [Настройка сред для реализации возможностей](#configureenvironment) далее в этой статье.
- **Отмена** — удаление среды для настройки функции.

### <a name="organizations"></a>Организации

Выполните следующие действия, чтобы совместно использовать функцию глобализации с внешней организацией.

1. На странице **Функции электронных накладных** выберите функцию и версию функции для общего доступа.
2. На вкладке **Организации** выберите **Поделиться**, а затем в раскрывающемся диалоговом окне введите имя домена организации.
3. Выберите **Поделиться**.

    ![Совместное использование функции с организацией.](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

Функция используется совместно с выбранной организацией и доступна для данной организации в глобальном репозитории. После этого эту функцию можно импортировать в экземпляр RCS организации или в Dynamics 365 Finance, чтобы ее можно было использовать.

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a>Повторное размещение производных функций глобализации

Производную функцию глобализации можно повторно изменить в новой или обновленной базовой версии функции. Таким образом, изменения, произошедшие в базовой версии, могут быть автоматически обновлены. Обновленная базовая версия функции создается поставщиком исходной конфигурации и затем публикуется или совместно используется.

![Обновленная базовая версия функции.](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

Например, если необходимо повторно разместить производную версию созданной функции, сначала нужно получить последнюю версию функции, импортировав ее из глобального репозитория.

1. На странице **Функции электронных накладных** выберите **Импорт**.
2. Выберите **Синхронизировать** для получения последних функций.
3. В списке функций выберите функции для импортирования, а затем выберите **Импорт**.

    ![Импорт последней версии функции.](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. В списке функций выберите функцию для повторного размещения.
5. На вкладке **Версия** выберите **Создать**, чтобы создать черновую версию.

    ![Создана новая черновая версия.](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. Выберите **Повторно разместить**.
7. В диалоговом окне **Повторно разместить** выберите последнюю версию функции, куда следует выполнить повторное размещение.

    ![Диалоговое окно повторного размещения.](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. Нажмите **ОК**.
9. Просмотрите компоненты функции и внесите необходимые изменения.
10. Выберите **Изменить статус** для завершения повторного размещения функции. После завершения повторного размещения можно выполнить дополнительные действия. Например, можно опубликовать функцию и сделать ее доступной для использования в службах глобализации.

    ![Статус функции обновлен до "Завершено".](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a>Настройка сред для функций глобализации

Пользователи служб глобализации могут управлять средой, чтобы настроить функцию глобализации и предоставить авторизацию другим пользователям, у которых будет к ней доступ.

1. В рабочей области **Функции глобализации**, а затем в разделе **Среды** выберите плитку **Электронные накладные**.

    ![Рабочая область функций глобализации.](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. Выберите **Параметры хранилища ключей**, а затем выберите **Создать**, чтобы создать секрет хранилища ключей Azure.
3. Введите имя и описание для хранилища ключей, а затем в поле **URI хранилища ключей** введите URL-адрес, идентифицирующий ресурс хранилища ключей в Azure.
4. На экспресс-вкладке **Сертификаты** выберите **Добавить**, чтобы добавить сертификат, а затем введите имя и описание для каждого сертификата.

    ![Сертификат добавлен.](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. Выберите **Создать** для создания новой среды.
6. Введите имя, описание и секретный ключ маркера подписи общего доступа, необходимый для хранения.
7. На экспресс-вкладке **Пользователи** выберите **Создать**, чтобы добавить пользователя, у которого будет разрешение на доступ к этой среде.
8. Введите код пользователя и адрес электронной почты пользователя.
9. Повторите шаги 7 и 8, чтобы добавить пользователей.
10. Выберите **Опубликовать**, чтобы опубликовать среду.

    ![Опубликованная среда.](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
