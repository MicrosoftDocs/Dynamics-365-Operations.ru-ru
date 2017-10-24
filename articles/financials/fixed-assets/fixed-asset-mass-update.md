---
title: "Массовое обновление основных средств"
description: "При использовании книг можно изменить соглашения по амортизации для группы активов, являющейся частью одной и той же книги."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3521
ms.assetid: 50207ffb-6b89-4fb9-92e9-928bc0729489
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c04997ccc29182f0f403af0e4ad5f039dbd4ae60
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="fixed-asset-mass-update"></a><span data-ttu-id="d6fd0-103">Массовое обновление основных средств</span><span class="sxs-lookup"><span data-stu-id="d6fd0-103">Fixed asset mass update</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d6fd0-104">При использовании книг можно изменить соглашения по амортизации для группы активов, являющейся частью одной и той же книги.</span><span class="sxs-lookup"><span data-stu-id="d6fd0-104">If you use books, you can change the depreciation conventions for groups of assets that are part of the same book.</span></span>

<span data-ttu-id="d6fd0-105">Например, если вы находитесь в Соединенных Штатах и в течение четвертого квартала ввели в эксплуатацию более 40 процентов своих основных средств, то необходимо использовать соглашение по амортизации для середины квартала.</span><span class="sxs-lookup"><span data-stu-id="d6fd0-105">For example, if you are in the United States, and you put more than 40 percent of your assets in service during the fourth quarter of the year, you must use the mid-quarter depreciation convention.</span></span> <span data-ttu-id="d6fd0-106">Можно использовать процесс массового обновления, чтобы внести изменения для всех активов, которым требуется новое соглашение по амортизации</span><span class="sxs-lookup"><span data-stu-id="d6fd0-106">You can use the process for a mass update to change all assets that require the new depreciation convention.</span></span> 

<span data-ttu-id="d6fd0-107">При обновлении соглашения по амортизации активов происходит удаление все проводок по амортизации, существующих для этих активов.</span><span class="sxs-lookup"><span data-stu-id="d6fd0-107">When you update the depreciation convention for assets, you delete all depreciation transactions that exist for those assets.</span></span> <span data-ttu-id="d6fd0-108">Также удаляются все проводки корректировок амортизации, проводки амортизационных премий и проводки дополнительной амортизации для этих активов.</span><span class="sxs-lookup"><span data-stu-id="d6fd0-108">You also delete all transactions for depreciation adjustments, transactions for bonus depreciation, and transactions for extraordinary depreciation for those assets.</span></span> 

<span data-ttu-id="d6fd0-109">Чтобы обновить соглашение по амортизации для активов, которые уже были списаны, необходимо сначала удалить существующие проводки выбытия, включая проводки, созданные по причине выполнения процесса списания.</span><span class="sxs-lookup"><span data-stu-id="d6fd0-109">To update the depreciation convention for assets that have already been disposed of, you must first delete the existing disposal transactions.</span></span> <span data-ttu-id="d6fd0-110">Также необходимо удалить все проводки, которые были созданы по причине выполнения процесса списания.</span><span class="sxs-lookup"><span data-stu-id="d6fd0-110">You must also delete all transactions that were generated because of the disposal process.</span></span> 

<span data-ttu-id="d6fd0-111">После обновления соглашения по амортизации для активов можно выполнить обработку амортизации и дополнительной амортизации для каждого актива.</span><span class="sxs-lookup"><span data-stu-id="d6fd0-111">After you update the depreciation convention for assets, you can process depreciation and extraordinary depreciation for each asset.</span></span> <span data-ttu-id="d6fd0-112">Если это необходимо, можно выполнить корректировки амортизации вручную.</span><span class="sxs-lookup"><span data-stu-id="d6fd0-112">You can also make manual depreciation adjustments, if any adjustments are required.</span></span>






