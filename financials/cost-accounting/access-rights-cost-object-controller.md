---
title: "Определение прав доступа для контроллеров объектов затрат"
description: "В этом разделе даны сведения о правах доступа для контроллеров объектов затрат."
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: eda924f36102550f2c543504b2bfb4acee810e9a
ms.openlocfilehash: 05d32f0cf70975700718adbabbaeb6dcefd9e882
ms.contentlocale: ru-ru
ms.lasthandoff: 09/18/2017

---

# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="3e8d4-103">Права доступа для контроллера объектов затрат</span><span class="sxs-lookup"><span data-stu-id="3e8d4-103">Access rights of a cost object controller</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3e8d4-104">Рабочая область **Управление затратами** является центральной точкой, где менеджеры могут просматривать производительность своих объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="3e8d4-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="3e8d4-105">Эта рабочая область позволяет менеджерам использовать данные учета затрат, даже если они не бухгалтеры по затратам.</span><span class="sxs-lookup"><span data-stu-id="3e8d4-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="3e8d4-106">По соображениям безопасности менеджеры должны видеть только данные учета затрат, которые относятся к конкретному объекту, за который они отвечают.</span><span class="sxs-lookup"><span data-stu-id="3e8d4-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="3e8d4-107">Существуют четыре уникальные роли в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="3e8d4-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="3e8d4-108">Имя роли</span><span class="sxs-lookup"><span data-stu-id="3e8d4-108">Role name</span></span>               | <span data-ttu-id="3e8d4-109">Лицензия</span><span class="sxs-lookup"><span data-stu-id="3e8d4-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="3e8d4-110">Диспетчер учета затрат</span><span class="sxs-lookup"><span data-stu-id="3e8d4-110">Cost accounting manager</span></span> | <span data-ttu-id="3e8d4-111">Деятельность</span><span class="sxs-lookup"><span data-stu-id="3e8d4-111">Activity</span></span>     |
| <span data-ttu-id="3e8d4-112">Бухгалтер, учитывающий затраты</span><span class="sxs-lookup"><span data-stu-id="3e8d4-112">Cost accountant</span></span>         | <span data-ttu-id="3e8d4-113">Operations</span><span class="sxs-lookup"><span data-stu-id="3e8d4-113">Operations</span></span>   |
| <span data-ttu-id="3e8d4-114">Младший бухгалтер по учету затрат</span><span class="sxs-lookup"><span data-stu-id="3e8d4-114">Cost accountant clerk</span></span>   | <span data-ttu-id="3e8d4-115">Operations</span><span class="sxs-lookup"><span data-stu-id="3e8d4-115">Operations</span></span>   |
| <span data-ttu-id="3e8d4-116">Контроллер объектов затрат</span><span class="sxs-lookup"><span data-stu-id="3e8d4-116">Cost object controller</span></span>  | <span data-ttu-id="3e8d4-117">Участники группы</span><span class="sxs-lookup"><span data-stu-id="3e8d4-117">Team members</span></span> |

<span data-ttu-id="3e8d4-118">В этом разделе объясняется, каким образом выполняется назначение роли **контроллера объекта затрат** для менеджера.</span><span class="sxs-lookup"><span data-stu-id="3e8d4-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="3e8d4-119">Когда роль **контроллера объекта затрат** назначается менеджеру, менеджер может выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="3e8d4-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="3e8d4-120">Доступ к рабочей области **Управление затратами** (в клиенте).</span><span class="sxs-lookup"><span data-stu-id="3e8d4-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="3e8d4-121">Детализация и переход к просмотр страниц, которые поддерживают опыт детализации.</span><span class="sxs-lookup"><span data-stu-id="3e8d4-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="3e8d4-122">Доступ к рабочей области **Управление затратами** (в мобильном приложении).</span><span class="sxs-lookup"><span data-stu-id="3e8d4-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="3e8d4-123">Роль **контроллера объекта затрат** не управляет, к каким объектам затрат может получить доступ и просмотр пользователь.</span><span class="sxs-lookup"><span data-stu-id="3e8d4-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="3e8d4-124">Безопасность на уровне строк предоставляется через иерархии аналитик и иерархию списков доступа.</span><span class="sxs-lookup"><span data-stu-id="3e8d4-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="3e8d4-125">Предоставление прав доступа</span><span class="sxs-lookup"><span data-stu-id="3e8d4-125">Grant access rights</span></span>
<span data-ttu-id="3e8d4-126">В следующем примере показано, как может выглядеть иерархия аналитик.</span><span class="sxs-lookup"><span data-stu-id="3e8d4-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="3e8d4-127">**Сведения об иерархии аналитик**</span><span class="sxs-lookup"><span data-stu-id="3e8d4-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="3e8d4-128">Имя иерархии аналитик</span><span class="sxs-lookup"><span data-stu-id="3e8d4-128">Dimension hierarchy name</span></span> | <span data-ttu-id="3e8d4-129">Аналитика</span><span class="sxs-lookup"><span data-stu-id="3e8d4-129">Dimension</span></span>    | <span data-ttu-id="3e8d4-130">Имя типа иерархии аналитик</span><span class="sxs-lookup"><span data-stu-id="3e8d4-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="3e8d4-131">Иерархия списков доступа</span><span class="sxs-lookup"><span data-stu-id="3e8d4-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="3e8d4-132">Cтруктурное подразделение</span><span class="sxs-lookup"><span data-stu-id="3e8d4-132">Organization</span></span>             | <span data-ttu-id="3e8d4-133">Места возникновения затрат</span><span class="sxs-lookup"><span data-stu-id="3e8d4-133">Cost centers</span></span> | <span data-ttu-id="3e8d4-134">Иерархия классификации аналитик</span><span class="sxs-lookup"><span data-stu-id="3e8d4-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="3e8d4-135">**Да**</span><span class="sxs-lookup"><span data-stu-id="3e8d4-135">**Yes**</span></span>               |

