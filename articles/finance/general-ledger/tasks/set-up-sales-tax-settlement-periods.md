---
title: Настройка периодов сопоставления налогов
description: В этом разделе описывается, как настроить периоды сопоставления налогов в Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5972c44261a6ebd49df0fcbcef9a8c60aaa487e2
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144728"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="56a3a-103">Настройка периодов сопоставления налогов</span><span class="sxs-lookup"><span data-stu-id="56a3a-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="56a3a-104">В этом разделе описывается, как настроить периоды сопоставления налогов.</span><span class="sxs-lookup"><span data-stu-id="56a3a-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="56a3a-105">Периоды сопоставления налога содержат сведения об интервалах периода, за которые необходимо отправить налоговые отчеты и выплатить налоги.</span><span class="sxs-lookup"><span data-stu-id="56a3a-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="56a3a-106">Процесс сопоставления можно выполнить для периода сопоставления для определенного интервала дат.</span><span class="sxs-lookup"><span data-stu-id="56a3a-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="56a3a-107">Будут сопоставлены все налоговые коды, связанные с периодом сопоставления.</span><span class="sxs-lookup"><span data-stu-id="56a3a-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="56a3a-108">В зависимости от настройки соответствующего налогового органа, налоговые обязательства разносятся на счет поставщика или счет ГК.</span><span class="sxs-lookup"><span data-stu-id="56a3a-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="56a3a-109">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="56a3a-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="56a3a-110">В области перехода выберите **Модули > Налог > Косвенные налоги > Налог > Периоды сопоставления налогов**.</span><span class="sxs-lookup"><span data-stu-id="56a3a-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="56a3a-111">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="56a3a-111">Select **New**.</span></span>
3. <span data-ttu-id="56a3a-112">В поле **Период сопоставления** введите значение.</span><span class="sxs-lookup"><span data-stu-id="56a3a-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="56a3a-113">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="56a3a-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="56a3a-114">В поле **Налоговый орган** выберите налоговый орган, который получает отчеты и платежи, созданные для периода сопоставления.</span><span class="sxs-lookup"><span data-stu-id="56a3a-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="56a3a-115">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="56a3a-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="56a3a-116">В поле **Условия оплаты** выберите требуемую запись в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="56a3a-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="56a3a-117">Соответствующий налоговый орган можно настроить в качестве поставщика, и при сопоставлении налогов будет создаваться открытая накладная поставщика.</span><span class="sxs-lookup"><span data-stu-id="56a3a-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="56a3a-118">Условия оплаты определяют срок выполнения для открытой накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="56a3a-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="56a3a-119">Выберите тип для интервалов периода сопоставления.</span><span class="sxs-lookup"><span data-stu-id="56a3a-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="56a3a-120">Введите количество единиц интервала периода на период.</span><span class="sxs-lookup"><span data-stu-id="56a3a-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="56a3a-121">Например, в квартале содержится 3 месяца.</span><span class="sxs-lookup"><span data-stu-id="56a3a-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="56a3a-122">Установите или снимите флажок **Использовать пакетную обработку для сопоставления налога**.</span><span class="sxs-lookup"><span data-stu-id="56a3a-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="56a3a-123">Процесс сопоставления за период сопоставления можно обработать как пакетное задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="56a3a-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="56a3a-124">Это рекомендуется в случае большого количества налоговых проводок в течение интервала периода.</span><span class="sxs-lookup"><span data-stu-id="56a3a-124">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="56a3a-125">В настоящее время это не поддерживается в Испании, Японии и Нидерландах.</span><span class="sxs-lookup"><span data-stu-id="56a3a-125">Currently this is not supported in Spain, Japan, and the Netherlands.</span></span>
11. <span data-ttu-id="56a3a-126">Установите или снимите флажок **Запретить создание проводок корреспонденции налогов**.</span><span class="sxs-lookup"><span data-stu-id="56a3a-126">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="56a3a-127">По умолчанию система создает проводки корреспонденции налогов в процессе сопоставления, что может вызывать проблему с производительностью, если существует большое количество налоговых проводок в течение интервала периода.</span><span class="sxs-lookup"><span data-stu-id="56a3a-127">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="56a3a-128">Установите этот флажок, чтобы запретить создание проводок корреспонденции налогов.</span><span class="sxs-lookup"><span data-stu-id="56a3a-128">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="56a3a-129">Разверните вкладку **Интервалы периода**.</span><span class="sxs-lookup"><span data-stu-id="56a3a-129">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="56a3a-130">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="56a3a-130">Select **Add**.</span></span>
14. <span data-ttu-id="56a3a-131">Введите дату в поле **Начальная дата** в новой строке.</span><span class="sxs-lookup"><span data-stu-id="56a3a-131">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="56a3a-132">В поле **Дата окончания** введите дату.</span><span class="sxs-lookup"><span data-stu-id="56a3a-132">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="56a3a-133">Выберите **Новый интервал периода**.</span><span class="sxs-lookup"><span data-stu-id="56a3a-133">Select **New period interval**.</span></span> <span data-ttu-id="56a3a-134">После ввода первого интервала периода новые периоды можно создавать автоматически.</span><span class="sxs-lookup"><span data-stu-id="56a3a-134">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="56a3a-135">Можно вернуться и добавить новые интервалы периода по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="56a3a-135">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="56a3a-136">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="56a3a-136">Close the page.</span></span>

