---
title: Копирование побочных продуктов из существующей версии формулы
description: В этой процедуре показано, как скопировать сопутствующие продукты из существующей версии формулы в другую версию формулы для выпущенного продукта.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79b70ccbdac2061baf3896ecbd9449da3c38842a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435766"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="9f5ea-103">Копирование побочных продуктов из существующей версии формулы</span><span class="sxs-lookup"><span data-stu-id="9f5ea-103">Copy co-products from an existing formula version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9f5ea-104">В этой процедуре показано, как скопировать сопутствующие продукты из существующей версии формулы в другую версию формулы для выпущенного продукта.</span><span class="sxs-lookup"><span data-stu-id="9f5ea-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="9f5ea-105">Обязательным условием является наличие по крайней мере одной версии формулы, связанной с сопутствующими продуктами.</span><span class="sxs-lookup"><span data-stu-id="9f5ea-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="9f5ea-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USP2.</span><span class="sxs-lookup"><span data-stu-id="9f5ea-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="9f5ea-107">Поиск выпущенного продукта</span><span class="sxs-lookup"><span data-stu-id="9f5ea-107">Find a released product</span></span>
1. <span data-ttu-id="9f5ea-108">Перейдите в раздел "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="9f5ea-108">Go to Released products.</span></span>
2. <span data-ttu-id="9f5ea-109">Щелкните "Показать фильтры".</span><span class="sxs-lookup"><span data-stu-id="9f5ea-109">Click Show filters.</span></span>
    * <span data-ttu-id="9f5ea-110">Вы собираетесь добавить поле "Тип производства" в диалоговое окно фильтра.</span><span class="sxs-lookup"><span data-stu-id="9f5ea-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="9f5ea-111">Нажмите кнопку "Добавить фильтр" для добавления поля "Тип производства".</span><span class="sxs-lookup"><span data-stu-id="9f5ea-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="9f5ea-112">На следующем шаге необходимо вручную ввести формулу в поле "Тип производства" перед нажатием кнопки "Применить".</span><span class="sxs-lookup"><span data-stu-id="9f5ea-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="9f5ea-113">В результате фильтр будет задан для списка выпущенных продуктов.</span><span class="sxs-lookup"><span data-stu-id="9f5ea-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="9f5ea-114">Вручную введите формулу в поле "Тип производства".</span><span class="sxs-lookup"><span data-stu-id="9f5ea-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="9f5ea-115">Нажмите кнопку Применить.</span><span class="sxs-lookup"><span data-stu-id="9f5ea-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="9f5ea-116">Выбор выпущенного продукта</span><span class="sxs-lookup"><span data-stu-id="9f5ea-116">Select a released product</span></span>
1. <span data-ttu-id="9f5ea-117">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="9f5ea-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="9f5ea-118">Щелкните "Версии формулы".</span><span class="sxs-lookup"><span data-stu-id="9f5ea-118">Click Formula versions.</span></span>
    * <span data-ttu-id="9f5ea-119">На панели операций технического отдела щелкните "Версии формулы".</span><span class="sxs-lookup"><span data-stu-id="9f5ea-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="9f5ea-120">Копирование сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="9f5ea-120">Copy co-products</span></span>
1. <span data-ttu-id="9f5ea-121">В области действий щелкните "Версия формулы".</span><span class="sxs-lookup"><span data-stu-id="9f5ea-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="9f5ea-122">Щелкните Побочные продукты.</span><span class="sxs-lookup"><span data-stu-id="9f5ea-122">Click Co-products.</span></span>
3. <span data-ttu-id="9f5ea-123">Щелкните Копировать.</span><span class="sxs-lookup"><span data-stu-id="9f5ea-123">Click Copy.</span></span>
4. <span data-ttu-id="9f5ea-124">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9f5ea-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="9f5ea-125">В поле "Версия формулы" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9f5ea-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="9f5ea-126">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9f5ea-126">Click OK.</span></span>
7. <span data-ttu-id="9f5ea-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f5ea-127">Close the page.</span></span>

