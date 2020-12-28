---
title: Интеграция с LinkedIn Talent Hub
description: В этом разделе объясняется, как настроить интеграцию между Microsoft Dynamics 365 Human Resources и LinkedIn Talent Hub.
author: jaredha
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6f70e3a6ccf9770c75334d355db5e9df9ee912dd
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527893"
---
# <a name="integrate-with-linkedin-talent-hub"></a>Интеграция с LinkedIn Talent Hub

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) является платформой системы отслеживания кандидатов (АТС). Оно позволяет искать, контролировать и нанимать сотрудников в одном месте. Интегрировав Microsoft Dynamics 365 Human Resources с LinkedIn Talent Hub, можно легко создавать записи о сотрудниках в Human Resources для претендентов, которые были приняты на должность.

## <a name="setup"></a>Настройка

Системный администратор должен выполнить задачи настройки для включения интеграции с LinkedIn Talent Hub. Во-первых, в среде Power Apps необходимо настроить пользователя и роль безопасности, чтобы предоставить LinkedIn Talent Hub соответствующие разрешения на запись данных в Human Resources.

### <a name="link-your-environment-to-linkedin-talent-hub"></a>Связывание среды с LinkedIn Talent Hub

1. Откройте [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).

2. В раскрывающемся меню пользователя выберите **Параметры продукта**.

3. В левой области переходов в разделе **Дополнительно** выберите **Интеграции**.

4. Выберите **Авторизовать** для интеграции Microsoft Dynamics 365 Human Resources.

