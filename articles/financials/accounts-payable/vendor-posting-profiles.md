---
title: Профили разноски по поставщикам
description: Профили разноски поставщика управляют разноской проводок поставщика в главную книгу.
author: abruer
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e81f8b472e7ac7578c184716dcb4e5f3d7aeb65d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1512176"
---
# <a name="vendor-posting-profiles"></a><span data-ttu-id="02386-103">Профили разноски по поставщикам</span><span class="sxs-lookup"><span data-stu-id="02386-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02386-104">Профили разноски поставщика управляют разноской проводок поставщика в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="02386-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="02386-105">Профили разноски по поставщикам</span><span class="sxs-lookup"><span data-stu-id="02386-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="02386-106">Профили разноски поставщиков позволяют назначить счета ГК и настройки документов всем поставщикам, группе поставщиков или отдельным поставщикам.</span><span class="sxs-lookup"><span data-stu-id="02386-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors or a single vendor.</span></span> <span data-ttu-id="02386-107">Эти настройки будут использоваться при создании заказов на покупку, накладных поставщиков и наличных платежей.</span><span class="sxs-lookup"><span data-stu-id="02386-107">These settings will be used when you create purchase orders, vendor invoices and cash payments.</span></span> <span data-ttu-id="02386-108">Для некоторых проводок можно выбрать профиль разноски, который отличается от профилей разноски, созданных для проводок на этой странице, и имеет преимущество по отношению к ним.</span><span class="sxs-lookup"><span data-stu-id="02386-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> <span data-ttu-id="02386-109">Профиль разноски по умолчанию определен на экспресс-вкладке "Главная книга и налог" на странице "Параметры расчетов с поставщиками".</span><span class="sxs-lookup"><span data-stu-id="02386-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts payable parameters page.</span></span> <span data-ttu-id="02386-110">После этого профиль разноски по умолчанию автоматически добавляется в заголовок новых документов, где его можно изменить на другой профиль разноски при необходимости.</span><span class="sxs-lookup"><span data-stu-id="02386-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="02386-111">Также можно связать определения разноски с типами разноски проводок на странице "Определения разноски проводок".</span><span class="sxs-lookup"><span data-stu-id="02386-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="02386-112">Определения разноски управляют разноской проводок поставщика в ГК вместо профилей разноски.</span><span class="sxs-lookup"><span data-stu-id="02386-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="02386-113">Создание профиля разноски</span><span class="sxs-lookup"><span data-stu-id="02386-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="02386-114">**Настройка**</span><span class="sxs-lookup"><span data-stu-id="02386-114">**Setup**</span></span>

<span data-ttu-id="02386-115">Укажите счета ГК, используемые для разноски проводок с выбранным профилем разноски.</span><span class="sxs-lookup"><span data-stu-id="02386-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="02386-116">Выбор кода счета и там, где это возможно, счета или группы номеров для выбранного профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="02386-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="02386-117">В процессе разноски будет выполняться поиск наиболее подходящего профиля разноски для каждой проводки посредством поиска самого подходящего кода счета, номера счета или комбинации номеров и группы в соответствии со следующим приоритетом.</span><span class="sxs-lookup"><span data-stu-id="02386-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="02386-118">Значение поля **Код счета**</span><span class="sxs-lookup"><span data-stu-id="02386-118">**Account code** field value</span></span> | <span data-ttu-id="02386-119">Значение поля **Номер счета/группы**</span><span class="sxs-lookup"><span data-stu-id="02386-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="02386-120">Приоритет поиска</span><span class="sxs-lookup"><span data-stu-id="02386-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="02386-121">**Таблица**</span><span class="sxs-lookup"><span data-stu-id="02386-121">**Table**</span></span>                    | <span data-ttu-id="02386-122">Определенный счет поставщика</span><span class="sxs-lookup"><span data-stu-id="02386-122">Specific vendor account</span></span>                     | <span data-ttu-id="02386-123">1</span><span class="sxs-lookup"><span data-stu-id="02386-123">1</span></span>               |
| <span data-ttu-id="02386-124">**Группа**</span><span class="sxs-lookup"><span data-stu-id="02386-124">**Group**</span></span>                    | <span data-ttu-id="02386-125">Группа поставщиков, назначенная поставщику</span><span class="sxs-lookup"><span data-stu-id="02386-125">vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="02386-126">2</span><span class="sxs-lookup"><span data-stu-id="02386-126">2</span></span>               |
| <span data-ttu-id="02386-127">**Все**</span><span class="sxs-lookup"><span data-stu-id="02386-127">**All**</span></span>                      | <span data-ttu-id="02386-128">Пустой</span><span class="sxs-lookup"><span data-stu-id="02386-128">Blank</span></span>                                       | <span data-ttu-id="02386-129">3</span><span class="sxs-lookup"><span data-stu-id="02386-129">3</span></span>               |

