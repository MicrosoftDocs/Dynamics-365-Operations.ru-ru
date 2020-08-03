---
title: Доступность запасов в двойной записи
description: В этой теме приводятся сведения о порядке проверки доступности запасов в случае двойной записи.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
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
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 227a2062a7985a787f8278c196f7df2fb6f31691
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443880"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="413f8-103">Доступность запасов в двойной записи</span><span class="sxs-lookup"><span data-stu-id="413f8-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="413f8-104">Используя доступность запасов, можно проверять запасы перед добавлением продукта на страницу **Предложения**, **Заказы** или **Накладные** в Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="413f8-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="413f8-105">Например, вы проверяете запасы и определяете дату выполнения как одну из ключевых задач в процессе [продажи перспективному клиенту](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="413f8-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="413f8-106">Если запасов не хватает, можно оценить дату поставки на основе прогнозируемых приходов и расходов на складе.</span><span class="sxs-lookup"><span data-stu-id="413f8-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="413f8-107">Можно также проверить информацию о доступных для заказа продуктов (ATP), в которой можно найти количество ATP по заранее определенной временной границе.</span><span class="sxs-lookup"><span data-stu-id="413f8-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="413f8-108">Запасы в наличии</span><span class="sxs-lookup"><span data-stu-id="413f8-108">On-hand inventory</span></span>

<span data-ttu-id="413f8-109">В Dynamics 365 Sales добавлена новая кнопка **Запасы в наличии** в заголовке страниц **Предложения**, **Заказы** и **Накладные**.</span><span class="sxs-lookup"><span data-stu-id="413f8-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="413f8-110">При выборе этой кнопки появляется диалоговое окно, в котором можно указать компанию и продукт, для которого необходимо проверить запасы в наличии.</span><span class="sxs-lookup"><span data-stu-id="413f8-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="413f8-111">В этом диалоговом окне отображаются те же сведения, что и в [Запасы в наличии](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="413f8-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="413f8-112">В диалоговом окне возвращаются сведения о запасах из Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="413f8-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="413f8-113">Эта информация содержит следующие количества:</span><span class="sxs-lookup"><span data-stu-id="413f8-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="413f8-114">Количество в наличии</span><span class="sxs-lookup"><span data-stu-id="413f8-114">On-hand quantity</span></span>
- <span data-ttu-id="413f8-115">Зарезервированное количество в наличии</span><span class="sxs-lookup"><span data-stu-id="413f8-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="413f8-116">Доступное количество в наличии</span><span class="sxs-lookup"><span data-stu-id="413f8-116">Available on-hand quantity</span></span>
- <span data-ttu-id="413f8-117">Заказанное количество</span><span class="sxs-lookup"><span data-stu-id="413f8-117">Ordered quantity</span></span>
- <span data-ttu-id="413f8-118">Количество в заказе</span><span class="sxs-lookup"><span data-stu-id="413f8-118">On-order quantity</span></span>
- <span data-ttu-id="413f8-119">Зарезервированное заказанное количество</span><span class="sxs-lookup"><span data-stu-id="413f8-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="413f8-120">Общее доступное количество</span><span class="sxs-lookup"><span data-stu-id="413f8-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="413f8-121">Информация о "доступно для резервирования"</span><span class="sxs-lookup"><span data-stu-id="413f8-121">ATP information</span></span>

<span data-ttu-id="413f8-122">В Sales новая кнопка **Информация ATP** была добавлена в позиции строки на страницах **Предложения**, **Заказы** и **Накладные**.</span><span class="sxs-lookup"><span data-stu-id="413f8-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="413f8-123">При выборе этой кнопки появляется диалоговое окно, в котором можно указать компанию, продукт, сайт запасов, склад запасов и количество заказа.</span><span class="sxs-lookup"><span data-stu-id="413f8-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="413f8-124">В этом диалоговом окне используются те же настройки, что и описанные в разделе [Резервирование по заказам](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="413f8-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="413f8-125">Диалоговое окно возвращает сведения о доступности для резервирования из модуля Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="413f8-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="413f8-126">Эта информация содержит следующие количества:</span><span class="sxs-lookup"><span data-stu-id="413f8-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="413f8-127">Количество "доступно для резервирования"</span><span class="sxs-lookup"><span data-stu-id="413f8-127">ATP quantity</span></span>
- <span data-ttu-id="413f8-128">Количество прихода</span><span class="sxs-lookup"><span data-stu-id="413f8-128">Receipt quantity</span></span>
- <span data-ttu-id="413f8-129">Количество расходов</span><span class="sxs-lookup"><span data-stu-id="413f8-129">Issue quantity</span></span>
- <span data-ttu-id="413f8-130">Количество в наличии</span><span class="sxs-lookup"><span data-stu-id="413f8-130">On-hand quantity</span></span>