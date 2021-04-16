---
title: Использование профиля учета в документах и запросах
description: В данном разделе содержится общая информация об использовании профиля учета.
author: v-nadyuz
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: kfend
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 5674eaf332114d7176a386cb5c5b1a9ea0dcd908
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836804"
---
# <a name="use-an-inventory-profile-in-documents-and-queries"></a><span data-ttu-id="f7154-103">Использование профиля учета в документах и запросах</span><span class="sxs-lookup"><span data-stu-id="f7154-103">Use an inventory profile in documents and queries</span></span>
[!include [banner](../includes/banner.md)]


## <a name="purchase-orders"></a><span data-ttu-id="f7154-104">Заказы на покупку</span><span class="sxs-lookup"><span data-stu-id="f7154-104">Purchase orders</span></span>

### <a name="define-a-posting-profile-in-purchase-orders"></a><span data-ttu-id="f7154-105">Определение профиля разноски в заказах на покупку</span><span class="sxs-lookup"><span data-stu-id="f7154-105">Define a posting profile in purchase orders</span></span>

1. <span data-ttu-id="f7154-106">Перейдите в раздел **Расчеты с поставщиками** \> **Заказы на покупку** \> **Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="f7154-106">Go to **Accounts payable** \> **Purchase orders** \> **All purchase orders**.</span></span>
2. <span data-ttu-id="f7154-107">Выберите Заказа на покупку и перейдите в представление **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="f7154-107">Select a purchase order, and switch to the **Header** view.</span></span>
3. <span data-ttu-id="f7154-108">На Экспресс-вкладке **настройки** в разделе **Профиль учета** в поле **вид деятельности** выберите вид деятельности.</span><span class="sxs-lookup"><span data-stu-id="f7154-108">On the **Setup** FastTab, in the **Inventory profile** section, in the **Kind of activity** field, select a kind of activity.</span></span>
4. <span data-ttu-id="f7154-109">В поле **Профиль учета** выберите профиль учета номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="f7154-109">In the **Inventory profile** field, select an inventory profile.</span></span>

    <span data-ttu-id="f7154-110">Если задать поля **Вид деятельности** и **Профиль учета** в основной записи поставщика в основной записи договора покупки или на странице **Параметры модуля расчетов с поставщиками**, эти значения вводятся по умолчанию в заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="f7154-110">If you set the **Kind of activity** and **Inventory profile** fields in the vendor master record, in the purchase agreement master record, or on the **Accounts payable parameters** page, the values are entered by default in the purchase order.</span></span>

5. <span data-ttu-id="f7154-111">Перейдите к представлению **Строки**.</span><span class="sxs-lookup"><span data-stu-id="f7154-111">Switch to the **Lines** view.</span></span>
6. <span data-ttu-id="f7154-112">На Экспресс-вкладке **сведения по строке** на вкладке **продукт** в разделе **аналитики отслеживания** в поле **Профиль учета** можно выбрать только значение профиля учета, соответствующее виду деятельности, выбранному в заголовке документа.</span><span class="sxs-lookup"><span data-stu-id="f7154-112">On the **Line details** FastTab, on the **Product** tab, in the **Tracking dimensions** section, in the **Inventory profile** field, you can select only an inventory profile value that corresponds to the kind of activity that you selected in the document header.</span></span> <span data-ttu-id="f7154-113">Если выбрано и профиль учета в представлении **заголовка**, в строке можно выбрать только один и тот же профиль учета.</span><span class="sxs-lookup"><span data-stu-id="f7154-113">If you selected and inventory profile in the **Header** view, you can select only the same inventory profile on the line.</span></span>
7. <span data-ttu-id="f7154-114">На вкладке **Настройка** в разделе **Разноска** обратите внимание на следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="f7154-114">On the **Setup** tab, in the **Posting** section, note the following details:</span></span>
    
    - <span data-ttu-id="f7154-115">Поле **счет ГК** недоступно, если для номенклатуры в строке заказа на покупку активен профиль учета.</span><span class="sxs-lookup"><span data-stu-id="f7154-115">The **Ledger account** field isn't available if the inventory profile is active for the item on the purchase order line.</span></span> <span data-ttu-id="f7154-116">Счет ГК определяется профилем учета, указанным в строке заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="f7154-116">The ledger account is determined by the inventory profile that is specified on a purchase order line.</span></span>
    - <span data-ttu-id="f7154-117">Поле **Профиль разноски** устанавливается автоматически в соответствии с профилем запасов в строке заказа на покупку, а также отношение между профилями учета и профилями разноски по поставщику.</span><span class="sxs-lookup"><span data-stu-id="f7154-117">The **Posting profile** field is automatically set, based on the inventory profile on the purchase order line and the relation between the inventory profiles and the vendor posting profiles.</span></span> <span data-ttu-id="f7154-118">Если профиль разноски не может определяться профилем запасов, или если в строке заказа на покупку не выбран профиль учета, поле **Профиль разноски** в строке заказа на покупку остается пустым.</span><span class="sxs-lookup"><span data-stu-id="f7154-118">If the posting profile can't be defined by the inventory profile, or if an inventory profile isn't selected on the purchase order line, the **Posting profile** field on the purchase order line remains blank.</span></span> <span data-ttu-id="f7154-119">В этом случае при разноске накладной будет использоваться профиль разноски, указанный в заголовке заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="f7154-119">In this case, when you post an invoice, the posting profile that is specified in the purchase order header will be used.</span></span>

### <a name="rules-for-automatically-splitting-product-receipts-and-invoices"></a><span data-ttu-id="f7154-120">Правила автоматического разделения поступлений продуктов и накладных</span><span class="sxs-lookup"><span data-stu-id="f7154-120">Rules for automatically splitting product receipts and invoices</span></span>

<span data-ttu-id="f7154-121">При разноске накладной заказа на покупку или поступления продуктов система разделяет документы по профилю разноски и виду действий, определенных в строках заказа.</span><span class="sxs-lookup"><span data-stu-id="f7154-121">When you post a purchase order invoice or product receipt, the system splits the documents by the posting profile and the kind of activity defined on the order lines.</span></span> <span data-ttu-id="f7154-122">Для строк заказа, которые имеют номенклатуры с неактивным профилем учета, используется **основное** действие и профиль разноски, указанный в заголовке заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="f7154-122">For order lines that have items with an inventory profile that isn't active, the **Basic** activity and the posting profile that is specified in the purchase order header are used.</span></span>

#### <a name="example-in-the-rumf-legal-entity"></a><span data-ttu-id="f7154-123">Пример в юридическом лице RUMF</span><span class="sxs-lookup"><span data-stu-id="f7154-123">Example in the RUMF legal entity</span></span>

1. <span data-ttu-id="f7154-124">На странице **Параметры модуля "Закупки и источники"** на вкладке **Сводное обновление** на Экспресс-вкладке **Сводное обновление** в разделе **Разделение на основании** в строке **Поступление продуктов** задайте параметрам **профиль разноски** и **Вид деятельности** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="f7154-124">On the **Procurement and sourcing parameters** page, on the **Summary update** tab, on the **Summary update** FastTab, in the **Split based on** section, on the **Product receipt** line, set the **Posting profile** and **Kind of activity** options to **Yes**.</span></span>
2. <span data-ttu-id="f7154-125">На странице **Параметры расчетов с поставщиками** на вкладке **Главная книга и налог** на Экспресс-вкладке **Разноска** в поле **Профиль разноски** выберите **Общий**.</span><span class="sxs-lookup"><span data-stu-id="f7154-125">On the **Accounts payable parameters** page, on the **Ledger and sales tax** tab, on the **Posting** FastTab, in the **Posting profile** field, select **Общий**.</span></span>
3.  <span data-ttu-id="f7154-126">Создайте два профиля разноски по поставщику: **GEN** и **COM**.</span><span class="sxs-lookup"><span data-stu-id="f7154-126">Create two vendor posting profiles: **GEN** and **COM**.</span></span> <span data-ttu-id="f7154-127">Затем создайте профили учета для **GEN** , **COM** и **MAT**.</span><span class="sxs-lookup"><span data-stu-id="f7154-127">Then create inventory profiles for **GEN**, **COM**, and **MAT**.</span></span> <span data-ttu-id="f7154-128">Наконец, настройте связь между профилями учета и профилями разноски по поставщику.</span><span class="sxs-lookup"><span data-stu-id="f7154-128">Finally, set up a relation between the inventory profiles and the vendor posting profiles.</span></span>

    | <span data-ttu-id="f7154-129">**Связь с профилем учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-129">**Inventory profile relation**</span></span> | <span data-ttu-id="f7154-130">**Вид деятельности**</span><span class="sxs-lookup"><span data-stu-id="f7154-130">**Kind of activity**</span></span> | <span data-ttu-id="f7154-131">**Профиль учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-131">**Inventory profile**</span></span> | <span data-ttu-id="f7154-132">**Профиль разноски по поставщику**</span><span class="sxs-lookup"><span data-stu-id="f7154-132">**Vendor posting profile**</span></span> |
    |--------------------------------|----------------------|-----------------------|----------------------------|
    | <span data-ttu-id="f7154-133">Профиль</span><span class="sxs-lookup"><span data-stu-id="f7154-133">Profile</span></span>                        | <span data-ttu-id="f7154-134">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-134">Basic</span></span>                | <span data-ttu-id="f7154-135">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-135">GEN</span></span>                   | <span data-ttu-id="f7154-136">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-136">GEN</span></span>                        |
    | <span data-ttu-id="f7154-137">Профиль</span><span class="sxs-lookup"><span data-stu-id="f7154-137">Profile</span></span>                        | <span data-ttu-id="f7154-138">Комиссионер</span><span class="sxs-lookup"><span data-stu-id="f7154-138">Commissioner</span></span>         | <span data-ttu-id="f7154-139">COM</span><span class="sxs-lookup"><span data-stu-id="f7154-139">COM</span></span>                   | <span data-ttu-id="f7154-140">COM</span><span class="sxs-lookup"><span data-stu-id="f7154-140">COM</span></span>                        |
    | <span data-ttu-id="f7154-141">Профиль</span><span class="sxs-lookup"><span data-stu-id="f7154-141">Profile</span></span>                        | <span data-ttu-id="f7154-142">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-142">Basic</span></span>                | <span data-ttu-id="f7154-143">MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-143">MAT</span></span>                   | <span data-ttu-id="f7154-144">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-144">GEN</span></span>                        |

