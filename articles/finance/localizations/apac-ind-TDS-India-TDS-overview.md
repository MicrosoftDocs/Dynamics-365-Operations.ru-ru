---
title: Обзор налога, удерживаемого в источнике (TDS), для Индии
description: В этой теме приводятся подробные сведения о налоге, удерживаемом в источнике (TDS), для Индии. В документации по TDS описываются функции этой возможности.
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023551"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a><span data-ttu-id="47aa0-104">Обзор налога, удерживаемого в источнике (TDS), для Индии</span><span class="sxs-lookup"><span data-stu-id="47aa0-104">Indian Tax Deducted at Source (TDS) overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47aa0-105">В этой теме приводятся подробные сведения о налоге, удерживаемом в источнике (TDS), для Индии.</span><span class="sxs-lookup"><span data-stu-id="47aa0-105">This topic provides detailed information about Indian Tax Deducted at Source (TDS).</span></span>

<span data-ttu-id="47aa0-106">В документации по TDS описываются функции этой возможности.</span><span class="sxs-lookup"><span data-stu-id="47aa0-106">The TDS documentation covers the functionality of this capability.</span></span> <span data-ttu-id="47aa0-107">В ней также объясняется, как выполнить базовые настройки для TDS, расчета TDS по проводкам, как выполнить процесс сопоставления TDS, записать номера сертификатов TDS и создать запросы TDS, отчеты TDS и сертификаты TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-107">It also explains how to do the basic setup for TDS, calculate TDS on transactions, complete the TDS settlement process, record TDS certificate numbers, and generate TDS inquiries, TDS statements, and TDS certificates.</span></span> <span data-ttu-id="47aa0-108">Документация включает следующие темы:</span><span class="sxs-lookup"><span data-stu-id="47aa0-108">The documentation includes the following topics:</span></span>

