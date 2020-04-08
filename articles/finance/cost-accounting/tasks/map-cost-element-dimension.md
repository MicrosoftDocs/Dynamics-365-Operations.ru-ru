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
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1a5805b7d86979389f1eb7496a63e3f4e7056c92
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3137876"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="8d7a0-103">Сопоставление аналитики элемента затрат</span><span class="sxs-lookup"><span data-stu-id="8d7a0-103">Map a cost element dimension</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8d7a0-104">Контроллер затрат может использовать эту процедуру для сопоставления аналитики элемента затрат аналитике элемента затрат в юридическом лице MXMF.</span><span class="sxs-lookup"><span data-stu-id="8d7a0-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="8d7a0-105">В этой записи используется компания с демонстрационными данными USP2.</span><span class="sxs-lookup"><span data-stu-id="8d7a0-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="8d7a0-106">Перейдите в раздел "Учет затрат" > "Аналитики" > "Аналитики элемента затрат".</span><span class="sxs-lookup"><span data-stu-id="8d7a0-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="8d7a0-107">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8d7a0-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8d7a0-108">В этом примере выберите "Элементы затрат".</span><span class="sxs-lookup"><span data-stu-id="8d7a0-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="8d7a0-109">Щелкните "Сопоставления аналитик".</span><span class="sxs-lookup"><span data-stu-id="8d7a0-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="8d7a0-110">Щелкните "Настроить сопоставления из этой аналитики".</span><span class="sxs-lookup"><span data-stu-id="8d7a0-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="8d7a0-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8d7a0-111">Click New.</span></span>
6. <span data-ttu-id="8d7a0-112">В поле "В аналитику" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8d7a0-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="8d7a0-113">В этом примере выберите "Элементы затрат MXMF".</span><span class="sxs-lookup"><span data-stu-id="8d7a0-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="8d7a0-114">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8d7a0-114">Click New.</span></span>
8. <span data-ttu-id="8d7a0-115">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="8d7a0-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="8d7a0-116">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8d7a0-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="8d7a0-117">В этом примере выберите элемент аналитики 606400, "Расходы на телефон и факс".</span><span class="sxs-lookup"><span data-stu-id="8d7a0-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="8d7a0-118">В поле "В элемент аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8d7a0-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="8d7a0-119">В этом примере выберите элемент аналитики 6001004 "Telefono".</span><span class="sxs-lookup"><span data-stu-id="8d7a0-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="8d7a0-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8d7a0-120">Click Save.</span></span>