4. <span data-ttu-id="f7154-145">Создайте следующие номенклатуры:</span><span class="sxs-lookup"><span data-stu-id="f7154-145">Create the following items:</span></span>

    - <span data-ttu-id="f7154-146">Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-146">Item1</span></span>
    - <span data-ttu-id="f7154-147">Item2</span><span class="sxs-lookup"><span data-stu-id="f7154-147">Item2</span></span>
    - <span data-ttu-id="f7154-148">Item3</span><span class="sxs-lookup"><span data-stu-id="f7154-148">Item3</span></span>
    - <span data-ttu-id="f7154-149">Item4</span><span class="sxs-lookup"><span data-stu-id="f7154-149">Item4</span></span>

5. <span data-ttu-id="f7154-150">Создайте заказ на покупку со следующими строками.</span><span class="sxs-lookup"><span data-stu-id="f7154-150">Create a purchase order that has the following lines.</span></span>

    | <span data-ttu-id="f7154-151">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f7154-151">**Item**</span></span> | <span data-ttu-id="f7154-152">**Профиль учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-152">**Inventory profile**</span></span> | <span data-ttu-id="f7154-153">**Количество**</span><span class="sxs-lookup"><span data-stu-id="f7154-153">**Quantity**</span></span> | <span data-ttu-id="f7154-154">**Профиль разноски по поставщику**</span><span class="sxs-lookup"><span data-stu-id="f7154-154">**Vendor posting profile**</span></span> |
    |----------|-----------------------|--------------|----------------------------|
    | <span data-ttu-id="f7154-155">Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-155">Item1</span></span>    | <span data-ttu-id="f7154-156">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-156">GEN</span></span>                   | <span data-ttu-id="f7154-157">10</span><span class="sxs-lookup"><span data-stu-id="f7154-157">10</span></span>           | <span data-ttu-id="f7154-158">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-158">GEN</span></span>                        |
    | <span data-ttu-id="f7154-159">Item2</span><span class="sxs-lookup"><span data-stu-id="f7154-159">Item2</span></span>    | <span data-ttu-id="f7154-160">MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-160">MAT</span></span>                   | <span data-ttu-id="f7154-161">10</span><span class="sxs-lookup"><span data-stu-id="f7154-161">10</span></span>           | <span data-ttu-id="f7154-162">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-162">GEN</span></span>                        |
    | <span data-ttu-id="f7154-163">Item3</span><span class="sxs-lookup"><span data-stu-id="f7154-163">Item3</span></span>    | <span data-ttu-id="f7154-164">COM</span><span class="sxs-lookup"><span data-stu-id="f7154-164">COM</span></span>                   | <span data-ttu-id="f7154-165">10</span><span class="sxs-lookup"><span data-stu-id="f7154-165">10</span></span>           | <span data-ttu-id="f7154-166">COM</span><span class="sxs-lookup"><span data-stu-id="f7154-166">COM</span></span>                        |
    | <span data-ttu-id="f7154-167">Item4</span><span class="sxs-lookup"><span data-stu-id="f7154-167">Item4</span></span>    |                       | <span data-ttu-id="f7154-168">10</span><span class="sxs-lookup"><span data-stu-id="f7154-168">10</span></span>           |                            |

6. <span data-ttu-id="f7154-169">Создание поступление продукта.</span><span class="sxs-lookup"><span data-stu-id="f7154-169">Create a product receipt.</span></span> <span data-ttu-id="f7154-170">На Экспресс-вкладках **Обзор** и **строки** на странице **Разноска поступлений продуктов** должны отобразиться следующие строки.</span><span class="sxs-lookup"><span data-stu-id="f7154-170">You should see the following lines on the **Overview** and **Lines** FastTabs of the **Posting product receipt** page.</span></span>

      - <span data-ttu-id="f7154-171">Экспресс-вкладка **Обзор**</span><span class="sxs-lookup"><span data-stu-id="f7154-171">**Overview** FastTab</span></span>

        |   <span data-ttu-id="f7154-172">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="f7154-172">Product receipt</span></span>   |  <span data-ttu-id="f7154-173">Профиль разноски по поставщику</span><span class="sxs-lookup"><span data-stu-id="f7154-173">Vendor posting profile</span></span>    |    <span data-ttu-id="f7154-174">Вид деятельности</span><span class="sxs-lookup"><span data-stu-id="f7154-174">Kind of activity</span></span>  | 
        |---------------------|----------------------------|----------------------|
        | <span data-ttu-id="f7154-175">PR1</span><span class="sxs-lookup"><span data-stu-id="f7154-175">PR1</span></span>                 | <span data-ttu-id="f7154-176">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-176">GEN</span></span>                        | <span data-ttu-id="f7154-177">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-177">Basic</span></span>                |
        | <span data-ttu-id="f7154-178">PR2</span><span class="sxs-lookup"><span data-stu-id="f7154-178">PR2</span></span>                 | <span data-ttu-id="f7154-179">COM</span><span class="sxs-lookup"><span data-stu-id="f7154-179">COM</span></span>                        | <span data-ttu-id="f7154-180">Комиссионер</span><span class="sxs-lookup"><span data-stu-id="f7154-180">Commissioner</span></span>         |
        | <span data-ttu-id="f7154-181">PR3</span><span class="sxs-lookup"><span data-stu-id="f7154-181">PR3</span></span>                 | <span data-ttu-id="f7154-182">Общий</span><span class="sxs-lookup"><span data-stu-id="f7154-182">Общий</span></span>                      | <span data-ttu-id="f7154-183">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-183">Basic</span></span>                |
        
     - <span data-ttu-id="f7154-184">Экспресс-вкладка **Строки**</span><span class="sxs-lookup"><span data-stu-id="f7154-184">**Lines** FastTab</span></span>
     
        | <span data-ttu-id="f7154-185">Раздел</span><span class="sxs-lookup"><span data-stu-id="f7154-185">Item</span></span>      |   <span data-ttu-id="f7154-186">Профиль учета</span><span class="sxs-lookup"><span data-stu-id="f7154-186">Inventory profile</span></span>   |   <span data-ttu-id="f7154-187">Количество</span><span class="sxs-lookup"><span data-stu-id="f7154-187">Quantity</span></span>   |
        |-----------|-----------------------|--------------|
        | <span data-ttu-id="f7154-188">Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-188">Item1</span></span>     | <span data-ttu-id="f7154-189">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-189">GEN</span></span>                   | <span data-ttu-id="f7154-190">10</span><span class="sxs-lookup"><span data-stu-id="f7154-190">10</span></span>           |
        | <span data-ttu-id="f7154-191">Item2</span><span class="sxs-lookup"><span data-stu-id="f7154-191">Item2</span></span>     | <span data-ttu-id="f7154-192">MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-192">MAT</span></span>                   | <span data-ttu-id="f7154-193">10</span><span class="sxs-lookup"><span data-stu-id="f7154-193">10</span></span>           |
        | <span data-ttu-id="f7154-194">Item3</span><span class="sxs-lookup"><span data-stu-id="f7154-194">Item3</span></span>     | <span data-ttu-id="f7154-195">COM</span><span class="sxs-lookup"><span data-stu-id="f7154-195">COM</span></span>                   | <span data-ttu-id="f7154-196">10</span><span class="sxs-lookup"><span data-stu-id="f7154-196">10</span></span>           |
        | <span data-ttu-id="f7154-197">Item4</span><span class="sxs-lookup"><span data-stu-id="f7154-197">Item4</span></span>     |                       | <span data-ttu-id="f7154-198">10</span><span class="sxs-lookup"><span data-stu-id="f7154-198">10</span></span>           |
    
    

7. <span data-ttu-id="f7154-199">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="f7154-199">Select **Post**.</span></span> <span data-ttu-id="f7154-200">Создается три поступления продуктов.</span><span class="sxs-lookup"><span data-stu-id="f7154-200">Three product receipts are generated.</span></span> <span data-ttu-id="f7154-201">Для накладных по заказу на покупку будет выполняться аналогичная разбивка.</span><span class="sxs-lookup"><span data-stu-id="f7154-201">A similar split will be done for purchase order invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="f7154-202">Если накладные расходы прикрепляются к заголовку заказа на покупку, при разноске накладных по заказу на покупку, разбитых по видам деятельности и профилям разноски, эти накладные расходы будут присоединены к каждой накладной.</span><span class="sxs-lookup"><span data-stu-id="f7154-202">If miscellaneous charges are attached to the purchase order header, when you post purchase order invoices that split by kinds of activity and posting profiles, those miscellaneous charges will be attached to each invoice.</span></span>

### <a name="rules-for-automatically-splitting-invoice-factures"></a><span data-ttu-id="f7154-203">Правила автоматической разбивки счетов-фактур по накладным</span><span class="sxs-lookup"><span data-stu-id="f7154-203">Rules for automatically splitting invoice-factures</span></span>

<span data-ttu-id="f7154-204">Если обработка счетов-фактур по накладным выполняется одновременно с разноской накладных по заказу на покупку, то разбиение по счетам-фактурам по накладным совпадает с разбивкой накладной по виду деятельности и профиль разноски.</span><span class="sxs-lookup"><span data-stu-id="f7154-204">If you process the invoice-factures at the same time that purchase order invoices are posted, the invoice-facture split is the same as the invoice split by the kind of activity and the posting profile.</span></span>

