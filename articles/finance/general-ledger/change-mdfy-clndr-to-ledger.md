---
title: Изменение или переназначение календаря книги учета
description: В этом разделе описывается, как изменить календарь, назначенный книге учета в данный момент, и как назначить новый календарь книге учета.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 052b8944c0a015187d1d7c4ba3db878c52faeeea
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039958"
---
# <a name="change-or-reassign-a-ledger-calendar"></a><span data-ttu-id="d9963-103">Изменение или переназначение календаря книги учета</span><span class="sxs-lookup"><span data-stu-id="d9963-103">Change or reassign a ledger calendar</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9963-104">В этом разделе описывается, как изменить календарь, назначенный книге учета в данный момент, и как назначить новый календарь книге учета.</span><span class="sxs-lookup"><span data-stu-id="d9963-104">This topic explains how to change the calendar that is currently assigned to a ledger, and how to assign a new calendar to the ledger.</span></span>

## <a name="issue"></a><span data-ttu-id="d9963-105">Проблема</span><span class="sxs-lookup"><span data-stu-id="d9963-105">Issue</span></span>

<span data-ttu-id="d9963-106">Иногда компании должны либо изменить существующий календарь, назначенный книге учета, либо назначить новый календарь.</span><span class="sxs-lookup"><span data-stu-id="d9963-106">Sometime, companies must either change the existing calendar that is assigned to a ledger or assign a new calendar.</span></span>

## <a name="resolution"></a><span data-ttu-id="d9963-107">Решение</span><span class="sxs-lookup"><span data-stu-id="d9963-107">Resolution</span></span>

<span data-ttu-id="d9963-108">Существует два сценария изменения или переназначения календаря книги учета.</span><span class="sxs-lookup"><span data-stu-id="d9963-108">There are two scenarios for changing or reassigning a ledger calendar.</span></span> <span data-ttu-id="d9963-109">Первый сценарий предполагает изменение существующего календаря, который уже назначен книге учета.</span><span class="sxs-lookup"><span data-stu-id="d9963-109">The first scenario involves changing an existing calendar that is already assigned to the ledger.</span></span> <span data-ttu-id="d9963-110">Второй сценарий предполагает создание нового календаря и его назначение книге учета.</span><span class="sxs-lookup"><span data-stu-id="d9963-110">The second scenario involves creating a new calendar and assigning it to the ledger.</span></span> <span data-ttu-id="d9963-111">Оба изменения можно выполнить в любое время, даже после разноски проводок в книгу учета.</span><span class="sxs-lookup"><span data-stu-id="d9963-111">Both changes can be done at any time, even after transactions have been posted to the ledger.</span></span>

### <a name="change-an-existing-fiscal-calendar"></a><span data-ttu-id="d9963-112">Изменение существующего финансового календаря</span><span class="sxs-lookup"><span data-stu-id="d9963-112">Change an existing fiscal calendar</span></span>

<span data-ttu-id="d9963-113">Чтобы изменить существующий календарь, назначенный книге учета, перейдите в раздел **Главная книга \> Настройка книги учета \> Книга учета** и перейдите по ссылке на финансовый календарь, чтобы открыть страницу **Календари книги учета**.</span><span class="sxs-lookup"><span data-stu-id="d9963-113">To change an existing calendar that is assigned to your ledger, go to **General ledger \> Ledger setup \> Ledger**, and select the link for the fiscal calendar to open the **Ledger calendars** page.</span></span>

<span data-ttu-id="d9963-114">Есть ограничения на изменения, которые могут быть внесены в календарь.</span><span class="sxs-lookup"><span data-stu-id="d9963-114">There are limits to the changes that can be made to a calendar.</span></span> <span data-ttu-id="d9963-115">Например, можно изменить даты начала и окончания *периодов* в году, но невозможно изменить даты начала и окончания *года* в календаре.</span><span class="sxs-lookup"><span data-stu-id="d9963-115">For example, you can change the start and end dates of the *periods* in a year, but you can't change the start and end dates of a *year* in the calendar.</span></span>

<span data-ttu-id="d9963-116">Чтобы изменить периоды в году, выберите соответствующий календарь и год.</span><span class="sxs-lookup"><span data-stu-id="d9963-116">To change the periods in a year, select the appropriate calendar and year.</span></span> <span data-ttu-id="d9963-117">Во-первых, нажмите кнопку **Удалить период**, чтобы удалить некоторые или все существующие операционные периоды.</span><span class="sxs-lookup"><span data-stu-id="d9963-117">First, use the use the **Delete period** button to delete some or all of the existing operating periods.</span></span> <span data-ttu-id="d9963-118">Можно удалить все операционные периоды, кроме первого.</span><span class="sxs-lookup"><span data-stu-id="d9963-118">All operating periods except the first can be deleted.</span></span> <span data-ttu-id="d9963-119">Затем нажмите кнопку **Разделить период**, чтобы разделить оставшийся период или периоды на новые периоды, введя соответствующую дату начала следующего периода.</span><span class="sxs-lookup"><span data-stu-id="d9963-119">Then use the **Divide period** button to divide the remaining period or periods into new periods by entering an appropriate start date for the next period.</span></span>

