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
ms.openlocfilehash: d6f1f1656f0ef04799b1ce6b397dac0f829e41c9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251945"
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