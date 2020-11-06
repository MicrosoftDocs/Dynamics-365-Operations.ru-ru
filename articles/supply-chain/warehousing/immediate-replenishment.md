---
title: Немедленное пополнение
description: В этом разделе описывается, как использовать немедленное пополнение для пополнения запасов, когда директива местонахождения не смогла распределить запасы.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c69a9c9fd595280ba4f05a11409a3e672e4b1691
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017516"
---
# <a name="immediate-replenishment"></a><span data-ttu-id="2400f-103">Немедленное пополнение</span><span class="sxs-lookup"><span data-stu-id="2400f-103">Immediate replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2400f-104">Немедленное пополнение позволяет пополнять запасы сразу после того, как строка директивы местонахождения не смогла распределить запасы.</span><span class="sxs-lookup"><span data-stu-id="2400f-104">Immediate replenishment lets you replenish inventory immediately after a location directive line fails to allocate inventory.</span></span> <span data-ttu-id="2400f-105">Пополнение основано на одной строке в настройках директивы местоположения.</span><span class="sxs-lookup"><span data-stu-id="2400f-105">The replenishment is based on a single line in the setup of the location directive.</span></span> <span data-ttu-id="2400f-106">Если запасы отсутствуют в наличии в единицах измерения, которые указаны в этой строке, пополнение этой единицы измерения выполняется немедленно.</span><span class="sxs-lookup"><span data-stu-id="2400f-106">If inventory isn't on hand in the unit of measure that is specified by that line, replenishment of that unit of measure occurs immediately.</span></span>

<span data-ttu-id="2400f-107">Немедленное пополнение обеспечивает альтернативный способ, в котором распределение запасов основывается на дополнительных строках в директиве местоположения, и где спрос суммируется в конце распределения и пополняется в единицах измерения, указанный в последней строке в директиве местоположения.</span><span class="sxs-lookup"><span data-stu-id="2400f-107">Immediate replenishment provides an alternative to the method where the allocation of inventory is based on more lines in the location directive, and where the demand is summed at the end of the allocation and replenished in the unit of measure that is specified by the last line in the location directive.</span></span>

<span data-ttu-id="2400f-108">Преимущества использования немедленного пополнения заключаются в том, что пополнение может быть ограничено определенными единицами измерения, а количества можно направить в определенные местоположения.</span><span class="sxs-lookup"><span data-stu-id="2400f-108">The benefits of using immediate replenishment are that replenishment can be limited by specific units and the quantity can be directed to specific locations.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="2400f-109">Бизнес-сценарий</span><span class="sxs-lookup"><span data-stu-id="2400f-109">Business scenario</span></span>

<span data-ttu-id="2400f-110">Например, у вас есть склад, имеющий отдельные области комплектации для единиц измерения "коробка" и "штуки".</span><span class="sxs-lookup"><span data-stu-id="2400f-110">For example, you have a warehouse that has separate picking areas for the "box" and "each" units of measure.</span></span> <span data-ttu-id="2400f-111">Вы хотите оптимизировать процесс комплектации, комплектуя как можно больше коробок, а затем комплектуя все оставшееся количество, которое меньше коробки, в области "штуки".</span><span class="sxs-lookup"><span data-stu-id="2400f-111">You want to optimize the picking process by picking as many boxes as possible and then picking any remaining quantity that is less than a box from the "each" area.</span></span>

