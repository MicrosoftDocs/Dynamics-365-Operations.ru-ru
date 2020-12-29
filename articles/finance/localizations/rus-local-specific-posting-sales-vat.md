---
title: Специфическая локальная разноска исходящего НДС
description: В этом разделе рассматриваются определенные параметры разнесения проводок расчетов по налогу на добавленную стоимость (НДС) в соответствии с российским законодательством.
author: anasyash
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: anasyash
ms.search.validFrom: 2019-07-23
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 75dfe57487967dd4ba30017fa87cfe9df022342d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408547"
---
# <a name="local-specific-posting-of-sales-vat"></a><span data-ttu-id="b9989-103">Специфическая локальная разноска исходящего НДС</span><span class="sxs-lookup"><span data-stu-id="b9989-103">Local specific posting of sales VAT</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="general-principles-of-tax-accounting"></a><span data-ttu-id="b9989-104">Общие принципы налогового учета</span><span class="sxs-lookup"><span data-stu-id="b9989-104">General principles of tax accounting</span></span>

1. <span data-ttu-id="b9989-105">Налоговые коды должны быть определены.</span><span class="sxs-lookup"><span data-stu-id="b9989-105">Sales tax codes should be determined.</span></span> <span data-ttu-id="b9989-106">Для каждого налогового кода определяется следующая информация: тип налога (НДС, акциз и т.д.), база для расчета налога, ставка или стоимость, срок действия и правила размещения на счетах.</span><span class="sxs-lookup"><span data-stu-id="b9989-106">For each sales tax code, the following information is determined: the type of tax (VAT, excise, and so on), the base for the tax calculation, the rate or value, the period of validity, and the rules for posting to accounts.</span></span> <span data-ttu-id="b9989-107">Правила разноски настраиваются посредством определения группы разноски для налогового кода.</span><span class="sxs-lookup"><span data-stu-id="b9989-107">The posting rules are set by specifying the posting group for the sales tax code.</span></span> <span data-ttu-id="b9989-108">Счета учета настроены на **Группы разноски ГК**.</span><span class="sxs-lookup"><span data-stu-id="b9989-108">The ledger accounts are set up on the **Ledger posting groups**.</span></span> <span data-ttu-id="b9989-109">Счета учета будут использоваться при проведении проводок учета для налогового кода.</span><span class="sxs-lookup"><span data-stu-id="b9989-109">The ledger accounts will be used when accounting transactions are performed for a tax code.</span></span>
2. <span data-ttu-id="b9989-110">Налоговые коды объединяются в налоговые группы и налоговые группы номенклатур.</span><span class="sxs-lookup"><span data-stu-id="b9989-110">Tax codes are combined into sales tax groups and item sales tax groups.</span></span>
3. <span data-ttu-id="b9989-111">При выполнении проводки покупки или продажи будут указаны налоговые группы и налоговые группы номенклатур.</span><span class="sxs-lookup"><span data-stu-id="b9989-111">When a purchase or sales transaction is performed, sales tax groups and item sales tax groups will be indicated.</span></span> <span data-ttu-id="b9989-112">Система определяет, какие налоги (налоговых коды) включаются и в налоговую группу, и в налоговую группу номенклатур.</span><span class="sxs-lookup"><span data-stu-id="b9989-112">The system determines which taxes (tax codes) are included in both the sales tax group and the item sales tax group.</span></span> <span data-ttu-id="b9989-113">Она также рассчитывает налоги и генерирует проводки учета для них при разнесении операции.</span><span class="sxs-lookup"><span data-stu-id="b9989-113">It also calculates the taxes, and generates accounting transactions for them when the operation is posted.</span></span>

<span data-ttu-id="b9989-114">Дополнительные сведения см. в разделе [Обзор косвенных налогов](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview).</span><span class="sxs-lookup"><span data-stu-id="b9989-114">For more information, see [Indirect taxes overview](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview).</span></span>

## <a name="posting-of-vat-payable-in-russia"></a><span data-ttu-id="b9989-115">Разнесение НДС, уплачиваемого в России</span><span class="sxs-lookup"><span data-stu-id="b9989-115">Posting of VAT payable in Russia</span></span>
<span data-ttu-id="b9989-116">В следующей таблице приводится пример записей учета для продаж товаров и услуг в России.</span><span class="sxs-lookup"><span data-stu-id="b9989-116">The following table shows an example of accounting entries for sales of goods and services in Russia.</span></span>

