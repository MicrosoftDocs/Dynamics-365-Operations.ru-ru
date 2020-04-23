---
title: Перемещение, замена и установка активов
description: В этом разделе объясняется, как перемещать, заменять и устанавливать активы в «Управлении активами».
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e203c9b1cfb61e0a512f678b0c29ff40b9628e8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216332"
---
# <a name="move-replace-and-install-assets"></a><span data-ttu-id="9214f-103">Перемещение, замена и установка активов</span><span class="sxs-lookup"><span data-stu-id="9214f-103">Move, replace, and install assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="9214f-104">В этом разделе объясняется, как перемещать, заменять и устанавливать активы в «Управлении активами».</span><span class="sxs-lookup"><span data-stu-id="9214f-104">This topic explains how to move, replace, and install assets in Asset Management.</span></span> <span data-ttu-id="9214f-105">Можно создать отдельные активы, не имеющие отношения к другим активам, или создать структуру активов, включающую материнский актив (актив верхнего уровня) и связанные с ним дочерние активы (вложенные активы).</span><span class="sxs-lookup"><span data-stu-id="9214f-105">You can create individual assets that have no relations to other assets, or you can create an asset structure that includes a parent asset (top-level asset) and related child assets (sub-assets).</span></span> <span data-ttu-id="9214f-106">В «Управлении активами» существует три подхода к перемещению и изменению местоположения актива:</span><span class="sxs-lookup"><span data-stu-id="9214f-106">In Asset Management, there are three approaches to moving and changing the location of an asset:</span></span>

- <span data-ttu-id="9214f-107">**Перемещение** — Перемещение активов в другую структуру актива или в другое местоположение в той же структуре актива.</span><span class="sxs-lookup"><span data-stu-id="9214f-107">**Move** – Move an asset either to another asset structure or to another location in the same asset structure.</span></span>
- <span data-ttu-id="9214f-108">**Заменить** — Временно удалить актив из структуры активов, так что он может быть отремонтирован или модернизирован, а затем добавить отремонтированный актив обратно в структуру активов позже.</span><span class="sxs-lookup"><span data-stu-id="9214f-108">**Replace** – Temporarily remove an asset from an asset structure so that it can be repaired or refurbished, and then add the refurbished asset back to the asset structure later.</span></span> <span data-ttu-id="9214f-109">Кроме того, окончательно заменить использованный актив новым активом.</span><span class="sxs-lookup"><span data-stu-id="9214f-109">Alternatively, permanently replace a used asset with a new asset.</span></span>
- <span data-ttu-id="9214f-110">**Установка** — Установка родительского актива и любых связанных с ним дочерних активов в функциональном местоположении.</span><span class="sxs-lookup"><span data-stu-id="9214f-110">**Install** – Install a parent asset and any related child assets on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="9214f-111">Актив, который вы перемещаете, заменяете или устанавливаете, может быть связан с другим функциональным местоположением.</span><span class="sxs-lookup"><span data-stu-id="9214f-111">The asset that you move, replace, or install might be related to another functional location.</span></span> <span data-ttu-id="9214f-112">В этом случае актив может использовать финансовую аналитику функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="9214f-112">In that case, the asset might use financial dimensions of the functional location.</span></span> <span data-ttu-id="9214f-113">На странице **Типы функциональных местоположений** настраивается обработка финансовой аналитики в функциональных местоположениях.</span><span class="sxs-lookup"><span data-stu-id="9214f-113">On the **Functional location types** page, you set up the handling of financial dimensions on functional locations.</span></span>

## <a name="move-asset"></a><span data-ttu-id="9214f-114">Перемещение актива</span><span class="sxs-lookup"><span data-stu-id="9214f-114">Move asset</span></span>

<span data-ttu-id="9214f-115">Используйте функцию **Перемещение актива** чтобы переместить актив в другую структуру актива или в другое местоположение в той же структуре актива.</span><span class="sxs-lookup"><span data-stu-id="9214f-115">Use the **Move asset** function to move an asset either to another asset structure or to another location in the same asset structure.</span></span> <span data-ttu-id="9214f-116">Вы также можете переместить актив из структуры активов, так что он становится автономным активом, который не имеет структурных отношений.</span><span class="sxs-lookup"><span data-stu-id="9214f-116">You can also move an asset out of an asset structure so that it becomes a standalone asset that has no structure relations.</span></span>

> [!NOTE]
> <span data-ttu-id="9214f-117">Не используйте эту функцию, если активы восстанавливаются или временно заменяются.</span><span class="sxs-lookup"><span data-stu-id="9214f-117">Don't use this function if assets are being repaired or temporarily replaced.</span></span> <span data-ttu-id="9214f-118">Вместо этого используйте функциональность **Заменить актив**, описанную позже в этой разделе.</span><span class="sxs-lookup"><span data-stu-id="9214f-118">Instead, use the **Replace asset** functionality that is described later in this topic.</span></span>