5. На странице **Dynamics 365 Human Resources** выберите среду, с которой требуется связать LinkedIn Talent Hub, затем выберите пункт **Ссылка**.

    ![Подключение LinkedIn Talent Hub](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > Можно привязывать только к средам, в которых ваша учетная запись пользователя имеет доступ администратора к среде Human Resources и к связанной среде Power Apps. Если на странице ссылки Human Resources отсутствуют среды, убедитесь, что у вас есть лицензированная среда Human Resources на клиенте, а пользователь, с которым вы выполнили вход на страницу ссылки, обладает правами администратора как в среде Human Resources, так и в среде Power Apps.

### <a name="create-a-power-apps-security-role"></a>Создание роли безопасности Power Apps

1. Откройте [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com).

2. В списке **Среды** выберите среду, связанную со средой Human Resources, с которой необходимо связать экземпляр LinkedIn Talent Hub.

3. Выберите **Параметры**.

4. Разверните узел **Пользователи + Разрешения** и выберите **Роли безопасности**.

5. На странице **Роли безопасности** на панели инструментов выберите **Создать роль**.

6. На вкладке **Сведения** введите имя роли, например, **Интеграция LinkedIn Talent Hub HRIS**.

7. На вкладке **Настройка** выберите разрешение **Чтение** на уровне организации для следующих сущностей:

    - Объект
    - Поле
    - Родственные связи

8. Сохраните и закройте роль безопасности.

### <a name="create-a-power-apps-application-user"></a>Создание пользователя приложения Power Apps

Пользователь приложения должен быть создан для адаптера LinkedIn Talent Hub, чтобы предоставить разрешения на адаптер для записи записей кандидатов в среду Power Apps.

1. Откройте [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com).

2. В списке **Среды** выберите среду, связанную со средой Human Resources, с которой необходимо связать экземпляр LinkedIn Talent Hub.

3. Выберите **Параметры**.

4. Разверните узел **Пользователи + Разрешения** и выберите **Пользователи**.

5. Выберите **Управление пользователями в Dynamics 365**.

6. Используйте раскрывающееся меню над списком, чтобы изменить представление с представления по умолчанию **Включенные пользователи** на **Пользователи приложения**.

    ![Представление пользователей приложений](./media/hr-admin-integration-power-apps-application-users.jpg)

7. На панели инструментов выберите **Создать**.

8. На странице **Создать пользователя** выполните следующие действия:

    1. Измените значение поля **Тип пользователя** на **Пользователь приложения**.
    2. Задайте в поле **Имя пользователя** значение **Интеграция Dynamics365 HR LinkedIn HRIS**.
    3. Задайте в поле **Код приложения** значение **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    4. Введите любое значение в поля **Имя**, **Фамилия** и **Основной адрес электронной почты**.
    5. На панели инструментов выберите **Сохранить \& закрыть**.

### <a name="assign-a-security-role-to-the-new-user"></a>Назначение роли безопасности новому пользователю

После сохранения и закрытия нового пользователя приложения в предыдущем разделе выполняется возврат на страницу **Список пользователя**.

1. На странице **Список пользователей** измените представление на **Пользователи приложения**.

2. Выберите пользователя приложения, которого вы создали в предыдущем разделе.

3. На панели инструментов выберите **Управление ролями**.

4. Выберите роль безопасности, которая была создана ранее для интеграции.

5. Нажмите **ОК**.

### <a name="add-an-azure-active-directory-app-in-human-resources"></a>Добавление приложения Azure Active Directory в Human Resources

1. В Dynamics 365 Human Resources откройте страницу **Приложения Azure Active Directory**.
2. Добавьте новую запись в список и задайте следующие поля:

    - **Код клиента**: введите **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    - **Имя**: введите имя созданной ранее роли безопасности Power Apps, например **Интеграция LinkedIn Talent Hub HRIS**.
    - **Код пользователя**: выберите пользователя, обладающего разрешениями на запись данных в управлении персоналом.

### <a name="create-the-entity-in-common-data-service"></a>Создание сущности в Common Data Service

> [!IMPORTANT]
> Интеграция с LinkedIn Talent Hub зависит от виртуальных сущностей в Common Data Service для Human Resources. В качестве обязательного условия для этого шага настройки необходимо настроить виртуальные сущности. Сведения о настройке виртуальных сущностей см. в разделе [Настройка виртуальных сущностей Common Data Service](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

1. В Human Resources откройте страницу **Интеграция Common Data Service (CDS)**.

2. Выберите вкладку **Виртуальные сущности**.

3. Отфильтруйте список сущностей по метке сущности, чтобы найти **Экспортированный кандидат LinkedIn**.

4. Выберите сущность, затем выберите **Генерировать/обновить**.

## <a name="exporting-candidate-records"></a>Экспорт записей кандидатов

После завершения настройки сотрудники по найму персонала и специалисты отдела кадров (HR) могут использовать функцию **Экспорт в HRIS** в LinkedIn Talent Hub для экспорта записей о нанятых кандидатах из LinkedIn Talent Hub в Human Resources.

### <a name="export-records-from-linkedin-talent-hub"></a>Экспорт записей из LinkedIn Talent Hub

После того как кандидат перешел в процесс набора персонала и был принят на работу, можно экспортировать запись кандидата из LinkedIn Talent Hub в модуль Human Resources.

1. В LinkedIn Talent Hub откройте проект, для которого вы нанимаете нового сотрудника.

2. Выберите запись кандидата.

3. Выберите **Изменить стадию**, затем выберите **Нанят**.

4. В меню с многоточием (**...**) для кандидата выберите **Экспорт в HRIS**.

5. В области **Экспорт в HRIS** введите информацию, которую необходимо экспортировать:

    - В поле **Поставщик HRIS** выберите **Microsoft Dynamics 365 Human Resources**.
    - В поле **Дата начала** выберите значение для нового сотрудника.
    - В поле **Должность** введите название должности для нового сотрудника.
    - В поле **Местоположение** введите местоположение, в котором будет базироваться сотрудник.
    - Введите или проверьте адрес электронной почты сотрудника.

![Панель экспорта в HRIS в LinkedIn Talent Hub](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a>Завершение подключения в модуле Human Resources

Записи кандидатов, экспортированные из LinkedIn Talent Hub в модуль Human Resources, отображаются в разделе **Кандидаты на прием на работу** на странице **Управления персоналом**.

1. В Human Resources откройте страницу **Управление персоналом**.

2. В разделе **Кандидаты на прием на работу** выберите **Нанять** для выбранного кандидата.

3. В диалоговом окне **Нанять нового работника** проверьте запись и добавьте все необходимые сведения. Можно также выбрать номер должности, на которую кандидат был нанят.

После ввода требуемой информации можно продолжить работу со стандартными процессами для создания записей о сотрудниках и адаптации сотрудников.

Следующие сведения импортируются и включаются в новую запись сотрудника:

- Имя
- Фамилия
- Дата начала трудоустройства
- Адрес электронной почты
- Номер телефона

## <a name="see-also"></a>См. также

[Настройка виртуальных сущностей Common Data Service](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Что такое Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)
