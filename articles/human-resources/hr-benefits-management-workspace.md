---
title: Рабочая область управления льготами
description: В этой теме описывается рабочее пространство "Управление льготами" в Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9b8dcad04e85a4beb2fe68e9d6fad4ec794e3ade
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805834"
---
# <a name="benefits-management-workspace"></a><span data-ttu-id="62856-103">Рабочая область управления льготами</span><span class="sxs-lookup"><span data-stu-id="62856-103">Benefits management workspace</span></span>

[!include [applies to](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="62856-104">В этой теме описывается рабочее пространство **Управление льготами** в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="62856-104">This topic describes the **Benefits management** workspace in Dynamics 365 Human Resources.</span></span>

> [!NOTE]
> <span data-ttu-id="62856-105">Для просмотра рабочей области **Управление льготами** необходимо сначала включить **(Предварительная версия) Рабочая область управления льготами** в управлении функциями.</span><span class="sxs-lookup"><span data-stu-id="62856-105">To view the **Benefits management** workspace, you must first enable the **(Preview) Benefits management workspace** feature in Feature management.</span></span> <span data-ttu-id="62856-106">Дополнительные сведения о включении предварительных версий функций см. в разделе [Управление функциями](../hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="62856-106">For more information about enabling preview features, see [Manage features](../hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="62856-107">![Включение рабочей области управления льготами](./media/hr-benefits-management-workspace-enable.png)</span><span class="sxs-lookup"><span data-stu-id="62856-107">![Enable Benefits management workspace](./media/hr-benefits-management-workspace-enable.png)</span></span>

<span data-ttu-id="62856-108">Рабочая область **Управление льготами** позволяет быстро просматривать льготы, требующие вашего внимания.</span><span class="sxs-lookup"><span data-stu-id="62856-108">The **Benefits management** workspace gives you a quick view of benefits items that require your attention.</span></span> <span data-ttu-id="62856-109">На этой странице показано:</span><span class="sxs-lookup"><span data-stu-id="62856-109">On this page, you can see:</span></span>

- <span data-ttu-id="62856-110">Итоги для номенклатур, ожидающих действия</span><span class="sxs-lookup"><span data-stu-id="62856-110">Totals for items awaiting action</span></span>
- <span data-ttu-id="62856-111">Работники с неподтвержденным выбором</span><span class="sxs-lookup"><span data-stu-id="62856-111">Workers with unconfirmed selections</span></span>
- <span data-ttu-id="62856-112">Работники, недавно зарегистрированные в льготах</span><span class="sxs-lookup"><span data-stu-id="62856-112">Workers who recently enrolled in benefits</span></span>
- <span data-ttu-id="62856-113">Работники с будущими жизненными событиями</span><span class="sxs-lookup"><span data-stu-id="62856-113">Workers with future life events</span></span>
- <span data-ttu-id="62856-114">Новые сотрудники, которые не были зарегистрированы</span><span class="sxs-lookup"><span data-stu-id="62856-114">New hires who aren't enrolled</span></span>
- <span data-ttu-id="62856-115">Работники с активными жизненными событиями</span><span class="sxs-lookup"><span data-stu-id="62856-115">Workers with active life events</span></span>
- <span data-ttu-id="62856-116">Работники с открытыми регистрациями, которые не выбрали планы</span><span class="sxs-lookup"><span data-stu-id="62856-116">Workers with open enrollments who haven't opted for any plans</span></span>

![Рабочая область управления льготами](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a><span data-ttu-id="62856-118">Просмотр элементов действия</span><span class="sxs-lookup"><span data-stu-id="62856-118">View action items</span></span>

<span data-ttu-id="62856-119">Можно просмотреть элементы действий, выбирая плитку или вкладку. При выборе вкладки можно просматривать и выбирать сотрудников прямо на странице рабочей области.</span><span class="sxs-lookup"><span data-stu-id="62856-119">You can view your action items by either selecting a tile or a tab. If you select a tab, you can view and select workers right on the workspace page.</span></span>

![Элементы действия](./media/hr-benefits-management-workspace-action-items.png)

<span data-ttu-id="62856-121">Если выбрать плитку, вы перейдете на страницу этой области.</span><span class="sxs-lookup"><span data-stu-id="62856-121">If you select a tile, you go to the page for that area.</span></span> <span data-ttu-id="62856-122">Например, при выборе любой из этих плиток отображается страница **Планы льгот работника**, отфильтрованная для сотрудников, по которым необходимо предпринять действие:</span><span class="sxs-lookup"><span data-stu-id="62856-122">For example, selecting any of these tiles displays the **Worker benefits plans** page, filtered for employees you need to take action on:</span></span>

- <span data-ttu-id="62856-123">**Неподтвержденные выбранные параметры**</span><span class="sxs-lookup"><span data-stu-id="62856-123">**Unconfirmed selections**</span></span>
- <span data-ttu-id="62856-124">**Открытые регистрации без извлеченных планов**</span><span class="sxs-lookup"><span data-stu-id="62856-124">**Open enrollments with no checked out plans**</span></span>
- <span data-ttu-id="62856-125">**Зарегистрированные для льгот**</span><span class="sxs-lookup"><span data-stu-id="62856-125">**Enrolled in benefits**</span></span>
- <span data-ttu-id="62856-126">**Новый сотрудник не зарегистрирован**</span><span class="sxs-lookup"><span data-stu-id="62856-126">**New hire not enrolled**</span></span>

![Планы льгот работника](./media/hr-benefits-management-workspace-plans.png)

<span data-ttu-id="62856-128">При выборе плиток **Активных жизненные события** или **Будущие жизненные события** открывается список активных или будущих жизненных событий.</span><span class="sxs-lookup"><span data-stu-id="62856-128">Selecting the **Active life events** or **Future life events** tiles takes you to a list of active or future life events.</span></span>

![Жизненные события](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a><span data-ttu-id="62856-130">Обрабатывается</span><span class="sxs-lookup"><span data-stu-id="62856-130">Processing</span></span>

<span data-ttu-id="62856-131">Для обработки допустимости регистрации, жизненных событий или обновления изменения ставки выберите соответствующий элемент на панели навигации.</span><span class="sxs-lookup"><span data-stu-id="62856-131">To process enrollment eligibility, life events, or rate change updates, select the appropriate item on the navigation bar.</span></span>

![Обрабатывается](./media/hr-benefits-management-workspace-processing.png)

<span data-ttu-id="62856-133">Чтобы просмотреть результаты процесса, выберите **Результаты обработки** на странице.</span><span class="sxs-lookup"><span data-stu-id="62856-133">To view process results, select **Process results** on the page.</span></span>

![Результаты обработки](./media/hr-benefits-management-workspace-process-results.png)

<span data-ttu-id="62856-135">Дополнительные сведения об обработке льгот см. в:</span><span class="sxs-lookup"><span data-stu-id="62856-135">For more information about benefits processing, see:</span></span>

- [<span data-ttu-id="62856-136">Обработка приемлемости регистрации</span><span class="sxs-lookup"><span data-stu-id="62856-136">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="62856-137">Обработка изменений событий в жизни</span><span class="sxs-lookup"><span data-stu-id="62856-137">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="62856-138">Обработка допустимости событий в жизни</span><span class="sxs-lookup"><span data-stu-id="62856-138">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="62856-139">Обработка событий в жизни</span><span class="sxs-lookup"><span data-stu-id="62856-139">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="62856-140">Обработка изменений рейтинга</span><span class="sxs-lookup"><span data-stu-id="62856-140">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a><span data-ttu-id="62856-141">Изменить период</span><span class="sxs-lookup"><span data-stu-id="62856-141">Change period</span></span>

<span data-ttu-id="62856-142">Для просмотра других льготных периодов выберите его из раскрывающегося списка **Период**.</span><span class="sxs-lookup"><span data-stu-id="62856-142">To view a different benefits period, select it from the **Period** dropdown.</span></span>

![Изменить период](./media/hr-benefits-management-workspace-period.png)

## <a name="view-more-options"></a><span data-ttu-id="62856-144">Просмотр дополнительных параметров</span><span class="sxs-lookup"><span data-stu-id="62856-144">View more options</span></span>

<span data-ttu-id="62856-145">Чтобы просмотреть дополнительные сведения и действия, которые можно выполнить, выберите **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="62856-145">To view more information and actions you can take, select **Links**.</span></span>

![Ссылки](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a><span data-ttu-id="62856-147">См. также</span><span class="sxs-lookup"><span data-stu-id="62856-147">See also</span></span>

[<span data-ttu-id="62856-148">Обзор управления льготами</span><span class="sxs-lookup"><span data-stu-id="62856-148">Benefits management overview</span></span>](hr-benefits-management-overview.md)