<span data-ttu-id="f7154-205">Если обработать счета-фактуры по накладным позднее (например, из журнала накладных поставщиков), можно комбинировать строки разных накладных, имеющих одинаковый вид деятельности, в одну счет-фактуру по накладным.</span><span class="sxs-lookup"><span data-stu-id="f7154-205">If you process invoice-factures later (for example, from a vendor invoice journal), you can combine the lines of different invoices that have the same kind of activity into one invoice-facture.</span></span> <span data-ttu-id="f7154-206">Для использования этого подхода выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f7154-206">To use this approach, follow these steps.</span></span>

1. <span data-ttu-id="f7154-207">Перейдите в раздел **Расчеты с поставщиками** \> **Запросы и отчеты** \> **Накладные** \> **Журнал накладных**.</span><span class="sxs-lookup"><span data-stu-id="f7154-207">Go to **Accounts payable** \> **Inquiries and reports** \> **Invoices** \> **Invoice journal**.</span></span>
2. <span data-ttu-id="f7154-208">Выберите накладную поставщика, для которой нет обработанной счета-фактуры по накладным, а затем выберите **создать фактуру \> обновления фактуры**.</span><span class="sxs-lookup"><span data-stu-id="f7154-208">Select a vendor invoice that doesn't have a processed invoice-facture, and then select **Create facture \> Update facture**.</span></span>
3. <span data-ttu-id="f7154-209">На странице **Обновление фактуры** в верхней области в поле **вид деятельности** выберите вид деятельности, для которого необходимо обработать счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="f7154-209">On the **Update facture** page, in the upper pane, in the **Kind of activity** field, select the kind of activity that you want to process factures for.</span></span> <span data-ttu-id="f7154-210">В нижней области отображаются накладные, имеющие выбранный вид деятельности.</span><span class="sxs-lookup"><span data-stu-id="f7154-210">The lower pane shows the invoices that have the selected kind of activity.</span></span>

   ![Страница обновления счета-фактуры](media/14_Update_facture.png)

<span data-ttu-id="f7154-212">Система сохраняет вид деятельности, который используется для разноски в поступления продуктов, накладные и счетов-фактур по накладным для заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="f7154-212">The system saves the kind of activity that is used for posting in the product receipts, invoices, and invoice-factures for the purchase order.</span></span> <span data-ttu-id="f7154-213">Вы можете просмотреть вид деятельности в следующих местах:</span><span class="sxs-lookup"><span data-stu-id="f7154-213">You can view the kind of activity in the following places:</span></span>

- <span data-ttu-id="f7154-214">В поле **вид деятельности** на вкладке **Обзор** в верхней области страницы **Журнал накладных** (**Расчеты с поставщиками** \> **Запросы и отчеты** \> **Накладные** \> **Журнал накладных**).</span><span class="sxs-lookup"><span data-stu-id="f7154-214">In the **Kind of activity** field on the **Overview** tab in the upper pane of the **Invoice journal** page (**Accounts payable** \> **Inquiries and reports** \> **Invoices** \> **Invoice journal**).</span></span>
- <span data-ttu-id="f7154-215">В поле **вид деятельности** на вкладке **Общие** в верхней области страницы **Журнал накладных** (**Расчеты с поставщиками** \> **Запросы и отчеты** \> **Счет-фактура**).</span><span class="sxs-lookup"><span data-stu-id="f7154-215">In the **Kind of activity** field on the **General** tab in the upper pane of the **Facture journal** page (**Accounts payable** \> **Inquiries and reports** \> **Facture**).</span></span>

## <a name="sales-orders"></a><span data-ttu-id="f7154-216">Заказы на продажу</span><span class="sxs-lookup"><span data-stu-id="f7154-216">Sales orders</span></span>

### <a name="define-a-posting-profile-in-sales-orders"></a><span data-ttu-id="f7154-217">Определение профиля разноски в заказах на продажу</span><span class="sxs-lookup"><span data-stu-id="f7154-217">Define a posting profile in sales orders</span></span>

1. <span data-ttu-id="f7154-218">Перейдите в раздел **Расчеты с клиентами** \> **Заказы** \> **Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="f7154-218">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="f7154-219">Выберите Заказ на продажу и перейдите в представление **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="f7154-219">Select a sales order, and switch to the **Header** view.</span></span>
3. <span data-ttu-id="f7154-220">На Экспресс-вкладке **настройки** в разделе **Профиль учета** в поле **вид деятельности** выберите вид деятельности.</span><span class="sxs-lookup"><span data-stu-id="f7154-220">On the **Setup** FastTab, in the **Inventory profile** section, in the **Kind of activity** field, select a kind of activity.</span></span>
4. <span data-ttu-id="f7154-221">В поле **Профиль учета** выберите профиль учета номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="f7154-221">In the **Inventory profile** field, select an inventory profile.</span></span>
5. <span data-ttu-id="f7154-222">Установите флажок **использовать совместимые профили учета** на **Да**, если профили учета, совместимые с профилем учета, которые выбраны в заголовке заказа на продажу, должны использоваться в строках заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="f7154-222">Set the **Use compatible inventory profiles** option to **Yes** if inventory profiles that are compatible with the inventory profile that is selected in the sales order header should be used on the sales order lines.</span></span>

    <span data-ttu-id="f7154-223">Если задать поля **Вид деятельности** и **Профиль учета** в основной записи клиента в основной записи договора продажи или на странице **Параметры модуля расчетов с клиентами**, эти значения вводятся по умолчанию в заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="f7154-223">If you set the **Kind of activity** and **Inventory profile** fields in the customer master record, in the sales agreement master record, or on the **Accounts receivable parameters** page, the values are entered by default in the sales order.</span></span>

6. <span data-ttu-id="f7154-224">Перейдите к представлению **Строки**.</span><span class="sxs-lookup"><span data-stu-id="f7154-224">Switch to the **Lines** view.</span></span>
7. <span data-ttu-id="f7154-225">На Экспресс-вкладке **сведения по строке** на вкладке **продукт** в разделе **аналитики отслеживания** в поле **Профиль учета** можно выбрать только профиль учета, совместимый с вид деятельности, выбранному в заголовке.</span><span class="sxs-lookup"><span data-stu-id="f7154-225">On the **Line details** FastTab, on the **Product** tab, in the **Tracking dimensions** section, in the **Inventory profile** field, you can select only an inventory profile that is compatible with the kind of activity that you selected in the header.</span></span>
8. <span data-ttu-id="f7154-226">На вкладке **Настройка** в разделе **Разноска** обратите внимание на следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="f7154-226">On the **Setup** tab, in the **Posting** section, note the following details:</span></span>

    - <span data-ttu-id="f7154-227">Поле **Счет ГК** не может редактироваться, если для номенклатуры в строке заказа на продажу активен профиль учета.</span><span class="sxs-lookup"><span data-stu-id="f7154-227">The **Main account** field isn't editable if the inventory profile is active for the item on the sales order line.</span></span> <span data-ttu-id="f7154-228">Счет ГК определяется профилем учета, указанным в строке заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="f7154-228">The ledger account is determined by the inventory profile that is specified on a sales order line.</span></span>
    - <span data-ttu-id="f7154-229">Поле **Профиль разноски** устанавливается автоматически в соответствии с профилем запасов в строке заказа на продажу, а также отношение между профилями учета и профилями разноски.</span><span class="sxs-lookup"><span data-stu-id="f7154-229">The **Posting profile** field is automatically set, based on the inventory profile on the sales order line and the relation between the inventory profiles and the posting profiles.</span></span> <span data-ttu-id="f7154-230">Если профиль разноски не может определяться профилем запасов, или если в строке заказа на продажу не выбран профиль учета, поле **Профиль разноски** в строке заказа на продажу остается пустым.</span><span class="sxs-lookup"><span data-stu-id="f7154-230">If the posting profile can't be defined by the inventory profile, or if an inventory profile isn't selected on the sales order line, the **Posting profile** field on the sales order line remains blank.</span></span> <span data-ttu-id="f7154-231">В этом случае при разноске накладной будет использоваться профиль разноски, указанный в заголовке заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="f7154-231">In this case, when you post an invoice, the posting profile that is specified in the sales order header will be used.</span></span>

<span data-ttu-id="f7154-232">При разноске накладной заказа на продажу или отборочной накладной система разделяет документы по профилям разноски и видам действий, которые определены в строках заказа.</span><span class="sxs-lookup"><span data-stu-id="f7154-232">When you post a sales order invoice or packing slip, the system splits the documents by the posting profiles and kinds of activity that are defined in the order lines.</span></span> <span data-ttu-id="f7154-233">Для строк заказа, которые имеют номенклатуры, для которых не активен профиль учета, используется **основной** вид деятельности и профиль разноски, указанный в заголовке заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="f7154-233">For order lines that have items where the inventory profile isn't active, the **Basic** kind of activity and the posting profile that is specified in the sales order header are used.</span></span>

### <a name="create-sales-order-lines"></a><span data-ttu-id="f7154-234">Создание строк заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="f7154-234">Create sales order lines</span></span>

<span data-ttu-id="f7154-235">При создании строк заказа на продажу с помощью команды **Добавить строки**, если профиль учета не выбран, система автоматически разделяет количество, которое будет продаваться профилями учета, для которых имеется физически доступная сумма сальдо.</span><span class="sxs-lookup"><span data-stu-id="f7154-235">When you create sales order lines by selecting **Add lines**, if you don't select the inventory profile, the system automatically splits the quantity that will be sold by the inventory profiles that there are physically available balances for.</span></span>

### <a name="example"></a><span data-ttu-id="f7154-236">Пример</span><span class="sxs-lookup"><span data-stu-id="f7154-236">Example</span></span>

