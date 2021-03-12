---
title: Настройка организационных иерархий
description: В этом разделе описывается, как настроить организационные иерархии в Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b887616ef29396ba99ca0c7428ab89df01b3008c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997783"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="7c663-103">Настройка организационных иерархий</span><span class="sxs-lookup"><span data-stu-id="7c663-103">Set up organization hierarchies</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7c663-104">В этом разделе описывается, как настроить организационные иерархии в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7c663-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7c663-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="7c663-105">Overview</span></span>

<span data-ttu-id="7c663-106">Перед созданием каналов необходимо подтвердить настройку организационных иерархий.</span><span class="sxs-lookup"><span data-stu-id="7c663-106">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="7c663-107">Организационные иерархии служат для просмотра сведений и составления отчетов о бизнесе с разных точек зрения.</span><span class="sxs-lookup"><span data-stu-id="7c663-107">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="7c663-108">Например, можно настроить одну иерархию для налоговой, юридической или правовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="7c663-108">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="7c663-109">И можно настроить другую иерархию, чтобы составлять отчеты с использованием финансовой информации, которая не является юридически обязательной, но используется для целей внутренней отчетности.</span><span class="sxs-lookup"><span data-stu-id="7c663-109">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="7c663-110">Перед созданием организационной иерархии необходимо создать организации.</span><span class="sxs-lookup"><span data-stu-id="7c663-110">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="7c663-111">Дополнительные сведения см. в задачах [Создание юридических лиц](channels-legal-entities.md) или [Создание операционных единиц](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="7c663-111">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="7c663-112">Дополнительные сведения см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="7c663-112">For more information, see the following topics.</span></span>
- [<span data-ttu-id="7c663-113">Обзор организаций и организационных иерархий</span><span class="sxs-lookup"><span data-stu-id="7c663-113">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="7c663-114">Планирование организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="7c663-114">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="7c663-115">Создание организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="7c663-115">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="7c663-116">Создание организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="7c663-116">Create an organizational hierarchy</span></span>

<span data-ttu-id="7c663-117">Для создания организационной иерархии выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7c663-117">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="7c663-118">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Организационные иерархии**.</span><span class="sxs-lookup"><span data-stu-id="7c663-118">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="7c663-119">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7c663-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7c663-120">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="7c663-120">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="7c663-121">В разделе **Назначение** выберите **Назначение цели**.</span><span class="sxs-lookup"><span data-stu-id="7c663-121">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="7c663-122">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="7c663-122">In the list, find and select the desired record.</span></span> <span data-ttu-id="7c663-123">Выберите цель для назначения организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="7c663-123">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="7c663-124">В разделе **Назначенные иерархии** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="7c663-124">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="7c663-125">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="7c663-125">In the list, mark the selected row.</span></span> <span data-ttu-id="7c663-126">Найдите только что созданную иерархию.</span><span class="sxs-lookup"><span data-stu-id="7c663-126">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="7c663-127">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7c663-127">Select **OK**.</span></span>

<span data-ttu-id="7c663-128">На следующем рисунке показан пример организационной иерархии, созданной для вымышленного набора магазинов "Adventure Works".</span><span class="sxs-lookup"><span data-stu-id="7c663-128">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Пример организационное иерархии](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="7c663-130">Добавление организаций в иерархию</span><span class="sxs-lookup"><span data-stu-id="7c663-130">Add organizations to a hierarchy</span></span>

<span data-ttu-id="7c663-131">Чтобы добавить организации в иерархию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7c663-131">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="7c663-132">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="7c663-132">In the list, find and select the desired record.</span></span> <span data-ttu-id="7c663-133">Выберите иерархию.</span><span class="sxs-lookup"><span data-stu-id="7c663-133">Select your hierarchy.</span></span>
1. <span data-ttu-id="7c663-134">На панели операций выберите **Вид**.</span><span class="sxs-lookup"><span data-stu-id="7c663-134">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="7c663-135">Добавьте организации при необходимости.</span><span class="sxs-lookup"><span data-stu-id="7c663-135">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="7c663-136">Чтобы добавить организацию, выберите **Правка**, затем выберите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="7c663-136">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="7c663-137">После внесения изменений можно сохранить черновик и опубликовать изменения.</span><span class="sxs-lookup"><span data-stu-id="7c663-137">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="7c663-138">На следующем рисунке показано юридическое лицо, добавленное в корень иерархии, и четыре места возникновения затрат, добавленные для каналов "Торговый центр", "Торговая точка", "Интернет" и "Центр обработки вызовов".</span><span class="sxs-lookup"><span data-stu-id="7c663-138">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="7c663-139">Затем можно добавить каналы розничной торговли, центра обработки вызовов и интернет-каналы.</span><span class="sxs-lookup"><span data-stu-id="7c663-139">Various retail, call center and online channels can then be added to each.</span></span>

![Пример конструктора иерархий](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="7c663-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7c663-141">Additional resources</span></span>

[<span data-ttu-id="7c663-142">Обзор организаций и организационных иерархий</span><span class="sxs-lookup"><span data-stu-id="7c663-142">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="7c663-143">Планирование организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="7c663-143">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="7c663-144">Создание юридических лиц</span><span class="sxs-lookup"><span data-stu-id="7c663-144">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="7c663-145">Создание операционных единиц</span><span class="sxs-lookup"><span data-stu-id="7c663-145">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="7c663-146">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="7c663-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7c663-147">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="7c663-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)
