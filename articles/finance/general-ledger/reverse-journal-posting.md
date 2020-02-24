---
title: Сторнирование разноски журнала
description: В этой теме описываются возможности, позволяющие сторнировать ваучеры из списка проводок по ваучеру или из финансовых журналов.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08aec836ce4b7b6a59c445f138365f101a78c68e
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030930"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="ccf3e-103">Сторнирование разноски журнала</span><span class="sxs-lookup"><span data-stu-id="ccf3e-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ccf3e-104">В этой теме описываются возможности Microsoft Dynamics 365 Finance, которые позволяют сторнировать весь журнал или сторнировать один или несколько ваучеров из списка проводок ваучера, независимо от их происхождения.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="ccf3e-105">Сторнирование журналов</span><span class="sxs-lookup"><span data-stu-id="ccf3e-105">Reversing journals</span></span>

<span data-ttu-id="ccf3e-106">Строки журнала можно сторнировать по отдельности.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="ccf3e-107">При сторнировании проводок журнала можно также сторнировать весь финансовый журнал.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="ccf3e-108">Чтобы сторнировать журнал:</span><span class="sxs-lookup"><span data-stu-id="ccf3e-108">To reverse a journal:</span></span> 

- <span data-ttu-id="ccf3e-109">Откройте финансовый журнал и отфильтруйте разнесенные журналы.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="ccf3e-110">Выберите меню **Реверсировать** в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="ccf3e-111">Вы увидите общее число операций и строк операций, а также общую сумму сторнируемых строк</span><span class="sxs-lookup"><span data-stu-id="ccf3e-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="ccf3e-112">Выберите **Да**, чтобы использовать существующие даты проводок или **Нет**, чтобы ввести новые.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="ccf3e-113">В некоторых случаях период исходной проводки может быть закрыт и необходимо ввести новую дату проводки для сторнирования.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="ccf3e-114">Если вы выбрали **Нет**, введите дату проводки для реверсирования.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="ccf3e-115">Введите комментарий, который необходимо добавить к реверсирующей проводке.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="ccf3e-116">Выберите кнопку **Реверсировать**.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="ccf3e-117">Проводки будут сторнированы.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="ccf3e-118">Если ваучер содержит более 100 строк, процесс реверсирования будет выполняться с использованием процесса пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="ccf3e-119">Просмотреть результаты реверсирования можно, просмотрев комментарии в пакетном задании.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="ccf3e-120">Любые проводки, которые не могут быть реверсированы, будут включены в журнал пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="ccf3e-121">Если ваучер содержит 100 строк или менее, процесс реверсирования будет выполнен немедленно.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="ccf3e-122">Результаты будут представлены в диалоговом окне с указанием любого ваучера, который не может быть реверсирован, и причины, по которой его невозможно реверсировать.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="ccf3e-123">Выберите **OK**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="ccf3e-124">Сторнирование операций из списка проводок по ваучерам.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="ccf3e-125">Кроме того, можно сторнировать ваучеры из **Списка проводок по ваучеру** по всем вспомогательным книгам.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="ccf3e-126">Кроме того, можно выполнить сторнирование более одного ваучера за раз.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="ccf3e-127">Чтобы сторнировать один или несколько ваучеров:</span><span class="sxs-lookup"><span data-stu-id="ccf3e-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="ccf3e-128">Выберите меню **Реверсировать** в верхней части страницы</span><span class="sxs-lookup"><span data-stu-id="ccf3e-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="ccf3e-129">Вы увидите общее число ваучеров и строк ваучеров, а также общую сумму реверсируемых строк.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="ccf3e-130">Выберите **Да**, чтобы использовать существующие даты проводок или **Нет**, чтобы ввести новые.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="ccf3e-131">В некоторых случаях период исходной проводки может быть закрыт и необходимо ввести новую дату проводки для реверсирования.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="ccf3e-132">Если вы выбрали **Нет**, введите дату проводки для реверсирования.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="ccf3e-133">Ввод комментария для описания реверсированной проводки.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="ccf3e-134">Выберите кнопку **Реверсировать**.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="ccf3e-135">Проводки будут сторнированы.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="ccf3e-136">Если содержится более 100 строк ваучера, процесс реверсирования будет выполняться с использованием процесса пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="ccf3e-137">Просмотреть результаты реверсирования можно, просмотрев комментарии в пакетном задании.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="ccf3e-138">Любые проводки, которые не могут быть реверсированы, будут указаны в журнале пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="ccf3e-139">Если количество строк ваучера составляет 100 строк или менее, процесс реверсирования будет выполнен немедленно.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="ccf3e-140">Результаты будут отображены в диалоговом окне с указанием любого ваучера, который не может быть реверсирован, и причины, по которой его невозможно реверсировать.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="ccf3e-141">Выберите **OK**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="ccf3e-142">Проводки могут быть реверсированы только в том случае, если они соответствуют бизнес-правилам для реверсирования.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="ccf3e-143">Невозможно реверсировать платежи поставщика, используя возможности, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="ccf3e-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="ccf3e-144">Платежи поставщика необходимо реверсировать, выполнив шаги, перечисленные в поле [Реверсирование платежа поставщику](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span><span class="sxs-lookup"><span data-stu-id="ccf3e-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>

