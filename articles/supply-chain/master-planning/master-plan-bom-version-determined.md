---
title: Определение версии спецификации
description: Во время развертывания спроса, если номенклатура имеет тип заказа по умолчанию со значением "Производство", механизм планирования ищет допустимую версию спецификации, основанную на узле.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d4fd5f28d0ee85c267ea6a86a1452fbacc824620
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833625"
---
# <a name="determine-the-bom-version"></a><span data-ttu-id="202d9-103">Определение версии спецификации</span><span class="sxs-lookup"><span data-stu-id="202d9-103">Determine the BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="202d9-104">Во время развертывания спроса, если номенклатура имеет тип заказа по умолчанию со значением "Производство", механизм планирования ищет допустимую версию спецификации, основанную на узле.</span><span class="sxs-lookup"><span data-stu-id="202d9-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="202d9-105">Аналитика сайта уже известна и указана в проводке по спросу.</span><span class="sxs-lookup"><span data-stu-id="202d9-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="202d9-106">Для определения версии спецификации для использования применяется следующий процесс.</span><span class="sxs-lookup"><span data-stu-id="202d9-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="202d9-107">Если для номенклатуры определена версия спецификации на узле спроса, программа использует эту зависящую от узла спецификацию.</span><span class="sxs-lookup"><span data-stu-id="202d9-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="202d9-108">Если для номенклатуры не определена версия спецификации на узле спроса, используется общая спецификация.</span><span class="sxs-lookup"><span data-stu-id="202d9-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="202d9-109">Общая спецификация не указывает узел и справедлива для нескольких узлов.</span><span class="sxs-lookup"><span data-stu-id="202d9-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="202d9-110">Если общая спецификация существует, она будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="202d9-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="202d9-111">Если отсутствует общая версия спецификации для использования, развертывание требования останавливается в этой точке.</span><span class="sxs-lookup"><span data-stu-id="202d9-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="202d9-112">Допустимая версия спецификации, зависящей от узла или общей, должна удовлетворять требуемым критериям на дату и количество.</span><span class="sxs-lookup"><span data-stu-id="202d9-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]