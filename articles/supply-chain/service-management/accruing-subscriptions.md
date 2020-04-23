---
title: Начисление подписок
description: С помощью подписок на обслуживание можно вручную начислять доход в периодах, следующих за датой выставления накладной по проводке по сборам.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9fba99eeea605f35abfe00068fe9a4cda4db0b6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203120"
---
# <a name="accruing-subscriptions"></a><span data-ttu-id="4f078-103">Начисление подписок</span><span class="sxs-lookup"><span data-stu-id="4f078-103">Accruing subscriptions</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="4f078-104">С помощью подписок на обслуживание можно вручную начислять доход в периодах, следующих за датой выставления накладной по проводке по сборам.</span><span class="sxs-lookup"><span data-stu-id="4f078-104">With service subscriptions, you manually accrue revenue in the periods following the date when you invoiced a fee transaction.</span></span>

<span data-ttu-id="4f078-105">Периоды начисления создаются для периода накладной, который настраивается для проводки по сборам. Периоды начисления основываются на коде периода для подписки.</span><span class="sxs-lookup"><span data-stu-id="4f078-105">Accrual periods are created for the invoice period that you set up for the subscription fee, and the accrual periods are based on the period code of the subscription.</span></span>

<span data-ttu-id="4f078-106">Можно выполнить начисление и сторнировать начисленный доход.</span><span class="sxs-lookup"><span data-stu-id="4f078-106">You can accrue and reverse accrued revenue.</span></span>

## <a name="reverse-accruals-of-credit-amounts"></a><span data-ttu-id="4f078-107">Реверсирование начислений сумм кредитов</span><span class="sxs-lookup"><span data-stu-id="4f078-107">Reverse accruals of credit amounts</span></span>

<span data-ttu-id="4f078-108">Если кредитуются суммы накладной по подписке, можно использовать 2 метода для реверсирования сумм начисления:</span><span class="sxs-lookup"><span data-stu-id="4f078-108">If you credit invoiced subscription amounts, you can use two methods to reverse the accrual amounts:</span></span>

  - <span data-ttu-id="4f078-109">Можно выполнить реверсирование каждой проводки по начисленному доходу по отдельности перед созданием предложения кредит-ноты для этой проводки.</span><span class="sxs-lookup"><span data-stu-id="4f078-109">You can reverse each accrued revenue transaction individually before you create the credit note proposal for the transaction.</span></span> <span data-ttu-id="4f078-110">Это ручной метод.</span><span class="sxs-lookup"><span data-stu-id="4f078-110">This is the manual method.</span></span> <span data-ttu-id="4f078-111">(вручную)</span><span class="sxs-lookup"><span data-stu-id="4f078-111">(manual)</span></span>

  - <span data-ttu-id="4f078-112">Можно выполнить реверсирование начисленных сумм по дате, когда разносится кредит-нота, или по первоначальной дате начисления.</span><span class="sxs-lookup"><span data-stu-id="4f078-112">You can have the accrued amounts reversed on the date where the credit note is posted or on the original posting date of the accrual.</span></span>

