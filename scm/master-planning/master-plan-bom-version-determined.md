---
title: "Определение версии спецификации"
description: "Во время развертывания спроса, если номенклатура имеет тип заказа по умолчанию со значением &quot;Производство&quot;, механизм планирования ищет допустимую версию спецификации, основанную на узле."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 134b9f7fd46b5326eb6f1f4fec4ed2bda8a8576a
ms.contentlocale: ru-ru
ms.lasthandoff: 04/25/2017


---

# <a name="determine-the-bom-version"></a>Определение версии спецификации

[!include[banner](../includes/banner.md)]


Во время развертывания спроса, если номенклатура имеет тип заказа по умолчанию со значением "Производство", механизм планирования ищет допустимую версию спецификации, основанную на узле. 

Аналитика сайта уже известна и указана в проводке по спросу. Для определения версии спецификации для использования применяется следующий процесс.

-   Если для номенклатуры определена версия спецификации на узле спроса, программа использует эту зависящую от узла спецификацию.
-   Если для номенклатуры не определена версия спецификации на узле спроса, используется общая спецификация. Общая спецификация не указывает узел и справедлива для нескольких узлов. Если общая спецификация существует, она будет использоваться.
-   Если отсутствует общая версия спецификации для использования, развертывание требования останавливается в этой точке.

Допустимая версия спецификации, зависящей от узла или общей, должна удовлетворять требуемым критериям на дату и количество.






