---
title: Настройка двойной записи из Lifecycle Services
description: В этой теме объясняется, как настроить подключение двойной записи из Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103577"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="403f9-103">Настройка двойной записи из Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="403f9-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="403f9-104">В этой теме объясняется, как включить двойную запись из Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="403f9-104">This topic explains how to enable dual-write from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="403f9-105">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="403f9-105">Prerequisites</span></span>

<span data-ttu-id="403f9-106">Необходимо завершить интеграцию Power Platform, как описано в следующих темах:</span><span class="sxs-lookup"><span data-stu-id="403f9-106">You must complete the Power Platform integration as described in the following topics:</span></span>

+ [<span data-ttu-id="403f9-107">Интеграция Power Platform — включение в ходе развертывания среды</span><span class="sxs-lookup"><span data-stu-id="403f9-107">Power Platform Integration - Enable during environment deployment</span></span>](../../power-platform/overview.md#enable-during-environment-deployment)
+ [<span data-ttu-id="403f9-108">Интеграция Power Platform — настройка после развертывания среды</span><span class="sxs-lookup"><span data-stu-id="403f9-108">Power Platform integration - Set up after environment deployment</span></span>](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a><span data-ttu-id="403f9-109">Настройка двойной записи для новых сред Dataverse</span><span class="sxs-lookup"><span data-stu-id="403f9-109">Set up dual-write for new Dataverse environments</span></span>

<span data-ttu-id="403f9-110">Выполните следующие действия, чтобы настроить двойную запись со страницы **Сведения о среде** LCS:</span><span class="sxs-lookup"><span data-stu-id="403f9-110">Follow these steps to set up dual-write from LCS **Environment Details** page:</span></span>

1. <span data-ttu-id="403f9-111">На странице **Сведения о среде** раскройте раздел **Интеграция Power Platform**.</span><span class="sxs-lookup"><span data-stu-id="403f9-111">On the **Environment Details** page, expand the **Power Platform Integration** section.</span></span>

2. <span data-ttu-id="403f9-112">Выберите кнопку **Приложение двойной записи**.</span><span class="sxs-lookup"><span data-stu-id="403f9-112">Select the **Dual-write application** button.</span></span>

    ![Интеграция Power Platform](media/powerplat_integration_step2.png)

3. <span data-ttu-id="403f9-114">Ознакомьтесь с условиями и выберите **Настроить**.</span><span class="sxs-lookup"><span data-stu-id="403f9-114">Review the terms and conditions, and then select **Configure**.</span></span>

4. <span data-ttu-id="403f9-115">Нажмите **ОК**, чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="403f9-115">Select **OK** to continue.</span></span>

5. <span data-ttu-id="403f9-116">Можно отслеживать ход выполнения, периодически обновляя страницу сведений о среде.</span><span class="sxs-lookup"><span data-stu-id="403f9-116">You can monitor the progress by periodically refreshing the environment details page.</span></span> <span data-ttu-id="403f9-117">Настройка обычно занимает не более 30 минут.</span><span class="sxs-lookup"><span data-stu-id="403f9-117">Setup typically takes 30 minutes or less.</span></span>  

6. <span data-ttu-id="403f9-118">После завершения настройки появится сообщение о том, что процесс был успешным или произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="403f9-118">When the setup is complete, a message will inform you if the process was successful or if there was a failure.</span></span> <span data-ttu-id="403f9-119">Если настройка завершилась с ошибкой, отображается соответствующее сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="403f9-119">If the setup failed, then a related error message is displayed.</span></span> <span data-ttu-id="403f9-120">Перед переходом к следующему шагу необходимо исправить все ошибки.</span><span class="sxs-lookup"><span data-stu-id="403f9-120">You must fix any errors before moving to the next step.</span></span>

7. <span data-ttu-id="403f9-121">Выберите **Связать со средой Power Platform** для создания связи между Dataverse и базами данных текущей среды.</span><span class="sxs-lookup"><span data-stu-id="403f9-121">Select **Link to Power Platform environment** to create a link between Dataverse and the current environment's databases.</span></span> <span data-ttu-id="403f9-122">Это обычно занимает менее 5 минут.</span><span class="sxs-lookup"><span data-stu-id="403f9-122">This typically takes less than 5 minutes.</span></span>

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Связать со средой Power Platform":::

8. <span data-ttu-id="403f9-124">После завершения связывания отображается гиперссылка.</span><span class="sxs-lookup"><span data-stu-id="403f9-124">When the linking is complete, a hyperlink is displayed.</span></span> <span data-ttu-id="403f9-125">Используйте ссылку для входа в область администрирования двойной записи в среде Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="403f9-125">Use the link to sign in to the dual-write administration area in the Finance and Operations environment.</span></span> <span data-ttu-id="403f9-126">Отсюда можно настроить сопоставления сущностей.</span><span class="sxs-lookup"><span data-stu-id="403f9-126">From there, you can set up entity mappings.</span></span>

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a><span data-ttu-id="403f9-127">Настройка двойной записи для существующей среды Dataverse</span><span class="sxs-lookup"><span data-stu-id="403f9-127">Set up dual-write for an existing Dataverse environment</span></span>

<span data-ttu-id="403f9-128">Для настройки двойной записи существующей среды Dataverse необходимо создать [запрос в службу поддержки](../../lifecycle-services/lcs-support.md) Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="403f9-128">To set up dual-write for an existing Dataverse environment, you must create a Microsoft [support ticket](../../lifecycle-services/lcs-support.md).</span></span> <span data-ttu-id="403f9-129">Запрос должен включать следующее:</span><span class="sxs-lookup"><span data-stu-id="403f9-129">The ticket must include:</span></span>

+ <span data-ttu-id="403f9-130">Код вашей среды Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="403f9-130">Your Finance and Operations environment ID.</span></span>
+ <span data-ttu-id="403f9-131">Имя вашей среды из Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="403f9-131">Your environment name from Lifecycle Services.</span></span>
+ <span data-ttu-id="403f9-132">Код организации Dataverse или код среды Power Platform из центра администрирования Power Platform.</span><span class="sxs-lookup"><span data-stu-id="403f9-132">The Dataverse organization ID or Power Platform Environment ID from Power Platform Admin Center.</span></span> <span data-ttu-id="403f9-133">В запросе запросите, чтобы идентификатор был экземпляром, используемым для интеграции Power Platform.</span><span class="sxs-lookup"><span data-stu-id="403f9-133">In your ticket, request that the ID be the instance used for Power Platform integration.</span></span>

> [!NOTE]
> <span data-ttu-id="403f9-134">Невозможно удалить связь среды с помощью LCS.</span><span class="sxs-lookup"><span data-stu-id="403f9-134">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="403f9-135">Чтобы отменить связь среды, откройте рабочую область **Интеграция данных** в среде Finance and Operations, затем выберите **Удалить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="403f9-135">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
