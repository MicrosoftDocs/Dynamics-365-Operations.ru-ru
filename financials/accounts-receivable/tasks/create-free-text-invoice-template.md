--- 
title: "Создание шаблона накладных с произвольным текстом"
description: "В данной записи используется демонстрационная компания USMF."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e9c9811b348d81cd735c5b75ca48e0a56a8d52be
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="60fc8-103">Создание шаблона накладных с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="60fc8-103">Create a free text invoice template</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60fc8-104">В данной записи используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="60fc8-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="60fc8-105">Запись предназначена для пользователя, ответственного за обработку накладных расчетов с клиентами и управление ими.</span><span class="sxs-lookup"><span data-stu-id="60fc8-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="60fc8-106">Перейдите в раздел "Расчеты с клиентами" > "Накладные" > "Периодические накладные" > "Шаблоны накладных с произвольным текстом".</span><span class="sxs-lookup"><span data-stu-id="60fc8-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="60fc8-107">Используйте эту форму для создания шаблонов накладной с произвольным текстом, которые могут включать строки накладной, накладные расходы, шаблон распределения по бухгалтерским счетам и сведения о счете ГК.</span><span class="sxs-lookup"><span data-stu-id="60fc8-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="60fc8-108">Нажмите кнопку "Создать", чтобы создать новый шаблон накладных с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="60fc8-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="60fc8-109">В поле "Имя шаблона" введите значение.</span><span class="sxs-lookup"><span data-stu-id="60fc8-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="60fc8-110">Имя шаблона однозначно определяет шаблон накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="60fc8-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="60fc8-111">Два шаблона не могут иметь одинаковое "Имя шаблона".</span><span class="sxs-lookup"><span data-stu-id="60fc8-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="60fc8-112">В поле "Описание" введите описание шаблона.</span><span class="sxs-lookup"><span data-stu-id="60fc8-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="60fc8-113">Разверните вкладку "Строки накладной".</span><span class="sxs-lookup"><span data-stu-id="60fc8-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="60fc8-114">В поле "Описание" введите описание строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60fc8-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="60fc8-115">В поле "Счет ГК" выберите счет выручки.</span><span class="sxs-lookup"><span data-stu-id="60fc8-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="60fc8-116">Можно выбрать счет корреспондирующей проводки кредита клиента для итоговой суммы накладной на странице "Профили разноски клиента".</span><span class="sxs-lookup"><span data-stu-id="60fc8-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="60fc8-117">В поле "Налоговая группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="60fc8-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="60fc8-118">Налоговая группа для текущей строки накладной является налоговой группой по умолчанию для счета клиента.</span><span class="sxs-lookup"><span data-stu-id="60fc8-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="60fc8-119">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="60fc8-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="60fc8-120">В поле "Налоговая группа номенклатур" выберите налоговую группу номенклатур для текущей строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60fc8-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="60fc8-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="60fc8-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="60fc8-122">В поле "Цена за единицу" введите или просмотрите цену за единицу для строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60fc8-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="60fc8-123">Эта сумма умножается на значение в поле "Количество" для определения суммы строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60fc8-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="60fc8-124">Добавьте новую строку в накладную с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="60fc8-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="60fc8-125">В поле "Описание" введите описание строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60fc8-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="60fc8-126">В поле "Счет ГК" выберите счет выручки.</span><span class="sxs-lookup"><span data-stu-id="60fc8-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="60fc8-127">Можно выбрать счет корреспондирующей проводки кредита клиента для итоговой суммы накладной на странице "Профили разноски клиента".</span><span class="sxs-lookup"><span data-stu-id="60fc8-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="60fc8-128">В поле "Налоговая группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="60fc8-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="60fc8-129">Налоговая группа для текущей строки накладной является налоговой группой по умолчанию для счета клиента.</span><span class="sxs-lookup"><span data-stu-id="60fc8-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="60fc8-130">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="60fc8-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="60fc8-131">В поле "Налоговая группа номенклатур" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="60fc8-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="60fc8-132">Налоговая группа номенклатур для текущей строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60fc8-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="60fc8-133">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="60fc8-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="60fc8-134">Ввод или просмотр количества единиц для строки накладной</span><span class="sxs-lookup"><span data-stu-id="60fc8-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="60fc8-135">Это число умножается на значение в поле "Цена за единицу" для определения суммы строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60fc8-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="60fc8-136">Введите или просмотрите цену за единицу для строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60fc8-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="60fc8-137">Эта сумма умножается на значение в поле "Количество" для определения суммы строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60fc8-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="60fc8-138">Просмотрите и измените распределения по бухгалтерским счетам для отдельной строки и всех дочерних строк.</span><span class="sxs-lookup"><span data-stu-id="60fc8-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="60fc8-139">Распределения по бухгалтерским счетам определяют способ учета сумм, например дохода, налога или накладных расходов в накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="60fc8-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="60fc8-140">Обновите распределения по бухгалтерским счетам для выбранной строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60fc8-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="60fc8-141">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="60fc8-141">Click Close.</span></span>


