---
title: Меченная инвентаризация запасов
description: Эта тема предоставляет информацию о меченной инвентаризации, которые используются для сравнения фактического содержимого склада с запасами в наличии.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efb555cdfbcf3fd0c10ec0e2abcdbe7f4a90d82d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435794"
---
# <a name="inventory-tag-counting"></a><span data-ttu-id="ad46f-103">Меченная инвентаризация запасов</span><span class="sxs-lookup"><span data-stu-id="ad46f-103">Inventory tag counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad46f-104">Эта тема предоставляет информацию о меченной инвентаризации, которые используются для сравнения фактического содержимого склада с запасами в наличии.</span><span class="sxs-lookup"><span data-stu-id="ad46f-104">This topic provides information about tag counting, which you use to compare the actual contents of a warehouse with the on-hand inventory.</span></span>

<span data-ttu-id="ad46f-105">Создавая строки на странице **Учет маркеров**, вы помещаете номер маркера в каждую складируемую номенклатуру, например номер от 1 до 500.</span><span class="sxs-lookup"><span data-stu-id="ad46f-105">By creating lines on the **Tag counting** page, you place a tag number on each inventory item, such as a number from 1 to 500.</span></span> <span data-ttu-id="ad46f-106">Во время инвентаризации вы вводите код номенклатуры и количество в соответствующий маркер.</span><span class="sxs-lookup"><span data-stu-id="ad46f-106">During the count, you enter the item number and the quantity on a corresponding tag.</span></span> <span data-ttu-id="ad46f-107">Затем этот маркер можно использовать как основу для ввода данных в журнале учета маркеров.</span><span class="sxs-lookup"><span data-stu-id="ad46f-107">This tag can then be used as the basis for input in the tag counting journal.</span></span> <span data-ttu-id="ad46f-108">После разноски журнала учета маркеров создается новый журнал учета на странице **Инвентаризация**.</span><span class="sxs-lookup"><span data-stu-id="ad46f-108">After you post the tag counting journal, a new counting journal is created on the **Counting** page.</span></span> <span data-ttu-id="ad46f-109">Новый журнал основан на строках созданного журнала учета маркеров.</span><span class="sxs-lookup"><span data-stu-id="ad46f-109">The new journal is based on the tag counting journal lines that you created.</span></span> <span data-ttu-id="ad46f-110">Чтобы учесть маркеры номенклатур по определенной складской аналитике, выберите аналитику на странице **Отобразить аналитики**, которая открывается при создании журнала учета маркеров.</span><span class="sxs-lookup"><span data-stu-id="ad46f-110">To tag-count items by a specific inventory dimension, select the dimension on the **Display dimension** page that is displayed when you create the tag counting journal.</span></span> <span data-ttu-id="ad46f-111">Например, чтобы учесть номенклатуры на определенном складе, установите флажок **Склад**.</span><span class="sxs-lookup"><span data-stu-id="ad46f-111">For example, to count items in a specific warehouse, select the **Warehouse** check box.</span></span> <span data-ttu-id="ad46f-112">Если выбран ползунок **Блокир. номенкл. при инвентаризации** на странице **Параметры модуля "Управление запасами и складами"**, номенклатуры невозможно физически обновить во время инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="ad46f-112">If the **Lock items during count** slider on the **Inventory and warehouse management parameters** page is selected, items can't be physically updated during counting.</span></span> <span data-ttu-id="ad46f-113">Однако номенклатуры в журналах учета маркеров не блокируются во время инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="ad46f-113">However, items in tag counting journals aren't locked during counting.</span></span> <span data-ttu-id="ad46f-114">Складские проводки не создаются, пока строки учета маркеров не будут разнесены и перенесены в журнал учета.</span><span class="sxs-lookup"><span data-stu-id="ad46f-114">Inventory transactions aren't created until the tag counting lines are posted and transferred to a counting journal.</span></span> <span data-ttu-id="ad46f-115">Если маркеры вводятся случайным образом и требуется идентифицировать отсутствующие маркеры, щелкните заголовок столбца **Маркер**, чтобы отсортировать строки по маркеру.</span><span class="sxs-lookup"><span data-stu-id="ad46f-115">If tags are entered randomly, and you want to identify missing tags, click the **Tag** column header to sort the lines by tag.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad46f-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ad46f-116">Additional resources</span></span>

[<span data-ttu-id="ad46f-117">Цикличный подсчет</span><span class="sxs-lookup"><span data-stu-id="ad46f-117">Cycle counting</span></span>](../warehousing/cycle-counting.md)
