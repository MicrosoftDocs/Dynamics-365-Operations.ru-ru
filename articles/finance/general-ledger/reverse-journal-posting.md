---
title: Сторнирование разноски журнала
description: В этой теме описываются возможности, позволяющие сторнировать ваучеры из списка проводок по ваучеру или из финансовых журналов.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248593"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="bf066-103">Сторнирование разноски журнала</span><span class="sxs-lookup"><span data-stu-id="bf066-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf066-104">В этой теме описываются возможности Microsoft Dynamics 365 Finance, которые позволяют сторнировать весь журнал или сторнировать один или несколько ваучеров из списка проводок ваучера, независимо от их происхождения.</span><span class="sxs-lookup"><span data-stu-id="bf066-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="bf066-105">Сторнирование журналов</span><span class="sxs-lookup"><span data-stu-id="bf066-105">Reversing journals</span></span>

<span data-ttu-id="bf066-106">Строки журнала можно сторнировать по отдельности.</span><span class="sxs-lookup"><span data-stu-id="bf066-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="bf066-107">При сторнировании проводок журнала можно также сторнировать весь финансовый журнал.</span><span class="sxs-lookup"><span data-stu-id="bf066-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="bf066-108">Чтобы сторнировать журнал:</span><span class="sxs-lookup"><span data-stu-id="bf066-108">To reverse a journal:</span></span> 
- <span data-ttu-id="bf066-109">Откройте финансовый журнал и отфильтруйте разнесенные журналы</span><span class="sxs-lookup"><span data-stu-id="bf066-109">Open the financial journal and filter on posted journals</span></span>
- <span data-ttu-id="bf066-110">Щелкните на меню сторнирования в верхней части страницы</span><span class="sxs-lookup"><span data-stu-id="bf066-110">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="bf066-111">Вы увидите общее число операций и строк операций, а также общую сумму сторнируемых строк</span><span class="sxs-lookup"><span data-stu-id="bf066-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="bf066-112">Выберите "Да", чтобы использовать существующие даты проводок или "Нет", чтобы ввести новые.</span><span class="sxs-lookup"><span data-stu-id="bf066-112">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="bf066-113">В некоторых случаях период исходной проводки может быть закрыт и необходимо ввести новую дату проводки для сторнирования.</span><span class="sxs-lookup"><span data-stu-id="bf066-113">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="bf066-114">Если вы выбрали "Нет", введите дату проводки для сторнирования.</span><span class="sxs-lookup"><span data-stu-id="bf066-114">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="bf066-115">Введите комментарий, который необходимо добавить к сторнирующей проводке</span><span class="sxs-lookup"><span data-stu-id="bf066-115">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="bf066-116">Нажмите кнопку "Сторнировать"</span><span class="sxs-lookup"><span data-stu-id="bf066-116">Click the Reverse button</span></span>

<span data-ttu-id="bf066-117">Проводки будут сторнированы.</span><span class="sxs-lookup"><span data-stu-id="bf066-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="bf066-118">Если количество строк операций превышает 100, процесс сторнирования будет выполняться с использованием процесса пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="bf066-118">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="bf066-119">Просмотреть результаты сторнирования можно, просмотрев комментарии в пакетном задании, которое было выполнено.</span><span class="sxs-lookup"><span data-stu-id="bf066-119">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="bf066-120">Все ошибки будут отмечены в журнале пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="bf066-120">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="bf066-121">Если количество строк операций составляет 100 строк или меньше, процесс сторнирования будет выполнен немедленно.</span><span class="sxs-lookup"><span data-stu-id="bf066-121">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="bf066-122">Результаты будут представлены в диалоговом окне с указанием любой операции, которая не может быть сторнирована, и причины, по которой ее невозможно сторнировать.</span><span class="sxs-lookup"><span data-stu-id="bf066-122">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="bf066-123">Нажмите кнопку OK, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="bf066-123">Click on Ok to close the dialog.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="bf066-124">Сторнирование операций из списка проводок по ваучерам.</span><span class="sxs-lookup"><span data-stu-id="bf066-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="bf066-125">Кроме того, можно сторнировать ваучеры из **Списка проводок по ваучеру** по всем вспомогательным книгам.</span><span class="sxs-lookup"><span data-stu-id="bf066-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="bf066-126">Кроме того, можно выполнить сторнирование более одного ваучера за раз.</span><span class="sxs-lookup"><span data-stu-id="bf066-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="bf066-127">Чтобы сторнировать один или несколько ваучеров:</span><span class="sxs-lookup"><span data-stu-id="bf066-127">To reverse one or more vouchers:</span></span> 
- <span data-ttu-id="bf066-128">Щелкните на меню сторнирования в верхней части страницы</span><span class="sxs-lookup"><span data-stu-id="bf066-128">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="bf066-129">Вы увидите общее число операций и строк операций, а также общую сумму сторнируемых строк</span><span class="sxs-lookup"><span data-stu-id="bf066-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="bf066-130">Выберите "Да", чтобы использовать существующие даты проводок или "Нет", чтобы ввести новые.</span><span class="sxs-lookup"><span data-stu-id="bf066-130">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="bf066-131">В некоторых случаях период исходной проводки может быть закрыт и необходимо ввести новую дату проводки для сторнирования.</span><span class="sxs-lookup"><span data-stu-id="bf066-131">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="bf066-132">Если вы выбрали "Нет", введите дату проводки для сторнирования.</span><span class="sxs-lookup"><span data-stu-id="bf066-132">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="bf066-133">Введите комментарий, который необходимо добавить к сторнирующей проводке</span><span class="sxs-lookup"><span data-stu-id="bf066-133">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="bf066-134">Нажмите кнопку "Сторнировать"</span><span class="sxs-lookup"><span data-stu-id="bf066-134">Click the Reverse button</span></span>

<span data-ttu-id="bf066-135">Проводки будут сторнированы.</span><span class="sxs-lookup"><span data-stu-id="bf066-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="bf066-136">Если количество строк операций превышает 100, процесс сторнирования будет выполняться с использованием процесса пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="bf066-136">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="bf066-137">Просмотреть результаты сторнирования можно, просмотрев комментарии в пакетном задании, которое было выполнено.</span><span class="sxs-lookup"><span data-stu-id="bf066-137">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="bf066-138">Все ошибки будут отмечены в журнале пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="bf066-138">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="bf066-139">Если количество строк операций составляет 100 строк или меньше, процесс сторнирования будет выполнен немедленно.</span><span class="sxs-lookup"><span data-stu-id="bf066-139">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="bf066-140">Результаты будут представлены в диалоговом окне с указанием любой операции, которая не может быть сторнирована, и причины, по которой ее невозможно сторнировать.</span><span class="sxs-lookup"><span data-stu-id="bf066-140">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="bf066-141">Нажмите кнопку OK, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="bf066-141">Click on Ok to close the dialog.</span></span>

