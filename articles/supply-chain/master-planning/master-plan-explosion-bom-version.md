---
title: Развертывание версии спецификации
description: В этой статье объясняется сценарий сводного планирования, который включает в себя развертывание версии спецификации (BOM).
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c4f1306faa2c0ae02fee48449839db4ff0907ff
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348400"
---
# <a name="explosion-of-a-bom-version"></a>Развертывание версии спецификации

[!include [banner](../includes/banner.md)]

В этой статье объясняется сценарий сводного планирования, который включает в себя развертывание версии спецификации (BOM).

Развертывание спроса версии спецификаций приводит к созданию спроса по каждой номенклатуре строки спецификаций на определенном сайте и, возможно, на определенном складе. Для спецификации сайта может быть определен конкретный склад для каждой строки спецификаций. Кроме того, для каждой строки спецификаций настройки аналитики номенклатуры определяют, требуется ли склад. Этот итоговый спрос по каждой номенклатуре строки спецификации становится, в свою очередь, исходной точкой для дополнительного развертывания спроса. Этот сценарий сводного планирования включает следующие условия:

-   Аналитика площадки является обязательной и должна вводится по проводке запроса.
-   Аналитика площадки является непротиворечивой. Поэтому площадка для запросов нижних уровней - та же, что и площадка для первоначальной проводки запросов.

На следующей иллюстрации показан процесс развертывания спроса сводного планирования. ![Развертывание спроса с использованием версии спецификации.](./media/multisitedemandexplosionscenariousingbomversion.gif)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Определение версии спецификации](master-plan-bom-version-determined.md)

[Обзор сводного планирования и функции работы с несколькими узлами](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]