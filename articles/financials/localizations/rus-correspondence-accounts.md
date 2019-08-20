---
title: Корреспонденция счетов
description: В этом разделе представлены сведения о корреспонденции счетов в России.
author: ShylaThompson
manager: AnnBe
ms.date: 04/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: cf25ea8fd9bbbcdc6f2c17cb41f257fc26820b96
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849312"
---
# <a name="correspondence-of-accounts"></a><span data-ttu-id="c65f5-103">Корреспонденция счетов</span><span class="sxs-lookup"><span data-stu-id="c65f5-103">Correspondence of accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c65f5-104">Корреспонденция счетов — это подход к непрерывной и взаимосвязанной регистрации деловых операций на корреспондентских счетах ГК.</span><span class="sxs-lookup"><span data-stu-id="c65f5-104">Correspondence of accounts is an approach to continuous and interrelated registration of business transactions in corresponding general ledger accounts.</span></span> <span data-ttu-id="c65f5-105">Он основан на двойной системе бухгалтерского учета.</span><span class="sxs-lookup"><span data-stu-id="c65f5-105">It's based on the double-entry bookkeeping system.</span></span> <span data-ttu-id="c65f5-106">Операции ГК представлены с корреспондентскими счетами с использованием российских стандартов учета.</span><span class="sxs-lookup"><span data-stu-id="c65f5-106">Ledger vouchers are represented together with corresponding accounts by using the Russian accounting standards.</span></span>

