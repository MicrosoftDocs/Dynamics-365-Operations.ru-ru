---
title: "Функциональность центра обработки вызовов"
description: "Этот раздел содержит обзор возможностей продаж в центре обработки вызовов в Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: dd35e895cdfe402b9d22e710c7b0166eadf412ff
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---

# <a name="call-center-functionality"></a><span data-ttu-id="1ab76-103">Функциональность центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="1ab76-103">Call center functionality</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="1ab76-104">Эта статья содержит обзор возможностей продаж в центре обработки вызовов в Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="1ab76-104">This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="1ab76-105">Dynamics 365 for Retail поддерживает центры обработки вызовов как тип канала розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="1ab76-105">Dynamics 365 for Retail supports call centers as a type of retail channel.</span></span> <span data-ttu-id="1ab76-106">В центре обработки вызовов работники принимают заказы от клиентов по телефону и создают заказы на продажу.</span><span class="sxs-lookup"><span data-stu-id="1ab76-106">In a call center, workers take orders from customers over the phone and create sales orders.</span></span> <span data-ttu-id="1ab76-107">К функциям центра обработки вызовов относится возможность более быстро принимать заказы по телефону и обслуживать клиентов в рамках процесса выполнения заказа.</span><span class="sxs-lookup"><span data-stu-id="1ab76-107">Call center functionality includes features that are designed to make it easier to take phone orders and handle customer service throughout the order fulfillment process.</span></span> <span data-ttu-id="1ab76-108">Например, сотрудники центра обработки вызовов могут вводить сведения о платежах непосредственно в заказ на продажу и просматривать подробную сводку расходов и платежей перед отправкой заказа.</span><span class="sxs-lookup"><span data-stu-id="1ab76-108">For example, call center workers can enter payment information directly into the sales order, and can view a detailed summary of charges and payments before they submit the order.</span></span> <span data-ttu-id="1ab76-109">Работники также могут контролировать ценообразование и имеют доступ к различным данным о клиентах, продуктах и ценах на странице **заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="1ab76-109">Workers also have options for controlling pricing, and can access various data about customers, products, and prices from the **Sales order** page.</span></span> <span data-ttu-id="1ab76-110">Кроме того, В центрах обработки вызовов также доступна расширенная функциональность для отслеживания истории клиентов и статуса заказов.</span><span class="sxs-lookup"><span data-stu-id="1ab76-110">Additionally, call centers have enhanced functionality for tracking customer history and order status.</span></span> <span data-ttu-id="1ab76-111">Каждый центр обработки вызовов может иметь собственных пользователей, способы оплаты, ценовые группы, финансовые аналитики и режимы доставки.</span><span class="sxs-lookup"><span data-stu-id="1ab76-111">Each call center can have its own users, payment methods, price groups, financial dimensions, and modes of delivery.</span></span> <span data-ttu-id="1ab76-112">Эти параметры можно настроить при создании центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="1ab76-112">You can configure these options when you create the call center.</span></span> <span data-ttu-id="1ab76-113">Кроме того, Страница **Центр обработки вызовов** используется для включения или отключения следующих групп функций, свойственных центрам обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="1ab76-113">Additionally, you can use the **Call center** page to enable or disable the following groups of features that are unique to call centers:</span></span>

-   <span data-ttu-id="1ab76-114">**Завершение заказа** — эта группа содержит функции, связанные с платежами и завершением заказа в странице **заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="1ab76-114">**Order completion** – This group includes features that are related to payments and order completion on the **Sales order** page.</span></span>
-   <span data-ttu-id="1ab76-115">**Направленные продажи** — эта группа содержит функции, связанные с кодами источников, сценариями и запросами каталогов.</span><span class="sxs-lookup"><span data-stu-id="1ab76-115">**Directed selling** – This group includes features that are related to source codes, scripts, and catalog requests.</span></span>

<span data-ttu-id="1ab76-116">Если эти функции включить в настройках центра обработки вызовов, они становятся доступны на странице **Заказ на продажу** для пользователей, связанных с центром обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="1ab76-116">After you enable these features in the call center settings, they are available on the **Sales order** page to users who are associated with the call center.</span></span> <span data-ttu-id="1ab76-117">Для большинства этих функций требуется дополнительная настройка, прежде чем их можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="1ab76-117">Most of these features require additional setup before they can be used.</span></span> <span data-ttu-id="1ab76-118">Прежде чем пользователи могут создать заказы центра обработки вызовов, вы должны добавить тех пользователей к центру обработки вызовов как пользователей центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="1ab76-118">Before users can create call center orders, you must add those users to the call center as call center users.</span></span> <span data-ttu-id="1ab76-119">Этот шаг включает конфигурацию и функции для центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="1ab76-119">This step enables the call center channel-specific configuration and functionality.</span></span> <span data-ttu-id="1ab76-120">Здесь некоторые примеры функциональности, которая будет доступной:</span><span class="sxs-lookup"><span data-stu-id="1ab76-120">Here are some examples of the functionality that becomes available:</span></span>

-   <span data-ttu-id="1ab76-121">Направленные продажи обеспечивают опции конфигурации для сценариев телепродаж и изображения продукта, которые помогают и направляют сотрудников отдела продаж, пока они принимают заказы.</span><span class="sxs-lookup"><span data-stu-id="1ab76-121">Guided selling provides configuration options for tele-sales scripts and product images to help and guide sales clerks while they take orders.</span></span>
-   <span data-ttu-id="1ab76-122">Заказы нельзя завершить до тех пор пока сотрудник отдела продаж не запишет по крайней мере один метод оплаты.</span><span class="sxs-lookup"><span data-stu-id="1ab76-122">Orders can't be completed until sales clerks have captured at least one payment method.</span></span>
-   <span data-ttu-id="1ab76-123">Правила расширения продаж и перекрестной продажи можно установить для того, чтобы предложить сотрудникам отдела продаж продвинуть определенные продукты для клиента.</span><span class="sxs-lookup"><span data-stu-id="1ab76-123">Upsell and cross-sell rules can be configured to prompt sales clerks to promote specific products to the customer.</span></span>
-   <span data-ttu-id="1ab76-124">Сотрудники отдела продаж могут захватить исходный код для каталога, из которого клиент заказывает.</span><span class="sxs-lookup"><span data-stu-id="1ab76-124">Sales clerks can capture the source code for the catalog that a customer is ordering from.</span></span>
-   <span data-ttu-id="1ab76-125">Сотрудники отдела продаж могут добавить купоны розничного торговца к заказу.</span><span class="sxs-lookup"><span data-stu-id="1ab76-125">Sales clerks can add a retailer's coupons to the order.</span></span>
-   <span data-ttu-id="1ab76-126">Сотрудники отдела продаж могут продать программы непрерывности.</span><span class="sxs-lookup"><span data-stu-id="1ab76-126">Sales clerks can sell continuity programs.</span></span>
-   <span data-ttu-id="1ab76-127">Заказы можно заблокировать вручную или автоматически, для того, чтобы показать, что дополнительное расследование необходимо, прежде чем заказ можно обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="1ab76-127">Orders can be put on hold manually or automatically, to indicate that additional investigation is required before the order can be processed.</span></span>





