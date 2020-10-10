---
title: Поддерживаемые сценарии для настройки двойной записи
description: В этом разделе описываются сценарии, поддерживаемые для настройки с двойной записью.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b4f69e7933bc5a50cccad6911c99cf08d2768578
ms.sourcegitcommit: b3df62842e62234e8eaa16992375582518976131
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/17/2020
ms.locfileid: "3818604"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="a8cea-103">Поддерживаемые сценарии для настройки двойной записи</span><span class="sxs-lookup"><span data-stu-id="a8cea-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="a8cea-104">Можно настроить подключение с двойной записью между средой Finance and Operations и средой Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a8cea-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="a8cea-105">**Среда Finance and Operations** предоставляет основную платформу для **приложений Finance and Operations** (например, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management и Dynamics 365 Retail).</span><span class="sxs-lookup"><span data-stu-id="a8cea-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="a8cea-106">**Среда Common Data Service** предоставляет основную платформу для **приложений на основе моделей в Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing и Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="a8cea-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="a8cea-107">Модуль Human Resources в Finance and Operations поддерживает подключения с двойной записью, но приложение Dynamics 365 Human Resources не поддерживает.</span><span class="sxs-lookup"><span data-stu-id="a8cea-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="a8cea-108">Механизм настройки различается в зависимости от подписки и среды.</span><span class="sxs-lookup"><span data-stu-id="a8cea-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="a8cea-109">Для новых экземпляров приложений Finance and Operations настройка подключения с двойной записью начинается с Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a8cea-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="a8cea-110">Если у вас есть лицензия на Power Platform, вы получите новую среду Common Data Service, если у клиента ее нет.</span><span class="sxs-lookup"><span data-stu-id="a8cea-110">If you have a license for Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="a8cea-111">Для существующих экземпляров приложений Finance and Operations настройка подключения двойной записи начинается со среды Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8cea-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="a8cea-112">Поддерживаются следующие сценарии настройки:</span><span class="sxs-lookup"><span data-stu-id="a8cea-112">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="a8cea-113">Новый экземпляр приложения Finance and Operations и новый экземпляр приложения на основе модели</span><span class="sxs-lookup"><span data-stu-id="a8cea-113">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="a8cea-114">Новый экземпляр приложения Finance and Operations и существующий экземпляр приложения на основе модели</span><span class="sxs-lookup"><span data-stu-id="a8cea-114">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="a8cea-115">Новый экземпляр приложения Finance and Operations с демонстрационными данными и новый экземпляр приложения на основе модели</span><span class="sxs-lookup"><span data-stu-id="a8cea-115">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="a8cea-116">Новый экземпляр приложения Finance and Operations с демонстрационными данными и существующий экземпляр приложения на основе модели</span><span class="sxs-lookup"><span data-stu-id="a8cea-116">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="a8cea-117">Существующий экземпляр приложения Finance and Operations и новый или существующий экземпляр приложения на основе модели</span><span class="sxs-lookup"><span data-stu-id="a8cea-117">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="a8cea-118">Новый экземпляр приложения Finance and Operations и новый экземпляр приложения на основе модели</span><span class="sxs-lookup"><span data-stu-id="a8cea-118">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="a8cea-119">Для настройки подключения с двойной записью между новым экземпляром приложения Finance and Operations, в котором отсутствуют данные, и новым экземпляром приложения на основе модели в Dynamics 365, выполните действия, указанные в разделе [Настройка двойной записи из Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="a8cea-119">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="a8cea-120">После завершения настройки подключения выполняются следующие действия автоматически:</span><span class="sxs-lookup"><span data-stu-id="a8cea-120">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="a8cea-121">Подготавливается новая пустая среда Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8cea-121">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="a8cea-122">Будет подготовлен новый пустой экземпляр приложения на основе модели, в котором устанавливается простое решение CRM.</span><span class="sxs-lookup"><span data-stu-id="a8cea-122">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="a8cea-123">Для данных компании DAT устанавливается подключение с двойной записью.</span><span class="sxs-lookup"><span data-stu-id="a8cea-123">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="a8cea-124">Сопоставления объектов включаются для синхронизации в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="a8cea-124">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="a8cea-125">Обе среды затем готовы для синхронизации данных в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="a8cea-125">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="a8cea-126">Новый экземпляр приложения Finance and Operations и существующий экземпляр приложения на основе модели</span><span class="sxs-lookup"><span data-stu-id="a8cea-126">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="a8cea-127">Для настройки подключения с двойной записью между новым экземпляром приложения Finance and Operations, в котором отсутствуют данные, и существующим экземпляром приложения на основе модели в Dynamics 365, выполните действия, указанные в разделе [Настройка двойной записи из Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="a8cea-127">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="a8cea-128">После завершения настройки подключения выполняются следующие действия автоматически:</span><span class="sxs-lookup"><span data-stu-id="a8cea-128">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="a8cea-129">Подготавливается новая пустая среда Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8cea-129">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="a8cea-130">Для данных компании DAT устанавливается подключение с двойной записью.</span><span class="sxs-lookup"><span data-stu-id="a8cea-130">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="a8cea-131">Сопоставления объектов включаются для синхронизации в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="a8cea-131">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="a8cea-132">Обе среды затем готовы для синхронизации данных в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="a8cea-132">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="a8cea-133">Чтобы синхронизировать существующие данные Common Data Service с приложением Finance and Operations, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a8cea-133">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="a8cea-134">Создайте новую компанию в приложении Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8cea-134">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="a8cea-135">Добавьте эту компанию в настройку подключения двойной записи.</span><span class="sxs-lookup"><span data-stu-id="a8cea-135">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="a8cea-136">[Выполните начальную загрузку](bootstrap-company-data.md) данных Common Data Service с помощью трехбуквенного кода ISO компании.</span><span class="sxs-lookup"><span data-stu-id="a8cea-136">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="a8cea-137">Поскольку двойная запись является режимом синхронизации в реальном времени, данные из Common Data Service автоматически начинают перетекать в приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8cea-137">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="a8cea-138">Новый экземпляр приложения Finance and Operations с демонстрационными данными и новый экземпляр приложения на основе модели</span><span class="sxs-lookup"><span data-stu-id="a8cea-138">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="a8cea-139">Чтобы настроить подключение с двойной записью между новым экземпляром приложения Finance and Operations, в котором имеются демонстрационные данные, и новым экземпляром приложения на основе модели в Dynamics 365, следуйте указаниям из раздела [Новый экземпляр приложения Finance and Operations и новый экземпляр приложения на основе модели](#new-new) ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="a8cea-139">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="a8cea-140">Если после завершения настройки подключения требуется синхронизировать демонстрационные данные с приложением на основе модели, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a8cea-140">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="a8cea-141">Откройте приложение Finance and Operations на странице LCS, войдите в систему, затем откройте **Управление данными \> Двойная запись**.</span><span class="sxs-lookup"><span data-stu-id="a8cea-141">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="a8cea-142">Выполните функцию **Начальная синхронизация** для тех объектов, для которых требуется синхронизировать данные.</span><span class="sxs-lookup"><span data-stu-id="a8cea-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="a8cea-143">Новый экземпляр приложения Finance and Operations с демонстрационными данными и существующий экземпляр приложения на основе модели</span><span class="sxs-lookup"><span data-stu-id="a8cea-143">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="a8cea-144">Чтобы настроить подключение с двойной записью между новым экземпляром приложения Finance and Operations, в котором имеются демонстрационные данные, и существующим экземпляром приложения на основе модели в Dynamics 365, следуйте указаниям из раздела [Новый экземпляр приложения Finance and Operations и существующий экземпляр приложения на основе модели](#new-existing) ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="a8cea-144">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="a8cea-145">Если после завершения настройки подключения требуется синхронизировать демонстрационные данные с приложением на основе модели, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a8cea-145">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="a8cea-146">Откройте приложение Finance and Operations на странице LCS, войдите в систему, затем откройте **Управление данными \> Двойная запись**.</span><span class="sxs-lookup"><span data-stu-id="a8cea-146">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="a8cea-147">Выполните функцию **Начальная синхронизация** для тех объектов, для которых требуется синхронизировать данные.</span><span class="sxs-lookup"><span data-stu-id="a8cea-147">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="a8cea-148">Чтобы синхронизировать существующие данные Common Data Service с приложением Finance and Operations, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a8cea-148">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="a8cea-149">Создайте новую компанию в приложении Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8cea-149">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="a8cea-150">Добавьте эту компанию в настройку подключения двойной записи.</span><span class="sxs-lookup"><span data-stu-id="a8cea-150">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="a8cea-151">[Выполните начальную загрузку](bootstrap-company-data.md) данных Common Data Service с помощью трехбуквенного кода ISO компании.</span><span class="sxs-lookup"><span data-stu-id="a8cea-151">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="a8cea-152">Поскольку двойная запись является режимом синхронизации в реальном времени, данные из Common Data Service автоматически начинают перетекать в приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8cea-152">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="a8cea-153">Существующий экземпляр приложения Finance and Operations и новый или существующий экземпляр приложения на основе модели</span><span class="sxs-lookup"><span data-stu-id="a8cea-153">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="a8cea-154">Настройка подключения двойной записи между существующим экземпляром приложения Finance and Operations и новым или существующим экземпляром приложения на основе модели в Dynamics 365 производится в среде Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8cea-154">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="a8cea-155">Настройте подключение из приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8cea-155">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="a8cea-156">Чтобы синхронизировать существующие данные Common Data Service с приложением Finance and Operations, необходимо [выполнить загрузку](bootstrap-company-data.md) данных Common Data Service, используя трехбуквенный код компании ISO.</span><span class="sxs-lookup"><span data-stu-id="a8cea-156">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="a8cea-157">Поскольку двойная запись является режимом синхронизации в реальном времени, данные из Common Data Service автоматически начинают перетекать в приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8cea-157">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
