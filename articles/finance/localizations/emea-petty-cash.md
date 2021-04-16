---
title: Мелкие наличные деньги для Восточной Европы и России
description: В этом разделе содержатся сведения о функциях мелких наличных деньги, которая позволяет пользователям в Эстонии, Литве, Чехии, Венгрии, Латвии, Польше и России отражать кассовые операции в системе.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCashBalance, RCashCountStatementForm, RCashPosting, RCashRemainLimit, RCashReportJour_PL, RCashTable, RCashTableBalance, RCashTableCredLimit, RCashTableLastRevaluation, RCashTableTransactions, RCashTrans
audience: Application User
ms.reviewer: kfend
ms.custom: 268504
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: a721d5602fa7b569b56e85e1bd66a8e543a39a41
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832704"
---
# <a name="petty-cash-for-eastern-europe-and-russia"></a><span data-ttu-id="ddff3-103">Мелкие наличные деньги для Восточной Европы и России</span><span class="sxs-lookup"><span data-stu-id="ddff3-103">Petty cash for Eastern Europe and Russia</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ddff3-104">В этом разделе содержатся сведения о функциях мелких наличных деньги, которая позволяет пользователям в Эстонии, Литве, Чехии, Венгрии, Латвии, Польше и России отражать кассовые операции в системе.</span><span class="sxs-lookup"><span data-stu-id="ddff3-104">This topic provides information about the petty cash functionality that lets users in Estonia, Lithuania, Czech Republic, Hungary, Latvia, Poland, and Russia reflect cash operations in the system.</span></span>

<span data-ttu-id="ddff3-105">Функцию мелких наличных денег можно использовать для автоматизации операций для приходов и расходов наличных, создания первичных документов и печати связанных отчетов.</span><span class="sxs-lookup"><span data-stu-id="ddff3-105">You can use the petty cash functionality to automate operations for receipts and expenditures of cash, the creation of primary documents, and the printing of related reports.</span></span> <span data-ttu-id="ddff3-106">Функция мелких наличных денег позволяет выполнять следующие операции:</span><span class="sxs-lookup"><span data-stu-id="ddff3-106">The petty cash functionality lets you perform the following operations:</span></span>

-   <span data-ttu-id="ddff3-107">Учет прихода и расхода доступных наличных средств.</span><span class="sxs-lookup"><span data-stu-id="ddff3-107">Account the receipt and expenditure of available cash assets.</span></span>
-   <span data-ttu-id="ddff3-108">Создание типовых наличных форм: приходные кассовые ордеры, расходные кассовые ордеры и журнал регистрации кассовых ордеров.</span><span class="sxs-lookup"><span data-stu-id="ddff3-108">Generate typical cash forms: Cash reimbursement slips, Cash disbursement slips, and a Journal of registration for cash slips.</span></span>
-   <span data-ttu-id="ddff3-109">Управление максимальной суммой наличных денег, которая допускается для операций с клиентами, поставщиками и т. д.</span><span class="sxs-lookup"><span data-stu-id="ddff3-109">Control the maximum cash amount that is allowed for operations with customers, vendors, and so on.</span></span>
-   <span data-ttu-id="ddff3-110">Отражение кассовых операций в различных валютах в системе.</span><span class="sxs-lookup"><span data-stu-id="ddff3-110">Reflect cash operations in various currencies in the system.</span></span>
-   <span data-ttu-id="ddff3-111">Преобразование сумм операций с наличными средствами в иностранной валюте в валюту по умолчанию, чтобы обеспечить отчетность по учету.</span><span class="sxs-lookup"><span data-stu-id="ddff3-111">Convert the amounts of cash operations in foreign currency to the default currency to provide accounting reporting.</span></span>
-   <span data-ttu-id="ddff3-112">Создание отчета **Кассовая книга** и отчета кассира.</span><span class="sxs-lookup"><span data-stu-id="ddff3-112">Generate a **Cash book** report and a cashier’s report.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ddff3-113">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="ddff3-113">Prerequisites</span></span>
<span data-ttu-id="ddff3-114">Чтобы вы могли использовать функцию мелких наличных денег, необходимо выполнить следующие обязательные условия:</span><span class="sxs-lookup"><span data-stu-id="ddff3-114">Before you can use the petty cash functionality, you must complete the following prerequisites:</span></span>

-   <span data-ttu-id="ddff3-115">Настройка кассовых счетов.</span><span class="sxs-lookup"><span data-stu-id="ddff3-115">Set up cash accounts.</span></span>
-   <span data-ttu-id="ddff3-116">Настройка профилей разноски кассы.</span><span class="sxs-lookup"><span data-stu-id="ddff3-116">Set up cash posting profiles.</span></span>
-   <span data-ttu-id="ddff3-117">Настройка номерных серий для нумерации кассовых документов.</span><span class="sxs-lookup"><span data-stu-id="ddff3-117">Set up number sequences for cash document numbering.</span></span>
-   <span data-ttu-id="ddff3-118">Настройка значений по умолчанию для параметров управления банком и кассовыми операциями.</span><span class="sxs-lookup"><span data-stu-id="ddff3-118">Set up default values for Cash and bank management parameters.</span></span>
-   <span data-ttu-id="ddff3-119">Настройка имен кассовых журналов в главной книге.</span><span class="sxs-lookup"><span data-stu-id="ddff3-119">Set up cash journal names in General ledger.</span></span>

### <a name="set-up-cash-accounts"></a><span data-ttu-id="ddff3-120">Настройка кассовых счетов</span><span class="sxs-lookup"><span data-stu-id="ddff3-120">Set up cash accounts</span></span>

<span data-ttu-id="ddff3-121">Чтобы настроить кассу, откройте **Управление банком и кассовыми операциями** &gt; **Банковские счета** &gt; **Кассы** и введите следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="ddff3-121">To set up a Cash, open **Cash and bank management** &gt; **Bank accounts** &gt; **Cash accounts**, and enter the following information.</span></span>

| <span data-ttu-id="ddff3-122">Поле</span><span class="sxs-lookup"><span data-stu-id="ddff3-122">Field</span></span>                 | <span data-ttu-id="ddff3-123">описание</span><span class="sxs-lookup"><span data-stu-id="ddff3-123">Description</span></span>                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddff3-124">Наличный расчет</span><span class="sxs-lookup"><span data-stu-id="ddff3-124">Cash</span></span>                  | <span data-ttu-id="ddff3-125">Введите код для идентификации кассового счета (кассы).</span><span class="sxs-lookup"><span data-stu-id="ddff3-125">Enter a code to identify the cash account (cash).</span></span>                                                                    |
| <span data-ttu-id="ddff3-126">Наименование</span><span class="sxs-lookup"><span data-stu-id="ddff3-126">Name</span></span>                  | <span data-ttu-id="ddff3-127">Введите описание кассового счета.</span><span class="sxs-lookup"><span data-stu-id="ddff3-127">Enter a description of the cash account.</span></span>                                                                             |
| <span data-ttu-id="ddff3-128">Валютное</span><span class="sxs-lookup"><span data-stu-id="ddff3-128">Currency</span></span>              | <span data-ttu-id="ddff3-129">Выберите валюту по умолчанию для кассовых проводок.</span><span class="sxs-lookup"><span data-stu-id="ddff3-129">Select the default currency code for cash transactions.</span></span>                                                              |
| <span data-ttu-id="ddff3-130">Группа номерных серий</span><span class="sxs-lookup"><span data-stu-id="ddff3-130">Number sequence group</span></span> | <span data-ttu-id="ddff3-131">Если нумерация кассовых документов должна отличаться от нумерации, которая указана в параметрах, введите код.</span><span class="sxs-lookup"><span data-stu-id="ddff3-131">If the numbering of cash documents must differ from the numbering that is specified in the parameters, enter a code.</span></span> |
| <span data-ttu-id="ddff3-132">Разные валюты</span><span class="sxs-lookup"><span data-stu-id="ddff3-132">More currencies</span></span>       | <span data-ttu-id="ddff3-133">Установите этот флажок, чтобы разрешить разноску валюты, отличной от валюта учета.</span><span class="sxs-lookup"><span data-stu-id="ddff3-133">Select this check box to allow currencies that differ from the accounting currency to be posted.</span></span>                     |
| <span data-ttu-id="ddff3-134">Отрицательная касса</span><span class="sxs-lookup"><span data-stu-id="ddff3-134">Negative cash</span></span>         | <span data-ttu-id="ddff3-135">Установите этот флажок, чтобы разрешить отрицательные денежные сальдо в любой валюте.</span><span class="sxs-lookup"><span data-stu-id="ddff3-135">Select this check box to allow negative cash balances in any currency.</span></span>                                               |