<span data-ttu-id="02386-130">Если необходимо всем проводкам поставщиков присвоить одинаковый профиль разноски, настройте только один профиль с указанием значения "Все" в поле "Код счета".</span><span class="sxs-lookup"><span data-stu-id="02386-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="02386-131">Определите следующие значения, чтобы настроить профиль разноски:</span><span class="sxs-lookup"><span data-stu-id="02386-131">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="02386-132">Поле</span><span class="sxs-lookup"><span data-stu-id="02386-132">Field</span></span></th>
<th><span data-ttu-id="02386-133">Описание</span><span class="sxs-lookup"><span data-stu-id="02386-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02386-134"><strong>Профиль разноски</strong></span><span class="sxs-lookup"><span data-stu-id="02386-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="02386-135">Код профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="02386-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="02386-136">Например, можно создать два профиля разноски, чтобы получить один счет для сальдо поставщика в национальной валюте, а другой — для сальдо поставщика в иностранной валюте.</span><span class="sxs-lookup"><span data-stu-id="02386-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="02386-137">Первый счет можно назвать "Национальная", второй — "Иностранная".</span><span class="sxs-lookup"><span data-stu-id="02386-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02386-138"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="02386-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="02386-139">Введите описание профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="02386-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02386-140"><strong>Код счета</strong></span><span class="sxs-lookup"><span data-stu-id="02386-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="02386-141">Укажите, будет ли профиль разноски применяться к одному поставщику, группе поставщиков или всем поставщикам:</span><span class="sxs-lookup"><span data-stu-id="02386-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="02386-142"><strong>Таблица</strong> — профиль разноски применяется к отдельному поставщику.</span><span class="sxs-lookup"><span data-stu-id="02386-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="02386-143">Выберите счет поставщика в поле "Номер счета/группы".</span><span class="sxs-lookup"><span data-stu-id="02386-143">Select the vendor account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="02386-144"><strong>Группа</strong> — профиль разноски применяется к группе поставщиков.</span><span class="sxs-lookup"><span data-stu-id="02386-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="02386-145">Выберите группу поставщиков в поле "Номер счета/группы".</span><span class="sxs-lookup"><span data-stu-id="02386-145">Select the vendor group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="02386-146"><strong>Все</strong> — профиль разноски применяется ко всем поставщикам.</span><span class="sxs-lookup"><span data-stu-id="02386-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="02386-147">Оставьте поле "Номер счета/группы" пустым.</span><span class="sxs-lookup"><span data-stu-id="02386-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02386-148"><strong>Номер счета/группы</strong></span><span class="sxs-lookup"><span data-stu-id="02386-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="02386-149">Если в поле "Код счета" выбрано значение "Все", выберите номер счета поставщика, связанного с данным профилем разноски.</span><span class="sxs-lookup"><span data-stu-id="02386-149">If Table is selected in the Account code field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="02386-150">Если выбран параметр "Группа", укажите группу поставщиков.</span><span class="sxs-lookup"><span data-stu-id="02386-150">If Group is selected, select a vendor group.</span></span> <span data-ttu-id="02386-151">Если выбрано значение "Все", в поле ничего вводить не нужно.</span><span class="sxs-lookup"><span data-stu-id="02386-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02386-152"><strong>Суммарный счет</strong></span><span class="sxs-lookup"><span data-stu-id="02386-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="02386-153">Выберите счет ГК для использования в качестве итогового счета поставщиков, с которым связан профиль разноски.</span><span class="sxs-lookup"><span data-stu-id="02386-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Заметка" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="02386-155"><strong>Примечание</strong></span><span class="sxs-lookup"><span data-stu-id="02386-155"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02386-156">Если переключатель "Использовать определения разносок" установлен на странице "Параметры главной книги", определение разноски проводки для накладных поставщика используется вместо итогового счета.</span><span class="sxs-lookup"><span data-stu-id="02386-156">If the Use posting definitions toggle is selected in the General ledger parameters page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02386-157"><strong>Закрытие счета</strong></span><span class="sxs-lookup"><span data-stu-id="02386-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="02386-158">Выберите счет ГК денежных средств, используемый для прогнозов движения денежных средств.</span><span class="sxs-lookup"><span data-stu-id="02386-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="02386-159">Это поле доступно, только если включен прогноз движения денежных средств.</span><span class="sxs-lookup"><span data-stu-id="02386-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02386-160"><strong>Счет налога по предоплате</strong></span><span class="sxs-lookup"><span data-stu-id="02386-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="02386-161">Выберите счет налога для платежей предоплаты.</span><span class="sxs-lookup"><span data-stu-id="02386-161">Select the account for sales tax payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Заметка" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="02386-163"><strong>Примечание</strong></span><span class="sxs-lookup"><span data-stu-id="02386-163"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02386-164">Профиль разноски, который используется, когда платеж помечен как предоплата, выбирается в поле "Профиль разноски с ваучером журнала предоплат" в главной книге и области налога на странице "Параметры расчетов с поставщиками".</span><span class="sxs-lookup"><span data-stu-id="02386-164">The posting profile that is used when the payment is marked as a prepayment is selected in the Posting profile with prepayment journal voucher field in the Ledger and sales tax area of the Accounts payable parameters page.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02386-165"><strong>Прибытие</strong></span><span class="sxs-lookup"><span data-stu-id="02386-165"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="02386-166">Выберите счет ГК, на который разносятся сведения о неутвержденных накладных поставщика.</span><span class="sxs-lookup"><span data-stu-id="02386-166">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="02386-167">Эти сведения вводятся в журнале регистрации накладных.</span><span class="sxs-lookup"><span data-stu-id="02386-167">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="02386-168">Например, пользователь вводит основные сведения о накладных поставщика по мере их приемки в журнале регистрации накладных.</span><span class="sxs-lookup"><span data-stu-id="02386-168">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="02386-169">Если регистр накладных разнесен, проводки разносятся на счет, введенный здесь и в поле "Корр. счет".</span><span class="sxs-lookup"><span data-stu-id="02386-169">When the invoice register is posted, the transactions are posted to the account that is entered here and in the Offset account field.</span></span> <span data-ttu-id="02386-170">После утверждения накладных этот долг переносится со счета "Прибытие" на итоговый счет поставщика.</span><span class="sxs-lookup"><span data-stu-id="02386-170">When the invoices are approved, the debt is transferred from the Arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02386-171"><strong>Корр. счет</strong></span><span class="sxs-lookup"><span data-stu-id="02386-171"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="02386-172">Выберите счет ГК, который используется для корректировки неутвержденных накладных поставщика, обновленных с помощью регистра накладных.</span><span class="sxs-lookup"><span data-stu-id="02386-172">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="02386-173">Корр. счет выступает в роли корр. счета для проводок, разнесенных на счета прибытия.</span><span class="sxs-lookup"><span data-stu-id="02386-173">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="02386-174">Поэтому счет содержит покупки поставщика, которые еще не были утверждены.</span><span class="sxs-lookup"><span data-stu-id="02386-174">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="02386-175">**Табличные ограничения**</span><span class="sxs-lookup"><span data-stu-id="02386-175">**Table restrictions**</span></span>

