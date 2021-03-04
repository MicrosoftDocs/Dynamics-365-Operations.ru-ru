---
title: Определение версии спецификации
description: Во время развертывания спроса, если номенклатура имеет тип заказа по умолчанию со значением "Производство", механизм планирования ищет допустимую версию спецификации, основанную на узле.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 766c857cca603f84bb7fcef2c7eea3bc76620c19
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436277"
---
# <a name="determine-the-bom-version"></a>Определение версии спецификации

[!include [banner](../includes/banner.md)]

Во время развертывания спроса, если номенклатура имеет тип заказа по умолчанию со значением "Производство", механизм планирования ищет допустимую версию спецификации, основанную на узле. 

Аналитика сайта уже известна и указана в проводке по спросу. Для определения версии спецификации для использования применяется следующий процесс.

-   Если для номенклатуры определена версия спецификации на узле спроса, программа использует эту зависящую от узла спецификацию.
-   Если для номенклатуры не определена версия спецификации на узле спроса, используется общая спецификация. Общая спецификация не указывает узел и справедлива для нескольких узлов. Если общая спецификация существует, она будет использоваться.
-   Если отсутствует общая версия спецификации для использования, развертывание требования останавливается в этой точке.

Допустимая версия спецификации, зависящей от узла или общей, должна удовлетворять требуемым критериям на дату и количество.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]