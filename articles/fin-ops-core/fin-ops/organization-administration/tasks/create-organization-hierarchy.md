---
title: Создание организационной иерархии
description: Следующая процедура используется для создания организационной иерархии.
author: sericks007
ms.date: 12/15/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d27bec86302f3e6cef8318a0d846f31d2d9c6a5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747401"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="8ec0f-103">Создание организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="8ec0f-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8ec0f-104">Следующая процедура используется для создания организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="8ec0f-105">Организационные иерархии служат для просмотра сведений и составления отчетов о бизнесе с разных точек зрения.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="8ec0f-106">Например, можно настроить одну иерархию для налоговой, юридической или правовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="8ec0f-107">И можно настроить другую иерархию, чтобы составлять отчеты с использованием финансовой информации, которая не является юридически обязательной, но используется для целей внутренней отчетности.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="8ec0f-108">Перед созданием организационной иерархию необходимо создать организации.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="8ec0f-109">Дополнительные сведения см. в задачах "Создание юридического лица" или "Создание операционной единицы".</span><span class="sxs-lookup"><span data-stu-id="8ec0f-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="8ec0f-110">Можно также создать подразделения и группы.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="8ec0f-111">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="8ec0f-112">Создание иерархии</span><span class="sxs-lookup"><span data-stu-id="8ec0f-112">Create a hierarchy</span></span>
1. <span data-ttu-id="8ec0f-113">Перейдите в раздел **Область переходов > Модули > Управление организацией > Организации > Организационные иерархии**.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="8ec0f-114">В области **Панель операций** щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="8ec0f-115">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="8ec0f-116">В разделе **Назначение** щелкните **Назначение цели**.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="8ec0f-117">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="8ec0f-118">Выберите цель для назначения организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="8ec0f-119">В разделе **Назначенные иерархии** щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-119">In the **Assigned hierarchies** section, click **Add**.</span></span>
7. <span data-ttu-id="8ec0f-120">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-120">In the list, mark the selected row.</span></span> <span data-ttu-id="8ec0f-121">Найдите только что созданную иерархию.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="8ec0f-122">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="8ec0f-123">Добавление организации в иерархию</span><span class="sxs-lookup"><span data-stu-id="8ec0f-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="8ec0f-124">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="8ec0f-125">Выберите иерархию.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="8ec0f-126">В разделе **Назначенные иерархии** щелкните **Просмотр иерархии**.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="8ec0f-127">Добавьте организации при необходимости.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="8ec0f-128">Для добавления организации нажмите кнопку **Изменить**, затем нажмите кнопку **Вставить**, чтобы добавить организацию.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="8ec0f-129">После внесения изменений можно **Сохранить** черновик и **Опубликовать** изменения.</span><span class="sxs-lookup"><span data-stu-id="8ec0f-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]