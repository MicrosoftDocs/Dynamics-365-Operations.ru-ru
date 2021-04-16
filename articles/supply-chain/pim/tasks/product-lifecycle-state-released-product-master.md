---
title: Назначение состояния жизненного цикла продукта шаблону выпущенного продукта
description: В этой процедуре показано, как назначить состояние жизненного цикла продукта выпущенному шаблону продукта и его вариантам.
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
ms.openlocfilehash: 66859c7f7f5be6eaadd9470fd9b792daa28ce33d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807896"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="718ae-103">Назначение состояния жизненного цикла продукта шаблону выпущенного продукта</span><span class="sxs-lookup"><span data-stu-id="718ae-103">Assign a product lifecycle state to a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="718ae-104">В этой процедуре показано, как назначить состояние жизненного цикла продукта выпущенному шаблону продукта и его вариантам.</span><span class="sxs-lookup"><span data-stu-id="718ae-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="718ae-105">Предварительное требование: сначала необходимо просмотреть проводник по задаче "Создание нового состояния жизненного цикла продукта", чтобы убедитесь, что создано хотя бы одно состояние жизненного цикла продукта, до просмотра этого проводника по задаче.</span><span class="sxs-lookup"><span data-stu-id="718ae-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="718ae-106">Поиск шаблона выпущенного продукта</span><span class="sxs-lookup"><span data-stu-id="718ae-106">Find a released product master</span></span>
1. <span data-ttu-id="718ae-107">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="718ae-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="718ae-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="718ae-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="718ae-109">Шаблон продукта имеет шаблон продукта подтипа продукта.</span><span class="sxs-lookup"><span data-stu-id="718ae-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="718ae-110">Обновление состояния жизненного цикла</span><span class="sxs-lookup"><span data-stu-id="718ae-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="718ae-111">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="718ae-111">Click Edit.</span></span>
2. <span data-ttu-id="718ae-112">В поле "Состояние жизненного цикла продукта" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="718ae-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="718ae-113">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="718ae-113">Click Save.</span></span>
4. <span data-ttu-id="718ae-114">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="718ae-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="718ae-115">Если выбран параметр "Да", все связанные выпущенные варианты продуктов, имеющие одинаковое исходное состояние, что и выпущенный шаблон продукта, также обновляются до нового состояния жизненного цикла продукта.</span><span class="sxs-lookup"><span data-stu-id="718ae-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="718ae-116">Если выбран параметр "Нет", все варианты сохраняют фактическое состояние.</span><span class="sxs-lookup"><span data-stu-id="718ae-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="718ae-117">Варианты, состояние жизненного цикла продукта которых отличается от выпущенного шаблона продукта, не обновляются.</span><span class="sxs-lookup"><span data-stu-id="718ae-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="718ae-118">Проверка состояния жизненного цикла вариантов</span><span class="sxs-lookup"><span data-stu-id="718ae-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="718ae-119">Щелкните "Варианты выпущенных продуктов".</span><span class="sxs-lookup"><span data-stu-id="718ae-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="718ae-120">Обратите внимание, что все варианты наследуют выбранное состояние жизненного цикла из выпущенного шаблона продукта.</span><span class="sxs-lookup"><span data-stu-id="718ae-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="718ae-121">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="718ae-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="718ae-122">В поле "Состояние жизненного цикла продукта" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="718ae-122">In the Product lifecycle state field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]