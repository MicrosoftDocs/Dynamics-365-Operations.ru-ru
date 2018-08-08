--- 
title: "Ввод данных счета в модуль расчетов с поставщиками с использованием журнала утверждения"
description: "В этом руководстве по задаче показано, как использовать регистр накладных для создания накладных и последующего использования журнала утверждения для обновления счетов расходов."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: d50ad27dc70a053dbe0b6d73688cd95f09cefd11
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="43550-103">Ввод данных счета в модуль расчетов с поставщиками с использованием журнала утверждения</span><span class="sxs-lookup"><span data-stu-id="43550-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43550-104">В этом руководстве по задаче показано, как использовать регистр накладных для создания накладных и последующего использования журнала утверждения для обновления счетов расходов.</span><span class="sxs-lookup"><span data-stu-id="43550-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="43550-105">Создание и разноска накладной</span><span class="sxs-lookup"><span data-stu-id="43550-105">Create and post and invoice</span></span>
1. <span data-ttu-id="43550-106">Перейдите в раздел "Расчеты с поставщиками" > "Накладные" > "Регистр накладных".</span><span class="sxs-lookup"><span data-stu-id="43550-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="43550-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="43550-107">Click New.</span></span>
3. <span data-ttu-id="43550-108">Выберите имя регистра накладных для использования.</span><span class="sxs-lookup"><span data-stu-id="43550-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="43550-109">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="43550-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="43550-110">Щелкните "Строки", чтобы открыть регистр и ввести строки расходов.</span><span class="sxs-lookup"><span data-stu-id="43550-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="43550-111">Выберите поставщика.</span><span class="sxs-lookup"><span data-stu-id="43550-111">Select a vendor.</span></span> <span data-ttu-id="43550-112">Например, введите или выберите US-104.</span><span class="sxs-lookup"><span data-stu-id="43550-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="43550-113">В поле "Накладная" введите значение.</span><span class="sxs-lookup"><span data-stu-id="43550-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="43550-114">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="43550-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="43550-115">В поле "Кредит" введите число.</span><span class="sxs-lookup"><span data-stu-id="43550-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="43550-116">В поле "Кем утверждено" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="43550-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="43550-117">Выделите утверждающее лицо и нажмите кнопку "Выбрать", чтобы выбрать его.</span><span class="sxs-lookup"><span data-stu-id="43550-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="43550-118">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="43550-118">Click Post.</span></span>
13. <span data-ttu-id="43550-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="43550-119">Close the page.</span></span>
14. <span data-ttu-id="43550-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="43550-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="43550-121">Утверждение накладной</span><span class="sxs-lookup"><span data-stu-id="43550-121">Approve an invoice</span></span>
1. <span data-ttu-id="43550-122">Перейдите в раздел "Расчеты с поставщиками" > "Накладные" > "Утверждение накладной".</span><span class="sxs-lookup"><span data-stu-id="43550-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="43550-123">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="43550-123">Click New.</span></span>
3. <span data-ttu-id="43550-124">Выберите имя журнала утверждений накладных для использования.</span><span class="sxs-lookup"><span data-stu-id="43550-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="43550-125">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="43550-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="43550-126">Щелкните строки для отображения страницы, на которой можно будет выбрать накладные, которые требуется утвердить.</span><span class="sxs-lookup"><span data-stu-id="43550-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="43550-127">Выберите "Найти ваучеры" для отображения всех накладных, готовых к утверждению.</span><span class="sxs-lookup"><span data-stu-id="43550-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="43550-128">Пометьте созданную накладную.</span><span class="sxs-lookup"><span data-stu-id="43550-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="43550-129">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="43550-129">Click Select.</span></span>
    * <span data-ttu-id="43550-130">Выбранные выше ваучеры перемещаются в этот список после их выбора.</span><span class="sxs-lookup"><span data-stu-id="43550-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="43550-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="43550-131">Click OK.</span></span>
10. <span data-ttu-id="43550-132">Щелкните поле "Номер счета" для добавления счета расходов в накладную.</span><span class="sxs-lookup"><span data-stu-id="43550-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="43550-133">Введите номер счета и выйдите из поля.</span><span class="sxs-lookup"><span data-stu-id="43550-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="43550-134">Например, введите 600120.</span><span class="sxs-lookup"><span data-stu-id="43550-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="43550-135">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="43550-135">Click Post.</span></span>
13. <span data-ttu-id="43550-136">Щелкните "Ваучер" для просмотра разнесенных записей.</span><span class="sxs-lookup"><span data-stu-id="43550-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="43550-137">Счет утверждения ожидающих накладных реверсируется и заменяется на счет фактических расходов.</span><span class="sxs-lookup"><span data-stu-id="43550-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  


