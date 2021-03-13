---
title: Создание бюджетов обслуживания
description: В этом разделе объясняется, как создать бюджет обслуживания в управлении активами.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 602a00060c1e56285d9954981d019bececaf90fd
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020997"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="780aa-103">Создание бюджетов обслуживания</span><span class="sxs-lookup"><span data-stu-id="780aa-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 



<span data-ttu-id="780aa-104">Бюджеты обслуживания используются для предоставления обзора ожидаемых затрат на профилактическое обслуживание.</span><span class="sxs-lookup"><span data-stu-id="780aa-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="780aa-105">Строки бюджета рассчитываются на основе строк графика обслуживания, которые имеют ожидаемую дату начала в течение бюджетного периода.</span><span class="sxs-lookup"><span data-stu-id="780aa-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="780aa-106">Бюджеты обслуживания основаны на типах затрат, используемых в управлении активами: **профилактические**, **корректирующие** и **инвестиции**.</span><span class="sxs-lookup"><span data-stu-id="780aa-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="780aa-107">Бюджетные затраты на инвестиционное обслуживание включены для активных активов, которые имеют дату замены в течение бюджетного периода и соответствующую восстановительную стоимость.</span><span class="sxs-lookup"><span data-stu-id="780aa-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="780aa-108">Бюджетные затраты на корректирующее обслуживание включаются в том случае, если в расчет бюджета включена прошлая корректирующая дата.</span><span class="sxs-lookup"><span data-stu-id="780aa-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="780aa-109">В этом случае корректирующие затраты более раннего периода рассчитываются для того же будущего периода, для которого вычисляет бюджет обслуживания.</span><span class="sxs-lookup"><span data-stu-id="780aa-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="780aa-110">Создание бюджета обслуживания</span><span class="sxs-lookup"><span data-stu-id="780aa-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="780aa-111">Выберите **Управление активами** \> **Запросы** \> **Бюджет обслуживания** \> **Бюджет**.</span><span class="sxs-lookup"><span data-stu-id="780aa-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="780aa-112">Выберите **Создать бюджет**.</span><span class="sxs-lookup"><span data-stu-id="780aa-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="780aa-113">В поле **Бюджет обслуживания** введите код бюджета.</span><span class="sxs-lookup"><span data-stu-id="780aa-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="780aa-114">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="780aa-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="780aa-115">На экспресс-вкладке **Период** в полях **Начальная дата** и **Конечная дата** введите начальную и конечную даты бюджетного периода.</span><span class="sxs-lookup"><span data-stu-id="780aa-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="780aa-116">Чтобы включить корректирующие бюджетные затраты, рассчитанные на основе фактических затрат предыдущего периода, в поле **Корректирующие с даты** введите дату начала периода, из которого должны быть включены эти затраты.</span><span class="sxs-lookup"><span data-stu-id="780aa-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="780aa-117">В зависимости от уровня детализации, необходимого в бюджете, задайте соответствующие параметры на пяти экспресс-вкладках **Группировать по**.</span><span class="sxs-lookup"><span data-stu-id="780aa-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="780aa-118">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="780aa-118">Select **OK**.</span></span>
8. <span data-ttu-id="780aa-119">Выберите **Строки бюджета**, чтобы открыть страницу **Строки бюджета обслуживания**, на которой можно просмотреть все строки бюджета, которые были созданы для данного периода.</span><span class="sxs-lookup"><span data-stu-id="780aa-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="780aa-120">Чтобы утвердить бюджет, выберите его на странице **Бюджеты обслуживания**, затем выберите **Утвердить**.</span><span class="sxs-lookup"><span data-stu-id="780aa-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="780aa-121">Затем в диалоговом окне **Утвердить бюджет** выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="780aa-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="780aa-122">Ваше имя вводится в поле **Кем утверждено** на странице **Бюджеты обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="780aa-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="780aa-123">После утверждения бюджета обслуживания невозможно пересчитать или скорректировать соответствующие строки на странице **Строки бюджета обслуживания**, если только вы не удалите утверждение.</span><span class="sxs-lookup"><span data-stu-id="780aa-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="780aa-124">Чтобы удалить утверждение бюджета обслуживания, выберите его на странице **Бюджеты обслуживания**, затем выберите **Утвердить**.</span><span class="sxs-lookup"><span data-stu-id="780aa-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="780aa-125">Затем в диалоговом окне **Утвердить бюджет** выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="780aa-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![Бюджеты обслуживания](media/01-maintenance-budgets.png)

<span data-ttu-id="780aa-127">Можно также создать новый бюджет обслуживания путем копирования существующего бюджета.</span><span class="sxs-lookup"><span data-stu-id="780aa-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="780aa-128">На странице **Бюджеты обслуживания** выберите бюджет для копирования, затем выберите **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="780aa-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="780aa-129">Этот подход полезен, если, например, вы создали бюджет на один месяц и хотите скопировать его в другие месяцы.</span><span class="sxs-lookup"><span data-stu-id="780aa-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="780aa-130">Бюджет обслуживания вычисляет только бюджетные затраты на основе строк графика обслуживания.</span><span class="sxs-lookup"><span data-stu-id="780aa-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="780aa-131">Чтобы рассчитать фактические затраты для этого же периода, этот расчет можно выполнить на странице **Управление затратами по активам**.</span><span class="sxs-lookup"><span data-stu-id="780aa-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 
