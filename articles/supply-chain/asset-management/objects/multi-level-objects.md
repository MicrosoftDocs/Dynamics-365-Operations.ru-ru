---
title: Многоуровневые активы
description: В этом разделе объясняется, как создавать и удалять многоуровневые активы.
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
ms.openlocfilehash: 4b7609a85f0315ee5cb5fae62d151b271ef5febe
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214899"
---
# <a name="multi-level-assets"></a><span data-ttu-id="3c569-103">Многоуровневые активы</span><span class="sxs-lookup"><span data-stu-id="3c569-103">Multi-level assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="3c569-104">В этом разделе объясняется, как создавать и удалять многоуровневые активы.</span><span class="sxs-lookup"><span data-stu-id="3c569-104">This topic explains how to create and delete multi-level assets.</span></span> <span data-ttu-id="3c569-105">Можно создавать активы и связанные с ними вложенные активы в иерархической структуре дерева.</span><span class="sxs-lookup"><span data-stu-id="3c569-105">You can create assets and related sub-assets in a hierarchical tree structure.</span></span> <span data-ttu-id="3c569-106">Таким образом, можно показать отношения и зависимости между активами.</span><span class="sxs-lookup"><span data-stu-id="3c569-106">In this way, you can show relations and dependencies among assets.</span></span> <span data-ttu-id="3c569-107">Задания обслуживания могут быть связаны со всеми уровнями структуры дерева.</span><span class="sxs-lookup"><span data-stu-id="3c569-107">Maintenance jobs can be related to all levels of the tree structure.</span></span> <span data-ttu-id="3c569-108">Статистические данные также могут быть созданы на индивидуальном уровне или в виде суммы всех уровней вложенных активов.</span><span class="sxs-lookup"><span data-stu-id="3c569-108">Statistics can also be created for an individual level or as a sum of all sub-asset levels.</span></span>

<span data-ttu-id="3c569-109">На странице списка **Все активы** (**Управление активами** \> **Общее** \> **Активы** \> **Все активы**), столбец **Активы** перечисляет активы в иерархическом порядке.</span><span class="sxs-lookup"><span data-stu-id="3c569-109">On the **All Assets** list page (**Asset management** \> **Common** \> **Assets** \> **All assets**), the **Asset** column lists assets in hierarchical order.</span></span> <span data-ttu-id="3c569-110">В столбце **Родитель** отображается связанный родитель.</span><span class="sxs-lookup"><span data-stu-id="3c569-110">The **Parent** column shows the related parent.</span></span> <span data-ttu-id="3c569-111">Кроме того, если активы и вложенные активы уже созданы, раздел **Дерево активов** в панели **Связанные сведения** показывает активы в структуре дерева.</span><span class="sxs-lookup"><span data-stu-id="3c569-111">Additionally, if assets and sub-assets have already been created, the **Asset tree** section in the **Related information** pane shows the assets in a tree structure.</span></span>

