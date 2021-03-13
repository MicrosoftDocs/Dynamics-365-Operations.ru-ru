---
title: Функциональные местоположения и активы
description: В этом разделе описываются функциональные местоположения и активы в «Управлении активами». «Управление активами» является передовым модулем для управления активами и заданиями обслуживания в Dynamics 365 Supply Chain Management.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f93a68f19b0b952eb2964b404bb957865c625cd
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018054"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="0aaf2-104">Функциональные местоположения и активы</span><span class="sxs-lookup"><span data-stu-id="0aaf2-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0aaf2-105">В этом разделе описываются функциональные местоположения и активы в «Управлении активами».</span><span class="sxs-lookup"><span data-stu-id="0aaf2-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="0aaf2-106">«Управление активами» является передовым модулем для управления активами и заданиями обслуживания в Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-106">Asset Management is an advanced module for managing assets and maintenance jobs in Dynamics 365 Supply Chain Management.</span></span>

## <a name="overview"></a><span data-ttu-id="0aaf2-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="0aaf2-107">Overview</span></span>

<span data-ttu-id="0aaf2-108">Управление активами полностью интегрировано с несколькими модулями с другими приложениями Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-108">Asset Management is integrated seamlessly with several modules with other Finance and Operations apps.</span></span> <span data-ttu-id="0aaf2-109">На следующем рисунке показаны интерфейсы с другими модулями.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-109">The following illustration shows the interfaces with other modules.</span></span>

![Диаграмма, показывающая как интерфейсы управления активами с другими модулями](media/01-overview-image.png)

<span data-ttu-id="0aaf2-111">«Управление активами» позволяет эффективно управлять и выполнять все задачи, связанные с управлением и обслуживанием многих типов оборудования в вашей компании.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="0aaf2-112">Это оборудование включает в себя машины, производственное оборудование и транспортные средства.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="0aaf2-113">«Управление активами» также поддерживает решения во многих отраслях промышленности.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="0aaf2-114">На следующем рисунке приведен обзор основных функций, охватываемых «Управлением активами».</span><span class="sxs-lookup"><span data-stu-id="0aaf2-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![Диаграмма, в которой показаны основные функции управления активами](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="0aaf2-116">Функциональные местоположения и активы</span><span class="sxs-lookup"><span data-stu-id="0aaf2-116">Functional locations and assets</span></span>

<span data-ttu-id="0aaf2-117">Функциональные местоположения используются для управления активами на местоположениях.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="0aaf2-118">Это управление включает отслеживание затрат на активы в функциональных местоположениях.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="0aaf2-119">Функциональные местоположения структурированы иерархически, и местоположения могут иметь вложенные местоположения.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="0aaf2-120">Структура функциональных местоположений статична.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-120">The structure of functional locations is static.</span></span> <span data-ttu-id="0aaf2-121">Другими словами, местоположения не могут измениться.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-121">In other words, locations can't change place.</span></span> <span data-ttu-id="0aaf2-122">Активы могут быть установлены в функциональных местоположениях и, при необходимости, могут быть установлены в других функциональных местоположениях позже.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="0aaf2-123">Стоимость активов всегда следует за местоположением актива.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="0aaf2-124">Другими словами, если вы устанавливаете актив в новом функциональном местоположении, актив автоматически использует финансовые аналитики, связанные с новым функциональным местоположением.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="0aaf2-125">Таким образом, затраты по активу всегда связаны с функциональным местоположением, в которое установлен актив на данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="0aaf2-126">Такая автоматическая обработка финансовых аналитик помогает гарантировать полное отслеживание затрат, когда ваша компания осуществляет контроль проектов и отчетность по функциональным местоположениям.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="0aaf2-127">Способ построения иерархии функциональных местоположений зависит от требований компании к обслуживанию внутреннего оборудования или обслуживанию оборудования для клиентов.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="0aaf2-128">На следующем рисунке показан пример функциональных местоположений, основанных на географических местоположениях.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![Диаграмма, показывающая функциональные местоположения на основе географических местоположений](media/03-overview-image.png)

<span data-ttu-id="0aaf2-130">На следующем рисунке показан пример функциональных местоположений, основанных на клиентах.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![Диаграмма, показывающая функциональные местоположения на основе клиентов](media/04-overview-image.png)
