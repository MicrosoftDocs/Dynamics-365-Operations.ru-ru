---
title: "Контроль качества товаров"
description: "В этой процедуре показано, как обрабатывать заказ контроля качества."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 3a4ace658b8a3a20d613b7a251eb85c32c7f1c09
ms.contentlocale: ru-ru
ms.lasthandoff: 01/17/2018

---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="ac15e-103">Контроль качества товаров</span><span class="sxs-lookup"><span data-stu-id="ac15e-103">Inspect the quality of goods</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ac15e-104">В этой процедуре показано, как обрабатывать заказ контроля качества.</span><span class="sxs-lookup"><span data-stu-id="ac15e-104">This procedure shows you how to process a quality order.</span></span> <span data-ttu-id="ac15e-105">Это руководство можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="ac15e-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="ac15e-106">Перед началом этой процедуры необходимо подтвердить заказ на покупку "000016" и разнести поступление продуктов.</span><span class="sxs-lookup"><span data-stu-id="ac15e-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="ac15e-107">При этом автоматически будет создан заказ контроля качества.</span><span class="sxs-lookup"><span data-stu-id="ac15e-107">This will automatically create a quality order.</span></span> <span data-ttu-id="ac15e-108">Контроль качества обычно производится сотрудником отдела контроля качества.</span><span class="sxs-lookup"><span data-stu-id="ac15e-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="ac15e-109">Выбор заказа контроля качества</span><span class="sxs-lookup"><span data-stu-id="ac15e-109">Select a quality order</span></span>
1. <span data-ttu-id="ac15e-110">Перейдите в раздел "Управление запасами" > "Периодические задачи" > "Управление качеством" > "Заказы контроля качества".</span><span class="sxs-lookup"><span data-stu-id="ac15e-110">Go to Inventory management > Periodic tasks > Quality management > Quality orders.</span></span>
2. <span data-ttu-id="ac15e-111">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="ac15e-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ac15e-112">Выберите заказ контроля качества, созданный перед началом этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="ac15e-112">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="ac15e-113">Запись результатов проверки</span><span class="sxs-lookup"><span data-stu-id="ac15e-113">Record test results</span></span>
1. <span data-ttu-id="ac15e-114">Щелкните "Результаты".</span><span class="sxs-lookup"><span data-stu-id="ac15e-114">Click Results.</span></span>
2. <span data-ttu-id="ac15e-115">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="ac15e-115">Click Edit.</span></span>
3. <span data-ttu-id="ac15e-116">В поле "Итоговое количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="ac15e-116">In the Result quantity field, enter a number.</span></span>
4. <span data-ttu-id="ac15e-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="ac15e-117">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="ac15e-118">В поле "Результат" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="ac15e-118">In the Outcome field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ac15e-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ac15e-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ac15e-120">В этом примере результат основан на заранее определенном итоге.</span><span class="sxs-lookup"><span data-stu-id="ac15e-120">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="ac15e-121">Обычно фиксируется более конкретный результат испытаний, например размер или другая аналитика.</span><span class="sxs-lookup"><span data-stu-id="ac15e-121">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
7. <span data-ttu-id="ac15e-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ac15e-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ac15e-123">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="ac15e-123">Click Save.</span></span>
9. <span data-ttu-id="ac15e-124">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ac15e-124">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="ac15e-125">Проверить заказ контроля качества</span><span class="sxs-lookup"><span data-stu-id="ac15e-125">Validate the quality order</span></span>
1. <span data-ttu-id="ac15e-126">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="ac15e-126">Click Validate.</span></span>
2. <span data-ttu-id="ac15e-127">В поле "Кем проверено" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="ac15e-127">In the Validated by field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ac15e-128">Выберите пользователя, который будет проводить контроль.</span><span class="sxs-lookup"><span data-stu-id="ac15e-128">Select the user performing the inspection.</span></span>  
3. <span data-ttu-id="ac15e-129">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ac15e-129">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ac15e-130">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="ac15e-130">Click Select.</span></span>
5. <span data-ttu-id="ac15e-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ac15e-131">Click OK.</span></span>
6. <span data-ttu-id="ac15e-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ac15e-132">Close the page.</span></span>

