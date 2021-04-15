---
title: Создание приложения для повторяющегося экспорта данных
description: В этой статье описывается создание приложения логики Microsoft Azure, которое экспортирует данные из Microsoft Dynamics 365 Human Resources по регулярному расписанию.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3d7fc01906a017d4214d4794097a11b4a3416b95
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801127"
---
# <a name="create-a-recurring-data-export-app"></a><span data-ttu-id="6ed5e-103">Создание приложения для повторяющегося экспорта данных</span><span class="sxs-lookup"><span data-stu-id="6ed5e-103">Create a recurring data export app</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6ed5e-104">В этой статье описывается создание приложения логики Microsoft Azure, которое экспортирует данные из Microsoft Dynamics 365 Human Resources по регулярному расписанию.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-104">This article shows how to create a Microsoft Azure logic app that exports data from Microsoft Dynamics 365 Human Resources on a recurring schedule.</span></span> <span data-ttu-id="6ed5e-105">В учебнике для экспорта данных используется API пакета DMF REST Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-105">The tutorial takes advantage of Human Resources' DMF package REST application programming interface (API) to export the data.</span></span> <span data-ttu-id="6ed5e-106">После экспорта данных приложение логики сохраняет экспортированный пакет данных в папке Microsoft OneDrive для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-106">After the data has been exported, the logic app saves the exported data package to a Microsoft OneDrive for Business folder.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="6ed5e-107">Бизнес-сценарий</span><span class="sxs-lookup"><span data-stu-id="6ed5e-107">Business scenario</span></span>

<span data-ttu-id="6ed5e-108">В одном обычном бизнес-сценарии для интеграции Microsoft Dynamics 365 данные должны быть экспортированы в нисходящий элемент в повторяющемся расписании.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-108">In one typical business scenario for Microsoft Dynamics 365 integrations, data must be exported to a downstream system on a recurring schedule.</span></span> <span data-ttu-id="6ed5e-109">В этом учебнике описывается, как экспортировать все записи работников из Microsoft Dynamics 365 Human Resources и сохранить список работников в папке OneDrive для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-109">This tutorial shows how to export all worker records from Microsoft Dynamics 365 Human Resources and save the list of workers in a OneDrive for Business folder.</span></span>

> [!TIP]
> <span data-ttu-id="6ed5e-110">Данные, экспортируемые в этом учебнике, и назначение экспортированных данных представляют собой только примеры.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-110">The specific data that is exported in this tutorial and the destination of the exported data are only examples.</span></span> <span data-ttu-id="6ed5e-111">Их можно легко изменить в зависимости от потребностей бизнеса.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-111">You can easily change them to meet your business needs.</span></span>

## <a name="technologies-used"></a><span data-ttu-id="6ed5e-112">Используемые технологии</span><span class="sxs-lookup"><span data-stu-id="6ed5e-112">Technologies used</span></span>

<span data-ttu-id="6ed5e-113">В этом учебнике используются следующие технологии:</span><span class="sxs-lookup"><span data-stu-id="6ed5e-113">This tutorial uses the following technologies:</span></span>

