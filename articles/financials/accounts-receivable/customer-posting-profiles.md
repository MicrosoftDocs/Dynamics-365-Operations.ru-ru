---
title: "Профили разноски по клиенту"
description: "Профили разноски клиента управляют разноской проводок клиента в ГК."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f246780a320f9a5e25ca423a099669a4f7e57bab
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---

# <a name="customer-posting-profiles"></a><span data-ttu-id="2a364-103">Профили разноски по клиенту</span><span class="sxs-lookup"><span data-stu-id="2a364-103">Customer posting profiles</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="2a364-104">Профили разноски клиента управляют разноской проводок клиента в ГК.</span><span class="sxs-lookup"><span data-stu-id="2a364-104">Customer posting profiles control the posting of customer transactions to the general ledger.</span></span>

<a name="customer-posting-profiles"></a><span data-ttu-id="2a364-105">Профили разноски по клиенту</span><span class="sxs-lookup"><span data-stu-id="2a364-105">Customer posting profiles</span></span>
-------------------------

<span data-ttu-id="2a364-106">Профили разноски клиентов позволяют назначить счета ГК и настройки документов всем клиентам, группе клиентов или отдельным клиентам.</span><span class="sxs-lookup"><span data-stu-id="2a364-106">Customer posting profiles enable you to assign general ledger accounts and document settings to all customers, a group of customers or a single customer.</span></span> <span data-ttu-id="2a364-107">Эти настройки будут использоваться для создания заказов на продажу, накладных с произвольным текстом, наличных платежей, писем-напоминаний и процент-нот.</span><span class="sxs-lookup"><span data-stu-id="2a364-107">These settings will be used when you create sales orders, free text invoices, cash payments, collection letters, and interest notes.</span></span> <span data-ttu-id="2a364-108">Для некоторых проводок можно выбрать профиль разноски, который отличается от профилей разноски, созданных для проводок на этой странице, и имеет преимущество по отношению к ним.</span><span class="sxs-lookup"><span data-stu-id="2a364-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> 

<span data-ttu-id="2a364-109">Профиль разноски по умолчанию определен на экспресс-вкладке "Главная книга и налог" на странице "Параметры расчетов с клиентами".</span><span class="sxs-lookup"><span data-stu-id="2a364-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts receivable parameters page.</span></span> <span data-ttu-id="2a364-110">После этого профиль разноски по умолчанию автоматически добавляется в заголовок новых документов, где его можно изменить на другой профиль разноски при необходимости.</span><span class="sxs-lookup"><span data-stu-id="2a364-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="2a364-111">Также можно связать определения разноски с типами разноски проводок на странице "Определения разноски проводок".</span><span class="sxs-lookup"><span data-stu-id="2a364-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="2a364-112">Определения разноски управляют разноской проводок клиента в ГК вместо профилей разноски.</span><span class="sxs-lookup"><span data-stu-id="2a364-112">Posting definitions control the posting of customer transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="2a364-113">Создание профиля разноски</span><span class="sxs-lookup"><span data-stu-id="2a364-113">Creating a posting profile</span></span>
<span data-ttu-id="2a364-114">Укажите счета ГК, используемые для разноски проводок с выбранным профилем разноски.</span><span class="sxs-lookup"><span data-stu-id="2a364-114">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="2a364-115">Выбор кода счета и там, где это возможно, счета или группы номеров для выбранного профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="2a364-115">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="2a364-116">В процессе разноски будет выполняться поиск наиболее подходящего профиля разноски для каждой проводки посредством поиска самого подходящего кода счета, номера счета или комбинации номеров и группы в соответствии со следующим приоритетом.</span><span class="sxs-lookup"><span data-stu-id="2a364-116">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="2a364-117">Значение поля **Код счета**</span><span class="sxs-lookup"><span data-stu-id="2a364-117">**Account code** field value</span></span> | <span data-ttu-id="2a364-118">Значение поля **Номер счета/группы**</span><span class="sxs-lookup"><span data-stu-id="2a364-118">**Account/Group number** field value</span></span>            | <span data-ttu-id="2a364-119">Приоритет поиска</span><span class="sxs-lookup"><span data-stu-id="2a364-119">Search priority</span></span> |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="2a364-120">**Таблица**</span><span class="sxs-lookup"><span data-stu-id="2a364-120">**Table**</span></span>                    | <span data-ttu-id="2a364-121">Определенный счет клиента</span><span class="sxs-lookup"><span data-stu-id="2a364-121">Specific customer account</span></span>                       | <span data-ttu-id="2a364-122">1</span><span class="sxs-lookup"><span data-stu-id="2a364-122">1</span></span>               |
| <span data-ttu-id="2a364-123">**Группа**</span><span class="sxs-lookup"><span data-stu-id="2a364-123">**Group**</span></span>                    | <span data-ttu-id="2a364-124">Группа клиентов, назначенная клиенту</span><span class="sxs-lookup"><span data-stu-id="2a364-124">Customer group that is assigned to the customer</span></span> | <span data-ttu-id="2a364-125">2</span><span class="sxs-lookup"><span data-stu-id="2a364-125">2</span></span>               |
| <span data-ttu-id="2a364-126">**Все**</span><span class="sxs-lookup"><span data-stu-id="2a364-126">**All**</span></span>                      | <span data-ttu-id="2a364-127">Пустой</span><span class="sxs-lookup"><span data-stu-id="2a364-127">Blank</span></span>                                           | <span data-ttu-id="2a364-128">3</span><span class="sxs-lookup"><span data-stu-id="2a364-128">3</span></span>               |

