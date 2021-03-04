---
title: Консолидированные партионные заказы
description: Эта статья описывает понятие консолидированных заказов партий.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: faeb90aa3366a58b746c0b397dd950bfb8c9024f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436206"
---
# <a name="consolidated-batch-orders"></a>Консолидированные партионные заказы

[!include [banner](../includes/banner.md)]

Эта статья описывает понятие консолидированных заказов партий.

Производимая нефасованная номенклатура считается родительской номенклатурой, тогда как номенклатура с упаковкой считается дочерней. Отношение между нефасованной номенклатурой и упакованной номенклатурой выражается в преобразовании нефасованной номенклатуры. Это преобразование нефасованной номенклатуры определяется для самой нефасованной номенклатуры.  

Номенклатуры в упаковке могут быть упакованы или в контейнеры одного размера или нескольких размеров, которые считаются одной единицей. Путем консолидации заказов для нефасованной номенклатуры можно просмотреть все связанные заказы партий в одном представлении, чтобы облегчить определение всей оставшейся работы, которая должны быть выполнена.  

Консолидированный партионный заказ может содержать любую комбинацию следующих заказов:

-   Один заказ нефасованной номенклатуры и несколько заказов фасованной номенклатуры
-   Несколько заказов нефасованной номенклатуры и несколько заказов фасованной номенклатуры
-   Несколько заказов нефасованной номенклатуры и один заказ фасованной номенклатуры
-   Только фасованные заказы






[!INCLUDE[footer-include](../../includes/footer-banner.md)]