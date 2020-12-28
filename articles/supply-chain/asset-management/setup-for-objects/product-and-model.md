---
title: Производители и модели актива
description: В этом разделе объясняется, как настроить производителей активов и связанные с ними модели в «Управлении активами».
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae2dfcebcbab77cba1795a8b559a3a4244abd00e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435943"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="bac90-103">Производители и модели актива</span><span class="sxs-lookup"><span data-stu-id="bac90-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="bac90-104">В этом разделе объясняется, как настроить производителей активов и связанные с ними модели в «Управлении активами».</span><span class="sxs-lookup"><span data-stu-id="bac90-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="bac90-105">Модели могут быть связаны с типами активов.</span><span class="sxs-lookup"><span data-stu-id="bac90-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="bac90-106">Настройте связи продукт-модель</span><span class="sxs-lookup"><span data-stu-id="bac90-106">Set up product-model relations</span></span>

1. <span data-ttu-id="bac90-107">Выберите **Управление активами** \> **Настройка** \> **Активы** \> **Производитель и модель**.</span><span class="sxs-lookup"><span data-stu-id="bac90-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="bac90-108">Выберите **Создать** для создания нового продукта.</span><span class="sxs-lookup"><span data-stu-id="bac90-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="bac90-109">В поле **Производитель** введите название для производителя актива.</span><span class="sxs-lookup"><span data-stu-id="bac90-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="bac90-110">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="bac90-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="bac90-111">На экспресс-вкладке **Модели** выберите **Добавить** для создания модели активов, которая должна быть связана с производителем активов.</span><span class="sxs-lookup"><span data-stu-id="bac90-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="bac90-112">В поле **Модель** введите название для модели актива.</span><span class="sxs-lookup"><span data-stu-id="bac90-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="bac90-113">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="bac90-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="bac90-114">В поле **Тип активов** выберите тип актива, с которым должна быть связана модель производителя.</span><span class="sxs-lookup"><span data-stu-id="bac90-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bac90-115">Можно также настроить отношения для типов активов, производителей и моделей в поиске **Типы активов**.</span><span class="sxs-lookup"><span data-stu-id="bac90-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="bac90-116">Дополнительные сведения см. в разделе [Типы активов](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="bac90-116">For more information, see [Asset types](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="bac90-117">На экспресс-вкладке **Подробно** поле **Модели** отображает количество моделей активов, настроенных на выбранного производителя активов.</span><span class="sxs-lookup"><span data-stu-id="bac90-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="bac90-118">Поле **Активы** показывает количество активов, использующих выбранного производителя.</span><span class="sxs-lookup"><span data-stu-id="bac90-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="bac90-119">Поле **Активы** показывает количество объектов, использующих модель производителя.</span><span class="sxs-lookup"><span data-stu-id="bac90-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="bac90-120">Тип активов может не иметь отношений модели производителя активов, он может быть связан с одной моделью производителя активов, или может быть связан с несколькими моделями производителя активов.</span><span class="sxs-lookup"><span data-stu-id="bac90-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="bac90-121">Если тип актива связан по крайней мере с одной моделью производителя, только комбинации, настроенные в поиске **Модел производителя**, могут быть выбраны на страницах «Управления активами», где комбинация типа активов, производителя и модели может быть настроены.</span><span class="sxs-lookup"><span data-stu-id="bac90-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="bac90-122">Эти страницы включают **Все активы**, **Уровни обслуживания активов**, **Типы задания по умолчанию**, и **Строки бюджета обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="bac90-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="bac90-123">Если некоторые типы активов не связаны с какой-либо моделью производителя, на страницах отображаются только те типы активов и модели производителей, которые также не имеют никакого отношения к типам активов.</span><span class="sxs-lookup"><span data-stu-id="bac90-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="bac90-124">Выберите производителя и модель по объекту</span><span class="sxs-lookup"><span data-stu-id="bac90-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="bac90-125">Выберите **Управление активами** \> **Общие** \> **Активы** \> **Все активы**.</span><span class="sxs-lookup"><span data-stu-id="bac90-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="bac90-126">В столбце **Актив** выберите ссылку для актива.</span><span class="sxs-lookup"><span data-stu-id="bac90-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="bac90-127">Появится страница **Подробно**.</span><span class="sxs-lookup"><span data-stu-id="bac90-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="bac90-128">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="bac90-128">Select **Edit**.</span></span>
4. <span data-ttu-id="bac90-129">На экспресс-вкладке **Общее** выберите значения в полях **Производитель** и **Модель**.</span><span class="sxs-lookup"><span data-stu-id="bac90-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>