<span data-ttu-id="2a364-129">Если необходимо всем проводкам клиентов присвоить одинаковый профиль разноски, настройте только один профиль с указанием значения "Все" в поле "Код счета".</span><span class="sxs-lookup"><span data-stu-id="2a364-129">If you want all customer transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="2a364-130">Определите следующие значения, чтобы настроить профиль разноски:</span><span class="sxs-lookup"><span data-stu-id="2a364-130">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a364-131">Поле</span><span class="sxs-lookup"><span data-stu-id="2a364-131">Field</span></span></th>
<th><span data-ttu-id="2a364-132">Описание</span><span class="sxs-lookup"><span data-stu-id="2a364-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a364-133"><strong>Профиль разноски</strong></span><span class="sxs-lookup"><span data-stu-id="2a364-133"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="2a364-134">Код профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="2a364-134">Enter a code for the posting profile.</span></span> <span data-ttu-id="2a364-135">Например, можно создать два профиля разноски, чтобы получить один счет для сальдо клиента в национальной валюте, а другой — для сальдо клиента в иностранной валюте.</span><span class="sxs-lookup"><span data-stu-id="2a364-135">For example, you could create two posting profiles to obtain one account for customer balances in the national currency and another for customer balances in a foreign currency.</span></span> <span data-ttu-id="2a364-136">Первый счет можно назвать "Национальная", второй — "Иностранная".</span><span class="sxs-lookup"><span data-stu-id="2a364-136">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a364-137"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="2a364-137"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="2a364-138">Введите описание профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="2a364-138">Enter a description of the posting profile.</span></span> <span data-ttu-id="2a364-139">Этот параметр используется для более четкого определения профиля разноски при его просмотре на этой странице.</span><span class="sxs-lookup"><span data-stu-id="2a364-139">This is only used to better identify the posting profile when you view it in this page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a364-140"><strong>Код счета</strong></span><span class="sxs-lookup"><span data-stu-id="2a364-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="2a364-141">Укажите, будет ли профиль разноски применяться к одному клиенту, группе клиентов или всем клиентам.</span><span class="sxs-lookup"><span data-stu-id="2a364-141">Specify whether the posting profile applies to a single customer, a group of customers, or all customers:</span></span>
<ul>
<li><span data-ttu-id="2a364-142"><strong>Таблица</strong> — профиль разноски применяется к отдельному клиенту.</span><span class="sxs-lookup"><span data-stu-id="2a364-142"><strong>Table</strong> – The posting profile applies to a single customer.</span></span> <span data-ttu-id="2a364-143">Выберите счет клиента в поле "Номер счета/группы".</span><span class="sxs-lookup"><span data-stu-id="2a364-143">Select the customer account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="2a364-144"><strong>Группа</strong> — профиль разноски применяется к группе клиентов.</span><span class="sxs-lookup"><span data-stu-id="2a364-144"><strong>Group</strong> – The posting profile applies to a customer group.</span></span> <span data-ttu-id="2a364-145">Выберите группу клиентов в поле "Номер счета/группы".</span><span class="sxs-lookup"><span data-stu-id="2a364-145">Select the customer group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="2a364-146"><strong>Все</strong> — профиль разноски применяется ко всем клиентам.</span><span class="sxs-lookup"><span data-stu-id="2a364-146"><strong>All</strong> – The posting profile applies to all customers.</span></span> <span data-ttu-id="2a364-147">Оставьте поле "Номер счета/группы" пустым.</span><span class="sxs-lookup"><span data-stu-id="2a364-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a364-148"><strong>Номер счета/группы</strong></span><span class="sxs-lookup"><span data-stu-id="2a364-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="2a364-149">Если в поле "Код счета" выбрано значение "Все", выберите номер счета клиента, связанного с данным профилем разноски.</span><span class="sxs-lookup"><span data-stu-id="2a364-149">If Table is selected in the Account code field, select the account number of the customer who is associated with the posting profile.</span></span> <span data-ttu-id="2a364-150">Если выбрано значение "Группа", выберите группу клиентов.</span><span class="sxs-lookup"><span data-stu-id="2a364-150">If Group is selected, select the customer group.</span></span> <span data-ttu-id="2a364-151">Если выбрано значение "Все", в поле ничего вводить не нужно.</span><span class="sxs-lookup"><span data-stu-id="2a364-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a364-152"><strong>Суммарный счет</strong></span><span class="sxs-lookup"><span data-stu-id="2a364-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="2a364-153">Выберите счет ГК для использования в качестве итогового счета клиента для клиентов, связанных с данным профилем разноски.</span><span class="sxs-lookup"><span data-stu-id="2a364-153">Select the ledger account that will be used as the customer summary account for the customers who are associated with the posting profile.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a364-154"><strong>Закрытие счета</strong></span><span class="sxs-lookup"><span data-stu-id="2a364-154"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="2a364-155">Выберите счет ГК денежных средств, используемый для прогнозов движения денежных средств.</span><span class="sxs-lookup"><span data-stu-id="2a364-155">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="2a364-156">Это поле отображается, только если включены прогнозы движения денежных средств.</span><span class="sxs-lookup"><span data-stu-id="2a364-156">This field will only appear if cash flow forecasts are enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a364-157"><strong>Счет налога по предоплате</strong></span><span class="sxs-lookup"><span data-stu-id="2a364-157"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="2a364-158">Выберите счет налога для платежей предоплаты.</span><span class="sxs-lookup"><span data-stu-id="2a364-158">Select the account for sales tax for payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Заметка" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="2a364-160"><strong>Примечание</strong></span><span class="sxs-lookup"><span data-stu-id="2a364-160"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a364-161">Используйте страницу "Параметры расчетов с клиентами", чтобы указать профиль разноски для использования, если платеж помечен как предоплата.</span><span class="sxs-lookup"><span data-stu-id="2a364-161">Use the Accounts receivable parameters page to specify the posting profile to use when a payment is marked as a prepayment.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a364-162"><strong>Счет задолженности по дисконту</strong></span><span class="sxs-lookup"><span data-stu-id="2a364-162"><strong>Liabilities for discount account</strong></span></span></td>
<td><span data-ttu-id="2a364-163">Выберите счет ГК для обязательств по скидкам.</span><span class="sxs-lookup"><span data-stu-id="2a364-163">Select the ledger account for liabilities of discount.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a364-164"><strong>Серия писем-напоминаний</strong></span><span class="sxs-lookup"><span data-stu-id="2a364-164"><strong>Collection letter sequence</strong></span></span></td>
<td><span data-ttu-id="2a364-165">Выберите код последовательности писем-напоминаний для использования для клиентов, которым назначен профиль разноски.</span><span class="sxs-lookup"><span data-stu-id="2a364-165">Select the identifier of the collection letter sequence to use for customers to whom the posting profile is assigned.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a364-166"><strong>Код процента</strong></span><span class="sxs-lookup"><span data-stu-id="2a364-166"><strong>Interest code</strong></span></span></td>
<td><span data-ttu-id="2a364-167">Выберите код процента для расчета процента для клиентов, которым назначен профиль разноски.</span><span class="sxs-lookup"><span data-stu-id="2a364-167">Select the interest code to use for the calculation of interest for customers to whom the posting profile is assigned.</span></span></td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a><span data-ttu-id="2a364-168">**Табличные ограничения**</span><span class="sxs-lookup"><span data-stu-id="2a364-168">**Table restrictions**</span></span>