1. <span data-ttu-id="f7154-237">Настройка следующих профилей учета.</span><span class="sxs-lookup"><span data-stu-id="f7154-237">Set up the following inventory profiles.</span></span>

| <span data-ttu-id="f7154-238">Профиль учета</span><span class="sxs-lookup"><span data-stu-id="f7154-238">Inventory profile</span></span> | <span data-ttu-id="f7154-239">Вид деятельности</span><span class="sxs-lookup"><span data-stu-id="f7154-239">Kind of activity</span></span> | <span data-ttu-id="f7154-240">Приоритет сопоставления</span><span class="sxs-lookup"><span data-stu-id="f7154-240">Matching priority</span></span> | <span data-ttu-id="f7154-241">Совместимые профили учета</span><span class="sxs-lookup"><span data-stu-id="f7154-241">Compatible inventory profiles</span></span> | <span data-ttu-id="f7154-242">Физически доступная сумма сальдо номенклатуры Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-242">Physically available balance of item Item1</span></span> |
|-------------------|------------------|-------------------|-------------------------------|--------------------------------------------|
| <span data-ttu-id="f7154-243">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-243">GEN</span></span>               | <span data-ttu-id="f7154-244">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-244">Basic</span></span>            | <span data-ttu-id="f7154-245">1</span><span class="sxs-lookup"><span data-stu-id="f7154-245">1</span></span>                 | <span data-ttu-id="f7154-246">COM, MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-246">COM, MAT</span></span>                      | <span data-ttu-id="f7154-247">8</span><span class="sxs-lookup"><span data-stu-id="f7154-247">8</span></span>                                          |
| <span data-ttu-id="f7154-248">MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-248">MAT</span></span>               | <span data-ttu-id="f7154-249">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-249">Basic</span></span>            | <span data-ttu-id="f7154-250">2</span><span class="sxs-lookup"><span data-stu-id="f7154-250">2</span></span>                 | <span data-ttu-id="f7154-251">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-251">GEN</span></span>                           | <span data-ttu-id="f7154-252">7</span><span class="sxs-lookup"><span data-stu-id="f7154-252">7</span></span>                                          |
| <span data-ttu-id="f7154-253">COM</span><span class="sxs-lookup"><span data-stu-id="f7154-253">COM</span></span>               | <span data-ttu-id="f7154-254">Комиссионер</span><span class="sxs-lookup"><span data-stu-id="f7154-254">Commissioner</span></span>     | <span data-ttu-id="f7154-255">3</span><span class="sxs-lookup"><span data-stu-id="f7154-255">3</span></span>                 |                               | <span data-ttu-id="f7154-256">10</span><span class="sxs-lookup"><span data-stu-id="f7154-256">10</span></span>                                         |

2. <span data-ttu-id="f7154-257">На странице **Параметры модуля расчетов с клиентами** установите для параметра **разбивка строк заказа по профилям учета** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="f7154-257">On the **Accounts receivable parameters** page, set the **Split order lines by inventory profiles** option to **Yes**.</span></span>
3. <span data-ttu-id="f7154-258">Создание нового заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="f7154-258">Create a new sales order.</span></span>
4. <span data-ttu-id="f7154-259">На экспресс-вкладке **Строки заказа на продажу** выберите **Добавить строки**.</span><span class="sxs-lookup"><span data-stu-id="f7154-259">On the **Sales order lines** FastTab, select **Add lines**.</span></span>
5. <span data-ttu-id="f7154-260">В диалоговом окне **Создание строк** установите следующие поля в строке, которая содержит ссылку на **Item1**, в поле **код номенклатуры**:</span><span class="sxs-lookup"><span data-stu-id="f7154-260">In the **Create lines** dialog box, set the following fields on the line that has the **Item1** reference in the **Item number** field:</span></span>

    - <span data-ttu-id="f7154-261">В поле **Продаваемое количество** введите **20**.</span><span class="sxs-lookup"><span data-stu-id="f7154-261">In the **Sales quantity** field, enter **20**.</span></span>
    - <span data-ttu-id="f7154-262">Оставьте поле **Профиль учета** пустым.</span><span class="sxs-lookup"><span data-stu-id="f7154-262">Leave the **Inventory profile** field blank.</span></span>

