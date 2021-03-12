---
title: Сопоставление аналитики элемента затрат
description: Контроллер затрат может использовать эту процедуру для сопоставления аналитики элемента затрат аналитике элемента затрат в юридическом лице MXMF.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5570d7cf2a8139d7959cb708d306e8b91065ed1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990675"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="58492-103">Сопоставление аналитики элемента затрат</span><span class="sxs-lookup"><span data-stu-id="58492-103">Map a cost element dimension</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58492-104">Контроллер затрат может использовать эту процедуру для сопоставления аналитики элемента затрат аналитике элемента затрат в юридическом лице MXMF.</span><span class="sxs-lookup"><span data-stu-id="58492-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="58492-105">В этой записи используется компания с демонстрационными данными USP2.</span><span class="sxs-lookup"><span data-stu-id="58492-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="58492-106">Перейдите в раздел "Учет затрат" > "Аналитики" > "Аналитики элемента затрат".</span><span class="sxs-lookup"><span data-stu-id="58492-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="58492-107">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="58492-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="58492-108">В этом примере выберите "Элементы затрат".</span><span class="sxs-lookup"><span data-stu-id="58492-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="58492-109">Щелкните "Сопоставления аналитик".</span><span class="sxs-lookup"><span data-stu-id="58492-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="58492-110">Щелкните "Настроить сопоставления из этой аналитики".</span><span class="sxs-lookup"><span data-stu-id="58492-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="58492-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="58492-111">Click New.</span></span>
6. <span data-ttu-id="58492-112">В поле "В аналитику" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="58492-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="58492-113">В этом примере выберите "Элементы затрат MXMF".</span><span class="sxs-lookup"><span data-stu-id="58492-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="58492-114">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="58492-114">Click New.</span></span>
8. <span data-ttu-id="58492-115">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="58492-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="58492-116">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="58492-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="58492-117">В этом примере выберите элемент аналитики 606400, "Расходы на телефон и факс".</span><span class="sxs-lookup"><span data-stu-id="58492-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="58492-118">В поле "В элемент аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="58492-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="58492-119">В этом примере выберите элемент аналитики 6001004 "Telefono".</span><span class="sxs-lookup"><span data-stu-id="58492-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="58492-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="58492-120">Click Save.</span></span>

