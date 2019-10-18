---
title: Создание шаблона процесса в Attract
description: Этот раздел содержит сведения о порядке создания шаблона процесса в Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 694835d20e3401aaeb22aa19082a2cd0e3a0163a
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010714"
---
# <a name="create-a-process-template"></a><span data-ttu-id="a5233-103">Создание шаблона процессов</span><span class="sxs-lookup"><span data-stu-id="a5233-103">Create a process template</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a5233-104">*Шаблон процесса найма на работу* содержит все действия, которые должны быть включены как часть процесса найма на работу.</span><span class="sxs-lookup"><span data-stu-id="a5233-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="a5233-105">В этом разделе описаны элементы шаблона процесса в Microsoft Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="a5233-105">This topic describes the elements of a process template in Microsoft Dynamics 365 Talent: Attract.</span></span> <span data-ttu-id="a5233-106">Также объясняется, как создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="a5233-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="a5233-107">Создание шаблона является частью надстройки Comprehensive Hiring для Attract.</span><span class="sxs-lookup"><span data-stu-id="a5233-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="a5233-108">Управление шаблонами</span><span class="sxs-lookup"><span data-stu-id="a5233-108">Template management</span></span>

<span data-ttu-id="a5233-109">Компании могут сами решать, кто может создавать шаблоны процессов в Attract: участники рабочей группы найма или только администраторы.</span><span class="sxs-lookup"><span data-stu-id="a5233-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="a5233-110">Для настройки управления шаблонами выберите **Центр администрирования** \> **Управление шаблонами**.</span><span class="sxs-lookup"><span data-stu-id="a5233-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="a5233-111">Чтобы разрешить членам группы создавать собственные шаблоны, включите управление шаблонами.</span><span class="sxs-lookup"><span data-stu-id="a5233-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="a5233-112">Если не включить управление шаблонами, только администраторы могут создавать шаблоны.</span><span class="sxs-lookup"><span data-stu-id="a5233-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="a5233-113">Шаблон по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a5233-113">Default template</span></span>

<span data-ttu-id="a5233-114">Только администраторы могут задавать шаблон по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a5233-114">Only admins can set the default template.</span></span> <span data-ttu-id="a5233-115">Шаблон по умолчанию используется в том случае, если шаблон не выбран при создании должности.</span><span class="sxs-lookup"><span data-stu-id="a5233-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="a5233-116">Для задания шаблона по умолчанию выберите **Центр администрирования** \> **Управление шаблонами**.</span><span class="sxs-lookup"><span data-stu-id="a5233-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="a5233-117">На карточке для шаблона, который должен быть шаблоном по умолчанию, нажмите кнопку с многоточием (**...**), затем выберите **Установить по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="a5233-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="a5233-118">Создание шаблона процесса</span><span class="sxs-lookup"><span data-stu-id="a5233-118">Create a process template</span></span>

<span data-ttu-id="a5233-119">Администраторы, агенты по найму кадров и менеджеры по найму могут создавать шаблоны процессов.</span><span class="sxs-lookup"><span data-stu-id="a5233-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="a5233-120">Шаблон процесса состоит из *этапов* и *действий*.</span><span class="sxs-lookup"><span data-stu-id="a5233-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="a5233-121">Этапы группируют одно или несколько действий.</span><span class="sxs-lookup"><span data-stu-id="a5233-121">Stages group together one or more activities.</span></span> <span data-ttu-id="a5233-122">По умолчанию, каждый шаблон процесса имеет действия "Соискатель", "Заявление" и "Предложение".</span><span class="sxs-lookup"><span data-stu-id="a5233-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="a5233-123">Этапы, которые содержат эти действия, могут быть переименованы.</span><span class="sxs-lookup"><span data-stu-id="a5233-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="a5233-124">Можно добавить дополнительные этапы, выбрав **+ Новый этап**.</span><span class="sxs-lookup"><span data-stu-id="a5233-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="a5233-125">Действия можно добавить в этап, перетащив их в соответствующий этап или двойным щелчком по ним в списке действий.</span><span class="sxs-lookup"><span data-stu-id="a5233-125">You can activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="a5233-126">Имена этапов отображаются для кандидатов на странице **Статус заявления**.</span><span class="sxs-lookup"><span data-stu-id="a5233-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="a5233-127">При выборе имен для этапов следует учитывать этот факт.</span><span class="sxs-lookup"><span data-stu-id="a5233-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="a5233-128">Дополнительные сведения о действиях см. в разделе [Действия процесса найма в Attract](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="a5233-128">To learn more about activities, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

<span data-ttu-id="a5233-129">Чтобы создать шаблон процесса, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a5233-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="a5233-130">Перейдите в пункт **Шаблоны**.</span><span class="sxs-lookup"><span data-stu-id="a5233-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="a5233-131">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a5233-131">Select **New**.</span></span>
3. <span data-ttu-id="a5233-132">В поле **Имя шаблона** введите имя для шаблона, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a5233-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="a5233-133">В списке **Выберите процесс утверждения** выберите **По умолчанию**, чтобы требовать утверждения для должности.</span><span class="sxs-lookup"><span data-stu-id="a5233-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="a5233-134">Выберите, чтобы включить или отключить соискателей.</span><span class="sxs-lookup"><span data-stu-id="a5233-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="a5233-135">Необязательно: добавление или удаление этапов.</span><span class="sxs-lookup"><span data-stu-id="a5233-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="a5233-136">Чтобы добавить стадию выберите **+ Создать стадию**.</span><span class="sxs-lookup"><span data-stu-id="a5233-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="a5233-137">Чтобы удалить этап, наведите указатель на этап, затем выберите кнопку корзины, которая появится.</span><span class="sxs-lookup"><span data-stu-id="a5233-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a5233-138">Этапы "Соискатель", "Заявление" и "Предложение" удалить невозможно, но их можно переименовать.</span><span class="sxs-lookup"><span data-stu-id="a5233-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="a5233-139">Необязательно: добавление или удаление действий.</span><span class="sxs-lookup"><span data-stu-id="a5233-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="a5233-140">Чтобы добавить действие, перетащите его из списка действий справа на соответствующий этап.</span><span class="sxs-lookup"><span data-stu-id="a5233-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="a5233-141">Можно также дважды щелкнуть действие, затем выбирать стадию, в которую его требуется добавить.</span><span class="sxs-lookup"><span data-stu-id="a5233-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="a5233-142">Чтобы удалить действие, разверните его, затем выберите кнопку корзины в заголовке действия.</span><span class="sxs-lookup"><span data-stu-id="a5233-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="a5233-143">Выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a5233-143">Select **Save**.</span></span>
