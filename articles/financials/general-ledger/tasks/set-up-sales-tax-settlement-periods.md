---
title: Настройка периодов сопоставления налогов
description: Периоды сопоставления налога содержат сведения об интервалах периода, за которые необходимо отправить налоговые отчеты и выплатить налоги.
author: twheeloc
manager: AnnBe
ms.date: 10/15/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1087ed78e91b487ca7157bfdac1d72ae3f477875
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "326201"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="cc4e8-103">Настройка периодов сопоставления налогов</span><span class="sxs-lookup"><span data-stu-id="cc4e8-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc4e8-104">Периоды сопоставления налога содержат сведения об интервалах периода, за которые необходимо отправить налоговые отчеты и выплатить налоги.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="cc4e8-105">Процесс сопоставления можно выполнить для периода сопоставления для определенного интервала дат.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="cc4e8-106">Будут сопоставлены все налоговые коды, связанные с периодом сопоставления.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="cc4e8-107">В зависимости от настройки соответствующего налогового органа, налоговые обязательства разносятся на счет поставщика или счет ГК.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="cc4e8-108">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="cc4e8-109">Перейдите в раздел "Налог" > "Косвенные налоги" > "Налог" > "Периоды сопоставления налогов".</span><span class="sxs-lookup"><span data-stu-id="cc4e8-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="cc4e8-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="cc4e8-110">Click New.</span></span>
3. <span data-ttu-id="cc4e8-111">В поле "Период сопоставления" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="cc4e8-112">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cc4e8-113">В поле "Налоговый орган" выберите налоговый орган, который получает отчеты и платежи, созданные для периода сопоставления.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="cc4e8-114">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="cc4e8-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="cc4e8-116">В поле "Условия оплаты" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cc4e8-117">Соответствующий налоговый орган можно настроить в качестве поставщика, и при сопоставлении налогов будет создаваться открытая накладная поставщика.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="cc4e8-118">Условия оплаты определяют срок выполнения для открытой накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="cc4e8-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="cc4e8-120">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="cc4e8-121">Выберите тип для интервалов периода сопоставления.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="cc4e8-122">Введите количество единиц интервала периода на период.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="cc4e8-123">Например, в квартале содержится 3 месяца.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="cc4e8-124">Установите или снимите флажок "Использовать пакетную обработку для сопоставления налога".</span><span class="sxs-lookup"><span data-stu-id="cc4e8-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="cc4e8-125">Процесс сопоставления за период сопоставления можно обработать как пакетное задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="cc4e8-126">Это рекомендуется в случае большого количества налоговых проводок в течение интервала периода.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="cc4e8-127">Установите или снимите флажок "Запретить создание проводок корреспонденции налогов".</span><span class="sxs-lookup"><span data-stu-id="cc4e8-127">Select or clear the Prevent generating offset tax transactions check box.</span></span>
    * <span data-ttu-id="cc4e8-128">По умолчанию система создает проводки корреспонденции налогов в процессе сопоставления, что может вызывать проблему с производительностью, если существует большое количество налоговых проводок в течение интервала периода.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-128">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="cc4e8-129">Установите этот флажок, чтобы запретить создание проводок корреспонденции налогов.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-129">Select this check box to prevent generating offset tax transactions.</span></span>
15. <span data-ttu-id="cc4e8-130">Разверните вкладку "Интервалы периода".</span><span class="sxs-lookup"><span data-stu-id="cc4e8-130">Expand the Period intervals tab.</span></span>
16. <span data-ttu-id="cc4e8-131">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-131">Click Add.</span></span>
17. <span data-ttu-id="cc4e8-132">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-132">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="cc4e8-133">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-133">In the From date field, enter a date.</span></span>
19. <span data-ttu-id="cc4e8-134">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-134">In the To date field, enter a date.</span></span>
20. <span data-ttu-id="cc4e8-135">Щелкните "Новый интервал периода".</span><span class="sxs-lookup"><span data-stu-id="cc4e8-135">Click New period interval.</span></span>
    * <span data-ttu-id="cc4e8-136">После ввода первого интервала периода новые периоды можно создавать автоматически.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-136">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="cc4e8-137">Можно вернуться и добавить новые интервалы периода по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-137">You can come back and add new period intervals as required.</span></span>  
21. <span data-ttu-id="cc4e8-138">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="cc4e8-138">Close the page.</span></span>