6. <span data-ttu-id="f7154-263">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f7154-263">Select **Create**.</span></span> <span data-ttu-id="f7154-264">В зависимости от настроек заказа на продажу система создает следующие строки заказа на продажу:</span><span class="sxs-lookup"><span data-stu-id="f7154-264">Depending on the sales order settings, the system creates the following sales order lines:</span></span>

    - <span data-ttu-id="f7154-265">**Вариант 1:** заказ на продажу имеет следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="f7154-265">**Option 1:** The sales order has the following settings.</span></span>

        | <span data-ttu-id="f7154-266">**Вид деятельности**</span><span class="sxs-lookup"><span data-stu-id="f7154-266">**Kind of activity**</span></span> | <span data-ttu-id="f7154-267">**Профиль учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-267">**Inventory profile**</span></span> | <span data-ttu-id="f7154-268">**Использовать совместимые профили учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-268">**Use compatible inventory profiles**</span></span> |
        |----------------------|-----------------------|---------------------------------------|
        | <span data-ttu-id="f7154-269">Не определено</span><span class="sxs-lookup"><span data-stu-id="f7154-269">Unspecified</span></span>          |                       | <span data-ttu-id="f7154-270">Нет</span><span class="sxs-lookup"><span data-stu-id="f7154-270">No</span></span>                                    |

        <span data-ttu-id="f7154-271">В этом случае система создает следующие строки.</span><span class="sxs-lookup"><span data-stu-id="f7154-271">In this case, the system creates the following lines.</span></span>

        | <span data-ttu-id="f7154-272">**Код номенклатуры**</span><span class="sxs-lookup"><span data-stu-id="f7154-272">**Item number**</span></span> | <span data-ttu-id="f7154-273">**Профиль учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-273">**Inventory profile**</span></span> | <span data-ttu-id="f7154-274">**Количество**</span><span class="sxs-lookup"><span data-stu-id="f7154-274">**Quantity**</span></span> |
        |-----------------|-----------------------|--------------|
        | <span data-ttu-id="f7154-275">Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-275">Item1</span></span>           | <span data-ttu-id="f7154-276">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-276">GEN</span></span>                   | <span data-ttu-id="f7154-277">8</span><span class="sxs-lookup"><span data-stu-id="f7154-277">8</span></span>            |
        | <span data-ttu-id="f7154-278">Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-278">Item1</span></span>           | <span data-ttu-id="f7154-279">MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-279">MAT</span></span>                   | <span data-ttu-id="f7154-280">7</span><span class="sxs-lookup"><span data-stu-id="f7154-280">7</span></span>            |
        | <span data-ttu-id="f7154-281">Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-281">Item1</span></span>           | <span data-ttu-id="f7154-282">COM</span><span class="sxs-lookup"><span data-stu-id="f7154-282">COM</span></span>                   | <span data-ttu-id="f7154-283">5</span><span class="sxs-lookup"><span data-stu-id="f7154-283">5</span></span>            |

        <span data-ttu-id="f7154-284">Система выбирает профили учета из сальдо на основе приоритета выбора профилей учета.</span><span class="sxs-lookup"><span data-stu-id="f7154-284">The system selects the inventory profiles from the balances, based on the priority for the selection of inventory profiles.</span></span>

    - <span data-ttu-id="f7154-285">**Вариант 2:** заказ на продажу имеет следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="f7154-285">**Option 2:** The sales order has the following settings.</span></span>

        | <span data-ttu-id="f7154-286">**Вид деятельности**</span><span class="sxs-lookup"><span data-stu-id="f7154-286">**Kind of activity**</span></span> | <span data-ttu-id="f7154-287">**Профиль учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-287">**Inventory profile**</span></span> | <span data-ttu-id="f7154-288">**Использовать совместимые профили учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-288">**Use compatible inventory profiles**</span></span> |
        |----------------------|-----------------------|---------------------------------------|
        | <span data-ttu-id="f7154-289">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-289">Basic</span></span>                |                       | <span data-ttu-id="f7154-290">Нет</span><span class="sxs-lookup"><span data-stu-id="f7154-290">No</span></span>                                    |

        <span data-ttu-id="f7154-291">В этом случае система создает следующие строки.</span><span class="sxs-lookup"><span data-stu-id="f7154-291">In this case, the system creates the following lines.</span></span>

        | <span data-ttu-id="f7154-292">**Код номенклатуры**</span><span class="sxs-lookup"><span data-stu-id="f7154-292">**Item number**</span></span> | <span data-ttu-id="f7154-293">**Профиль учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-293">**Inventory profile**</span></span> | <span data-ttu-id="f7154-294">**Количество**</span><span class="sxs-lookup"><span data-stu-id="f7154-294">**Quantity**</span></span> |
        |-----------------|-----------------------|--------------|
        | <span data-ttu-id="f7154-295">Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-295">Item1</span></span>           | <span data-ttu-id="f7154-296">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-296">GEN</span></span>                   | <span data-ttu-id="f7154-297">13</span><span class="sxs-lookup"><span data-stu-id="f7154-297">13</span></span>           |
        | <span data-ttu-id="f7154-298">Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-298">Item1</span></span>           | <span data-ttu-id="f7154-299">MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-299">MAT</span></span>                   | <span data-ttu-id="f7154-300">7</span><span class="sxs-lookup"><span data-stu-id="f7154-300">7</span></span>            |

        <span data-ttu-id="f7154-301">Система выбирает профили учета из сальдо на основе приоритета выбора профилей учета и указанного вида деятельности.</span><span class="sxs-lookup"><span data-stu-id="f7154-301">The system selects inventory profiles from the balances, based on the priority for the selection of inventory profiles and the specified kind of activity.</span></span> <span data-ttu-id="f7154-302">Система добавляет количество, отсутствующее в сальдо, в строку заказа, содержащую профиль учета, который обладает наивысшим приоритетом выбора (**GEN** в данном примере).</span><span class="sxs-lookup"><span data-stu-id="f7154-302">The system adds the quantity that is missing in the balances to the order line that contains the inventory profile has the highest selection priority (**GEN** in this example).</span></span>

    - <span data-ttu-id="f7154-303">**Вариант 3:** заказ на продажу имеет следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="f7154-303">**Option 3:** The sales order has the following settings.</span></span>

        | <span data-ttu-id="f7154-304">**Вид деятельности**</span><span class="sxs-lookup"><span data-stu-id="f7154-304">**Kind of activity**</span></span> | <span data-ttu-id="f7154-305">**Профиль учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-305">**Inventory profile**</span></span> | <span data-ttu-id="f7154-306">**Использовать совместимые профили учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-306">**Use compatible inventory profiles**</span></span> |
        |----------------------|-----------------------|---------------------------------------|
        | <span data-ttu-id="f7154-307">Не определено</span><span class="sxs-lookup"><span data-stu-id="f7154-307">Unspecified</span></span>          |                       | <span data-ttu-id="f7154-308">Да</span><span class="sxs-lookup"><span data-stu-id="f7154-308">Yes</span></span>                                   |

        <span data-ttu-id="f7154-309">В этом случае система создает следующие строки.</span><span class="sxs-lookup"><span data-stu-id="f7154-309">In this case, the system creates the following lines.</span></span>

        | <span data-ttu-id="f7154-310">**Код номенклатуры**</span><span class="sxs-lookup"><span data-stu-id="f7154-310">**Item number**</span></span> | <span data-ttu-id="f7154-311">**Профиль учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-311">**Inventory profile**</span></span> | <span data-ttu-id="f7154-312">**Количество**</span><span class="sxs-lookup"><span data-stu-id="f7154-312">**Quantity**</span></span> |
        |-----------------|-----------------------|--------------|
        | <span data-ttu-id="f7154-313">Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-313">Item1</span></span>           | <span data-ttu-id="f7154-314">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-314">GEN</span></span>                   | <span data-ttu-id="f7154-315">8</span><span class="sxs-lookup"><span data-stu-id="f7154-315">8</span></span>            |
        | <span data-ttu-id="f7154-316">Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-316">Item1</span></span>           | <span data-ttu-id="f7154-317">COM</span><span class="sxs-lookup"><span data-stu-id="f7154-317">COM</span></span>                   | <span data-ttu-id="f7154-318">10</span><span class="sxs-lookup"><span data-stu-id="f7154-318">10</span></span>           |
        | <span data-ttu-id="f7154-319">Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-319">Item1</span></span>           | <span data-ttu-id="f7154-320">MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-320">MAT</span></span>                   | <span data-ttu-id="f7154-321">2</span><span class="sxs-lookup"><span data-stu-id="f7154-321">2</span></span>            |

        <span data-ttu-id="f7154-322">Система выбирает профили учета из сальдо на основе приоритета выбора профилей учета и параметров совместимых профилей учета.</span><span class="sxs-lookup"><span data-stu-id="f7154-322">The system selects the inventory profiles from the balances, based on the priority for the selection of inventory profiles and the settings of compatible inventory profiles.</span></span> <span data-ttu-id="f7154-323">Сначала выбирается профиль учета **GEN**, так как он имеет наивысший приоритет.</span><span class="sxs-lookup"><span data-stu-id="f7154-323">First, the **GEN** inventory profile is selected, because it has the highest priority.</span></span> <span data-ttu-id="f7154-324">Затем выбираются профили учета **COM** и **MAT**, совместимые с профилем учета **GEN**, в соответствии с процедурой выбора совместимых профилей учета.</span><span class="sxs-lookup"><span data-stu-id="f7154-324">Then the **COM** and **MAT** inventory profiles that are compatible with the **GEN** inventory profile are selected, in accordance with the procedure for selecting compatible inventory profiles.</span></span>

    - <span data-ttu-id="f7154-325">**Вариант 4:** заказ на продажу имеет следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="f7154-325">**Option 4:** The sales order has the following settings.</span></span>

        | <span data-ttu-id="f7154-326">**Вид деятельности**</span><span class="sxs-lookup"><span data-stu-id="f7154-326">**Kind of activity**</span></span> | <span data-ttu-id="f7154-327">**Профиль учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-327">**Inventory profile**</span></span> | <span data-ttu-id="f7154-328">**Использовать совместимые профили учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-328">**Use compatible inventory profiles**</span></span> |
        |----------------------|-----------------------|---------------------------------------|
        | <span data-ttu-id="f7154-329">Не определено</span><span class="sxs-lookup"><span data-stu-id="f7154-329">Unspecified</span></span>          | <span data-ttu-id="f7154-330">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-330">GEN</span></span>                   | <span data-ttu-id="f7154-331">Да</span><span class="sxs-lookup"><span data-stu-id="f7154-331">Yes</span></span>                                   |

        <span data-ttu-id="f7154-332">В этом случае система создает следующие строки.</span><span class="sxs-lookup"><span data-stu-id="f7154-332">In this case, the system creates the following lines.</span></span>

        | <span data-ttu-id="f7154-333">**Код номенклатуры**</span><span class="sxs-lookup"><span data-stu-id="f7154-333">**Item number**</span></span> | <span data-ttu-id="f7154-334">**Профиль учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-334">**Inventory profile**</span></span> | <span data-ttu-id="f7154-335">**Количество**</span><span class="sxs-lookup"><span data-stu-id="f7154-335">**Quantity**</span></span> |
        |-----------------|-----------------------|--------------|
        | <span data-ttu-id="f7154-336">Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-336">Item1</span></span>           | <span data-ttu-id="f7154-337">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-337">GEN</span></span>                   | <span data-ttu-id="f7154-338">13</span><span class="sxs-lookup"><span data-stu-id="f7154-338">13</span></span>           |
        | <span data-ttu-id="f7154-339">Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-339">Item1</span></span>           | <span data-ttu-id="f7154-340">MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-340">MAT</span></span>                   | <span data-ttu-id="f7154-341">7</span><span class="sxs-lookup"><span data-stu-id="f7154-341">7</span></span>            |

        <span data-ttu-id="f7154-342">Система выбирает профили учета из сальдо на основе приоритета выбора профилей учета в заказе на продажу и параметров совместимых профилей учета.</span><span class="sxs-lookup"><span data-stu-id="f7154-342">The system selects the inventory profiles from the balances, based on the inventory profile that is selected in the sales order and the settings of compatible inventory profiles.</span></span> <span data-ttu-id="f7154-343">Могут быть выбраны только профили учета, соответствующие видам деятельности, указанному в заказе на продажу.</span><span class="sxs-lookup"><span data-stu-id="f7154-343">Only the inventory profiles that correspond to the kind of activity that is specified in the sales order can be selected.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="f7154-344">Заказы на перемещение</span><span class="sxs-lookup"><span data-stu-id="f7154-344">Transfer orders</span></span>

1. <span data-ttu-id="f7154-345">Перейдите к **Управление запасами** \> **Входящие заказы** \> **Заказ на перемещение** или **Управление запасами** \> **Исходящие заказы** \> **Заказ на перемещение**.</span><span class="sxs-lookup"><span data-stu-id="f7154-345">Go to **Inventory management** \> **Inbound orders** \> **Transfer order** or **Inventory management** \> **Outbound orders** \> **Transfer order**.</span></span>
2. <span data-ttu-id="f7154-346">Выберите заказ на перемещение и перейдите в представление **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="f7154-346">Select a transfer order, and switch to the **Header** view.</span></span>
3. <span data-ttu-id="f7154-347">На Экспресс-вкладке **настройки** в разделе **Профиль учета** в поле **вид деятельности** выберите вид деятельности.</span><span class="sxs-lookup"><span data-stu-id="f7154-347">On the **Setup** FastTab, in the **Inventory profile** section, in the **Kind of activity** field, select a kind of activity.</span></span>
4. <span data-ttu-id="f7154-348">В поле **Профиль учета** выберите профиль учета номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="f7154-348">In the **Inventory profile** field, select an inventory profile.</span></span>
5. <span data-ttu-id="f7154-349">Установите флажок **использовать совместимые профили учета** на **Да**, если профили учета, совместимые с профилем учета, которые выбраны в заголовке заказа на перемещение, должны использоваться в строках заказа на перемещение.</span><span class="sxs-lookup"><span data-stu-id="f7154-349">Set the **Use compatible inventory profiles** option to **Yes** if inventory profiles that are compatible with the inventory profile that is selected in the transfer order header should be used on the transfer order lines.</span></span>

<span data-ttu-id="f7154-350">Если задать поля **Вид деятельности** и **Профиль учета** в основной записи склада или на странице **Параметры модуля "Управление запасами и складами"**, эти значения вводятся по умолчанию в заказ на перемещение.</span><span class="sxs-lookup"><span data-stu-id="f7154-350">If you set the **Kind of activity** and **Inventory profile** fields in the warehouse master record or on the **Inventory and warehouse management parameters** page, the values are entered by default in the transfer order.</span></span> <span data-ttu-id="f7154-351">По умолчанию для параметра **использовать совместимые профили учета** устанавливается значение, равное значению на странице **Параметры управления запасами и складами**.</span><span class="sxs-lookup"><span data-stu-id="f7154-351">By default, the **Use compatible inventory profiles** option is set to the same value that it's set to on the **Inventory and warehouse management parameters** page.</span></span>

## <a name="inventory-journals-and-production-orders"></a><span data-ttu-id="f7154-352">Журналы запасов и производственные заказы</span><span class="sxs-lookup"><span data-stu-id="f7154-352">Inventory journals and production orders</span></span>

