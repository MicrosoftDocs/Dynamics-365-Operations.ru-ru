--- 
title: "Настройка периодов сопоставления налогов"
description: "Периоды сопоставления налога содержат сведения об интервалах периода, за которые необходимо отправить налоговые отчеты и выплатить налоги."
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: fbe31ee6a66733087677f8083c1047552d4ecffc
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="71c43-103">Настройка периодов сопоставления налогов</span><span class="sxs-lookup"><span data-stu-id="71c43-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71c43-104">Периоды сопоставления налога содержат сведения об интервалах периода, за которые необходимо отправить налоговые отчеты и выплатить налоги.</span><span class="sxs-lookup"><span data-stu-id="71c43-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="71c43-105">Процесс сопоставления можно выполнить для периода сопоставления для определенного интервала дат.</span><span class="sxs-lookup"><span data-stu-id="71c43-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="71c43-106">Будут сопоставлены все налоговые коды, связанные с периодом сопоставления.</span><span class="sxs-lookup"><span data-stu-id="71c43-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="71c43-107">В зависимости от настройки соответствующего налогового органа, налоговые обязательства разносятся на счет поставщика или счет ГК.</span><span class="sxs-lookup"><span data-stu-id="71c43-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="71c43-108">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="71c43-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="71c43-109">Перейдите в раздел "Налог" > "Косвенные налоги" > "Налог" > "Периоды сопоставления налогов".</span><span class="sxs-lookup"><span data-stu-id="71c43-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="71c43-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="71c43-110">Click New.</span></span>
3. <span data-ttu-id="71c43-111">В поле "Период сопоставления" введите значение.</span><span class="sxs-lookup"><span data-stu-id="71c43-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="71c43-112">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="71c43-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="71c43-113">В поле "Налоговый орган" выберите налоговый орган, который получает отчеты и платежи, созданные для периода сопоставления.</span><span class="sxs-lookup"><span data-stu-id="71c43-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="71c43-114">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="71c43-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="71c43-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="71c43-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="71c43-116">В поле "Условия оплаты" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="71c43-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="71c43-117">Соответствующий налоговый орган можно настроить в качестве поставщика, и при сопоставлении налогов будет создаваться открытая накладная поставщика.</span><span class="sxs-lookup"><span data-stu-id="71c43-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="71c43-118">Условия оплаты определяют срок выполнения для открытой накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="71c43-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="71c43-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="71c43-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="71c43-120">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="71c43-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="71c43-121">Выберите тип для интервалов периода сопоставления.</span><span class="sxs-lookup"><span data-stu-id="71c43-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="71c43-122">Введите количество единиц интервала периода на период.</span><span class="sxs-lookup"><span data-stu-id="71c43-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="71c43-123">Например, в квартале содержится 3 месяца.</span><span class="sxs-lookup"><span data-stu-id="71c43-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="71c43-124">Установите или снимите флажок "Использовать пакетную обработку для сопоставления налога".</span><span class="sxs-lookup"><span data-stu-id="71c43-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="71c43-125">Процесс сопоставления за период сопоставления можно обработать как пакетное задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="71c43-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="71c43-126">Это рекомендуется в случае большого количества налоговых проводок в течение интервала периода.</span><span class="sxs-lookup"><span data-stu-id="71c43-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="71c43-127">Разверните вкладку "Интервалы периода".</span><span class="sxs-lookup"><span data-stu-id="71c43-127">Expand the Period intervals tab.</span></span>
15. <span data-ttu-id="71c43-128">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="71c43-128">Click Add.</span></span>
16. <span data-ttu-id="71c43-129">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="71c43-129">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="71c43-130">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="71c43-130">In the From date field, enter a date.</span></span>
18. <span data-ttu-id="71c43-131">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="71c43-131">In the To date field, enter a date.</span></span>
19. <span data-ttu-id="71c43-132">Щелкните "Новый интервал периода".</span><span class="sxs-lookup"><span data-stu-id="71c43-132">Click New period interval.</span></span>
    * <span data-ttu-id="71c43-133">После ввода первого интервала периода новые периоды можно создавать автоматически.</span><span class="sxs-lookup"><span data-stu-id="71c43-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="71c43-134">Можно вернуться и добавить новые интервалы периода по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="71c43-134">You can come back and add new period intervals as required.</span></span>  
20. <span data-ttu-id="71c43-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="71c43-135">Close the page.</span></span>


