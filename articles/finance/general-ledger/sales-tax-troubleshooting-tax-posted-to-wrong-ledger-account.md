---
title: Налог разносится на некорректный счет ГК в ваучере
description: В этом разделе содержатся сведения об устранении неполадок, которые могут помочь при разноске налога на неправильный счет ГК в ваучере.
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3d197046bd547757f32712a50949b41897f6fedf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020099"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a><span data-ttu-id="9da84-103">Налог разносится на некорректный счет ГК в ваучере</span><span class="sxs-lookup"><span data-stu-id="9da84-103">Tax is posted to the wrong ledger account in the voucher</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9da84-104">Во время разноски налог может быть разнесен на неправильный счет ГК в ваучере.</span><span class="sxs-lookup"><span data-stu-id="9da84-104">During posting, tax might be posted to the wrong ledger account in the voucher.</span></span> <span data-ttu-id="9da84-105">Для решения проблемы выполните действия, указанные в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="9da84-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span> <span data-ttu-id="9da84-106">В примерах этой темы в качестве делового документа используется заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="9da84-106">The examples in this topic use a sales order as the business document.</span></span>

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a><span data-ttu-id="9da84-107">Поиск налогового кода неправильно разнесенной налоговой проводки</span><span class="sxs-lookup"><span data-stu-id="9da84-107">Find the tax code of the incorrectly posted tax transaction</span></span>

