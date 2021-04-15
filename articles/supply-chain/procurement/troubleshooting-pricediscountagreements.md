---
title: Устранение неполадок по ценам, скидкам, соглашениям и бонусам
description: В этой теме описывается, как устранять проблемы, которые могут встретиться при работе с ценами, скидками, соглашениями и бонусами.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 12bc3cbccb1577c278489f640299510b3ced17e7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811094"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a><span data-ttu-id="9640f-103">Устранение неполадок по ценам, скидкам, соглашениям и бонусам</span><span class="sxs-lookup"><span data-stu-id="9640f-103">Troubleshoot prices, discounts, agreements, and rebates</span></span>

<span data-ttu-id="9640f-104">В этой теме описывается, как устранять проблемы, которые могут встретиться при работе с ценами, скидками, соглашениями и бонусами.</span><span class="sxs-lookup"><span data-stu-id="9640f-104">This topic describes how to fix issues that you might encounter while you work with prices, discounts, agreements, and rebates.</span></span>

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a><span data-ttu-id="9640f-105">После создания заказа на покупку невозможно связать договор покупки со строкой заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="9640f-105">I can't link a purchase agreement to a purchase order line after the purchase order is created.</span></span>

<span data-ttu-id="9640f-106">Договор покупки необходимо связать с заказом на покупку при создании заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="9640f-106">A purchase agreement must be associated with a purchase order when the purchase order is created.</span></span> <span data-ttu-id="9640f-107">В противном случае строки заказа на покупку не могут быть связаны со строками договора покупки.</span><span class="sxs-lookup"><span data-stu-id="9640f-107">Otherwise, purchase order lines can't be associated with purchase agreement lines.</span></span>

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a><span data-ttu-id="9640f-108">Какая проверка запускает сообщение "Обновите цены и скидки, введенные вручную, или внешний документ"?</span><span class="sxs-lookup"><span data-stu-id="9640f-108">What check triggers the "Update prices and discounts entered manually or external document" message?</span></span>

<span data-ttu-id="9640f-109">При изменении даты отгрузки может быть получено сообщение, в котором говорится "Обновите цены и скидки, введенные вручную, или внешний документ".</span><span class="sxs-lookup"><span data-stu-id="9640f-109">When you change the shipping date, you might receive a message that states, "Update prices and discounts entered manually or external document."</span></span> <span data-ttu-id="9640f-110">Это сообщение выводится из-за того, что при изменении даты отгрузки может быть запущено другое торговое соглашение или договор продажи, и это приводит к изменению цены.</span><span class="sxs-lookup"><span data-stu-id="9640f-110">You receive this message because, if the shipping date is changed, a different trade or sales agreement might be triggered and cause a price change.</span></span> <span data-ttu-id="9640f-111">Изменение даты отгрузки также может повлиять на складские графики и другие связанные данные.</span><span class="sxs-lookup"><span data-stu-id="9640f-111">A change to the shipping date can also affect warehouse schedules and other related information.</span></span>

<span data-ttu-id="9640f-112">Сообщение запускается каждый раз, когда изменяются любые даты или другие параметры.</span><span class="sxs-lookup"><span data-stu-id="9640f-112">The message is triggered whenever any of the dates or some other parameters are changed.</span></span> <span data-ttu-id="9640f-113">Целью сообщения является обеспечение осведомленности об изменениях цены, которые могут возникнуть вследствие этих изменений.</span><span class="sxs-lookup"><span data-stu-id="9640f-113">The purpose of the message is to make sure that you're aware of price changes that can occur because of those changes.</span></span>