<span data-ttu-id="c65f5-107">Можно ввести проводки с несколькими аналитиками в журналы Главной книги и другие модули.</span><span class="sxs-lookup"><span data-stu-id="c65f5-107">You can enter multidimensional transactions in the ledger journals and other modules.</span></span> <span data-ttu-id="c65f5-108">В большинстве случаев проводки, которые автоматически создаются из других модулей, имеют несколько аналитик.</span><span class="sxs-lookup"><span data-stu-id="c65f5-108">In most cases, transactions that are automatically created from other modules are multidimensional.</span></span> <span data-ttu-id="c65f5-109">Эти проводки нужно изменить на двухмерные.</span><span class="sxs-lookup"><span data-stu-id="c65f5-109">These transactions should be changed to two-dimensional.</span></span> <span data-ttu-id="c65f5-110">Это изменение может включать разделение проводок ГК.</span><span class="sxs-lookup"><span data-stu-id="c65f5-110">This change might involve splitting ledger transactions.</span></span> <span data-ttu-id="c65f5-111">В этом случае указываются следующие случаи корреспонденции.</span><span class="sxs-lookup"><span data-stu-id="c65f5-111">In this case, the following correspondence cases are specified.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c65f5-112">Тип корреспонденции</span><span class="sxs-lookup"><span data-stu-id="c65f5-112">Type of correspondence</span></span></th>
<th><span data-ttu-id="c65f5-113">Перед корреспонденцией</span><span class="sxs-lookup"><span data-stu-id="c65f5-113">Before correspondence</span></span></th>
<th><span data-ttu-id="c65f5-114">После корреспонденции</span><span class="sxs-lookup"><span data-stu-id="c65f5-114">After correspondence</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c65f5-115">Взаимно-однозначный</span><span class="sxs-lookup"><span data-stu-id="c65f5-115">One-to-one</span></span></td>
<td>
<p><span data-ttu-id="c65f5-116">Счет А 200 (дебетовая проводка)</span><span class="sxs-lookup"><span data-stu-id="c65f5-116">Account A 200 (debit transaction)</span></span></p>
<p><span data-ttu-id="c65f5-117">Счет В 200 (кредитная проводка)</span><span class="sxs-lookup"><span data-stu-id="c65f5-117">Account B 200 (credit transaction)</span></span></p>
</td>
<td>
<p><span data-ttu-id="c65f5-118">Счет A – Счет B 200</span><span class="sxs-lookup"><span data-stu-id="c65f5-118">Account A – Account B 200</span></span></p>
<p><span data-ttu-id="c65f5-119">(Две проводки)</span><span class="sxs-lookup"><span data-stu-id="c65f5-119">(Two transactions)</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="c65f5-120">Один-ко-многим</span><span class="sxs-lookup"><span data-stu-id="c65f5-120">One-to-many</span></span></td>
<td>
<p><span data-ttu-id="c65f5-121">Счет А 200 (дебетовая проводка)</span><span class="sxs-lookup"><span data-stu-id="c65f5-121">Account A 200 (debit transaction)</span></span></p>
<p><span data-ttu-id="c65f5-122">Счет В 160 (кредитная проводка)</span><span class="sxs-lookup"><span data-stu-id="c65f5-122">Account B 160 (credit transaction)</span></span></p>
<p><span data-ttu-id="c65f5-123">Счет С 40 (кредитная проводка)</span><span class="sxs-lookup"><span data-stu-id="c65f5-123">Account C 40 (credit transaction)</span></span></p>
</td>
<td>
<p><span data-ttu-id="c65f5-124">Счет A – Счет B 160</span><span class="sxs-lookup"><span data-stu-id="c65f5-124">Account A – Account B 160</span></span></p>
<p><span data-ttu-id="c65f5-125">Счет A – Счет С 40</span><span class="sxs-lookup"><span data-stu-id="c65f5-125">Account A – Account C 40</span></span></p>
<p><span data-ttu-id="c65f5-126">(Четыре проводки)</span><span class="sxs-lookup"><span data-stu-id="c65f5-126">(Four transactions)</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="c65f5-127">Многие-к-одному</span><span class="sxs-lookup"><span data-stu-id="c65f5-127">Many-to-one</span></span></td>
<td>
<p><span data-ttu-id="c65f5-128">Счет А 200 (дебетовая проводка)</span><span class="sxs-lookup"><span data-stu-id="c65f5-128">Account A 200 (debit transaction)</span></span></p>
<p><span data-ttu-id="c65f5-129">Счет В 160 (дебетовая проводка)</span><span class="sxs-lookup"><span data-stu-id="c65f5-129">Account B 160 (debit transaction)</span></span></p>
<p><span data-ttu-id="c65f5-130">Счет С 360 (кредитная проводка)</span><span class="sxs-lookup"><span data-stu-id="c65f5-130">Account C 360 (credit transaction)</span></span></p>
</td>
<td>
<p><span data-ttu-id="c65f5-131">Счет A – Счет С 200</span><span class="sxs-lookup"><span data-stu-id="c65f5-131">Account A – Account C 200</span></span></p>
<p><span data-ttu-id="c65f5-132">Счет В – Счет С 160</span><span class="sxs-lookup"><span data-stu-id="c65f5-132">Account B – Account C 160</span></span></p>
<p><span data-ttu-id="c65f5-133">(Четыре проводки)</span><span class="sxs-lookup"><span data-stu-id="c65f5-133">(Four transactions)</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="c65f5-134">Много-к-много</span><span class="sxs-lookup"><span data-stu-id="c65f5-134">Many-to-many</span></span></td>
<td>
<p><span data-ttu-id="c65f5-135">Счет А 200 (дебетовая проводка)</span><span class="sxs-lookup"><span data-stu-id="c65f5-135">Account A 200 (debit transaction)</span></span></p>
<p><span data-ttu-id="c65f5-136">Счет В 160 (дебетовая проводка)</span><span class="sxs-lookup"><span data-stu-id="c65f5-136">Account B 160 (debit transaction)</span></span></p>
<p><span data-ttu-id="c65f5-137">Счет С 260 (кредитная проводка)</span><span class="sxs-lookup"><span data-stu-id="c65f5-137">Account C 260 (credit transaction)</span></span></p>
<p><span data-ttu-id="c65f5-138">Счет D 100 (кредитная проводка)</span><span class="sxs-lookup"><span data-stu-id="c65f5-138">Account D 100 (credit transaction)</span></span></p>
</td>
<td>
<p><span data-ttu-id="c65f5-139">Индивидуальная обработка</span><span class="sxs-lookup"><span data-stu-id="c65f5-139">Individual processing</span></span></p>
<p><span data-ttu-id="c65f5-140">(Несколько проводок)</span><span class="sxs-lookup"><span data-stu-id="c65f5-140">(Multiple transactions)</span></span></p>
</td>
</tr>
</tbody>
</table>

<span data-ttu-id="c65f5-141">Когда механизм соответствия проводок включен, каждая создаваемая новая бухгалтерская проводка состоит из набора двухсторонних корреспондирующих проводок.</span><span class="sxs-lookup"><span data-stu-id="c65f5-141">When the transactions correspondence mechanism is turned on, each new accounting transaction that is created consists of a set of two-way corresponding transactions.</span></span> <span data-ttu-id="c65f5-142">При разноске бухгалтерских проводок связь корреспонденции определяется автоматически.</span><span class="sxs-lookup"><span data-stu-id="c65f5-142">When the accounting transactions are posted, the corresponding relationship is automatically defined.</span></span> <span data-ttu-id="c65f5-143">Если механизм не включен, отношения корреспонденции не создаются между проводками.</span><span class="sxs-lookup"><span data-stu-id="c65f5-143">If the mechanism isn't turned on, no correspondence relationships are created between transactions.</span></span>

