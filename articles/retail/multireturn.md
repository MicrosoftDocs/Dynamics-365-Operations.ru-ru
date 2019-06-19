---
title: Возврат номенклатур по нескольким заказам и накладным клиента
description: В этой теме рассматривается функциональность, обеспечивающая возврат по нескольким заказам и накладным клиента в Microsoft Dynamics 365 for Retail.
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
ms.openlocfilehash: c201311028b11121d626e93859a2b98497c047d1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565308"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="8d2ef-103">Возврат номенклатур по нескольким заказам и накладным клиента</span><span class="sxs-lookup"><span data-stu-id="8d2ef-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="8d2ef-104">В Dynamics 365 for Finance and Operations версии 10.0 возвраты могут выполняться по нескольким заказам и накладным, тогда как в выпусках до 10.0 одновременная обработка была возможна только по одной накладной.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-104">In Dynamics 365 for Finance and Operations version 10.0, returns can be made across multiple orders and invoices, whereas in releases prior to 10.0, returns could only be processed by a single invoice at a time.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="8d2ef-105">Настройка Retail для поддержки возвратов по нескольким заказам и накладным клиента</span><span class="sxs-lookup"><span data-stu-id="8d2ef-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="8d2ef-106">Выберите **Параметры розничной торговли \> Клиентские заказы**.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="8d2ef-107">Включите параметр **Разрешить возврат по нескольким заказам**.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="8d2ef-108">Обработка возвратов</span><span class="sxs-lookup"><span data-stu-id="8d2ef-108">Process returns</span></span>

<span data-ttu-id="8d2ef-109">После включения этого параметра и синхронизации изменений с магазинами кассир в магазине может выбрать для клиента несколько заказов на продажу, чтобы обработать возврат.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="8d2ef-110">При выборе заказов отображается список всех доступных для возврата продуктов по всем накладным для этих заказов.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="8d2ef-111">Кассир может затем выбрать возвращаемые продукты.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="8d2ef-112">Создается один заказ на возврат для всех выбранных продуктов.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-112">A single return order will be created for all the selected products.</span></span>