- <span data-ttu-id="6ed5e-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** — Главный источник данных для работников, которые будут экспортированы.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – The master data source for workers that will be exported.</span></span>
- <span data-ttu-id="6ed5e-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** — технология, обеспечивающая согласование и планирование повторяющегося экспорта.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – The technology that provides orchestration and scheduling of the recurring export.</span></span>

    - <span data-ttu-id="6ed5e-116">**[Соединители](https://docs.microsoft.com/azure/connectors/apis-list)** — технология, используемая для подключения приложения логики к необходимым конечным точкам.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-116">**[Connectors](https://docs.microsoft.com/azure/connectors/apis-list)** – The technology that is used to connect the logic app to the required endpoints.</span></span>

        - <span data-ttu-id="6ed5e-117">[HTTP с соединителем Azure AD](https://docs.microsoft.com/connectors/webcontents/)</span><span class="sxs-lookup"><span data-stu-id="6ed5e-117">[HTTP with Azure AD](https://docs.microsoft.com/connectors/webcontents/) connector</span></span>
        - <span data-ttu-id="6ed5e-118">Соединитель [OneDrive для бизнеса](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)</span><span class="sxs-lookup"><span data-stu-id="6ed5e-118">[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector</span></span>

- <span data-ttu-id="6ed5e-119">**[Пакет DMF REST API](../dev-itpro/data-entities/data-management-api.md)** — технология, используемая для запуска экспорта и отслеживания его выполнения.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-119">**[DMF package REST API](../dev-itpro/data-entities/data-management-api.md)** – The technology that is used to trigger the export and monitor its progress.</span></span>
- <span data-ttu-id="6ed5e-120">**[OneDrive для бизнеса](https://onedrive.live.com/about/business/)** — место назначения для экспортируемых работников.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – The destination for the exported workers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6ed5e-121">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="6ed5e-121">Prerequisites</span></span>

<span data-ttu-id="6ed5e-122">Прежде чем приступить к выполнению упражнения данного учебника, необходимо иметь следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="6ed5e-122">Before you begin the exercise in this tutorial, you must have the following items:</span></span>

- <span data-ttu-id="6ed5e-123">Среда Human Resources, имеющая разрешения уровня администратора в среде</span><span class="sxs-lookup"><span data-stu-id="6ed5e-123">A Human Resources environment that has admin-level permissions in the environment</span></span>
- <span data-ttu-id="6ed5e-124">[Подписка Azure](https://azure.microsoft.com/free/) для размещения приложения логики</span><span class="sxs-lookup"><span data-stu-id="6ed5e-124">An [Azure subscription](https://azure.microsoft.com/free/) to host the logic app</span></span>

## <a name="the-exercise"></a><span data-ttu-id="6ed5e-125">Упражнение</span><span class="sxs-lookup"><span data-stu-id="6ed5e-125">The exercise</span></span>

<span data-ttu-id="6ed5e-126">В конце этого упражнения у вас будет приложение логики, связанное с вашей средой Human Resources и вашей учетной записью OneDrive для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-126">At the end of this exercise, you will have a logic app that is connected to your Human Resources environment and your OneDrive for Business account.</span></span> <span data-ttu-id="6ed5e-127">Приложение логики экспортирует пакет данных из Human Resources, дождитесь завершения экспорта, загрузите экспортированный пакет данных и сохраните пакет данных в указанную папку OneDrive для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-127">The logic app will export a data package from Human Resources, wait for the export to be completed, download the exported data package, and save the data package in the OneDrive for Business folder that you specified.</span></span>

<span data-ttu-id="6ed5e-128">Готовое приложение логики будет похоже на следующее.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-128">The completed logic app will resemble the following illustration.</span></span>

![Обзор приложения логики](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a><span data-ttu-id="6ed5e-130">Шаг 1. Создание проекта экспорта данных в Human Resources</span><span class="sxs-lookup"><span data-stu-id="6ed5e-130">Step 1: Create a data export project in Human Resources</span></span>

<span data-ttu-id="6ed5e-131">В Human Resources создайте проект экспорта данных, экспортирующий работников.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-131">In Human Resources, create a data export project that exports workers.</span></span> <span data-ttu-id="6ed5e-132">Назовите проект **Export Workers** и убедитесь , что для параметра **Создать пакет данных** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-132">Name the project **Export Workers**, and make sure that the **Generate data package** option is set to **Yes**.</span></span> <span data-ttu-id="6ed5e-133">Добавьте один объект (**Работник**) в проект и выберите формат, в котором выполняется экспорт.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-133">Add a single entity (**Worker**) to the project, and select the format to export in.</span></span> <span data-ttu-id="6ed5e-134">(Формат Microsoft Excel используется в данном учебнике.)</span><span class="sxs-lookup"><span data-stu-id="6ed5e-134">(Microsoft Excel format is used in this tutorial.)</span></span>

![Экспорт проекта данных о работниках](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> <span data-ttu-id="6ed5e-136">Помните название проекта экспорта данных.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-136">Remember the name of the data export project.</span></span> <span data-ttu-id="6ed5e-137">Это потребуется при создании приложения логики на следующем шаге.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-137">You will need it when you create the logic app in the next step.</span></span>

### <a name="step-2-create-the-logic-app"></a><span data-ttu-id="6ed5e-138">Шаг 2. Создание приложения логики</span><span class="sxs-lookup"><span data-stu-id="6ed5e-138">Step 2: Create the logic app</span></span>

<span data-ttu-id="6ed5e-139">Здесь создается приложение логики.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-139">The bulk of the exercise involves creating the logic app.</span></span>

1. <span data-ttu-id="6ed5e-140">На портале Azure создайте приложение логики.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-140">In the Azure portal, create a logic app.</span></span>

    ![Страница создания приложения логики](media/integration-logic-app-creation-1.png)

2. <span data-ttu-id="6ed5e-142">В Logic Apps Designer начнем с чистого приложения логики.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-142">In the Logic Apps Designer, start with a blank logic app.</span></span>
3. <span data-ttu-id="6ed5e-143">Добавьте [Триггер расписания повторения](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) для запуска приложения логики каждые 24 часа (или в соответствии с выбранным расписанием).</span><span class="sxs-lookup"><span data-stu-id="6ed5e-143">Add a [Recurrence Schedule trigger](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) to run the logic app every 24 hours (or according to a schedule of your choice).</span></span>

    ![Диалоговое окно повторения](media/integration-logic-app-recurrence-step.png)

4. <span data-ttu-id="6ed5e-145">Вызовите DMF REST API [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage), чтобы запланировать экспорт пакета данных.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-145">Call the [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API to schedule the export of your data package.</span></span>

    1. <span data-ttu-id="6ed5e-146">Используйте действие **Вызвать запрос HTTP** из HTTP с соединителем Azure AD.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-146">Use the **Invoke an HTTP request** action from the HTTP with Azure AD connector.</span></span>

        - <span data-ttu-id="6ed5e-147">**URL-адрес базового ресурса:** URL-адрес вашей среды Human Resources (не включайте информацию о пути и пространстве имен.)</span><span class="sxs-lookup"><span data-stu-id="6ed5e-147">**Base Resource URL:** The URL of your Human Resources environment (Don't include path/namespace information.)</span></span>
        - <span data-ttu-id="6ed5e-148">**URI-адрес ресурса Azure AD:** `http://hr.talent.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="6ed5e-148">**Azure AD Resource URI:** `http://hr.talent.dynamics.com`</span></span>

        > [!NOTE]
        > <span data-ttu-id="6ed5e-149">Служба Human Resources еще не предоставляет соединитель, который предоставляет все API REST, которые составляют пакет DMF REST API, например, **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-149">The Human Resources service doesn't yet provide a connector that exposes all the APIs that make up the DMF package REST API, such as **ExportToPackage**.</span></span> <span data-ttu-id="6ed5e-150">Вместо этого необходимо вызывать API с помощью необработанных запросов HTTPS через HTTP с соединителем Azure AD.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-150">Instead, you must call the APIs by using raw HTTPS requests through the HTTP with Azure AD connector.</span></span> <span data-ttu-id="6ed5e-151">Этот разъем использует Azure Active Directory (Azure AD) для аутентификации и авторизации в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-151">This connector uses Azure Active Directory (Azure AD) for authentication and authorization to Human Resources.</span></span>

        ![HTTP с соединителем Azure AD](media/integration-logic-app-http-aad-connector-step.png)

    2. <span data-ttu-id="6ed5e-153">Выполните вход в среду Human Resources с помощью HTTP с соединителем Azure AD.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-153">Sign in to your Human Resources environment through the HTTP with Azure AD connector.</span></span>
    3. <span data-ttu-id="6ed5e-154">Настройте запрос HTTP **POST** для вызова DMF REST API **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-154">Set up an HTTP **POST** request to call the **ExportToPackage** DMF REST API.</span></span>

        - <span data-ttu-id="6ed5e-155">**Метод:** POST</span><span class="sxs-lookup"><span data-stu-id="6ed5e-155">**Method:** POST</span></span>
        - <span data-ttu-id="6ed5e-156">**URL-адрес запроса:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="6ed5e-156">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span></span>
        - <span data-ttu-id="6ed5e-157">**Состав запроса:**</span><span class="sxs-lookup"><span data-stu-id="6ed5e-157">**Body of the request:**</span></span>

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
    > <span data-ttu-id="6ed5e-159">Возможно, потребуется переименовать каждый шаг, чтобы он более был более значимым, чем имя по умолчанию, **Вызвать HTTP-запрос**.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-159">You might want to rename each step so that it's more meaningful than the default name, **Invoke an HTTP request**.</span></span> <span data-ttu-id="6ed5e-160">Например, можно переименовать этот шаг **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-160">For example, you can rename this step **ExportToPackage**.</span></span>

5. <span data-ttu-id="6ed5e-161">[Инициализируйте переменную](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) для хранения статуса выполнения запроса **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-161">[Initialize a variable](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) to store the execution status of the **ExportToPackage** request.</span></span>

    ![Инициализация действия переменной](media/integration-logic-app-initialize-variable-step.png)

6. <span data-ttu-id="6ed5e-163">Подождите, пока статус выполнения экспорта данных станет **Успешно**.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-163">Wait until the execution status of the data export is **Succeeded**.</span></span>

    1. <span data-ttu-id="6ed5e-164">Добавьте [цикл Until](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop), который повторяется до тех пор, пока значение переменной **ExecutionStatus** не будет выполнено **Успешно**.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-164">Add an [Until loop](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) that repeats until the value of the **ExecutionStatus** variable is **Succeeded**.</span></span>
    2. <span data-ttu-id="6ed5e-165">Добавьте действие **Задержка**, которое ждет пять секунд, прежде чем оно будет опрашивать текущее состояние выполнения экспорта.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-165">Add a **Delay** action that waits five seconds before it polls for the current execution status of the export.</span></span>

        ![Контейнер цикла Until](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > <span data-ttu-id="6ed5e-167">Установите предельное число **15**, чтобы подождать максимум 75 секунд (15 итераций по 5 секунд), чтобы завершить экспорт.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-167">Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="6ed5e-168">Если экспорт занимает больше времени, скорректируйте количество предельных значений.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-168">If your export takes more time, adjust the limit count as appropriate.</span></span>        

    3. <span data-ttu-id="6ed5e-169">Добавьте действие **Вызывать HTTP- запрос** для вызова DMF REST API [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) и задайте переменную **ExecutionStatus** для ответа результата **GetExecutionSummaryStatus**.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-169">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>

        > <span data-ttu-id="6ed5e-170">В этом примере проверка ошибок не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-170">This sample doesn't do error checking.</span></span> <span data-ttu-id="6ed5e-171">API **GetExecutionSummaryStatus** может возвращать неудачные состояния терминала (то есть состояние, отличное от **Успешно**).</span><span class="sxs-lookup"><span data-stu-id="6ed5e-171">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="6ed5e-172">Дополнительные сведения см. в [документации по API](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span><span class="sxs-lookup"><span data-stu-id="6ed5e-172">For more information, see the [API documentation](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

        - <span data-ttu-id="6ed5e-173">**Метод:** POST</span><span class="sxs-lookup"><span data-stu-id="6ed5e-173">**Method:** POST</span></span>
        - <span data-ttu-id="6ed5e-174">**URL-адрес запроса:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="6ed5e-174">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span></span>
        - <span data-ttu-id="6ed5e-175">**Состав запроса:** body('Invoke\_an\_HTTP\_request')?['value']</span><span class="sxs-lookup"><span data-stu-id="6ed5e-175">**Body of the request:** body('Invoke\_an\_HTTP\_request')?['value']</span></span>

            > [!NOTE]
            > <span data-ttu-id="6ed5e-176">Возможно, потребуется ввести значение **Состав запроса** либо в представлении кода, либо в редакторе функций конструктора.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-176">You might have to enter the **Body of the request** value either in code view or in the function editor in the designer.</span></span>

        ![Вызов действия запроса HTTP 2](media/integration-logic-app-get-execution-status-step.png)

        ![Определение действия переменной](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > <span data-ttu-id="6ed5e-179">Значение действия **Задать переменную** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) будет отличаться от значения для значения состава **Вызвать HTTP-запрос 2**, даже если в конструкторе будет показаны значения тем же образом.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-179">The value for the **Set variable** action (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) will differ from the value for the **Invoke an HTTP request 2** body value, even though the designer will show the values in the same way.</span></span>

7. <span data-ttu-id="6ed5e-180">Получите URL-адрес загрузки экспортированного пакета.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-180">Get the download URL of the exported package.</span></span>

    - <span data-ttu-id="6ed5e-181">Добавьте действие **Вызвать HTTP-запрос** для вызова DMF REST API [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl).</span><span class="sxs-lookup"><span data-stu-id="6ed5e-181">Add an **Invoke HTTP request** action to call the [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span></span>

        - <span data-ttu-id="6ed5e-182">**Метод:** POST</span><span class="sxs-lookup"><span data-stu-id="6ed5e-182">**Method:** POST</span></span>
        - <span data-ttu-id="6ed5e-183">**URL-адрес запроса:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="6ed5e-183">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span></span>
        - <span data-ttu-id="6ed5e-184">**Состав запроса:** {"executionId": body('GetExportedPackageURL')?['value']}</span><span class="sxs-lookup"><span data-stu-id="6ed5e-184">**Body of the request:** {"executionId": body('GetExportedPackageURL')?['value']}</span></span>

        ![Действие GetExportedPackageURL](media/integration-logic-app-get-exported-package-step.png)

8. <span data-ttu-id="6ed5e-186">Загрузите экспортированный пакет.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-186">Download the exported package.</span></span>

    - <span data-ttu-id="6ed5e-187">Добавьте запрос HTTP **GET** (встроенное [действие соединителя HTTP](https://docs.microsoft.com/azure/connectors/connectors-native-http)) для загрузки пакета по URL-адресу, который был возвращен на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-187">Add an HTTP **GET** request (a built-in [HTTP connector action](https://docs.microsoft.com/azure/connectors/connectors-native-http)) to download the package from the URL that was returned in the previous step.</span></span>

        - <span data-ttu-id="6ed5e-188">**Метод:** GET</span><span class="sxs-lookup"><span data-stu-id="6ed5e-188">**Method:** GET</span></span>
        - <span data-ttu-id="6ed5e-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span><span class="sxs-lookup"><span data-stu-id="6ed5e-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="6ed5e-190">Возможно, потребуется ввести значение **URI** либо в представлении кода, либо в редакторе функций конструктора.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-190">You might have to enter the **URI** value either in code view or in the function editor in the designer.</span></span>

        ![Действие HTTP GET](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > <span data-ttu-id="6ed5e-192">Этот запрос не требует дополнительной аутентификации, так как URL-адрес, возвращаемый API **GetExportedPackageUrl**, включает токен подписей общего доступа, который предоставляет доступ для загрузки файла.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-192">This request doesn't require any additional authentication, because the URL that the **GetExportedPackageUrl** API returns includes a shared access signatures token that grants access to download the file.</span></span>

9. <span data-ttu-id="6ed5e-193">Сохраните загруженный пакет, используя [Соединитель OneDrive для бизнеса](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness).</span><span class="sxs-lookup"><span data-stu-id="6ed5e-193">Save the downloaded package by using the [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector.</span></span>

    - <span data-ttu-id="6ed5e-194">Добавьте действие [Создать файл](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) для OneDrive для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-194">Add a OneDrive for Business [Create File](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) action.</span></span>
    - <span data-ttu-id="6ed5e-195">Подключитесь к учетной записи OneDrive для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-195">Connect to your OneDrive for Business account, as required.</span></span>

        - <span data-ttu-id="6ed5e-196">**Путь к папке:** выбранная папка</span><span class="sxs-lookup"><span data-stu-id="6ed5e-196">**Folder Path:** A folder of your choice</span></span>
        - <span data-ttu-id="6ed5e-197">**Имя файла:** worker\_package.zip</span><span class="sxs-lookup"><span data-stu-id="6ed5e-197">**File Name:** worker\_package.zip</span></span>
        - <span data-ttu-id="6ed5e-198">**Содержимое файла:** содержимое предыдущего шага (динамическое содержимое)</span><span class="sxs-lookup"><span data-stu-id="6ed5e-198">**File Content:** The body from the previous step (dynamic content)</span></span>

        ![Действие создания файла](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a><span data-ttu-id="6ed5e-200">Шаг 3. Проверка приложения логики</span><span class="sxs-lookup"><span data-stu-id="6ed5e-200">Step 3: Test the logic app</span></span>

<span data-ttu-id="6ed5e-201">Для проверки приложения логики нажмите кнопку **Выполнить** в конструкторе.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-201">To test your logic app, select the **Run** button in the designer.</span></span> <span data-ttu-id="6ed5e-202">Вы увидите, что все шаги приложения логики начинают выполняться.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-202">You will see that the steps of the logic app start to run.</span></span> <span data-ttu-id="6ed5e-203">После 30–40 секунд приложение логики должно быть завершено, а папка OneDrive для бизнеса должна содержать новый файл пакета, содержащий экспортируемых работников.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-203">After 30 to 40 seconds, the logic app should finish running, and your OneDrive for Business folder should include a new package file that contains the exported workers.</span></span>

<span data-ttu-id="6ed5e-204">Если для какого-либо этапа выводится сообщение об ошибке, выберите неудачный шаг в конструкторе и проверьте для него поля **Вход** и **Выход**.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-204">If a failure is reported for any step, select the failed step in the designer, and examine the **Inputs** and **Outputs** fields for it.</span></span> <span data-ttu-id="6ed5e-205">Выполните шаг отладки и корректировки, необходимый для исправления ошибок.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-205">Debug and adjust the step as required to correct the errors.</span></span>

<span data-ttu-id="6ed5e-206">На следующем рисунке показано, как будет выглядеть Logic Apps Designer, когда все этапы приложения логики выполняются успешно.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-206">The following illustration shows what the Logic Apps Designer looks like when all the steps of the logic app run successfully.</span></span>

![Приложение логики успешно выполнено](media/integration-logic-app-successful-run.png)

## <a name="summary"></a><span data-ttu-id="6ed5e-208">Сводка</span><span class="sxs-lookup"><span data-stu-id="6ed5e-208">Summary</span></span>

<span data-ttu-id="6ed5e-209">В этом учебнике было рассмотрено, как использовать приложение логики для экспорта данных из Human Resources и сохранения экспортированных данных в папке OneDrive для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-209">In this tutorial, you learned how to use a logic app to export data from Human Resources and save the exported data to a OneDrive for Business folder.</span></span> <span data-ttu-id="6ed5e-210">Шаги данного руководства можно изменить, если это необходимо для нужд бизнеса.</span><span class="sxs-lookup"><span data-stu-id="6ed5e-210">You can modify the steps of this tutorial as required to suit your business needs.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]