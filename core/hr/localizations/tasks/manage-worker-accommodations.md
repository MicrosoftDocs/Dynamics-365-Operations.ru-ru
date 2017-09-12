--- 
title: "Управление проживанием работников"
description: "Эта процедура демонстрирует шаги, которые необходимо предпринять для настройки типов удобств, таких как эргономичные стулья или периодические перерывы."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 10d34d0b2eca95034d1f67931ff72a035be9a6b8
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="manage-worker-accommodations"></a><span data-ttu-id="50c99-103">Управление проживанием работников</span><span class="sxs-lookup"><span data-stu-id="50c99-103">Manage worker accommodations</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="50c99-104">Эта процедура демонстрирует шаги, которые необходимо предпринять для настройки типов удобств, таких как эргономичные стулья или периодические перерывы.</span><span class="sxs-lookup"><span data-stu-id="50c99-104">This procedure walks through the steps for setting up work environment accommodation types, such as ergonomic chairs or periodic breaks.</span></span> <span data-ttu-id="50c99-105">В ней также показано, как назначить эти типы удобств работнику и либо утвердить запрос на удобства этого типа, либо отказать в нем.</span><span class="sxs-lookup"><span data-stu-id="50c99-105">It also shows how to assign these accommodation types to a worker, and either approve or deny the accommodation type.</span></span> <span data-ttu-id="50c99-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="50c99-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="setup-accommodations"></a><span data-ttu-id="50c99-107">Настройка удобств</span><span class="sxs-lookup"><span data-stu-id="50c99-107">Setup accommodations</span></span>
1. <span data-ttu-id="50c99-108">Перейдите в раздел "Управление персоналом" > "Настройка" > "Типы помещений".</span><span class="sxs-lookup"><span data-stu-id="50c99-108">Go to Human resources > Setup > Accommodation types.</span></span>
2. <span data-ttu-id="50c99-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="50c99-109">Click New.</span></span>
3. <span data-ttu-id="50c99-110">В поле "Тип проживания" введите название для удобства.</span><span class="sxs-lookup"><span data-stu-id="50c99-110">In the Accommodation type field, enter a name for the accommodation.</span></span> <span data-ttu-id="50c99-111">Пример: "Клавиатура".</span><span class="sxs-lookup"><span data-stu-id="50c99-111">Example: Keyboard.</span></span>
4. <span data-ttu-id="50c99-112">В поле "Описание" введите описание для удобства.</span><span class="sxs-lookup"><span data-stu-id="50c99-112">In the Description field, enter a description for the accommodation.</span></span> <span data-ttu-id="50c99-113">Пример: "Эргономичная клавиатура".</span><span class="sxs-lookup"><span data-stu-id="50c99-113">Example: Ergonomic Keyboard.</span></span>
5. <span data-ttu-id="50c99-114">В поле "Примечание" введите какую-либо информацию, которая помогает понять, в чем суть удобства.</span><span class="sxs-lookup"><span data-stu-id="50c99-114">In the Note field, enter any information that helps to clarify the accommodation.</span></span>
6. <span data-ttu-id="50c99-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="50c99-115">Click Save.</span></span>
7. <span data-ttu-id="50c99-116">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="50c99-116">Close the page.</span></span>