<span data-ttu-id="3c569-112">Дополнительные сведения о создании актива см. в разделе [Создать актив](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="3c569-112">For information about how to create an asset, see [Create an asset](../objects/create-an-object.md).</span></span> <span data-ttu-id="3c569-113">Чтобы создать вложенный актив, выберите родительский актив в поле **Родитель** на экспресс-вкладке **Общее**.</span><span class="sxs-lookup"><span data-stu-id="3c569-113">To create a sub-asset, select the parent asset in the **Parent** field on the **General** FastTab.</span></span>

## <a name="copy-an-asset-or-asset-structure"></a><span data-ttu-id="3c569-114">Копирование актива или структуры актива</span><span class="sxs-lookup"><span data-stu-id="3c569-114">Copy an asset or asset structure</span></span>

<span data-ttu-id="3c569-115">Если ваша компания имеет несколько аналогичных структур активов, вы можете использовать функцию копирования в «Управлении активами», чтобы быстро создать их.</span><span class="sxs-lookup"><span data-stu-id="3c569-115">If your company has several similar asset structures, you can use the Copy function in Asset Management to quickly create them.</span></span>

1. <span data-ttu-id="3c569-116">Выберите **Управление активами** \> **Общие** \> **Активы** \> **Все активы**.</span><span class="sxs-lookup"><span data-stu-id="3c569-116">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="3c569-117">На странице списка **Все активы** выберите актив для копирования.</span><span class="sxs-lookup"><span data-stu-id="3c569-117">On the **All assets** list page, select the asset to copy.</span></span> <span data-ttu-id="3c569-118">Например, если вы хотите копировать всю структуру актива, включая вложенные активы, выберите родительский актив.</span><span class="sxs-lookup"><span data-stu-id="3c569-118">For example, if you want to copy the whole asset structure, including sub-assets, select a parent asset.</span></span>
3. <span data-ttu-id="3c569-119">Выберите **Копировать актив**.</span><span class="sxs-lookup"><span data-stu-id="3c569-119">Select **Copy asset**.</span></span> <span data-ttu-id="3c569-120">В разделе **Копировать из** поле **Актив** настроено на актив, выбранный на странице списка.</span><span class="sxs-lookup"><span data-stu-id="3c569-120">In the **Copy from** section, the **Asset** field is set to the asset that you selected on the list page.</span></span>
4. <span data-ttu-id="3c569-121">В разделе **Копировать в** в поле **Актив** введите имя нового актива.</span><span class="sxs-lookup"><span data-stu-id="3c569-121">In the **Copy to** section, in the **Asset** field, enter the name of the new asset.</span></span>
5. <span data-ttu-id="3c569-122">Если создаваемый актив должен быть частью существующей структуры актива, в разделе **Родительский актива** в поле **Актив** выберите идентификатор родительского актива.</span><span class="sxs-lookup"><span data-stu-id="3c569-122">If the asset that you're creating should be part of an existing asset structure, in the **Parent asset** section, in the **Asset** field, select a parent ID.</span></span>
6. <span data-ttu-id="3c569-123">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3c569-123">Select **OK**.</span></span> <span data-ttu-id="3c569-124">Новая структура актива отображается на странице списка **Все активы**.</span><span class="sxs-lookup"><span data-stu-id="3c569-124">The new asset structure is shown on the **All assets** list page.</span></span> <span data-ttu-id="3c569-125">Все атрибуты актива, планы обслуживания и циклы обслуживания, связанные с скопированным активом, перемещаются в новый актив или структуру актива.</span><span class="sxs-lookup"><span data-stu-id="3c569-125">All asset attributes, maintenance plans, and maintenance rounds that are related to the asset that you copied are transferred to the new asset or asset structure.</span></span>

<span data-ttu-id="3c569-126">При копировании структуры актива вложенные активы в новой структуре имеют то же имя, что и вложенные активы, которые вы скопировали.</span><span class="sxs-lookup"><span data-stu-id="3c569-126">When you copy an asset structure, the sub-assets in the new structure have the same name as the sub-assets that you copied.</span></span> <span data-ttu-id="3c569-127">После завершения процедуры копирования можно легко изменить имя и другие настройки актива.</span><span class="sxs-lookup"><span data-stu-id="3c569-127">After the copy procedure is completed, you can easily change the name and other settings for an asset.</span></span> <span data-ttu-id="3c569-128">Выберите актив на странице списка **Все активы**, а затем выберите кнопку **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="3c569-128">Select the asset on the **All assets** list page, and then select the **Edit** button.</span></span>

> [!NOTE]
> <span data-ttu-id="3c569-129">При копировании актива или структуры актива состояние жизненного цикла новых активов сбрасывается в любое состояние, определяемое как исходное состояние жизненного цикла для активов.</span><span class="sxs-lookup"><span data-stu-id="3c569-129">When you copy an asset or asset structure, the lifecycle state of the new assets is reset to whatever state you defined as the initial lifecycle state for assets.</span></span> <span data-ttu-id="3c569-130">Функциональное местоположение сбросится в функциональное местоположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c569-130">The functional location is reset to the default functional location.</span></span>

## <a name="delete-an-asset-or-asset-structure"></a><span data-ttu-id="3c569-131">Удалить актив или структуру актива</span><span class="sxs-lookup"><span data-stu-id="3c569-131">Delete an asset or asset structure</span></span>

<span data-ttu-id="3c569-132">Если актив имеет связанные вложенные активы, вы можете удалить его только в том случае, если на любом из активов не зарегистрированы запросы на обслуживание, задания по заказу на работу, регистрации ошибок или оценки состояния.</span><span class="sxs-lookup"><span data-stu-id="3c569-132">If an asset has related sub-assets, you can delete it only if no maintenance requests, work order jobs, fault registrations, or condition assessments are registered on any of the assets.</span></span>

1. <span data-ttu-id="3c569-133">На странице списка **Все активы** выберите актив для удаления.</span><span class="sxs-lookup"><span data-stu-id="3c569-133">On the **All assets** list page, select the asset to delete.</span></span>
2. <span data-ttu-id="3c569-134">Выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="3c569-134">Select **Delete**.</span></span>

> [!NOTE]
> <span data-ttu-id="3c569-135">Если вы не можете удалить актив с помощью этой процедуры, другой способ выполнения удаления — настроить для этой цели состояние жизненного цикла актива.</span><span class="sxs-lookup"><span data-stu-id="3c569-135">If you can't delete an asset by using this procedure, another way to handle deletion is to set up an asset lifecycle state for this purpose.</span></span> <span data-ttu-id="3c569-136">Например, можно настроить состояние жизненного цикла **Списано** или **Удалено** на странице **Состояния жизненного цикла активов**.</span><span class="sxs-lookup"><span data-stu-id="3c569-136">For example, you can set up a **Scrapped** or **Deleted** lifecycle state on the **Asset lifecycle states** page.</span></span>
