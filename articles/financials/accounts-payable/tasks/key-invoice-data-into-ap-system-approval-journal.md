---
title: Ключевые сведения по накладной в систему расчетов с поставщиками с использованием журнала утверждения
description: В этом руководстве по задаче показано, как использовать регистр накладных для создания накладных и последующего использования журнала утверждения для обновления счетов расходов.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 048eda77064b6aa3f666e998a8e551d2f7adc385
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550382"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a><span data-ttu-id="c19d5-103">Ключевые сведения по накладной в систему расчетов с поставщиками с использованием журнала утверждения</span><span class="sxs-lookup"><span data-stu-id="c19d5-103">Key invoice data into AP system using approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c19d5-104">В этом руководстве по задаче показано, как использовать регистр накладных для создания накладных и последующего использования журнала утверждения для обновления счетов расходов.</span><span class="sxs-lookup"><span data-stu-id="c19d5-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="c19d5-105">Создание и разноска накладной</span><span class="sxs-lookup"><span data-stu-id="c19d5-105">Create and post and invoice</span></span>
1. <span data-ttu-id="c19d5-106">Перейдите в раздел "Расчеты с поставщиками" > "Накладные" > "Регистр накладных".</span><span class="sxs-lookup"><span data-stu-id="c19d5-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="c19d5-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c19d5-107">Click New.</span></span>
3. <span data-ttu-id="c19d5-108">Выберите имя регистра накладных для использования.</span><span class="sxs-lookup"><span data-stu-id="c19d5-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="c19d5-109">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c19d5-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c19d5-110">Щелкните "Строки", чтобы открыть регистр и ввести строки расходов.</span><span class="sxs-lookup"><span data-stu-id="c19d5-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="c19d5-111">Выберите поставщика.</span><span class="sxs-lookup"><span data-stu-id="c19d5-111">Select a vendor.</span></span> <span data-ttu-id="c19d5-112">Например, введите или выберите US-104.</span><span class="sxs-lookup"><span data-stu-id="c19d5-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="c19d5-113">В поле "Накладная" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c19d5-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="c19d5-114">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c19d5-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="c19d5-115">В поле "Кредит" введите число.</span><span class="sxs-lookup"><span data-stu-id="c19d5-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="c19d5-116">В поле "Кем утверждено" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c19d5-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="c19d5-117">Выделите утверждающее лицо и нажмите кнопку "Выбрать", чтобы выбрать его.</span><span class="sxs-lookup"><span data-stu-id="c19d5-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="c19d5-118">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="c19d5-118">Click Post.</span></span>
13. <span data-ttu-id="c19d5-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c19d5-119">Close the page.</span></span>
14. <span data-ttu-id="c19d5-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c19d5-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="c19d5-121">Утверждение накладной</span><span class="sxs-lookup"><span data-stu-id="c19d5-121">Approve an invoice</span></span>
1. <span data-ttu-id="c19d5-122">Перейдите в раздел "Расчеты с поставщиками" > "Накладные" > "Утверждение накладной".</span><span class="sxs-lookup"><span data-stu-id="c19d5-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="c19d5-123">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c19d5-123">Click New.</span></span>
3. <span data-ttu-id="c19d5-124">Выберите имя журнала утверждений накладных для использования.</span><span class="sxs-lookup"><span data-stu-id="c19d5-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="c19d5-125">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c19d5-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c19d5-126">Щелкните строки для отображения страницы, на которой можно будет выбрать накладные, которые требуется утвердить.</span><span class="sxs-lookup"><span data-stu-id="c19d5-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="c19d5-127">Выберите "Найти ваучеры" для отображения всех накладных, готовых к утверждению.</span><span class="sxs-lookup"><span data-stu-id="c19d5-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="c19d5-128">Пометьте созданную накладную.</span><span class="sxs-lookup"><span data-stu-id="c19d5-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="c19d5-129">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="c19d5-129">Click Select.</span></span>
    * <span data-ttu-id="c19d5-130">Выбранные выше ваучеры перемещаются в этот список после их выбора.</span><span class="sxs-lookup"><span data-stu-id="c19d5-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="c19d5-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c19d5-131">Click OK.</span></span>
10. <span data-ttu-id="c19d5-132">Щелкните поле "Номер счета" для добавления счета расходов в накладную.</span><span class="sxs-lookup"><span data-stu-id="c19d5-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="c19d5-133">Введите номер счета и выйдите из поля.</span><span class="sxs-lookup"><span data-stu-id="c19d5-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="c19d5-134">Например, введите 600120.</span><span class="sxs-lookup"><span data-stu-id="c19d5-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="c19d5-135">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="c19d5-135">Click Post.</span></span>
13. <span data-ttu-id="c19d5-136">Щелкните "Ваучер" для просмотра разнесенных записей.</span><span class="sxs-lookup"><span data-stu-id="c19d5-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="c19d5-137">Счет утверждения ожидающих накладных реверсируется и заменяется на счет фактических расходов.</span><span class="sxs-lookup"><span data-stu-id="c19d5-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

