---
title: Устранение проблем с синхронизацией в режиме реального времени
description: В этом разделе содержатся сведения об устранении неполадок при синхронизации в режиме реального времени.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: ca12759096bd1bafda0a5eee18287a694083db69
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685571"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Устранение проблем с синхронизацией в режиме реального времени

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Dataverse. А именно, в нем содержатся сведения об устранении неполадок при синхронизации в режиме реального времени.

> [!IMPORTANT]
> Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD). В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Синхронизация в режиме реального времени создает ошибку "403 Запрещено" при создании строки в приложении Finance and Operations

При создании строки в приложении Finance and Operations может появиться следующее сообщение об ошибке:

*\[{\\"ошибка\\":{\\"код\\":\\"0x80072560\\",\\"сообщение\\":\\"Пользователь не является членом организации.\\"}}\], Удаленный сервер вернул ошибку: (403) Запрещено."}}".*

Чтобы устранить проблему, выполните шаги, указанные в разделе [Системные требования и предварительные условия](requirements-and-prerequisites.md). Для выполнения этих шагов пользователь с двойной записью, созданный в Dataverse, должен иметь роль администратора системы. Группа-владелец по умолчанию должна также иметь роль администратора системы.

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Синхронизация в режиме реального времени для любого объекта постоянно создает аналогичную ошибку при создании строки в приложении Finance and Operations

**Роль, требуемая для исправления ошибки:** системный администратор

При каждом попытке сохранить данные объекта в приложении Finance and Operations может появиться сообщение об ошибке, подобное следующему:

*Не удается сохранить изменения в базе данных. Единица работы не может зафиксировать проводку. Невозможно записать данные в единицы измерения объекта. Операции записи в UnitOfMeasureEntity заканчиваются сбоем с сообщением об ошибке "Не удается синхронизировать с единицами измерения объекта".*

Чтобы устранить проблему, необходимо убедиться, что необходимые ссылочные данные существуют как в приложении Finance and Operations ,так и в Dataverse. Например, если клиент, указанный в приложении Finance and Operations, принадлежит определенной группе клиентов, убедитесь, что эта группа клиентов существует в Dataverse.

Если данные существуют на обеих сторонах, и вы убедились, что проблема не связана с данными, выполните следующие действия.

1. Остановите связанный объект.
2. Выполните вход в приложение Finance and Operations и убедитесь, что строки для объекта, в котором возникает ошибка, существуют в таблицах DualWriteProjectConfiguration и DualWriteProjectFieldConfiguration. Например, вот как выглядит запрос, если происходит сбой объекта **Клиенты**.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. Если имеются строки для объекта, в котором возникает ошибка, даже после остановки сопоставления таблиц, удалите строки, относящиеся к объекту, в котором возникает ошибка. Запишите столбец **projectname** в таблице DualWriteProjectConfiguration и извлеките запись в таблице DualWriteProjectFieldConfiguration, используя это имя проекта, чтобы удалить строку.
4. Запустите сопоставление таблиц. Проверьте, были ли данные синхронизированы без каких-либо проблем.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Обработка ошибок привилегии чтения или записи при создании данных в приложении Finance and Operations

При создании данных в приложении Finance and Operations может быть получено сообщение об ошибке "Ошибочный запрос", которая напоминает следующий пример.

![Пример сообщения об ошибке "Ошибочный запрос"](media/error_record_id_source.png)

Чтобы решить эту проблему, необходимо назначить правильную роль безопасности для рабочей группы сопоставленного подразделения Dynamics 365 Sales или Dynamics 365 Customer Service, чтобы включить отсутствующую привилегию.

1. В приложении Finance and Operations найдите подразделение, сопоставленное в наборе подключений интеграции данных.

    ![Сопоставление организации](media/mapped_business_unit.png)

2. Выполните вход в среду приложения на основе модели в Dynamics 365, перейдите к пункту **Параметры \>Безопасность** и найдите рабочую группу сопоставленного подразделения.

    ![Рабочая группа сопоставленного подразделения](media/setting_security_page.png)

3. Откройте страницу этой рабочей группы для редактирования, затем выберите **Управление ролями**, чтобы открыть диалоговое окно **Управление ролями группы**.

    ![Кнопка "Управление ролями"](media/manage_team_roles.png)

4. Назначьте роль с привилегиями на чтение/запись для соответствующих таблиц, затем выберите **ОК**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Устранение проблем синхронизации в среде с недавно измененной средой Dataverse

**Роль, требуемая для исправления ошибки:** системный администратор

При создании данных в приложении Finance and Operations может появиться следующее сообщение об ошибке:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Не удается создать полезную нагрузку для объекта CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Сбой создания полезной нагрузки с ошибкой Недопустимый URI: URI пуст."}\],"isErrorCountUpdated":true}*

Вот как выглядит эта ошибка в приложении на основе модели в Dynamics 365:

*Возникла непредвиденная ошибка в коде независимого разработчика. (ErrorType = ClientError) Непредвиденное исключение от подключаемого модуля (Выполнить): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: не удалось обработать учетную запись объекта - (Сбой попытки подключения, так как подключенная стороне не предоставляет правильный ответ в течение некоторого периода времени, или сбой установленного подключения из-за отсутствия ответа от хост-компьютера*

Эта ошибка возникает в том случае, когда среда Dataverse ошибочно сбрасывается одновременно с попыткой создать данные в приложении Finance and Operations.

Чтобы устранить проблему, выполните следующие действия.

1. Выполните вход на виртуальную машину Finance and Operations, откройте SQL Server Management Studio (SSMS) и выполните поиск строк в таблице DUALWRITEPROJECTCONFIGURATIONENTITY, где **internalentityname** равно **Customers V3** и **externalentityname** равно **accounts**. Вот как выглядит этот запрос.

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. Используйте имя проекта из результатов предыдущего запроса, чтобы выполнить следующий запрос.

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. Убедитесь, что столбец **externalenvironmentURL** имеет правильный URL-адрес Dataverse или приложения. Удалите все дубликаты строк, которые указывают на неправильный URL-адрес Dataverse. Удалите соответствующие строки в таблицах DUALWRITEPROJECTFIELDCONFIGURATION и DUALWRITEPROJECTCONFIGURATION.
4. Остановите сопоставление таблиц, а затем перезапустите его


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]