<span data-ttu-id="ddff3-136">Чтобы настроить правила контроля сальдо денежных средств для кассового счета, выберите кассовый счет, затем на панели действий на вкладке **Кассовый счет** в группе **Лимит остатка** щелкните **Лимит остатка**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-136">To set up cash balance control rules for a cash account, select the cash account, and then, on the Action Pane, on the **Cash account** tab, in the **Balance limit** group, click **Balance limit**.</span></span> <span data-ttu-id="ddff3-137">Введите следующую информацию.</span><span class="sxs-lookup"><span data-stu-id="ddff3-137">Enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ddff3-138">Поле</span><span class="sxs-lookup"><span data-stu-id="ddff3-138">Field</span></span></th>
<th><span data-ttu-id="ddff3-139">описание</span><span class="sxs-lookup"><span data-stu-id="ddff3-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ddff3-140">Тип валюты</span><span class="sxs-lookup"><span data-stu-id="ddff3-140">Currency type</span></span></td>
<td><span data-ttu-id="ddff3-141">Выберите тип валюты:</span><span class="sxs-lookup"><span data-stu-id="ddff3-141">Select the type of currency:</span></span>
<ul>
<li><span data-ttu-id="ddff3-142"><strong>Валюта учета</strong> — используется основной код валюты компании.</span><span class="sxs-lookup"><span data-stu-id="ddff3-142"><strong>Accounting currency</strong> – Use the basic company currency code.</span></span></li>
<li><span data-ttu-id="ddff3-143"><strong>Указанная валюта</strong> — используется код валюты, отличный от основного кода валюты компании.</span><span class="sxs-lookup"><span data-stu-id="ddff3-143"><strong>Indicated currency</strong> – Use a currency code that differs from the basic company currency code.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-144">Валютное</span><span class="sxs-lookup"><span data-stu-id="ddff3-144">Currency</span></span></td>
<td><span data-ttu-id="ddff3-145">Если выбрано значение <strong>Указанная валюта</strong> в поле <strong>Тип валюты</strong>, выберите код валюты.</span><span class="sxs-lookup"><span data-stu-id="ddff3-145">If you selected <strong>Indicated currency</strong> in the <strong>Currency type</strong> field, select a currency code.</span></span> <span data-ttu-id="ddff3-146">Это поле недоступно, если в поле <strong>Тип валюты</strong> выбрано значение <strong>Валюта учета</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-146">This field is unavailable if you selected <strong>Accounting currency</strong> in the <strong>Currency type</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-147">Тип лимита остатка</span><span class="sxs-lookup"><span data-stu-id="ddff3-147">Balance limit type</span></span></td>
<td><span data-ttu-id="ddff3-148">Выберите одно из доступных значений:</span><span class="sxs-lookup"><span data-stu-id="ddff3-148">Select one of the available values:</span></span>
<ul>
<li><span data-ttu-id="ddff3-149"><strong>Максимум</strong> — сальдо денежных средств не должны превышать сумму <strong>Лимит остатка</strong> для кассового счета (верхняя граница).</span><span class="sxs-lookup"><span data-stu-id="ddff3-149"><strong>Maximum</strong> – The cash balance should not be allowed to exceed the <strong>Balance limit</strong> amount for the cash account (upper bound).</span></span></li>
<li><span data-ttu-id="ddff3-150"><strong>Минимум</strong> — сальдо денежных средств не должны опускаться ниже суммы <strong>Лимит остатка</strong> для кассового счета (нижняя граница).</span><span class="sxs-lookup"><span data-stu-id="ddff3-150"><strong>Minimum</strong> – The cash balance should not be allowed to go below the <strong>Balance limit</strong> amount for the cash account (bottom bound).</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-151">Проверка остатка</span><span class="sxs-lookup"><span data-stu-id="ddff3-151">Check balance limit</span></span></td>
<td><span data-ttu-id="ddff3-152">Выберите, что происходит во время процесса утверждения для кассовых документов, если сумма <strong>Лимит остатка</strong> для кассового счета превышена:</span><span class="sxs-lookup"><span data-stu-id="ddff3-152">Select what occurs during the approval process for cash documents if the <strong>Balance limit</strong> amount for the cash account is exceeded:</span></span>
<ul>
<li><span data-ttu-id="ddff3-153"><strong>Принять</strong> — лимит может быть превышен.</span><span class="sxs-lookup"><span data-stu-id="ddff3-153"><strong>Accept</strong> – The limit can be exceeded.</span></span></li>
<li><span data-ttu-id="ddff3-154"><strong>Предупреждение</strong> — лимит может быть превышен, но пользователь получает предупреждающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="ddff3-154"><strong>Warning</strong> – The limit can be exceeded, but the user receives a warning message.</span></span> <span data-ttu-id="ddff3-155">Кассовый документ подтверждается или утверждается.</span><span class="sxs-lookup"><span data-stu-id="ddff3-155">The cash document is confirmed or approved.</span></span></li>
<li><span data-ttu-id="ddff3-156"><strong>Ошибка</strong> — лимит не может быть превышен.</span><span class="sxs-lookup"><span data-stu-id="ddff3-156"><strong>Error</strong> – The limit can&#39;t be exceeded.</span></span> <span data-ttu-id="ddff3-157">Пользователь получает сообщение об ошибке, и кассовый документ не подтверждается или не утверждается.</span><span class="sxs-lookup"><span data-stu-id="ddff3-157">The user receives an error message, and the cash document isn&#39;t confirmed or approved.</span></span></li>
</ul>
<span data-ttu-id="ddff3-158">Дополнительные сведения о процессе утверждения для кассовых документов см. в пункте &quot;Утверждение и разноска кассовых проводок&quot; далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="ddff3-158">For more information about the approval process for cash documents, see the &quot;Cash transaction approval and posting&quot; section, later in this topic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-159">Лимит остатка</span><span class="sxs-lookup"><span data-stu-id="ddff3-159">Balance limit</span></span></td>
<td><span data-ttu-id="ddff3-160">Введите лимит для сальдо кассового счета.</span><span class="sxs-lookup"><span data-stu-id="ddff3-160">Enter a limit for the cash account balance.</span></span> <span data-ttu-id="ddff3-161">Сумма должна быть в указанной валюте.</span><span class="sxs-lookup"><span data-stu-id="ddff3-161">The amount should be in the currency that you specified.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-posting-profiles"></a><span data-ttu-id="ddff3-162">Настройка профилей разноски кассы</span><span class="sxs-lookup"><span data-stu-id="ddff3-162">Set up cash posting profiles</span></span>

<span data-ttu-id="ddff3-163">Профили разноски кассы определяют разноски в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="ddff3-163">Cash posting profiles define postings to the general ledger.</span></span> <span data-ttu-id="ddff3-164">Чтобы настроить профиль разноски кассы, перейдите в пункт **Управление** **банком и кассовыми операциями** &gt; **Настройка** &gt; **Профили разноски кассы** и выберите или создайте профиль разноски.</span><span class="sxs-lookup"><span data-stu-id="ddff3-164">To set up a cash posting profile, go to **Cash** **and bank management** &gt; **Setup** &gt; **Cash posting profiles**, and select or create a posting profile.</span></span> <span data-ttu-id="ddff3-165">Введите следующую информацию.</span><span class="sxs-lookup"><span data-stu-id="ddff3-165">Enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ddff3-166">Поле</span><span class="sxs-lookup"><span data-stu-id="ddff3-166">Field</span></span></th>
<th><span data-ttu-id="ddff3-167">описание</span><span class="sxs-lookup"><span data-stu-id="ddff3-167">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ddff3-168">Допустимый для</span><span class="sxs-lookup"><span data-stu-id="ddff3-168">Valid for</span></span></td>
<td><span data-ttu-id="ddff3-169">Выберите, будет ли профиль разноски применяться к конкретному кассовому счету или ко всем кассовым счетам:</span><span class="sxs-lookup"><span data-stu-id="ddff3-169">Select whether the posting profile applies to a specific cash account or all cash accounts:</span></span>
<ul>
<li><span data-ttu-id="ddff3-170"><strong>Таблица</strong> — если имеется строка профиля разноски для кассового счета, эта строка используется для разноски проводки по кассе.</span><span class="sxs-lookup"><span data-stu-id="ddff3-170"><strong>Table</strong> – If there is a posting profile line for the cash account, that line is used for cash transaction posting.</span></span></li>
<li><span data-ttu-id="ddff3-171"><strong>Все</strong> – отсутствует строка профиля разноски для кассового счета.</span><span class="sxs-lookup"><span data-stu-id="ddff3-171"><strong>All</strong> – There is no posting profile line for the cash account.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-172">Наличный расчет</span><span class="sxs-lookup"><span data-stu-id="ddff3-172">Cash</span></span></td>
<td><span data-ttu-id="ddff3-173">Если вы выбрали <strong>Таблица</strong> в поле <strong>Допустимый для</strong>, укажите кассовый счет.</span><span class="sxs-lookup"><span data-stu-id="ddff3-173">If you selected <strong>Table</strong> in the <strong>Valid for</strong> field, specify the cash account.</span></span> <span data-ttu-id="ddff3-174">Это поле остается пустым, если вы выбрали <strong>Все</strong> в поле <strong>Допустимый для</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-174">This field remains blank if you selected <strong>All</strong> in the <strong>Valid for</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-175">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="ddff3-175">Ledger account</span></span></td>
<td><span data-ttu-id="ddff3-176">Введите номер счета учета для использования в качестве итогового счета для кассового счета.</span><span class="sxs-lookup"><span data-stu-id="ddff3-176">Enter the number of the ledger account to use as the summary account for the cash account.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-number-sequences-for-cash-documents"></a><span data-ttu-id="ddff3-177">Настройка номерных серий для кассовых документов</span><span class="sxs-lookup"><span data-stu-id="ddff3-177">Set up number sequences for cash documents</span></span>

<span data-ttu-id="ddff3-178">Чтобы настроить номерные серии для кассовых документов, перейдите в пункт **Управление банком и кассовыми операциями** &gt; **Настройка** &gt; **Параметры управления банком и кассовыми операциями**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-178">To set up number sequences for cash documents, go to **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters**.</span></span> <span data-ttu-id="ddff3-179">На вкладке **Номерная серия** укажите коды номерных серий для документов **Приходные кассовые ордера**, **Расходные кассовые ордера**, **Ваучер сторно по кассе** и **Курсовая разница**, а также для **Номер отчета по обор. по ден. счетам.**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-179">On the **Number sequence** tab, specify number sequence codes for the **Cash reimbursement slips**, **Cash disbursement slips**, **Cash correction voucher**, and **Exchange adjustment** documents, and for **Cash report number**.</span></span>

