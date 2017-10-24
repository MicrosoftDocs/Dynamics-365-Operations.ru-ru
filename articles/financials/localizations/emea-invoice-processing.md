---
title: "Обработка накладных"
description: "В этой теме приведена информация об обработке накладных для Восточной Европы."
author: v-kikozl
manager: AnnBe
ms.date: 07/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations, Core
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-kikozl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Enterprise edition, July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e37b318e365c346a31397cadc81e79285cfa2106
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="invoice-processing"></a><span data-ttu-id="3b474-103">Обработка накладных</span><span class="sxs-lookup"><span data-stu-id="3b474-103">Invoice processing</span></span>

<span data-ttu-id="3b474-104">В этой теме кратко описаны некоторые сценарии, характерные для конкретных стран, такие как внутренний налог на добавленную стоимость (НДС) и отложенный налог.</span><span class="sxs-lookup"><span data-stu-id="3b474-104">This topic briefly describes some country-specific scenarios, such as intra-community value-added tax (VAT) and deferred tax.</span></span> <span data-ttu-id="3b474-105">Требования законодательства в некоторых странах Европы влияют на процесс обработки накладных.</span><span class="sxs-lookup"><span data-stu-id="3b474-105">Legal requirements for some European countries affect the invoicing process.</span></span> <span data-ttu-id="3b474-106">В этой теме также приводятся сведения о том, как в этих странах происходит обработка накладных клиента и накладных поставщика.</span><span class="sxs-lookup"><span data-stu-id="3b474-106">This topic provides also an information about how customer and vendor invoices are processed for these countries.</span></span> 
<table>
<thead>
<tr>
<th><span data-ttu-id="3b474-107">Сценарий</span><span class="sxs-lookup"><span data-stu-id="3b474-107">Scenario</span></span></th>
<th><span data-ttu-id="3b474-108">Страны</span><span class="sxs-lookup"><span data-stu-id="3b474-108">Countries</span></span></th>
<th><span data-ttu-id="3b474-109">Описание изменений в функциональности</span><span class="sxs-lookup"><span data-stu-id="3b474-109">Description of the functionality changes</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3b474-110"> Даты по расчетам с клиентами и расчетам с поставщиками для НДС</span><span class="sxs-lookup"><span data-stu-id="3b474-110">Accounts receivable and Accounts payable dates for VAT</span></span></td>
<td><span data-ttu-id="3b474-111">Чешская Республика, Польша</span><span class="sxs-lookup"><span data-stu-id="3b474-111">Czech Republic, Poland</span></span></td>
<td>
<p><span data-ttu-id="3b474-112">При покупке товаров в странах Европейского Союза (ЕС) существует обязательство по самостоятельной оценке НДС:</span><span class="sxs-lookup"><span data-stu-id="3b474-112">When goods are purchased from European Union (EU) countries, there is an obligation of self-assessment of VAT:</span></span></p>
<ul>
<li><span data-ttu-id="3b474-113">Исходящий НДС должен уплачиваться в том периоде НДС, в которой была выставлена накладная (дата документа).</span><span class="sxs-lookup"><span data-stu-id="3b474-113">The output VAT must be paid in a VAT period where the invoice was issued (document date).</span></span></li>
<li><span data-ttu-id="3b474-114">Входящий НДС не может быть вычтен до поступления документа (дата регистрации НДС).</span><span class="sxs-lookup"><span data-stu-id="3b474-114">The input VAT can’t be deducted before the document receipt (VAT register date).</span></span></li>
</ul>
<p><span data-ttu-id="3b474-115">Для поддержки этого сценария следует настроить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="3b474-115">The following settings should be configured to support this scenario:</span></span></p>
<ul>
<li><span data-ttu-id="3b474-116">На странице <strong>Параметры модуля расчетов с поставщиками</strong> включите параметры <strong>Внутренний НДС (ЕС)</strong> и <strong>Дата документа для внутреннего НДС (ЕС)</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b474-116">On the <strong>Accounts payable parameters</strong> page, enable the <strong>Intra-community VAT</strong> and <strong>Document date for intra-community VAT</strong> parameters.</span></span></li>
<li><span data-ttu-id="3b474-117">Настройте две налоговых кода, один с положительным процентом налога и один с отрицательным процентом налога.</span><span class="sxs-lookup"><span data-stu-id="3b474-117">Set up two sales tax codes, one that has a positive sales tax percentage and one that has a negative sales tax percentage.</span></span></li>
<li><span data-ttu-id="3b474-118">Настройте налоговую группу, которая включает в себя и положительный, и отрицательный налоговый код.</span><span class="sxs-lookup"><span data-stu-id="3b474-118">Set up a sales tax group that includes both the positive and negative sales tax codes.</span></span> <span data-ttu-id="3b474-119">Для отрицательного налогового кода задайте для параметра <strong>Внутренний НДС (ЕС)</strong> значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b474-119">For the negative sales tax code, set the <strong>Intracommunity VAT</strong> parameter to <strong>Yes</strong>.</span></span></li>
</ul>
<p><span data-ttu-id="3b474-120">После успешной настройки у покупок будет две разнесенные налоговые проводки:</span><span class="sxs-lookup"><span data-stu-id="3b474-120">After successful setup, purchases will have two posted sales tax transactions:</span></span></p>
<ul>
<li><span data-ttu-id="3b474-121">Положительная проводка с направлением <strong>налог к получению</strong> и датой регистрации НДС, равной дате со страницы разноски накладной.</span><span class="sxs-lookup"><span data-stu-id="3b474-121">A positive transaction that has a direction of <strong>sales tax receivable</strong> and a VAT register date that equals the date from the invoice posting page.</span></span></li>
<li><span data-ttu-id="3b474-122">Отрицательная проводка с направлением <strong>налог к уплате</strong> и датой регистрации НДС, равной дате документа.</span><span class="sxs-lookup"><span data-stu-id="3b474-122">A negative transaction that has a direction of <strong>sales tax payable</strong> and a VAT register date that equals the document date.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="3b474-123">Изменение даты документа продажи.</span><span class="sxs-lookup"><span data-stu-id="3b474-123">Modify a sales document date.</span></span></td>
<td><span data-ttu-id="3b474-124">Все страны Восточной Европы</span><span class="sxs-lookup"><span data-stu-id="3b474-124">All Eastern European countries</span></span></td>
<td><p><span data-ttu-id="3b474-125">Поле <strong>Дата документа</strong> в накладной по проекту можно изменить.</span><span class="sxs-lookup"><span data-stu-id="3b474-125">You can modify the <strong>Document date</strong> field on a project invoice.</span></span> <span data-ttu-id="3b474-126">Эта дата присутствует на напечатанной накладной.</span><span class="sxs-lookup"><span data-stu-id="3b474-126">This date appears on the printed invoice.</span></span></p>
<p><span data-ttu-id="3b474-127">Поле <strong>Дата документа</strong> также есть на страницах <strong>Разноска накладной</strong> и <strong>Накладная с произвольным текстом</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b474-127">There is also a <strong>Document date</strong> field on the <strong>Posting invoice</strong> and <strong>Free text invoice</strong> pages.</span></span> <span data-ttu-id="3b474-128">После разноски накладной дата документа отображается в заголовке накладной.</span><span class="sxs-lookup"><span data-stu-id="3b474-128">After you post an invoice, the document date appears on the invoice header.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="3b474-129">Дата документа для валютных курсов</span><span class="sxs-lookup"><span data-stu-id="3b474-129">Document date for exchange rates</span></span></td>
<td><span data-ttu-id="3b474-130">Польша, Венгрия, Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="3b474-130">Poland, Hungary, Czech Republic</span></span></td>
<td>
<p><span data-ttu-id="3b474-131">Законодательство предусматривает различные правила для выбора действительных валютных курсов для бизнес-транзакций.</span><span class="sxs-lookup"><span data-stu-id="3b474-131">Legislation provides different rules for selecting valid exchange rates for business transactions.</span></span> <span data-ttu-id="3b474-132">В поле <strong>Дата валютного курса</strong> на страницах <strong>Параметры модуля расчетов с клиентами</strong> и <strong>Параметры модуля расчетов с поставщиками</strong> можно выбрать дату, которая должна использоваться для сумм в расчете валюты учета в документах покупки и продажи.</span><span class="sxs-lookup"><span data-stu-id="3b474-132">In the <strong>Exchange rate date</strong> field on the <strong>Accounts receivable parameters</strong> and <strong>Accounts payable parameters</strong> pages, you can select the date that should be used for amounts in the accounting currency calculation on purchase and sales documents.</span></span> <span data-ttu-id="3b474-133">При вводе данных система извлекает валютный курс для проводки на основании этого параметра.</span><span class="sxs-lookup"><span data-stu-id="3b474-133">During data entry, the system retrieves the exchange rate for the transaction, based on this parameter.</span></span></p>
<blockquote>[!NOTE]<br><span data-ttu-id="3b474-134">При выборе в поле <strong>Дата валютного курса</strong> значения <strong>Дата документа (только для торговли ЕС)</strong> система использует налоговую группу.</span><span class="sxs-lookup"><span data-stu-id="3b474-134">When you set the <strong>Exchange rate date</strong> field to <strong>Document date (for EU trade only)</strong>, the system uses the sales tax group.</span></span> <span data-ttu-id="3b474-135">Для налоговой группы существует параметр <strong>Торговля ЕС</strong> на вкладке <strong>Общие</strong>. Если параметр <strong>Торговля ЕС</strong> для налоговой группы имеет значение <strong>Да</strong> и если налоговая группа присутствует в заголовке документа, система извлекает валютный курс на основании даты документа.</span><span class="sxs-lookup"><span data-stu-id="3b474-135">For the sales tax group, there is a <strong>EU trade</strong> parameter on the <strong>General</strong> tab. If the <strong>EU trade</strong> option is set to <strong>Yes</strong> for the sales tax group, and if this sales tax group exists on the header of the document, the system retrieves the exchange rate based on the document date.</span></span> <span data-ttu-id="3b474-136">Если параметр <strong>Торговля ЕС</strong> для этой налоговой группы имеет значение <strong>Нет</strong>, система извлекает валютный курс на основании даты разноски документа.</span><span class="sxs-lookup"><span data-stu-id="3b474-136">If the <strong>EU trade</strong> option is set to <strong>No</strong> for this sales tax group, the system retrieves the exchange rate based on the posting date of the document.</span></span></blockquote>
</td>
</tr>
<tr>
<td><span data-ttu-id="3b474-137">Даты торговли, даты регистрации НДС и контроль даты документа и НДС</span><span class="sxs-lookup"><span data-stu-id="3b474-137">Trade dates, VAT register dates, and document and VAT date control</span></span></td>
<td><span data-ttu-id="3b474-138">Польша, Венгрия, Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="3b474-138">Poland, Hungary, Czech Republic</span></span></td>
<td>
<p><span data-ttu-id="3b474-139">Дата продажи и дата поступления документа являются обязательными для отчетности по НДС:</span><span class="sxs-lookup"><span data-stu-id="3b474-139">The sales date and the document receipt date are required for VAT reporting:</span></span></p>
<ul>
<li><span data-ttu-id="3b474-140">Дата продажи — это дата выполнения проводки в модуле "Расчеты с клиентами".</span><span class="sxs-lookup"><span data-stu-id="3b474-140">The sales date is the fulfilment date of the transaction in Accounts receivable.</span></span></li>
<li><span data-ttu-id="3b474-141">Дата поступления документа — это дата, которая демонстрирует право требовать вычета НДС в модуле "Расчеты с поставщиками".</span><span class="sxs-lookup"><span data-stu-id="3b474-141">The document receipt date is a date that demonstrates the rights to claim a VAT deduction in Accounts payable.</span></span> <span data-ttu-id="3b474-142">Каждый полученный документ имеет дату для целей аудита.</span><span class="sxs-lookup"><span data-stu-id="3b474-142">Each document that is received has a date for audit purposes.</span></span></li>
</ul>
<p><span data-ttu-id="3b474-143">Венгерская функциональность для крайних сроков, чешская функциональность для дат выполнения и польская функциональность для даты регистрации НДС включают в себя требование о налоговой отчетности на основании даты, отличной от даты разноски.</span><span class="sxs-lookup"><span data-stu-id="3b474-143">The Hungarian functionality for date deadlines, the Czech Republic functionality for fulfill dates, and the Polish functionality for the VAT register date include the requirement for tax information reporting that is based on a date that differs from the posting date.</span></span></p>
<p><span data-ttu-id="3b474-144">Поле <strong>Дата регистра НДС</strong> поддерживает это требование и присутствует более чем на 20 страницах.</span><span class="sxs-lookup"><span data-stu-id="3b474-144">The <strong>Date of VAT register</strong> field supports this requirement and appears on more than 20 pages.</span></span> <span data-ttu-id="3b474-145">Эти страницы включают в себя журналы, заказы на продажу, заказы на покупку, накладные с произвольным текстом, журналы накладных поставщика и накладные по проекту.</span><span class="sxs-lookup"><span data-stu-id="3b474-145">These pages include journals, sales orders, purchase orders, free-text invoices, vendor invoice journals, and project invoices.</span></span> <span data-ttu-id="3b474-146">При обновлении или разноске документов все налоги разносятся с использованием соответствующей даты регистра НДС, и эта дата присутствует на таких страницах, как страницы журналов накладных клиентов и поставщиков.</span><span class="sxs-lookup"><span data-stu-id="3b474-146">When you update or post the documents, all taxes are posted by using the corresponding date of the VAT register, and the date is included on pages such as the customer and vendor invoice journals pages.</span></span></p>
<p><span data-ttu-id="3b474-147">В частности, для Чешской Республики поле <strong>Дата регистра НДС</strong> может быть пустым во время разноски в случае отложенной разноски НДС.</span><span class="sxs-lookup"><span data-stu-id="3b474-147">Specifically, for the Czech Republic, the <strong>VAT register date</strong> field can be blank during posting, in the event of postponed VAT posting.</span></span> <span data-ttu-id="3b474-148">В противном случае это поле является обязательным и должно быть заполнено.</span><span class="sxs-lookup"><span data-stu-id="3b474-148">Otherwise, the field is mandatory and must be filled in.</span></span></p>
<p><span data-ttu-id="3b474-149">Параметры проверки дат могут быть заданы на странице <strong>Налоговые группы</strong>:</span><span class="sxs-lookup"><span data-stu-id="3b474-149">Date validation parameters can be set on the <strong>Sales tax groups</strong> page:</span></span></p>
<ul>
<li><span data-ttu-id="3b474-150">Параметры <strong>Заполнение даты регистра НДС</strong> и <strong>Заполнение даты продажи</strong> используются в качестве метода заполнения по умолчанию для соответствующих дат.</span><span class="sxs-lookup"><span data-stu-id="3b474-150">The <strong>Date of VAT register filling</strong> and <strong>Sales date filling</strong> parameters are used as a default filling method for appropriate dates.</span></span> <span data-ttu-id="3b474-151">Также предусмотрены возможность ввода вручную и несколько методов автоматического ввода.</span><span class="sxs-lookup"><span data-stu-id="3b474-151">Manual input and several automated input methods are also available.</span></span></li>
<li><span data-ttu-id="3b474-152">Поле <strong>Обязательная дата продажи</strong> указывает, должна ли перед разноской накладной на продажу быть введена дата продажи.</span><span class="sxs-lookup"><span data-stu-id="3b474-152">The <strong>Mandatory sales date</strong> field indicates whether the sales date must be entered before a sales invoice is posted.</span></span></li>
</ul>
<p><span data-ttu-id="3b474-153">На странице <strong>Проводки в регистре НДС</strong> можно заполнить пустые даты для регистрации НДС для разнесенных проводок по налогу.</span><span class="sxs-lookup"><span data-stu-id="3b474-153">On the <strong>VAT Register transactions</strong> page, you can fill in blank dates for the VAT register for posted tax transactions.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="3b474-154">Даты регистрации НДС, которые включают отложенный налог</span><span class="sxs-lookup"><span data-stu-id="3b474-154">VAT register dates that include deferred tax</span></span></td>
<td><span data-ttu-id="3b474-155">Венгрия</span><span class="sxs-lookup"><span data-stu-id="3b474-155">Hungary</span></span></td>
<td>
<p><span data-ttu-id="3b474-156">Налоговое законодательство Венгрии требует, чтобы накладные создавались либо в момент выполнения, либо не позднее 15 дней с момента выполнения.</span><span class="sxs-lookup"><span data-stu-id="3b474-156">Hungary tax regulations require that invoices be created at either the time of fulfilment or no later than 15 days after fulfilment.</span></span></p>
<p><span data-ttu-id="3b474-157">Дата выполнения — это либо дата, когда были оказаны заказанные услуги, либо дата, когда были поставлены заказанные номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3b474-157">The fulfilment date is either the date when the ordered services were provided or the date when ordered items were delivered.</span></span> <span data-ttu-id="3b474-158">При обновлении или разноске документов все налоги разносятся с использованием соответствующей даты регистрации НДС, и эта дата присутствует на соответствующих страницах.</span><span class="sxs-lookup"><span data-stu-id="3b474-158">When you update or post the documents, all taxes are posted by using the corresponding date of the VAT register, and the date appears on relevant pages.</span></span> <span data-ttu-id="3b474-159">Кроме того, законодательство требует, чтобы НДС на непрерывно оказываемых услугах, таких как аренда, лизинг, консалтинг и отопление, соответствовал следующим критериям:</span><span class="sxs-lookup"><span data-stu-id="3b474-159">Additionally, regulations require that VAT on continuous delivery of services, such as renting, leasing, consulting, and heating, meet the following criteria:</span></span></p>
<ul>
<li><span data-ttu-id="3b474-160">НДС должен разноситься на специальный счет главной книги на дату накладной.</span><span class="sxs-lookup"><span data-stu-id="3b474-160">VAT must be posted to a dedicated general ledger account on the invoice date.</span></span></li>
<li><span data-ttu-id="3b474-161">НДС должен перемещаться со специальных счетов на счет налога к получению или на счет налога к уплате и включаться в отчет по НДС на требуемую дату.</span><span class="sxs-lookup"><span data-stu-id="3b474-161">VAT must be transferred from the special accounts to a sales tax receivable account or a payable account, and must be included in the VAT report on the due date.</span></span></li>
</ul>
<p><span data-ttu-id="3b474-162">Для удовлетворения этих требований вы можете переместить разноски главной книги на счет отложенного входящего налога и на счет отложенного исходящего налога.</span><span class="sxs-lookup"><span data-stu-id="3b474-162">To support these requirements, you can transfer General ledger postings to the Deferred incoming tax account and the Deferred outgoing tax account.</span></span> <span data-ttu-id="3b474-163">Тем не менее сначала необходимо выполнить следующие предварительные требования:</span><span class="sxs-lookup"><span data-stu-id="3b474-163">However, you must first complete the following prerequisites:</span></span></p>
<ul>
<li><span data-ttu-id="3b474-164">Настроить счета главной книги "Исходящий отсроченный НДС" и "Входящий отсроченный НДС" в группах разноски ГК.</span><span class="sxs-lookup"><span data-stu-id="3b474-164">Set up the Deferred VAT Payable and Deferred VAT Receivable ledger accounts in ledger posting groups.</span></span></li>
<li><span data-ttu-id="3b474-165">Включить параметр <strong>Отложенный НДС</strong> для налоговых групп номенклатур.</span><span class="sxs-lookup"><span data-stu-id="3b474-165">Enable the <strong>Deferred VAT</strong> parameter for item sales tax groups.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="3b474-166"> Обязательная дата НДС</span><span class="sxs-lookup"><span data-stu-id="3b474-166">Mandatory VAT date</span></span></td>
<td><span data-ttu-id="3b474-167">Польша</span><span class="sxs-lookup"><span data-stu-id="3b474-167">Poland</span></span></td>
<td>
<p><span data-ttu-id="3b474-168">Можно потребовать, чтобы дата регистрации НДС включалась в записи проводок по покупке и продаже.</span><span class="sxs-lookup"><span data-stu-id="3b474-168">You can require that the date of the VAT register be included in purchase and sales transaction records.</span></span> <span data-ttu-id="3b474-169">Таким образом можно зафиксировать дату регистрации НДС до разноски проводки.</span><span class="sxs-lookup"><span data-stu-id="3b474-169">Therefore, the date of the VAT register can be captured before a transaction is posted.</span></span> <span data-ttu-id="3b474-170">Эта функциональность помогает избежать необходимости обрабатывать несколько проводок в конце периода.</span><span class="sxs-lookup"><span data-stu-id="3b474-170">This functionality helps you avoid having to handle multiple transactions at the end of the period.</span></span></p>
<p><span data-ttu-id="3b474-171">Можно сделать поле <strong>Дата регистра НДС</strong> обязательным при разноске проводок клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="3b474-171">You can make the <strong>Date of VAT register</strong> field mandatory when customer or vendor transactions are posted.</span></span> <span data-ttu-id="3b474-172">Чтобы сделать это поле обязательным, включите параметр <strong>Необходимо указать дату НДС</strong> для связанного счета клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="3b474-172">To make this field mandatory, enable the <strong>VAT date is required</strong> option for the related customer or vendor account.</span></span></p>
</td>
</tr>
</tbody>
</table>