<span data-ttu-id="02386-176">Для проводок с выбранным профилем разноски укажите, будут ли проводки сопоставляться автоматически, будет ли рассчитываться процент и будут ли отправляться письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="02386-176">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="02386-177">Также можно выбрать счет, используемый при закрытии проводок с выбранным профилем разноски.</span><span class="sxs-lookup"><span data-stu-id="02386-177">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="02386-178">Определите следующие значения, чтобы настроить профиль разноски:</span><span class="sxs-lookup"><span data-stu-id="02386-178">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="02386-179">Поле</span><span class="sxs-lookup"><span data-stu-id="02386-179">Field</span></span>          | <span data-ttu-id="02386-180">Описание</span><span class="sxs-lookup"><span data-stu-id="02386-180">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02386-181">**Сопоставление**</span><span class="sxs-lookup"><span data-stu-id="02386-181">**Settlement**</span></span> | <span data-ttu-id="02386-182">Используйте этот параметр, чтобы включить автоматическое сопоставление проводок с этим профилем разноски.</span><span class="sxs-lookup"><span data-stu-id="02386-182">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="02386-183">Если этот параметр не выбран, необходимо вручную сопоставить проводки на странице "Сопоставление открытых проводок".</span><span class="sxs-lookup"><span data-stu-id="02386-183">If this option is cleared, you must manually settle transactions by using the Settle open transactions page.</span></span> |
| <span data-ttu-id="02386-184">**Отменить**</span><span class="sxs-lookup"><span data-stu-id="02386-184">**Cancel**</span></span>     | <span data-ttu-id="02386-185">Используйте этот параметр, если требуется иметь возможность отменить проводки с этим профилем разноски.</span><span class="sxs-lookup"><span data-stu-id="02386-185">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="02386-186">**Закрыть**</span><span class="sxs-lookup"><span data-stu-id="02386-186">**Close**</span></span>      | <span data-ttu-id="02386-187">Выберите профиль разноски, на который нужно переключиться после закрытия проводок с этим профилем разноски.</span><span class="sxs-lookup"><span data-stu-id="02386-187">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="02386-188">Проводка считается закрытой, если она полностью сопоставлена.</span><span class="sxs-lookup"><span data-stu-id="02386-188">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |





