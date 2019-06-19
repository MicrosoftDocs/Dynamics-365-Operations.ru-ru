---
title: Авансовые отчеты с бюджетным контролем (Россия)
description: В этом разделе показано, как создать субкниги из документов-источников, таких как накладные, отборочные накладные и отгрузочные накладные для клиентов и поставщиков.
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Russia
ms.author: shylaw
ms.dyn365.ops.version: 8.0999999999999996
ms.search.validFrom: 2018-10-31
ms.openlocfilehash: 93a690db8ea1499b911a03a715fa196df99b5ca2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545425"
---
# <a name="advance-reports-with-budget-control-russia"></a><span data-ttu-id="9e85b-103">Авансовые отчеты с бюджетным контролем (Россия)</span><span class="sxs-lookup"><span data-stu-id="9e85b-103">Advance reports with budget control (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e85b-104">Авансовый отчет используется для сообщения о путевых расходах, понесенных сотрудником во время командировки.</span><span class="sxs-lookup"><span data-stu-id="9e85b-104">An advance report is used to report travel expenses that an employee incurs during a business trip.</span></span> <span data-ttu-id="9e85b-105">Можно распределить сумму расходов между аналитиками учета.</span><span class="sxs-lookup"><span data-stu-id="9e85b-105">You can distribute the expense amount across ledger dimensions.</span></span> <span data-ttu-id="9e85b-106">Можно просмотреть созданные записи ГК и проверить распределение суммы расходов.</span><span class="sxs-lookup"><span data-stu-id="9e85b-106">You can view the ledger entries and verify the distribution of the expense amount.</span></span> <span data-ttu-id="9e85b-107">Разноска авансового отчета поддерживает функции строк ГК, корректировки курса и авансовые корректировки.</span><span class="sxs-lookup"><span data-stu-id="9e85b-107">Advance report posting supports ledger line functions, exchange adjustments, and advance adjustments.</span></span> <span data-ttu-id="9e85b-108">Если проводки авансового отчета разделены по распределению, отмененный авансовый отчет поддерживает создание учетной проводки со сторно для учета распределения.</span><span class="sxs-lookup"><span data-stu-id="9e85b-108">If the advance report transactions are split by distribution, the canceled advance report supports the creation of a storno accounting transaction to account the distribution.</span></span>

<span data-ttu-id="9e85b-109">Дополнительные сведения см. в разделе [Ежедневные операции для подотчетных лиц в России](rus-advance-holders-daily-operations.md).</span><span class="sxs-lookup"><span data-stu-id="9e85b-109">For more information, see [Daily operations for advance holders in Russia](rus-advance-holders-daily-operations.md).</span></span>

## <a name="budget-control-for-advance-reports"></a><span data-ttu-id="9e85b-110">Бюджетный контроль авансовых отчетов</span><span class="sxs-lookup"><span data-stu-id="9e85b-110">Budget control for advance reports</span></span>

<span data-ttu-id="9e85b-111">Использование бюджетного контроля позволяет проверять наличие достаточных средств для запланированных или фактических покупок.</span><span class="sxs-lookup"><span data-stu-id="9e85b-111">By using budget control, you can make sure that sufficient funds are available for planned or actual purchases.</span></span> <span data-ttu-id="9e85b-112">После настройки базового бюджетирования можно настроить бюджетный контроль.</span><span class="sxs-lookup"><span data-stu-id="9e85b-112">After you set up basic budgeting, you can set up budget control.</span></span> <span data-ttu-id="9e85b-113">Бюджетный контроль можно использовать для подтверждения доступности бюджетных средств по документам-источникам, таким как заказы на покупку, отчеты по расходам, авансовые отчеты и журналы учета.</span><span class="sxs-lookup"><span data-stu-id="9e85b-113">You can use budget control to confirm whether budget funds are available on source documents, such as purchase orders, expense reports, advance reports, and accounting journals.</span></span> <span data-ttu-id="9e85b-114">Если бюджетные средства превышают установленное ограничение бюджета, можно запретить дополнительную обработку документа.</span><span class="sxs-lookup"><span data-stu-id="9e85b-114">If the budget funds exceed the budget limit that is set, additional processing of the document can be prevented.</span></span>

<span data-ttu-id="9e85b-115">Авансовый отчет в основном используется для сообщения о путевых расходах, понесенных сотрудником во время командировки.</span><span class="sxs-lookup"><span data-stu-id="9e85b-115">An advance report is primarily used to report travel expenses that an employee incurs during a business trip.</span></span> <span data-ttu-id="9e85b-116">Если понесенные по авансовому отчету расходы превышают заданный бюджет, бюджетный контроль укажет на недоступность средств.</span><span class="sxs-lookup"><span data-stu-id="9e85b-116">If the expenses that are incurred on an advance report exceed the budget that is set, budget control indicates that the funds aren't available.</span></span>

<span data-ttu-id="9e85b-117">Чтобы активировать бюджетный контроль для авансовых отчетов, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="9e85b-117">To enable budget control for advance reports, follow these steps.</span></span>

