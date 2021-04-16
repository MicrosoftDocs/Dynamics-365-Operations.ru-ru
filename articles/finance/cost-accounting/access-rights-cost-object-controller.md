---
title: Права доступа для контроллеров объектов затрат
description: В этом разделе даны сведения о правах доступа для контроллеров объектов затрат.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a3639c05b24de31cfa09d2d9d0cf427122f51eae
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810206"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="4e2ac-103">Права доступа для контроллеров объектов затрат</span><span class="sxs-lookup"><span data-stu-id="4e2ac-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e2ac-104">Рабочая область **Управление затратами** является центральной точкой, где менеджеры могут просматривать производительность своих объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="4e2ac-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="4e2ac-105">Эта рабочая область позволяет менеджерам использовать данные учета затрат, даже если они не бухгалтеры по затратам.</span><span class="sxs-lookup"><span data-stu-id="4e2ac-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="4e2ac-106">По соображениям безопасности менеджеры должны видеть только данные учета затрат, которые относятся к конкретному объекту, за который они отвечают.</span><span class="sxs-lookup"><span data-stu-id="4e2ac-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="4e2ac-107">Существуют четыре уникальные роли в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="4e2ac-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="4e2ac-108">Имя роли</span><span class="sxs-lookup"><span data-stu-id="4e2ac-108">Role name</span></span>               | <span data-ttu-id="4e2ac-109">Лицензия</span><span class="sxs-lookup"><span data-stu-id="4e2ac-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="4e2ac-110">Диспетчер учета затрат</span><span class="sxs-lookup"><span data-stu-id="4e2ac-110">Cost accounting manager</span></span> | <span data-ttu-id="4e2ac-111">Деятельность</span><span class="sxs-lookup"><span data-stu-id="4e2ac-111">Activity</span></span>     |
| <span data-ttu-id="4e2ac-112">Бухгалтер, учитывающий затраты</span><span class="sxs-lookup"><span data-stu-id="4e2ac-112">Cost accountant</span></span>         | <span data-ttu-id="4e2ac-113">Operations</span><span class="sxs-lookup"><span data-stu-id="4e2ac-113">Operations</span></span>   |
| <span data-ttu-id="4e2ac-114">Младший бухгалтер по учету затрат</span><span class="sxs-lookup"><span data-stu-id="4e2ac-114">Cost accountant clerk</span></span>   | <span data-ttu-id="4e2ac-115">Operations</span><span class="sxs-lookup"><span data-stu-id="4e2ac-115">Operations</span></span>   |
| <span data-ttu-id="4e2ac-116">Контроллер объектов затрат</span><span class="sxs-lookup"><span data-stu-id="4e2ac-116">Cost object controller</span></span>  | <span data-ttu-id="4e2ac-117">Участники группы</span><span class="sxs-lookup"><span data-stu-id="4e2ac-117">Team members</span></span> |

<span data-ttu-id="4e2ac-118">В этом разделе объясняется, каким образом выполняется назначение роли **контроллера объекта затрат** для менеджера.</span><span class="sxs-lookup"><span data-stu-id="4e2ac-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="4e2ac-119">Когда роль **контроллера объекта затрат** назначается менеджеру, менеджер может выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="4e2ac-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="4e2ac-120">Доступ к рабочей области **Управление затратами** (в клиенте).</span><span class="sxs-lookup"><span data-stu-id="4e2ac-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="4e2ac-121">Детализация и переход к просмотр страниц, которые поддерживают опыт детализации.</span><span class="sxs-lookup"><span data-stu-id="4e2ac-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="4e2ac-122">Доступ к рабочей области **Управление затратами** (в мобильном приложении).</span><span class="sxs-lookup"><span data-stu-id="4e2ac-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="4e2ac-123">Роль **контроллера объекта затрат** не управляет, к каким объектам затрат может получить доступ и просмотр пользователь.</span><span class="sxs-lookup"><span data-stu-id="4e2ac-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="4e2ac-124">Безопасность на уровне строк предоставляется через иерархии аналитик и иерархию списков доступа.</span><span class="sxs-lookup"><span data-stu-id="4e2ac-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="4e2ac-125">Предоставление прав доступа</span><span class="sxs-lookup"><span data-stu-id="4e2ac-125">Grant access rights</span></span>
<span data-ttu-id="4e2ac-126">В следующем примере показано, как может выглядеть иерархия аналитик.</span><span class="sxs-lookup"><span data-stu-id="4e2ac-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="4e2ac-127">**Сведения об иерархии аналитик**</span><span class="sxs-lookup"><span data-stu-id="4e2ac-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="4e2ac-128">Имя иерархии аналитик</span><span class="sxs-lookup"><span data-stu-id="4e2ac-128">Dimension hierarchy name</span></span> | <span data-ttu-id="4e2ac-129">Аналитика</span><span class="sxs-lookup"><span data-stu-id="4e2ac-129">Dimension</span></span>    | <span data-ttu-id="4e2ac-130">Имя типа иерархии аналитик</span><span class="sxs-lookup"><span data-stu-id="4e2ac-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="4e2ac-131">Иерархия списков доступа</span><span class="sxs-lookup"><span data-stu-id="4e2ac-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="4e2ac-132">Cтруктурное подразделение</span><span class="sxs-lookup"><span data-stu-id="4e2ac-132">Organization</span></span>             | <span data-ttu-id="4e2ac-133">Места возникновения затрат</span><span class="sxs-lookup"><span data-stu-id="4e2ac-133">Cost centers</span></span> | <span data-ttu-id="4e2ac-134">Иерархия классификации аналитик</span><span class="sxs-lookup"><span data-stu-id="4e2ac-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="4e2ac-135">**Да**</span><span class="sxs-lookup"><span data-stu-id="4e2ac-135">**Yes**</span></span>               |

