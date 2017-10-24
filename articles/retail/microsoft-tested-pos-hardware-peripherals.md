---
title: "Периферийное POS-оборудование"
description: "Retail Modern POS и Cloud POS могут использовать широкий диапазон периферийных POS-устройств с несколькими интерфейсами и параметрами развертывания для охвата различных бизнес-сценариев в розничной торговле."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 215234
ms.assetid: 1893d4b3-e1b7-4b66-be58-0102addd5b36
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 17738e794f18fddc7320b1b40ef55376fba0de24
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="pos-hardware-peripherals"></a><span data-ttu-id="a09f3-103">Периферийное POS-оборудование</span><span class="sxs-lookup"><span data-stu-id="a09f3-103">POS hardware peripherals</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a09f3-104">Retail Modern POS и Cloud POS могут использовать широкий диапазон периферийных POS-устройств с несколькими интерфейсами и параметрами развертывания для охвата различных бизнес-сценариев в розничной торговле.</span><span class="sxs-lookup"><span data-stu-id="a09f3-104">Retail Modern point of sale (POS) and Cloud POS can utilize a wide range of POS hardware peripherals, with multiple interfaces and deployment options to achieve a retailer’s various business scenarios.</span></span> 

<span data-ttu-id="a09f3-105">Для поддержки самого широкого выбора устройств разных производителей и моделей POS использует стандартные интерфейсы, такие как OLE for Retail POS (OPOS), драйверы устройств Windows и интерфейсы прикладного программирования POS Windows.</span><span class="sxs-lookup"><span data-stu-id="a09f3-105">To support the widest selection of devices across manufactures and models, POS utilizes standard interfaces such as OLE for Retail POS (OPOS), Windows device drivers, and Windows point of service application program interfaces (APIs).</span></span> <span data-ttu-id="a09f3-106">Обычно POS будет работать на этих устройствах при условии наличия соответствующего драйвера.</span><span class="sxs-lookup"><span data-stu-id="a09f3-106">Generally, POS will work on these devices provided that the appropriate driver is supplied.</span></span> <span data-ttu-id="a09f3-107">Однако, поскольку реализации этих стандартов у каждого производителя и разработчика ПО могут отличаться, поддерживаемые возможности и поведение часто различаются.</span><span class="sxs-lookup"><span data-stu-id="a09f3-107">However, because each manufacturer and software developer’s implementation of these standards can vary, there are often differences in supported capabilities or behaviors.</span></span>

<span data-ttu-id="a09f3-108">Следующий список включает модели устройств в каждом классе, которые были проверены в корпорации Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a09f3-108">The following list includes device models, in each class, that have been tested internally by Microsoft.</span></span>

<span data-ttu-id="a09f3-109">**устройства OPOS**</span><span class="sxs-lookup"><span data-stu-id="a09f3-109">**OPOS devices**</span></span>

-   <span data-ttu-id="a09f3-110">Штрих-код — Motorola DS9208</span><span class="sxs-lookup"><span data-stu-id="a09f3-110">Barcode – Motorola DS9208</span></span>
-   <span data-ttu-id="a09f3-111">MSR — HP IDRA-334133, Magtek PN — 21073062</span><span class="sxs-lookup"><span data-stu-id="a09f3-111">MSR – HP IDRA-334133, Magtek PN - 21073062</span></span>
-   <span data-ttu-id="a09f3-112">LineDisplay — Epson M58DC</span><span class="sxs-lookup"><span data-stu-id="a09f3-112">LineDisplay – Epson M58DC</span></span>
-   <span data-ttu-id="a09f3-113">Панель для ввода PIN-кода — Verifone 1000SE</span><span class="sxs-lookup"><span data-stu-id="a09f3-113">Pinpad – Verifone 1000SE</span></span>
-   <span data-ttu-id="a09f3-114">Электронный идентификатор подписи — Scriptel ST1550</span><span class="sxs-lookup"><span data-stu-id="a09f3-114">Signature pad – Scriptel ST1550</span></span>
-   <span data-ttu-id="a09f3-115">Принтер — EPSON TM-T88IV, TMT88V</span><span class="sxs-lookup"><span data-stu-id="a09f3-115">Printer – EPSON TM-T88IV, TMT88V</span></span>
-   <span data-ttu-id="a09f3-116">Кассовый лоток — Star SMD2-1317BK44</span><span class="sxs-lookup"><span data-stu-id="a09f3-116">Cash drawer – Star SMD2-1317BK44</span></span>
-   <span data-ttu-id="a09f3-117">Весы — Datalogic Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="a09f3-117">Scale – Datalogic Magellan 8400</span></span>

<span data-ttu-id="a09f3-118">**MSR с электронным соединителем клавиатуры**</span><span class="sxs-lookup"><span data-stu-id="a09f3-118">**Keyboard wedge MSR**</span></span>

-   <span data-ttu-id="a09f3-119">Magtek USB</span><span class="sxs-lookup"><span data-stu-id="a09f3-119">Magtek USB</span></span>

<span data-ttu-id="a09f3-120">**Платежный терминал**</span><span class="sxs-lookup"><span data-stu-id="a09f3-120">**Payment terminal**</span></span>

-   <span data-ttu-id="a09f3-121">Equinox L3500</span><span class="sxs-lookup"><span data-stu-id="a09f3-121">Equinox L3500</span></span>
-   <span data-ttu-id="a09f3-122">Verifone MX925</span><span class="sxs-lookup"><span data-stu-id="a09f3-122">Verifone MX925</span></span>

<span data-ttu-id="a09f3-123">**Сетевые устройства**</span><span class="sxs-lookup"><span data-stu-id="a09f3-123">**Network devices**</span></span>

-   <span data-ttu-id="a09f3-124">Принтер — Star TSP650II</span><span class="sxs-lookup"><span data-stu-id="a09f3-124">Printer – Star TSP650II</span></span>
-   <span data-ttu-id="a09f3-125">Кассовый лоток — APG Atwood</span><span class="sxs-lookup"><span data-stu-id="a09f3-125">Cash drawer – APG Atwood</span></span>
-   <span data-ttu-id="a09f3-126">Платежный терминал – MX915, MX925</span><span class="sxs-lookup"><span data-stu-id="a09f3-126">Payment terminal – MX915, MX925</span></span>

<span data-ttu-id="a09f3-127">**Только MPOS direct IPC**</span><span class="sxs-lookup"><span data-stu-id="a09f3-127">**MPOS direct IPC only**</span></span>

-   <span data-ttu-id="a09f3-128">Штрих-код — Honeywell 1900, HP LS2208</span><span class="sxs-lookup"><span data-stu-id="a09f3-128">Barcode – Honeywell 1900, HP LS2208</span></span>
-   <span data-ttu-id="a09f3-129">MSR — Magtek PN — 21073075</span><span class="sxs-lookup"><span data-stu-id="a09f3-129">MSR – Magtek PN - 21073075</span></span>





