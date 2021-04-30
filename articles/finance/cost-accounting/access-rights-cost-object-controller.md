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
ms.openlocfilehash: fa8faf0f0f45f901151b3b20a1792b3d8f264fa6
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897632"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="aee32-103">Права доступа для контроллеров объектов затрат</span><span class="sxs-lookup"><span data-stu-id="aee32-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aee32-104">Рабочая область **Управление затратами** является центральной точкой, где менеджеры могут просматривать производительность своих объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="aee32-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="aee32-105">Эта рабочая область позволяет менеджерам использовать данные учета затрат, даже если они не бухгалтеры по затратам.</span><span class="sxs-lookup"><span data-stu-id="aee32-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="aee32-106">По соображениям безопасности менеджеры должны видеть только данные учета затрат, которые относятся к конкретному объекту, за который они отвечают.</span><span class="sxs-lookup"><span data-stu-id="aee32-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="aee32-107">Существуют четыре уникальные роли в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="aee32-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="aee32-108">Имя роли</span><span class="sxs-lookup"><span data-stu-id="aee32-108">Role name</span></span>               | <span data-ttu-id="aee32-109">Лицензия</span><span class="sxs-lookup"><span data-stu-id="aee32-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="aee32-110">Диспетчер учета затрат</span><span class="sxs-lookup"><span data-stu-id="aee32-110">Cost accounting manager</span></span> | <span data-ttu-id="aee32-111">Деятельность</span><span class="sxs-lookup"><span data-stu-id="aee32-111">Activity</span></span>     |
| <span data-ttu-id="aee32-112">Бухгалтер, учитывающий затраты</span><span class="sxs-lookup"><span data-stu-id="aee32-112">Cost accountant</span></span>         | <span data-ttu-id="aee32-113">Operations</span><span class="sxs-lookup"><span data-stu-id="aee32-113">Operations</span></span>   |
| <span data-ttu-id="aee32-114">Младший бухгалтер по учету затрат</span><span class="sxs-lookup"><span data-stu-id="aee32-114">Cost accountant clerk</span></span>   | <span data-ttu-id="aee32-115">Operations</span><span class="sxs-lookup"><span data-stu-id="aee32-115">Operations</span></span>   |
| <span data-ttu-id="aee32-116">Контроллер объектов затрат</span><span class="sxs-lookup"><span data-stu-id="aee32-116">Cost object controller</span></span>  | <span data-ttu-id="aee32-117">Участники группы</span><span class="sxs-lookup"><span data-stu-id="aee32-117">Team members</span></span> |

<span data-ttu-id="aee32-118">В этом разделе объясняется, каким образом выполняется назначение роли **контроллера объекта затрат** для менеджера.</span><span class="sxs-lookup"><span data-stu-id="aee32-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="aee32-119">Когда роль **контроллера объекта затрат** назначается менеджеру, менеджер может выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="aee32-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="aee32-120">Доступ к рабочей области **Управление затратами** (в клиенте).</span><span class="sxs-lookup"><span data-stu-id="aee32-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="aee32-121">Детализация и переход к просмотр страниц, которые поддерживают опыт детализации.</span><span class="sxs-lookup"><span data-stu-id="aee32-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="aee32-122">Доступ к рабочей области **Управление затратами** (в мобильном приложении).</span><span class="sxs-lookup"><span data-stu-id="aee32-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="aee32-123">Роль **контроллера объекта затрат** не управляет, к каким объектам затрат может получить доступ и просмотр пользователь.</span><span class="sxs-lookup"><span data-stu-id="aee32-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="aee32-124">Безопасность на уровне строк предоставляется через иерархии аналитик и иерархию списков доступа.</span><span class="sxs-lookup"><span data-stu-id="aee32-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="aee32-125">Предоставление прав доступа</span><span class="sxs-lookup"><span data-stu-id="aee32-125">Grant access rights</span></span>
<span data-ttu-id="aee32-126">В следующем примере показано, как может выглядеть иерархия аналитик.</span><span class="sxs-lookup"><span data-stu-id="aee32-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="aee32-127">**Сведения об иерархии аналитик**</span><span class="sxs-lookup"><span data-stu-id="aee32-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="aee32-128">Имя иерархии аналитик</span><span class="sxs-lookup"><span data-stu-id="aee32-128">Dimension hierarchy name</span></span> | <span data-ttu-id="aee32-129">Аналитика</span><span class="sxs-lookup"><span data-stu-id="aee32-129">Dimension</span></span>    | <span data-ttu-id="aee32-130">Имя типа иерархии аналитик</span><span class="sxs-lookup"><span data-stu-id="aee32-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="aee32-131">Иерархия списков доступа</span><span class="sxs-lookup"><span data-stu-id="aee32-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="aee32-132">Cтруктурное подразделение</span><span class="sxs-lookup"><span data-stu-id="aee32-132">Organization</span></span>             | <span data-ttu-id="aee32-133">Места возникновения затрат</span><span class="sxs-lookup"><span data-stu-id="aee32-133">Cost centers</span></span> | <span data-ttu-id="aee32-134">Иерархия классификации аналитик</span><span class="sxs-lookup"><span data-stu-id="aee32-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="aee32-135">**Да**</span><span class="sxs-lookup"><span data-stu-id="aee32-135">**Yes**</span></span>               |