<span data-ttu-id="d9963-120">После изменения периодов в календаре необходимо запустить процесс **Пересчет периодов ГК** в каждом юридическом лице (компании), которой назначен календарь.</span><span class="sxs-lookup"><span data-stu-id="d9963-120">After you change the periods in a calendar, you must run the **Recalculate ledger periods** process in every legal entity (company) that the calendar is assigned to.</span></span> <span data-ttu-id="d9963-121">Хотя вы не получаете предупреждение с напоминанием о необходимости выполнить этот шаг, процесс пересчета требуется для обновления периода, назначенного каждой разнесенной проводке в главной книге.</span><span class="sxs-lookup"><span data-stu-id="d9963-121">Although no warning message reminds you to complete this step, the recalculation process is required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="d9963-122">Для запуска процесса пересчета выберите **Пересчет периодов ГК** на странице **Настройка книги учета** в каждой компании.</span><span class="sxs-lookup"><span data-stu-id="d9963-122">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page in each company.</span></span>

<span data-ttu-id="d9963-123">Если процесс пересчета не выполнить, сальдо проводок в пробном балансе или финансовых отчетах могут быть неправильно включены в периоды.</span><span class="sxs-lookup"><span data-stu-id="d9963-123">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="d9963-124">В этом случае вы можете исправить сальдо в любое время, запустив процесс пересчета.</span><span class="sxs-lookup"><span data-stu-id="d9963-124">In this case, you can correct the balances at any time by running the recalculation process.</span></span>

### <a name="assign-a-new-fiscal-calendar"></a><span data-ttu-id="d9963-125">Назначение нового финансового календаря</span><span class="sxs-lookup"><span data-stu-id="d9963-125">Assign a new fiscal calendar</span></span>

<span data-ttu-id="d9963-126">Чтобы назначить новый финансовый календарь, перейдите в раздел **Главная книга \> Настройка книги учета \> Книга учета** и выберите **Правка**, чтобы перевести страницу **Книга учета** в режим редактирования.</span><span class="sxs-lookup"><span data-stu-id="d9963-126">To assign a new fiscal calendar, go to **General ledger \> Ledger setup \> Ledger**, and select **Edit** to put the **Ledger** page into edit mode.</span></span> <span data-ttu-id="d9963-127">Затем в поле **Финансовый календарь** выберите новый финансовый календарь.</span><span class="sxs-lookup"><span data-stu-id="d9963-127">Then, in the **Fiscal calendar** field, select a new fiscal calendar.</span></span>

<span data-ttu-id="d9963-128">После изменения финансового календаря для книги учета необходимо запустить процесс **Пересчет периодов ГК**.</span><span class="sxs-lookup"><span data-stu-id="d9963-128">After you change the fiscal calendar for a ledger, you must run the **Recalculate ledger periods**.</span></span> <span data-ttu-id="d9963-129">При назначении нового финансового календаря книге учета вы получите напоминание о необходимости выполнить этот шаг.</span><span class="sxs-lookup"><span data-stu-id="d9963-129">When you assign a new fiscal calendar to a ledger, a message reminds you to complete this step.</span></span> <span data-ttu-id="d9963-130">Хотя из сообщения вам может показаться, что процесс пересчета является необязательным, это не так.</span><span class="sxs-lookup"><span data-stu-id="d9963-130">Although the message might seem to indicate that the recalculation process is optional, it isn't.</span></span> <span data-ttu-id="d9963-131">Он необходим для обновления периода, назначенного каждой разнесенной проводке в главной книге.</span><span class="sxs-lookup"><span data-stu-id="d9963-131">It's required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="d9963-132">Для запуска процесса пересчета выберите **Пересчет периодов ГК** на странице **Настройка книги учета**.</span><span class="sxs-lookup"><span data-stu-id="d9963-132">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page.</span></span>

<span data-ttu-id="d9963-133">Если процесс пересчета не выполнить, сальдо проводок в пробном балансе или финансовых отчетах могут быть неправильно включены в периоды.</span><span class="sxs-lookup"><span data-stu-id="d9963-133">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="d9963-134">В этом случае вы можете исправить сальдо в любое время, запустив процесс пересчета.</span><span class="sxs-lookup"><span data-stu-id="d9963-134">In this case, you can correct the balances at any time by running the recalculation process.</span></span>
