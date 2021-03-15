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
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a90a257debe8f24e149ddca1738d8376b2124012
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966988"
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