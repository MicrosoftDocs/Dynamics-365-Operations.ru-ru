---
title: Создание приложения для повторяющегося экспорта данных
description: В этой статье описывается создание приложения логики Microsoft Azure, которое экспортирует данные из Microsoft Dynamics 365 Human Resources по регулярному расписанию.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 97972d2179c42e9d2d672cbebb75643ef0a02a62
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113976"
---
# <a name="create-a-recurring-data-export-app"></a>Создание приложения для повторяющегося экспорта данных

В этой статье описывается создание приложения логики Microsoft Azure, которое экспортирует данные из Microsoft Dynamics 365 Human Resources по регулярному расписанию. В учебнике для экспорта данных используется API пакета DMF REST Human Resources. После экспорта данных приложение логики сохраняет экспортированный пакет данных в папке Microsoft OneDrive для бизнеса.

## <a name="business-scenario"></a>Бизнес-сценарий

В одном обычном бизнес-сценарии для интеграции Microsoft Dynamics 365 данные должны быть экспортированы в нисходящий элемент в повторяющемся расписании. В этом учебнике описывается, как экспортировать все записи работников из Microsoft Dynamics 365 Human Resources и сохранить список работников в папке OneDrive для бизнеса.

> [!TIP]
> Данные, экспортируемые в этом учебнике, и назначение экспортированных данных представляют собой только примеры. Их можно легко изменить в зависимости от потребностей бизнеса.

## <a name="technologies-used"></a>Используемые технологии

В этом учебнике используются следующие технологии:

- **[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** — Главный источник данных для работников, которые будут экспортированы.
- **[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** — технология, обеспечивающая согласование и планирование повторяющегося экспорта.

    - **[Соединители](https://docs.microsoft.com/azure/connectors/apis-list)** — технология, используемая для подключения приложения логики к необходимым конечным точкам.

        - [HTTP с соединителем Azure AD](https://docs.microsoft.com/connectors/webcontents/)
        - Соединитель [OneDrive для бизнеса](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)

- **[Пакет DMF REST API](../dev-itpro/data-entities/data-management-api.md)** — технология, используемая для запуска экспорта и отслеживания его выполнения.
- **[OneDrive для бизнеса](https://onedrive.live.com/about/business/)** — место назначения для экспортируемых работников.

## <a name="prerequisites"></a>Необходимые условия

Прежде чем приступить к выполнению упражнения данного учебника, необходимо иметь следующие компоненты:

- Среда Human Resources, имеющая разрешения уровня администратора в среде
- [Подписка Azure](https://azure.microsoft.com/free/) для размещения приложения логики

## <a name="the-exercise"></a>Упражнение

В конце этого упражнения у вас будет приложение логики, связанное с вашей средой Human Resources и вашей учетной записью OneDrive для бизнеса. Приложение логики экспортирует пакет данных из Human Resources, дождитесь завершения экспорта, загрузите экспортированный пакет данных и сохраните пакет данных в указанную папку OneDrive для бизнеса.

Готовое приложение логики будет похоже на следующее.

![Обзор приложения логики](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a>Шаг 1. Создание проекта экспорта данных в Human Resources

В Human Resources создайте проект экспорта данных, экспортирующий работников. Назовите проект **Export Workers** и убедитесь , что для параметра **Создать пакет данных** установлено значение **Да**. Добавьте один объект (**Работник**) в проект и выберите формат, в котором выполняется экспорт. (Формат Microsoft Excel используется в данном учебнике.)

![Экспорт проекта данных о работниках](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> Помните название проекта экспорта данных. Это потребуется при создании приложения логики на следующем шаге.

### <a name="step-2-create-the-logic-app"></a>Шаг 2. Создание приложения логики

Здесь создается приложение логики.

1. На портале Azure создайте приложение логики.

    ![Страница создания приложения логики](media/integration-logic-app-creation-1.png)

2. В Logic Apps Designer начнем с чистого приложения логики.
3. Добавьте [Триггер расписания повторения](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) для запуска приложения логики каждые 24 часа (или в соответствии с выбранным расписанием).

    ![Диалоговое окно повторения](media/integration-logic-app-recurrence-step.png)

4. Вызовите DMF REST API [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage), чтобы запланировать экспорт пакета данных.

    1. Используйте действие **Вызвать запрос HTTP** из HTTP с соединителем Azure AD.

        - **URL-адрес базового ресурса:** URL-адрес вашей среды Human Resources (не включайте информацию о пути и пространстве имен.)
        - **URI-адрес ресурса Azure AD:** `http://hr.talent.dynamics.com`

        > [!NOTE]
        > Служба Human Resources еще не предоставляет соединитель, который предоставляет все API REST, которые составляют пакет DMF REST API, например, **ExportToPackage**. Вместо этого необходимо вызывать API с помощью необработанных запросов HTTPS через HTTP с соединителем Azure AD. Этот разъем использует Azure Active Directory (Azure AD) для аутентификации и авторизации в Human Resources.

        ![HTTP с соединителем Azure AD](media/integration-logic-app-http-aad-connector-step.png)

    2. Выполните вход в среду Human Resources с помощью HTTP с соединителем Azure AD.
    3. Настройте запрос HTTP **POST** для вызова DMF REST API **ExportToPackage**.

        - **Метод:** POST
        - **URL-адрес запроса:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
        - **Состав запроса:**

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Вызов действия запроса HTTP](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > Возможно, потребуется переименовать каждый шаг, чтобы он более был более значимым, чем имя по умолчанию, **Вызвать HTTP-запрос**. Например, можно переименовать этот шаг **ExportToPackage**.

5. [Инициализируйте переменную](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) для хранения статуса выполнения запроса **ExportToPackage**.

    ![Инициализация действия переменной](media/integration-logic-app-initialize-variable-step.png)

6. Подождите, пока статус выполнения экспорта данных станет **Успешно**.

    1. Добавьте [цикл Until](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop), который повторяется до тех пор, пока значение переменной **ExecutionStatus** не будет выполнено **Успешно**.
    2. Добавьте действие **Задержка**, которое ждет пять секунд, прежде чем оно будет опрашивать текущее состояние выполнения экспорта.

        ![Контейнер цикла Until](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > Установите предельное число **15**, чтобы подождать максимум 75 секунд (15 итераций по 5 секунд), чтобы завершить экспорт. Если экспорт занимает больше времени, скорректируйте количество предельных значений.        

    3. Добавьте действие **Вызывать HTTP- запрос** для вызова DMF REST API [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) и задайте переменную **ExecutionStatus** для ответа результата **GetExecutionSummaryStatus**.

        > В этом примере проверка ошибок не выполняется. API **GetExecutionSummaryStatus** может возвращать неудачные состояния терминала (то есть состояние, отличное от **Успешно**). Дополнительные сведения см. в [документации по API](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).

        - **Метод:** POST
        - **URL-адрес запроса:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
        - **Состав запроса:** body('Invoke\_an\_HTTP\_request')?['value']

            > [!NOTE]
            > Возможно, потребуется ввести значение **Состав запроса** либо в представлении кода, либо в редакторе функций конструктора.

        ![Вызов действия запроса HTTP 2](media/integration-logic-app-get-execution-status-step.png)

        ![Определение действия переменной](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > Значение действия **Задать переменную** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) будет отличаться от значения для значения состава **Вызвать HTTP-запрос 2**, даже если в конструкторе будет показаны значения тем же образом.

7. Получите URL-адрес загрузки экспортированного пакета.

    - Добавьте действие **Вызвать HTTP-запрос** для вызова DMF REST API [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl).

        - **Метод:** POST
        - **URL-адрес запроса:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
        - **Состав запроса:** {"executionId": body('GetExportedPackageURL')?['value']}

        ![Действие GetExportedPackageURL](media/integration-logic-app-get-exported-package-step.png)

8. Загрузите экспортированный пакет.

    - Добавьте запрос HTTP **GET** (встроенное [действие соединителя HTTP](https://docs.microsoft.com/azure/connectors/connectors-native-http)) для загрузки пакета по URL-адресу, который был возвращен на предыдущем шаге.

        - **Метод:** GET
        - **URI:** body('Invoke\_an\_HTTP\_request\_3').value

            > [!NOTE]
            > Возможно, потребуется ввести значение **URI** либо в представлении кода, либо в редакторе функций конструктора.

        ![Действие HTTP GET](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > Этот запрос не требует дополнительной аутентификации, так как URL-адрес, возвращаемый API **GetExportedPackageUrl**, включает токен подписей общего доступа, который предоставляет доступ для загрузки файла.

9. Сохраните загруженный пакет, используя [Соединитель OneDrive для бизнеса](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness).

    - Добавьте действие [Создать файл](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) для OneDrive для бизнеса.
    - Подключитесь к учетной записи OneDrive для бизнеса.

        - **Путь к папке:** выбранная папка
        - **Имя файла:** worker\_package.zip
        - **Содержимое файла:** содержимое предыдущего шага (динамическое содержимое)

        ![Действие создания файла](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a>Шаг 3. Проверка приложения логики

Для проверки приложения логики нажмите кнопку **Выполнить** в конструкторе. Вы увидите, что все шаги приложения логики начинают выполняться. После 30–40 секунд приложение логики должно быть завершено, а папка OneDrive для бизнеса должна содержать новый файл пакета, содержащий экспортируемых работников.

Если для какого-либо этапа выводится сообщение об ошибке, выберите неудачный шаг в конструкторе и проверьте для него поля **Вход** и **Выход**. Выполните шаг отладки и корректировки, необходимый для исправления ошибок.

На следующем рисунке показано, как будет выглядеть Logic Apps Designer, когда все этапы приложения логики выполняются успешно.

![Приложение логики успешно выполнено](media/integration-logic-app-successful-run.png)

## <a name="summary"></a>Сводка

В этом учебнике было рассмотрено, как использовать приложение логики для экспорта данных из Human Resources и сохранения экспортированных данных в папке OneDrive для бизнеса. Шаги данного руководства можно изменить, если это необходимо для нужд бизнеса.




[!INCLUDE[footer-include](../includes/footer-banner.md)]