1. <span data-ttu-id="9214f-119">Выберите **Управление активами** \> **Общее** \> **Активы** \> **Все активы** или **Активные активы**.</span><span class="sxs-lookup"><span data-stu-id="9214f-119">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="9214f-120">В списке выберите перемещаемый актив.</span><span class="sxs-lookup"><span data-stu-id="9214f-120">In the list, select the asset to move.</span></span> <span data-ttu-id="9214f-121">Если актив имеет дочерние активы, вы также перемещаете эти активы.</span><span class="sxs-lookup"><span data-stu-id="9214f-121">If the asset has child assets, you also move those assets.</span></span>
3. <span data-ttu-id="9214f-122">Выберите **Перемещение актива**.</span><span class="sxs-lookup"><span data-stu-id="9214f-122">Select **Move asset**.</span></span>
4. <span data-ttu-id="9214f-123">Чтобы переместить актив таким образом, чтобы он стал частью структуры актива, выберите новый родительский актив в поле **Родительский актив**.</span><span class="sxs-lookup"><span data-stu-id="9214f-123">To move the asset so that it becomes part of an asset structure, select the new parent asset in the **Parent asset** field.</span></span> <span data-ttu-id="9214f-124">Если вы перемещаете дочерний актив, и вы хотите сделать его автономным активом, который не имеет структурных отношений, оставьте поле **Родительский актив** пустым.</span><span class="sxs-lookup"><span data-stu-id="9214f-124">If you're moving a child asset, and you want to make it a standalone asset that has no structure relations, leave the **Parent asset** field blank.</span></span>
5. <span data-ttu-id="9214f-125">По умолчанию, в поле **Действует с** автоматически задаются текущая дата и время.</span><span class="sxs-lookup"><span data-stu-id="9214f-125">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="9214f-126">Тем не менее, можно выбрать другую дату и время, с которого перемещение актива действительно.</span><span class="sxs-lookup"><span data-stu-id="9214f-126">However, you can select a different date and time that the asset move is valid from.</span></span>
6. <span data-ttu-id="9214f-127">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9214f-127">Select **OK**.</span></span>

## <a name="replace-asset"></a><span data-ttu-id="9214f-128">Заменить актив</span><span class="sxs-lookup"><span data-stu-id="9214f-128">Replace asset</span></span>