<span data-ttu-id="aee32-136">Можно использовать экспресс-вкладку **Пользователи** в конструкторе иерархии, чтобы вставить один или несколько кодов пользователей в каждом узле.</span><span class="sxs-lookup"><span data-stu-id="aee32-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|             <span data-ttu-id="aee32-137">Узлы</span><span class="sxs-lookup"><span data-stu-id="aee32-137">Nodes</span></span>                 | <span data-ttu-id="aee32-138">Пользователи</span><span class="sxs-lookup"><span data-stu-id="aee32-138">Users</span></span>            | <span data-ttu-id="aee32-139">Из элемента аналитики</span><span class="sxs-lookup"><span data-stu-id="aee32-139">From dimension member</span></span>     |   <span data-ttu-id="aee32-140">В элемент аналитики</span><span class="sxs-lookup"><span data-stu-id="aee32-140">To dimension member</span></span>   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="aee32-141">Cтруктурное подразделение</span><span class="sxs-lookup"><span data-stu-id="aee32-141">Organization</span></span>                      | <span data-ttu-id="aee32-142">Бенджамин, Клер</span><span class="sxs-lookup"><span data-stu-id="aee32-142">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="aee32-143">&nbsp;&nbsp;Администрирование</span><span class="sxs-lookup"><span data-stu-id="aee32-143">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="aee32-144">апреля</span><span class="sxs-lookup"><span data-stu-id="aee32-144">April</span></span>            |                           |                         |
| <span data-ttu-id="aee32-145">&nbsp;&nbsp;&nbsp;&nbsp;Финансы</span><span class="sxs-lookup"><span data-stu-id="aee32-145">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="aee32-146">Алиша</span><span class="sxs-lookup"><span data-stu-id="aee32-146">Alicia</span></span>           | <span data-ttu-id="aee32-147">CC002</span><span class="sxs-lookup"><span data-stu-id="aee32-147">CC002</span></span>                     | <span data-ttu-id="aee32-148">CC003</span><span class="sxs-lookup"><span data-stu-id="aee32-148">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="aee32-149">CC007</span><span class="sxs-lookup"><span data-stu-id="aee32-149">CC007</span></span>                     | <span data-ttu-id="aee32-150">CC007</span><span class="sxs-lookup"><span data-stu-id="aee32-150">CC007</span></span>                   |
| <span data-ttu-id="aee32-151">&nbsp;&nbsp;&nbsp;&nbsp;Отдел кадров</span><span class="sxs-lookup"><span data-stu-id="aee32-151">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="aee32-152">Арни</span><span class="sxs-lookup"><span data-stu-id="aee32-152">Arnie</span></span>            | <span data-ttu-id="aee32-153">CC001</span><span class="sxs-lookup"><span data-stu-id="aee32-153">CC001</span></span>                     | <span data-ttu-id="aee32-154">CC001</span><span class="sxs-lookup"><span data-stu-id="aee32-154">CC001</span></span>                   |
| <span data-ttu-id="aee32-155">&nbsp;&nbsp;Производство</span><span class="sxs-lookup"><span data-stu-id="aee32-155">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="aee32-156">Дэвид</span><span class="sxs-lookup"><span data-stu-id="aee32-156">David</span></span>            |                           |                         |
| <span data-ttu-id="aee32-157">&nbsp;&nbsp;&nbsp;&nbsp;Упаковка</span><span class="sxs-lookup"><span data-stu-id="aee32-157">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="aee32-158">Эллен</span><span class="sxs-lookup"><span data-stu-id="aee32-158">Ellen</span></span>            | <span data-ttu-id="aee32-159">CC005</span><span class="sxs-lookup"><span data-stu-id="aee32-159">CC005</span></span>                     | <span data-ttu-id="aee32-160">CC005</span><span class="sxs-lookup"><span data-stu-id="aee32-160">CC005</span></span>                   |
| <span data-ttu-id="aee32-161">&nbsp;&nbsp;&nbsp;&nbsp;Сборка</span><span class="sxs-lookup"><span data-stu-id="aee32-161">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="aee32-162">Крис</span><span class="sxs-lookup"><span data-stu-id="aee32-162">Chris</span></span>            | <span data-ttu-id="aee32-163">CC006</span><span class="sxs-lookup"><span data-stu-id="aee32-163">CC006</span></span>                     | <span data-ttu-id="aee32-164">CC006</span><span class="sxs-lookup"><span data-stu-id="aee32-164">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="aee32-165">Бухгалтеры затрат должны быть назначены на верхнем уровне иерархии, чтобы они моги видеть все записи в учете затрат.</span><span class="sxs-lookup"><span data-stu-id="aee32-165">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="aee32-166">Перед применением настроек иерархии списков доступа и параметров безопасности необходимо задать параметр **Включить доступ на просмотр по элементам аналитик объектов затрат** как **Да** на вкладке **Общие** на странице **Параметры учета затрат** (**Учет затрат** > **Настройка** > **Параметры**).</span><span class="sxs-lookup"><span data-stu-id="aee32-166">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="aee32-167">Настройки иерархии списков доступа используются для управления данными, которые отображаются в следующих областях:</span><span class="sxs-lookup"><span data-stu-id="aee32-167">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="aee32-168">Рабочая область **Управление затратами** (в клиенте):</span><span class="sxs-lookup"><span data-stu-id="aee32-168">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="aee32-169">Данные на страницах, которые используются для детализации</span><span class="sxs-lookup"><span data-stu-id="aee32-169">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="aee32-170">Рабочая область **Управление затратами** (в мобильном приложении):</span><span class="sxs-lookup"><span data-stu-id="aee32-170">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="aee32-171">Сальдо в карточках</span><span class="sxs-lookup"><span data-stu-id="aee32-171">Balances in cards</span></span>

