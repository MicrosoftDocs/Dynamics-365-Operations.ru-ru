---
title: Руководство по настройке двойной записи
description: В этом разделе описываются сценарии, поддерживаемые для настройки с двойной записью.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 78a7cdc18476a1c523c83c92ca6f354c3ba806dc
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744861"
---
# <a name="guidance-for-dual-write-setup"></a><span data-ttu-id="95017-103">Руководство по настройке двойной записи</span><span class="sxs-lookup"><span data-stu-id="95017-103">Guidance for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="95017-104">Можно настроить подключение с двойной записью между средой Finance and Operations и средой Dataverse.</span><span class="sxs-lookup"><span data-stu-id="95017-104">You can set up a dual-write connection between a Finance and Operations environment and a Dataverse environment.</span></span>

+ <span data-ttu-id="95017-105">**Среда Finance and Operations** предоставляет основную платформу для **приложений Finance and Operations** (например, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce и Dynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="95017-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="95017-106">**Среда Dataverse** предоставляет основную платформу для **приложений для взаимодействия с клиентами** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing и Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="95017-106">A **Dataverse environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95017-107">Модуль Human Resources в Dynamics 365 Finance поддерживает подключения с двойной записью, но приложение Dynamics 365 Human Resources не поддерживает.</span><span class="sxs-lookup"><span data-stu-id="95017-107">The Human Resources module in Dynamics 365 Finance supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="95017-108">Механизм настройки различается в зависимости от подписки и среды:</span><span class="sxs-lookup"><span data-stu-id="95017-108">The setup mechanism varies, depending on your subscription and the environment:</span></span>

+ <span data-ttu-id="95017-109">Для новых экземпляров приложений Finance and Operations настройка подключения с двойной записью начинается с Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="95017-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="95017-110">Если у вас есть лицензия на Microsoft Power Platform, вы получите новую среду Dataverse, если у клиента ее нет.</span><span class="sxs-lookup"><span data-stu-id="95017-110">If you have a license for Microsoft Power Platform, you will get a new Dataverse environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="95017-111">Для существующих экземпляров приложений Finance and Operations настройка подключения двойной записи начинается со среды Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="95017-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="95017-112">Прежде чем начать двойную запись по сущности, можно выполнить начальную синхронизацию для обработки существующих данных на обеих сторонах: приложений Finance and Operations и приложений для взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="95017-112">Before you start dual-write on an entity, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="95017-113">Исходную синхронизацию можно пропустить, если не требуется синхронизация данных между этими двумя средами.</span><span class="sxs-lookup"><span data-stu-id="95017-113">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="95017-114">Исходная синхронизация позволяет копировать существующие данные из одного приложения в другое двунаправленно.</span><span class="sxs-lookup"><span data-stu-id="95017-114">An initial synchronization lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="95017-115">Существует несколько сценариев настройки, в зависимости от того, какие среды уже имеются, и какие типы данных имеются в них.</span><span class="sxs-lookup"><span data-stu-id="95017-115">There are several setup scenarios, depending on the environments that you already have and the type of data in them.</span></span>

<span data-ttu-id="95017-116">Поддерживаются следующие сценарии настройки:</span><span class="sxs-lookup"><span data-stu-id="95017-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="95017-117">Новый экземпляр приложения Finance and Operations и новый экземпляр приложения взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="95017-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="95017-118">Новый экземпляр приложения Finance and Operations и существующий экземпляр приложения взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="95017-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="95017-119">Новый экземпляр приложения Finance and Operations с данными и новый экземпляр приложения взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="95017-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="95017-120">Новый экземпляр приложения Finance and Operations с данными и существующий экземпляр приложения взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="95017-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="95017-121">Существующий экземпляр приложения Finance and Operations и новый экземпляр приложения взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="95017-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="95017-122">Существующий экземпляр приложения Finance and Operations и существующий экземпляр приложения взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="95017-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="95017-123">Новый экземпляр приложения Finance and Operations и новый экземпляр приложения взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="95017-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="95017-124">Для настройки подключения с двойной записью между новым экземпляром приложения Finance and Operations, в котором отсутствуют данные, и новым экземпляром приложения взаимодействия с клиентами, выполните действия, указанные в разделе [Настройка двойной записи из Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="95017-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="95017-125">После завершения настройки подключения выполняются следующие действия автоматически:</span><span class="sxs-lookup"><span data-stu-id="95017-125">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="95017-126">Подготавливается новая пустая среда Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="95017-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="95017-127">Будет подготовлен новый пустой экземпляр приложения взаимодействия с клиентами, в котором устанавливается простое решение CRM.</span><span class="sxs-lookup"><span data-stu-id="95017-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="95017-128">Для данных компании DAT устанавливается подключение с двойной записью.</span><span class="sxs-lookup"><span data-stu-id="95017-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="95017-129">Сопоставления таблиц включаются для синхронизации в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="95017-129">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="95017-130">Обе среды затем готовы для синхронизации данных в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="95017-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="95017-131">Новый экземпляр приложения Finance and Operations и существующий экземпляр приложения взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="95017-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="95017-132">Для настройки подключения с двойной записью между новым экземпляром приложения Finance and Operations, в котором отсутствуют данные, и существующим экземпляром приложения взаимодействия с клиентами, выполните действия, указанные в разделе [Настройка двойной записи из Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="95017-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="95017-133">После завершения настройки подключения выполняются следующие действия автоматически:</span><span class="sxs-lookup"><span data-stu-id="95017-133">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="95017-134">Подготавливается новая пустая среда Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="95017-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="95017-135">Для данных компании DAT устанавливается подключение с двойной записью.</span><span class="sxs-lookup"><span data-stu-id="95017-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="95017-136">Сопоставления таблиц включаются для синхронизации в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="95017-136">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="95017-137">Обе среды затем готовы для синхронизации данных в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="95017-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="95017-138">Чтобы синхронизировать существующие данные Dataverse с приложением Finance and Operations, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="95017-138">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="95017-139">Создайте новую компанию в приложении Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="95017-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="95017-140">Добавьте эту компанию в настройку подключения двойной записи.</span><span class="sxs-lookup"><span data-stu-id="95017-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="95017-141">[Выполните начальную загрузку](bootstrap-company-data.md) данных Dataverse с помощью трехбуквенного кода ISO компании.</span><span class="sxs-lookup"><span data-stu-id="95017-141">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="95017-142">Выполните функцию **Начальная синхронизация** для тех таблиц, для которых требуется синхронизировать данные.</span><span class="sxs-lookup"><span data-stu-id="95017-142">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="95017-143">Ссылки на пример и альтернативный подход см. в разделе [Пример](#example) ниже в этой теме.</span><span class="sxs-lookup"><span data-stu-id="95017-143">For links to an example and an alternative approach, see the [Example](#example) section later in this topic.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="95017-144">Новый экземпляр приложения Finance and Operations с данными и новый экземпляр приложения взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="95017-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="95017-145">Чтобы настроить подключение с двойной записью между новым экземпляром приложения Finance and Operations, в котором имеются данные, и новым экземпляром приложения взаимодействия с клиентами, следуйте указаниям из раздела [Новый экземпляр приложения Finance and Operations и новый экземпляр приложения взаимодействия с клиентами](#new-new) ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="95017-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="95017-146">Если после завершения настройки подключения требуется синхронизировать данные с приложением взаимодействия с клиентами, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="95017-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="95017-147">Откройте приложение Finance and Operations на странице LCS, войдите в систему, затем откройте **Управление данными \> Двойная запись**.</span><span class="sxs-lookup"><span data-stu-id="95017-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="95017-148">Выполните функцию **Начальная синхронизация** для тех таблиц, для которых требуется синхронизировать данные.</span><span class="sxs-lookup"><span data-stu-id="95017-148">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="95017-149">Ссылки на пример и альтернативный подход см. в разделе [Пример](#example).</span><span class="sxs-lookup"><span data-stu-id="95017-149">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="95017-150">Новый экземпляр приложения Finance and Operations с данными и существующий экземпляр приложения взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="95017-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="95017-151">Чтобы настроить подключение с двойной записью между новым экземпляром приложения Finance and Operations, в котором имеются данные, и существующим экземпляром приложения взаимодействия с клиентами, следуйте указаниям из раздела [Новый экземпляр приложения Finance and Operations и существующий экземпляр приложения взаимодействия с клиентами](#new-existing) ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="95017-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="95017-152">Если после завершения настройки подключения требуется синхронизировать данные с приложением взаимодействия с клиентами, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="95017-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="95017-153">Откройте приложение Finance and Operations на странице LCS, войдите в систему, затем откройте **Управление данными \> Двойная запись**.</span><span class="sxs-lookup"><span data-stu-id="95017-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="95017-154">Выполните функцию **Начальная синхронизация** для тех таблиц, для которых требуется синхронизировать данные.</span><span class="sxs-lookup"><span data-stu-id="95017-154">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="95017-155">Чтобы синхронизировать существующие данные Dataverse с приложением Finance and Operations, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="95017-155">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="95017-156">Создайте новую компанию в приложении Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="95017-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="95017-157">Добавьте эту компанию в настройку подключения двойной записи.</span><span class="sxs-lookup"><span data-stu-id="95017-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="95017-158">[Выполните начальную загрузку](bootstrap-company-data.md) данных Dataverse с помощью трехбуквенного кода ISO компании.</span><span class="sxs-lookup"><span data-stu-id="95017-158">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="95017-159">Выполните функцию **Начальная синхронизация** для тех таблиц, для которых требуется синхронизировать данные.</span><span class="sxs-lookup"><span data-stu-id="95017-159">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="95017-160">Ссылки на пример и альтернативный подход см. в разделе [Пример](#example).</span><span class="sxs-lookup"><span data-stu-id="95017-160">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="95017-161">Существующий экземпляр приложения Finance and Operations и новый экземпляр приложения взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="95017-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="95017-162">Настройка подключения двойной записи между существующим экземпляром приложения Finance and Operations и новым экземпляром приложения взаимодействия с клиентами производится в среде Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="95017-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="95017-163">[Настройте подключение из приложения Finance and Operations](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="95017-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="95017-164">Выполните функцию **Начальная синхронизация** для тех таблиц, для которых требуется синхронизировать данные.</span><span class="sxs-lookup"><span data-stu-id="95017-164">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="95017-165">Ссылки на пример и альтернативный подход см. в разделе [Пример](#example).</span><span class="sxs-lookup"><span data-stu-id="95017-165">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="95017-166">Существующий экземпляр приложения Finance and Operations и существующий экземпляр приложения взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="95017-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="95017-167">Настройка подключения двойной записи между существующим экземпляром приложения Finance and Operations и существующим экземпляром приложения взаимодействия с клиентами производится в среде Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="95017-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="95017-168">[Настройте подключение из приложения Finance and Operations](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="95017-168">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="95017-169">Чтобы синхронизировать существующие данные Dataverse с приложением Finance and Operations, необходимо [выполнить загрузку](bootstrap-company-data.md) данных Dataverse, используя трехбуквенный код компании ISO.</span><span class="sxs-lookup"><span data-stu-id="95017-169">To sync the existing Dataverse data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="95017-170">Выполните функцию **Начальная синхронизация** для тех таблиц, для которых требуется синхронизировать данные.</span><span class="sxs-lookup"><span data-stu-id="95017-170">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="95017-171">Ссылки на пример и альтернативный подход см. в разделе [Пример](#example).</span><span class="sxs-lookup"><span data-stu-id="95017-171">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="example"></a><span data-ttu-id="95017-172">Пример</span><span class="sxs-lookup"><span data-stu-id="95017-172">Example</span></span>

<span data-ttu-id="95017-173">Пример см. в разделе [Включение сопоставления таблиц "Клиенты v3" — "Контакты"](enable-entity-map.md#enable-table-map)</span><span class="sxs-lookup"><span data-stu-id="95017-173">For an example, see [Enabling the Customers V3—Contacts table map](enable-entity-map.md#enable-table-map)</span></span>

<span data-ttu-id="95017-174">Для альтернативного подхода, основанного на томах данных в каждой сущности, требующих выполнения первоначальной синхронизации, см. в разделе [Рекомендации по первоначальной синхронизации](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="95017-174">For an alternative approach that is based on data volumes in each entity that must run an initial synchronization, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