<span data-ttu-id="9214f-129">Используйте функцию **Заменить актив** в связи с ремонтом, реконструкцией или окончательной заменой изношенного актива новым активом.</span><span class="sxs-lookup"><span data-stu-id="9214f-129">Use the **Replace asset** function in connection with repairs, refurbishment, or permanent replacement of a worn-out asset by a new asset.</span></span> <span data-ttu-id="9214f-130">Эта функция используется для замены дочерних активов в структуре активов.</span><span class="sxs-lookup"><span data-stu-id="9214f-130">This function is used to replace child assets in an asset structure.</span></span> <span data-ttu-id="9214f-131">Для родительских активов (т.е. активов, которые в настоящее время не имеют родительского актива) эта замена выполняется в функциональном местоположении.</span><span class="sxs-lookup"><span data-stu-id="9214f-131">For parent assets (that is, assets that don't currently have a parent asset), this replacement is done on a functional location.</span></span> <span data-ttu-id="9214f-132">Для получения дополнительной информации о том, как заменить родительские активы в функциональном местоположении, см. раздел [Установка активов в функциональных местоположениях](../functional-locations/install-objects-on-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="9214f-132">For more information about how to replace parent assets on a functional location, see [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="9214f-133">Если ремонтная мастерская связана с вашим производственным подразделением, вы можете создать функциональные местоположения, такие как **Ремонт**, **Отходы**, и **Хранение** для обработки ремонта и замены активов.</span><span class="sxs-lookup"><span data-stu-id="9214f-133">If a repair shop is related to your production department, you can create functional locations such as **Repair**, **Scrap**, and **Storage** to handle the repair and replacement of assets.</span></span>

1. <span data-ttu-id="9214f-134">Выберите **Управление активами** \> **Общее** \> **Активы** \> **Все активы** или **Активные активы**.</span><span class="sxs-lookup"><span data-stu-id="9214f-134">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="9214f-135">В списке выберите дочерний актив для замены.</span><span class="sxs-lookup"><span data-stu-id="9214f-135">In the list, select the child asset to replace.</span></span> <span data-ttu-id="9214f-136">Если актив имеет дочерние активы, вы также заменяете эти активы.</span><span class="sxs-lookup"><span data-stu-id="9214f-136">If the asset has child assets, you also replace those assets.</span></span>
3. <span data-ttu-id="9214f-137">Выберите **Заменить актив**.</span><span class="sxs-lookup"><span data-stu-id="9214f-137">Select **Replace asset**.</span></span>

    <span data-ttu-id="9214f-138">Поле **Изменение структуры** показывает последнюю дату и время перемещения выбранного актива и связанных с ними дочерних активов в структуре актива.</span><span class="sxs-lookup"><span data-stu-id="9214f-138">The **Structure change** field shows the last date and time that the selected asset and related child assets were moved in the asset structure.</span></span>

4. <span data-ttu-id="9214f-139">В разделе **Выбранный актив** в поле **Целевое функциональное местоположение** выберите функциональное местоположение для перемещения актива.</span><span class="sxs-lookup"><span data-stu-id="9214f-139">In the **Selected asset** section, in the **Target functional location** field, select the functional location to move the asset to.</span></span> <span data-ttu-id="9214f-140">Например, выберите местоположение **Ремонт** или **Отходы**.</span><span class="sxs-lookup"><span data-stu-id="9214f-140">For example, select the **Repair** or **Scrap** location.</span></span>

    <span data-ttu-id="9214f-141">В разделе **Родительский актив** поле **Действует с** показывает последнюю дату и время установки или перемещения родительского актива и связанных с ними дочерних активов в текущее функциональное местоположение.</span><span class="sxs-lookup"><span data-stu-id="9214f-141">In the **Parent asset** section, the **Effective** field shows the last date and time that the parent asset and related child assets were installed or moved on the current functional location.</span></span>

5. <span data-ttu-id="9214f-142">В разделе **Новый актив** в поле **Актив** выберите актив для вставки в качестве временной или постоянной замены выбранного актива.</span><span class="sxs-lookup"><span data-stu-id="9214f-142">In the **New asset** section, in the **Asset** field, select the asset to insert as a temporary or permanent replacement for the selected asset.</span></span> <span data-ttu-id="9214f-143">В настоящее время этот актив может находиться в другом функциональном местоположении, например, **Хранение**.</span><span class="sxs-lookup"><span data-stu-id="9214f-143">This asset might currently be located on another functional location, such as **Storage**.</span></span>
7. <span data-ttu-id="9214f-144">В разделе **Действует с** поле **Действует с** по умолчанию задаются текущая дата и время.</span><span class="sxs-lookup"><span data-stu-id="9214f-144">In the **Effective from** section, the **Effective** field is set to the current date and time by default.</span></span> <span data-ttu-id="9214f-145">Тем не менее, можно выбрать другую дату и время, с которого замена актива действительна.</span><span class="sxs-lookup"><span data-stu-id="9214f-145">However, you can select a different date and time that the asset replacement is valid from.</span></span>
8. <span data-ttu-id="9214f-146">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9214f-146">Select **OK**.</span></span>

## <a name="install-asset"></a><span data-ttu-id="9214f-147">Установите актив</span><span class="sxs-lookup"><span data-stu-id="9214f-147">Install asset</span></span>

<span data-ttu-id="9214f-148">Используйте функцию **Установить актив** для установки структуры актива в функциональном местоположении.</span><span class="sxs-lookup"><span data-stu-id="9214f-148">Use the **Install asset** function to install an asset structure on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="9214f-149">Всегда выбирайте родительский актив.</span><span class="sxs-lookup"><span data-stu-id="9214f-149">Always select a parent asset.</span></span> <span data-ttu-id="9214f-150">Родительский актив и связанные с ними дочерние активы будут перемещены в выбранное функциональное местоположение.</span><span class="sxs-lookup"><span data-stu-id="9214f-150">The parent asset and related child assets will be moved to the selected functional location.</span></span>

1. <span data-ttu-id="9214f-151">Выберите **Управление активами** \> **Общее** \> **Активы** \> **Все активы** или **Активные активы**.</span><span class="sxs-lookup"><span data-stu-id="9214f-151">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="9214f-152">В списке выберите родительский актив для установки в другое функциональное местоположение.</span><span class="sxs-lookup"><span data-stu-id="9214f-152">In the list, select the parent asset to install on another functional location.</span></span>
3. <span data-ttu-id="9214f-153">Выберите **Установить актив**.</span><span class="sxs-lookup"><span data-stu-id="9214f-153">Select **Install asset**.</span></span>

    <span data-ttu-id="9214f-154">Раздел **Атрибуты** показывает атрибуты актива, настроенные на родительский актив.</span><span class="sxs-lookup"><span data-stu-id="9214f-154">The **Attributes** section shows the asset attributes that are set up on the parent asset.</span></span>

4. <span data-ttu-id="9214f-155">В поле **Функциональное местоположение** выберите новое местоположение.</span><span class="sxs-lookup"><span data-stu-id="9214f-155">In the **Functional location** field, select the new location.</span></span>
5. <span data-ttu-id="9214f-156">По умолчанию, в поле **Действует с** автоматически задаются текущая дата и время.</span><span class="sxs-lookup"><span data-stu-id="9214f-156">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="9214f-157">Тем не менее, можно выбрать другую дату и время, с которого установка в структуру актива действительна.</span><span class="sxs-lookup"><span data-stu-id="9214f-157">However, you can select a different date and time that the installation on the asset structure is valid from.</span></span>
6. <span data-ttu-id="9214f-158">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9214f-158">Select **OK**.</span></span>