1. <span data-ttu-id="9da84-108">На странице **Проводки по ваучеру** выберите проводку, с которой необходимо работать, а затем выберите **Разнесенный налог**.</span><span class="sxs-lookup"><span data-stu-id="9da84-108">On the **Voucher transactions** page, select the transaction that you want to work with, and then select **Posted sales tax**.</span></span>

    <span data-ttu-id="9da84-109">[![Кнопка разнесенного налога на странице проводки по ваучеру](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="9da84-109">[![Posted sales tax button on the Voucher transactions page](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span></span>

2. <span data-ttu-id="9da84-110">Проверьте значение в поле **Код налога**.</span><span class="sxs-lookup"><span data-stu-id="9da84-110">Review the value in the **Sales tax code** field.</span></span> <span data-ttu-id="9da84-111">В этом примере устанавливается значение **НДС 19**.</span><span class="sxs-lookup"><span data-stu-id="9da84-111">In this example, it's **VAT 19**.</span></span>

    <span data-ttu-id="9da84-112">[![Поле налогового кода на странице разнесенного налога](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="9da84-112">[![Sales tax code field on the Posted sales tax page](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span></span>

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a><span data-ttu-id="9da84-113">Проверка группы разноски главной книги по налоговому коду</span><span class="sxs-lookup"><span data-stu-id="9da84-113">Check the ledger posting group of the tax code</span></span>

1. <span data-ttu-id="9da84-114">Перейдите в раздел **Налог** \> **Косвенные налоги** \> **Налог** \> **Налоговые коды**.</span><span class="sxs-lookup"><span data-stu-id="9da84-114">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="9da84-115">Найдите и выберите налоговый код, а затем проверьте значение в поле **Группа разноски главной книги**.</span><span class="sxs-lookup"><span data-stu-id="9da84-115">Find and select the tax code, and then review the value in the **Ledger posting group** field.</span></span> <span data-ttu-id="9da84-116">В этом примере устанавливается значение **НДС**.</span><span class="sxs-lookup"><span data-stu-id="9da84-116">In this example, it's **VAT**.</span></span>

    <span data-ttu-id="9da84-117">[![Поле группы разноски ГК на странице налоговых кодов](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="9da84-117">[![Ledger posting group field on the Sales tax codes page](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span></span>

3. <span data-ttu-id="9da84-118">Значение в поле **Группа разноски ГК** — это ссылка.</span><span class="sxs-lookup"><span data-stu-id="9da84-118">The value in the **Ledger posting group** field is a link.</span></span> <span data-ttu-id="9da84-119">Чтобы просмотреть сведения о конфигурации группы, выберите ссылку.</span><span class="sxs-lookup"><span data-stu-id="9da84-119">To view the details of the group's configuration, select the link.</span></span> <span data-ttu-id="9da84-120">Или же выберите и удерживайте (или щелкните правой кнопкой мыши) поле, а затем выберите **Просмотреть сведения**.</span><span class="sxs-lookup"><span data-stu-id="9da84-120">Alternatively, select and hold (or right-click) in the field, and then select **View details**.</span></span>

    <span data-ttu-id="9da84-121">[![Команда просмотра сведений](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="9da84-121">[![View details command](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span></span>

4. <span data-ttu-id="9da84-122">В поле **Подлежащий оплате налог** проверьте правильность номера счета в соответствии с типом проводки.</span><span class="sxs-lookup"><span data-stu-id="9da84-122">In the **Sales tax payable** field, verify that the account number is correct, according to the transaction type.</span></span> <span data-ttu-id="9da84-123">Если неправильный, выберите правильный счет для разноски.</span><span class="sxs-lookup"><span data-stu-id="9da84-123">If it isn't, select the correct account to post to.</span></span> <span data-ttu-id="9da84-124">В этом примере налог заказа на продажу должен быть разнесен на счет уплачиваемого налога 222200.</span><span class="sxs-lookup"><span data-stu-id="9da84-124">In this example, the sales tax of the sales order should be posted to sales tax payable account 222200.</span></span>

    <span data-ttu-id="9da84-125">[![Поле "Исходящий налог" на странице "Группы разноски ГК"](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="9da84-125">[![Sales tax payable field on the Ledger posting groups page](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span></span>

    <span data-ttu-id="9da84-126">В следующей таблице приводятся сведения о каждом поле на странице **Группы разноски главной книги**.</span><span class="sxs-lookup"><span data-stu-id="9da84-126">The following table provides information about each field on the **Ledger posting groups** page.</span></span>

    | <span data-ttu-id="9da84-127">Поле</span><span class="sxs-lookup"><span data-stu-id="9da84-127">Field</span></span>                  | <span data-ttu-id="9da84-128">описание</span><span class="sxs-lookup"><span data-stu-id="9da84-128">Description</span></span> |
    |------------------------|-------------|
    | <span data-ttu-id="9da84-129">Исходящий налог</span><span class="sxs-lookup"><span data-stu-id="9da84-129">Sales tax payable</span></span>      | <span data-ttu-id="9da84-130">Счет главной книги для исходящих налогов, выплачиваемых налоговым органам.</span><span class="sxs-lookup"><span data-stu-id="9da84-130">The main account for outgoing sales taxes that are payable to the tax authority.</span></span> |
    | <span data-ttu-id="9da84-131">Входящий налог</span><span class="sxs-lookup"><span data-stu-id="9da84-131">Sales tax receivable</span></span>   | <span data-ttu-id="9da84-132">Счет главной книги для входящих налогов, получаемых от налоговых органов.</span><span class="sxs-lookup"><span data-stu-id="9da84-132">The main account for incoming taxes that are received from the tax authority.</span></span> |
    | <span data-ttu-id="9da84-133">Расходы по налогу за пользование</span><span class="sxs-lookup"><span data-stu-id="9da84-133">Use tax expense</span></span>        | <span data-ttu-id="9da84-134">Счет ГК, который используется для разноски начисленных налогов на пользование, которые поставщики не заявляют или не сообщают в налоговый орган как часть Европейского союза (ЕС), налог с удержанием с покупателя, налоги на товары и услуги (GST)/HST-налог.</span><span class="sxs-lookup"><span data-stu-id="9da84-134">The main account that is used to post deductible use taxes that vendors don't claim or report to the tax authority as part of European Union (EU) reverse charge Goods and Services Tax (GST)/Harmonized Sales Tax (HST).</span></span> <span data-ttu-id="9da84-135">**Налог за пользование** должен быть выбран для код налога в налоговой группе, используемой в проводке.</span><span class="sxs-lookup"><span data-stu-id="9da84-135">**Use tax** must be selected for the sales tax code in the sales tax group that is used in the transaction.</span></span> <span data-ttu-id="9da84-136">Это поле не будет доступно, если параметр **Применить правила налогообложения** выбран на странице **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="9da84-136">This field isn't available if **Apply sales tax taxation rules** is selected on the **General ledger parameters** page.</span></span> |
    | <span data-ttu-id="9da84-137">Налог за пользование, подлежащий уплате</span><span class="sxs-lookup"><span data-stu-id="9da84-137">Use tax payable</span></span>        | <span data-ttu-id="9da84-138">Счет ГК, используемый для разноски входящих налогов на пользование, подлежащих оплате в налоговые органы.</span><span class="sxs-lookup"><span data-stu-id="9da84-138">The main account that is used to post incoming use taxes that are payable to tax authorities.</span></span> |
    | <span data-ttu-id="9da84-139">Сопоставление счета</span><span class="sxs-lookup"><span data-stu-id="9da84-139">Settlement account</span></span>     | <span data-ttu-id="9da84-140">Счет ГК, используемый для разноски сальдо счетов ГК, указанных в полях **Налог за пользование** и **Входящий налог**.</span><span class="sxs-lookup"><span data-stu-id="9da84-140">The main account that is used to post the net balance of the ledger accounts that are specified in the **Use tax payable** and **Sales tax receivable** fields.</span></span> |
    | <span data-ttu-id="9da84-141">Скидка по оплате по поставщику</span><span class="sxs-lookup"><span data-stu-id="9da84-141">Vendor cash discount</span></span>   | <span data-ttu-id="9da84-142">Счет ГК, используемый для разноски скидки по оплате для налоговых кодов, связанных с данной группой разноски ГК.</span><span class="sxs-lookup"><span data-stu-id="9da84-142">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |
    | <span data-ttu-id="9da84-143">Скидка при оплате наличными по клиенту</span><span class="sxs-lookup"><span data-stu-id="9da84-143">Customer case discount</span></span> | <span data-ttu-id="9da84-144">Счет ГК, используемый для разноски скидки по оплате для налоговых кодов, связанных с данной группой разноски ГК.</span><span class="sxs-lookup"><span data-stu-id="9da84-144">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |

    <span data-ttu-id="9da84-145">Дополнительные сведения см. в разделе [Настройка групп разноски ГК для налога](tasks/set-up-ledger-posting-groups-sales-tax.md)</span><span class="sxs-lookup"><span data-stu-id="9da84-145">For more information, see, [Set up Ledger posting groups for sales tax](tasks/set-up-ledger-posting-groups-sales-tax.md)</span></span>

## <a name="debug-in-code-to-check-ledger-dimensions"></a><span data-ttu-id="9da84-146">Отладка в коде для проверки аналитик ГК</span><span class="sxs-lookup"><span data-stu-id="9da84-146">Debug in code to check ledger dimensions</span></span>

<span data-ttu-id="9da84-147">В коде счет разноски определяется аналитикой главной книги.</span><span class="sxs-lookup"><span data-stu-id="9da84-147">In the code, the posting account is determined by the ledger dimension.</span></span> <span data-ttu-id="9da84-148">Аналитика ГК сохраняет код записи счета в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9da84-148">The ledger dimension saves the record ID of an account in the database.</span></span>

1. <span data-ttu-id="9da84-149">Для заказа на продажу добавьте точку останова в методах **Tax::saveAndPost()** и **Tax::post()**.</span><span class="sxs-lookup"><span data-stu-id="9da84-149">For a sales order, add a breakpoint at the **Tax::saveAndPost()** and **Tax::post()** methods.</span></span> <span data-ttu-id="9da84-150">Обратите внимание на значение **\_ledgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="9da84-150">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="9da84-151">[![Пример кода заказа на продажу с точкой останова](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="9da84-151">[![Sales order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span></span>

    <span data-ttu-id="9da84-152">Для заказа на покупку добавьте точку останова в методах **TaxPost::saveAndPost()** и **TaxPost::postToTaxTrans()**.</span><span class="sxs-lookup"><span data-stu-id="9da84-152">For a purchase order, add a breakpoint at the **TaxPost::saveAndPost()** and **TaxPost::postToTaxTrans()** methods.</span></span> <span data-ttu-id="9da84-153">Обратите внимание на значение **\_ledgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="9da84-153">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="9da84-154">[![Пример кода заказа на покупку с точкой останова](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span><span class="sxs-lookup"><span data-stu-id="9da84-154">[![Purchase order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span></span>

2. <span data-ttu-id="9da84-155">Выполните следующий запрос SQL, чтобы найти отображаемое значение счета в базе данных на основе кода записи, сохраненного аналитикой главной книги.</span><span class="sxs-lookup"><span data-stu-id="9da84-155">Run the following SQL query to find the display value of the account in the database, based on the record ID that is saved by the ledger dimension.</span></span>

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    <span data-ttu-id="9da84-156">[![Отображаемое значение кода записи](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span><span class="sxs-lookup"><span data-stu-id="9da84-156">[![Display value of the record ID](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span></span>

3. <span data-ttu-id="9da84-157">Проверьте стек вызовов, чтобы найти место, в котором назначено значение **_ledgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="9da84-157">Examine the callstack to find where the **_ledgerDimension** value is assigned.</span></span> <span data-ttu-id="9da84-158">Обычно значение берется из **TmpTaxWorkTrans**.</span><span class="sxs-lookup"><span data-stu-id="9da84-158">Usually, the value is from **TmpTaxWorkTrans**.</span></span> <span data-ttu-id="9da84-159">В этом случае необходимо добавить точку останова в **TmpTaxWorkTrans::insert()** и **TmpTaxWorkTrans::update()**, чтобы найти, где было назначено значение.</span><span class="sxs-lookup"><span data-stu-id="9da84-159">In this case, you should add a breakpoint at **TmpTaxWorkTrans::insert()** and **TmpTaxWorkTrans::update()** to find where the value assigned.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="9da84-160">Определение существования настройки</span><span class="sxs-lookup"><span data-stu-id="9da84-160">Determine whether customization exists</span></span>

<span data-ttu-id="9da84-161">Если вы выполнили шаги в предыдущих разделах, но не смогли решить проблему, определите, существует ли настройка.</span><span class="sxs-lookup"><span data-stu-id="9da84-161">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="9da84-162">Если настройки не существует, создайте запрос в службу поддержки Майкрософт для получения дополнительной поддержки.</span><span class="sxs-lookup"><span data-stu-id="9da84-162">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
