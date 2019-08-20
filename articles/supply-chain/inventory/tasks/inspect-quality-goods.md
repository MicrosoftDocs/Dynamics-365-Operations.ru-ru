---
title: Контроль качества товаров
description: В этом разделе объясняется, как обработать заказ для контроля качества.
author: perlynne
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10acb9aadfeb11ede1d66dd525ace7b70db3bd1c
ms.sourcegitcommit: fbaccf72df82e6b6927f0c9f0d35af0ca3ecbc2d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/02/2019
ms.locfileid: "1855694"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="47633-103">Контроль качества товаров</span><span class="sxs-lookup"><span data-stu-id="47633-103">Inspect the quality of goods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="47633-104">В этом разделе объясняется, как обработать заказ для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="47633-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="47633-105">Это руководство можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="47633-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="47633-106">Перед началом этой процедуры необходимо подтвердить заказ на покупку "000016" и разнести поступление продуктов.</span><span class="sxs-lookup"><span data-stu-id="47633-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="47633-107">При этом автоматически будет создан заказ контроля качества.</span><span class="sxs-lookup"><span data-stu-id="47633-107">This will automatically create a quality order.</span></span> <span data-ttu-id="47633-108">Контроль качества обычно производится сотрудником отдела контроля качества.</span><span class="sxs-lookup"><span data-stu-id="47633-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="47633-109">Выбор заказа контроля качества</span><span class="sxs-lookup"><span data-stu-id="47633-109">Select a quality order</span></span>
1. <span data-ttu-id="47633-110">В области перехода перейдите к **Модули > Управление запасами > Периодические задачи > Управление качеством > Заказы на контроль качества**.</span><span class="sxs-lookup"><span data-stu-id="47633-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="47633-111">Выберите заказ контроля качества, созданный перед началом этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="47633-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="47633-112">Запись результатов проверки</span><span class="sxs-lookup"><span data-stu-id="47633-112">Record test results</span></span>
1. <span data-ttu-id="47633-113">Выберите **Результаты**.</span><span class="sxs-lookup"><span data-stu-id="47633-113">Select **Results**.</span></span>
2. <span data-ttu-id="47633-114">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="47633-114">Select **Edit**.</span></span>
3. <span data-ttu-id="47633-115">В поле **Итоговое количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="47633-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="47633-116">В поле **Результат** выберите требуемую запись в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="47633-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="47633-117">В этом примере результат основан на заранее определенном итоге.</span><span class="sxs-lookup"><span data-stu-id="47633-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="47633-118">Обычно фиксируется более конкретный результат испытаний, например размер или другая аналитика.</span><span class="sxs-lookup"><span data-stu-id="47633-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="47633-119">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="47633-119">Select **Save**.</span></span>
6. <span data-ttu-id="47633-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="47633-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="47633-121">Проверить заказ контроля качества</span><span class="sxs-lookup"><span data-stu-id="47633-121">Validate the quality order</span></span>
1. <span data-ttu-id="47633-122">Выберите **Проверить**.</span><span class="sxs-lookup"><span data-stu-id="47633-122">Select **Validate**.</span></span>
2. <span data-ttu-id="47633-123">В поле **Кем проверено** выберите пользователя, выполняющего проверку, из раскрывающегося меню.</span><span class="sxs-lookup"><span data-stu-id="47633-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="47633-124">Щелкните **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="47633-124">Click **Select**.</span></span>
4. <span data-ttu-id="47633-125">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="47633-125">Select **OK**.</span></span>
5. <span data-ttu-id="47633-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="47633-126">Close the page.</span></span>

