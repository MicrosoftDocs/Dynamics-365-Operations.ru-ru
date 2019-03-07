---
title: Создание шаблона накладных с произвольным текстом
description: Эта процедура показывает, как создать шаблона периодической накладной с произвольным текстом.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91f2ec2f8ab21616c6a1b886ee89d6faf84023e4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "310791"
---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="60d9b-103">Создание шаблона накладных с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="60d9b-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60d9b-104">В данном примере используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="60d9b-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="60d9b-105">Эта процедура предназначена для пользователя, ответственного за обработку накладных расчетов с клиентами и управление ими.</span><span class="sxs-lookup"><span data-stu-id="60d9b-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="60d9b-106">Создать шаблон</span><span class="sxs-lookup"><span data-stu-id="60d9b-106">Create a template</span></span>

1. <span data-ttu-id="60d9b-107">Перейдите в раздел "Расчеты с клиентами" > "Накладные" > "Периодические накладные" > "Шаблоны накладных с произвольным текстом".</span><span class="sxs-lookup"><span data-stu-id="60d9b-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="60d9b-108">Используйте эту форму для создания шаблонов накладной с произвольным текстом, которые могут включать строки накладной, накладные расходы, шаблон распределения по бухгалтерским счетам и сведения о счете ГК.</span><span class="sxs-lookup"><span data-stu-id="60d9b-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="60d9b-109">Нажмите кнопку "Создать", чтобы создать новый шаблон накладных с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="60d9b-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="60d9b-110">В поле "Имя шаблона" введите значение.</span><span class="sxs-lookup"><span data-stu-id="60d9b-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="60d9b-111">Имя шаблона однозначно определяет шаблон накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="60d9b-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="60d9b-112">Два шаблона не могут иметь одинаковое "Имя шаблона".</span><span class="sxs-lookup"><span data-stu-id="60d9b-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="60d9b-113">В поле "Описание" введите описание шаблона.</span><span class="sxs-lookup"><span data-stu-id="60d9b-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="60d9b-114">Разверните вкладку "Строки накладной".</span><span class="sxs-lookup"><span data-stu-id="60d9b-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="60d9b-115">В поле "Описание" введите описание строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60d9b-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="60d9b-116">В поле "Счет ГК" выберите счет выручки.</span><span class="sxs-lookup"><span data-stu-id="60d9b-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="60d9b-117">Можно выбрать счет корреспондирующей проводки кредита клиента для итоговой суммы накладной на странице "Профили разноски клиента".</span><span class="sxs-lookup"><span data-stu-id="60d9b-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="60d9b-118">В поле "Налоговая группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="60d9b-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="60d9b-119">Налоговая группа для текущей строки накладной является налоговой группой по умолчанию для счета клиента.</span><span class="sxs-lookup"><span data-stu-id="60d9b-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="60d9b-120">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="60d9b-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="60d9b-121">В поле "Налоговая группа номенклатур" выберите налоговую группу номенклатур для текущей строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60d9b-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="60d9b-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="60d9b-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="60d9b-123">В поле "Цена за единицу" введите или просмотрите цену за единицу для строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60d9b-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="60d9b-124">Эта сумма умножается на значение в поле "Количество" для определения суммы строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60d9b-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="60d9b-125">Добавьте новую строку в накладную с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="60d9b-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="60d9b-126">В поле "Описание" введите описание строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60d9b-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="60d9b-127">В поле "Счет ГК" выберите счет выручки.</span><span class="sxs-lookup"><span data-stu-id="60d9b-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="60d9b-128">Можно выбрать счет корреспондирующей проводки кредита клиента для итоговой суммы накладной на странице "Профили разноски клиента".</span><span class="sxs-lookup"><span data-stu-id="60d9b-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="60d9b-129">В поле "Налоговая группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="60d9b-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="60d9b-130">Налоговая группа для текущей строки накладной является налоговой группой по умолчанию для счета клиента.</span><span class="sxs-lookup"><span data-stu-id="60d9b-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="60d9b-131">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="60d9b-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="60d9b-132">В поле "Налоговая группа номенклатур" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="60d9b-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="60d9b-133">Налоговая группа номенклатур для текущей строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60d9b-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="60d9b-134">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="60d9b-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="60d9b-135">Ввод или просмотр количества единиц для строки накладной</span><span class="sxs-lookup"><span data-stu-id="60d9b-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="60d9b-136">Это число умножается на значение в поле "Цена за единицу" для определения суммы строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60d9b-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="60d9b-137">Введите или просмотрите цену за единицу для строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60d9b-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="60d9b-138">Эта сумма умножается на значение в поле "Количество" для определения суммы строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60d9b-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="60d9b-139">Просмотрите и измените распределения по бухгалтерским счетам для отдельной строки и всех дочерних строк.</span><span class="sxs-lookup"><span data-stu-id="60d9b-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="60d9b-140">Распределения по бухгалтерским счетам определяют способ учета сумм, например дохода, налога или накладных расходов в накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="60d9b-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="60d9b-141">Обновите распределения по бухгалтерским счетам для выбранной строки накладной.</span><span class="sxs-lookup"><span data-stu-id="60d9b-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="60d9b-142">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="60d9b-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="60d9b-143">Сохранение накладной с произвольным текстом в качестве шаблона.</span><span class="sxs-lookup"><span data-stu-id="60d9b-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="60d9b-144">Можно также сохранить существующую накладную с произвольным текстом в качестве шаблона.</span><span class="sxs-lookup"><span data-stu-id="60d9b-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="60d9b-145">При выборе Сохранить в шаблон на вкладке Накладная, введите имя и описание для шаблона.</span><span class="sxs-lookup"><span data-stu-id="60d9b-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="60d9b-146">Если шаблон с таким именем уже существует, появится уведомление о том, что шаблон с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="60d9b-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="60d9b-147">По-прежнему можно щелкнуть "Ok", чтобы заменить его.</span><span class="sxs-lookup"><span data-stu-id="60d9b-147">You can still click on Ok to replace it.</span></span> 