<span data-ttu-id="f7154-353">Профиль учета можно использовать в следующих журналах запасов, так же как и другие складские аналитики:</span><span class="sxs-lookup"><span data-stu-id="f7154-353">You can use the inventory profile in the following inventory journals, just as you can use other inventory dimensions:</span></span>

- <span data-ttu-id="f7154-354">Перемещение (**Управление запасами** \> **Записи журнала** \> **Номенклатуры** \> **Перемещение**)</span><span class="sxs-lookup"><span data-stu-id="f7154-354">Movement (**Inventory management** \> **Journal entries** \> **Items** \> **Movement**)</span></span>
- <span data-ttu-id="f7154-355">Корректировка запасов (**Управление запасами** \> **Записи журнала** \> **Номенклатуры** \> **Корректировка запасов**)</span><span class="sxs-lookup"><span data-stu-id="f7154-355">Inventory adjustment (**Inventory management** \> **Journal entries** \> **Items** \> **Inventory adjustment**)</span></span>
- <span data-ttu-id="f7154-356">Спецификации (**Управление запасами** \> **Записи журнала** \> **Номенклатуры** \> **Спецификации**)</span><span class="sxs-lookup"><span data-stu-id="f7154-356">Bills of materials (**Inventory management** \> **Journal entries** \> **Items** \> **Bills of materials**)</span></span>
- <span data-ttu-id="f7154-357">Инвентаризация (**Управление запасами** \> **Записи журнала** \> **Инвентаризация номенклатуры** \> **Инвентаризация**)</span><span class="sxs-lookup"><span data-stu-id="f7154-357">Counting (**Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**)</span></span>

<span data-ttu-id="f7154-358">В журнале перемещений (**Управление запасами** \> **Записи журнала** \> **Номенклатуры** \> **Перемещение**) на Экспресс-вкладке **Сведения по строке** в разделах **из складских аналитик** и **в складские аналитики** можно выбрать только те профили учета, которые имеют одинаковый вид деятельности.</span><span class="sxs-lookup"><span data-stu-id="f7154-358">In the Transfer journal (**Inventory management** \> **Journal entries** \> **Items** \> **Transfer**), on the **Line details** FastTab, in the **From inventory dimensions** and **To inventory dimensions** sections, you can select only inventory profiles that have the same kind of activity.</span></span> <span data-ttu-id="f7154-359">При разноске журнала ваучеры из главной книги создаются только в том случае, если эти профили учета отличаются.</span><span class="sxs-lookup"><span data-stu-id="f7154-359">When you post the journal, general ledger vouchers are created only if these inventory profiles differ.</span></span> <span data-ttu-id="f7154-360">В этом случае строка журнала перемещения разносится в главную книгу, независимо от значения поля **журналы переноса и заказы на перемещение** в разделе **Финансовая Разноска** на вкладке **Общие** на странице **Параметры управления запасами и складами**.</span><span class="sxs-lookup"><span data-stu-id="f7154-360">In this case, the transfer journal line is posted to the general ledger, regardless of the value of the **Transfer journals and transfer orders** field in the **Financial posting** section on the **General** tab of the **Inventory and warehouse management parameters** page.</span></span>

<span data-ttu-id="f7154-361">При создании производственного заказа, если строка спецификации содержит номенклатуру, в которой активен профиль учета, соответствующая строка спецификации в производственном заказе будет иметь профиль учета из одного из следующих мест:</span><span class="sxs-lookup"><span data-stu-id="f7154-361">When you create a production order, if the BOM line contains an item where the inventory profile is active, the corresponding BOM line in the production order will have the inventory profile from one of the following places:</span></span>

- <span data-ttu-id="f7154-362">Строка спецификации, если в ней указан профиль учета</span><span class="sxs-lookup"><span data-stu-id="f7154-362">The BOM line, if the inventory profile is specified there</span></span>
- <span data-ttu-id="f7154-363">Страница **Параметры управления запасами и складами**, если в ней указан профиль учета</span><span class="sxs-lookup"><span data-stu-id="f7154-363">The **Inventory and warehouse management parameters** page, if the inventory profile is specified there</span></span>

<span data-ttu-id="f7154-364">Если значение аналитики **профиля учета** для строки спецификации производственного заказа не может быть определено, создается сообщение об ошибке, и создание производственного заказа отменяется.</span><span class="sxs-lookup"><span data-stu-id="f7154-364">If the value of the **Inventory profile** dimension for the production order BOM line can't be determined, an error message is generated, and creation of the production order is canceled.</span></span>

## <a name="filter-the-on-hand-list-page-by-the-kind-of-activity"></a><span data-ttu-id="f7154-365">Фильтрация страницы Список количества в наличии по видам деятельности</span><span class="sxs-lookup"><span data-stu-id="f7154-365">Filter the On-hand list page by the kind of activity</span></span>

<span data-ttu-id="f7154-366">На странице **Список количества в наличии** можно фильтровать по видам деятельности.</span><span class="sxs-lookup"><span data-stu-id="f7154-366">On the **On-hand list** page, you can filter by the kind of activity.</span></span>

1. <span data-ttu-id="f7154-367">Перейдите в раздел **Управление запасами** \> **Запросы и отчеты** \> **Список количества в наличии**.</span><span class="sxs-lookup"><span data-stu-id="f7154-367">Go to **Inventory management** \> **Inquiries and reports** \> **On-hand list**.</span></span>
2. <span data-ttu-id="f7154-368">В верхней области в поле **вид деятельности** выберите вид деятельности, для которого необходимо просмотреть сальдо по номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="f7154-368">In the upper pane, in the **Kind of activity** field, select the kind of activity that you want to see item balances for.</span></span>

<span data-ttu-id="f7154-369">В запросе отображаются только сальдо по номенклатуре для профилей учета, которые относятся к выбранному виду деятельности.</span><span class="sxs-lookup"><span data-stu-id="f7154-369">The query shows only the item balances for the inventory profiles that are related to the selected kind of activity.</span></span> <span data-ttu-id="f7154-370">Отображаются только те номенклатуры, для которых активна складская аналитика **Профиль учета**.</span><span class="sxs-lookup"><span data-stu-id="f7154-370">Only items where the **Inventory profile** inventory dimension is active are shown.</span></span> <span data-ttu-id="f7154-371">Чтобы отобразить все сальдо, независимо от вида деятельности, выберите значение не **Не указано** в поле **вид деятельности**.</span><span class="sxs-lookup"><span data-stu-id="f7154-371">To show all balances, regardless of the kind of activity, select **Unspecified** in the **Kind of activity** field.</span></span>

## <a name="cash-flow-forecasts-on-purchase-and-sales-orders"></a><span data-ttu-id="f7154-372">Прогнозы движения денежных средств в заказах на покупку и продажу</span><span class="sxs-lookup"><span data-stu-id="f7154-372">Cash flow forecasts on purchase and sales orders</span></span>

<span data-ttu-id="f7154-373">Можно создавать прогнозы движения денежных средств для заказов на покупку и заказов на продажу на основе вида деятельности и профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="f7154-373">You can generate cash flow forecasts for purchase orders and sale orders, based on the kind of activity and posting profile.</span></span> <span data-ttu-id="f7154-374">В строках прогноза движения денежных средств поля **Вид деятельности** и **Профиль разноски** настраивается при создании прогноза.</span><span class="sxs-lookup"><span data-stu-id="f7154-374">On the cash flow forecast lines, the **Kind of activity** and **Posting profile** fields are set when the forecast is generated.</span></span> <span data-ttu-id="f7154-375">Профили учета, указанные в строках заказа, рассматриваются, чтобы определить счета разноски для складских перемещений, а также счета разноски для проводок клиента и поставщика.</span><span class="sxs-lookup"><span data-stu-id="f7154-375">The inventory profiles that are specified on the order lines are considered, to determine the posting accounts of inventory movements, and also the posting accounts of customer and vendor transactions.</span></span> <span data-ttu-id="f7154-376">Для строк заказа, где не указан профиль учета, используется **основной** вид деятельности и профиль разноски, указанный в заголовке заказа.</span><span class="sxs-lookup"><span data-stu-id="f7154-376">For order lines where an inventory profile isn't specified, the **Basic** kind of activity and the posting profile that is specified in the order header are used.</span></span>

### <a name="example"></a><span data-ttu-id="f7154-377">Пример</span><span class="sxs-lookup"><span data-stu-id="f7154-377">Example</span></span>

1. <span data-ttu-id="f7154-378">Создание следующих профилей учета.</span><span class="sxs-lookup"><span data-stu-id="f7154-378">Create the following inventory profiles.</span></span>

      | <span data-ttu-id="f7154-379">**Профиль учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-379">**Inventory profile**</span></span> | <span data-ttu-id="f7154-380">**Вид деятельности**</span><span class="sxs-lookup"><span data-stu-id="f7154-380">**Kind of activity**</span></span> |
      |-----------------------|----------------------|
      | <span data-ttu-id="f7154-381">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-381">GEN</span></span>                   | <span data-ttu-id="f7154-382">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-382">Basic</span></span>                |
      | <span data-ttu-id="f7154-383">MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-383">MAT</span></span>                   | <span data-ttu-id="f7154-384">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-384">Basic</span></span>                |
      | <span data-ttu-id="f7154-385">COM</span><span class="sxs-lookup"><span data-stu-id="f7154-385">COM</span></span>                   | <span data-ttu-id="f7154-386">Комиссионер</span><span class="sxs-lookup"><span data-stu-id="f7154-386">Commissioner</span></span>         |

