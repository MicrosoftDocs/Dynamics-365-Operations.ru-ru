---
title: Ведение маршрута для модели продукта
description: Выполнение этой процедуры требует наличия модели конфигурации продукта.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e793466e021671501570aed06959d684d5e9c15
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "317162"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="7ca8a-103">Ведение маршрута для модели продукта</span><span class="sxs-lookup"><span data-stu-id="7ca8a-103">Maintain route for a product model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7ca8a-104">Выполнение этой процедуры требует наличия модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="7ca8a-105">Эта процедура использует модель динамика класса Hi-End в демонстрационной компании USMF для описания процесса.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="7ca8a-106">Добавление операции маршрута</span><span class="sxs-lookup"><span data-stu-id="7ca8a-106">Add a route operation</span></span>
1. <span data-ttu-id="7ca8a-107">Щелкните "Определение модели вариантов продукта".</span><span class="sxs-lookup"><span data-stu-id="7ca8a-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="7ca8a-108">Щелкните "Модели конфигурации продукта".</span><span class="sxs-lookup"><span data-stu-id="7ca8a-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="7ca8a-109">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7ca8a-110">Выберите модель динамика класса Hi--End для этого упражнения.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="7ca8a-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="7ca8a-112">Разверните раздел "Операции маршрута".</span><span class="sxs-lookup"><span data-stu-id="7ca8a-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="7ca8a-113">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-113">Click Add.</span></span>
7. <span data-ttu-id="7ca8a-114">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="7ca8a-115">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="7ca8a-116">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="7ca8a-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="7ca8a-117">Ввод сведений об операции маршрута</span><span class="sxs-lookup"><span data-stu-id="7ca8a-117">Enter route operation details</span></span>
1. <span data-ttu-id="7ca8a-118">Щелкните "Сведения об операции маршрута".</span><span class="sxs-lookup"><span data-stu-id="7ca8a-118">Click Route operation details.</span></span>
2. <span data-ttu-id="7ca8a-119">В поле "Операция" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="7ca8a-120">В поле Операция</span><span class="sxs-lookup"><span data-stu-id="7ca8a-120">In the Oper.</span></span> <span data-ttu-id="7ca8a-121">№ п/п</span><span class="sxs-lookup"><span data-stu-id="7ca8a-121">No.</span></span> <span data-ttu-id="7ca8a-122">введите число.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-122">field, enter a number.</span></span>
    * <span data-ttu-id="7ca8a-123">Номера операции определяют последовательность маршрута.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="7ca8a-124">Каждое свойство операции маршрута может получить статическое значение или быть сопоставленным с атрибутом.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="7ca8a-125">Сопоставление с атрибутом приведет к тому, что значение будет задано в рамках конфигурации.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="7ca8a-126">В поле "Маршрутная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="7ca8a-127">Маршрутная группа определяет важное поведение для учета затрат, потребления и настройки.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="7ca8a-128">Перейдите на вкладку "Настройка".</span><span class="sxs-lookup"><span data-stu-id="7ca8a-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="7ca8a-129">Перейдите на вкладку "Время".</span><span class="sxs-lookup"><span data-stu-id="7ca8a-129">Click the Times tab.</span></span>
7. <span data-ttu-id="7ca8a-130">В поле "К-во процесса" введите число.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="7ca8a-131">Укажите количество, которое будет обработано в течение одной операции.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="7ca8a-132">В поле "Часы/время" введите число.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="7ca8a-133">Введите коэффициент времени.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="7ca8a-134">Установите флажок "Задать".</span><span class="sxs-lookup"><span data-stu-id="7ca8a-134">Select the Set check box.</span></span>
10. <span data-ttu-id="7ca8a-135">В поле "Время выполнения" введите число.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="7ca8a-136">Определите время обработки для указанного количества.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="7ca8a-137">Нажмите на вкладку "Потребности ресурса".</span><span class="sxs-lookup"><span data-stu-id="7ca8a-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="7ca8a-138">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-138">Click Add.</span></span>
13. <span data-ttu-id="7ca8a-139">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="7ca8a-140">В поле "Тип потребности" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="7ca8a-141">Укажите при необходимости определенные ресурсы или возможности, которыми они должны обладать.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="7ca8a-142">В поле "Потребность" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="7ca8a-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="7ca8a-143">Click OK.</span></span>