<span data-ttu-id="2400f-112">В этом случае можно использовать немедленное пополнение.</span><span class="sxs-lookup"><span data-stu-id="2400f-112">In this case, you can use immediate replenishment.</span></span> <span data-ttu-id="2400f-113">В директиве местоположения можно настроить немедленное пополнение для коробок, чтобы пополнение спроса использовалось сразу же, как возникает нехватка коробок, которые можно скомплектовать для запрошенного количества.</span><span class="sxs-lookup"><span data-stu-id="2400f-113">In the location directive, you can set up immediate replenishment for boxes so that demand replenishment is used as soon as there is a shortage of boxes that can be picked for the demand quantity.</span></span> <span data-ttu-id="2400f-114">Таким образом вы оптимизируете процесс комплектации, чтобы комплектация включала максимально возможное число коробок.</span><span class="sxs-lookup"><span data-stu-id="2400f-114">In this way, you optimize the picking process so that picking includes as many boxes as possible.</span></span> <span data-ttu-id="2400f-115">Немедленное пополнения создает пополнение коробок, и спрос не передается далее, чтобы эти количества комплектовались в единицах измерения "штука".</span><span class="sxs-lookup"><span data-stu-id="2400f-115">Immediate replenishment will generate replenishment of the boxes, and the demand won't be passed on so that the quantities are picked in the "each" unit of measure.</span></span> <span data-ttu-id="2400f-116">Другими словами, только количества, которая предназначены для комплектации в единицах измерения "штуки" (то есть, количества, которые меньше коробки) будет комплектоваться в области "штуки".</span><span class="sxs-lookup"><span data-stu-id="2400f-116">In other words, only the quantities that are supposed to be picked in the "each" unit of measure (that is, quantities that are less than a box) will be picked from the "each" area.</span></span> <span data-ttu-id="2400f-117">При возникновении недостатка в области "коробки" можно скомплектовать как можно больше коробок из общего требования.</span><span class="sxs-lookup"><span data-stu-id="2400f-117">If a shortage occurs in the "box" area, you can pick as many boxes as possible out of the total demand.</span></span> <span data-ttu-id="2400f-118">Затем оставшиеся количества будет комплектоваться из области "штуки".</span><span class="sxs-lookup"><span data-stu-id="2400f-118">The remaining quantities will then be picked from the "each" area.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="2400f-119">Где это применяется</span><span class="sxs-lookup"><span data-stu-id="2400f-119">Where it applies</span></span>

<span data-ttu-id="2400f-120">Немедленное пополнение используется во время выполнения волны, если не удается выполнить распределение для строки директивы местонахождения, у которой задан шаблон пополнения.</span><span class="sxs-lookup"><span data-stu-id="2400f-120">Immediate replenishment is used during wave execution if allocation fails for a location directive line that a replenishment template is set for.</span></span>

## <a name="set-up-immediate-replenishment"></a><span data-ttu-id="2400f-121">Настройка немедленного пополнения</span><span class="sxs-lookup"><span data-stu-id="2400f-121">Set up immediate replenishment</span></span>

- <span data-ttu-id="2400f-122">Выберите **Управление складом** \> **Настройка** \> **Директивы для мест хранения** , затем на вкладке **Строки** в списке **Шаблон немедленного пополнения** выберите шаблон пополнения для спроса волны.</span><span class="sxs-lookup"><span data-stu-id="2400f-122">Go to **Warehouse management** \> **Setup** \> **Location directives** , and then, on the **Lines** tab, in the **Immediate replenishment template** list, select a replenishment template for wave demand.</span></span>

<span data-ttu-id="2400f-123">Шаблон пополнения применяется, если строка директивы места хранения не смогла распределить специальную единицу измерения.</span><span class="sxs-lookup"><span data-stu-id="2400f-123">The replenishment template is applied if the location directive line fails to allocate a dedicated unit of measure.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="2400f-124">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="2400f-124">Troubleshooting</span></span>

<span data-ttu-id="2400f-125">Если немедленное пополнение выбрано для строки директивы места хранения, но работа пополнения не создается при использовании шаблонов пополнения спроса для этой строки директивы места хранения, необходимо изучить две основные причины:</span><span class="sxs-lookup"><span data-stu-id="2400f-125">If immediate replenishment is selected for a location directive line, but no replenishment work is generated when you use demand replenishment templates for that location directive line, two main causes must be investigated:</span></span>

- <span data-ttu-id="2400f-126">Убедитесь в том, что шаблон пополнения спроса, который применяется, настроен для использования правильных шаблонов места хранения и шаблонов работы типа **Пополнение**.</span><span class="sxs-lookup"><span data-stu-id="2400f-126">Make sure that the demand replenishment template that is applied is set up to use the correct location templates and work templates of the **Replenishment** type.</span></span>
- <span data-ttu-id="2400f-127">Убедитесь, что имеется достаточное количество запасов в наличии в местах хранения, в которых шаблон пополнения ищет запасы в наличии для пополнения.</span><span class="sxs-lookup"><span data-stu-id="2400f-127">Make sure that there is enough on-hand inventory at the locations where the demand replenishment template searches for on-hand inventory for replenishment.</span></span>