2. <span data-ttu-id="f7154-387">Создайте заказ на покупку со следующими строками.</span><span class="sxs-lookup"><span data-stu-id="f7154-387">Create a purchase order that has the following lines.</span></span>

      | <span data-ttu-id="f7154-388">**Код номенклатуры**</span><span class="sxs-lookup"><span data-stu-id="f7154-388">**Item number**</span></span> | <span data-ttu-id="f7154-389">**Профиль учета**</span><span class="sxs-lookup"><span data-stu-id="f7154-389">**Inventory profile**</span></span> | <span data-ttu-id="f7154-390">**Количество**</span><span class="sxs-lookup"><span data-stu-id="f7154-390">**Quantity**</span></span> | <span data-ttu-id="f7154-391">**Цена ед. изм.**</span><span class="sxs-lookup"><span data-stu-id="f7154-391">**Unit price**</span></span> | <span data-ttu-id="f7154-392">**Профиль разноски**</span><span class="sxs-lookup"><span data-stu-id="f7154-392">**Posting profile**</span></span> |
      |-----------------|-----------------------|--------------|----------------|---------------------|
      | <span data-ttu-id="f7154-393">Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-393">Item1</span></span>           | <span data-ttu-id="f7154-394">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-394">GEN</span></span>                   | <span data-ttu-id="f7154-395">8</span><span class="sxs-lookup"><span data-stu-id="f7154-395">8</span></span>            | <span data-ttu-id="f7154-396">10</span><span class="sxs-lookup"><span data-stu-id="f7154-396">10</span></span>             | <span data-ttu-id="f7154-397">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-397">GEN</span></span>                 |
      | <span data-ttu-id="f7154-398">Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-398">Item1</span></span>           | <span data-ttu-id="f7154-399">COM</span><span class="sxs-lookup"><span data-stu-id="f7154-399">COM</span></span>                   | <span data-ttu-id="f7154-400">10</span><span class="sxs-lookup"><span data-stu-id="f7154-400">10</span></span>           | <span data-ttu-id="f7154-401">9</span><span class="sxs-lookup"><span data-stu-id="f7154-401">9</span></span>              | <span data-ttu-id="f7154-402">COM</span><span class="sxs-lookup"><span data-stu-id="f7154-402">COM</span></span>                 |
      | <span data-ttu-id="f7154-403">Item1</span><span class="sxs-lookup"><span data-stu-id="f7154-403">Item1</span></span>           | <span data-ttu-id="f7154-404">MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-404">MAT</span></span>                   | <span data-ttu-id="f7154-405">2</span><span class="sxs-lookup"><span data-stu-id="f7154-405">2</span></span>            | <span data-ttu-id="f7154-406">12</span><span class="sxs-lookup"><span data-stu-id="f7154-406">12</span></span>             | <span data-ttu-id="f7154-407">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-407">GEN</span></span>                 |
      | <span data-ttu-id="f7154-408">Item2</span><span class="sxs-lookup"><span data-stu-id="f7154-408">Item2</span></span>           |                       | <span data-ttu-id="f7154-409">5</span><span class="sxs-lookup"><span data-stu-id="f7154-409">5</span></span>            | <span data-ttu-id="f7154-410">20</span><span class="sxs-lookup"><span data-stu-id="f7154-410">20</span></span>             | <span data-ttu-id="f7154-411">Общий</span><span class="sxs-lookup"><span data-stu-id="f7154-411">Общий</span></span>               |

3. <span data-ttu-id="f7154-412">Установите текущую дату на 7 января 2019 и укажите, что в заказе на покупку используется срок платежа, использующий задержку в пять дней.</span><span class="sxs-lookup"><span data-stu-id="f7154-412">Set the current date to January 7, 2019, and specify that the purchase order has payment terms that use a delay of five days.</span></span>
4. <span data-ttu-id="f7154-413">Добавьте накладные расходы в сумме 50 рублей (руб.) к заголовку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="f7154-413">Add miscellaneous charges in the amount of 50 rubles (RUB) to the purchase order header.</span></span> <span data-ttu-id="f7154-414">Для кода накладных расходов разноска по дебету настраивается для номенклатуры, а разноска по кредиту настраивается для поставщика.</span><span class="sxs-lookup"><span data-stu-id="f7154-414">For the miscellaneous charge code, debit posting is set up for the item, and credit posting is set up for the vendor.</span></span>

<span data-ttu-id="f7154-415">Прогноз движения денежных средств для заказа на покупку будет содержать следующие строки.</span><span class="sxs-lookup"><span data-stu-id="f7154-415">The cash flow forecast for the purchase order will contain the following lines.</span></span>

