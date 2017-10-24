---
title: "Упаковочные материалы и сборы"
description: "Сборы за упаковочные материалы выплачиваются компании утилизации с определенными интервалами. Для каждого материала, из которого состоит единица упаковки, должна выплачиваться сумма за единицу веса. Сборы за упаковочные материалы рассчитываются и учитываются в отчетах, но никакие проводки ГК не разносятся, так как сборы не рассматриваются в качестве налогов, которые необходимо платить налоговому органу."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5d7cd7b3d60e9c265a766695b53d8d27ee2a8d0a
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="packing-materials-and-fees"></a><span data-ttu-id="8a943-105">Упаковочные материалы и сборы</span><span class="sxs-lookup"><span data-stu-id="8a943-105">Packing materials and fees</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8a943-106">Сборы за упаковочные материалы выплачиваются компании утилизации с определенными интервалами.</span><span class="sxs-lookup"><span data-stu-id="8a943-106">Packing material fees are paid to a recycling company at certain intervals.</span></span> <span data-ttu-id="8a943-107">Для каждого материала, из которого состоит единица упаковки, должна выплачиваться сумма за единицу веса.</span><span class="sxs-lookup"><span data-stu-id="8a943-107">An amount is paid, per unit of weight, for each material that a packing unit consists of.</span></span> <span data-ttu-id="8a943-108">Сборы за упаковочные материалы рассчитываются и учитываются в отчетах, но никакие проводки ГК не разносятся, так как сборы не рассматриваются в качестве налогов, которые необходимо платить налоговому органу.</span><span class="sxs-lookup"><span data-stu-id="8a943-108">Packing material fees are calculated and reported, but no ledger transactions are posted because the fees are not regarded as taxes to be paid to an authority.</span></span>

<span data-ttu-id="8a943-109">Вес и сборы для упаковочных материалов рассчитываются как для строк заказов на продажу, так и для строк заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="8a943-109">Packing material weights and fees are calculated for sales order lines and for purchase order lines.</span></span>

<span data-ttu-id="8a943-110">Можно определить одну или несколько единиц упаковки для номенклатуры, для группы упаковки номенклатур или для всех номенклатур.</span><span class="sxs-lookup"><span data-stu-id="8a943-110">You can define one or more packing units for an item, for a packing group of items, or for all items.</span></span> <span data-ttu-id="8a943-111">Единица упаковки состоит из различных упаковочных материалов и их веса, а также количества номенклатур, входящих в единицу упаковки.</span><span class="sxs-lookup"><span data-stu-id="8a943-111">A packing unit consists of the packing materials, their weights, and the number of items that are included in the packing unit.</span></span> <span data-ttu-id="8a943-112">Каждому определенному типу упаковочных материалов назначается код упаковочных материалов.</span><span class="sxs-lookup"><span data-stu-id="8a943-112">A packing material code is assigned to each type of packing material that is defined.</span></span> <span data-ttu-id="8a943-113">На основе кода упаковочных материалов можно указать цену за заданный период.</span><span class="sxs-lookup"><span data-stu-id="8a943-113">Based on the packing material code, you can specify a price for a specified period.</span></span> <span data-ttu-id="8a943-114">Сборы за упаковочные материалы рассчитываются на основе этих сведений.</span><span class="sxs-lookup"><span data-stu-id="8a943-114">The packing material fee is calculated based on this information.</span></span>

| <span data-ttu-id="8a943-115">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="8a943-115">**Note**</span></span>                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a943-116">Даже если компания не оплачивает сборы за упаковочный материал, эту функцию можно использовать, чтобы рассчитать статистику для веса упаковочных материалов.</span><span class="sxs-lookup"><span data-stu-id="8a943-116">Even if your company does not pay packing material fees, you can use the functionality to calculate statistics for the weights of packing materials.</span></span> |

## <a name="setup-requirements-for-packing-material-fees"></a><span data-ttu-id="8a943-117">Настройка требований к сборам за упаковочные материалы</span><span class="sxs-lookup"><span data-stu-id="8a943-117">Setup requirements for packing material fees</span></span>
<span data-ttu-id="8a943-118">Перед расчетом веса или сборов для упаковочных материалов или обоих значений, необходимо создать следующие базовые данные.</span><span class="sxs-lookup"><span data-stu-id="8a943-118">Before you calculate packing material weights or packing material fees, or both, you must create the following base data:</span></span>

