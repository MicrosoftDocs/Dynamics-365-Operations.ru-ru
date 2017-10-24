---
title: "Продажа и возврат продуктов за пределами ассортимента"
description: "С 365 Dynamics for Retail можно продавать и возвращать продукты за пределами ассортиментов."
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: 
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7fa5b240bc9c9f96ae5483be316eff62df915570
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="sell-and-return-products-outside-of-an-assortment"></a><span data-ttu-id="27d76-103">Продажа и возврат продуктов за пределами ассортимента</span><span class="sxs-lookup"><span data-stu-id="27d76-103">Sell and return products outside of an assortment</span></span>
<span data-ttu-id="27d76-104">Для любого предприятия розничной торговли достаточно распространенным является сценарий с продажей продуктов и приемом возвратов продуктов, даже если эти продукты отсутствуют в магазине (иными словами, продуктов, не входящих в ассортимент магазина).</span><span class="sxs-lookup"><span data-stu-id="27d76-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don’t carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>
<span data-ttu-id="27d76-105">Вот некоторые типовые сценарии:</span><span class="sxs-lookup"><span data-stu-id="27d76-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="27d76-106">В конкретном магазине предприятия розничной торговли не выставлены все продукты, которыми торгует предприятие.</span><span class="sxs-lookup"><span data-stu-id="27d76-106">A retailer doesn’t carry all its products in a specific store.</span></span> <span data-ttu-id="27d76-107">Остальные продукты хранятся на складе.</span><span class="sxs-lookup"><span data-stu-id="27d76-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="27d76-108">Сотрудник магазина может помочь клиенту, найдя продукты на складе, добавив их в корзину и оформив заказ путем выбора метода доставки, — например, продукт может быть доставлен со склада по определенному адресу или клиент может забрать его из данного магазина или из другого магазина.</span><span class="sxs-lookup"><span data-stu-id="27d76-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="27d76-109">В магазине, которые посетил клиент, определенные продукты не выставлены или их нет в наличии, однако эти продукты имеются в других магазинах.</span><span class="sxs-lookup"><span data-stu-id="27d76-109">A retailer doesn’t carry specific products in the store or doesn’t have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="27d76-110">Сотрудник магазина помочь клиенту, найдя продукты в другом магазине, добавив их в корзину и оформив заказ путем выбора метода доставки.</span><span class="sxs-lookup"><span data-stu-id="27d76-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="27d76-111">У предприятия розничной торговли несколько магазинов в конкретном городе или районе, и предприятие не требует, чтобы клиенты возвращали купленные продукты именно в тот магазин, где они их приобрели.</span><span class="sxs-lookup"><span data-stu-id="27d76-111">A retailer has many stores in and around a specific city or zip code and doesn’t want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="27d76-112">Клиенты могут сделать возврат в любом удобном им магазине.</span><span class="sxs-lookup"><span data-stu-id="27d76-112">Instead, customers can return products to any store.</span></span>


<span data-ttu-id="27d76-113">С помощью Dynamics 365 for Retail предприятия розничной торговли могут реализовать эти типовые сценарии.</span><span class="sxs-lookup"><span data-stu-id="27d76-113">Those common scenarios are available for retailers using Dynamics 365 for Retail.</span></span> <span data-ttu-id="27d76-114">Система Retail позволяет:</span><span class="sxs-lookup"><span data-stu-id="27d76-114">With Retail, you can:</span></span>
+ <span data-ttu-id="27d76-115">Искать или просматривать продукты в других магазинах.</span><span class="sxs-lookup"><span data-stu-id="27d76-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="27d76-116">Искать или просматривать все выпущенные в продажу продукты.</span><span class="sxs-lookup"><span data-stu-id="27d76-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="27d76-117">Создавать проводки "заплатил и забрал" или заказы клиентов.</span><span class="sxs-lookup"><span data-stu-id="27d76-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="27d76-118">Выбирать варианты доставки для заказов клиентов.</span><span class="sxs-lookup"><span data-stu-id="27d76-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="27d76-119">Оформлять самовывоз продуктов клиентами из текущего магазина или из другого магазина.</span><span class="sxs-lookup"><span data-stu-id="27d76-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="27d76-120">Отменять заказы в текущем магазине или в другом магазине.</span><span class="sxs-lookup"><span data-stu-id="27d76-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="27d76-121">Оформлять возврат заказов с учетом или без учета прихода в текущем магазине или в другом магазине.</span><span class="sxs-lookup"><span data-stu-id="27d76-121">Return an order with or without the receipt at the current store or another store.</span></span>

