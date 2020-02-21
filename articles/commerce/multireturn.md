---
title: Возврат номенклатур по нескольким заказам и накладным клиента
description: В этом разделе описывается функциональность, обеспечивающая возвраты по нескольким заказам и накладным клиента в Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: c5f17424f0837344030f9ce2d2d037cde08c4e49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004466"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="d1a52-103">Возврат номенклатур по нескольким заказам и накладным клиента</span><span class="sxs-lookup"><span data-stu-id="d1a52-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="d1a52-104">Возврат может выполняться по нескольким заказам и накладным.</span><span class="sxs-lookup"><span data-stu-id="d1a52-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="d1a52-105">Настройка Commerce для поддержки возвратов по нескольким заказам и накладным клиента</span><span class="sxs-lookup"><span data-stu-id="d1a52-105">Configure Commerce to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="d1a52-106">Выберите **Параметры Commerce \> Клиентские заказы**.</span><span class="sxs-lookup"><span data-stu-id="d1a52-106">Go to **Commerce parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="d1a52-107">Включите параметр **Разрешить возврат по нескольким заказам**.</span><span class="sxs-lookup"><span data-stu-id="d1a52-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="d1a52-108">Обработка возвратов</span><span class="sxs-lookup"><span data-stu-id="d1a52-108">Process returns</span></span>

<span data-ttu-id="d1a52-109">После включения этого параметра и синхронизации изменений с магазинами кассир в магазине может выбрать для клиента несколько заказов на продажу, чтобы обработать возврат.</span><span class="sxs-lookup"><span data-stu-id="d1a52-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="d1a52-110">При выборе заказов отображается список всех доступных для возврата продуктов по всем накладным для этих заказов.</span><span class="sxs-lookup"><span data-stu-id="d1a52-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="d1a52-111">Кассир может затем выбрать возвращаемые продукты.</span><span class="sxs-lookup"><span data-stu-id="d1a52-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="d1a52-112">Создается один заказ на возврат для всех выбранных продуктов.</span><span class="sxs-lookup"><span data-stu-id="d1a52-112">A single return order will be created for all the selected products.</span></span>