<span data-ttu-id="4e2ac-136">Можно использовать экспресс-вкладку **Пользователи** в конструкторе иерархии, чтобы вставить один или несколько кодов пользователей в каждом узле.</span><span class="sxs-lookup"><span data-stu-id="4e2ac-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="4e2ac-137">Пользователи</span><span class="sxs-lookup"><span data-stu-id="4e2ac-137">Users</span></span>            | <span data-ttu-id="4e2ac-138">Диапазоны элементов аналитики</span><span class="sxs-lookup"><span data-stu-id="4e2ac-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="4e2ac-139">**Узлы**</span><span class="sxs-lookup"><span data-stu-id="4e2ac-139">**Nodes**</span></span>                         | <span data-ttu-id="4e2ac-140">**Код пользователя**</span><span class="sxs-lookup"><span data-stu-id="4e2ac-140">**User ID**</span></span>      | <span data-ttu-id="4e2ac-141">**Из элемента аналитики**</span><span class="sxs-lookup"><span data-stu-id="4e2ac-141">**From dimension member**</span></span> | <span data-ttu-id="4e2ac-142">**В элемент аналитики**</span><span class="sxs-lookup"><span data-stu-id="4e2ac-142">**To dimension member**</span></span> |
| <span data-ttu-id="4e2ac-143">Cтруктурное подразделение</span><span class="sxs-lookup"><span data-stu-id="4e2ac-143">Organization</span></span>                      | <span data-ttu-id="4e2ac-144">Бенджамин, Клер</span><span class="sxs-lookup"><span data-stu-id="4e2ac-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="4e2ac-145">&nbsp;&nbsp;Администрирование</span><span class="sxs-lookup"><span data-stu-id="4e2ac-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="4e2ac-146">апреля</span><span class="sxs-lookup"><span data-stu-id="4e2ac-146">April</span></span>            |                           |                         |
| <span data-ttu-id="4e2ac-147">&nbsp;&nbsp;&nbsp;&nbsp;Финансы</span><span class="sxs-lookup"><span data-stu-id="4e2ac-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="4e2ac-148">Алиша</span><span class="sxs-lookup"><span data-stu-id="4e2ac-148">Alicia</span></span>           | <span data-ttu-id="4e2ac-149">CC002</span><span class="sxs-lookup"><span data-stu-id="4e2ac-149">CC002</span></span>                     | <span data-ttu-id="4e2ac-150">CC003</span><span class="sxs-lookup"><span data-stu-id="4e2ac-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="4e2ac-151">CC007</span><span class="sxs-lookup"><span data-stu-id="4e2ac-151">CC007</span></span>                     | <span data-ttu-id="4e2ac-152">CC007</span><span class="sxs-lookup"><span data-stu-id="4e2ac-152">CC007</span></span>                   |
| <span data-ttu-id="4e2ac-153">&nbsp;&nbsp;&nbsp;&nbsp;Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="4e2ac-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="4e2ac-154">Арни</span><span class="sxs-lookup"><span data-stu-id="4e2ac-154">Arnie</span></span>            | <span data-ttu-id="4e2ac-155">CC001</span><span class="sxs-lookup"><span data-stu-id="4e2ac-155">CC001</span></span>                     | <span data-ttu-id="4e2ac-156">CC001</span><span class="sxs-lookup"><span data-stu-id="4e2ac-156">CC001</span></span>                   |
| <span data-ttu-id="4e2ac-157">&nbsp;&nbsp;Производство</span><span class="sxs-lookup"><span data-stu-id="4e2ac-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="4e2ac-158">Дэвид</span><span class="sxs-lookup"><span data-stu-id="4e2ac-158">David</span></span>            |                           |                         |
| <span data-ttu-id="4e2ac-159">&nbsp;&nbsp;&nbsp;&nbsp;Упаковка</span><span class="sxs-lookup"><span data-stu-id="4e2ac-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="4e2ac-160">Эллен</span><span class="sxs-lookup"><span data-stu-id="4e2ac-160">Ellen</span></span>            | <span data-ttu-id="4e2ac-161">CC005</span><span class="sxs-lookup"><span data-stu-id="4e2ac-161">CC005</span></span>                     | <span data-ttu-id="4e2ac-162">CC005</span><span class="sxs-lookup"><span data-stu-id="4e2ac-162">CC005</span></span>                   |
| <span data-ttu-id="4e2ac-163">&nbsp;&nbsp;&nbsp;&nbsp;Сборка</span><span class="sxs-lookup"><span data-stu-id="4e2ac-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="4e2ac-164">Крис</span><span class="sxs-lookup"><span data-stu-id="4e2ac-164">Chris</span></span>            | <span data-ttu-id="4e2ac-165">CC006</span><span class="sxs-lookup"><span data-stu-id="4e2ac-165">CC006</span></span>                     | <span data-ttu-id="4e2ac-166">CC006</span><span class="sxs-lookup"><span data-stu-id="4e2ac-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="4e2ac-167">Бухгалтеры затрат должны быть назначены на верхнем уровне иерархии, чтобы они моги видеть все записи в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="4e2ac-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="4e2ac-168">Перед применением настроек иерархии списков доступа и параметров безопасности необходимо задать параметр **Включить доступ на просмотр по элементам аналитик объектов затрат** как **Да** на вкладке **Общие** на странице **Параметры учета затрат** (**Учет затрат** > **Настройка** > **Параметры**).</span><span class="sxs-lookup"><span data-stu-id="4e2ac-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="4e2ac-169">Настройки иерархии списков доступа используются для управления данными, которые отображаются в следующих областях:</span><span class="sxs-lookup"><span data-stu-id="4e2ac-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="4e2ac-170">Рабочая область **Управление затратами** (в клиенте):</span><span class="sxs-lookup"><span data-stu-id="4e2ac-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="4e2ac-171">Данные на страницах, которые используются для детализации</span><span class="sxs-lookup"><span data-stu-id="4e2ac-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="4e2ac-172">Рабочая область **Управление затратами** (в мобильном приложении):</span><span class="sxs-lookup"><span data-stu-id="4e2ac-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="4e2ac-173">Сальдо в карточках</span><span class="sxs-lookup"><span data-stu-id="4e2ac-173">Balances in cards</span></span>