<span data-ttu-id="2a364-169">Для проводок с выбранным профилем разноски укажите, будут ли проводки сопоставляться автоматически, будет ли рассчитываться процент и будут ли отправляться письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="2a364-169">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="2a364-170">Также можно выбрать счет, используемый при закрытии проводок с выбранным профилем разноски.</span><span class="sxs-lookup"><span data-stu-id="2a364-170">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="2a364-171">Определите следующие значения, чтобы настроить профиль разноски:</span><span class="sxs-lookup"><span data-stu-id="2a364-171">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="2a364-172">Поле</span><span class="sxs-lookup"><span data-stu-id="2a364-172">Field</span></span>                 | <span data-ttu-id="2a364-173">Описание</span><span class="sxs-lookup"><span data-stu-id="2a364-173">Description</span></span>                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a364-174">**Сопоставление**</span><span class="sxs-lookup"><span data-stu-id="2a364-174">**Settlement**</span></span>        | <span data-ttu-id="2a364-175">Используйте этот переключатель, чтобы включить автоматическое сопоставление проводок с этим профилем разноски.</span><span class="sxs-lookup"><span data-stu-id="2a364-175">Select this toggle to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="2a364-176">Если этот переключатель не установлен, необходимо вручную сопоставить проводки на странице "Сопоставление открытых проводок" или на странице "Ввод платежей клиента".</span><span class="sxs-lookup"><span data-stu-id="2a364-176">If this toggle is cleared, you must manually settle transactions by using the Settle open transactions page or the Enter customer payments page.</span></span> |
| <span data-ttu-id="2a364-177">**Процент**</span><span class="sxs-lookup"><span data-stu-id="2a364-177">**Interest**</span></span>          | <span data-ttu-id="2a364-178">Установите этот переключатель, если следует рассчитывать процент по остаточным сальдо для счетов клиентов с этим профилем.</span><span class="sxs-lookup"><span data-stu-id="2a364-178">Select this toggle if interest should be calculated on outstanding balances for customer accounts that use this profile.</span></span> <span data-ttu-id="2a364-179">Если этот переключатель не установлен, процент не будет рассчитываться для этих клиентов.</span><span class="sxs-lookup"><span data-stu-id="2a364-179">If this toggle is cleared, interest will not be calculated for these customers.</span></span>                                           |
| <span data-ttu-id="2a364-180">**Письмо-напоминание**</span><span class="sxs-lookup"><span data-stu-id="2a364-180">**Collection letter**</span></span> | <span data-ttu-id="2a364-181">Установите этот переключатель, если следует создавать письма-напоминания для счетов клиентов с этим профилем.</span><span class="sxs-lookup"><span data-stu-id="2a364-181">Select this toggle if collection letters should be generated for customer accounts that use this profile.</span></span> <span data-ttu-id="2a364-182">Если этот переключатель не установлен, письма-напоминания не будут создаваться для этих клиентов.</span><span class="sxs-lookup"><span data-stu-id="2a364-182">If this toggle is cleared, collection letters will not be generated for these customers.</span></span>                                                 |
| <span data-ttu-id="2a364-183">**Закрыть**</span><span class="sxs-lookup"><span data-stu-id="2a364-183">**Close**</span></span>             | <span data-ttu-id="2a364-184">Выберите профиль разноски, на который нужно переключиться после закрытия проводок с этим профилем разноски.</span><span class="sxs-lookup"><span data-stu-id="2a364-184">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="2a364-185">Проводка считается закрытой, если она полностью сопоставлена.</span><span class="sxs-lookup"><span data-stu-id="2a364-185">A transaction is regarded as closed when it has been settled in full.</span></span>                                                                           |



<span data-ttu-id="2a364-186">Дополнительные сведения см. в разделе [Обзор платежей клиентов](../cash-bank-management/tasks/customer-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2a364-186">For more information, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>