### <a name="set-up-default-values-for-cash-and-bank-management-parameters"></a><span data-ttu-id="ddff3-180">Настройка значений по умолчанию для параметров управления банком и кассовыми операциями</span><span class="sxs-lookup"><span data-stu-id="ddff3-180">Set up default values for Cash and bank management parameters</span></span>

<span data-ttu-id="ddff3-181">Чтобы настроить значения по умолчанию для параметров управления банком и кассовыми операциями для функции мелких наличных денег, перейдите к пункту **Управление банком и кассовыми операциями** &gt; **Настройка** &gt; **Параметры управления банком и кассовыми операциями**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-181">To set up default values for Cash and bank management parameters for the petty cash functionality, go to **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters**.</span></span> <span data-ttu-id="ddff3-182">На вкладке **Касса** введите следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="ddff3-182">On the **Cash** tab, enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ddff3-183">Поле</span><span class="sxs-lookup"><span data-stu-id="ddff3-183">Field</span></span></th>
<th><span data-ttu-id="ddff3-184">описание</span><span class="sxs-lookup"><span data-stu-id="ddff3-184">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ddff3-185">Наличный расчет</span><span class="sxs-lookup"><span data-stu-id="ddff3-185">Cash</span></span></td>
<td><span data-ttu-id="ddff3-186">Выберите кассовый счет по умолчанию в журналах.</span><span class="sxs-lookup"><span data-stu-id="ddff3-186">Select the default cash account in journals.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-187">Разноска кассы</span><span class="sxs-lookup"><span data-stu-id="ddff3-187">Cash posting</span></span></td>
<td><span data-ttu-id="ddff3-188">Введите профиль разноски кассы по умолчанию, который используется, если не указан другой профиль разноски.</span><span class="sxs-lookup"><span data-stu-id="ddff3-188">Enter the default cash posting profile that is used if no other posting profile is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-189">Контроль использования ваучеров</span><span class="sxs-lookup"><span data-stu-id="ddff3-189">Check for voucher used</span></span></td>
<td><span data-ttu-id="ddff3-190">Выберите, что происходит, если дублирование номеров обнаружено во время проверки номера кассового документа:</span><span class="sxs-lookup"><span data-stu-id="ddff3-190">Select what occurs if duplicate numbers are found during the check of the cash document number:</span></span>
<ul>
<li><span data-ttu-id="ddff3-191">Запрещать дубликаты</span><span class="sxs-lookup"><span data-stu-id="ddff3-191">Reject duplicate</span></span></li>
<li><span data-ttu-id="ddff3-192">Запрещать копии внутри финансового года</span><span class="sxs-lookup"><span data-stu-id="ddff3-192">Reject copies within fiscal year</span></span></li>
<li><span data-ttu-id="ddff3-193">Принять дубликаты</span><span class="sxs-lookup"><span data-stu-id="ddff3-193">Accept duplicates</span></span></li>
<li><span data-ttu-id="ddff3-194">Предупреждать в случае повторений</span><span class="sxs-lookup"><span data-stu-id="ddff3-194">Warn in case of duplicates</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-195">Проверка суммы операции</span><span class="sxs-lookup"><span data-stu-id="ddff3-195">Check operations limit</span></span></td>
<td><span data-ttu-id="ddff3-196">Укажите, что произойдет при превышении лимита для операций с контрагентами:</span><span class="sxs-lookup"><span data-stu-id="ddff3-196">Specify what occurs if the limit for operations with counteragents is exceeded:</span></span>
<ul>
<li><span data-ttu-id="ddff3-197"><strong>Принять</strong> — лимит может быть превышен.</span><span class="sxs-lookup"><span data-stu-id="ddff3-197"><strong>Accept</strong> – The limit can be exceeded.</span></span></li>
<li><span data-ttu-id="ddff3-198"><strong>Предупреждение</strong> — лимит может быть превышен, но пользователь получает предупреждающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="ddff3-198"><strong>Warning</strong> – The limit can be exceeded, but the user receives a warning message.</span></span> <span data-ttu-id="ddff3-199">Операция разнесена.</span><span class="sxs-lookup"><span data-stu-id="ddff3-199">The operation is posted.</span></span></li>
<li><span data-ttu-id="ddff3-200"><strong>Ошибка</strong> — лимит не может быть превышен.</span><span class="sxs-lookup"><span data-stu-id="ddff3-200"><strong>Error</strong> – The limit can&#39;t be exceeded.</span></span> <span data-ttu-id="ddff3-201">Пользователь получает сообщение об ошибке, и операция не разносится.</span><span class="sxs-lookup"><span data-stu-id="ddff3-201">The user receives an error message, and the operation isn&#39;t posted.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-202">Метод проверки</span><span class="sxs-lookup"><span data-stu-id="ddff3-202">Validation method</span></span></td>
<td><span data-ttu-id="ddff3-203">Выберите метод проверки, который будет использоваться для управления превышением сумм лимитов по операциям:</span><span class="sxs-lookup"><span data-stu-id="ddff3-203">Select the validation method that is used to control exceeded limit amounts for operations:</span></span>
<ul>
<li><span data-ttu-id="ddff3-204"><strong>Операция</strong> — проверка выполняется по проводкам</span><span class="sxs-lookup"><span data-stu-id="ddff3-204"><strong>Operation</strong> – Validation is done per transaction</span></span></li>
<li><span data-ttu-id="ddff3-205"><strong>Соглашение</strong> — проверка выполняется отдельно по каждой проводке, для которой указан контракт с контрагентом.</span><span class="sxs-lookup"><span data-stu-id="ddff3-205"><strong>Agreement</strong> – Validation is done per transaction that has a specified contract with a counteragent.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-206">Лимит операций</span><span class="sxs-lookup"><span data-stu-id="ddff3-206">Operations limit</span></span></td>
<td><span data-ttu-id="ddff3-207">Введите максимальную сумму, которая допускается для операций с контрагентами в наличных средствах.</span><span class="sxs-lookup"><span data-stu-id="ddff3-207">Enter the maximum amount that is allowed for operations with counteragents in cash.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-208">Разноска на более раннюю дату</span><span class="sxs-lookup"><span data-stu-id="ddff3-208">Posting on earlier date</span></span></td>
<td><span data-ttu-id="ddff3-209">Установите этот флажок, чтобы разрешить разнесение кассовых проводок до последней даты кассовой проводки.</span><span class="sxs-lookup"><span data-stu-id="ddff3-209">Select this check box to enable cash transactions to be posted before the last date of the cash transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-210">Аналитики</span><span class="sxs-lookup"><span data-stu-id="ddff3-210">Dimensions</span></span></td>
<td><span data-ttu-id="ddff3-211">Введите аналитики в поля <strong>Код подразделения</strong>, <strong>Аналитический код</strong> и <strong>Код назначения</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-211">Enter dimensions in the <strong>Department code</strong>, <strong>Analytical code</strong>, and <strong>Purpose code</strong> fields.</span></span> <span data-ttu-id="ddff3-212">Форма печати для кассовых документов будет отражать эти сведения.</span><span class="sxs-lookup"><span data-stu-id="ddff3-212">The printing form for cash documents will reflect this information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-213">Использовать подтверждение</span><span class="sxs-lookup"><span data-stu-id="ddff3-213">Use confirm status</span></span></td>
<td><span data-ttu-id="ddff3-214">Установите этот флажок для использования дополнительного статуса <strong>Подтвержден</strong> во время процесса утверждении для кассовых документов.</span><span class="sxs-lookup"><span data-stu-id="ddff3-214">Select this check box to use an additional status, <strong>Confirmed</strong>, during the approval process for cash documents.</span></span> <span data-ttu-id="ddff3-215">(Дополнительные сведения см. в разделе &quot;Утверждение и разноска кассовых проводок&quot;.)</span><span class="sxs-lookup"><span data-stu-id="ddff3-215">(For more information, see the &quot;Cash transaction approval and posting&quot; section.)</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-journal-names-in-general-ledger"></a><span data-ttu-id="ddff3-216">Настройка имен кассовых журналов в главной книге</span><span class="sxs-lookup"><span data-stu-id="ddff3-216">Set up cash journal names in General ledger</span></span>

<span data-ttu-id="ddff3-217">Чтобы создать журнал для разноски проводок по кассе, перейдите к пункту **Главная книга** &gt; **Настройки журнала** &gt; **Имена журналов** и создайте новую запись.</span><span class="sxs-lookup"><span data-stu-id="ddff3-217">To create a journal for cash transaction posting, go to **General ledger** &gt; **Journal setup** &gt; **Journal names**, and create a new record.</span></span> <span data-ttu-id="ddff3-218">В поле **Тип журнала** укажите **Касса**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-218">In the **Journal type** field, specify **Cash**.</span></span> <span data-ttu-id="ddff3-219">Определите другие параметры журнала по умолчанию, как требуется.</span><span class="sxs-lookup"><span data-stu-id="ddff3-219">Define other default journal parameters as you require.</span></span>