<span data-ttu-id="4f078-113">Дополнительные сведения см. в разделе [Параметры подписки (форма)](https://technet.microsoft.com/library/aa619615.aspx).</span><span class="sxs-lookup"><span data-stu-id="4f078-113">For more information, see [Subscription parameters (form)](https://technet.microsoft.com/library/aa619615.aspx).</span></span>

## <a name="setup-requirements"></a><span data-ttu-id="4f078-114">Требования для настройки</span><span class="sxs-lookup"><span data-stu-id="4f078-114">Setup requirements</span></span>

<span data-ttu-id="4f078-115">Чтобы начислить доход, убедитесь, что выполняются следующие требования к данным.</span><span class="sxs-lookup"><span data-stu-id="4f078-115">To accrue revenue, make sure that the following data requirements are met:</span></span>

## <a name="account-setup"></a><span data-ttu-id="4f078-116">Настройка счета</span><span class="sxs-lookup"><span data-stu-id="4f078-116">Account setup</span></span>

<span data-ttu-id="4f078-117">Должны быть настроены счета **НЗП - подписка** и **Начисленная выручка - подписка** в модуле **Проект**.</span><span class="sxs-lookup"><span data-stu-id="4f078-117">The **WIP - subscription** and the **Accrued revenue - subscription** accounts must be set up in the **Project** module.</span></span>

<span data-ttu-id="4f078-118">При разноске начисленного дохода счет **НЗП - подписка** дебетуется на сумму начисления, а счет **Начисленная выручка - подписка** кредитуется на сумму начисления.</span><span class="sxs-lookup"><span data-stu-id="4f078-118">When you post accrued revenue, the **WIP - subscription** account is debited with the accrual amount, and the **Accrued revenue - subscription** account is credited with the accrual amount.</span></span>

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a><span data-ttu-id="4f078-119">Настройка счетов для начисления дохода для подписки</span><span class="sxs-lookup"><span data-stu-id="4f078-119">Set up accounts for accrual of subscription revenue</span></span>

1.  <span data-ttu-id="4f078-120">Щелкните **Управление и учет по проектам** \> **Настройка** \> **Разноска** \> **Настройка разноски ГК**.</span><span class="sxs-lookup"><span data-stu-id="4f078-120">Click **Project management and accounting** \> **Setup** \> **Posting** \> **Ledger posting setup**.</span></span>

2.  <span data-ttu-id="4f078-121">Перейдите на вкладку **Счета выручки** и выберите **НЗП - подписка** или **Начисленная выручка - подписка**, чтобы настроить счета.</span><span class="sxs-lookup"><span data-stu-id="4f078-121">Click the **Revenue accounts** tab, and select **WIP - subscription** or **Accrued revenue - subscription** to set up the accounts.</span></span>

## <a name="subscription-group-setup"></a><span data-ttu-id="4f078-122">Настройка группы подписок</span><span class="sxs-lookup"><span data-stu-id="4f078-122">Subscription group setup</span></span>

<span data-ttu-id="4f078-123">Для обеспечения возможности начисления выручки по подпискам должен быть установлен флажок **Начислить выручку**.</span><span class="sxs-lookup"><span data-stu-id="4f078-123">To be able to accrue revenue for subscriptions, the **Accrue revenue** check box must be selected.</span></span> <span data-ttu-id="4f078-124">Он находится в форме **Группы подписки** для группы, которая присоединена к подписке.</span><span class="sxs-lookup"><span data-stu-id="4f078-124">This is found on the **Subscription groups** form for the group that is attached to the subscription.</span></span> <span data-ttu-id="4f078-125">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Подписки на сервисное обслуживание** \> **Группы подписки**.</span><span class="sxs-lookup"><span data-stu-id="4f078-125">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="enable-revenue-accrual-on-a-subscription-group"></a><span data-ttu-id="4f078-126">Включение начисления дохода в группе подписок</span><span class="sxs-lookup"><span data-stu-id="4f078-126">Enable revenue accrual on a subscription group</span></span>

1.  <span data-ttu-id="4f078-127">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Подписки на сервисное обслуживание** \> **Группы подписки**.</span><span class="sxs-lookup"><span data-stu-id="4f078-127">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="periods"></a><span data-ttu-id="4f078-128">Периоды</span><span class="sxs-lookup"><span data-stu-id="4f078-128">Periods</span></span>

<span data-ttu-id="4f078-129">Следует настроить код периода выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="4f078-129">You must set up an invoicing period code.</span></span> <span data-ttu-id="4f078-130">Также необходимо настроить период начисления, если начисление дохода будет производиться не в тех же временных интервалах, которые использованы для выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="4f078-130">Unless you want to accrue revenue in the same time intervals as you use for invoicing, you must also set up an accrual period.</span></span>

<span data-ttu-id="4f078-131">В следующей таблице приводятся общие сведения о том, какие периоды начислений могут быть настроены для каждого периода обработки накладной.</span><span class="sxs-lookup"><span data-stu-id="4f078-131">The following table provides an overview of which accrual periods can be set up for each invoicing period:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f078-132">Период выписки накладной</span><span class="sxs-lookup"><span data-stu-id="4f078-132">Invoicing period</span></span></p></th>
<th><p><span data-ttu-id="4f078-133">Период начисления</span><span class="sxs-lookup"><span data-stu-id="4f078-133">Accrual period</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f078-134"><strong>Годы</strong></span><span class="sxs-lookup"><span data-stu-id="4f078-134"><strong>Years</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="4f078-135"><strong>Годы</strong></span><span class="sxs-lookup"><span data-stu-id="4f078-135"><strong>Years</strong></span></span></p></li>
<li><p><span data-ttu-id="4f078-136"><strong>Квартал</strong></span><span class="sxs-lookup"><span data-stu-id="4f078-136"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="4f078-137"><strong>Месяц</strong></span><span class="sxs-lookup"><span data-stu-id="4f078-137"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="4f078-138"><strong>день</strong></span><span class="sxs-lookup"><span data-stu-id="4f078-138"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f078-139"><strong>Квартал</strong></span><span class="sxs-lookup"><span data-stu-id="4f078-139"><strong>Quarter</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="4f078-140"><strong>Квартал</strong></span><span class="sxs-lookup"><span data-stu-id="4f078-140"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="4f078-141"><strong>Месяц</strong></span><span class="sxs-lookup"><span data-stu-id="4f078-141"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="4f078-142"><strong>день</strong></span><span class="sxs-lookup"><span data-stu-id="4f078-142"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f078-143"><strong>Месяц</strong></span><span class="sxs-lookup"><span data-stu-id="4f078-143"><strong>Month</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="4f078-144"><strong>Месяц</strong></span><span class="sxs-lookup"><span data-stu-id="4f078-144"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="4f078-145"><strong>день</strong></span><span class="sxs-lookup"><span data-stu-id="4f078-145"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f078-146"><strong>Неделя</strong></span><span class="sxs-lookup"><span data-stu-id="4f078-146"><strong>Week</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="4f078-147"><strong>день</strong></span><span class="sxs-lookup"><span data-stu-id="4f078-147"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f078-148"><strong>день</strong></span><span class="sxs-lookup"><span data-stu-id="4f078-148"><strong>Day</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="4f078-149"><strong>день</strong></span><span class="sxs-lookup"><span data-stu-id="4f078-149"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4f078-150">Настройка периода выставления накладных является обязательной частью общей настройки групп подписок.</span><span class="sxs-lookup"><span data-stu-id="4f078-150">Setting up the invoicing period is a mandatory part of the overall subscription group setup.</span></span> <span data-ttu-id="4f078-151">Также можно определить, необходимо ли настроить период начисления для группы подписок.</span><span class="sxs-lookup"><span data-stu-id="4f078-151">You can decide whether to also set up an accrual period for the subscription group.</span></span> <span data-ttu-id="4f078-152">Если настраивается период начисления для группы подписок, этот период предлагается в поле **Код периода**.</span><span class="sxs-lookup"><span data-stu-id="4f078-152">If you set up an accrual period for the subscription group, this period is suggested in the **Period code** field.</span></span> <span data-ttu-id="4f078-153">Это поле находится в форме **Начисление выручки по подписке**, когда начисляется выручка по подписке.</span><span class="sxs-lookup"><span data-stu-id="4f078-153">This field is found in the **Accrue subscription revenue** form, when you accrue subscription revenue.</span></span> <span data-ttu-id="4f078-154">Однако период начисления — это дополнительная информация о группе подписок.</span><span class="sxs-lookup"><span data-stu-id="4f078-154">However, the accrual period is optional information about the subscription group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4f078-155">Используйте следующий путь, чтобы открыть форму <STRONG>Начисление выручки по подписке</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="4f078-155">Use the following path to open the <STRONG>Accrue subscription revenue</STRONG> form.</span></span> <span data-ttu-id="4f078-156">Щелкните <STRONG>Управление сервисным обслуживанием</STRONG> &gt; <STRONG>Периодические операции</STRONG> &gt; <STRONG>Подписки на сервисное обслуживание</STRONG> &gt; <STRONG>Начисление выручки по подписке</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="4f078-156">Click <STRONG>Service management</STRONG> &gt; <STRONG>Periodic</STRONG> &gt; <STRONG>Service subscriptions</STRONG> &gt; <STRONG>Accrue subscription revenue</STRONG>.</span></span></P>


## <a name="transactions"></a><span data-ttu-id="4f078-157">Транзакции</span><span class="sxs-lookup"><span data-stu-id="4f078-157">Transactions</span></span>

<span data-ttu-id="4f078-158">Можно регулировать количество проводок ГК, которые создаются при разноске начисленной выручки.</span><span class="sxs-lookup"><span data-stu-id="4f078-158">You can control the number of ledger transactions that are created when you post accrued revenue.</span></span> <span data-ttu-id="4f078-159">В подписках укажите, должны ли проводки ГК должны создаваться по итоговому значению или по строкам.</span><span class="sxs-lookup"><span data-stu-id="4f078-159">On subscriptions, define if the ledger transactions should be created as a total or per line.</span></span>

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a><span data-ttu-id="4f078-160">Указание уровня данных разноски, которые будут отображаться для проводок начисления</span><span class="sxs-lookup"><span data-stu-id="4f078-160">Specify the level of posting details to display for accrued transactions</span></span>

1.  <span data-ttu-id="4f078-161">Щелкните **Управление и учет по проектам** \> **Настройка** \> **Параметры модуля "Управление и учет по проектам"**.</span><span class="sxs-lookup"><span data-stu-id="4f078-161">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="4f078-162">На вкладке **Финансы** в поле **Накладная** выберите **Итог** или **Строка**.</span><span class="sxs-lookup"><span data-stu-id="4f078-162">On the **Financial** tab, in the **Invoice** field, select **Total** or **Line**.</span></span>


## <a name="see-also"></a><span data-ttu-id="4f078-163">См. также</span><span class="sxs-lookup"><span data-stu-id="4f078-163">See also</span></span>

[<span data-ttu-id="4f078-164">Начислить выручку по подписке</span><span class="sxs-lookup"><span data-stu-id="4f078-164">Accrue subscription revenue</span></span>](accrue-subscription-revenue.md)

  