-   <span data-ttu-id="8a943-119">Группы упаковки. Создайте группы упаковки для назначения номенклатурам.</span><span class="sxs-lookup"><span data-stu-id="8a943-119">Packing groups – Create packing groups to assign to items.</span></span>
-   <span data-ttu-id="8a943-120">Коды упаковочных материалов. Создайте коды упаковочных материалов для каждого определенного типа упаковочных материалов.</span><span class="sxs-lookup"><span data-stu-id="8a943-120">Packing material codes – Create packing material codes for each type of packing material that is defined.</span></span>
-   <span data-ttu-id="8a943-121">Единицы упаковки. Определите единицу упаковки для номенклатуры, группы упаковки или для всех номенклатур.</span><span class="sxs-lookup"><span data-stu-id="8a943-121">Packing units – Specify a packing unit for an item, for a packing group, or for all items.</span></span> <span data-ttu-id="8a943-122">Для каждой единицы упаковки определите включаемые упаковочные материалы, назначьте вес и в поле "Коэффициент единицы упаковки" введите коэффициент преобразования из единиц складского учета.</span><span class="sxs-lookup"><span data-stu-id="8a943-122">For each packing unit, define which packing materials to include, assign weights, and, in the Packing unit factor field, enter the conversion factor from the inventory unit.</span></span>
-   <span data-ttu-id="8a943-123">Сборы за упаковочные материалы. Определите сборы за упаковочный материал для кода упаковочного материала.</span><span class="sxs-lookup"><span data-stu-id="8a943-123">Packing material fees – Specify packing material fees per packing material code.</span></span> <span data-ttu-id="8a943-124">Для каждого типа материала определите период действия, цену за материал, валюту и единицу.</span><span class="sxs-lookup"><span data-stu-id="8a943-124">For each type of material, define the period of validity, the price per material, the currency, and the unit.</span></span>

## <a name="packing-units-on-sales-order-lines"></a><span data-ttu-id="8a943-125">Единицы упаковки в строках заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="8a943-125">Packing units on sales order lines</span></span>
<span data-ttu-id="8a943-126">При создании строки заказа на продажу система проверяет, были ли определены единицы упаковки для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="8a943-126">When you create a sales order line, the system checks to see whether packing units are specified for the item.</span></span> <span data-ttu-id="8a943-127">Если единицы упаковки были указаны, в строке заказа на продажу обновляются указанная единица упаковки и количество единиц упаковки.</span><span class="sxs-lookup"><span data-stu-id="8a943-127">If packing units are specified, the system updates the sales order line with the specified packing unit and the packing unit quantity.</span></span> <span data-ttu-id="8a943-128">Количество единиц упаковки рассчитывается путем деления заказанного количества на число номенклатур в выбранной единице упаковки.</span><span class="sxs-lookup"><span data-stu-id="8a943-128">The packing unit quantity is based on the ordered quantity divided by the number of items in the selected packing unit.</span></span> <span data-ttu-id="8a943-129">Если единица упаковки не была определена, можно вручную ввести единицу упаковки и количество единиц упаковки в строке заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="8a943-129">If a packing unit has not been specified, you can manually enter a packing unit and a packing unit quantity on the sales order line.</span></span> <span data-ttu-id="8a943-130">Единицу упаковки и количество единиц упаковки также можно изменить при разноске строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="8a943-130">You can also change the packing unit and the packing unit quantity when you post the sales order line.</span></span> <span data-ttu-id="8a943-131">Это имеет значение, если доставка или выписывание накладной для строки заказа на продажу выполнены только частично.</span><span class="sxs-lookup"><span data-stu-id="8a943-131">This is relevant if the sales order line is only partly delivered or partly invoiced.</span></span> <span data-ttu-id="8a943-132">Проводки по упаковочному материалу создаются при выставлении накладной по строке заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="8a943-132">When you invoice the sales order, packing material transactions are created.</span></span> <span data-ttu-id="8a943-133">Проводки по упаковочным материалам содержат вес упаковочных материалов для строки продажи.</span><span class="sxs-lookup"><span data-stu-id="8a943-133">Packing material transactions contain the weights of the packing materials for the sales line.</span></span> <span data-ttu-id="8a943-134">После выставления накладных проводки можно отредактировать, а затем создать новые.</span><span class="sxs-lookup"><span data-stu-id="8a943-134">You can also modify the transactions after you invoice them, and then create new transactions.</span></span>