| <span data-ttu-id="b9989-117">**Проводка**</span><span class="sxs-lookup"><span data-stu-id="b9989-117">**Transaction**</span></span>                          | <span data-ttu-id="b9989-118">**Сумма, руб.**</span><span class="sxs-lookup"><span data-stu-id="b9989-118">**Amount**</span></span>                    | <span data-ttu-id="b9989-119">**Источник проводок**</span><span class="sxs-lookup"><span data-stu-id="b9989-119">**Origin of transactions**</span></span>                                                                                                                                                                                                                                                                                                  |
|------------------------------------------|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9989-120">D62 [Задолженность] C90.1 [Доходы]</span><span class="sxs-lookup"><span data-stu-id="b9989-120">D62 [Debts] C90.1 [Revenue]</span></span>              | <span data-ttu-id="b9989-121">Сумма продаж, включая налоги</span><span class="sxs-lookup"><span data-stu-id="b9989-121">Sales amount, including taxes</span></span> | <span data-ttu-id="b9989-122">Дебетовый счет определяется из настройки разноски по клиенту.</span><span class="sxs-lookup"><span data-stu-id="b9989-122">The debit account is determined from the setup of customer posting.</span></span> <span data-ttu-id="b9989-123">Кредитовый счет определяется из настройки либо счета выручки от разноски запасов или счета выручки от строки накладной по продаже с произвольным текстом (поле **Счет ГК**).</span><span class="sxs-lookup"><span data-stu-id="b9989-123">The credit account is determined from the setup of either the revenue account from the inventory posting or the revenue account from the sales free text invoice line (**Main account** field).</span></span>                                                         |
| <span data-ttu-id="b9989-124">D90.2 [Себестоимость проданных товаров] C41 [Товары]</span><span class="sxs-lookup"><span data-stu-id="b9989-124">D90.2 [Cost of goods sold] C41 [Goods]</span></span>   | <span data-ttu-id="b9989-125">Стоимость товаров и услуг</span><span class="sxs-lookup"><span data-stu-id="b9989-125">Cost of goods and services</span></span>    | <span data-ttu-id="b9989-126">Счета определяются из настройки разноски запасов.</span><span class="sxs-lookup"><span data-stu-id="b9989-126">Accounts are determined from the setup of the inventory posting.</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="b9989-127">D90.3 [НДС от продаж] C68 [Налоги] / НДС</span><span class="sxs-lookup"><span data-stu-id="b9989-127">D90.3 [VAT from sales] C68 [Taxes] / VAT</span></span> | <span data-ttu-id="b9989-128">Сумма НДС</span><span class="sxs-lookup"><span data-stu-id="b9989-128">VAT amount</span></span>                    | <span data-ttu-id="b9989-129">Дебетовые и кредитовые счета определяются из настройки группы разноски ГК для налогов.</span><span class="sxs-lookup"><span data-stu-id="b9989-129">The debit and credit accounts are determined from the setup of the ledger posting groups for taxes.</span></span> <span data-ttu-id="b9989-130">Дебетовый счет определяется из поля **Корр.счет уплаты**.</span><span class="sxs-lookup"><span data-stu-id="b9989-130">The debit account is determined from the **Payment offset account** field.</span></span> <span data-ttu-id="b9989-131">Кредитовый счет определяется из поля **Исходящий налог** страницы **Группы разноски ГК** (**Налог** \> **Настройка** \> **Налог**).</span><span class="sxs-lookup"><span data-stu-id="b9989-131">The credit account is determined from the **Sales Tax Payable** field of the **Ledger posting groups** page (**Tax** \> **Setup** \> **Sales tax**).</span></span> |

## <a name="system-setup"></a><span data-ttu-id="b9989-132">Настройка системы</span><span class="sxs-lookup"><span data-stu-id="b9989-132">System setup</span></span>

### <a name="set-up-fixed-offset-posting"></a><span data-ttu-id="b9989-133">Настройка **Фиксированная корреспонденция**</span><span class="sxs-lookup"><span data-stu-id="b9989-133">Set up **fixed offset posting**</span></span>

<span data-ttu-id="b9989-134">Для совершения проводок продаж в соответствии с российскими стандартами необходимо завершить следующую конфигурацию, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="b9989-134">To perform sales transactions in accordance with Russian standards, you must complete the following configuration as shown in the preceding.</span></span>

1. <span data-ttu-id="b9989-135">Перейдите к **Налог** \> **Параметры** \> **Настройка** \> **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="b9989-135">Go to **Tax** \> **Parameters** \> **Setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="b9989-136">На вкладке **Налог** убедитесь, что поле **Метод расчета** настроено на **Строка**.</span><span class="sxs-lookup"><span data-stu-id="b9989-136">On the **Sales tax** tab, make sure that the **Calculation method** field is set to  **Line**.</span></span>
3. <span data-ttu-id="b9989-137">Убедитесь, параметр **Фиксированная корреспонденция** включен.</span><span class="sxs-lookup"><span data-stu-id="b9989-137">Make sure that the **Fixed offset posting** option is turned on.</span></span>

> [!NOTE] 
> <span data-ttu-id="b9989-138">Если параметр **Фиксированная корреспонденция** отключен, система выполняет следующие проводки по продаже товаров и услуг:</span><span class="sxs-lookup"><span data-stu-id="b9989-138">If the **Fixed offset posting** option is turned off, the system performs the following transactions for sales of goods and services:</span></span>
>
> - <span data-ttu-id="b9989-139">D90.2 C41 — Себестоимость</span><span class="sxs-lookup"><span data-stu-id="b9989-139">D90.2 C41 – Cost price</span></span>
> - <span data-ttu-id="b9989-140">D62 C90.1 — Сумма продаж без налогов</span><span class="sxs-lookup"><span data-stu-id="b9989-140">D62 C90.1 – Sales amount without taxes</span></span>
> - <span data-ttu-id="b9989-141">D62 C68 — Сумма налога</span><span class="sxs-lookup"><span data-stu-id="b9989-141">D62 C68 – Tax amount</span></span>

