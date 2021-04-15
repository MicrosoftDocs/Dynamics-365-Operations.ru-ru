---
title: Поиск устаревших вариантов продуктов
description: В данной процедуре показано, как находить устаревшие используемые продукты или варианты продуктов, а также как связать состояние жизненного цикла продукта с устаревшими продуктами.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 807297a87a7f0e59023d80fbd371bffbf2b086bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808000"
---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="ae294-103">Поиск устаревших вариантов продуктов</span><span class="sxs-lookup"><span data-stu-id="ae294-103">Find obsolete product variants</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae294-104">В данной процедуре показано, как находить устаревшие используемые продукты или варианты продуктов, а также как связать состояние жизненного цикла продукта с устаревшими продуктами.</span><span class="sxs-lookup"><span data-stu-id="ae294-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="ae294-105">Необходимое условие: следует определить по крайней мере одно состояние жизненного цикла продукта, которое неактивно для планирования, до запуска этого проводника по задаче.</span><span class="sxs-lookup"><span data-stu-id="ae294-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="ae294-106">Выполнение моделирования</span><span class="sxs-lookup"><span data-stu-id="ae294-106">Run a simulation</span></span>
1. <span data-ttu-id="ae294-107">Перейдите в раздел "Управление сведениями о продукте" > "Периодические задачи" > "Изменить состояние жизненного цикла для устаревших продуктов".</span><span class="sxs-lookup"><span data-stu-id="ae294-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="ae294-108">В поле "Новое состояние жизненного цикла продукта" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ae294-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="ae294-109">Выберите "Да" в поле "Запустить моделирование без обновления данных о продуктах".</span><span class="sxs-lookup"><span data-stu-id="ae294-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="ae294-110">В поле "Исключить продукты, созданные в течение этого числа дней" введите число.</span><span class="sxs-lookup"><span data-stu-id="ae294-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="ae294-111">В поле "Исключить продукты, использованные в транзакциях (в днях)" введите число.</span><span class="sxs-lookup"><span data-stu-id="ae294-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="ae294-112">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="ae294-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="ae294-113">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="ae294-113">Click Filter.</span></span>
8. <span data-ttu-id="ae294-114">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="ae294-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="ae294-115">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ae294-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="ae294-116">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ae294-116">Click OK.</span></span>
11. <span data-ttu-id="ae294-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ae294-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="ae294-118">Рекомендуется выполнять пакетное моделирование, если ожидается, что будет выполняться поиск большого числа продуктов.</span><span class="sxs-lookup"><span data-stu-id="ae294-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="ae294-119">Кроме того убедитесь, что моделирование не выполняется в наиболее активное рабочее время компании.</span><span class="sxs-lookup"><span data-stu-id="ae294-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="ae294-120">Проверка результатов моделирования</span><span class="sxs-lookup"><span data-stu-id="ae294-120">Review the simulation results</span></span>
1. <span data-ttu-id="ae294-121">Перейдите в раздел "Управление сведениями о продукте" > "Запросы и отчеты" > "Журнал обслуживания состояний жизненного цикла продуктов".</span><span class="sxs-lookup"><span data-stu-id="ae294-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="ae294-122">На этой странице можно просмотреть результаты моделирования и оценить, сколько продуктов и вариантов продукта будут связаны с новым состоянием жизненного цикла продукта при выполнении обновления без моделирования.</span><span class="sxs-lookup"><span data-stu-id="ae294-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="ae294-123">Запуск обновления состояния жизненного цикла продукта для устаревших продуктов</span><span class="sxs-lookup"><span data-stu-id="ae294-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="ae294-124">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ae294-124">Close the page.</span></span>
2. <span data-ttu-id="ae294-125">Перейдите в раздел "Управление сведениями о продукте" > "Периодические задачи" > "Изменить состояние жизненного цикла для устаревших продуктов".</span><span class="sxs-lookup"><span data-stu-id="ae294-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="ae294-126">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="ae294-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="ae294-127">Обратите внимание, что был сохранен последний выбор.</span><span class="sxs-lookup"><span data-stu-id="ae294-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="ae294-128">Выберите "Нет" в поле "Запустить моделирование без обновления данных о продуктах".</span><span class="sxs-lookup"><span data-stu-id="ae294-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="ae294-129">Разверните раздел "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="ae294-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="ae294-130">В зависимости от того, сколько продуктов и вариантов продуктов затронуто, рассмотрите возможность пакетного выполнения этого задания.</span><span class="sxs-lookup"><span data-stu-id="ae294-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="ae294-131">Убедитесь, что задание значительных обновлений не выполняется в наиболее активное рабочее время компании.</span><span class="sxs-lookup"><span data-stu-id="ae294-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="ae294-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ae294-132">Click OK.</span></span>
7. <span data-ttu-id="ae294-133">Перейдите в раздел "Управление сведениями о продукте" > "Запросы и отчеты" > "Журнал обслуживания состояний жизненного цикла продуктов".</span><span class="sxs-lookup"><span data-stu-id="ae294-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="ae294-134">Просмотрите измененные выпущенные продукты и варианты продуктов.</span><span class="sxs-lookup"><span data-stu-id="ae294-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="ae294-135">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ae294-135">In the list, find and select the desired record.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]