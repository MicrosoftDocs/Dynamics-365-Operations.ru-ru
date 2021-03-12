---
title: Обзор каналов
description: Этот раздел содержит обзор каналов в Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e060fe2a578296f079653244ed4d5676313e5ea8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963068"
---
# <a name="channels-overview"></a><span data-ttu-id="97c74-103">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="97c74-103">Channels overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="97c74-104">Этот раздел содержит обзор каналов в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="97c74-104">This topic presents an overview of channels in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="97c74-105">Она содержит сведения о задачах, которую следует выполнить как до, так и после настройки каждого канала.</span><span class="sxs-lookup"><span data-stu-id="97c74-105">It includes information about the tasks that you must complete both before and after you set up each channel.</span></span>

## <a name="types-of-channels"></a><span data-ttu-id="97c74-106">Типы каналов</span><span class="sxs-lookup"><span data-stu-id="97c74-106">Types of Channels</span></span>

<span data-ttu-id="97c74-107">Dynamics 365 Commerce поддерживает три различных типа каналов: розница, центр обработки вызовов и интернет-каналы.</span><span class="sxs-lookup"><span data-stu-id="97c74-107">Dynamics 365 Commerce supports three different channel types: retail, call center, and online channels.</span></span>

### <a name="retail-channels"></a><span data-ttu-id="97c74-108">Каналы розничной торговли</span><span class="sxs-lookup"><span data-stu-id="97c74-108">Retail channels</span></span>

<span data-ttu-id="97c74-109">Каналы розничной торговли представляют собой стандартные физические магазины.</span><span class="sxs-lookup"><span data-stu-id="97c74-109">Retail channels represent standard brick-and-mortar stores.</span></span> <span data-ttu-id="97c74-110">У каждого магазина свои кассы POS, приходные и расходные счета и персонал.</span><span class="sxs-lookup"><span data-stu-id="97c74-110">Each store can have its own point of sale (POS) registers, income and expense accounts, and staff.</span></span> 

### <a name="call-center-channels"></a><span data-ttu-id="97c74-111">Каналы центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="97c74-111">Call center channels</span></span>

<span data-ttu-id="97c74-112">Каналы центра обработки вызовов представляют порядок и управление клиентами в центре обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="97c74-112">Call center channels represent call center order and customer management.</span></span>

### <a name="online-channels"></a><span data-ttu-id="97c74-113">Интерактивные каналы</span><span class="sxs-lookup"><span data-stu-id="97c74-113">Online channels</span></span>

<span data-ttu-id="97c74-114">Интернет-каналы представляют собой интернет-магазины электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="97c74-114">Online channels represent online e-Commerce storefronts.</span></span> <span data-ttu-id="97c74-115">После создания интернет-канала необходимо создать сайт с помощью построителя сайтов Microsoft Dynamics 365 Commerce или другого решения электронной коммерции сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="97c74-115">Once an online channel is created, a site must be created using the Microsoft Dynamics 365 Commerce Site Builder tool or other third-party e-Commerce solution.</span></span>

## <a name="channel-setup-basics"></a><span data-ttu-id="97c74-116">Основы настройки канала</span><span class="sxs-lookup"><span data-stu-id="97c74-116">Channel setup basics</span></span>

<span data-ttu-id="97c74-117">Настройка канала выполняется в инструменте Commerce.</span><span class="sxs-lookup"><span data-stu-id="97c74-117">Channel set up is performed in the Commerce tool.</span></span> <span data-ttu-id="97c74-118">У каждого канала могут быть собственные методы оплаты, ценовые группы, иерархии продуктов, ассортименты и набор продуктов.</span><span class="sxs-lookup"><span data-stu-id="97c74-118">Each channel can have its own payment methods, price groups, product hierarchies, assortments, and set of products.</span></span> <span data-ttu-id="97c74-119">После создания канала назначаются продукты, которые должны использоваться и продаваться в магазине.</span><span class="sxs-lookup"><span data-stu-id="97c74-119">After you create a channel, you assign the products that you want it to carry and sell.</span></span> <span data-ttu-id="97c74-120">Каждый тип канала имеет уникальный набор функций, которые могут может потребоваться настроить.</span><span class="sxs-lookup"><span data-stu-id="97c74-120">Each channel type has a unique set of features that may need to be configured.</span></span> <span data-ttu-id="97c74-121">Например, каналу розничной торговли требуется назначить сотрудников, кассы и клиентов.</span><span class="sxs-lookup"><span data-stu-id="97c74-121">For example, a retail channel needs assigned employees, registers, and customers.</span></span> <span data-ttu-id="97c74-122">После создания нового канала его необходимо назначить организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="97c74-122">Once a new channel is created, it needs to be assigned to an organization hierarchy.</span></span>

## <a name="channel-setup-prerequisites"></a><span data-ttu-id="97c74-123">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="97c74-123">Channel setup prerequisites</span></span>

<span data-ttu-id="97c74-124">Перед настройкой канала необходимо выполнить некоторые условия на основе типа канала.</span><span class="sxs-lookup"><span data-stu-id="97c74-124">Before you can set up a channel, you must complete some prerequisite tasks based on the channel type.</span></span> <span data-ttu-id="97c74-125">Дополнительные сведения см. в разделе [Необходимые условия для настройки каналов](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="97c74-125">For more information, see [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="set-up-a-channel"></a><span data-ttu-id="97c74-126">Настройка канала</span><span class="sxs-lookup"><span data-stu-id="97c74-126">Set up a channel</span></span>

<span data-ttu-id="97c74-127">После выполнения необходимых условий дальнейшие инструкции см. по следующим ссылкам.</span><span class="sxs-lookup"><span data-stu-id="97c74-127">After you complete the prerequisite tasks, for further setup instructions, use the following links.</span></span>

- [<span data-ttu-id="97c74-128">Настройка канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="97c74-128">Set up a retail channel</span></span>](channel-setup-retail.md)
- [<span data-ttu-id="97c74-129">Настройка канала центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="97c74-129">Set up a call center channel</span></span>](channel-setup-callcenter.md)
- [<span data-ttu-id="97c74-130">Настройка интернет-канала</span><span class="sxs-lookup"><span data-stu-id="97c74-130">Set up an online channel</span></span>](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a><span data-ttu-id="97c74-131">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="97c74-131">Additional resources</span></span>

[<span data-ttu-id="97c74-132">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="97c74-132">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="97c74-133">Настройка канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="97c74-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="97c74-134">Настройка интернет-канала</span><span class="sxs-lookup"><span data-stu-id="97c74-134">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="97c74-135">Настройка канала центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="97c74-135">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="97c74-136">Настройка организационных иерархий</span><span class="sxs-lookup"><span data-stu-id="97c74-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)
