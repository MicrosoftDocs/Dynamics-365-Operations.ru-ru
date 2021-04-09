---
title: Возврат номенклатур по нескольким заказам и накладным клиента
description: В этом разделе описывается функциональность, обеспечивающая возвраты по нескольким заказам и накладным клиента в Dynamics 365 Commerce.
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4a64794a0e04516441fab628d441640e4d154b8d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796905"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="609db-103">Возврат номенклатур по нескольким заказам и накладным клиента</span><span class="sxs-lookup"><span data-stu-id="609db-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="609db-104">В этой статье описываются две функции, которые оптимизируют возвраты по заказам клиентов по нескольким накладным.</span><span class="sxs-lookup"><span data-stu-id="609db-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="609db-105">Включить возвраты денежных средств по нескольким фиксациям</span><span class="sxs-lookup"><span data-stu-id="609db-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="609db-106">Эта функция активирует несколько связанных возвратов денежных средств для одного и того же заказа клиента.</span><span class="sxs-lookup"><span data-stu-id="609db-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="609db-107">Перейдите в рабочую область **Управление функциями** и найдите функцию **Включить возвраты денежных средств по нескольким фиксациям**.</span><span class="sxs-lookup"><span data-stu-id="609db-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="609db-108">Выберите **Включить возвраты денежных средств по нескольким заказам**, затем нажмите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="609db-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="609db-109">Включить надлежащий расчет налога для возвратов с частичным количеством</span><span class="sxs-lookup"><span data-stu-id="609db-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="609db-110">Эта функция гарантирует, что при возврате заказа с использованием нескольких накладных налоги в конечном итоге будут равняться первоначальной начисленной сумме налога.</span><span class="sxs-lookup"><span data-stu-id="609db-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="609db-111">Перейдите к рабочей области **Управление функциями** и найдите функцию **Включить надлежащий расчет налога для возвратов с частичным количеством**.</span><span class="sxs-lookup"><span data-stu-id="609db-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="609db-112">Выберите **Включить надлежащий расчет налога для возвратов с частичным количеством**, затем нажмите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="609db-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="609db-113">Обработка возвратов</span><span class="sxs-lookup"><span data-stu-id="609db-113">Process returns</span></span>

<span data-ttu-id="609db-114">После включения этих функций и синхронизации изменений с магазинами кассир в магазине может выбрать для клиента несколько заказов на продажу, чтобы обработать возврат.</span><span class="sxs-lookup"><span data-stu-id="609db-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="609db-115">При выборе заказов отображается список всех доступных для возврата продуктов по всем накладным для этих заказов.</span><span class="sxs-lookup"><span data-stu-id="609db-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="609db-116">Кассир может затем выбрать возвращаемые продукты.</span><span class="sxs-lookup"><span data-stu-id="609db-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="609db-117">Создается один заказ на возврат для всех выбранных продуктов.</span><span class="sxs-lookup"><span data-stu-id="609db-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="609db-118">Если заказ полностью возвращен, сумма налогов, возвращенная клиенту, будет равна исходной сумме начисленного налога.</span><span class="sxs-lookup"><span data-stu-id="609db-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]