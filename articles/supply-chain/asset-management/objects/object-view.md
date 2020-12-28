---
title: Представление актива
description: Этот раздел описывает представление актива в «Управлении активами».
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTree, EntAssetFunctionalLocationTree
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc4cd9ada9c1f64b434cd657eb5f5654c1328ef4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436173"
---
# <a name="asset-view"></a><span data-ttu-id="5d2c8-103">Представление актива</span><span class="sxs-lookup"><span data-stu-id="5d2c8-103">Asset view</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5d2c8-104">Этот раздел описывает представление актива в «Управлении активами».</span><span class="sxs-lookup"><span data-stu-id="5d2c8-104">This topic describes the asset view in Asset Management.</span></span> <span data-ttu-id="5d2c8-105">Страница **Представление актива** показывает активные активы и функциональные местоположения в представлении дерева.</span><span class="sxs-lookup"><span data-stu-id="5d2c8-105">The **Asset view** page shows active assets and functional locations in a tree view.</span></span> <span data-ttu-id="5d2c8-106">Таким образом, вы можете легко получить обзор связей актива с функциональными местоположениями.</span><span class="sxs-lookup"><span data-stu-id="5d2c8-106">Therefore, you can easily get an overview of asset relations to functional locations.</span></span> <span data-ttu-id="5d2c8-107">Кроме того, вы можете просматривать детальную информацию о функциональных местоположениях, активах и связанных с ними спецификациями.</span><span class="sxs-lookup"><span data-stu-id="5d2c8-107">Additionally, you can view detailed information about functional locations, assets, and related bills of materials (BOMs).</span></span> <span data-ttu-id="5d2c8-108">Вы также можете получить краткий обзор активных запросов на обслуживание и заказов на работу, связанных с активом.</span><span class="sxs-lookup"><span data-stu-id="5d2c8-108">You can also get a quick overview of active maintenance requests and work orders that are related to an asset.</span></span>

1. <span data-ttu-id="5d2c8-109">Выберите **Управление активами** \> **Общие** \> **Активы** \> **Представление актива**.</span><span class="sxs-lookup"><span data-stu-id="5d2c8-109">Select **Asset management** \> **Common** \> **Assets** \> **Asset view**.</span></span>
2. <span data-ttu-id="5d2c8-110">Чтобы изменить представление, отображаемое на странице, выберите новое значение в поле **Представление**.</span><span class="sxs-lookup"><span data-stu-id="5d2c8-110">To change the view that is shown on the page, select a new value in the **View** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5d2c8-111">Представление по умолчанию, отображаемое при открытии страницы **Представление актива** зависит от значения, выбранного в поле **Представление** на вкладке **Активы** страницы **Параметры управления активами** (**Управление активами** \> **Настройка** \> **Параметры управления активами**).</span><span class="sxs-lookup"><span data-stu-id="5d2c8-111">The default view that is shown when you open the **Asset view** page depends on the value that is selected in the **View** field on the **Assets** tab of the **Asset management parameters** page (**Asset management** \> **Setup** \> **Asset management parameters**).</span></span>

<span data-ttu-id="5d2c8-112">На правой стороне страницы экспресс-вкладка показывает детали выбранного представления.</span><span class="sxs-lookup"><span data-stu-id="5d2c8-112">On the right side of the page, FastTabs shows details of the selected view.</span></span>

<span data-ttu-id="5d2c8-113">След навигации, которая появляется выше представления дерева, показывает текущий выбор в представлении дерева.</span><span class="sxs-lookup"><span data-stu-id="5d2c8-113">The breadcrumb trail that appears above the tree view shows the current selection in the tree view.</span></span> <span data-ttu-id="5d2c8-114">Этот след навигации использует следующий формат:</span><span class="sxs-lookup"><span data-stu-id="5d2c8-114">This breadcrumb trail uses the following format:</span></span>

<span data-ttu-id="5d2c8-115">Идентификатор функционального местоположения / Идентификатор функционального местоположения (если есть более одного функционального местоположения) \> Идентификатор актива / Идентификатор актива (если есть более одного актива) — Код номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="5d2c8-115">Functional location ID / Functional location ID (if there is more than one functional location) \> Asset ID / Asset ID (if there is more than one asset) - Item number.</span></span>

<span data-ttu-id="5d2c8-116">Если вы выбрали актив в представлении дерева, можно выбрать **Активные запросы** или **Активные заказы на работу** для просмотра запросов на обслуживание или заказов на работу, связанных с активом.</span><span class="sxs-lookup"><span data-stu-id="5d2c8-116">If you've selected an asset in the tree view, you can select **Active requests** or **Active work orders** to view the maintenance requests or work orders that are related to the asset.</span></span> <span data-ttu-id="5d2c8-117">Вы также можете выбрать **Открыть** \> **Функциональное местоположение**, **Актив**, или **Спецификация актива**, чтобы открыть связанное представление.</span><span class="sxs-lookup"><span data-stu-id="5d2c8-117">You can also select **Open** \> **Functional location**, **Asset**, or **Asset BOM** to open the related view.</span></span>

<span data-ttu-id="5d2c8-118">Параметр **Функциональные местоположения актива**, который можно выбрать в поле **Представление**, также доступен в любом поиске активов, где можно выбрать актив.</span><span class="sxs-lookup"><span data-stu-id="5d2c8-118">The **Asset functional locations** option that you can select in the **View** field is also available in any asset lookup where you can select an asset.</span></span> <span data-ttu-id="5d2c8-119">Представление дерева отображается на вкладке **Представление актива**, например, где вы [создаете актив](../objects/create-an-object.md), создаете запрос на обслуживание или создаете заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="5d2c8-119">The tree view is shown on an **Asset view** tab, for example, where you [create an asset](../objects/create-an-object.md), create a maintenance request, or create a work order.</span></span>
