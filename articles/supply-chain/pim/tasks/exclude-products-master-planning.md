--- 
title: "Создание состояния жизненного цикла продукта для исключения продуктов из сводного планирования"
description: "В этой процедуре показано, как создать новое состояние жизненного цикла продукта, которое исключает продукты из сводного планирования и расчета уровня спецификации."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 57b84e62b259e5dcbf68ee447b9627443d932476
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="6edce-103">Создание состояния жизненного цикла продукта для исключения продуктов из сводного планирования</span><span class="sxs-lookup"><span data-stu-id="6edce-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6edce-104">В этой процедуре показано, как создать новое состояние жизненного цикла продукта, которое исключает продукты из сводного планирования и расчета уровня спецификации.</span><span class="sxs-lookup"><span data-stu-id="6edce-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="6edce-105">Создание устаревшего состояния</span><span class="sxs-lookup"><span data-stu-id="6edce-105">Create an obsolete state</span></span>
1. <span data-ttu-id="6edce-106">Перейдите в раздел "Управление сведениями о продукте" > "Настройка" > "Состояние жизненного цикла продукта".</span><span class="sxs-lookup"><span data-stu-id="6edce-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="6edce-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6edce-107">Click New.</span></span>
3. <span data-ttu-id="6edce-108">В поле "Состояние" введите значение.</span><span class="sxs-lookup"><span data-stu-id="6edce-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="6edce-109">Выберите "Нет" в поле "Активен для планирования".</span><span class="sxs-lookup"><span data-stu-id="6edce-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="6edce-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="6edce-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="6edce-111">Связь устаревшего состояния с выпущенным продуктом</span><span class="sxs-lookup"><span data-stu-id="6edce-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="6edce-112">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6edce-112">Close the page.</span></span>
2. <span data-ttu-id="6edce-113">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="6edce-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="6edce-114">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="6edce-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6edce-115">Например, отфильтруйте поле "Имя поиска" по значению "M00".</span><span class="sxs-lookup"><span data-stu-id="6edce-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="6edce-116">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="6edce-116">Click Edit.</span></span>
5. <span data-ttu-id="6edce-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="6edce-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="6edce-118">В поле "Состояние жизненного цикла продукта" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6edce-118">In the Product lifecycle state field, enter or select a value.</span></span>