<span data-ttu-id="3e8d4-136">Можно использовать экспресс-вкладку **Пользователи** в конструкторе иерархии, чтобы вставить один или несколько кодов пользователей в каждом узле.</span><span class="sxs-lookup"><span data-stu-id="3e8d4-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="3e8d4-137">Пользователи</span><span class="sxs-lookup"><span data-stu-id="3e8d4-137">Users</span></span>            | <span data-ttu-id="3e8d4-138">Диапазоны элементов аналитики</span><span class="sxs-lookup"><span data-stu-id="3e8d4-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="3e8d4-139">**Узлы**</span><span class="sxs-lookup"><span data-stu-id="3e8d4-139">**Nodes**</span></span>                         | <span data-ttu-id="3e8d4-140">**Код пользователя**</span><span class="sxs-lookup"><span data-stu-id="3e8d4-140">**User ID**</span></span>      | <span data-ttu-id="3e8d4-141">**Из элемента аналитики**</span><span class="sxs-lookup"><span data-stu-id="3e8d4-141">**From dimension member**</span></span> | <span data-ttu-id="3e8d4-142">**В элемент аналитики**</span><span class="sxs-lookup"><span data-stu-id="3e8d4-142">**To dimension member**</span></span> |
| <span data-ttu-id="3e8d4-143">Cтруктурное подразделение</span><span class="sxs-lookup"><span data-stu-id="3e8d4-143">Organization</span></span>                      | <span data-ttu-id="3e8d4-144">Бенджамин, Клер</span><span class="sxs-lookup"><span data-stu-id="3e8d4-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="3e8d4-145">&nbsp;&nbsp;Администрирование</span><span class="sxs-lookup"><span data-stu-id="3e8d4-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="3e8d4-146">апреля</span><span class="sxs-lookup"><span data-stu-id="3e8d4-146">April</span></span>            |                           |                         |
| <span data-ttu-id="3e8d4-147">&nbsp;&nbsp;&nbsp;&nbsp;Финансы</span><span class="sxs-lookup"><span data-stu-id="3e8d4-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="3e8d4-148">Алиша</span><span class="sxs-lookup"><span data-stu-id="3e8d4-148">Alicia</span></span>           | <span data-ttu-id="3e8d4-149">CC002</span><span class="sxs-lookup"><span data-stu-id="3e8d4-149">CC002</span></span>                     | <span data-ttu-id="3e8d4-150">CC003</span><span class="sxs-lookup"><span data-stu-id="3e8d4-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="3e8d4-151">CC007</span><span class="sxs-lookup"><span data-stu-id="3e8d4-151">CC007</span></span>                     | <span data-ttu-id="3e8d4-152">CC007</span><span class="sxs-lookup"><span data-stu-id="3e8d4-152">CC007</span></span>                   |
| <span data-ttu-id="3e8d4-153">&nbsp;&nbsp;&nbsp;&nbsp;Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="3e8d4-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="3e8d4-154">Арни</span><span class="sxs-lookup"><span data-stu-id="3e8d4-154">Arnie</span></span>            | <span data-ttu-id="3e8d4-155">CC001</span><span class="sxs-lookup"><span data-stu-id="3e8d4-155">CC001</span></span>                     | <span data-ttu-id="3e8d4-156">CC001</span><span class="sxs-lookup"><span data-stu-id="3e8d4-156">CC001</span></span>                   |
| <span data-ttu-id="3e8d4-157">&nbsp;&nbsp;Производство</span><span class="sxs-lookup"><span data-stu-id="3e8d4-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="3e8d4-158">Дэвид</span><span class="sxs-lookup"><span data-stu-id="3e8d4-158">David</span></span>            |                           |                         |
| <span data-ttu-id="3e8d4-159">&nbsp;&nbsp;&nbsp;&nbsp;Упаковка</span><span class="sxs-lookup"><span data-stu-id="3e8d4-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="3e8d4-160">Эллен</span><span class="sxs-lookup"><span data-stu-id="3e8d4-160">Ellen</span></span>            | <span data-ttu-id="3e8d4-161">CC005</span><span class="sxs-lookup"><span data-stu-id="3e8d4-161">CC005</span></span>                     | <span data-ttu-id="3e8d4-162">CC005</span><span class="sxs-lookup"><span data-stu-id="3e8d4-162">CC005</span></span>                   |
| <span data-ttu-id="3e8d4-163">&nbsp;&nbsp;&nbsp;&nbsp;Сборка</span><span class="sxs-lookup"><span data-stu-id="3e8d4-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="3e8d4-164">Крис</span><span class="sxs-lookup"><span data-stu-id="3e8d4-164">Chris</span></span>            | <span data-ttu-id="3e8d4-165">CC006</span><span class="sxs-lookup"><span data-stu-id="3e8d4-165">CC006</span></span>                     | <span data-ttu-id="3e8d4-166">CC006</span><span class="sxs-lookup"><span data-stu-id="3e8d4-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="3e8d4-167">Бухгалтеры затрат должны быть назначены на верхнем уровне иерархии, чтобы они моги видеть все записи в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="3e8d4-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="3e8d4-168">Перед применением настроек иерархии списков доступа и параметров безопасности необходимо задать параметр **Включить доступ на просмотр по элементам аналитик объектов затрат** как **Да** на вкладке **Общие** на странице **Параметры учета затрат** (**Учет затрат** > **Настройка** > **Параметры**).</span><span class="sxs-lookup"><span data-stu-id="3e8d4-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="3e8d4-169">Настройки иерархии списков доступа используются для управления данными, которые отображаются в следующих областях:</span><span class="sxs-lookup"><span data-stu-id="3e8d4-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="3e8d4-170">Рабочая область **Управление затратами** (в клиенте):</span><span class="sxs-lookup"><span data-stu-id="3e8d4-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="3e8d4-171">Данные на страницах, которые используются для детализации</span><span class="sxs-lookup"><span data-stu-id="3e8d4-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="3e8d4-172">Рабочая область **Управление затратами** (в мобильном приложении):</span><span class="sxs-lookup"><span data-stu-id="3e8d4-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="3e8d4-173">Сальдо в карточках</span><span class="sxs-lookup"><span data-stu-id="3e8d4-173">Balances in cards</span></span>