<span data-ttu-id="9640f-114">Сообщение является запросом оценки коммерческого соглашения (TAE).</span><span class="sxs-lookup"><span data-stu-id="9640f-114">The message is the trade agreement evaluation (TAE) prompt.</span></span> <span data-ttu-id="9640f-115">Полное описание см. в разделе [Политики оценки коммерческих соглашений](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span><span class="sxs-lookup"><span data-stu-id="9640f-115">For a full description, see [Trade agreement evaluation policies](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span></span>

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a><span data-ttu-id="9640f-116">В приходе по заказу на покупку не включаются все расходы.</span><span class="sxs-lookup"><span data-stu-id="9640f-116">A purchase order receipt doesn't include all charges.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="9640f-117">Воспроизведение проблемы</span><span class="sxs-lookup"><span data-stu-id="9640f-117">Reproduce the issue</span></span>

<span data-ttu-id="9640f-118">Следующая процедура показывает один из способов воспроизведения проблемы.</span><span class="sxs-lookup"><span data-stu-id="9640f-118">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="9640f-119">На странице **Параметры модуля "Закупки и источники"** на вкладке **Доставка** убедитесь, что для параметра **Формировать накладные расходы при приходе продукта** установлено значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="9640f-119">On the **Procurement and sourcing parameters** page, on the **Delivery** tab, make sure that the **Generate charges on product receipt** option is set to *Yes*.</span></span>
1. <span data-ttu-id="9640f-120">Создайте заказ на покупку, включающий накладные расходы.</span><span class="sxs-lookup"><span data-stu-id="9640f-120">Create a purchase order that includes charges.</span></span>
1. <span data-ttu-id="9640f-121">Подтвердите заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="9640f-121">Confirm the purchase order.</span></span>
1. <span data-ttu-id="9640f-122">Получите заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="9640f-122">Receive the purchase order.</span></span>
1. <span data-ttu-id="9640f-123">Просмотрите итоговую сумму прихода и сравните ее с ожидаемым итогом.</span><span class="sxs-lookup"><span data-stu-id="9640f-123">Look at the receipt total, and compare it to the expected total.</span></span>
1. <span data-ttu-id="9640f-124">Обратите внимание, что не все накладные расходы включены в приход заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="9640f-124">Notice that not all the charges are included on the purchase order receipt.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9640f-125">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="9640f-125">Issue resolution</span></span>

<span data-ttu-id="9640f-126">Разрешение зависит от способа настройки накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="9640f-126">The resolution depends on the way that the miscellaneous charges have been set up.</span></span> <span data-ttu-id="9640f-127">Сведения о порядке настройки накладных расходов, чтобы они удовлетворяли вашим требованиям, см. в следующей записи блога: [Разноска накладных расходов в момент поступления продуктов](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="9640f-127">For information about how to set up miscellaneous charges to meet your requirements, see the following blog post: [Post misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a><span data-ttu-id="9640f-128">Цены и скидки коммерческого соглашения не применяются к строкам заказа на продажу или покупку, которые импортированы с применением управления данными.</span><span class="sxs-lookup"><span data-stu-id="9640f-128">Trade agreement prices and discounts aren't applied on sales or purchase order lines that are imported through data management.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9640f-129">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="9640f-129">Issue description</span></span>

<span data-ttu-id="9640f-130">Коммерческие соглашения, которые применимы к строкам заказа на продажу или покупку, не применяются в строках, которые импортированы с применением управления данными.</span><span class="sxs-lookup"><span data-stu-id="9640f-130">Trade agreements that are applicable to sales or purchase order lines aren't applied on lines that are imported through data management.</span></span> <span data-ttu-id="9640f-131">Однако те же коммерческие соглашения применяются к строкам заказа на продажу или покупку, созданным вручную.</span><span class="sxs-lookup"><span data-stu-id="9640f-131">However, the same trade agreements are applied on sales or purchase order lines that are manually created.</span></span>

### <a name="reason-for-the-issue"></a><span data-ttu-id="9640f-132">Причина проблемы</span><span class="sxs-lookup"><span data-stu-id="9640f-132">Reason for the issue</span></span>

<span data-ttu-id="9640f-133">Если строки заказа на покупку, импортируемые через управление данными, уже содержат информацию о цене, коммерческое соглашение не будет заново оцениваться для этих строк.</span><span class="sxs-lookup"><span data-stu-id="9640f-133">If purchase order lines that are imported via data management already include price information, the trade agreement won't be reevaluated for those lines.</span></span> <span data-ttu-id="9640f-134">Например, если в строке указан **процент скидки по строке** или какое-либо значение цены и скидки, коммерческие соглашения не будут проверяться для этой строки.</span><span class="sxs-lookup"><span data-stu-id="9640f-134">For example, if **Line discount percentage** or any of the price and discount values is set for a line, then trade agreements will not be looked up for that line.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="9640f-135">Временное решение проблемы</span><span class="sxs-lookup"><span data-stu-id="9640f-135">Issue workaround</span></span>

<span data-ttu-id="9640f-136">Такое поведение является ожидаемым и аналогично для заказов на продажу и заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="9640f-136">This behavior is expected, and is similar for both sales orders and purchase orders.</span></span>

<span data-ttu-id="9640f-137">В качестве временного решения импортируйте строки заказа на покупку, не задавая никакой информации о цене.</span><span class="sxs-lookup"><span data-stu-id="9640f-137">As a workaround, import the purchase order lines without setting any price information.</span></span> <span data-ttu-id="9640f-138">Затем будут применяться коммерческие соглашения, и строки заказа на покупку будут обновлены на основе определенных коммерческих соглашений.</span><span class="sxs-lookup"><span data-stu-id="9640f-138">The trade agreements will then be applied, and the purchase order lines will be updated based on the defined trade agreements.</span></span>

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a><span data-ttu-id="9640f-139">Бонус поставщика не накапливается на основе накладных.</span><span class="sxs-lookup"><span data-stu-id="9640f-139">A vendor rebate isn't cumulated based on invoices.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9640f-140">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="9640f-140">Issue description</span></span>

<span data-ttu-id="9640f-141">Если накладные, которые разносятся, имеют разные сроки исполнения, эти накладные не отражаются в бонусах поставщика, которые создаются из них.</span><span class="sxs-lookup"><span data-stu-id="9640f-141">If invoices that are posted have different due dates, those invoices aren't reflected in vendor rebates that are generated from them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9640f-142">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="9640f-142">Issue resolution</span></span>

<span data-ttu-id="9640f-143">По дизайну срок выполнения не учитывается при расчете бонуса поставщика.</span><span class="sxs-lookup"><span data-stu-id="9640f-143">By design, the due date isn't considered when the vendor rebate is calculated.</span></span> <span data-ttu-id="9640f-144">Рассмотрите возможность настройки системы таким образом, чтобы дата исполнения и связь с накладной были более очевидны по отношению к фактической бонусу поставщика.</span><span class="sxs-lookup"><span data-stu-id="9640f-144">Consider customizing the system so that the due date and the relation to the invoice are more apparent with respect to the actual vendor rebate.</span></span>

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a><span data-ttu-id="9640f-145">Цены за единицу в заказах на покупку не рассчитываются на основе преобразования единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="9640f-145">Unit prices on purchase orders aren't calculated based on the unit conversion.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9640f-146">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="9640f-146">Issue description</span></span>

<span data-ttu-id="9640f-147">При изменении единицы в заказе на покупку цены коммерческих соглашений не пересчитываются в соответствии с определениями пересчета единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="9640f-147">When a unit is changed on a purchase order, trade agreement prices aren't recalculated according to unit conversion definitions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9640f-148">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="9640f-148">Issue resolution</span></span>

<span data-ttu-id="9640f-149">Цены всегда извлекаются из коммерческих соглашениях (или других настроек цен в системе, таких как соглашения о продаже или цены номенклатур), и они настраиваются для единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="9640f-149">Prices are always obtained from trade agreements (or other price settings in the system, such as sales agreements or item prices), and they are set for a unit.</span></span>

<span data-ttu-id="9640f-150">Если единица измерения изменяется в строке заказа, система выполняет поиск цены для новой единицы измерения и применяет эту цену.</span><span class="sxs-lookup"><span data-stu-id="9640f-150">If the unit is changed on an order line, the system looks for a price for the new unit and applies that price.</span></span> <span data-ttu-id="9640f-151">Если для единицы измерения цена не найдена, система не применяет цену.</span><span class="sxs-lookup"><span data-stu-id="9640f-151">If no price is found for the unit, the system doesn't apply a price.</span></span> <span data-ttu-id="9640f-152">Пересчет единиц измерения не может использоваться для пересчета цены в другую единицу измерения.</span><span class="sxs-lookup"><span data-stu-id="9640f-152">The unit conversion can't be used to recalculate the price into another unit.</span></span> <span data-ttu-id="9640f-153">Теоретически цена за один ящик с десятком может не быть равна десяти ценам одного ящика.</span><span class="sxs-lookup"><span data-stu-id="9640f-153">Theoretically, the price for one box of ten might not equal ten times the price of one box.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="9640f-154">Временное решение проблемы</span><span class="sxs-lookup"><span data-stu-id="9640f-154">Issue workaround</span></span>

<span data-ttu-id="9640f-155">Одним из способов обхода этой проблемы является обеспечение наличия коммерческих соглашений для единиц измерения, которые, как вы ожидаете, будут использоваться в строках заказа для данной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="9640f-155">One way to work around this issue is to make sure that there are trade agreements for the units that you expect will be used on order lines for the item.</span></span>

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a><span data-ttu-id="9640f-156">В коммерческих соглашениях возникают проблемы при конвертации валют.</span><span class="sxs-lookup"><span data-stu-id="9640f-156">Currency conversion issues occur with trade agreements.</span></span>

<span data-ttu-id="9640f-157">Цены коммерческого соглашения не пересчитываются в соответствии с валютой, когда валюта отличается в заказе на покупку.</span><span class="sxs-lookup"><span data-stu-id="9640f-157">Trade agreement prices aren't recalculated according to the currency when the currency differs on a purchase order.</span></span>

<span data-ttu-id="9640f-158">Функция *Универсальная валюта* позволяет определять цены и скидки только в одной валюте.</span><span class="sxs-lookup"><span data-stu-id="9640f-158">The *Generic currency* feature lets you define prices and discounts in only one currency.</span></span> <span data-ttu-id="9640f-159">Затем можно выполнить преобразование в другие валюты по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="9640f-159">You can then convert to other currencies as you require.</span></span> <span data-ttu-id="9640f-160">Более того, после выполнения преобразования функция может автоматически применять психологическое округление.</span><span class="sxs-lookup"><span data-stu-id="9640f-160">Furthermore, after the conversion is done, the feature can automatically apply smart rounding.</span></span>

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a><span data-ttu-id="9640f-161">При открытии страницы договора покупки в режиме строкового вида невозможно настроить страницу, добавив поле "Единица измерения цены" в обзоре строки.</span><span class="sxs-lookup"><span data-stu-id="9640f-161">When I open the Purchase agreement page in a line view mode, I can't personalize the page by adding the Price unit field in the overview of the line.</span></span>

<span data-ttu-id="9640f-162">Некоторые общие поля в структуре соглашений не могут включаться в персонализации.</span><span class="sxs-lookup"><span data-stu-id="9640f-162">Some shared fields in the agreement framework can't be included in personalizations.</span></span> <span data-ttu-id="9640f-163">Это ограничение происходит из-за реализованной модели данных.</span><span class="sxs-lookup"><span data-stu-id="9640f-163">This limitation occurs because of the data model that is implemented.</span></span> <span data-ttu-id="9640f-164">Таким образом, нельзя персонализировать поле **Единица измерения цены**.</span><span class="sxs-lookup"><span data-stu-id="9640f-164">Therefore, you can't personalize the **Price unit** field.</span></span>

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a><span data-ttu-id="9640f-165">Максимальное ограничение по договору покупки не эффективно для заявки на закупку.</span><span class="sxs-lookup"><span data-stu-id="9640f-165">The maximum limit from a purchase agreement isn't effective on a purchase requisition.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9640f-166">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="9640f-166">Issue description</span></span>

<span data-ttu-id="9640f-167">Когда заявка на закупку связана с договором покупки, максимальная граница из договора покупки не действует в отношении данной заявки на закупку.</span><span class="sxs-lookup"><span data-stu-id="9640f-167">When a purchase requisition is linked to a purchase agreement, the maximum limit from the purchase agreement isn't effective on the purchase requisition.</span></span> <span data-ttu-id="9640f-168">Сведения о цене по умолчанию введены правильно, но в заявке на закупку может быть заказано больше максимально допустимого лимита из договора покупки.</span><span class="sxs-lookup"><span data-stu-id="9640f-168">The default price information is correctly entered, but more than the maximum limit from the purchase agreement can be ordered in the purchase requisition.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9640f-169">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="9640f-169">Issue resolution</span></span>

<span data-ttu-id="9640f-170">Это поведение является ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="9640f-170">This behavior is expected.</span></span> <span data-ttu-id="9640f-171">Поскольку заявки не всегда утверждены, в договоре покупки не следует резервировать количество или сумму.</span><span class="sxs-lookup"><span data-stu-id="9640f-171">Because requisitions aren't always approved, a quantity or amount should not be reserved on the purchase agreement.</span></span> <span data-ttu-id="9640f-172">Следовательно, максимальная граница из договора покупки не будет достигнута.</span><span class="sxs-lookup"><span data-stu-id="9640f-172">Therefore, you won't meet the maximum limit from the purchase agreement.</span></span>

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a><span data-ttu-id="9640f-173">Торговые соглашения можно создавать из отклоненных запросов предложений.</span><span class="sxs-lookup"><span data-stu-id="9640f-173">Trade agreements can be created from rejected RFQs.</span></span> <span data-ttu-id="9640f-174">Поэтому система не препятствует созданию журналов коммерческих соглашений, если строка запроса предложения не была принята.</span><span class="sxs-lookup"><span data-stu-id="9640f-174">Therefore, the system doesn't prevent trade agreement journals from being created if the RFQ line hasn't been accepted.</span></span>

<span data-ttu-id="9640f-175">Торговые соглашения можно создавать для любых ответов на запрос предложения, независимо от того, были ли они приняты или отклонены.</span><span class="sxs-lookup"><span data-stu-id="9640f-175">You can create trade agreements for any replies for a request for quotation (RFQ), regardless of whether they were accepted or rejected.</span></span> <span data-ttu-id="9640f-176">Дополнительные сведения см. в разделе [Обзор запросов предложений](request-quotations.md).</span><span class="sxs-lookup"><span data-stu-id="9640f-176">For more information, see [Requests for quotation (RFQs) overview](request-quotations.md).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]