- <span data-ttu-id="4e2ac-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="4e2ac-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="4e2ac-175">Данные, показанные в визуализации Power BI</span><span class="sxs-lookup"><span data-stu-id="4e2ac-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="4e2ac-176">Визуализация данных Power BI, которые встроены в клиент Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="4e2ac-176">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="4e2ac-177">Прежде чем иерархия списков доступа может повлиять на данные в Power BI, необходимо подсоединить иерархию списка доступа и безопасность на уровне строк в Power BI.</span><span class="sxs-lookup"><span data-stu-id="4e2ac-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="4e2ac-178">Дополнительные сведения см. в разделе [Настройка защиты пакета содержимого учета затрат](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="4e2ac-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="4e2ac-179">В этом разделе показаны необходимые компоненты, которые должны присутствовать перед использованием рабочей области **Управление затратами**.</span><span class="sxs-lookup"><span data-stu-id="4e2ac-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="4e2ac-180">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4e2ac-180">Additional resources</span></span>

- [<span data-ttu-id="4e2ac-181">Рабочая область управления затратами</span><span class="sxs-lookup"><span data-stu-id="4e2ac-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="4e2ac-182">Иерархия аналитик</span><span class="sxs-lookup"><span data-stu-id="4e2ac-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="4e2ac-183">Настройка безопасности для пакета содержимого учета затрат</span><span class="sxs-lookup"><span data-stu-id="4e2ac-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]