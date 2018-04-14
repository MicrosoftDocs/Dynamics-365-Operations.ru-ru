--- 
title: "Создание организационной иерархии"
description: "Следующая процедура используется для создания организационной иерархии."
author: sericks007
manager: AnnBe
ms.date: 06/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2deec5470eef68f18042bb789e3760189caffdeb
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="a27c0-103">Создание организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="a27c0-103">Create an organization hierarchy</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a27c0-104">Следующая процедура используется для создания организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="a27c0-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="a27c0-105">Организационные иерархии служат для просмотра сведений и составления отчетов о бизнесе с разных точек зрения.</span><span class="sxs-lookup"><span data-stu-id="a27c0-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="a27c0-106">Например, можно настроить одну иерархию для налоговой, юридической или правовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="a27c0-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="a27c0-107">И можно настроить другую иерархию, чтобы составлять отчеты с использованием финансовой информации, которая не является юридически обязательной, но используется для целей внутренней отчетности.</span><span class="sxs-lookup"><span data-stu-id="a27c0-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 



<span data-ttu-id="a27c0-108">Перед созданием организационной иерархию необходимо создать организации.</span><span class="sxs-lookup"><span data-stu-id="a27c0-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="a27c0-109">Дополнительные сведения см. в задачах "Создание юридического лица" или "Создание операционной единицы".</span><span class="sxs-lookup"><span data-stu-id="a27c0-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="a27c0-110">Можно также создать подразделения и группы.</span><span class="sxs-lookup"><span data-stu-id="a27c0-110">You can also create departments and teams.</span></span> 



<span data-ttu-id="a27c0-111">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="a27c0-111">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-hierarchy"></a><span data-ttu-id="a27c0-112">Создание иерархии</span><span class="sxs-lookup"><span data-stu-id="a27c0-112">Create a hierarchy</span></span>
1. <span data-ttu-id="a27c0-113">Перейдите в раздел "Управление организацией" > "Организации" > "Организационные иерархии".</span><span class="sxs-lookup"><span data-stu-id="a27c0-113">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="a27c0-114">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a27c0-114">Click New.</span></span>
3. <span data-ttu-id="a27c0-115">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a27c0-115">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a27c0-116">Щелкните "Назначить цель".</span><span class="sxs-lookup"><span data-stu-id="a27c0-116">Click Assign purpose.</span></span>
5. <span data-ttu-id="a27c0-117">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a27c0-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a27c0-118">Выберите цель для назначения организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="a27c0-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="a27c0-119">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="a27c0-119">Click Add.</span></span>
7. <span data-ttu-id="a27c0-120">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="a27c0-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a27c0-121">Найдите только что созданную иерархию.</span><span class="sxs-lookup"><span data-stu-id="a27c0-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="a27c0-122">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a27c0-122">Click OK.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="a27c0-123">Добавление организации в иерархию</span><span class="sxs-lookup"><span data-stu-id="a27c0-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="a27c0-124">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a27c0-124">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a27c0-125">Выберите иерархию.</span><span class="sxs-lookup"><span data-stu-id="a27c0-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="a27c0-126">Щелкните "Просмотр иерархии".</span><span class="sxs-lookup"><span data-stu-id="a27c0-126">Click View hierarchy.</span></span>
    * <span data-ttu-id="a27c0-127">Добавьте организации при необходимости.</span><span class="sxs-lookup"><span data-stu-id="a27c0-127">Add organizations, as necessary.</span></span>  
    * <span data-ttu-id="a27c0-128">Для добавления организации нажмите кнопку "Изменить", затем нажмите кнопку "Вставить", чтобы добавить организацию.</span><span class="sxs-lookup"><span data-stu-id="a27c0-128">To add an organization, click Edit and then Insert to add the organization.</span></span>     <span data-ttu-id="a27c0-129">После внесения изменений можно сохранить черновик и опубликовать изменения.</span><span class="sxs-lookup"><span data-stu-id="a27c0-129">When you are done making changes you can save a draft and/or publish the changes.</span></span>  


