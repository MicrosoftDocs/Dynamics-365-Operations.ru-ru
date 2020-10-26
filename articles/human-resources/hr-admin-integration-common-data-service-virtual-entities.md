---
title: Настройка виртуальных сущностей Common Data Service
description: В этом разделе показано, как настроить виртуальные сущности для Dynamics 365 Human Resources. Создание и обновление существующих виртуальных сущностей и анализ созданных и доступных сущностей.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0848b7556100fba38fcab0aa2a1a109e2e055fc9
ms.sourcegitcommit: b89baab13e530b5b1f079231619c628309a4742d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/05/2020
ms.locfileid: "3959583"
---
# <a name="configure-common-data-service-virtual-entities"></a>Настройка виртуальных сущностей Common Data Service

[!include [banner](includes/preview-feature.md)]

Dynamics 365 Human Resources — это виртуальный источник данных в Common Data Service. Он предоставляет полные операции создания, чтения, обновления и удаления (CRUD) в Common Data Service и Microsoft Power Platform. Данные для виртуальных сущностей хранятся не в Common Data Service, а в базе данных приложения. 

Чтобы включить операции CRUD для сущностей Human Resources в Common Data Service, необходимо сделать эти сущности доступными в качестве виртуальных сущностей в Common Data Service. Это позволяет выполнять операции CRUD из Common Data Service и Microsoft Power Platform с данными, находящимися в приложении Human Resources. Операции также поддерживают полные проверки бизнес-логики Human Resources для обеспечения целостности данных при записи данных в сущности.

## <a name="available-virtual-entities-for-human-resources"></a>Доступные виртуальные сущности для Human Resources

Все сущности Open Data Protocol (OData) в приложении Human Resources доступны как виртуальные сущности в Common Data Service. Они также доступны в Power Platform. Теперь можно создавать приложения и взаимодействие с данными непосредственно из модуля Human Resources, используя полные возможности CRUD, без копирования или синхронизации данных с Common Data Service. Порталы Power Apps можно использовать для создания веб-сайтов с внешним интерфейсом, которые позволяют выполнять сценарии совместной работы в приложении Human Resources.