## <a name="assign-accommodations"></a><span data-ttu-id="50c99-117">Назначение удобств</span><span class="sxs-lookup"><span data-stu-id="50c99-117">Assign accommodations</span></span>
1. <span data-ttu-id="50c99-118">Перейдите в раздел "Управление персоналом" > "Работники" > "Сотрудники".</span><span class="sxs-lookup"><span data-stu-id="50c99-118">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="50c99-119">Выберите в списке сотрудника.</span><span class="sxs-lookup"><span data-stu-id="50c99-119">From the list, select an employee.</span></span>
3. <span data-ttu-id="50c99-120">Щелкните имя сотрудника, чтобы просмотреть сведения о сотруднике, который запрашивает удобство.</span><span class="sxs-lookup"><span data-stu-id="50c99-120">Click the employee's name to view details about the employee who is requesting the accommodation.</span></span>
4. <span data-ttu-id="50c99-121">Разверните экспресс-вкладку "Личные данные".</span><span class="sxs-lookup"><span data-stu-id="50c99-121">Expand the Personal information FastTab.</span></span>
5. <span data-ttu-id="50c99-122">Щелкните "Проживание".</span><span class="sxs-lookup"><span data-stu-id="50c99-122">Click Accommodations.</span></span>
6. <span data-ttu-id="50c99-123">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="50c99-123">Click New.</span></span>
7. <span data-ttu-id="50c99-124">В поле "Тип проживания" выберите соответствующее удобство.</span><span class="sxs-lookup"><span data-stu-id="50c99-124">In the Accommodation type field, select the appropriate accommodation.</span></span> <span data-ttu-id="50c99-125">Пример: "Клавиатура"</span><span class="sxs-lookup"><span data-stu-id="50c99-125">Example: Keyboard</span></span>
8. <span data-ttu-id="50c99-126">В поле "Задача задания" выберите рабочую задачу, для которой необходимо запрашиваемое удобство.</span><span class="sxs-lookup"><span data-stu-id="50c99-126">In the Job task field, enter the work task that requires the accommodation.</span></span>
9. <span data-ttu-id="50c99-127">В поле "Статус" введите соответствующий статус.</span><span class="sxs-lookup"><span data-stu-id="50c99-127">In the Status field, enter the appropriate status.</span></span> <span data-ttu-id="50c99-128">Пример: "Разумно"</span><span class="sxs-lookup"><span data-stu-id="50c99-128">Example: Reasonable</span></span>
    * <span data-ttu-id="50c99-129">Предусмотрены следующие статусы.</span><span class="sxs-lookup"><span data-stu-id="50c99-129">The following statuses are available.</span></span> <span data-ttu-id="50c99-130">Статус "Запрошено" означает, что запрос на удобство создан, но еще не рассмотрен.</span><span class="sxs-lookup"><span data-stu-id="50c99-130">Requested indicates that the accommodation has been created but not yet reviewed.</span></span> <span data-ttu-id="50c99-131">Статус "Разумно" означает, что запрос на удобство является разумным и будет удовлетворен.</span><span class="sxs-lookup"><span data-stu-id="50c99-131">Reasonable indicates that the accommodation is reasonable and will be granted.</span></span> <span data-ttu-id="50c99-132">Статус "Чрезмерные трудности" означает, что удовлетворение запроса на удобство будет связано с чрезмерными трудностями для работодателя, поэтому в запросе отказано.</span><span class="sxs-lookup"><span data-stu-id="50c99-132">Undue hardship indicates that the accommodation will place an unreasonable burden on the employer, and has been denied.</span></span> <span data-ttu-id="50c99-133">В этом примере запрос был утвержден немедленно, поскольку запрос на удобство минимальным.</span><span class="sxs-lookup"><span data-stu-id="50c99-133">In this example, the request was approved immediately because the accommodation request was minimal.</span></span>  
10. <span data-ttu-id="50c99-134">В поле "Принято" выберите пользователя, который принял запрос на удобство.</span><span class="sxs-lookup"><span data-stu-id="50c99-134">In the Accepted field, select the person who accepted the accommodation request.</span></span>
11. <span data-ttu-id="50c99-135">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="50c99-135">Click Select.</span></span>
12. <span data-ttu-id="50c99-136">В поле "Дата и время принятия" введите дату и время принятия запроса на удобство.</span><span class="sxs-lookup"><span data-stu-id="50c99-136">In the Accepted date field, enter the date and time when the accommodation request was accepted.</span></span>
13. <span data-ttu-id="50c99-137">Разверните раздел "Примечание".</span><span class="sxs-lookup"><span data-stu-id="50c99-137">Expand the Note section.</span></span>
14. <span data-ttu-id="50c99-138">В поле "Финансовое" введите какую-либо информацию или затраты на ресурсы, которые помогают понять стоимость удобства.</span><span class="sxs-lookup"><span data-stu-id="50c99-138">In the Financial field, enter any information or resource costs that helps to clarify the impact of the accommodation.</span></span>
    * <span data-ttu-id="50c99-139">Если в запросе на проживание отказано, в поле "Ответ" можно указать, почему в запросе было отказано.</span><span class="sxs-lookup"><span data-stu-id="50c99-139">If the accommodation has been denied, the Reply field can be used to indicate why a request was denied.</span></span>  
15. <span data-ttu-id="50c99-140">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="50c99-140">Click Save.</span></span>


