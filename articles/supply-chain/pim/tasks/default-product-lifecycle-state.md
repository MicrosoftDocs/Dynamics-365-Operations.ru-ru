---
title: Создание состояния жизненного цикла продукта по умолчанию
description: В этой процедуре показано, как создать состояние жизненного цикла продукта по умолчанию, а также связать состояние по умолчанию с выпущенными продуктами.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e7e637157ee06a3d07a1a9c5da71295eb75b424
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564186"
---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="8a137-103">Создание состояния жизненного цикла продукта по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8a137-103">Create a default product lifecycle state</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a137-104">В этой процедуре показано, как создать состояние жизненного цикла продукта по умолчанию, а также связать состояние по умолчанию с выпущенными продуктами.</span><span class="sxs-lookup"><span data-stu-id="8a137-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="8a137-105">Создание состояния жизненного цикла по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8a137-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="8a137-106">Перейдите в раздел "Управление сведениями о продукте" > "Настройка" > "Состояние жизненного цикла продукта".</span><span class="sxs-lookup"><span data-stu-id="8a137-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="8a137-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8a137-107">Click New.</span></span>
3. <span data-ttu-id="8a137-108">В поле "Состояние" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8a137-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="8a137-109">Выберите "Да" в поле "По умолчанию при выпуске юридическому лицу".</span><span class="sxs-lookup"><span data-stu-id="8a137-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="8a137-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8a137-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="8a137-111">Выберите "Нет" в поле "Активен для планирования".</span><span class="sxs-lookup"><span data-stu-id="8a137-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="8a137-112">Если новый выпущенный продукт не следует включать в сводное планирование, выберите "Нет".</span><span class="sxs-lookup"><span data-stu-id="8a137-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="8a137-113">Если он должен быть включен в сводное планирование, оставьте для элемента управления значение по умолчанию "Да".</span><span class="sxs-lookup"><span data-stu-id="8a137-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="8a137-114">Создание нового выпущенного продукта</span><span class="sxs-lookup"><span data-stu-id="8a137-114">Create a new released product</span></span>
1. <span data-ttu-id="8a137-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8a137-115">Close the page.</span></span>
2. <span data-ttu-id="8a137-116">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="8a137-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="8a137-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8a137-117">Click New.</span></span>
4. <span data-ttu-id="8a137-118">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8a137-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="8a137-119">В поле "Имя продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8a137-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="8a137-120">В поле "Краткое наименование" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8a137-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="8a137-121">В поле "Группа номенклатурных моделей" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8a137-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="8a137-122">В поле "Номенклатурная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8a137-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="8a137-123">В поле "Группа аналитик хранения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8a137-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="8a137-124">В поле "Группа аналитик отслеживания" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8a137-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="8a137-125">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8a137-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="8a137-126">Состояние жизненного цикла продукта по умолчанию является глобальным определением.</span><span class="sxs-lookup"><span data-stu-id="8a137-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="8a137-127">Изменение состояния продукта на "Активно"</span><span class="sxs-lookup"><span data-stu-id="8a137-127">Change the product to an active state</span></span>
1. <span data-ttu-id="8a137-128">В поле "Состояние жизненного цикла продукта" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8a137-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="8a137-129">Предположим, что вы задали активное состояние, теперь вы можете выбрать активное состояние, чтобы разрешить использовать продукт в сводном планировании и расчете уровня спецификации.</span><span class="sxs-lookup"><span data-stu-id="8a137-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="8a137-130">Очевидно, что имеет смысл указать все сведения о продукте, необходимые для согласованного планирования.</span><span class="sxs-lookup"><span data-stu-id="8a137-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  

