---
title: Настройка организационных иерархий
description: В этом разделе описывается, как настроить организационные иерархии в Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4238d1aa277bf2f1df30825ef20dbf3095d13ebc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800575"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="b30b6-103">Настройка организационных иерархий</span><span class="sxs-lookup"><span data-stu-id="b30b6-103">Set up organization hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b30b6-104">В этом разделе описывается, как настроить организационные иерархии в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b30b6-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b30b6-105">Перед созданием каналов необходимо подтвердить настройку организационных иерархий.</span><span class="sxs-lookup"><span data-stu-id="b30b6-105">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="b30b6-106">Организационные иерархии служат для просмотра сведений и составления отчетов о бизнесе с разных точек зрения.</span><span class="sxs-lookup"><span data-stu-id="b30b6-106">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="b30b6-107">Например, можно настроить одну иерархию для налоговой, юридической или правовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="b30b6-107">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="b30b6-108">И можно настроить другую иерархию, чтобы составлять отчеты с использованием финансовой информации, которая не является юридически обязательной, но используется для целей внутренней отчетности.</span><span class="sxs-lookup"><span data-stu-id="b30b6-108">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="b30b6-109">Перед созданием организационной иерархии необходимо создать организации.</span><span class="sxs-lookup"><span data-stu-id="b30b6-109">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="b30b6-110">Дополнительные сведения см. в задачах [Создание юридических лиц](channels-legal-entities.md) или [Создание операционных единиц](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="b30b6-110">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="b30b6-111">Дополнительные сведения см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="b30b6-111">For more information, see the following topics.</span></span>
- [<span data-ttu-id="b30b6-112">Обзор организаций и организационных иерархий</span><span class="sxs-lookup"><span data-stu-id="b30b6-112">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="b30b6-113">Планирование организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="b30b6-113">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="b30b6-114">Создание организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="b30b6-114">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="b30b6-115">Создание организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="b30b6-115">Create an organizational hierarchy</span></span>

<span data-ttu-id="b30b6-116">Для создания организационной иерархии выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b30b6-116">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="b30b6-117">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Организационные иерархии**.</span><span class="sxs-lookup"><span data-stu-id="b30b6-117">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="b30b6-118">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b30b6-118">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="b30b6-119">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="b30b6-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="b30b6-120">В разделе **Назначение** выберите **Назначение цели**.</span><span class="sxs-lookup"><span data-stu-id="b30b6-120">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="b30b6-121">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b30b6-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="b30b6-122">Выберите цель для назначения организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="b30b6-122">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="b30b6-123">В разделе **Назначенные иерархии** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="b30b6-123">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="b30b6-124">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b30b6-124">In the list, mark the selected row.</span></span> <span data-ttu-id="b30b6-125">Найдите только что созданную иерархию.</span><span class="sxs-lookup"><span data-stu-id="b30b6-125">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="b30b6-126">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b30b6-126">Select **OK**.</span></span>

<span data-ttu-id="b30b6-127">На следующем рисунке показан пример организационной иерархии, созданной для вымышленного набора магазинов "Adventure Works".</span><span class="sxs-lookup"><span data-stu-id="b30b6-127">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Пример организационное иерархии](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="b30b6-129">Добавление организаций в иерархию</span><span class="sxs-lookup"><span data-stu-id="b30b6-129">Add organizations to a hierarchy</span></span>

<span data-ttu-id="b30b6-130">Чтобы добавить организации в иерархию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b30b6-130">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="b30b6-131">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b30b6-131">In the list, find and select the desired record.</span></span> <span data-ttu-id="b30b6-132">Выберите иерархию.</span><span class="sxs-lookup"><span data-stu-id="b30b6-132">Select your hierarchy.</span></span>
1. <span data-ttu-id="b30b6-133">На панели операций выберите **Вид**.</span><span class="sxs-lookup"><span data-stu-id="b30b6-133">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="b30b6-134">Добавьте организации при необходимости.</span><span class="sxs-lookup"><span data-stu-id="b30b6-134">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="b30b6-135">Чтобы добавить организацию, выберите **Правка**, затем выберите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="b30b6-135">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="b30b6-136">После внесения изменений можно сохранить черновик и опубликовать изменения.</span><span class="sxs-lookup"><span data-stu-id="b30b6-136">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="b30b6-137">На следующем рисунке показано юридическое лицо, добавленное в корень иерархии, и четыре места возникновения затрат, добавленные для каналов "Торговый центр", "Торговая точка", "Интернет" и "Центр обработки вызовов".</span><span class="sxs-lookup"><span data-stu-id="b30b6-137">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="b30b6-138">Затем можно добавить каналы розничной торговли, центра обработки вызовов и интернет-каналы.</span><span class="sxs-lookup"><span data-stu-id="b30b6-138">Various retail, call center and online channels can then be added to each.</span></span>

![Пример конструктора иерархий](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="b30b6-140">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b30b6-140">Additional resources</span></span>

[<span data-ttu-id="b30b6-141">Обзор организаций и организационных иерархий</span><span class="sxs-lookup"><span data-stu-id="b30b6-141">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="b30b6-142">Планирование организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="b30b6-142">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="b30b6-143">Создание юридических лиц</span><span class="sxs-lookup"><span data-stu-id="b30b6-143">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="b30b6-144">Создание операционных единиц</span><span class="sxs-lookup"><span data-stu-id="b30b6-144">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="b30b6-145">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="b30b6-145">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="b30b6-146">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="b30b6-146">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