<span data-ttu-id="c65f5-144">Если до включения механизма корреспонденции счетов уже существуют какие-либо некорреспондирующие счета, они не связываются автоматически.</span><span class="sxs-lookup"><span data-stu-id="c65f5-144">If any non-corresponding accounts exist before the account correspondence mechanism is turned on, they aren't automatically linked.</span></span> <span data-ttu-id="c65f5-145">Необходимо вручную определить связи для этих проводок.</span><span class="sxs-lookup"><span data-stu-id="c65f5-145">You must manually define relationships for the transactions.</span></span>

## <a name="turn-on-the-account-correspondence-mechanism-for-accounting-transactions"></a><span data-ttu-id="c65f5-146">Включение механизма соответствия счетов для проводок учета</span><span class="sxs-lookup"><span data-stu-id="c65f5-146">Turn on the account correspondence mechanism for accounting transactions</span></span> 

<span data-ttu-id="c65f5-147">Механизм соответствия счетов позволяет создавать корреспондентские связи между проводками.</span><span class="sxs-lookup"><span data-stu-id="c65f5-147">The account correspondence mechanism lets you create correspondence relations between transactions.</span></span> <span data-ttu-id="c65f5-148">Выполните следующие действия, чтобы включить его.</span><span class="sxs-lookup"><span data-stu-id="c65f5-148">Follow these steps to turn it on.</span></span>

1. <span data-ttu-id="c65f5-149">Перейдите в раздел **Главная книга** \> **Настройка главной книги** \> **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="c65f5-149">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="c65f5-150">На вкладке **Главная книга** задайте для параметра **Использовать механизм корреспонденции счетов** значение **Да**, чтобы включить механизм корреспонденции счетов.</span><span class="sxs-lookup"><span data-stu-id="c65f5-150">On the **Ledger** tab, set the **Use corresponding mechanism** option to **Yes** to turn on the account correspondence mechanism.</span></span>

> [!NOTE]
> <span data-ttu-id="c65f5-151">После включения механизма соответствия все новые проводки будут иметь корреспондентские связи.</span><span class="sxs-lookup"><span data-stu-id="c65f5-151">After the correspondence mechanism is turned on, all new transactions will have correspondence relations.</span></span> <span data-ttu-id="c65f5-152">Если для проводки невозможно установить корреспондентскую связь, вы получите сообщение с предупреждением.</span><span class="sxs-lookup"><span data-stu-id="c65f5-152">If you can't establish a correspondence link for a transaction, you receive a warning message.</span></span> <span data-ttu-id="c65f5-153">Выберите это сообщение, чтобы использовать функцию корреспонденции проводок в ручном режиме для корреспондирования проводок вручную.</span><span class="sxs-lookup"><span data-stu-id="c65f5-153">Select this message to use the manual transaction correspondence function to manually correspond the transactions.</span></span>

## <a name="manually-define-correspondence-relations-for-transactions"></a><span data-ttu-id="c65f5-154">Вручную определите корреспондирующие отношения для проводок</span><span class="sxs-lookup"><span data-stu-id="c65f5-154">Manually define correspondence relations for transactions</span></span>

<span data-ttu-id="c65f5-155">Используйте функцию корреспонденции проводок вручную для определения связей между некорреспондирующими проводками.</span><span class="sxs-lookup"><span data-stu-id="c65f5-155">Use the manual transaction correspondence function to define a relationship between non-corresponding transactions.</span></span> <span data-ttu-id="c65f5-156">Если механизм корреспондирования счетов в главной книге отключен, все проводки создаются обычным образом.</span><span class="sxs-lookup"><span data-stu-id="c65f5-156">When the account correspondence mechanism is turned off in the ledger, all transactions are generated in the usual way.</span></span> <span data-ttu-id="c65f5-157">Никакая корреспондирующая связь между счетами не устанавливается.</span><span class="sxs-lookup"><span data-stu-id="c65f5-157">No correspondence link is established between accounts.</span></span> <span data-ttu-id="c65f5-158">Функция корреспонденции проводок ручную не имеет обратной силы.</span><span class="sxs-lookup"><span data-stu-id="c65f5-158">The manual transaction correspondence function isn't retroactive.</span></span> <span data-ttu-id="c65f5-159">Когда механизм корреспондирования счетов включен, корреспондирование не устанавливается для проводок, которые были выполнены ранее.</span><span class="sxs-lookup"><span data-stu-id="c65f5-159">When the account correspondence mechanism is turned on, correspondence isn't established for transactions that were performed earlier.</span></span>

