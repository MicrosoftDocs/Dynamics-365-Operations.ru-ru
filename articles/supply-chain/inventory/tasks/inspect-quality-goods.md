---
title: Контроль качества товаров
description: В этом разделе объясняется, как обработать заказы для контроля качества.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956142"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="0a48f-103">Контроль качества товаров</span><span class="sxs-lookup"><span data-stu-id="0a48f-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a48f-104">В этом разделе объясняется, как обработать заказы для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="0a48f-104">This topic describes how to process quality orders.</span></span> <span data-ttu-id="0a48f-105">Контроль качества обычно выполняется сотрудником отдела контроля качества.</span><span class="sxs-lookup"><span data-stu-id="0a48f-105">Quality inspections are typically done by a quality clerk.</span></span>

<span data-ttu-id="0a48f-106">Если установлены стандартные демонстрационные данные, их можно использовать для выполнения процедур, описанных в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="0a48f-106">If the standard demo data is installed, you can use it to complete the procedures in this topic.</span></span> <span data-ttu-id="0a48f-107">Для использования демонстрационных данных выберите юридическое лицо *USMF*.</span><span class="sxs-lookup"><span data-stu-id="0a48f-107">To use the demo data, select the *USMF* legal entity before you begin.</span></span> <span data-ttu-id="0a48f-108">Затем необходимо подтвердить заказ на покупку *000016* и разнести поступление продуктов.</span><span class="sxs-lookup"><span data-stu-id="0a48f-108">You must then confirm purchase order *000016* and post a product receipt.</span></span> <span data-ttu-id="0a48f-109">Автоматически создается заказа на контроль качества.</span><span class="sxs-lookup"><span data-stu-id="0a48f-109">A quality order is automatically generated.</span></span>

## <a name="step-1-select-a-quality-order"></a><span data-ttu-id="0a48f-110">Шаг 1. Выбор заказа контроля качества</span><span class="sxs-lookup"><span data-stu-id="0a48f-110">Step 1: Select a quality order</span></span>

<span data-ttu-id="0a48f-111">Чтобы выбрать заказ контроля качества, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0a48f-111">To select a quality order, follow these steps.</span></span>

1. <span data-ttu-id="0a48f-112">Перейдите в раздел **Управление запасами \> Периодические задачи \> Управление качеством \> Заказы для контроля качества**.</span><span class="sxs-lookup"><span data-stu-id="0a48f-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="0a48f-113">Выберите заказ контроля качества, созданный перед началом этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="0a48f-113">Select the quality order that was generated before you started this procedure.</span></span>

## <a name="step-2-record-test-results"></a><span data-ttu-id="0a48f-114">Шаг 2. Запись результатов проверки</span><span class="sxs-lookup"><span data-stu-id="0a48f-114">Step 2: Record test results</span></span>

<span data-ttu-id="0a48f-115">Чтобы записать результаты проверки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0a48f-115">To record test results, follow these steps.</span></span>

1. <span data-ttu-id="0a48f-116">Выберите **Результаты**.</span><span class="sxs-lookup"><span data-stu-id="0a48f-116">Select **Results**.</span></span>
1. <span data-ttu-id="0a48f-117">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="0a48f-117">Select **Edit**.</span></span>
1. <span data-ttu-id="0a48f-118">В поле **Итоговое количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="0a48f-118">In the **Result quantity** field, enter a number.</span></span>
1. <span data-ttu-id="0a48f-119">В поле **Результаты** выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="0a48f-119">In the **Outcome** field, select the desired record.</span></span> <span data-ttu-id="0a48f-120">В этом примере результат основан на заранее определенном итоге.</span><span class="sxs-lookup"><span data-stu-id="0a48f-120">In this example, the result is based on a predefined outcome.</span></span> <span data-ttu-id="0a48f-121">Обычно фиксируется более конкретный результат проверки, например размер или другая аналитика.</span><span class="sxs-lookup"><span data-stu-id="0a48f-121">Usually, you will record a more specific test result, such as a size or other dimension.</span></span>
1. <span data-ttu-id="0a48f-122">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0a48f-122">Select **Save**.</span></span>
1. <span data-ttu-id="0a48f-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="0a48f-123">Close the page.</span></span>

## <a name="step-3-validate-the-quality-order"></a><span data-ttu-id="0a48f-124">Шаг 3. Проверить заказ контроля качества</span><span class="sxs-lookup"><span data-stu-id="0a48f-124">Step 3: Validate the quality order</span></span>

<span data-ttu-id="0a48f-125">Чтобы проверить заказ контроля качества, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0a48f-125">To validate the quality order, follow these steps.</span></span>

1. <span data-ttu-id="0a48f-126">Выберите **Проверить**.</span><span class="sxs-lookup"><span data-stu-id="0a48f-126">Select **Validate**.</span></span>
1. <span data-ttu-id="0a48f-127">В поле **Кем проверено** выберите пользователя, который выполняет проверку.</span><span class="sxs-lookup"><span data-stu-id="0a48f-127">In the **Validated by** field, select the user who is doing the inspection.</span></span>
1. <span data-ttu-id="0a48f-128">Выберите **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="0a48f-128">Select **Select**.</span></span>
1. <span data-ttu-id="0a48f-129">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0a48f-129">Select **OK**.</span></span>
1. <span data-ttu-id="0a48f-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="0a48f-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
