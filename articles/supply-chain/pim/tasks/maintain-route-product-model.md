---
title: Ведение маршрута для модели продукта
description: Выполнение этой процедуры требует наличия модели конфигурации продукта.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921273"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="b50d4-103">Ведение маршрута для модели продукта</span><span class="sxs-lookup"><span data-stu-id="b50d4-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b50d4-104">Выполнение этой процедуры требует наличия модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="b50d4-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="b50d4-105">Эта процедура использует модель динамика класса Hi-End в демонстрационной компании USMF для описания процесса.</span><span class="sxs-lookup"><span data-stu-id="b50d4-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>

## <a name="add-a-route-operation"></a><span data-ttu-id="b50d4-106">Добавление операции маршрута</span><span class="sxs-lookup"><span data-stu-id="b50d4-106">Add a route operation</span></span>

1. <span data-ttu-id="b50d4-107">Перейдите в раздел **Управление сведениями о продукте \> Продукты \> Модели конфигурации продукта**.</span><span class="sxs-lookup"><span data-stu-id="b50d4-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="b50d4-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b50d4-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b50d4-109">Выберите модель динамика класса Hi--End для этого упражнения.</span><span class="sxs-lookup"><span data-stu-id="b50d4-109">Select the High end speaker model for this exercise.</span></span>  
1. <span data-ttu-id="b50d4-110">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b50d4-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="b50d4-111">Разверните раздел **Операции маршрута**.</span><span class="sxs-lookup"><span data-stu-id="b50d4-111">Expand the **Route operations** section.</span></span>
1. <span data-ttu-id="b50d4-112">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="b50d4-112">Select **Add**.</span></span>
1. <span data-ttu-id="b50d4-113">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="b50d4-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="b50d4-114">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="b50d4-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="b50d4-115">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b50d4-115">Select **Save**.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="b50d4-116">Ввод сведений об операции маршрута</span><span class="sxs-lookup"><span data-stu-id="b50d4-116">Enter route operation details</span></span>

1. <span data-ttu-id="b50d4-117">Выберите **Сведения об операции маршрута**.</span><span class="sxs-lookup"><span data-stu-id="b50d4-117">Select **Route operation details**.</span></span>
1. <span data-ttu-id="b50d4-118">В поле **Операция** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b50d4-118">In the **Operation** field, enter or select a value.</span></span>
1. <span data-ttu-id="b50d4-119">В поле **Операция №**</span><span class="sxs-lookup"><span data-stu-id="b50d4-119">In the **Oper. No.**</span></span> <span data-ttu-id="b50d4-120">введите число.</span><span class="sxs-lookup"><span data-stu-id="b50d4-120">field, enter a number.</span></span>
    * <span data-ttu-id="b50d4-121">Номера операции определяют последовательность маршрута.</span><span class="sxs-lookup"><span data-stu-id="b50d4-121">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="b50d4-122">Каждое свойство операции маршрута может получить статическое значение или быть сопоставленным с атрибутом.</span><span class="sxs-lookup"><span data-stu-id="b50d4-122">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="b50d4-123">Сопоставление с атрибутом приведет к тому, что значение будет задано в рамках конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b50d4-123">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
1. <span data-ttu-id="b50d4-124">В поле **Маршрутная группа** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b50d4-124">In the **Route group** field, enter or select a value.</span></span>
    * <span data-ttu-id="b50d4-125">Маршрутная группа определяет важное поведение для учета затрат, потребления и настройки.</span><span class="sxs-lookup"><span data-stu-id="b50d4-125">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
1. <span data-ttu-id="b50d4-126">Выберите вкладку **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="b50d4-126">Select the **Setup** tab.</span></span>
1. <span data-ttu-id="b50d4-127">Выберите вкладку **Время**.</span><span class="sxs-lookup"><span data-stu-id="b50d4-127">Select the **Times** tab.</span></span>
1. <span data-ttu-id="b50d4-128">В поле **К-во процесса** введите число.</span><span class="sxs-lookup"><span data-stu-id="b50d4-128">In the **Process qty.** field, enter a number.</span></span>
    * <span data-ttu-id="b50d4-129">Укажите количество, которое будет обработано в течение одной операции.</span><span class="sxs-lookup"><span data-stu-id="b50d4-129">Determine how many will be processed during one operation.</span></span>  
1. <span data-ttu-id="b50d4-130">В поле **Часы/время** введите число.</span><span class="sxs-lookup"><span data-stu-id="b50d4-130">In the **Hours/time** field, enter a number.</span></span>
    * <span data-ttu-id="b50d4-131">Введите коэффициент времени.</span><span class="sxs-lookup"><span data-stu-id="b50d4-131">Enter the time ratio.</span></span>  
1. <span data-ttu-id="b50d4-132">Установите флажок **Задать**.</span><span class="sxs-lookup"><span data-stu-id="b50d4-132">Select the **Set** check box.</span></span>
1. <span data-ttu-id="b50d4-133">В поле **Время выполнения** введите число.</span><span class="sxs-lookup"><span data-stu-id="b50d4-133">In the **Run time** field, enter a number.</span></span>
    * <span data-ttu-id="b50d4-134">Определите время обработки для указанного количества.</span><span class="sxs-lookup"><span data-stu-id="b50d4-134">Determine the processing time for the quantity that you have specified.</span></span>  
1. <span data-ttu-id="b50d4-135">Выберите вкладку **Потребности ресурса**.</span><span class="sxs-lookup"><span data-stu-id="b50d4-135">Select the **Resource requirements** tab.</span></span>
1. <span data-ttu-id="b50d4-136">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="b50d4-136">Select **Add**.</span></span>
1. <span data-ttu-id="b50d4-137">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b50d4-137">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="b50d4-138">В поле **Тип потребности** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="b50d4-138">In the **Requirement type** field, select an option.</span></span>
    * <span data-ttu-id="b50d4-139">Укажите при необходимости определенные ресурсы или возможности, которыми они должны обладать.</span><span class="sxs-lookup"><span data-stu-id="b50d4-139">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
1. <span data-ttu-id="b50d4-140">В поле **Потребность** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b50d4-140">In the **Requirement** field, enter or select a value.</span></span>
1. <span data-ttu-id="b50d4-141">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b50d4-141">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]