## <a name="daily-cash-operations-via-a-slip-journal"></a><span data-ttu-id="ddff3-220">Ежедневные кассовые операции через журнал кассовых ордеров</span><span class="sxs-lookup"><span data-stu-id="ddff3-220">Daily cash operations via a Slip journal</span></span>
<span data-ttu-id="ddff3-221">Чтобы создать кассовый документ через журнал кассовых ордеров, перейдите к пункту **Управление банком и кассовыми операциями** &gt; **Проводки по кассе** &gt; **Журнал кассовых ордеров** и создайте новый журнал.</span><span class="sxs-lookup"><span data-stu-id="ddff3-221">To create a cash document via a Slip journal, go to **Cash and bank management** &gt; **Cash transactions** &gt; **Slip journal**, and create a new journal.</span></span> <span data-ttu-id="ddff3-222">В области действий щелкните **Строки**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-222">On the Action Pane, click **Lines**.</span></span> <span data-ttu-id="ddff3-223">Добавьте новую строку и введите следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="ddff3-223">Add a new line, and enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ddff3-224">Поле</span><span class="sxs-lookup"><span data-stu-id="ddff3-224">Field</span></span></th>
<th><span data-ttu-id="ddff3-225">описание</span><span class="sxs-lookup"><span data-stu-id="ddff3-225">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ddff3-226">Дата</span><span class="sxs-lookup"><span data-stu-id="ddff3-226">Date</span></span></td>
<td><span data-ttu-id="ddff3-227">Введите дату проводки.</span><span class="sxs-lookup"><span data-stu-id="ddff3-227">Enter the date of the transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-228">Учетная запись</span><span class="sxs-lookup"><span data-stu-id="ddff3-228">Account</span></span></td>
<td><span data-ttu-id="ddff3-229">Выберите кассовый счет.</span><span class="sxs-lookup"><span data-stu-id="ddff3-229">Select the cash account.</span></span> <span data-ttu-id="ddff3-230">По умолчанию кассовый счет задается в параметрах управления банком и кассовыми операциями.</span><span class="sxs-lookup"><span data-stu-id="ddff3-230">By default, a cash account is specified in the Cash and bank management parameters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-231">описание</span><span class="sxs-lookup"><span data-stu-id="ddff3-231">Description</span></span></td>
<td><span data-ttu-id="ddff3-232">Введите пояснительный текста для проводки.</span><span class="sxs-lookup"><span data-stu-id="ddff3-232">Enter explanatory text for the transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-233">Дебет и кредит</span><span class="sxs-lookup"><span data-stu-id="ddff3-233">Debit Credit</span></span></td>
<td><span data-ttu-id="ddff3-234">Введите сумму кассового документа в одном из этих полей:</span><span class="sxs-lookup"><span data-stu-id="ddff3-234">Enter cash document amount in one of these fields:</span></span>
<ul>
<li><span data-ttu-id="ddff3-235"><strong>Дебет</strong> — это поле используется для регистрации поступления наличных денег и приходного кассового ордера.</span><span class="sxs-lookup"><span data-stu-id="ddff3-235"><strong>Debit</strong> – Use this field to register cash receipts and a Cash reimbursement slip.</span></span></li>
<li><span data-ttu-id="ddff3-236"><strong>Кредит</strong> — это поле используется для регистрации расходов наличных средств и расходного кассового ордера.</span><span class="sxs-lookup"><span data-stu-id="ddff3-236"><strong>Credit</strong> – Use this field to register cash expenditures and a Cash disbursement slip.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-237">Тип корр. счета и корр. счет</span><span class="sxs-lookup"><span data-stu-id="ddff3-237">Offset account type Offset account</span></span></td>
<td><span data-ttu-id="ddff3-238">Выберите тип корр. счета и номер корр. счета.</span><span class="sxs-lookup"><span data-stu-id="ddff3-238">Select an offset account type and offset account number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-239">Валютное</span><span class="sxs-lookup"><span data-stu-id="ddff3-239">Currency</span></span></td>
<td><span data-ttu-id="ddff3-240">Выберите код для валюты проводки.</span><span class="sxs-lookup"><span data-stu-id="ddff3-240">Select the code for the transaction currency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-241">Ваучер</span><span class="sxs-lookup"><span data-stu-id="ddff3-241">Voucher</span></span></td>
<td><span data-ttu-id="ddff3-242">Это поле заполняется автоматически на основе настроек журнала.</span><span class="sxs-lookup"><span data-stu-id="ddff3-242">This field is filled in automatically, based on the journal setup.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-243">Порядковый номер</span><span class="sxs-lookup"><span data-stu-id="ddff3-243">Order number</span></span></td>
<td><span data-ttu-id="ddff3-244">Если никакая другая номерная серия не настроена для кассового счета, это поле будет заполнено автоматически на основе номерной серии, которая указана в параметрах.</span><span class="sxs-lookup"><span data-stu-id="ddff3-244">If no other number sequence is set up for the cash account, this field is filled in automatically, based on the number sequence that is specified in the parameters.</span></span> <span data-ttu-id="ddff3-245">Можно вручную ввести в этом поле требуемый порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="ddff3-245">You can manually enter an order number in this field as you require.</span></span> <span data-ttu-id="ddff3-246">Чтобы исключить несоответствия в нумерации кассовых документов, применяется следующее правило: номер кассового документа, имеющего более раннюю дату операции, не может быть выше, чем номер кассового документа, который имеет более позднюю дату операции.</span><span class="sxs-lookup"><span data-stu-id="ddff3-246">To prevent inconsistence in cash document numbering, the following control is applied: the number of a cash document that has an earlier date of operation can&#39;t be higher than number of a cash document that has a later date of operation.</span></span> <span data-ttu-id="ddff3-247">Если это правило не требуется, установите флажок <strong>Разноска на более раннюю дату</strong> в параметрах управления банком и кассовыми операциями.</span><span class="sxs-lookup"><span data-stu-id="ddff3-247">If you don&#39;t require this control, select the <strong>Posting on earlier date</strong> check box in the Cash and bank management parameters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-248">Статус одобрения</span><span class="sxs-lookup"><span data-stu-id="ddff3-248">Approval status</span></span></td>
<td><span data-ttu-id="ddff3-249">Статус первой проводки имеет значение <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-249">The first transaction status is <strong>None</strong>.</span></span> <span data-ttu-id="ddff3-250">Сведения о том, как задать статус проводки, см. в разделе &quot;Утверждение и разноска кассовых проводок&quot;.</span><span class="sxs-lookup"><span data-stu-id="ddff3-250">For information about how to set the transaction status, See the &quot;Cash transaction approval and posting&quot; section.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-251">Вид документа</span><span class="sxs-lookup"><span data-stu-id="ddff3-251">Document type</span></span></td>
<td><span data-ttu-id="ddff3-252">Это поле на вкладке <strong>Кассовый ордер</strong> заполняется автоматически на основе суммы, введенной для кассового документа:</span><span class="sxs-lookup"><span data-stu-id="ddff3-252">This field on the <strong>Cash order</strong> tab is filled in automatically, based on the amount that you entered for the cash document:</span></span>
<ul>
<li><span data-ttu-id="ddff3-253"><strong>Приходный кассовый ордер</strong> — это значение используется в том случае, если вы ввели сумму в поле <strong>Дебет</strong> для кассового счета.</span><span class="sxs-lookup"><span data-stu-id="ddff3-253"><strong>Cash reimbursement slip</strong> – This value is used if you entered an amount in the <strong>Debit</strong> field for the cash account.</span></span></li>
<li><span data-ttu-id="ddff3-254"><strong>Расходный кассовый ордер</strong> — это значение используется в том случае, если вы ввели сумму в поле <strong>Кредит</strong> для кассового счета.</span><span class="sxs-lookup"><span data-stu-id="ddff3-254"><strong>Cash disbursement slip</strong> – This value is used if you entered an amount in the <strong>Credit</strong> field for the cash account</span></span></li>
<li><span data-ttu-id="ddff3-255"><strong>Коррекция</strong> — вы ввели отрицательную сумму в поле <strong>Дебет</strong> или <strong>Кредит</strong> для кассового счета.</span><span class="sxs-lookup"><span data-stu-id="ddff3-255"><strong>Correction</strong> – You entered a negative amount in either the <strong>Debit</strong> field or the <strong>Credit</strong> field for the cash account.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-256">Налоговая группа</span><span class="sxs-lookup"><span data-stu-id="ddff3-256">Sales tax group</span></span></td>
<td><span data-ttu-id="ddff3-257">Укажите налоговую группу для расчета налогов для операции.</span><span class="sxs-lookup"><span data-stu-id="ddff3-257">Specify a sales tax group to calculate taxes on the operation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-258">Налоговая группа номенклатур</span><span class="sxs-lookup"><span data-stu-id="ddff3-258">Item sales tax group</span></span></td>
<td><span data-ttu-id="ddff3-259">Укажите налоговую группу номенклатур для расчета налогов для операции.</span><span class="sxs-lookup"><span data-stu-id="ddff3-259">Specify an item sales tax group to calculate taxes on the operation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-260">Причина</span><span class="sxs-lookup"><span data-stu-id="ddff3-260">Reason</span></span></td>
<td><span data-ttu-id="ddff3-261">На вкладке <strong>Кассовый ордер</strong> введите текст, описывающий тему проводки.</span><span class="sxs-lookup"><span data-stu-id="ddff3-261">On the <strong>Cash order</strong> tab, enter text that describes the transaction subject.</span></span> <span data-ttu-id="ddff3-262">Этот текст печатается на бланке отчетности кассового ордера.</span><span class="sxs-lookup"><span data-stu-id="ddff3-262">This text will be printed on the cash slip reporting form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-263">Дата документа</span><span class="sxs-lookup"><span data-stu-id="ddff3-263">Document Date</span></span></td>
<td><span data-ttu-id="ddff3-264">Введите описание, номер и дату основного документа, который является основанием для проводки (например, авансовые отчеты, счет или ордер).</span><span class="sxs-lookup"><span data-stu-id="ddff3-264">Enter the description, number, and date of the primary document that is the reason for the transaction (for example, advance reports, invoice, or order).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-265">Тип представителя</span><span class="sxs-lookup"><span data-stu-id="ddff3-265">Representative type</span></span></td>
<td><span data-ttu-id="ddff3-266">Это поле может содержать следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ddff3-266">This field can have the following values:</span></span>
<ul>
<li><span data-ttu-id="ddff3-267"><strong>Работник</strong> — поле поиска <strong>Представитель</strong> содержит список сотрудников, если в поле <strong>Корр. счет</strong> задано значение <strong>Главная книга</strong> или <strong>Банк</strong>, или список контактных лиц контрагента, если в поле <strong>Корр. счет</strong> задано значение <strong>Клиент</strong> или <strong>Поставщик</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-267"><strong>Worker</strong> – The <strong>Representative</strong> lookup contains a list of employees if the <strong>Offset account</strong> field is set to <strong>Ledger</strong> or <strong>Bank</strong>, or a list of the counteragent&#39;s contact persons if the <strong>Offset account</strong> field is set to <strong>Customer</strong> or <strong>Vendor</strong>.</span></span> <span data-ttu-id="ddff3-268">Чтобы настроить представителей, перейдите к пункту <strong>Основное</strong> &gt; <strong>Настройка</strong> &gt; <strong>Контакты</strong> &gt; <strong>Контактное лицо</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-268">To set up representatives, go to <strong>Basic</strong> &gt; <strong>Setup</strong> &gt; <strong>Contacts</strong> &gt; <strong>Contact person</strong>.</span></span></li>
<li><span data-ttu-id="ddff3-269"><strong>Другие</strong> — поле поиска <strong>Представитель</strong> содержит список других клиентов.</span><span class="sxs-lookup"><span data-stu-id="ddff3-269"><strong>Other</strong> – The <strong>Representative</strong> lookup contains a list of other clients.</span></span> <span data-ttu-id="ddff3-270">Чтобы настроить получателей, которые не отображаются в таблице <strong>Клиенты</strong> или <strong>Поставщики</strong>, перейдите к пункту <strong>Главная книга</strong> &gt; <strong>Получатели</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-270">To set up receivers who don&#39;t appear in the <strong>Customers</strong> or <strong>Vendors</strong> table, go to <strong>General ledger</strong> &gt; <strong>Receivers</strong>.</span></span> <span data-ttu-id="ddff3-271">Этот тип доступен только для Латвии.</span><span class="sxs-lookup"><span data-stu-id="ddff3-271">This type is available only for Latvia.</span></span> <span data-ttu-id="ddff3-272">(Должен быть включен конфигурационный ключ <strong>CSELatvia</strong>.)</span><span class="sxs-lookup"><span data-stu-id="ddff3-272">(The <strong>CSELatvia</strong> configuration key should be enabled.)</span></span></li>
<li><span data-ttu-id="ddff3-273"><strong>Поставщик</strong> — поле поиска <strong>Представитель</strong> содержит список других поставщиков.</span><span class="sxs-lookup"><span data-stu-id="ddff3-273"><strong>Vendor</strong> – The <strong>Representative</strong> lookup contains a list of vendors.</span></span> <span data-ttu-id="ddff3-274">Для настройки поставщиков перейдите к <strong>Расчеты с поставщиками</strong> &gt; <strong>Поставщики</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-274">To set up vendors, go to <strong>Accounts payable</strong> &gt; <strong>Vendors</strong>.</span></span></li>
<li><span data-ttu-id="ddff3-275"><strong>Клиент</strong> — поле поиска <strong>Представитель</strong> содержит список других клиентов.</span><span class="sxs-lookup"><span data-stu-id="ddff3-275"><strong>Customer</strong> – The <strong>Representative</strong> lookup contains a list of customers.</span></span> <span data-ttu-id="ddff3-276">Чтобы настроить клиентов, перейдите к пункту <strong>Расчеты с клиентами</strong> &gt; <strong>Клиенты</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-276">To set up customers, go to <strong>Accounts receivable</strong> &gt; <strong>Customers</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-277">Уполномоченный</span><span class="sxs-lookup"><span data-stu-id="ddff3-277">Representative</span></span></td>
<td><span data-ttu-id="ddff3-278">Выберите представителя типа, указанного в поле <strong>Тип представителя</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-278">Select a representative of the type that you specified in the <strong>Representative type</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-279">Имя</span><span class="sxs-lookup"><span data-stu-id="ddff3-279">Name of person</span></span></td>
<td><span data-ttu-id="ddff3-280">Это поле заполняется автоматически на основе полей <strong>Корр. счет</strong> и <strong>Представитель</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-280">This field is filled in automatically, based on the <strong>Offset account</strong> and <strong>Representative</strong> fields.</span></span> <span data-ttu-id="ddff3-281">Форма печати для кассовых ордеров будет отражать эти сведения.</span><span class="sxs-lookup"><span data-stu-id="ddff3-281">The printing form for cash slips will reflect this information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-282">Удостоверение личности</span><span class="sxs-lookup"><span data-stu-id="ddff3-282">Identity card</span></span></td>
<td><span data-ttu-id="ddff3-283">Это поле заполняется автоматически на основе данных карты удостоверения личности для контактного лица (представителя).</span><span class="sxs-lookup"><span data-stu-id="ddff3-283">This field is filled in automatically, based on the identity card data for the contact person (representative).</span></span> <span data-ttu-id="ddff3-284">Если в поле <strong>Тип корр. счета</strong> задано значение <strong>Подотчетное лицо</strong>, а в поле <strong>Корр. счет</strong> задан номер сотрудника, приходы и расходы денежных средств могут осуществляться от сотрудника или сотруднику.</span><span class="sxs-lookup"><span data-stu-id="ddff3-284">If the <strong>Offset account type</strong> field is set to <strong>Advance holder</strong>, and the <strong>Offset account</strong> field is set to an employee number, cash receipts or expenditures can be done from or to the employee.</span></span> <span data-ttu-id="ddff3-285">В этом случае поле <strong>Удостоверение личности</strong> заполняется автоматически с использованием данных для удостоверения личности из таблицы <strong>Сотрудник</strong> (<strong>Учет кадров</strong> &gt; <strong>Таблица сотрудников</strong>).</span><span class="sxs-lookup"><span data-stu-id="ddff3-285">In this case the <strong>Identity card</strong> field is filled in automatically by using data for the identity card from the <strong>Employee</strong> table (<strong>Staff accounting</strong> &gt; <strong>Employee table</strong>).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-286">Цель</span><span class="sxs-lookup"><span data-stu-id="ddff3-286">Purpose</span></span></td>
<td><span data-ttu-id="ddff3-287">В таблице <strong>Назначение</strong> определите один или несколько кодов назначения для суммы проводки.</span><span class="sxs-lookup"><span data-stu-id="ddff3-287">In the <strong>Purpose</strong> table, define one or more destination codes for the transaction amount.</span></span> <span data-ttu-id="ddff3-288">Выберите код назначения в поле <strong>Назначение</strong> и введите пояснение в поле <strong>Текст проводки</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-288">Select a destination code in the <strong>Purpose</strong> field, and enter an explanation in the <strong>Transaction text</strong> field.</span></span> <span data-ttu-id="ddff3-289">В поле <strong>Сумма</strong> введите сумму в валюте проводки.</span><span class="sxs-lookup"><span data-stu-id="ddff3-289">In the <strong>Amount</strong> field, enter an amount in the transaction currency.</span></span> <span data-ttu-id="ddff3-290">Поле <strong>Процент</strong> показывает (в процентах) отношение суммы назначения к общей сумме проводки.</span><span class="sxs-lookup"><span data-stu-id="ddff3-290">The <strong>Percent</strong> field shows, as a percentage, the ratio of the destination amount to the total transaction amount.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-291">Остаток</span><span class="sxs-lookup"><span data-stu-id="ddff3-291">Remainder</span></span></td>
<td><span data-ttu-id="ddff3-292">Рассчитанная сумма остатка.</span><span class="sxs-lookup"><span data-stu-id="ddff3-292">The remaining amount that is calculated.</span></span> <span data-ttu-id="ddff3-293">Обратите внимание, что коды назначения должны быть назначены всей сумме проводки.</span><span class="sxs-lookup"><span data-stu-id="ddff3-293">Note that the whole transaction amount must be assigned to destination codes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-294">Должностные лица</span><span class="sxs-lookup"><span data-stu-id="ddff3-294">Officials</span></span></td>
<td><span data-ttu-id="ddff3-295">На вкладке <strong>Должностные лица</strong> укажите имена и должности ответственных лиц: директор, главный бухгалтер и кассир.</span><span class="sxs-lookup"><span data-stu-id="ddff3-295">On the <strong>Officials</strong> tab, specify the names and titles for responsible persons: Director, Chief accountant, and Cashier.</span></span> <span data-ttu-id="ddff3-296">Значения <strong>Должность</strong> определяются настройкой должностных лиц на вкладках <strong>Общее</strong> и <strong>Главная книга</strong> страницы <strong>Должностные лица</strong> (<strong>Основное</strong> &gt; <strong>Настройка</strong> &gt; <strong>Контакты</strong> &gt; <strong>Должностные лица</strong>).</span><span class="sxs-lookup"><span data-stu-id="ddff3-296">The <strong>Position</strong> values are determined by the setup of officials on the <strong>General</strong> and <strong>Ledger</strong> tabs of the <strong>Officials</strong> page (<strong>Basic</strong> &gt; <strong>Setup</strong> &gt; <strong>Contacts</strong> &gt; <strong>Officials</strong>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-297">Предоплата</span><span class="sxs-lookup"><span data-stu-id="ddff3-297">Prepayment</span></span></td>
<td><span data-ttu-id="ddff3-298">Этот флажок устанавливается, если проводка является предоплатой.</span><span class="sxs-lookup"><span data-stu-id="ddff3-298">Select this check box if the transaction is a prepayment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-299">Профиль разноски</span><span class="sxs-lookup"><span data-stu-id="ddff3-299">Posting profile</span></span></td>
<td><span data-ttu-id="ddff3-300">Введите профиль разноски для кассового счета.</span><span class="sxs-lookup"><span data-stu-id="ddff3-300">Enter the posting profile for the cash account.</span></span> <span data-ttu-id="ddff3-301">По умолчанию используется профиль разноски, который указан в параметрах управления банком и кассовыми операциями.</span><span class="sxs-lookup"><span data-stu-id="ddff3-301">By default, the posting profile that is specified in the Cash and bank management parameters is used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-302">Разноска по корр. счету</span><span class="sxs-lookup"><span data-stu-id="ddff3-302">Offset posting profile</span></span></td>
<td><span data-ttu-id="ddff3-303">Введите профиль разноски для выбранного корр. счета.</span><span class="sxs-lookup"><span data-stu-id="ddff3-303">Enter the posting profile for the selected offset account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-304">Итоговая сумма</span><span class="sxs-lookup"><span data-stu-id="ddff3-304">Total amount</span></span></td>
<td><span data-ttu-id="ddff3-305">В группе полей <strong>Общая сумма</strong> в нижней части страницы поле <strong>Приход</strong> показывает общую сумму, которая вычисляется для всех приходных кассовых ордеров, которые введены в текущий журнал, а поле <strong>Расход</strong> показывает общую сумму для всех расходных кассовых ордеров.</span><span class="sxs-lookup"><span data-stu-id="ddff3-305">In the <strong>Total amount</strong> field group at the bottom of the page, the <strong>Reimb</strong> field shows the total that is calculated for all Cash reimbursement slips that are entered in the current journal, and the <strong>Disb</strong> field shows the total for all Cash disbursement slips.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ddff3-306">Чтобы проверить записи журнала на панели операций щелкните **Проверить**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-306">To check journal entries, on the Action Pane, click **Validate**.</span></span>

## <a name="daily-cash-operations-via-a-general-journal"></a><span data-ttu-id="ddff3-307">Ежедневные кассовые операции через общий журнал</span><span class="sxs-lookup"><span data-stu-id="ddff3-307">Daily cash operations via a General journal</span></span>
<span data-ttu-id="ddff3-308">Для создания кассовой проводки через общий журнал, перейдите к пункту **Главная книга** &gt; **Записи журнала** &gt; **Общие журналы** и создайте новый журнал.</span><span class="sxs-lookup"><span data-stu-id="ddff3-308">To create a cash transaction via a General journal, go to **General ledger** &gt; **Journal entries** &gt; **General journals**, and create a new journal.</span></span> <span data-ttu-id="ddff3-309">В области действий щелкните **Строки**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-309">On the Action Pane, click **Lines**.</span></span> <span data-ttu-id="ddff3-310">Добавьте новую строку и введите следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="ddff3-310">Add a new line, and enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ddff3-311">Поле</span><span class="sxs-lookup"><span data-stu-id="ddff3-311">Field</span></span></th>
<th><span data-ttu-id="ddff3-312">описание</span><span class="sxs-lookup"><span data-stu-id="ddff3-312">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ddff3-313">Дата</span><span class="sxs-lookup"><span data-stu-id="ddff3-313">Date</span></span></td>
<td><span data-ttu-id="ddff3-314">Введите дату проводки.</span><span class="sxs-lookup"><span data-stu-id="ddff3-314">Enter the date of the transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-315">Тип счета</span><span class="sxs-lookup"><span data-stu-id="ddff3-315">Account type</span></span></td>
<td><span data-ttu-id="ddff3-316">Выберите <strong>Кассовые операции</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-316">Select <strong>Petty cash</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-317">Учетная запись</span><span class="sxs-lookup"><span data-stu-id="ddff3-317">Account</span></span></td>
<td><span data-ttu-id="ddff3-318">Выберите номер кассового счета.</span><span class="sxs-lookup"><span data-stu-id="ddff3-318">Select the cash account number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-319">Текст проводки</span><span class="sxs-lookup"><span data-stu-id="ddff3-319">Transaction text</span></span></td>
<td><span data-ttu-id="ddff3-320">Введите пояснительный текста для проводки.</span><span class="sxs-lookup"><span data-stu-id="ddff3-320">Enter explanatory text for the transaction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-321">Дебет и кредит</span><span class="sxs-lookup"><span data-stu-id="ddff3-321">Debit Credit</span></span></td>
<td><span data-ttu-id="ddff3-322">Введите сумму кассового документа в одном из этих полей:</span><span class="sxs-lookup"><span data-stu-id="ddff3-322">Enter cash document amount in one of these fields:</span></span>
<ul>
<li><span data-ttu-id="ddff3-323"><strong>Дебет</strong> — это поле используется для регистрации поступления наличных денег и приходного кассового ордера.</span><span class="sxs-lookup"><span data-stu-id="ddff3-323"><strong>Debit</strong> – Use this field to register cash receipts and a Cash reimbursement slip.</span></span></li>
<li><span data-ttu-id="ddff3-324"><strong>Кредит</strong> — это поле используется для регистрации расходов наличных средств и расходного кассового ордера.</span><span class="sxs-lookup"><span data-stu-id="ddff3-324"><strong>Credit</strong> – Use this field to register cash expenditures and a Cash disbursement slip.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-325">Тип корр. счета и корр. счет</span><span class="sxs-lookup"><span data-stu-id="ddff3-325">Offset account type Offset account</span></span></td>
<td><span data-ttu-id="ddff3-326">Выберите тип корр. счета и номер корр. счета.</span><span class="sxs-lookup"><span data-stu-id="ddff3-326">Select an offset account type and offset account number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-327">Валютное</span><span class="sxs-lookup"><span data-stu-id="ddff3-327">Currency</span></span></td>
<td><span data-ttu-id="ddff3-328">Выберите код для валюты проводки.</span><span class="sxs-lookup"><span data-stu-id="ddff3-328">Select the code for the transaction currency.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ddff3-329">На вкладке **Накладная** можно указать профили разноски для выбранного счета и корр. счета.</span><span class="sxs-lookup"><span data-stu-id="ddff3-329">On the **Invoice** tab, you can specify posting profiles for the selected account and offset account.</span></span> <span data-ttu-id="ddff3-330">Если зарегистрированная проводка является предоплатой, установите флажок **Предоплата** на вкладке **Платеж**. В группе полей **Представитель** заполните поля, как вы делали для строк журнала ордеров для печати отчета **Касса**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-330">If the registered transaction is a prepayment, select the **Prepayment** check box on the **Payment** tab. In the **Representative** field group, fill in the fields as you did for the Slip journal lines to print on the **Cash** report.</span></span> <span data-ttu-id="ddff3-331">Чтобы проверить записи журнала на панели операций щелкните **Проверить**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-331">To check journal entries, on the Action Pane, click **Validate**.</span></span>

## <a name="cash-transaction-approval-and-posting"></a><span data-ttu-id="ddff3-332">Утверждение и разноска кассовых проводок</span><span class="sxs-lookup"><span data-stu-id="ddff3-332">Cash transaction approval and posting</span></span>
<span data-ttu-id="ddff3-333">Для проводок по кассе могут быть применены следующие статусы: **Нет**, **Подтверждено**, **Утверждено** и **Отклонено**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-333">For cash transactions, the following statuses can be applied: **None**, **Confirmed**, **Approved**, and **Rejected**.</span></span> <span data-ttu-id="ddff3-334">Параметр **Использовать подтверждение** на экспресс-вкладке **Утверждение** вкладки **Касса** на странице **Управление банком и кассовыми операциями** &gt; **Настройка** &gt; **Параметры управления банком и кассовыми операциями** позволяет активировать два дополнительных статуса: **Подтверждено** и **Отклонено**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-334">A **Use confirm status** parameter on the **Approval** FastTab of the **Cash** tab at **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters** lets you activate two additional statuses: **Confirmed** and **Rejected**.</span></span> <span data-ttu-id="ddff3-335">Подтверждение удобно, когда выдаются кассовые документы, а кассовые приходные и расходные ордера являются общими для двух сотрудников: бухгалтер и кассир.</span><span class="sxs-lookup"><span data-stu-id="ddff3-335">Confirmation is appropriate when cash documents are issued, and cash receipts or expenditures are shared between two employees: accountant and cashier.</span></span> <span data-ttu-id="ddff3-336">Функция **Сброс статуса** меняет текущий статус проводки.</span><span class="sxs-lookup"><span data-stu-id="ddff3-336">The **Reset status** function changes the current transaction status.</span></span> <span data-ttu-id="ddff3-337">**Утверждено** становится **Подтверждено**, а **Подтверждено** становится **Нет**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-337">**Approved** becomes **Confirmed**, and **Confirmed** becomes **None**.</span></span> <span data-ttu-id="ddff3-338">Записи в кассовом журнале могут редактироваться только в том случае, если они имеют статус **Нет**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-338">Cash journal entries can be edited only when the status is **None**.</span></span> <span data-ttu-id="ddff3-339">Проводки по кассе могут быть отклонены только в том случае, если статус проводки имеет значение **Подтверждено**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-339">Cash transactions can be rejected only if the transaction status is **Confirmed**.</span></span> <span data-ttu-id="ddff3-340">Отклоненные кассовые документы включаются в отчет **Журнал регистрации кассовых документов**, но они отражаются в отчете **Кассовая книга**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-340">Rejected cash documents are included on the **Journal of registration of cash documents** report, but they aren't reflected on the **Cash book** report.</span></span> <span data-ttu-id="ddff3-341">Чтобы подтвердить проводку, выберите соответствующую строку журнала ордеров, затем щелкните **Одобрение документов** &gt; **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-341">To confirm a transaction, select the corresponding Slip journal line, and then click **Documents approval** &gt; **Confirm**.</span></span> <span data-ttu-id="ddff3-342">Создается номер ордера на основе указанной номерной серии.</span><span class="sxs-lookup"><span data-stu-id="ddff3-342">An order number is generated, based on the specified number sequence.</span></span> <span data-ttu-id="ddff3-343">Статус проводки изменяется на **Подтверждено**, и изменять строку журнала больше нельзя.</span><span class="sxs-lookup"><span data-stu-id="ddff3-343">The transaction status is changed to **Confirmed**, and you can no longer edit the journal line.</span></span> <span data-ttu-id="ddff3-344">Сальдо кассового счета не изменяется.</span><span class="sxs-lookup"><span data-stu-id="ddff3-344">The cash account balance remains unchanged.</span></span> <span data-ttu-id="ddff3-345">Чтобы отклонить кассовый документ, щелкните **Одобрение документов** &gt; **Отклонить**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-345">To reject a cash document, click **Documents approval** &gt; **Reject**.</span></span> <span data-ttu-id="ddff3-346">Этот вариант доступен только для документов со статусом **Подтверждено**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-346">This option is available only for documents that have **Confirmed** status.</span></span> <span data-ttu-id="ddff3-347">Чтобы утвердить проводку, выберите соответствующую строку журнала ордеров, затем щелкните **Одобрение документов** &gt; **Утвердить**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-347">To approve a transaction, select the corresponding Slip journal line, and then click **Documents approval** &gt; **Approve**.</span></span> <span data-ttu-id="ddff3-348">Статус **Утверждено** указывает, что денежные средства получены или выданы.</span><span class="sxs-lookup"><span data-stu-id="ddff3-348">The **Approved** status indicates that cash funds are received or expended.</span></span> <span data-ttu-id="ddff3-349">Кассовое сальдо изменяется.</span><span class="sxs-lookup"><span data-stu-id="ddff3-349">The cash balance is changed.</span></span> <span data-ttu-id="ddff3-350">Можно разнести проводки по кассе.</span><span class="sxs-lookup"><span data-stu-id="ddff3-350">The cash transaction can be posted.</span></span> <span data-ttu-id="ddff3-351">Чтобы отменить статус **Утверждено** и сбросить статус на **Нет**, щелкните **Одобрение документов** &gt; **Сброс статуса**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-351">To cancel an **Approved** status and reset the status to **None**, click **Documents approval** &gt; **Reset status**.</span></span> <span data-ttu-id="ddff3-352">Можно разносить только утвержденные проводки по кассе.</span><span class="sxs-lookup"><span data-stu-id="ddff3-352">Only approved cash transactions can be posted.</span></span> <span data-ttu-id="ddff3-353">Чтобы разнести журнал, щелкните **Разноска** &gt; **Разноска**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-353">To post a journal, click **Post** &gt; **Post**.</span></span>

## <a name="print-a-cash-order"></a><span data-ttu-id="ddff3-354">Печать кассового ордера</span><span class="sxs-lookup"><span data-stu-id="ddff3-354">Print a cash order</span></span>
<span data-ttu-id="ddff3-355">Чтобы напечатать кассовый ордер, выберите строку журнала ордеров, затем в области действий щелкните **Печать** &gt; **Отчет по кассовым ордерам**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-355">To print a cash order, select a Slip journal line, and then, on the Action Pane, click **Print** &gt; **Cash order report**.</span></span> <span data-ttu-id="ddff3-356">Система генерирует форму печати расходного кассового ордера или приходного кассового ордера, в зависимости от того, введена ли сумма в поле **Дебет** или **Кредит** для выбранной строки:</span><span class="sxs-lookup"><span data-stu-id="ddff3-356">The system generates a printing form for either a Cash reimbursement slip or a Cash disbursement slip, depending on whether an amount is entered in the **Debit** field the or **Credit** field for the selected line:</span></span>

-   <span data-ttu-id="ddff3-357">Если есть сумма в поле **Дебет**: приходный кассовый ордер</span><span class="sxs-lookup"><span data-stu-id="ddff3-357">If there is an amount in the **Debit** field: Cash reimbursement slip</span></span>
-   <span data-ttu-id="ddff3-358">Если есть сумма в поле **Кредит**: расходный кассовый ордер</span><span class="sxs-lookup"><span data-stu-id="ddff3-358">If there is an amount in the **Credit** field: Cash disbursement slip</span></span>

<span data-ttu-id="ddff3-359">Строки журнала ордеров со статусом **Подтверждено**, **Утверждено** или **Отклонено** могут быть напечатаны.</span><span class="sxs-lookup"><span data-stu-id="ddff3-359">Slip journal lines that have **Confirmed**, **Approved**, or **Rejected** status can be printed.</span></span> <span data-ttu-id="ddff3-360">Можно также печатать документы кассовых ордеров с помощью пункта **Управление банком и кассовыми операциями** &gt; **Запросы и отчеты** &gt; **Кассовый ордер**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-360">You can also print cash order documents at **Cash and bank management** &gt; **Inquires and reports** &gt; **Cash order**.</span></span>

## <a name="periodic-tasks"></a><span data-ttu-id="ddff3-361">Периодические задачи</span><span class="sxs-lookup"><span data-stu-id="ddff3-361">Periodic tasks</span></span>
<span data-ttu-id="ddff3-362">Следующие задачи могут выполняться с помощью пункта **Управление банком и кассовыми операциями** &gt; **Периодические задачи**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-362">The following tasks can be performed at **Cash and bank management** &gt; **Periodic tasks**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ddff3-363">Периодическая задача</span><span class="sxs-lookup"><span data-stu-id="ddff3-363">Periodic task</span></span></th>
<th><span data-ttu-id="ddff3-364">описание</span><span class="sxs-lookup"><span data-stu-id="ddff3-364">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ddff3-365">Проверка остатка</span><span class="sxs-lookup"><span data-stu-id="ddff3-365">Check balance limit</span></span></td>
<td><span data-ttu-id="ddff3-366">Проверьте сальдо для выбранного кассового счета на указанную дату и выведите результат в информационном сообщении.</span><span class="sxs-lookup"><span data-stu-id="ddff3-366">Check the balance for the selected cash account on the specified date, and show the result in an information message.</span></span> <span data-ttu-id="ddff3-367">Только утвержденные проводки могут учитываться в расчет сальдо.</span><span class="sxs-lookup"><span data-stu-id="ddff3-367">Only approved transactions can be counted in the balance calculation.</span></span> <span data-ttu-id="ddff3-368">Проводки, помеченные как <strong>На зарплату</strong>, не учитываются.</span><span class="sxs-lookup"><span data-stu-id="ddff3-368">Transactions that are marked as <strong>For payroll</strong> aren&#39;t considered.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-369">Пересчет баланса по кассе</span><span class="sxs-lookup"><span data-stu-id="ddff3-369">Cash balance recalculation</span></span></td>
<td><span data-ttu-id="ddff3-370">Используйте эту задачу, чтобы убедиться в том, что бухгалтерский баланс для кассовых счетов соответствует сальдо по кассе.</span><span class="sxs-lookup"><span data-stu-id="ddff3-370">Use this task to make sure that the ledger balances for cash accounts fit the cash balance.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-371">Создание кассового отчета (только для Польши)</span><span class="sxs-lookup"><span data-stu-id="ddff3-371">Cash report creation (for Poland only)</span></span></td>
<td><span data-ttu-id="ddff3-372">Создайте отчет <strong>Касса</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-372">Create a <strong>Cash</strong> report.</span></span> <span data-ttu-id="ddff3-373">Номер отчета <strong>Касса</strong> создается на основе номерной серии, которая настроена для <strong>Номер отчета</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-373">The <strong>Cash</strong> report number is generated based on the number sequence that is set up for <strong>Report number</strong>.</span></span> <span data-ttu-id="ddff3-374">В диалоговом окне для задачи в поле <strong>До даты</strong> укажите последнюю даты, для которой проводки по кассе должны учитываться для отчета <strong>Касса</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-374">In the dialog box for the task, in the <strong>To date</strong>, specify the last date for which cash transactions should be counted for the <strong>Cash</strong> report.</span></span> <span data-ttu-id="ddff3-375">Используйте функцию <strong>Фильтр</strong> на вкладке <strong>Записи для добавления</strong>, чтобы указать дополнительные критерии для ограничения выбора кассовых проводок.</span><span class="sxs-lookup"><span data-stu-id="ddff3-375">Use the <strong>Filter</strong> function on the <strong>Records to include</strong> tab to specify additional criteria to limit the selection of cash transactions.</span></span> <span data-ttu-id="ddff3-376">Эти критерии могут включать номера кассовых счетов и коды валют.</span><span class="sxs-lookup"><span data-stu-id="ddff3-376">These criteria can include cash account numbers and currency codes.</span></span> <span data-ttu-id="ddff3-377">В поле <strong>Создать по</strong> выберите пользователя, ответственного за создание отчета.</span><span class="sxs-lookup"><span data-stu-id="ddff3-377">In the <strong>Create by</strong> field, select the user who is responsible for report creation.</span></span> <span data-ttu-id="ddff3-378">Для просмотра созданного отчета <strong>Касса</strong> используйте кнопку <strong>Кассовые отчеты</strong> на странице <strong>Кассовые счета</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-378">To view the <strong>Cash</strong> report that is created, use the <strong>Cash reports</strong> button on the <strong>Cash accounts</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddff3-379">Касса — Курсовая разница ФИФО и ЛИФО (только для Польши)</span><span class="sxs-lookup"><span data-stu-id="ddff3-379">Cash - Exchange adjustment FIFO and LIFO (for Poland only)</span></span></td>
<td><span data-ttu-id="ddff3-380">Расчет курсовой разницы по польским стандартам.</span><span class="sxs-lookup"><span data-stu-id="ddff3-380">Calculate the exchange adjustment per Polish standards.</span></span> <span data-ttu-id="ddff3-381">Используйте функцию <strong>Фильтр</strong> на вкладке <strong>Записи для добавления</strong>, чтобы указать кассовый счет, для которого требуется выполнить задачу.</span><span class="sxs-lookup"><span data-stu-id="ddff3-381">Use the <strong>Filter</strong> function on the <strong>Records to include</strong> tab to specify the cash account to run the task for.</span></span> <span data-ttu-id="ddff3-382">Установите флажок <strong>Пересчет</strong>, чтобы сделать полный перерасчет корректировки курсовой разницы для всех открытых периодов.</span><span class="sxs-lookup"><span data-stu-id="ddff3-382">Select the <strong>Recalculation</strong> check box to do a full recalculation of the exchange adjustment difference for all open periods.</span></span> <span data-ttu-id="ddff3-383">Ниже указан порядок расчета курсовой разницы при использовании методов ФИФО (первым пришел, первым ушел) и ЛИФО (последним пришел, первым ушел):</span><span class="sxs-lookup"><span data-stu-id="ddff3-383">Here is how the exchange adjustment is calculated when the first in, first out (FIFO) and last in, first out (LIFO) methods are used:</span></span>
<ul>
<li><span data-ttu-id="ddff3-384"><strong>Метод ФИФО</strong> — система выполняет поиск проводок расхода, которые имеют более раннюю дату проводки (меньший порядковый номер), и сопоставляет их с проводками прихода, которые имеют более раннюю дату проводки (меньший порядковый номер).</span><span class="sxs-lookup"><span data-stu-id="ddff3-384"><strong>FIFO method</strong> – The system searches for an expenditure transaction that has an earlier transaction date (smaller order number) and settles it with a receipt transaction that has an earlier transaction date (smaller order number).</span></span></li>
<li><span data-ttu-id="ddff3-385"><strong>Метод ЛИФО</strong> — система выполняет поиск проводок расхода, которые имеют более позднюю дату проводки (больший порядковый номер), и сопоставляет их с проводками прихода, которые имеют более позднюю дату проводки (больший порядковый номер).</span><span class="sxs-lookup"><span data-stu-id="ddff3-385"><strong>LIFO method</strong> – The system searches for an expenditure transaction that has a later transaction date (larger order number) and settles it with a receipt transaction that has a later transaction date (larger order number).</span></span></li>
</ul>
<span data-ttu-id="ddff3-386">Сопоставленная сумма отражается в поле <strong>Сопоставлено в валюте</strong> на странице <strong>Проводки по кассе</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-386">The settled amount is reflected in the <strong>Settled currency</strong> field on the <strong>Cash transaction</strong> page.</span></span> <span data-ttu-id="ddff3-387">Если имеется корректировка курсовой разницы, сумма отражается в поле <strong>Сумма курсовой разницы</strong>, и создается проводка с типом документа <strong>Курсовая разница</strong> в таблице <strong>Проводки по кассе</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-387">If there is an exchange adjustment difference, the amount is reflected in the <strong>Exchange adjustment amount</strong> field, and a transaction of the <strong>Exchange rate difference</strong> document type is generated in the <strong>Cash transaction</strong> table.</span></span> <span data-ttu-id="ddff3-388">Счета ГК для проводок прибылей/убытков задаются в таблице <strong>Валюта</strong> (<strong>Финансовая прибыль от курсовой разницы</strong> и <strong>Финансовый убыток от курсовой разницы</strong>).</span><span class="sxs-lookup"><span data-stu-id="ddff3-388">Ledger accounts for profit/loss transactions are set in the <strong>Currency</strong> table (<strong>Exchange rate financial profit</strong> and <strong>Exchange rate financial loss</strong>).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddff3-389">Переоценка в иностранной валюте — Касса</span><span class="sxs-lookup"><span data-stu-id="ddff3-389">Foreign currency revaluation - Cash</span></span></td>
<td><span data-ttu-id="ddff3-390">Используйте эту задачу, чтобы получить адекватное сальдо в валюте по умолчанию на дату отчетности, когда операции вводятся в иностранных валютах.</span><span class="sxs-lookup"><span data-stu-id="ddff3-390">Use this task to have an adequate balance in the default currency on the reporting date when the operations are entered in foreign currencies.</span></span> <span data-ttu-id="ddff3-391">Используйте функцию <strong>Фильтр</strong> на вкладке <strong>Записи для добавления</strong>, чтобы указать кассовый счет, для которого требуется выполнить задачу.</span><span class="sxs-lookup"><span data-stu-id="ddff3-391">Use the <strong>Filter</strong> function on the <strong>Records to include</strong> tab to specify the cash account to run the task for.</span></span> <span data-ttu-id="ddff3-392">В диалоговом окне для задачи используйте поля <strong>Из валюты</strong> и <strong>В валюту</strong>, чтобы указать валюты проводки.</span><span class="sxs-lookup"><span data-stu-id="ddff3-392">In the dialog box for the task, use the <strong>From currency</strong> and <strong>To Currency</strong> fields to specify transaction currencies.</span></span> <span data-ttu-id="ddff3-393">Система сравнивает сумму в валюте, которая была конвертирована с использованием валютного курса на выбранную дату, с суммой в валюте по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ddff3-393">The system compares the amount in the currency that was converted by using exchange rate on the selected date with the amount in the default currency.</span></span> <span data-ttu-id="ddff3-394">Разность этих сумм (за исключением предыдущей корректировки курсовой разницы) является рассчитанной курсовой разницей.</span><span class="sxs-lookup"><span data-stu-id="ddff3-394">The difference between the two amounts (excluding the previous exchange adjustment) is the calculated exchange adjustment.</span></span> <span data-ttu-id="ddff3-395">Эта задача создает утвержденную проводку по кассе типа <strong>Курсовая разница</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-395">This task creates an approved cash transaction of the <strong>Exchange adjustment</strong> type.</span></span> <span data-ttu-id="ddff3-396">Эта проводка ГК формируется с использованием счета учета для кассы и счета учета, который указан в пункте <strong>Внереализационная прибыль</strong> или <strong>Внереализационный убыток</strong> в таблице <strong>Валюта</strong>.</span><span class="sxs-lookup"><span data-stu-id="ddff3-396">The ledger transaction is formed by using the ledger account for cash and the ledger account that is specified in <strong>Unrealized profit</strong> or <strong>Unrealized loss</strong> in the <strong>Currency</strong> table.</span></span></td>
</tr>
</tbody>
</table>

## <a name="inquiries-and-reports"></a><span data-ttu-id="ddff3-397">Запросы и отчеты</span><span class="sxs-lookup"><span data-stu-id="ddff3-397">Inquiries and reports</span></span>

| <span data-ttu-id="ddff3-398">Запрос или отчет</span><span class="sxs-lookup"><span data-stu-id="ddff3-398">Inquiry or report</span></span>                             | <span data-ttu-id="ddff3-399">описание</span><span class="sxs-lookup"><span data-stu-id="ddff3-399">Description</span></span>                                                                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddff3-400">Просмотр проводок по кассе</span><span class="sxs-lookup"><span data-stu-id="ddff3-400">Cash transactions view</span></span>                        | <span data-ttu-id="ddff3-401">Для строки журнала ордеров используйте кнопку **Запросы** на панели действий для просмотра проводок по ГК, кассового сальдо и других сведений.</span><span class="sxs-lookup"><span data-stu-id="ddff3-401">For a Slip journal line, use the **Inquiries** button on the Action Pane to view ledger transactions, the cash balance, and other information.</span></span>                                                                                  |
| <span data-ttu-id="ddff3-402">Проводки по кассе</span><span class="sxs-lookup"><span data-stu-id="ddff3-402">Cash transaction</span></span>                              | <span data-ttu-id="ddff3-403">Выберите **Управление банком и кассовыми операциями** &gt; **Запросы и отчеты** &gt; **Проводки по кассе** для просмотра проводок по кассе.</span><span class="sxs-lookup"><span data-stu-id="ddff3-403">Go to **Cash and bank management** &gt; **Inquiries and reports** &gt; **Cash transactions** to view cash transactions.</span></span> <span data-ttu-id="ddff3-404">Используйте функцию **Фильтр**, чтобы указать дополнительные критерии для ограничения выбора кассовых проводок.</span><span class="sxs-lookup"><span data-stu-id="ddff3-404">Use the **Filter** function to specify additional criteria to limit the selection of cash transactions.</span></span> |
| <span data-ttu-id="ddff3-405">Журнал регистрации (для Эстонии и России)</span><span class="sxs-lookup"><span data-stu-id="ddff3-405">Journal of registration (for Estonia, Russia)</span></span> | <span data-ttu-id="ddff3-406">Отчет в пункте **Управление банком и кассовыми операциями** &gt; **Запросы и отчеты** &gt; **Журнал регистрации** отражает все приходных и расходные кассовые ордера, которые были выданы.</span><span class="sxs-lookup"><span data-stu-id="ddff3-406">The report at **Cash and bank management** &gt; **Inquiries and reports** &gt; **Journal of registration** reflects all cash reimbursement and cash disbursement slips that have been issued.</span></span>                                   |
| <span data-ttu-id="ddff3-407">Кассовая книга (для Латвии, Литвы, России)</span><span class="sxs-lookup"><span data-stu-id="ddff3-407">Cash book (for Latvia, Lithuania, Russia)</span></span>     | <span data-ttu-id="ddff3-408">Отчет в пункте **Управление банком и кассовыми операциями** &gt; **Запросы и отчеты** &gt; **Отчет по кассовой книге** отражает фактическое движение денежных средств (приходы и расходы).</span><span class="sxs-lookup"><span data-stu-id="ddff3-408">The report at **Cash and bank management** &gt; **Inquiries and reports** &gt; **Cash book report** reflects actual cash fund movements (receipts and expenditures).</span></span>                                                            |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]