1. <span data-ttu-id="9e85b-118">На странице **Конфигурация бюджетного контроля** на вкладке **Выберите документы-источники** выберите **Авансовые отчеты** в качестве документа-источника для бюджетного контроля и активируйте проверки бюджета для строк авансового отчета.</span><span class="sxs-lookup"><span data-stu-id="9e85b-118">On the **Budget control configuration** page, on the **Select source documents** tab, select **Advance reports** as a source document for budget control, and enable budget checks for advance report lines.</span></span>
2. <span data-ttu-id="9e85b-119">На вкладке **Доступные бюджетные средства** задайте процедуру расчета для определения доступности бюджетных средств для авансовых отчетов.</span><span class="sxs-lookup"><span data-stu-id="9e85b-119">On the **Budget funds available** tab, define the calculation that determines whether budget funds for advance reports are available.</span></span>

### <a name="budget-calculation"></a><span data-ttu-id="9e85b-120">Расчет бюджета</span><span class="sxs-lookup"><span data-stu-id="9e85b-120">Budget calculation</span></span>

<span data-ttu-id="9e85b-121">При задании процедуры расчета бюджета для авансовых отчетов необходимо учитывать фактические расходы и неразнесенные фактические расходы.</span><span class="sxs-lookup"><span data-stu-id="9e85b-121">When you define the budget calculation for advance reports, you should consider actual expenditures and unposted actual expenditures.</span></span>

<span data-ttu-id="9e85b-122">**Пример**</span><span class="sxs-lookup"><span data-stu-id="9e85b-122">**Example**</span></span>

<span data-ttu-id="9e85b-123">Доступные бюджетные средства = (Исходный бюджет + Изменения бюджета + Переносы бюджета) – (Фактические расходы + Неразнесенные фактические расходы)</span><span class="sxs-lookup"><span data-stu-id="9e85b-123">Budget funds available = (Original budget + Budget revisions + Budget transfers) – (Actual expenditures + Unposted actual expenditures)</span></span>

<span data-ttu-id="9e85b-124">Фактические расходы и неразнесенные фактические расходы для каждой строки авансового отчета можно посмотреть на странице **Фактические расходы**.</span><span class="sxs-lookup"><span data-stu-id="9e85b-124">You can view the actual expenditures and unposted actual expenditures for each advance report line on the **Actual expenditures** page.</span></span>

### <a name="budget-checking"></a><span data-ttu-id="9e85b-125">Проверка бюджета</span><span class="sxs-lookup"><span data-stu-id="9e85b-125">Budget checking</span></span>

<span data-ttu-id="9e85b-126">Проверка бюджета для авансовых отчетов позволяет проверять наличие бюджетных средств для запланированных или будущих расходов.</span><span class="sxs-lookup"><span data-stu-id="9e85b-126">Budget checking for advance reports makes sure that budget funds are available for planned or future expenditures.</span></span> <span data-ttu-id="9e85b-127">Процесс проверки бюджета запускается автоматически при сохранении или разноске авансового отчета.</span><span class="sxs-lookup"><span data-stu-id="9e85b-127">The budget checking process runs automatically when an advance report line is saved, or when the report is posted.</span></span>

## <a name="accounting-distributions-and-subledger-journals"></a><span data-ttu-id="9e85b-128">Распределения по бухгалтерским счетам и журналам субкниги</span><span class="sxs-lookup"><span data-stu-id="9e85b-128">Accounting distributions and subledger journals</span></span>

<span data-ttu-id="9e85b-129">Строки журнала субкниги — это записи ГК, разнесенные в главную книгу с помощью общего журнала.</span><span class="sxs-lookup"><span data-stu-id="9e85b-129">Subledger journal lines are accounting entries that are posted to the general ledger by using the general journal.</span></span> <span data-ttu-id="9e85b-130">Можно создать субкниги из документов-источников, таких как накладные, отборочные накладные и отгрузочные накладные для клиентов и поставщиков.</span><span class="sxs-lookup"><span data-stu-id="9e85b-130">You can generate subledgers from source documents such as invoices, packing slips, and picking lists for customers and vendors.</span></span> <span data-ttu-id="9e85b-131">Перед разноской сведения о поставщике в главной книге можно просмотреть или изменить журналы субкниги с помощью метода распределения.</span><span class="sxs-lookup"><span data-stu-id="9e85b-131">Before you post the voucher information to the general ledger, you can view or modify subledger journals by using the distribution method.</span></span> <span data-ttu-id="9e85b-132">Этот метод позволяет распределить суммы разноски между несколькими финансовыми аналитиками.</span><span class="sxs-lookup"><span data-stu-id="9e85b-132">This method lets you allocate posting amounts among multiple financial dimensions.</span></span> <span data-ttu-id="9e85b-133">В зависимости от разрешений пользователя можно также изменить номер счета ГК или значения финансовых аналитик по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9e85b-133">Depending on your user permissions, you can also change the default ledger account number or financial dimension values.</span></span> <span data-ttu-id="9e85b-134">Распределения служат в качестве интерфейса в журналы субкниги и содержат только одну сторону учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9e85b-134">Distributions serve as an interface to the subledger journals and contain only one side of the accounting entry.</span></span>
