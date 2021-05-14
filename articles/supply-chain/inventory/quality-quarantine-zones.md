---
title: Карантинные зоны для несоответствий
description: В этой теме описывается, как создавать и использовать карантинные зоны для несоответствий.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93ca74ec4586fffa3b9156aadab887629283b98a
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956808"
---
# <a name="quarantine-zones-for-nonconformances"></a><span data-ttu-id="967fc-103">Карантинные зоны для несоответствий</span><span class="sxs-lookup"><span data-stu-id="967fc-103">Quarantine zones for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="967fc-104">В этой теме описывается, как создавать и использовать карантинные зоны для несоответствий.</span><span class="sxs-lookup"><span data-stu-id="967fc-104">This topic describes how to create and use quarantine zones for nonconformances.</span></span>

<span data-ttu-id="967fc-105">На странице **карантинные зоны** определите зоны, которые могут быть назначены для несоответствий.</span><span class="sxs-lookup"><span data-stu-id="967fc-105">You use the **Quarantine zones** page to define zones that can be assigned to nonconformances.</span></span> <span data-ttu-id="967fc-106">При создании несоответствия можно настроить поля **Карантинная зона** и **Тип карантина** на вкладке **Общее** на странице **Несоответствия**.</span><span class="sxs-lookup"><span data-stu-id="967fc-106">When you create a nonconformance, you can set the **Quarantine zone** and **Quarantine type** fields on the **General** tab of the **Non conformances** page.</span></span> <span data-ttu-id="967fc-107">Поле зона **Карантинная зона** обычно указывает область или местоположение, в котором находится номенклатура.</span><span class="sxs-lookup"><span data-stu-id="967fc-107">The **Quarantine zone** field typically indicates the area or location where the item is located.</span></span> <span data-ttu-id="967fc-108">Поле **Тип карантина** определяет номенклатуру как *Ограниченное использование* или *Непригодно для использования*.</span><span class="sxs-lookup"><span data-stu-id="967fc-108">The **Quarantine type** field defines the item as either *Restricted usage* or *Unusable*.</span></span>

<span data-ttu-id="967fc-109">При печати отчета о несоответствии или отчета исправлений для несоответствия можно просмотреть карантинную зону, в которой находится номенклатура.</span><span class="sxs-lookup"><span data-stu-id="967fc-109">When you print a nonconformance or corrections report for a nonconformance, you can view the quarantine zone where the item is located.</span></span>

<span data-ttu-id="967fc-110">Можно также распечатать тег несоответствия для несоответствия.</span><span class="sxs-lookup"><span data-stu-id="967fc-110">You can also print a nonconformance tag for a nonconformance.</span></span> <span data-ttu-id="967fc-111">Этот отчет содержит назначенную карантинную зону вместе со сведениями об использовании для ведения обработки бракованного материала.</span><span class="sxs-lookup"><span data-stu-id="967fc-111">This report shows the assigned quarantine zone and information about usage to provide guidance about how defective material should be handled.</span></span> <span data-ttu-id="967fc-112">Карантинные зоны могут соответствовать местоположению запасов или операционным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="967fc-112">The quarantine zones might correspond to inventory locations or operations resources.</span></span>

## <a name="examples-of-quarantine-zones"></a><span data-ttu-id="967fc-113">Примеры карантинных зон</span><span class="sxs-lookup"><span data-stu-id="967fc-113">Examples of quarantine zones</span></span>

### <a name="example-1"></a><span data-ttu-id="967fc-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="967fc-114">Example 1</span></span>

<span data-ttu-id="967fc-115">Вы работаете в компании-производителе электроники, которая производит и распространяет телевизоры, динамики и мультимедийные проигрыватели.</span><span class="sxs-lookup"><span data-stu-id="967fc-115">You work at an electronics manufacturing company that produces and distributes televisions, speakers, and media players.</span></span> <span data-ttu-id="967fc-116">В этом случае можно настроить карантинную зону для представления каждого типа продукта.</span><span class="sxs-lookup"><span data-stu-id="967fc-116">In this case, you can configure a quarantine zone to represent each type of product.</span></span>

### <a name="example-2"></a><span data-ttu-id="967fc-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="967fc-117">Example 2</span></span>

<span data-ttu-id="967fc-118">Для хранения несоответствующих номенклатур используются три ячейки и две стойки.</span><span class="sxs-lookup"><span data-stu-id="967fc-118">Three bins and two racks are used to store items that are nonconforming.</span></span> <span data-ttu-id="967fc-119">В этом случае можно настроить пять карантинных зон, по одной для каждой ячейки и для каждой стойки.</span><span class="sxs-lookup"><span data-stu-id="967fc-119">In this case, you can configure five quarantine zones, one for each bin and each rack.</span></span>

## <a name="create-a-quarantine-zone"></a><span data-ttu-id="967fc-120">Создание карантинной зоны</span><span class="sxs-lookup"><span data-stu-id="967fc-120">Create a quarantine zone</span></span>

1. <span data-ttu-id="967fc-121">Перейдите в раздел **Управление запасами \> Настройка \> Управление качеством \> Карантинные зоны**.</span><span class="sxs-lookup"><span data-stu-id="967fc-121">Go to **Inventory management \> Setup \> Quality management \> Quarantine zones**.</span></span>
1. <span data-ttu-id="967fc-122">На панели операций выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="967fc-122">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="967fc-123">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="967fc-123">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="967fc-124">**Карантинная зона** — введите уникальный код или имя карантинной зоны.</span><span class="sxs-lookup"><span data-stu-id="967fc-124">**Quarantine zone** – Enter a unique ID or name for the quarantine zone.</span></span>
    - <span data-ttu-id="967fc-125">**Описание** — введите подробное описание карантинной зоны.</span><span class="sxs-lookup"><span data-stu-id="967fc-125">**Description** – Enter a detailed description of the quarantine zone.</span></span>

1. <span data-ttu-id="967fc-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="967fc-126">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="967fc-127">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="967fc-127">Additional resources</span></span>

- [<span data-ttu-id="967fc-128">Обзор управления качеством</span><span class="sxs-lookup"><span data-stu-id="967fc-128">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="967fc-129">Включение управления качеством и несоответствием</span><span class="sxs-lookup"><span data-stu-id="967fc-129">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="967fc-130">Работники, ответственные за утверждение несоответствий</span><span class="sxs-lookup"><span data-stu-id="967fc-130">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="967fc-131">Типы проблем для несоответствий</span><span class="sxs-lookup"><span data-stu-id="967fc-131">Problem types for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="967fc-132">Типы диагностики для несоответствий</span><span class="sxs-lookup"><span data-stu-id="967fc-132">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="967fc-133">Расходы по контролю качества для несоответствий</span><span class="sxs-lookup"><span data-stu-id="967fc-133">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="967fc-134">Операции для несоответствий</span><span class="sxs-lookup"><span data-stu-id="967fc-134">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="967fc-135">Управление качеством для складских процессов</span><span class="sxs-lookup"><span data-stu-id="967fc-135">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
