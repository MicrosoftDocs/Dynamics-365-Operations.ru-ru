---
title: Создание организационной иерархии
description: Следующая процедура используется для создания организационной иерархии.
author: sericks007
manager: AnnBe
ms.date: 12/15/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8627c1aa0ce9ec011b568224040b1143f0f54c31
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796930"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="997d6-103">Создание организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="997d6-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="997d6-104">Следующая процедура используется для создания организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="997d6-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="997d6-105">Организационные иерархии служат для просмотра сведений и составления отчетов о бизнесе с разных точек зрения.</span><span class="sxs-lookup"><span data-stu-id="997d6-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="997d6-106">Например, можно настроить одну иерархию для налоговой, юридической или правовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="997d6-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="997d6-107">И можно настроить другую иерархию, чтобы составлять отчеты с использованием финансовой информации, которая не является юридически обязательной, но используется для целей внутренней отчетности.</span><span class="sxs-lookup"><span data-stu-id="997d6-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="997d6-108">Перед созданием организационной иерархию необходимо создать организации.</span><span class="sxs-lookup"><span data-stu-id="997d6-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="997d6-109">Дополнительные сведения см. в задачах "Создание юридического лица" или "Создание операционной единицы".</span><span class="sxs-lookup"><span data-stu-id="997d6-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="997d6-110">Можно также создать подразделения и группы.</span><span class="sxs-lookup"><span data-stu-id="997d6-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="997d6-111">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="997d6-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="997d6-112">Создание иерархии</span><span class="sxs-lookup"><span data-stu-id="997d6-112">Create a hierarchy</span></span>
1. <span data-ttu-id="997d6-113">Перейдите в раздел **Область переходов > Модули > Управление организацией > Организации > Организационные иерархии**.</span><span class="sxs-lookup"><span data-stu-id="997d6-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="997d6-114">В области **Панель операций** щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="997d6-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="997d6-115">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="997d6-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="997d6-116">В разделе **Назначение** щелкните **Назначение цели**.</span><span class="sxs-lookup"><span data-stu-id="997d6-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="997d6-117">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="997d6-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="997d6-118">Выберите цель для назначения организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="997d6-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="997d6-119">В разделе **Назначенные иерархии** щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="997d6-119">In the **Assigned hierarchies** section, click **Add**.</span></span>
7. <span data-ttu-id="997d6-120">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="997d6-120">In the list, mark the selected row.</span></span> <span data-ttu-id="997d6-121">Найдите только что созданную иерархию.</span><span class="sxs-lookup"><span data-stu-id="997d6-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="997d6-122">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="997d6-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="997d6-123">Добавление организации в иерархию</span><span class="sxs-lookup"><span data-stu-id="997d6-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="997d6-124">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="997d6-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="997d6-125">Выберите иерархию.</span><span class="sxs-lookup"><span data-stu-id="997d6-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="997d6-126">В разделе **Назначенные иерархии** щелкните **Просмотр иерархии**.</span><span class="sxs-lookup"><span data-stu-id="997d6-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="997d6-127">Добавьте организации при необходимости.</span><span class="sxs-lookup"><span data-stu-id="997d6-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="997d6-128">Для добавления организации нажмите кнопку **Изменить**, затем нажмите кнопку **Вставить**, чтобы добавить организацию.</span><span class="sxs-lookup"><span data-stu-id="997d6-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="997d6-129">После внесения изменений можно **Сохранить** черновик и **Опубликовать** изменения.</span><span class="sxs-lookup"><span data-stu-id="997d6-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  