## <a name="set-up-a-posting-group"></a><span data-ttu-id="b9989-142">Настройка группы разноски</span><span class="sxs-lookup"><span data-stu-id="b9989-142">Set up a posting group</span></span>

<span data-ttu-id="b9989-143">Группа разноски должна быть указана для каждого налогового кода.</span><span class="sxs-lookup"><span data-stu-id="b9989-143">A posting group must be specified for each sales tax code.</span></span> <span data-ttu-id="b9989-144">Используйте стандартный метод для настройки параметров в группе разноски.</span><span class="sxs-lookup"><span data-stu-id="b9989-144">Use the standard method to set up parameters in the posting group.</span></span>

1. <span data-ttu-id="b9989-145">Перейдите к **Налог** \> **Настройка** \> **Налог** \> **Группы разноски ГК**, чтобы открыть страницу **Группы разноски ГК**.</span><span class="sxs-lookup"><span data-stu-id="b9989-145">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups** to open the **Ledger  posting groups** page.</span></span>
2. <span data-ttu-id="b9989-146">Введите в поле **Группа разноски ГК** уникальный код для группы разноски.</span><span class="sxs-lookup"><span data-stu-id="b9989-146">In the **Ledger Posting group** field, enter unique code for the posting  group.</span></span>
3. <span data-ttu-id="b9989-147">В поле **Описание** введите описание группы разноски.</span><span class="sxs-lookup"><span data-stu-id="b9989-147">In the **Description** field, enter a description of the posting group.</span></span>
4. <span data-ttu-id="b9989-148">В поле **Исходящий налог** укажите счет для исходящего налога.</span><span class="sxs-lookup"><span data-stu-id="b9989-148">In the **Sales Tax Payable** field, specify the account for tax payable.</span></span>
5. <span data-ttu-id="b9989-149">В поле **Корр. счет уплаты** укажите соответствующий счет для уплаты налога.</span><span class="sxs-lookup"><span data-stu-id="b9989-149">In the **Payment offset account** field, specify corresponding account for  tax payable.</span></span>

> [!NOTE] 
> <span data-ttu-id="b9989-150">Это поле, характерное для России, используется при включении параметра **Фиксированная корреспонденция** (см. таблицу ранее в этом разделе для примера разноски).</span><span class="sxs-lookup"><span data-stu-id="b9989-150">This Russia-specific field is used when the **Fixed offset posting** option is turned on (see the table earlier in this topic for a posting example).</span></span>

6. <span data-ttu-id="b9989-151">Укажите соответствующие счета обычным способом для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="b9989-151">Specify the appropriate accounts in the usual way for the following fields:</span></span>

- <span data-ttu-id="b9989-152">**Входящий налог**</span><span class="sxs-lookup"><span data-stu-id="b9989-152">**Sales Tax Receivable**</span></span>
- <span data-ttu-id="b9989-153">**Отложенный налог**</span><span class="sxs-lookup"><span data-stu-id="b9989-153">**Deferred tax**</span></span>
- <span data-ttu-id="b9989-154">**Оплата входящего налога**</span><span class="sxs-lookup"><span data-stu-id="b9989-154">**Incoming tax payment**</span></span>
- <span data-ttu-id="b9989-155">**Расходы по налогу за пользование**</span><span class="sxs-lookup"><span data-stu-id="b9989-155">**Use tax expense**</span></span>
- <span data-ttu-id="b9989-156">**Налог за пользование, подлежащий уплате**</span><span class="sxs-lookup"><span data-stu-id="b9989-156">**Use tax payable**</span></span>
- <span data-ttu-id="b9989-157">**Скидка по оплате по поставщику**</span><span class="sxs-lookup"><span data-stu-id="b9989-157">**Vendor cash discount**</span></span>
- <span data-ttu-id="b9989-158">**Скидка по оплате по клиенту**</span><span class="sxs-lookup"><span data-stu-id="b9989-158">**Customer cash discount**</span></span>

> [!NOTE]
> <span data-ttu-id="b9989-159">Счета в поле **Тип разноски** должны иметь значение **Налог**.</span><span class="sxs-lookup"><span data-stu-id="b9989-159">Accounts in the **Posting type** field must have a **Tax** value.</span></span> <span data-ttu-id="b9989-160">Если счета не имеют этого значения, его можно добавить на вкладке **Проверка разноски** на странице **Счета ГК**.</span><span class="sxs-lookup"><span data-stu-id="b9989-160">If the accounts don't have this value, you can add it on the **Posting validation** tab on the **Main accounts** page.</span></span>
