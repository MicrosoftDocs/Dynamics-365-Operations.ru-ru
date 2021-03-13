---
title: Обзор профилактического обслуживания
description: В этом разделе описываются профилактическое обслуживание в модуле "Управление активами".
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 36a70a3e60566fd8048ad404e0c391d898053a0a
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016736"
---
# <a name="preventive-maintenance-overview"></a><span data-ttu-id="88e10-103">Обзор профилактического обслуживания</span><span class="sxs-lookup"><span data-stu-id="88e10-103">Preventive maintenance overview</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="88e10-104">В этом разделе описываются профилактическое обслуживание в модуле "Управление активами".</span><span class="sxs-lookup"><span data-stu-id="88e10-104">This topic explains preventive maintenance in Asset Management.</span></span> <span data-ttu-id="88e10-105">Профилактическое обслуживание — это дисциплина, включающая запланированные задания обслуживания, например, регулярный сервис, калибровка и проверки.</span><span class="sxs-lookup"><span data-stu-id="88e10-105">Preventive maintenance is a discipline involving planned maintenance jobs, for example, regular service, calibration, and inspections.</span></span> <span data-ttu-id="88e10-106">В модуле **Управление активами** можно создавать планы обслуживания и настраивать их для активов и функциональных местоположений.</span><span class="sxs-lookup"><span data-stu-id="88e10-106">In **Asset Management**, you can create maintenance plans and set them up on assets and functional locations.</span></span> <span data-ttu-id="88e10-107">Можно также настроить циклы обслуживания для функциональных местоположений.</span><span class="sxs-lookup"><span data-stu-id="88e10-107">You can also set up maintenance rounds on functional locations.</span></span> <span data-ttu-id="88e10-108">Планы обслуживания в активах активны, независимо от того, где установлен актив.</span><span class="sxs-lookup"><span data-stu-id="88e10-108">Maintenance plans on assets are active regardless of where the asset is installed.</span></span> <span data-ttu-id="88e10-109">Планы обслуживания и циклы обслуживания в функциональных местоположениях активны для активов, установленных в данный момент в этом местоположении.</span><span class="sxs-lookup"><span data-stu-id="88e10-109">Maintenance plans and maintenance rounds on functional location are active for the assets currently installed at the location.</span></span> <span data-ttu-id="88e10-110">Вместо настройки планов обслуживания в активах или настройкой циклов обслуживания в функциональных местоположениях, можно создать циклы обслуживания, включающие несколько активов, для которых требуется выполнить соответствующие типы заданий обслуживания в одной и той же рабочей процедуре.</span><span class="sxs-lookup"><span data-stu-id="88e10-110">Instead of setting up maintenance plans on assets, or setting up maintenance rounds on functional locations, you can create maintenance rounds that include multiple assets on which you need to perform related types of maintenance jobs in the same work routine.</span></span> <span data-ttu-id="88e10-111">Циклы обслуживания, созданные из активов (вместо создания их в функциональных местоположениях) означают, что можно выбрать несколько активов для одного цикла обслуживания, которые не установлены в одном и том же функциональном местоположении.</span><span class="sxs-lookup"><span data-stu-id="88e10-111">Maintenance rounds created from assets - instead of created on functional locations - means that you can select a number of assets for one maintenance round, which are not installed on the same functional location.</span></span>

<span data-ttu-id="88e10-112">Планы обслуживания используются для профилактического и оперативного обслуживания отдельных активов.</span><span class="sxs-lookup"><span data-stu-id="88e10-112">Maintenance plans are used for preventive and reactive maintenance on individual assets.</span></span> <span data-ttu-id="88e10-113">Циклы обслуживания используются для профилактического обслуживания группы или набора активов.</span><span class="sxs-lookup"><span data-stu-id="88e10-113">Maintenance rounds are used for preventive maintenance on a group or a set of assets.</span></span> <span data-ttu-id="88e10-114">Планы обслуживания и циклы обслуживания используются для создания предложений по заказам на работу.</span><span class="sxs-lookup"><span data-stu-id="88e10-114">Maintenance plans and maintenance rounds are used for generating work order proposals.</span></span> <span data-ttu-id="88e10-115">Предложения по заказам на работу сохраняются как строки графика обслуживания, которые могут быть объединены и преобразованы в заказы на работу.</span><span class="sxs-lookup"><span data-stu-id="88e10-115">The work order proposals are saved as maintenance schedule lines, which can be bundled and converted into work orders.</span></span>

<span data-ttu-id="88e10-116">На следующей иллюстрации представлен обзор процесса от создания планов обслуживания и циклов обслуживания до создания заказов на работу для активов на основе этих планов обслуживания и циклов обслуживания.</span><span class="sxs-lookup"><span data-stu-id="88e10-116">The following illustration provides an overview of the work flow from creating maintenance plans and maintenance rounds to creating work orders for assets, based on those maintenance plans and maintenance rounds.</span></span>

![Рисунок 1](media/01-preventive-maintenance.png)

