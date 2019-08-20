---
title: Руководство по устранению неполадок при интеграции данных
description: Эта тема предоставляет информацию об устранении неполадок интеграции данных между Microsoft Dynamics 365 for Finance and Operations и Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797283"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="056e1-103">Руководство по устранению неполадок при интеграции данных</span><span class="sxs-lookup"><span data-stu-id="056e1-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a><span data-ttu-id="056e1-104">Включение трассировки подключаемых модулей в Common Data Service и проверка сведений об ошибках подключаемого модуля двойной записи</span><span class="sxs-lookup"><span data-stu-id="056e1-104">Enable Plugin Trace in Common Data Service and check the dual-write Plugin error details</span></span>

<span data-ttu-id="056e1-105">Если вы столкнулись с проблемой или ошибкой с синхронизацией с двойной записью, вы можете проверить ошибки в журнале трассировки:</span><span class="sxs-lookup"><span data-stu-id="056e1-105">If you are facing an issue or error with dual-write synchronization, you can inspect the errors in the trace log:</span></span>

1. <span data-ttu-id="056e1-106">Прежде чем вы сможете проверить ошибки, необходимо включить трассировку подключаемых модулей, используя инструкции в разделе [Регистрация подключаемого модуля](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs), чтобы включить трассировку подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="056e1-106">Before you can inspect the errors, you must enable Plugin trace using the instructions in [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) to enable Plugin trace.</span></span> <span data-ttu-id="056e1-107">Теперь вы можете проверить ошибки.</span><span class="sxs-lookup"><span data-stu-id="056e1-107">Now you can inspect the errors.</span></span>
2. <span data-ttu-id="056e1-108">Выполните вход в Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="056e1-108">Login to Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="056e1-109">Щелкните значок настроек (шестеренка) и выберите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="056e1-109">Click on the Settings icon (a gear), and select **Advanced Settings**.</span></span>
4. <span data-ttu-id="056e1-110">В меню **Настройки** выберите **Настройка > Журнал трассировки подключаемых модулей**.</span><span class="sxs-lookup"><span data-stu-id="056e1-110">In the **Settings** menu, choose **Customization > Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="056e1-111">Нажмите на имя типа **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**, чтобы отобразить детали ошибки.</span><span class="sxs-lookup"><span data-stu-id="056e1-111">Click the type name **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** to display the error details.</span></span>

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="056e1-112">Проверка ошибок синхронизации двойной записи в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="056e1-112">Check dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="056e1-113">Вы можете проверить ошибки во время тестирования, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="056e1-113">You can check the errors during testing by following these steps:</span></span>

+ <span data-ttu-id="056e1-114">Выполните вход в LifeCycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="056e1-114">Login to LifeCycle Services (LCS).</span></span>
+ <span data-ttu-id="056e1-115">Откройте проект LCS, который вы выбрали для выполнения тестирования двойной записи.</span><span class="sxs-lookup"><span data-stu-id="056e1-115">Open the LCS project that you chose to perform dual-write testing.</span></span>
+ <span data-ttu-id="056e1-116">Перейдите в размещенные в облаке среды.</span><span class="sxs-lookup"><span data-stu-id="056e1-116">Go to Cloud Hosted Environments.</span></span>
+ <span data-ttu-id="056e1-117">Удаленный рабочий стол для ВМ Finance and Operations с использованием локальной учетной записи, которая отображается в LCS.</span><span class="sxs-lookup"><span data-stu-id="056e1-117">Remote desktop to Finance and Operations VM using local account that is displayed in LCS.</span></span>
+ <span data-ttu-id="056e1-118">Откройте средство просмотра событий.</span><span class="sxs-lookup"><span data-stu-id="056e1-118">Open the event viewer.</span></span> 
+ <span data-ttu-id="056e1-119">Перейдите по пути **Журналы приложений и служб > Microsoft > Dynamics > AX-DualWriteSync > Операционные**.</span><span class="sxs-lookup"><span data-stu-id="056e1-119">Navigate to **Applications and Services logs > Microsoft > Dynamics > AX-DualWriteSync > Operational**.</span></span> <span data-ttu-id="056e1-120">Отображаются ошибки и детали.</span><span class="sxs-lookup"><span data-stu-id="056e1-120">The errors and details are displayed.</span></span>

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a><span data-ttu-id="056e1-121">Как отвязать среду Common Data Service от Finance and Operations и привязать другую среду</span><span class="sxs-lookup"><span data-stu-id="056e1-121">How to unlink and link another Common Data Service environment from Finance and Operations</span></span>

<span data-ttu-id="056e1-122">Вы можете обновить ссылки, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="056e1-122">You can update links by following these steps:</span></span>

+ <span data-ttu-id="056e1-123">Перейдите в среду Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="056e1-123">Navigate to the Finance and Operations environment.</span></span>
+ <span data-ttu-id="056e1-124">Откройте управление данными.</span><span class="sxs-lookup"><span data-stu-id="056e1-124">Open Data Management.</span></span>
+ <span data-ttu-id="056e1-125">Щелкните **Ссылка на CDS для приложений**.</span><span class="sxs-lookup"><span data-stu-id="056e1-125">Click on **Link to CDS for apps**.</span></span>
+ <span data-ttu-id="056e1-126">Выберите все запущенные отображения и нажмите **Остановить**.</span><span class="sxs-lookup"><span data-stu-id="056e1-126">Select all the running mappings and click **Stop**.</span></span> 
+ <span data-ttu-id="056e1-127">Выберите все отображения и нажмите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="056e1-127">Select all the mappings and click **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="056e1-128">Вариант **Удалить** не появится, если выбран шаблон **CustomerV3-Account**.</span><span class="sxs-lookup"><span data-stu-id="056e1-128">The **Delete** option will not appear if **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="056e1-129">Отмените его выбор, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="056e1-129">Unselect it if needed.</span></span> <span data-ttu-id="056e1-130">**CustomerV3-Account** — это старый подготовленный шаблон, который работает с решением "Перспективный клиент в наличные деньги".</span><span class="sxs-lookup"><span data-stu-id="056e1-130">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="056e1-131">Поскольку он выпущен глобально, он отображается под всеми шаблонами.</span><span class="sxs-lookup"><span data-stu-id="056e1-131">Because it is globally released, it shows up under all templates.</span></span>

+ <span data-ttu-id="056e1-132">Щелкните **Удалить связь со средой**.</span><span class="sxs-lookup"><span data-stu-id="056e1-132">Click **Unlink environment**.</span></span>
+ <span data-ttu-id="056e1-133">Нажмите **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="056e1-133">Click **Yes** for confirmation.</span></span>
+ <span data-ttu-id="056e1-134">Чтобы связать новую среду, выполните шаги из [руководства по установке](https://aka.ms/dualwrite-docs).</span><span class="sxs-lookup"><span data-stu-id="056e1-134">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>