Можно просмотреть список виртуальных сущностей, включенных в среде, и начать работу с сущностями в [Power Apps](https://make.powerapps.com), в решении **Виртуальные сущности Dynamics 365 HR**.

![Виртуальные сущности Dynamics 365 HR в Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a>Сравнение виртуальных и естественных сущностей

Виртуальные сущности для приложения Human Resources не совпадают с естественными сущностями Common Data Service, созданными для приложения Human Resources. Естественные сущности для приложения Human Resources создаются отдельно и поддерживаются в общем решении HCM в Common Data Service. В случае естественных сущностей данные хранятся в Common Data Service и требуют синхронизации с базой данных приложения Human Resources.

> [!NOTE]
> Список естественных сущностей Common Data Service для решения Human Resources см. в разделе [Сущности Common Data Service](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).

## <a name="setup"></a>Настройка

Для включения виртуальных сущностей в среде выполните следующие шаги настройки. 

### <a name="register-the-app-in-microsoft-azure"></a>Регистрация приложения в Microsoft Azure

Прежде всего необходимо зарегистрировать приложение на портале Azure, чтобы платформа идентификации Microsoft могла предоставлять службы проверки подлинности и авторизации для приложения и пользователей. Дополнительные сведения о регистрации приложений в Azure см. в разделе [Краткое руководство: регистрация приложения на платформе идентификации Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

1. Откройте [портал Microsoft Azure](https://portal.azure.com).

2. В списке служб Azure выберите **Регистрации приложений**.

3. Выберите **Создать регистрацию**.

4. В поле **Имя** введите описательное имя для приложения. Например, **Виртуальные сущности Dynamics 365 Human Resources**.

5. В поле **URI перенаправления** введите URL-адрес пространства имен вашего экземпляра Human Resources.

6. Выберите **Регистр**.

7. После завершения регистрации портал Azure отображает область **Обзор** регистрации приложения, которая содержит **Код приложения (клиента)**. На этом этапе запишите **Код приложения (клиента)**. Эти сведения будут введены при [настройке источника данных виртуальной сущности](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

8. В левой области навигации выберите **Сертификаты и секреты**.

9. В разделе **Секреты клиентов** этой страницы выберите **Создать секрет клиента**.

10. Введите описание, выберите продолжительность и выберите **Добавить**.

11. Запишите значение секрета. Эти сведения будут введены при [настройке источника данных виртуальной сущности](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

    > [!IMPORTANT]
    > На этом этапе обязательно запишите значение секрета. Секрет никогда не отображается снова после выхода с этой страницы.

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a>Установка приложения Dynamics 365 HR Virtual Entity

Установите приложение Dynamics 365 HR Virtual Entity в своей среде Power Apps, чтобы развернуть пакет решения виртуальных сущностей в Common Data Service.

1. Откройте [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com).

2. В списке **Среды** выберите среду Power Apps, связанную с экземпляром приложения Human Resources.

3. В разделе **Ресурсы** этой страницы выберите **Приложения Dynamics 365**.

4. Выберите действие **Установить приложение**.

5. Выберите **Dynamics 365 HR Virtual Entity**, затем выберите **Далее**.

6. Просмотрите и отметьте, чтобы принять условия обслуживания.

7. Выберите **Установить**.

Установка занимает несколько минут. После завершения переходите к следующим шагам.

![Установка приложения Dynamics 365 HR Virtual Entity с помощью центра администрирования Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a>Настройка источника данных виртуальной сущности 

Следующим шагом является настройка источника данных виртуальных сущностей в среде Power Apps. 

1. Откройте [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com).

2. В списке **Среды** выберите среду Power Apps, связанную с экземпляром приложения Human Resources.

3. Выберите **URL-адрес среды** в разделе **Сведения** на странице.

4. В разделе **Центр работоспособности решений** выберите значок **Расширенный поиск** в верхнем правом углу страницы приложения.

5. На странице **Расширенный поиск** в раскрывающемся списке **Найти** выберите **Конфигурации виртуальных источников данных Finance and Operations**.

6. Выберите **Результаты**.

7. Выберите запись **Источник данных Microsoft HR**.

8. Введите требуемые сведения для конфигурации источника данных.

   - **Целевой URL-адрес**: URL-адрес вашего пространства имен Human Resources.
   - **Код клиента**: код клиента Azure Active Directory ( Azure AD).
   - **Код приложения AAD**: код приложения (клиента), созданный для приложения, зарегистрированного на портале Microsoft Azure. Эта информация была получена ранее на шаге [Регистрация приложения в Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).
   - **Секрет приложения AAD**: секрет приложения (клиента), созданный для приложения, зарегистрированного на портале Microsoft Azure. Эта информация была получена ранее на шаге [Регистрация приложения в Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

9. Нажмите **Сохранить и закрыть**.

   ![Источник данных Microsoft HR](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a>Предоставление разрешений приложения в Human Resources

Предоставьте разрешения двум приложениям Azure AD в Human Resources:

- Приложение, созданное для вашего клиента на портале Microsoft Azure
- Приложение Dynamics 365 HR Virtual Entity, установленное в среде Power Apps 

1. В Human Resources откройте страницу **Приложения Azure Active Directory**.

2. Выберите **Создать** для создания новой записи приложения:

    - В поле **Код клиента** введите код клиента приложения, зарегистрированного на портале Microsoft Azure.
    - В поле **Имя** введите имя приложения, зарегистрированного на портале Microsoft Azure.
    - В поле **Код пользователя** выберите код пользователя с разрешениями администратора в модуле Human Resources и среде Power Apps.

3. Выберите **Создать** для создания записи второго приложения:

    - **Код клиента**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Имя**: Dynamics 365 HR Virtual Entity
    - В поле **Код пользователя** выберите код пользователя с разрешениями администратора в модуле Human Resources и среде Power Apps.

## <a name="generate-virtual-entities"></a>Создание виртуальных сущностей

По завершении настройки можно выбрать виртуальные сущности, которые требуется создать и включить в данном экземпляре Common Data Service.

1. Откройте [Центр администрирования Power Platform](https://admin.powerplatform.microsoft.com).

2. В списке **Среды** выберите среду Power Apps, связанную с экземпляром приложения Human Resources.

3. Выберите **URL-адрес среды** в разделе **Сведения** на странице.

4. В разделе **Центр работоспособности решений** выберите значок **Расширенный поиск** в верхнем правом углу страницы.

5. На странице **Расширенный поиск** в раскрывающемся списке **Найти** выберите **Доступные сущности HR**.

6. Воспользуйтесь параметрами фильтра, чтобы найти сущности или сущности, которые требуется включить.

7. Выберите сущность в списке.

8. На странице сущности измените значение свойства **Создана** на **Да** для сущности.

9. Сохраните и закройте страницу сущности.

> [!NOTE]
> Можно создать сразу несколько виртуальных сущностей, используя страницу **Изменение нескольких записей**. Выберите несколько записей на странице и нажмите кнопку **Изменить** на ленте. Затем можно изменить свойство **Создана** для всех выбранных записей.

![Доступные сущности HR](./media/hr-admin-integration-virtual-entities-available.jpg)

> [!NOTE]
> Для упрощения процесса создания виртуальных сущностей в будущих выпусках процесс будет выполняться на странице в модуле Human Resources.

## <a name="see-also"></a>См. также

[Что такое Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[Обзора сущностей](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[Обзор отношений сущностей](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[Создание и редактирование виртуальных сущностей, содержащих данные из внешнего источника данных](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Что такое порталы Power Apps?](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[Обзор создания приложений в Power Apps](https://docs.microsoft.com/powerapps/maker/)
