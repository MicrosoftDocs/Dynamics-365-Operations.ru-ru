---
title: "Консолидированные партионные заказы"
description: "Эта статья описывает понятие консолидированных заказов партий."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 45c83752b4dc50a615e3bb64320cb22b7fc6dec0
ms.contentlocale: ru-ru
ms.lasthandoff: 05/25/2017


---

# <a name="consolidated-batch-orders"></a>Консолидированные партионные заказы

[!include[banner](../includes/banner.md)]


Эта статья описывает понятие консолидированных заказов партий.

Производимая нефасованная номенклатура считается родительской номенклатурой, тогда как номенклатура с упаковкой считается дочерней. Отношение между нефасованной номенклатурой и упакованной номенклатурой выражается в преобразовании нефасованной номенклатуры. Это преобразование нефасованной номенклатуры определяется для самой нефасованной номенклатуры.  

Номенклатуры в упаковке могут быть упакованы или в контейнеры одного размера или нескольких размеров, которые считаются одной единицей. Путем консолидации заказов для нефасованной номенклатуры можно просмотреть все связанные заказы партий в одном представлении, чтобы облегчить определение всей оставшейся работы, которая должны быть выполнена.  

Консолидированный партионный заказ может содержать любую комбинацию следующих заказов:

-   Один заказ нефасованной номенклатуры и несколько заказов фасованной номенклатуры
-   Несколько заказов нефасованной номенклатуры и несколько заказов фасованной номенклатуры
-   Несколько заказов нефасованной номенклатуры и один заказ фасованной номенклатуры
-   Только фасованные заказы