## <a name="packing-units-on-purchase-order-lines"></a><span data-ttu-id="8a943-135">Единицы упаковки в строках заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="8a943-135">Packing units on purchase order lines</span></span>
<span data-ttu-id="8a943-136">Система не создает проводки по упаковочному материалу для строк заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="8a943-136">Packing material transactions for a purchase order line are not created by the system.</span></span> <span data-ttu-id="8a943-137">Проводки для строк заказа на покупку, но которым выставлена накладная, создаются вручную на странице **Проводки по упаковочному материалу**.</span><span class="sxs-lookup"><span data-stu-id="8a943-137">You create transactions for invoiced purchase order lines manually in the **Packing material transactions** page.</span></span>

## <a name="set-up-customer-packagingmaterialfee-license-numbers"></a><span data-ttu-id="8a943-138">Настройка номера лицензий сборов за упаковочный материал клиента</span><span class="sxs-lookup"><span data-stu-id="8a943-138">Set up customer packagingmaterialfee license numbers</span></span>
<span data-ttu-id="8a943-139">Если клиенты уплачивают сбор за упаковочные материалы, укажите номера лицензий сборов за упаковочный материал для таких клиентов на странице **Клиенты**.</span><span class="sxs-lookup"><span data-stu-id="8a943-139">If the customers pay the packaging material fees, specify the customers' packaging-material-fee license numbers in the **Customers** page.</span></span> <span data-ttu-id="8a943-140">После назначения клиенту номера лицензии сборы за упаковочный материал рассчитываются автоматически при выставлении счета к заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="8a943-140">When a license number has been assigned to a customer, the packaging material fees are calculated automatically when sales orders are invoiced.</span></span> <span data-ttu-id="8a943-141">После выставления накладной флажок **Рассчитать сбор** на странице **Проводки по упаковочному материалу** сбрасывается, поскольку нет необходимости готовить и распечатывать отчет.</span><span class="sxs-lookup"><span data-stu-id="8a943-141">After invoicing, the **Calculate fee** check box is cleared in the **Packing material transactions** page, because you do not have to calculate and print a report.</span></span> <span data-ttu-id="8a943-142">Предусмотрена возможность печати веса упаковочных материалов в накладной и уведомления клиента о необходимости уплаты сборов.</span><span class="sxs-lookup"><span data-stu-id="8a943-142">You can print the packaging material weights on the invoice, and inform the customers that they pay the fees.</span></span> 

<span data-ttu-id="8a943-143">Если сбор за упаковочный материал уплачивает ваша компания, не вводите номера лицензий клиентов.</span><span class="sxs-lookup"><span data-stu-id="8a943-143">If your company pays the packaging material fees, do not specify the customer license numbers.</span></span> <span data-ttu-id="8a943-144">После выставления накладной флажок **Рассчитать сбор** устанавливается на странице **Проводки по упаковочному материалу**.</span><span class="sxs-lookup"><span data-stu-id="8a943-144">After invoicing, the **Calculate fee** check box is selected in the **Packing material transactions** page.</span></span> <span data-ttu-id="8a943-145">Это означает, что расчет сборов производится при создании отчета.</span><span class="sxs-lookup"><span data-stu-id="8a943-145">This indicates that the fees are calculated when a report is created.</span></span> <span data-ttu-id="8a943-146">Можно распечатать вес на накладной и указать, что ваша компания уплачивает сборы.</span><span class="sxs-lookup"><span data-stu-id="8a943-146">You can print the weights on the invoice, and indicate that your company pays the fees.</span></span>

## <a name="print-packaging-material-weights-on-invoices"></a><span data-ttu-id="8a943-147">Распечатывание веса упаковочных материалов на накладных</span><span class="sxs-lookup"><span data-stu-id="8a943-147">Print packaging material weights on invoices</span></span>
<span data-ttu-id="8a943-148">Можно распечатать вес упаковочных материалов в накладной и указать, кто уплачивает сборы за упаковочные материалы.</span><span class="sxs-lookup"><span data-stu-id="8a943-148">You can print the packaging material weights on the invoice, and indicate who pays the packaging material fees.</span></span> <span data-ttu-id="8a943-149">Вес суммируется по упаковочному коду.</span><span class="sxs-lookup"><span data-stu-id="8a943-149">The weights are summarized by packaging code.</span></span>
 




