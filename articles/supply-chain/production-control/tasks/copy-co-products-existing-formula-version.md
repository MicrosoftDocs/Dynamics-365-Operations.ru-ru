---
title: Копирование побочных продуктов из существующей версии формулы
description: В этой процедуре показано, как скопировать сопутствующие продукты из существующей версии формулы в другую версию формулы для выпущенного продукта.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 626c0fc8a60eeb84060d7279833de583d55a95a2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838759"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="1faa4-103">Копирование побочных продуктов из существующей версии формулы</span><span class="sxs-lookup"><span data-stu-id="1faa4-103">Copy co-products from an existing formula version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1faa4-104">В этой процедуре показано, как скопировать сопутствующие продукты из существующей версии формулы в другую версию формулы для выпущенного продукта.</span><span class="sxs-lookup"><span data-stu-id="1faa4-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="1faa4-105">Обязательным условием является наличие по крайней мере одной версии формулы, связанной с сопутствующими продуктами.</span><span class="sxs-lookup"><span data-stu-id="1faa4-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="1faa4-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USP2.</span><span class="sxs-lookup"><span data-stu-id="1faa4-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="1faa4-107">Поиск выпущенного продукта</span><span class="sxs-lookup"><span data-stu-id="1faa4-107">Find a released product</span></span>
1. <span data-ttu-id="1faa4-108">Перейдите в раздел "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="1faa4-108">Go to Released products.</span></span>
2. <span data-ttu-id="1faa4-109">Щелкните "Показать фильтры".</span><span class="sxs-lookup"><span data-stu-id="1faa4-109">Click Show filters.</span></span>
    * <span data-ttu-id="1faa4-110">Вы собираетесь добавить поле "Тип производства" в диалоговое окно фильтра.</span><span class="sxs-lookup"><span data-stu-id="1faa4-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="1faa4-111">Нажмите кнопку "Добавить фильтр" для добавления поля "Тип производства".</span><span class="sxs-lookup"><span data-stu-id="1faa4-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="1faa4-112">На следующем шаге необходимо вручную ввести формулу в поле "Тип производства" перед нажатием кнопки "Применить".</span><span class="sxs-lookup"><span data-stu-id="1faa4-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="1faa4-113">В результате фильтр будет задан для списка выпущенных продуктов.</span><span class="sxs-lookup"><span data-stu-id="1faa4-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="1faa4-114">Вручную введите формулу в поле "Тип производства".</span><span class="sxs-lookup"><span data-stu-id="1faa4-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="1faa4-115">Нажмите кнопку Применить.</span><span class="sxs-lookup"><span data-stu-id="1faa4-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="1faa4-116">Выбор выпущенного продукта</span><span class="sxs-lookup"><span data-stu-id="1faa4-116">Select a released product</span></span>
1. <span data-ttu-id="1faa4-117">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="1faa4-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="1faa4-118">Щелкните "Версии формулы".</span><span class="sxs-lookup"><span data-stu-id="1faa4-118">Click Formula versions.</span></span>
    * <span data-ttu-id="1faa4-119">На панели операций технического отдела щелкните "Версии формулы".</span><span class="sxs-lookup"><span data-stu-id="1faa4-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="1faa4-120">Копирование сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="1faa4-120">Copy co-products</span></span>
1. <span data-ttu-id="1faa4-121">В области действий щелкните "Версия формулы".</span><span class="sxs-lookup"><span data-stu-id="1faa4-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="1faa4-122">Щелкните Побочные продукты.</span><span class="sxs-lookup"><span data-stu-id="1faa4-122">Click Co-products.</span></span>
3. <span data-ttu-id="1faa4-123">Щелкните Копировать.</span><span class="sxs-lookup"><span data-stu-id="1faa4-123">Click Copy.</span></span>
4. <span data-ttu-id="1faa4-124">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1faa4-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="1faa4-125">В поле "Версия формулы" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1faa4-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="1faa4-126">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1faa4-126">Click OK.</span></span>
7. <span data-ttu-id="1faa4-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1faa4-127">Close the page.</span></span>

