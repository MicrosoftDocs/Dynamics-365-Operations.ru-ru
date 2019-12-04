---
title: Развертывание версии спецификации
description: В этой статье объясняется сценарий сводного планирования, который включает в себя развертывание версии спецификации (BOM).
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dbdfc169365cb73e13383b11efcd8983aef4bbca
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815326"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="2c44e-103">Развертывание версии спецификации</span><span class="sxs-lookup"><span data-stu-id="2c44e-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c44e-104">В этой статье объясняется сценарий сводного планирования, который включает в себя развертывание версии спецификации (BOM).</span><span class="sxs-lookup"><span data-stu-id="2c44e-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="2c44e-105">Развертывание спроса версии спецификаций приводит к созданию спроса по каждой номенклатуре строки спецификаций на определенном сайте и, возможно, на определенном складе.</span><span class="sxs-lookup"><span data-stu-id="2c44e-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="2c44e-106">Для спецификации сайта может быть определен конкретный склад для каждой строки спецификаций.</span><span class="sxs-lookup"><span data-stu-id="2c44e-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="2c44e-107">Кроме того, для каждой строки спецификаций настройки аналитики номенклатуры определяют, требуется ли склад.</span><span class="sxs-lookup"><span data-stu-id="2c44e-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="2c44e-108">Этот итоговый спрос по каждой номенклатуре строки спецификации становится, в свою очередь, исходной точкой для дополнительного развертывания спроса.</span><span class="sxs-lookup"><span data-stu-id="2c44e-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="2c44e-109">Этот сценарий сводного планирования включает следующие условия:</span><span class="sxs-lookup"><span data-stu-id="2c44e-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="2c44e-110">Аналитика площадки является обязательной и должна вводится по проводке запроса.</span><span class="sxs-lookup"><span data-stu-id="2c44e-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="2c44e-111">Аналитика площадки является непротиворечивой.</span><span class="sxs-lookup"><span data-stu-id="2c44e-111">The site dimension is consistent.</span></span> <span data-ttu-id="2c44e-112">Поэтому площадка для запросов нижних уровней - та же, что и площадка для первоначальной проводки запросов.</span><span class="sxs-lookup"><span data-stu-id="2c44e-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="2c44e-113">На следующей иллюстрации показан процесс развертывания спроса сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="2c44e-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Развертывание спроса с использованием версии спецификации](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="2c44e-115">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2c44e-115">Additional resources</span></span>
--------

[<span data-ttu-id="2c44e-116">Определение версии спецификации</span><span class="sxs-lookup"><span data-stu-id="2c44e-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="2c44e-117">Обзор сводного планирования и функции работы с несколькими узлами</span><span class="sxs-lookup"><span data-stu-id="2c44e-117">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)



