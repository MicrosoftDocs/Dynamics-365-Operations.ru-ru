---
title: Установка надстройки аналитики Интернета вещей в LCS
description: В этом разделе объясняется, как установить надстройки аналитики Интернета вещей в Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d55ca1975589699cbce03dcc7bf81e0762738d24
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963493"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="ed77b-103">Установка надстройки аналитики Интернета вещей в LCS</span><span class="sxs-lookup"><span data-stu-id="ed77b-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ed77b-104">В этом разделе объясняется, как установить надстройки аналитики Интернета вещей в Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ed77b-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="ed77b-105">Обратите внимание, что надстройки невозможно установить в демонстрационной или пробной среде.</span><span class="sxs-lookup"><span data-stu-id="ed77b-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="ed77b-106">Прежде чем можно будет установить надстройку, необходимо [создать ресурсы Azure](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="ed77b-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="ed77b-107">Настройка среды LCS</span><span class="sxs-lookup"><span data-stu-id="ed77b-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="ed77b-108">Откройте LCS и перейдите в вашу среду Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ed77b-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="ed77b-109">Перейдите в раздел **Надстройки среды**.</span><span class="sxs-lookup"><span data-stu-id="ed77b-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="ed77b-110">Выберите **установить новую надстройку** для отображения списка надстроек, включенных в среду.</span><span class="sxs-lookup"><span data-stu-id="ed77b-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="ed77b-111">В диалоговом окне **Выбор надстройки для установки** выберите **аналитики Интернета вещей**.</span><span class="sxs-lookup"><span data-stu-id="ed77b-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="ed77b-112">В диалоговом окне **Установка надстройки** предоставьте сведения об узле Интернета вещей и кэше Redis.</span><span class="sxs-lookup"><span data-stu-id="ed77b-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="ed77b-113">Необходимые значения можно найти в своем хранилище ключей, созданном при [создании ресурсов Azure](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="ed77b-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="ed77b-114">**Код клиента** — в портале Azure перейдите в хранилище ключей, а затем в левой области перехода выберите **Обзор** и скопируйте значение **код каталога**.</span><span class="sxs-lookup"><span data-stu-id="ed77b-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="ed77b-115">Вставьте это значение в диалоговое окно **Установка надстройки**.</span><span class="sxs-lookup"><span data-stu-id="ed77b-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="ed77b-116">**URI хранилища ключей конечной точки, совместимой с центром событий Интернета вещей** — перейдите в хранилище ключей, а затем в левой области перехода выберите **Обзор** и скопируйте значение **имени DNS**.</span><span class="sxs-lookup"><span data-stu-id="ed77b-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="ed77b-117">Вставьте это значение в диалоговое окно **Установка надстройки**.</span><span class="sxs-lookup"><span data-stu-id="ed77b-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="ed77b-118">**Имя секрета конечной точки, совместимой с центром событий Интернета вещей** — перейдите в хранилище ключей, а затем в левой области перехода выберите **секреты** и скопируйте имя секрета, в котором хранится строка подключения к центру событий для узла Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="ed77b-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="ed77b-119">Вставьте это значение в диалоговое окно **Установка надстройки**.</span><span class="sxs-lookup"><span data-stu-id="ed77b-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="ed77b-120">**URI хранилища ключей кэша Redis** — перейдите в хранилище ключей, а затем в левой области перехода выберите **Обзор** и скопируйте значение **имени DNS**.</span><span class="sxs-lookup"><span data-stu-id="ed77b-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="ed77b-121">Вставьте это значение в диалоговое окно **Установка надстройки**.</span><span class="sxs-lookup"><span data-stu-id="ed77b-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="ed77b-122">**Имя секрета конечной точки кэша Redis** — перейдите в хранилище ключей, а затем в левой области перехода выберите **секреты** и скопируйте имя секрета, в котором хранится строка подключения для узла кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="ed77b-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="ed77b-123">Вставьте это значение в диалоговое окно **Установка надстройки**.</span><span class="sxs-lookup"><span data-stu-id="ed77b-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="ed77b-124">Установите этот флажок, чтобы принять условия.</span><span class="sxs-lookup"><span data-stu-id="ed77b-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="ed77b-125">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="ed77b-125">Select **Install**.</span></span>
8. <span data-ttu-id="ed77b-126">Появляется окно сообщения, в котором указано, что "надстройка была успешно активирована для установки".</span><span class="sxs-lookup"><span data-stu-id="ed77b-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="ed77b-127">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ed77b-127">Select **OK**.</span></span>

<span data-ttu-id="ed77b-128">Настройка LCS завершена.</span><span class="sxs-lookup"><span data-stu-id="ed77b-128">LCS setup is now completed.</span></span> <span data-ttu-id="ed77b-129">Следующим шагом является [Настройка сценариев](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="ed77b-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="ed77b-130">Удаление надстройки</span><span class="sxs-lookup"><span data-stu-id="ed77b-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="ed77b-131">В Supply Chain Management [отключите сценарии](iot-scenario-setup.md#disable-a-scenario).</span><span class="sxs-lookup"><span data-stu-id="ed77b-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#disable-a-scenario).</span></span>
2. <span data-ttu-id="ed77b-132">В LCS, перейдите к сведениям о вашей среде Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ed77b-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="ed77b-133">Перейдите в раздел **Надстройки среды**.</span><span class="sxs-lookup"><span data-stu-id="ed77b-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="ed77b-134">Выберите **Удаление** для надстройки аналитики Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="ed77b-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>
