---
title: Руководство по устранению неполадок при интеграции данных
description: Эта тема предоставляет информацию по устранению неполадок для интеграции данных между приложениями Finance and Operations и Common Data Service.
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
ms.openlocfilehash: 87bdb72024c1c3844ff61e832a92f7edcc77c5d6
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019981"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="ef689-103">Руководство по устранению неполадок при интеграции данных</span><span class="sxs-lookup"><span data-stu-id="ef689-103">Troubleshooting guide for data integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="ef689-104">Включение журналов трассировки подключаемых модулей в Common Data Service и проверка сведений об ошибках подключаемого модуля двойной записи</span><span class="sxs-lookup"><span data-stu-id="ef689-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

<span data-ttu-id="ef689-105">Если возникла проблема или ошибка во время синхронизации с двойной записью, выполните следующие действия для проверки ошибок в журнале трассировки.</span><span class="sxs-lookup"><span data-stu-id="ef689-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="ef689-106">Прежде чем можно будет исследовать ошибки, необходимо включить журналы трассировки подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="ef689-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="ef689-107">Инструкции см. в разделе "Просмотр журналов трассировки" в разделе [Учебник: создание и регистрация подключаемого модуля](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span><span class="sxs-lookup"><span data-stu-id="ef689-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="ef689-108">Теперь вы можете проверить ошибки.</span><span class="sxs-lookup"><span data-stu-id="ef689-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="ef689-109">Войдите в Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="ef689-109">Sign in to Microsoft Dynamics 365 Sales.</span></span>
3. <span data-ttu-id="ef689-110">Выберите кнопку **Настройки** (символ шестеренки), затем выберите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="ef689-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="ef689-111">В меню **Настройки** выберите **Настройка \> Журнал трассировки подключаемых модулей**.</span><span class="sxs-lookup"><span data-stu-id="ef689-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="ef689-112">Выберите имя типа **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**, чтобы отобразить детали ошибки.</span><span class="sxs-lookup"><span data-stu-id="ef689-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors"></a><span data-ttu-id="ef689-113">Проверка ошибок синхронизации двойной записи</span><span class="sxs-lookup"><span data-stu-id="ef689-113">Inspect dual-write synchronization errors</span></span>

<span data-ttu-id="ef689-114">Чтобы исследовать ошибки во время тестирования, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ef689-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="ef689-115">Выполните вход в Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ef689-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="ef689-116">Откройте проект LCS, для которого требуется выполнить тестирование двойной записи.</span><span class="sxs-lookup"><span data-stu-id="ef689-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="ef689-117">Выберите **Размещенные в облаке среды**.</span><span class="sxs-lookup"><span data-stu-id="ef689-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="ef689-118">Создайте подключение удаленного рабочего стола к виртуальной машине (ВМ) приложения, используя локальную учетную запись, отображаемую в LCS.</span><span class="sxs-lookup"><span data-stu-id="ef689-118">Make a Remote desktop connection to the application virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="ef689-119">Откройте средство просмотра событий.</span><span class="sxs-lookup"><span data-stu-id="ef689-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="ef689-120">Выберите **Журналы приложений и служб \> Microsoft \> Dynamics \> AX-DualWriteSync \> Операционные**.</span><span class="sxs-lookup"><span data-stu-id="ef689-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="ef689-121">Отображаются ошибки и детали.</span><span class="sxs-lookup"><span data-stu-id="ef689-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a><span data-ttu-id="ef689-122">Отмена привязки одной среды Common Data Service к приложению и привязка другой среды</span><span class="sxs-lookup"><span data-stu-id="ef689-122">Unlink one Common Data Service environment from the application and link another environment</span></span>

<span data-ttu-id="ef689-123">Выполните эти шаги, чтобы обновить ссылки.</span><span class="sxs-lookup"><span data-stu-id="ef689-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="ef689-124">Перейдите в среду приложения.</span><span class="sxs-lookup"><span data-stu-id="ef689-124">Go to the application environment.</span></span>
2. <span data-ttu-id="ef689-125">Откройте управление данными.</span><span class="sxs-lookup"><span data-stu-id="ef689-125">Open Data Management.</span></span>
3. <span data-ttu-id="ef689-126">Выберите **Ссылка на CDS для приложений**.</span><span class="sxs-lookup"><span data-stu-id="ef689-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="ef689-127">Выберите все выполняющиеся сопоставления, затем выберите **Остановить**.</span><span class="sxs-lookup"><span data-stu-id="ef689-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="ef689-128">Выберите все сопоставления, затем выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="ef689-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef689-129">Вариант **Удалить** недоступен, если выбран шаблон **CustomerV3-Account**.</span><span class="sxs-lookup"><span data-stu-id="ef689-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="ef689-130">При необходимости отмените выбор этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="ef689-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="ef689-131">**CustomerV3-Account** — это старый подготовленный шаблон, который работает с решением "Перспективный клиент в наличные деньги".</span><span class="sxs-lookup"><span data-stu-id="ef689-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="ef689-132">Поскольку он выпущен глобально, он отображается под всеми шаблонами.</span><span class="sxs-lookup"><span data-stu-id="ef689-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="ef689-133">Выберите **Удалить связь со средой**.</span><span class="sxs-lookup"><span data-stu-id="ef689-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="ef689-134">Выберите **Да**, чтобы подтвердить операцию.</span><span class="sxs-lookup"><span data-stu-id="ef689-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="ef689-135">Чтобы связать новую среду, выполните шаги из [руководства по установке](https://aka.ms/dualwrite-docs).</span><span class="sxs-lookup"><span data-stu-id="ef689-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
