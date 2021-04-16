---
title: Запуск производственного заказа
description: Следующая процедура показывает запуск производственного заказа в управлении цехом.
author: johanhoffmann
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be1c389bc4193ef080dbeb1639b69acf466ef0de
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831874"
---
# <a name="start-a-production-order"></a><span data-ttu-id="bbf62-103">Запуск производственного заказа</span><span class="sxs-lookup"><span data-stu-id="bbf62-103">Start a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bbf62-104">Следующая процедура показывает запуск производственного заказа в управлении цехом.</span><span class="sxs-lookup"><span data-stu-id="bbf62-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="bbf62-105">Потребление времени и материалов указываются в этом процессе.</span><span class="sxs-lookup"><span data-stu-id="bbf62-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="bbf62-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="bbf62-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bbf62-107">Это пятая из семи процедур, которая объясняет жизненный цикл производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="bbf62-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="bbf62-108">Запуск производственного заказа</span><span class="sxs-lookup"><span data-stu-id="bbf62-108">Start a production order</span></span>
1. <span data-ttu-id="bbf62-109">Перейдите в раздел "Управление производством" > "Производственные заказы" > "Все производственные заказы".</span><span class="sxs-lookup"><span data-stu-id="bbf62-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="bbf62-110">Выберите производственный заказ со статусом "Выпущено".</span><span class="sxs-lookup"><span data-stu-id="bbf62-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="bbf62-111">В области действий щелкните "Производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="bbf62-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="bbf62-112">Щелкните "Начать".</span><span class="sxs-lookup"><span data-stu-id="bbf62-112">Click Start.</span></span>
    * <span data-ttu-id="bbf62-113">На этой странице можно подтвердить запуск производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="bbf62-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="bbf62-114">Перейдите на вкладку "Общие".</span><span class="sxs-lookup"><span data-stu-id="bbf62-114">Click the General tab.</span></span>
5. <span data-ttu-id="bbf62-115">В поле "От операции</span><span class="sxs-lookup"><span data-stu-id="bbf62-115">In the From Oper.</span></span> <span data-ttu-id="bbf62-116">№ п/п</span><span class="sxs-lookup"><span data-stu-id="bbf62-116">No.</span></span> <span data-ttu-id="bbf62-117">введите "10".</span><span class="sxs-lookup"><span data-stu-id="bbf62-117">field, enter '10'.</span></span>
6. <span data-ttu-id="bbf62-118">В поле "Автопотребление на маршруте" выберите "Всегда".</span><span class="sxs-lookup"><span data-stu-id="bbf62-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="bbf62-119">Установите флажок "Разнести карту маршрута".</span><span class="sxs-lookup"><span data-stu-id="bbf62-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="bbf62-120">В поле "Автопотребление по спецификации" выберите "Всегда".</span><span class="sxs-lookup"><span data-stu-id="bbf62-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="bbf62-121">Установите флажок "Разнести лист подбора".</span><span class="sxs-lookup"><span data-stu-id="bbf62-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="bbf62-122">Установите флажок "Печать листа подбора".</span><span class="sxs-lookup"><span data-stu-id="bbf62-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="bbf62-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bbf62-123">Click OK.</span></span>
    * <span data-ttu-id="bbf62-124">Это напечатанный лист подбора, содержащий материалы, используемые для производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="bbf62-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="bbf62-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bbf62-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="bbf62-126">Проверка листа подбора</span><span class="sxs-lookup"><span data-stu-id="bbf62-126">Validate the picking list</span></span>
1. <span data-ttu-id="bbf62-127">В области действий щелкните "Показать".</span><span class="sxs-lookup"><span data-stu-id="bbf62-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="bbf62-128">Щелкните "Лист подбора".</span><span class="sxs-lookup"><span data-stu-id="bbf62-128">Click Picking list.</span></span>
3. <span data-ttu-id="bbf62-129">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="bbf62-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="bbf62-130">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bbf62-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="bbf62-131">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="bbf62-131">Click Edit.</span></span>
6. <span data-ttu-id="bbf62-132">В поле "Потребление" введите число.</span><span class="sxs-lookup"><span data-stu-id="bbf62-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="bbf62-133">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="bbf62-133">Click Post.</span></span>
8. <span data-ttu-id="bbf62-134">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bbf62-134">Click OK.</span></span>
    * <span data-ttu-id="bbf62-135">В журнале ведомостей комплектации разносятся материалы, потребленные производственным заказом.</span><span class="sxs-lookup"><span data-stu-id="bbf62-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="bbf62-136">Перед разноской журнала можно вносить корректировки, если есть разница между расчетным количеством и фактическим потребленным количеством.</span><span class="sxs-lookup"><span data-stu-id="bbf62-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="bbf62-137">Перейдите на вкладку "Панель сетки".</span><span class="sxs-lookup"><span data-stu-id="bbf62-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="bbf62-138">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bbf62-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="bbf62-139">Проверка журнала карты маршрута</span><span class="sxs-lookup"><span data-stu-id="bbf62-139">Verify the route card journal</span></span>
1. <span data-ttu-id="bbf62-140">В области действий щелкните "Показать".</span><span class="sxs-lookup"><span data-stu-id="bbf62-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="bbf62-141">Щелкните "Карта маршрута".</span><span class="sxs-lookup"><span data-stu-id="bbf62-141">Click Route card.</span></span>
3. <span data-ttu-id="bbf62-142">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="bbf62-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="bbf62-143">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bbf62-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="bbf62-144">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="bbf62-144">Click Edit.</span></span>
6. <span data-ttu-id="bbf62-145">В поле "Часы" введите число.</span><span class="sxs-lookup"><span data-stu-id="bbf62-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="bbf62-146">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="bbf62-146">Click Post.</span></span>
8. <span data-ttu-id="bbf62-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bbf62-147">Click OK.</span></span>
    * <span data-ttu-id="bbf62-148">В журнале карт маршрутов регистрируется время, затраченное на отдельные операции.</span><span class="sxs-lookup"><span data-stu-id="bbf62-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="bbf62-149">Правильное и ошибочное количество можно также вносить в отчет.</span><span class="sxs-lookup"><span data-stu-id="bbf62-149">Good and error quantity can also be reported.</span></span>  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]