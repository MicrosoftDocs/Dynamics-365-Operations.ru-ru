---
title: "Развертывание версии спецификации"
description: "В этой статье объясняется сценарий сводного планирования, который включает в себя развертывание версии спецификации (BOM)."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 80c9fa6ec98bd2cdc3edd5329e2a619ef9cc8cb2
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="explosion-of-a-bom-version"></a>Развертывание версии спецификации

[!include [banner](../includes/banner.md)]

В этой статье объясняется сценарий сводного планирования, который включает в себя развертывание версии спецификации (BOM).

Развертывание спроса версии спецификаций приводит к созданию спроса по каждой номенклатуре строки спецификаций на определенном сайте и, возможно, на определенном складе. Для спецификации сайта может быть определен конкретный склад для каждой строки спецификаций. Кроме того, для каждой строки спецификаций настройки аналитики номенклатуры определяют, требуется ли склад. Этот итоговый спрос по каждой номенклатуре строки спецификации становится, в свою очередь, исходной точкой для дополнительного развертывания спроса. Этот сценарий сводного планирования включает следующие условия:

-   Аналитика площадки является обязательной и должна вводится по проводке запроса.
-   Аналитика площадки является непротиворечивой. Поэтому площадка для запросов нижних уровней - та же, что и площадка для первоначальной проводки запросов.

На следующей иллюстрации показан процесс развертывания спроса сводного планирования. ![Развертывание спроса с использованием версии спецификации](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a>Дополнительные ресурсы
--------

[Сводное планирование — определение версии спецификации](master-plan-bom-version-determined.md)

[Сводное планирование и функция работы с несколькими узлами](master-plan-multisite-functionality.md)