1. <span data-ttu-id="c65f5-160">Перейдите в раздел **Главная книга** \> **Периодические задачи** \> **Ручная корреспонденция**.</span><span class="sxs-lookup"><span data-stu-id="c65f5-160">Go to **General ledger** \> **Periodic tasks** \> **Manual correspondence**.</span></span>
2. <span data-ttu-id="c65f5-161">В левой области просмотрите список операций, которые были разнесены.</span><span class="sxs-lookup"><span data-stu-id="c65f5-161">In the left pane, view the list of vouchers that have been posted.</span></span>
3. <span data-ttu-id="c65f5-162">В поле **Показать ваучеры ГК** выберите, какие ваучеры должны быть перечислены:</span><span class="sxs-lookup"><span data-stu-id="c65f5-162">In the **Show only vouchers** field, select which vouchers should be listed:</span></span>

    - <span data-ttu-id="c65f5-163">**Неоткорреспондированные** — показать только ваучеры, для которых нет соответствующих проводок ГК.</span><span class="sxs-lookup"><span data-stu-id="c65f5-163">**Not corresponded** − Show only vouchers that have no corresponding ledger transactions.</span></span>
    - <span data-ttu-id="c65f5-164">**Откорреспондированные** — показать только ваучеры, для которых есть соответствующие проводки ГК.</span><span class="sxs-lookup"><span data-stu-id="c65f5-164">**Corresponded** − Show only vouchers that have corresponding ledger transactions.</span></span>
    - <span data-ttu-id="c65f5-165">**Все** — показать все ваучеры.</span><span class="sxs-lookup"><span data-stu-id="c65f5-165">**All** − Show all vouchers.</span></span>

4. <span data-ttu-id="c65f5-166">Выберите ваучер, затем на экспресс-вкладке **Обзор** выберите проводки по ваучеру.</span><span class="sxs-lookup"><span data-stu-id="c65f5-166">Select a voucher, and then, on the **Overview** FastTab, view the voucher transactions.</span></span>
5. <span data-ttu-id="c65f5-167">На экспресс-вкладке **Корр. счет** выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="c65f5-167">On the **Offset** FastTab, follow one of these steps:</span></span>

    - <span data-ttu-id="c65f5-168">Чтобы откорреспондировать выбранные проводки дебета и кредита для выбранного ваучера, выберите строку в сетке **Проводки по дебету**, выберите строку в сетке **Проводки по кредиту**, затем выберите кнопку **\<-\>**, чтобы откорреспондировать проводки.</span><span class="sxs-lookup"><span data-stu-id="c65f5-168">To correspond selected debit and credit transactions for the selected voucher, select a row in the **Debit transactions** grid, select a row in the **Credit transactions** grid, and then select the **\<-\>** button to correspond the transactions.</span></span>

    - <span data-ttu-id="c65f5-169">Чтобы автоматически корреспондировать все проводки по кредиту и дебету для выбранного ваучера, выберите кнопку **\<\<-\>\>**.</span><span class="sxs-lookup"><span data-stu-id="c65f5-169">To automatically correspond all credit and debit transactions for the selected voucher, select the **\<\<-\>\>** button.</span></span>
    <span data-ttu-id="c65f5-170">Проводки, которые были откорреспондированы, перемещаются в сетку **Сведения**.</span><span class="sxs-lookup"><span data-stu-id="c65f5-170">Transactions that have been corresponded are moved to the **Details** grid.</span></span>
    
 <!--add here screenshot Correspondence-Offset from WI-->

7. <span data-ttu-id="c65f5-171">На экспресс-вкладке **Корр. счет** выберите **Сохранить** для сохранения результатов или **Восстановить**, чтобы отменить последнее изменение.</span><span class="sxs-lookup"><span data-stu-id="c65f5-171">On the **Offset** FastTab, select **Save** to save the results or **Restore** to cancel the last change.</span></span>
8. <span data-ttu-id="c65f5-172">В области действий выберите **Обновить данные** для обновления данных на странице **Ручная корреспонденция**.</span><span class="sxs-lookup"><span data-stu-id="c65f5-172">On the Action Pane, select **Refresh data** to update the data on the **Manual correspondence** page.</span></span>

<span data-ttu-id="c65f5-173">Чтобы удалить корреспондентские связи для ваучера, выберите ваучер в области слева, затем, на панели операций выберите **Удалить корресп.**.</span><span class="sxs-lookup"><span data-stu-id="c65f5-173">To remove the correspondence relations for a voucher, select the voucher in the left pane, and then, on the Action Pane, select **Remove ledger bond**.</span></span> <span data-ttu-id="c65f5-174">Затем выберите **Обновить данные** для обновления данных на странице.</span><span class="sxs-lookup"><span data-stu-id="c65f5-174">Then select **Refresh data** to update the data on the page.</span></span>
