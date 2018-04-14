--- 
title: "Сопоставление аналитики элемента затрат"
description: "Контроллер затрат может использовать эту процедуру для сопоставления аналитики элемента затрат аналитике элемента затрат в юридическом лице MXMF."
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 52497aa2c67e852b366a39058d4cbf7597f1bd4a
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="4268d-103">Сопоставление аналитики элемента затрат</span><span class="sxs-lookup"><span data-stu-id="4268d-103">Map a cost element dimension</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4268d-104">Контроллер затрат может использовать эту процедуру для сопоставления аналитики элемента затрат аналитике элемента затрат в юридическом лице MXMF.</span><span class="sxs-lookup"><span data-stu-id="4268d-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="4268d-105">В этой записи используется компания с демонстрационными данными USP2.</span><span class="sxs-lookup"><span data-stu-id="4268d-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="4268d-106">Перейдите в раздел "Учет затрат" > "Аналитики" > "Аналитики элемента затрат".</span><span class="sxs-lookup"><span data-stu-id="4268d-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="4268d-107">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4268d-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4268d-108">В этом примере выберите "Элементы затрат".</span><span class="sxs-lookup"><span data-stu-id="4268d-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="4268d-109">Щелкните "Сопоставления аналитик".</span><span class="sxs-lookup"><span data-stu-id="4268d-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="4268d-110">Щелкните "Настроить сопоставления из этой аналитики".</span><span class="sxs-lookup"><span data-stu-id="4268d-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="4268d-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4268d-111">Click New.</span></span>
6. <span data-ttu-id="4268d-112">В поле "В аналитику" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4268d-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="4268d-113">В этом примере выберите "Элементы затрат MXMF".</span><span class="sxs-lookup"><span data-stu-id="4268d-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="4268d-114">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4268d-114">Click New.</span></span>
8. <span data-ttu-id="4268d-115">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4268d-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="4268d-116">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4268d-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4268d-117">В этом примере выберите элемент аналитики 606400, "Расходы на телефон и факс".</span><span class="sxs-lookup"><span data-stu-id="4268d-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="4268d-118">В поле "В элемент аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4268d-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4268d-119">В этом примере выберите элемент аналитики 6001004 "Telefono".</span><span class="sxs-lookup"><span data-stu-id="4268d-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="4268d-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4268d-120">Click Save.</span></span>