<table>
<tbody>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-416"><strong>Профиль разноски</strong></span><span class="sxs-lookup"><span data-stu-id="f7154-416"><strong>Posting profile</strong></span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-417"><strong>Вид деятельности</strong></span><span class="sxs-lookup"><span data-stu-id="f7154-417"><strong>Kind of activity</strong></span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-418"><strong>Счет учета</strong></span><span class="sxs-lookup"><span data-stu-id="f7154-418"><strong>Ledger account</strong></span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-419"><strong>Дата</strong></span><span class="sxs-lookup"><span data-stu-id="f7154-419"><strong>Date</strong></span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-420"><strong>Разноска</strong></span><span class="sxs-lookup"><span data-stu-id="f7154-420"><strong>Posting</strong></span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-421"><strong>Денежный</strong></span><span class="sxs-lookup"><span data-stu-id="f7154-421"><strong>Currency</strong></span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-422"><strong>Сумма в валюте</strong></span><span class="sxs-lookup"><span data-stu-id="f7154-422"><strong>Amount in currency</strong></span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-423"><strong>Сумма, руб.</strong></span><span class="sxs-lookup"><span data-stu-id="f7154-423"><strong>Amount</strong></span></span></p>
</td>
</tr>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-424">COM</span><span class="sxs-lookup"><span data-stu-id="f7154-424">COM</span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-425">Комиссионер</span><span class="sxs-lookup"><span data-stu-id="f7154-425">Commissioner</span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-426">41.COM</span><span class="sxs-lookup"><span data-stu-id="f7154-426">41.COM</span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-427">01.07.2019</span><span class="sxs-lookup"><span data-stu-id="f7154-427">01.07.2019</span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-428">Покупка, поступление</span><span class="sxs-lookup"><span data-stu-id="f7154-428">Purchase, receipt</span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-429">руб.</span><span class="sxs-lookup"><span data-stu-id="f7154-429">RUB</span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-430">90.00</span><span class="sxs-lookup"><span data-stu-id="f7154-430">90.00</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-431">90.00</span><span class="sxs-lookup"><span data-stu-id="f7154-431">90.00</span></span></p>
</td>
</tr>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-432">COM</span><span class="sxs-lookup"><span data-stu-id="f7154-432">COM</span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-433">Комиссионер</span><span class="sxs-lookup"><span data-stu-id="f7154-433">Commissioner</span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-434">51.TEST</span><span class="sxs-lookup"><span data-stu-id="f7154-434">51.TEST</span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-435">06.07.2019</span><span class="sxs-lookup"><span data-stu-id="f7154-435">06.07.2019</span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-436">Сальдо по поставщику</span><span class="sxs-lookup"><span data-stu-id="f7154-436">Vendor balance</span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-437">руб.</span><span class="sxs-lookup"><span data-stu-id="f7154-437">RUB</span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-438">-140,00</span><span class="sxs-lookup"><span data-stu-id="f7154-438">-140.00</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-439">-140,00</span><span class="sxs-lookup"><span data-stu-id="f7154-439">-140.00</span></span></p>
</td>
</tr>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-440">COM</span><span class="sxs-lookup"><span data-stu-id="f7154-440">COM</span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-441">Комиссионер</span><span class="sxs-lookup"><span data-stu-id="f7154-441">Commissioner</span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-442">60.1.COM</span><span class="sxs-lookup"><span data-stu-id="f7154-442">60.1.COM</span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-443">01.07.2019</span><span class="sxs-lookup"><span data-stu-id="f7154-443">01.07.2019</span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-444">Сальдо по поставщику</span><span class="sxs-lookup"><span data-stu-id="f7154-444">Vendor balance</span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-445">руб.</span><span class="sxs-lookup"><span data-stu-id="f7154-445">RUB</span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-446">-140,00</span><span class="sxs-lookup"><span data-stu-id="f7154-446">-140.00</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-447">-140,00</span><span class="sxs-lookup"><span data-stu-id="f7154-447">-140.00</span></span></p>
</td>
</tr>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-448">COM</span><span class="sxs-lookup"><span data-stu-id="f7154-448">COM</span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-449">Комиссионер</span><span class="sxs-lookup"><span data-stu-id="f7154-449">Commissioner</span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-450">60.1.COM</span><span class="sxs-lookup"><span data-stu-id="f7154-450">60.1.COM</span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-451">06.07.2019</span><span class="sxs-lookup"><span data-stu-id="f7154-451">06.07.2019</span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-452">Сальдо по поставщику</span><span class="sxs-lookup"><span data-stu-id="f7154-452">Vendor balance</span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-453">руб.</span><span class="sxs-lookup"><span data-stu-id="f7154-453">RUB</span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-454">140.00</span><span class="sxs-lookup"><span data-stu-id="f7154-454">140.00</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-455">140.00</span><span class="sxs-lookup"><span data-stu-id="f7154-455">140.00</span></span></p>
</td>
</tr>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-456">MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-456">MAT</span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-457">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-457">Basic</span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-458">41.MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-458">41.MAT</span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-459">01.07.2019</span><span class="sxs-lookup"><span data-stu-id="f7154-459">01.07.2019</span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-460">Покупка, поступление</span><span class="sxs-lookup"><span data-stu-id="f7154-460">Purchase, receipt</span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-461">руб.</span><span class="sxs-lookup"><span data-stu-id="f7154-461">RUB</span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-462">24.00</span><span class="sxs-lookup"><span data-stu-id="f7154-462">24.00</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-463">24.00</span><span class="sxs-lookup"><span data-stu-id="f7154-463">24.00</span></span></p>
</td>
</tr>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-464">MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-464">MAT</span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-465">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-465">Basic</span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-466">51.TEST</span><span class="sxs-lookup"><span data-stu-id="f7154-466">51.TEST</span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-467">06.07.2019</span><span class="sxs-lookup"><span data-stu-id="f7154-467">06.07.2019</span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-468">Сальдо по поставщику</span><span class="sxs-lookup"><span data-stu-id="f7154-468">Vendor balance</span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-469">руб.</span><span class="sxs-lookup"><span data-stu-id="f7154-469">RUB</span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-470">-74,00</span><span class="sxs-lookup"><span data-stu-id="f7154-470">-74.00</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-471">-74,00</span><span class="sxs-lookup"><span data-stu-id="f7154-471">-74.00</span></span></p>
</td>
</tr>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-472">MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-472">MAT</span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-473">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-473">Basic</span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-474">60.1.MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-474">60.1.MAT</span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-475">01.07.2019</span><span class="sxs-lookup"><span data-stu-id="f7154-475">01.07.2019</span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-476">Сальдо по поставщику</span><span class="sxs-lookup"><span data-stu-id="f7154-476">Vendor balance</span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-477">руб.</span><span class="sxs-lookup"><span data-stu-id="f7154-477">RUB</span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-478">-74,00</span><span class="sxs-lookup"><span data-stu-id="f7154-478">-74.00</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-479">-74,00</span><span class="sxs-lookup"><span data-stu-id="f7154-479">-74.00</span></span></p>
</td>
</tr>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-480">MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-480">MAT</span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-481">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-481">Basic</span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-482">60.1.MAT</span><span class="sxs-lookup"><span data-stu-id="f7154-482">60.1.MAT</span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-483">06.07.2019</span><span class="sxs-lookup"><span data-stu-id="f7154-483">06.07.2019</span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-484">Сальдо по поставщику</span><span class="sxs-lookup"><span data-stu-id="f7154-484">Vendor balance</span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-485">руб.</span><span class="sxs-lookup"><span data-stu-id="f7154-485">RUB</span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-486">74.00</span><span class="sxs-lookup"><span data-stu-id="f7154-486">74.00</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-487">74.00</span><span class="sxs-lookup"><span data-stu-id="f7154-487">74.00</span></span></p>
</td>
</tr>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-488">Общий</span><span class="sxs-lookup"><span data-stu-id="f7154-488">Общий</span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-489">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-489">Basic</span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-490">10.100</span><span class="sxs-lookup"><span data-stu-id="f7154-490">10.100</span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-491">01.07.2019</span><span class="sxs-lookup"><span data-stu-id="f7154-491">01.07.2019</span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-492">Покупка, поступление</span><span class="sxs-lookup"><span data-stu-id="f7154-492">Purchase, receipt</span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-493">руб.</span><span class="sxs-lookup"><span data-stu-id="f7154-493">RUB</span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-494">100.00</span><span class="sxs-lookup"><span data-stu-id="f7154-494">100.00</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-495">100.00</span><span class="sxs-lookup"><span data-stu-id="f7154-495">100.00</span></span></p>
</td>
</tr>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-496">Общий</span><span class="sxs-lookup"><span data-stu-id="f7154-496">Общий</span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-497">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-497">Basic</span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-498">51.101</span><span class="sxs-lookup"><span data-stu-id="f7154-498">51.101</span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-499">06.07.2019</span><span class="sxs-lookup"><span data-stu-id="f7154-499">06.07.2019</span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-500">Сальдо по поставщику</span><span class="sxs-lookup"><span data-stu-id="f7154-500">Vendor balance</span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-501">руб.</span><span class="sxs-lookup"><span data-stu-id="f7154-501">RUB</span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-502">-150,00</span><span class="sxs-lookup"><span data-stu-id="f7154-502">-150.00</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-503">-150,00</span><span class="sxs-lookup"><span data-stu-id="f7154-503">-150.00</span></span></p>
</td>
</tr>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-504">Общий</span><span class="sxs-lookup"><span data-stu-id="f7154-504">Общий</span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-505">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-505">Basic</span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-506">60.030</span><span class="sxs-lookup"><span data-stu-id="f7154-506">60.030</span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-507">01.07.2019</span><span class="sxs-lookup"><span data-stu-id="f7154-507">01.07.2019</span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-508">Сальдо по поставщику</span><span class="sxs-lookup"><span data-stu-id="f7154-508">Vendor balance</span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-509">руб.</span><span class="sxs-lookup"><span data-stu-id="f7154-509">RUB</span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-510">-150,00</span><span class="sxs-lookup"><span data-stu-id="f7154-510">-150.00</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-511">-150,00</span><span class="sxs-lookup"><span data-stu-id="f7154-511">-150.00</span></span></p>
</td>
</tr>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-512">Общий</span><span class="sxs-lookup"><span data-stu-id="f7154-512">Общий</span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-513">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-513">Basic</span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-514">60.030</span><span class="sxs-lookup"><span data-stu-id="f7154-514">60.030</span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-515">06.07.2019</span><span class="sxs-lookup"><span data-stu-id="f7154-515">06.07.2019</span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-516">Сальдо по поставщику</span><span class="sxs-lookup"><span data-stu-id="f7154-516">Vendor balance</span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-517">руб.</span><span class="sxs-lookup"><span data-stu-id="f7154-517">RUB</span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-518">150.00</span><span class="sxs-lookup"><span data-stu-id="f7154-518">150.00</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-519">150.00</span><span class="sxs-lookup"><span data-stu-id="f7154-519">150.00</span></span></p>
</td>
</tr>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-520">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-520">GEN</span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-521">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-521">Basic</span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-522">41.GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-522">41.GEN</span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-523">01.07.2019</span><span class="sxs-lookup"><span data-stu-id="f7154-523">01.07.2019</span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-524">Покупка, поступление</span><span class="sxs-lookup"><span data-stu-id="f7154-524">Purchase, receipt</span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-525">руб.</span><span class="sxs-lookup"><span data-stu-id="f7154-525">RUB</span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-526">80.00</span><span class="sxs-lookup"><span data-stu-id="f7154-526">80.00</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-527">80.00</span><span class="sxs-lookup"><span data-stu-id="f7154-527">80.00</span></span></p>
</td>
</tr>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-528">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-528">GEN</span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-529">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-529">Basic</span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-530">51.TEST</span><span class="sxs-lookup"><span data-stu-id="f7154-530">51.TEST</span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-531">06.07.2019</span><span class="sxs-lookup"><span data-stu-id="f7154-531">06.07.2019</span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-532">Сальдо по поставщику</span><span class="sxs-lookup"><span data-stu-id="f7154-532">Vendor balance</span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-533">руб.</span><span class="sxs-lookup"><span data-stu-id="f7154-533">RUB</span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-534">-130,00</span><span class="sxs-lookup"><span data-stu-id="f7154-534">-130.00</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-535">-130,00</span><span class="sxs-lookup"><span data-stu-id="f7154-535">-130.00</span></span></p>
</td>
</tr>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-536">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-536">GEN</span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-537">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-537">Basic</span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-538">60.1.GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-538">60.1.GEN</span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-539">01.07.2019</span><span class="sxs-lookup"><span data-stu-id="f7154-539">01.07.2019</span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-540">Сальдо по поставщику</span><span class="sxs-lookup"><span data-stu-id="f7154-540">Vendor balance</span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-541">руб.</span><span class="sxs-lookup"><span data-stu-id="f7154-541">RUB</span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-542">-130,00</span><span class="sxs-lookup"><span data-stu-id="f7154-542">-130.00</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-543">-130,00</span><span class="sxs-lookup"><span data-stu-id="f7154-543">-130.00</span></span></p>
</td>
</tr>
<tr>
<td width="79">
<p><span data-ttu-id="f7154-544">GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-544">GEN</span></span></p>
</td>
<td width="125">
<p><span data-ttu-id="f7154-545">Основное</span><span class="sxs-lookup"><span data-stu-id="f7154-545">Basic</span></span></p>
</td>
<td width="96">
<p><span data-ttu-id="f7154-546">60.1.GEN</span><span class="sxs-lookup"><span data-stu-id="f7154-546">60.1.GEN</span></span></p>
</td>
<td width="91">
<p><span data-ttu-id="f7154-547">06.07.2019</span><span class="sxs-lookup"><span data-stu-id="f7154-547">06.07.2019</span></span></p>
</td>
<td width="92">
<p><span data-ttu-id="f7154-548">Сальдо по поставщику</span><span class="sxs-lookup"><span data-stu-id="f7154-548">Vendor balance</span></span></p>
</td>
<td width="76">
<p><span data-ttu-id="f7154-549">руб.</span><span class="sxs-lookup"><span data-stu-id="f7154-549">RUB</span></span></p>
</td>
<td width="94">
<p><span data-ttu-id="f7154-550">130.00</span><span class="sxs-lookup"><span data-stu-id="f7154-550">130.00</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="f7154-551">130.00</span><span class="sxs-lookup"><span data-stu-id="f7154-551">130.00</span></span></p>
</td>
</tr>
</tbody>
</table>

<span data-ttu-id="f7154-552">Накладные расходы для заголовка заказа на покупку или заказа на продажу повторяются в прогнозе движения денежных средств для всех комбинаций вида деятельности и профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="f7154-552">The miscellaneous charges for the purchase order or sales order header are repeated in the cash flow forecast for all combinations of a kind of activity and a posting profile.</span></span>

<span data-ttu-id="f7154-553">Более подробную информацию см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="f7154-553">Find more details in the following topics:</span></span>

-  [<span data-ttu-id="f7154-554">Обзор профиля учета</span><span class="sxs-lookup"><span data-stu-id="f7154-554">Inventory profile overview</span></span>](rus-inventory-profile-overview.md)
-  [<span data-ttu-id="f7154-555">Настройка профиля учета</span><span class="sxs-lookup"><span data-stu-id="f7154-555">Set up an inventory profile</span></span>](rus-set-up-inventory-profile.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]