---
title: Возврат номенклатур по нескольким заказам и накладным клиента
description: В этом разделе описывается функциональность, обеспечивающая возвраты по нескольким заказам и накладным клиента в Dynamics 365 Retail.
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
ms.openlocfilehash: 25a1081e5f903076e23089c41dda7437f8a70124
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017997"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="33281-103">Возврат номенклатур по нескольким заказам и накладным клиента</span><span class="sxs-lookup"><span data-stu-id="33281-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="33281-104">Возврат может выполняться по нескольким заказам и накладным.</span><span class="sxs-lookup"><span data-stu-id="33281-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="33281-105">Настройка Retail для поддержки возвратов по нескольким заказам и накладным клиента</span><span class="sxs-lookup"><span data-stu-id="33281-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="33281-106">Выберите **Параметры розничной торговли \> Клиентские заказы**.</span><span class="sxs-lookup"><span data-stu-id="33281-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="33281-107">Включите параметр **Разрешить возврат по нескольким заказам**.</span><span class="sxs-lookup"><span data-stu-id="33281-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="33281-108">Обработка возвратов</span><span class="sxs-lookup"><span data-stu-id="33281-108">Process returns</span></span>

<span data-ttu-id="33281-109">После включения этого параметра и синхронизации изменений с магазинами кассир в магазине может выбрать для клиента несколько заказов на продажу, чтобы обработать возврат.</span><span class="sxs-lookup"><span data-stu-id="33281-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="33281-110">При выборе заказов отображается список всех доступных для возврата продуктов по всем накладным для этих заказов.</span><span class="sxs-lookup"><span data-stu-id="33281-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="33281-111">Кассир может затем выбрать возвращаемые продукты.</span><span class="sxs-lookup"><span data-stu-id="33281-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="33281-112">Создается один заказ на возврат для всех выбранных продуктов.</span><span class="sxs-lookup"><span data-stu-id="33281-112">A single return order will be created for all the selected products.</span></span>