- <span data-ttu-id="aee32-172">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="aee32-172">Microsoft Power BI:</span></span>

    - <span data-ttu-id="aee32-173">Данные, показанные в визуализации Power BI</span><span class="sxs-lookup"><span data-stu-id="aee32-173">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="aee32-174">Визуализация данных Power BI, которые встроены в клиент Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="aee32-174">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="aee32-175">Прежде чем иерархия списков доступа может повлиять на данные в Power BI, необходимо подсоединить иерархию списка доступа и безопасность на уровне строк в Power BI.</span><span class="sxs-lookup"><span data-stu-id="aee32-175">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="aee32-176">Дополнительные сведения см. в разделе [Настройка защиты пакета содержимого учета затрат](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="aee32-176">For more information, see [Set up security for Cost accounting content pack](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="aee32-177">В этом разделе показаны необходимые компоненты, которые должны присутствовать перед использованием рабочей области **Управление затратами**.</span><span class="sxs-lookup"><span data-stu-id="aee32-177">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="aee32-178">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="aee32-178">Additional resources</span></span>

- [<span data-ttu-id="aee32-179">Рабочая область управления затратами</span><span class="sxs-lookup"><span data-stu-id="aee32-179">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="aee32-180">Иерархия аналитик</span><span class="sxs-lookup"><span data-stu-id="aee32-180">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="aee32-181">Настройка безопасности для пакета содержимого учета затрат</span><span class="sxs-lookup"><span data-stu-id="aee32-181">Set up security for Cost accounting content pack</span></span>](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