- <span data-ttu-id="3e8d4-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="3e8d4-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="3e8d4-175">Данные, показанные в визуализации Power BI</span><span class="sxs-lookup"><span data-stu-id="3e8d4-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="3e8d4-176">Визуализация данных Power BI, которые встроены в Microsoft Dynamics 365 для Finance and Operations, Enterprise Edition, клиент</span><span class="sxs-lookup"><span data-stu-id="3e8d4-176">Data Power BI visualizations that are embedded in the Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="3e8d4-177">Прежде чем иерархия списков доступа может повлиять на данные в Power BI, необходимо подсоединить иерархию списка доступа и безопасность на уровне строк в Power BI.</span><span class="sxs-lookup"><span data-stu-id="3e8d4-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="3e8d4-178">Дополнительные сведения см. в разделе [Настройка защиты пакета содержимого учета затрат](/dynamics365/unified-operations/dev-itpro/analytics/setup-security-cost-accounting-content-pack).</span><span class="sxs-lookup"><span data-stu-id="3e8d4-178">For more information, see [Set up security for Cost accounting content pack](/dynamics365/unified-operations/dev-itpro/analytics/setup-security-cost-accounting-content-pack).</span></span>
> - <span data-ttu-id="3e8d4-179">В этом разделе показаны необходимые компоненты, которые должны присутствовать перед использованием рабочей области **Управление затратами**.</span><span class="sxs-lookup"><span data-stu-id="3e8d4-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="3e8d4-180">См. также</span><span class="sxs-lookup"><span data-stu-id="3e8d4-180">See also</span></span>

- [<span data-ttu-id="3e8d4-181">Рабочая область управления затратами</span><span class="sxs-lookup"><span data-stu-id="3e8d4-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="3e8d4-182">Иерархия аналитик</span><span class="sxs-lookup"><span data-stu-id="3e8d4-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="3e8d4-183">Настройка безопасности для пакета содержимого учета затрат</span><span class="sxs-lookup"><span data-stu-id="3e8d4-183">Set up security for Cost accounting content pack</span></span>](/dynamics365/unified-operations/dev-itpro/analytics/setup-security-cost-accounting-content-pack)