- [<span data-ttu-id="47aa0-109">Базовая настройка TDS</span><span class="sxs-lookup"><span data-stu-id="47aa0-109">Basic setup for TDS</span></span>](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [<span data-ttu-id="47aa0-110">Конструктор формул и функции лимитов порога, используемые для расчета TDS</span><span class="sxs-lookup"><span data-stu-id="47aa0-110">Formula designer and threshold limit functionality used for TDS calculation</span></span>](apac-ind-TDS-Formula-designer.md)
- [<span data-ttu-id="47aa0-111">Расчет TDS по накладным, платежам, простым векселям и внутрихолдинговым проводкам</span><span class="sxs-lookup"><span data-stu-id="47aa0-111">Calculation of TDS on invoices, payments, promissory notes, and intercompany transactions</span></span>](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [<span data-ttu-id="47aa0-112">Периодическое сопоставление TDS и сопоставление сумм TDS с поставщиками центра TDS</span><span class="sxs-lookup"><span data-stu-id="47aa0-112">Periodic TDS settlement process and settlement of TDS amounts to TDS authority vendors</span></span>](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [<span data-ttu-id="47aa0-113">Запись и обновление номеров и дат сертификатов TDS</span><span class="sxs-lookup"><span data-stu-id="47aa0-113">Recording and updating TDS certificate numbers and dates</span></span>](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a><span data-ttu-id="47aa0-114">Введение в TDS</span><span class="sxs-lookup"><span data-stu-id="47aa0-114">Introduction to TDS</span></span>

<span data-ttu-id="47aa0-115">Согласно акту о подоходном налоге 1961 г. подоходный налог вычитается в источнике получателем услуги во время авансового платежа или учета кредита в зависимости, что происходит первым.</span><span class="sxs-lookup"><span data-stu-id="47aa0-115">Per the Income tax Act, 1961, income tax is deducted at the source by the receiver of the service at the time of advance payment or accounting of credit, whichever occurs first.</span></span> <span data-ttu-id="47aa0-116">Лицо, осуществляющее платеж, должно вычесть сумму налога и оплатить только чистое сальдо поставщику услуги.</span><span class="sxs-lookup"><span data-stu-id="47aa0-116">The person who makes the payment must deduct the tax amount and pay only the net balance to the provider of the service.</span></span> <span data-ttu-id="47aa0-117">TDS применяется к услугам, которые указаны правительственным органом, и налог вычитается с использованием ставок, которые правительственный орган определяет для периода.</span><span class="sxs-lookup"><span data-stu-id="47aa0-117">TDS is applied on services that the government specifies, and the tax is deducted by using the rates that the government specifies for a period.</span></span> <span data-ttu-id="47aa0-118">Ставка вычета базируется на статусе объекта, который получает платеж или предоставляет услугу.</span><span class="sxs-lookup"><span data-stu-id="47aa0-118">The rate of deduction is based on the status of the entity that receives the payment or provides the service.</span></span> <span data-ttu-id="47aa0-119">Статусы включают **Физическое лицо**, **Индийская семья** (**HUF**), **Компания**, **Фирма**, **Ассоциация лиц** (**AOP**), **Объединение физических лиц** (**BOI**) и **Локальный орган**.</span><span class="sxs-lookup"><span data-stu-id="47aa0-119">Statuses include **Individual**, **Hindu Undivided Family** (**HUF**), **Company**, **Firm**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**), and **Local authority**.</span></span>

<span data-ttu-id="47aa0-120">В следующих разделах перечислены услуги, к которым применяется этот TDS, указанный в правительственных учреждениях Индии.</span><span class="sxs-lookup"><span data-stu-id="47aa0-120">The following sections list the services that TDS is applied on, as specified by the Government of India.</span></span>

<span data-ttu-id="47aa0-121">**Резиденты**</span><span class="sxs-lookup"><span data-stu-id="47aa0-121">**Residents**</span></span>

- <span data-ttu-id="47aa0-122">Доходы от заработной платы (в разделе 192)</span><span class="sxs-lookup"><span data-stu-id="47aa0-122">Income from salaries (Under section 192)</span></span>
- <span data-ttu-id="47aa0-123">Доход от процентов ценных бумаг (в разделе 193)</span><span class="sxs-lookup"><span data-stu-id="47aa0-123">Income from interest on securities (Under section 193)</span></span>
- <span data-ttu-id="47aa0-124">Доходы от дивидендов (в разделе 194)</span><span class="sxs-lookup"><span data-stu-id="47aa0-124">Income from dividend (Under section 194)</span></span>
- <span data-ttu-id="47aa0-125">Доходы от процентов (в разделе 194A)</span><span class="sxs-lookup"><span data-stu-id="47aa0-125">Income from interest (Under section 194A)</span></span>
- <span data-ttu-id="47aa0-126">Доход от лотерей или головоломок (в разделе 194B)</span><span class="sxs-lookup"><span data-stu-id="47aa0-126">Income from lotteries or puzzles (Under section 194B)</span></span>
- <span data-ttu-id="47aa0-127">Выигрыш на скачках и т. п. (в разделе 194BB)</span><span class="sxs-lookup"><span data-stu-id="47aa0-127">Winning from horse races etc. (Under section 194BB)</span></span>
- <span data-ttu-id="47aa0-128">Подрядчики и субподрядчики (в разделе 194C)</span><span class="sxs-lookup"><span data-stu-id="47aa0-128">Contractors and sub-contractors (Under section 194C)</span></span>
- <span data-ttu-id="47aa0-129">Страховая комиссия (в разделе 194D)</span><span class="sxs-lookup"><span data-stu-id="47aa0-129">Insurance commission (Under section 194D)</span></span>
- <span data-ttu-id="47aa0-130">Доход от депозита по национальной программе накоплений (в разделе 194EE)</span><span class="sxs-lookup"><span data-stu-id="47aa0-130">Income from deposit under national saving scheme (Under section 194EE)</span></span>
- <span data-ttu-id="47aa0-131">Доходы от паевого фонда или UTI (в разделе 194F)</span><span class="sxs-lookup"><span data-stu-id="47aa0-131">Income from mutual fund or UTI (Under section 194F)</span></span>
- <span data-ttu-id="47aa0-132">Комиссия, компенсация, приз и т. п. по продажам или лотереи (в разделе 194G)</span><span class="sxs-lookup"><span data-stu-id="47aa0-132">Commission, Remuneration, Prize etc., on sale or lottery (Under section 194G)</span></span>
- <span data-ttu-id="47aa0-133">Оплата комиссии или брокерская комиссия (в разделе 194H)</span><span class="sxs-lookup"><span data-stu-id="47aa0-133">Payment of Commission or brokerage (Under section 194H)</span></span>
- <span data-ttu-id="47aa0-134">Аренда (в разделе 194I)</span><span class="sxs-lookup"><span data-stu-id="47aa0-134">Rent (Under section 194I)</span></span>
- <span data-ttu-id="47aa0-135">Профессиональная служба (в разделе 194J)</span><span class="sxs-lookup"><span data-stu-id="47aa0-135">Professional service (Under section 194J)</span></span>
- <span data-ttu-id="47aa0-136">Доходы от подразделений (в разделе 194K)</span><span class="sxs-lookup"><span data-stu-id="47aa0-136">Income from Units (Under section 194K)</span></span>
- <span data-ttu-id="47aa0-137">Оплата компенсации по приобретению определенного недвижимого имущества (в разделе 194LA)</span><span class="sxs-lookup"><span data-stu-id="47aa0-137">Payment of compensation on acquisition of certain immovable property (Under section 194LA)</span></span>

<span data-ttu-id="47aa0-138">**Нерезиденты**</span><span class="sxs-lookup"><span data-stu-id="47aa0-138">**Non-residents**</span></span>

- <span data-ttu-id="47aa0-139">Платежи спортсменам или спортивным ассоциациям-нерезидентам (в разделе 194E)</span><span class="sxs-lookup"><span data-stu-id="47aa0-139">Payments to Non-resident sportsmen or sports association (Under section 194E)</span></span>
- <span data-ttu-id="47aa0-140">Прочие суммы (в разделе 195)</span><span class="sxs-lookup"><span data-stu-id="47aa0-140">Other sums (Under section 195)</span></span>
- <span data-ttu-id="47aa0-141">Доходы в отношении подразделений нерезидентов (в разделе 196A)</span><span class="sxs-lookup"><span data-stu-id="47aa0-141">Income in respect of units of non-residents (Under section 196A)</span></span>

    - <span data-ttu-id="47aa0-142">Доходы в иностранной валюте по векселям или акциям индийской компании (в разделе 196C)</span><span class="sxs-lookup"><span data-stu-id="47aa0-142">Income from foreign currency bonds or shares of Indian Company (Under section 196C)</span></span>
    - <span data-ttu-id="47aa0-143">Доход иностранных институциональных инвесторов от ценных бумаг (в разделе 196D)</span><span class="sxs-lookup"><span data-stu-id="47aa0-143">Incomes of foreign institutional investors from securities (Under section 196D)</span></span>
    - <span data-ttu-id="47aa0-144">Зарплата и все остальные положительные доходы по всем заголовкам дохода (раздел 192)</span><span class="sxs-lookup"><span data-stu-id="47aa0-144">Salary and all other positive incomes under any head on income (Section 192)</span></span>
    - <span data-ttu-id="47aa0-145">Процент по ценным бумагам (раздел 193)</span><span class="sxs-lookup"><span data-stu-id="47aa0-145">Interest on securities (Section 193)</span></span>
    - <span data-ttu-id="47aa0-146">Проценты, отличные от процента по ценным бумагам (раздел 194A)</span><span class="sxs-lookup"><span data-stu-id="47aa0-146">Interest other than interest on securities (Section 194A)</span></span>
    - <span data-ttu-id="47aa0-147">Выплата подрядчикам и субподрядчикам (раздел 194C)</span><span class="sxs-lookup"><span data-stu-id="47aa0-147">Payments to contractors and sub-contractors (Section 194C)</span></span>
    - <span data-ttu-id="47aa0-148">Выигрыш в лотерею или кроссворды, головоломки (раздел 194B)</span><span class="sxs-lookup"><span data-stu-id="47aa0-148">Winnings from Lottery or crossword puzzles (Section 194B)</span></span>
    - <span data-ttu-id="47aa0-149">Выигрыш на скачках (разделе 194BB)</span><span class="sxs-lookup"><span data-stu-id="47aa0-149">Winnings from horse races (Section 194BB)</span></span>
    - <span data-ttu-id="47aa0-150">Комиссия страхования, охватывающая все платежи для ведения страхового бизнеса (раздел 194D)</span><span class="sxs-lookup"><span data-stu-id="47aa0-150">Insurance Commission covering all payments for procuring Insurance business (Section 194D)</span></span>
    - <span data-ttu-id="47aa0-151">Любой процент, отличающийся от процента по ценным бумагам, выплачиваемый нерезидентам, не являющимися компанией, или компанией в иностранную компанию (раздел 195)</span><span class="sxs-lookup"><span data-stu-id="47aa0-151">Any interest other than interest on securities payable to non-residents not being a company or to a foreign company (Section 195)</span></span>
    - <span data-ttu-id="47aa0-152">Платеж в спортсмену-нерезиденту, включая атлетов или спортивные ассоциации или учреждения.</span><span class="sxs-lookup"><span data-stu-id="47aa0-152">Payment to non-resident sportsman including athlete or sports association or institution.</span></span> <span data-ttu-id="47aa0-153">В случае спортсменов-нерезидентов платежи в отношении рекламных объявлений, а также статей по любой игре/спорту в Индии в газетах, журналах и так далее.</span><span class="sxs-lookup"><span data-stu-id="47aa0-153">In case of non-resident sportsman, payments in respect of advertisements as well as articles on any game/sports in India in newspapers, magazines, and so.</span></span> <span data-ttu-id="47aa0-154">включено (раздел 194E)</span><span class="sxs-lookup"><span data-stu-id="47aa0-154">is included (Section 194E)</span></span>
    - <span data-ttu-id="47aa0-155">Платеж в соответствии с депозитами по \[национальной программе накоплений\] NSS (раздел 194EE)</span><span class="sxs-lookup"><span data-stu-id="47aa0-155">Payment in respect of deposits under NSS \[National Savings Scheme\] (Section 194EE)</span></span>
    - <span data-ttu-id="47aa0-156">Платеж на счет для выкупа подразделений по паевому фонду или UTI (раздел 194F)</span><span class="sxs-lookup"><span data-stu-id="47aa0-156">Payment on account of repurchase of Units by Mutual Fund or UTI (Section 194F)</span></span>
    - <span data-ttu-id="47aa0-157">Оплата комиссии или брокерская комиссия (раздел 194H)</span><span class="sxs-lookup"><span data-stu-id="47aa0-157">Payment for Commission or brokerage (Section 194H)</span></span>
    - <span data-ttu-id="47aa0-158">Оплата аренды (раздел 194I)</span><span class="sxs-lookup"><span data-stu-id="47aa0-158">Payment of rent (Section 194I)</span></span>
    - <span data-ttu-id="47aa0-159">Оплата сборов для профессиональных или технических услуг (раздел 194J)</span><span class="sxs-lookup"><span data-stu-id="47aa0-159">Payment of fees for professional or technical services (Section 194J)</span></span>
    - <span data-ttu-id="47aa0-160">Комиссию компании с запасами, дистрибуторам, покупателям и лотерейных билетов, в том числе компенсация или приз для таких билетов (раздел 194G)</span><span class="sxs-lookup"><span data-stu-id="47aa0-160">Commission to Stockiest, distributors, buyers and sellers of Lottery tickets including remuneration or prize on such tickets (Section 194G)</span></span>
    - <span data-ttu-id="47aa0-161">Доходы от единиц, приобретаемые в иностранной валюте или в долгосрочной капитализации из-за передачи таких единиц, которые приобретены в иностранной валюте (раздел 196B)</span><span class="sxs-lookup"><span data-stu-id="47aa0-161">Income from Units purchased in foreign currency or long-term capital gain arising from the transfer of such Units purchased in foreign currency (Section 196B)</span></span>
    - <span data-ttu-id="47aa0-162">Оплата любых доходов нерезидентам по процентам или дивидендам на векселя и акции (раздел 196C)</span><span class="sxs-lookup"><span data-stu-id="47aa0-162">Payment of any income to non-residents in respect of interest or dividend on bonds and shares (Section 196C)</span></span>

<span data-ttu-id="47aa0-163">TDS рассчитан на покупки, продажи, возвраты продаж, кредит-ноты, приобретения основных средств, предоплаты, авансовые платежи, простые векселя, налог на работу и внутрихолдинговые проводки.</span><span class="sxs-lookup"><span data-stu-id="47aa0-163">TDS is calculated on purchases, sales, sales returns, credit notes, fixed asset acquisitions, prepayments, advance payments, promissory notes, works tax, and intercompany transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="47aa0-164">В текущем налоговом сценарии для Индии TDS не рассчитывается для проводок по продажам.</span><span class="sxs-lookup"><span data-stu-id="47aa0-164">In the current Indian tax scenario, TDS isn't calculated on sales transactions.</span></span> <span data-ttu-id="47aa0-165">Однако система включает в себя подготовку к расчету TDS с восстановлением по проводкам по продажам, особенно для внутрихолдинговых проводок.</span><span class="sxs-lookup"><span data-stu-id="47aa0-165">However, the system includes a provision to calculate TDS recoverable on sales transactions, especially for intercompany transactions.</span></span>

<span data-ttu-id="47aa0-166">Расчет TDS всегда учитывает порог и порог исключения, которые определены для компонента TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-166">The calculation of TDS always considers the threshold and the exception threshold that are defined for the TDS component.</span></span>

<span data-ttu-id="47aa0-167">Должен запускаться периодический процесс сопоставления TDS, а платежи TDS должны быть сопоставлены с поставщиками органа TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-167">The periodic TDS settlement process must be run, and the TDS payments must be settled to TDS authority vendors.</span></span>

<span data-ttu-id="47aa0-168">Номера и даты сертификатов для сертификатов TDS, полученных от поставщиков или клиентов, могут быть записаны и обновлены.</span><span class="sxs-lookup"><span data-stu-id="47aa0-168">The certificate numbers and dates for TDS certificates that are received from vendors or customers can be recorded and updated.</span></span> <span data-ttu-id="47aa0-169">Кроме того, форма 26Q и форма 27Q (ежеквартальные выписки), и форма 16A (сертификат) для TDS могут быть созданы в Finance.</span><span class="sxs-lookup"><span data-stu-id="47aa0-169">Additionally, Form 26Q and Form 27Q quarterly statements, and the Form 16A certificate for TDS, can be generated in Finance.</span></span>

## <a name="setting-up-and-working-with-tds"></a><span data-ttu-id="47aa0-170">Настройка и работа с TDS</span><span class="sxs-lookup"><span data-stu-id="47aa0-170">Setting up and working with TDS</span></span>

<span data-ttu-id="47aa0-171">Ниже приводится обзор процесса настройки и работы с TDS:</span><span class="sxs-lookup"><span data-stu-id="47aa0-171">Here is an overview of the process for setting up and working with TDS:</span></span>

1. <span data-ttu-id="47aa0-172">**Настройка TDS:**</span><span class="sxs-lookup"><span data-stu-id="47aa0-172">**TDS setup:**</span></span>

    - <span data-ttu-id="47aa0-173">Настройка параметров:</span><span class="sxs-lookup"><span data-stu-id="47aa0-173">Parameter setup:</span></span>

        - <span data-ttu-id="47aa0-174">В параметрах главной книги активируйте параметры, которые относятся к TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-174">In General ledger parameters, activate parameters that are related to TDS.</span></span>
        - <span data-ttu-id="47aa0-175">В параметрах главной книги настройте номерную серию для платежей подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="47aa0-175">In General ledger parameters, set up the number sequence for withholding tax payments.</span></span>
        - <span data-ttu-id="47aa0-176">Настройте параметры в модуле "Расчеты с поставщиками" и "Расчеты с клиентами".</span><span class="sxs-lookup"><span data-stu-id="47aa0-176">Set up parameters in Accounts payable and Accounts receivable.</span></span>

    - <span data-ttu-id="47aa0-177">Основная настройка:</span><span class="sxs-lookup"><span data-stu-id="47aa0-177">Basic setup:</span></span>

        - <span data-ttu-id="47aa0-178">Настроите регистрационные номера TDS для компании, клиентов и поставщиков.</span><span class="sxs-lookup"><span data-stu-id="47aa0-178">Set up TDS registration numbers for a company, customers, and vendors.</span></span>
        - <span data-ttu-id="47aa0-179">Настройте группы компонентов TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-179">Set up TDS component groups.</span></span>
        - <span data-ttu-id="47aa0-180">Настройте компоненты TDS, присоедините к ним группы компонентов TDS и задайте для них порог и порог исключений.</span><span class="sxs-lookup"><span data-stu-id="47aa0-180">Set up TDS components, attach TDS component groups to them, and define the threshold and exception threshold for them.</span></span>
        - <span data-ttu-id="47aa0-181">Настройте органы TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-181">Set up TDS authorities.</span></span>
        - <span data-ttu-id="47aa0-182">Настройте периоды сопоставления TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-182">Set up TDS settlement periods.</span></span>
        - <span data-ttu-id="47aa0-183">Настройте налоговые коды TDS и присоедините к ним компоненты TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-183">Set up TDS tax codes, and attach TDS components to them.</span></span>
        - <span data-ttu-id="47aa0-184">Настройте налоговые группы TDS и присоедините к ним налоговые коды TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-184">Set up TDS tax groups, and attach TDS tax codes to them.</span></span>
        - <span data-ttu-id="47aa0-185">В конструкторе формул определите формулу для расчета TDS для группы TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-185">In the formula designer, define a formula to calculate TDS for a TDS group.</span></span>
        - <span data-ttu-id="47aa0-186">Запишите номера сертификатов на предоставление налоговых льгот TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-186">Record TDS concession certificate numbers.</span></span>

    - <span data-ttu-id="47aa0-187">Счета ГК и настройка компании:</span><span class="sxs-lookup"><span data-stu-id="47aa0-187">Ledger accounts and company setup:</span></span>

        - <span data-ttu-id="47aa0-188">Настройте счета ГК для модуля "расчеты с поставщиками" и "расчеты с клиентами".</span><span class="sxs-lookup"><span data-stu-id="47aa0-188">Set up TDS payable and receivable ledger accounts.</span></span>
        - <span data-ttu-id="47aa0-189">Настройте для компании налоговый вычет и номер счета сбора (TAN) и категорию типа вычета.</span><span class="sxs-lookup"><span data-stu-id="47aa0-189">Set up a Tax Deduction and Collection Account Number (TAN) and a deductor type category for the company.</span></span>

    - <span data-ttu-id="47aa0-190">Другие настройки:</span><span class="sxs-lookup"><span data-stu-id="47aa0-190">Other setup:</span></span>

        - <span data-ttu-id="47aa0-191">Настройте график платежей, включающий распределение TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-191">Set up a payment schedule that includes TDS allocation.</span></span>
        - <span data-ttu-id="47aa0-192">Настройте типа сбора по платежам для органа TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-192">Set up a payment fee type for payments to the TDS authority.</span></span>
        - <span data-ttu-id="47aa0-193">Настройте информацию о группах TDS, номерах постоянных счетов (PAN) и TAN для поставщиков и клиентов.</span><span class="sxs-lookup"><span data-stu-id="47aa0-193">Set up information about TDS groups, permanent account numbers (PANs), and TANs for vendors and customers.</span></span>

2. <span data-ttu-id="47aa0-194">**Расчет TDS в проводках:**</span><span class="sxs-lookup"><span data-stu-id="47aa0-194">**Calculation of TDS in transactions:**</span></span>

    - <span data-ttu-id="47aa0-195">Накладные и платежи</span><span class="sxs-lookup"><span data-stu-id="47aa0-195">Invoices and payments</span></span>
    - <span data-ttu-id="47aa0-196">Простые векселя</span><span class="sxs-lookup"><span data-stu-id="47aa0-196">Promissory notes</span></span>
    - <span data-ttu-id="47aa0-197">Авансовые платежи</span><span class="sxs-lookup"><span data-stu-id="47aa0-197">Advance payments</span></span>
    - <span data-ttu-id="47aa0-198">Предоплаты</span><span class="sxs-lookup"><span data-stu-id="47aa0-198">Prepayments</span></span>

3. <span data-ttu-id="47aa0-199">**Сопоставление TDS**</span><span class="sxs-lookup"><span data-stu-id="47aa0-199">**TDS settlement:**</span></span>

    - <span data-ttu-id="47aa0-200">Периодический процесс сопоставления TDS</span><span class="sxs-lookup"><span data-stu-id="47aa0-200">Periodic TDS settlement process</span></span>
    - <span data-ttu-id="47aa0-201">Сопоставление проводок TDS с поставщиками органа TDS и создание Challan TDS</span><span class="sxs-lookup"><span data-stu-id="47aa0-201">Settlement of TDS payments to TDS authority vendors and generation of TDS challan</span></span>

4. <span data-ttu-id="47aa0-202">**Запросы TDS, отчеты и сертификат:**</span><span class="sxs-lookup"><span data-stu-id="47aa0-202">**TDS inquiries, statements, and certificate:**</span></span>

    - <span data-ttu-id="47aa0-203">Запишите и обновите номера и даты сертификатов TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-203">Record and update TDS certificate numbers and dates.</span></span>
    - <span data-ttu-id="47aa0-204">Создайте запрос TDS и разнесенный запрос TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-204">Generate a TDS inquiry and a posted TDS inquiry.</span></span>
    - <span data-ttu-id="47aa0-205">Создайте формы 27A, 26Q и 27Q TDS и ежеквартальные отчеты e-TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-205">Generate Form 27A, Form 26Q, and Form 27Q TDS and e-TDS quarterly statements.</span></span>
    - <span data-ttu-id="47aa0-206">Создайте сертификат по форме 16A TDS.</span><span class="sxs-lookup"><span data-stu-id="47aa0-206">Generate a Form 16A TDS certificate.</span></span>
