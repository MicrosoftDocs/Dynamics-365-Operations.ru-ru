---
title: Консолидированные партионные заказы
description: Эта статья описывает понятие консолидированных заказов партий.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e8d7656889b69cfd1dcffb45b52eb649bce59629
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809238"
---
# <a name="consolidated-batch-orders"></a><span data-ttu-id="3f944-103">Консолидированные партионные заказы</span><span class="sxs-lookup"><span data-stu-id="3f944-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f944-104">Эта статья описывает понятие консолидированных заказов партий.</span><span class="sxs-lookup"><span data-stu-id="3f944-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="3f944-105">Производимая нефасованная номенклатура считается родительской номенклатурой, тогда как номенклатура с упаковкой считается дочерней.</span><span class="sxs-lookup"><span data-stu-id="3f944-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="3f944-106">Отношение между нефасованной номенклатурой и упакованной номенклатурой выражается в преобразовании нефасованной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3f944-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="3f944-107">Это преобразование нефасованной номенклатуры определяется для самой нефасованной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3f944-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="3f944-108">Номенклатуры в упаковке могут быть упакованы или в контейнеры одного размера или нескольких размеров, которые считаются одной единицей.</span><span class="sxs-lookup"><span data-stu-id="3f944-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="3f944-109">Путем консолидации заказов для нефасованной номенклатуры можно просмотреть все связанные заказы партий в одном представлении, чтобы облегчить определение всей оставшейся работы, которая должны быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="3f944-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="3f944-110">Консолидированный партионный заказ может содержать любую комбинацию следующих заказов:</span><span class="sxs-lookup"><span data-stu-id="3f944-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="3f944-111">Один заказ нефасованной номенклатуры и несколько заказов фасованной номенклатуры</span><span class="sxs-lookup"><span data-stu-id="3f944-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="3f944-112">Несколько заказов нефасованной номенклатуры и несколько заказов фасованной номенклатуры</span><span class="sxs-lookup"><span data-stu-id="3f944-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="3f944-113">Несколько заказов нефасованной номенклатуры и один заказ фасованной номенклатуры</span><span class="sxs-lookup"><span data-stu-id="3f944-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="3f944-114">Только фасованные заказы</span><span class="sxs-lookup"><span data-stu-id="3f944-114">Only packed orders</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]