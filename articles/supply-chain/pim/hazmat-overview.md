---
title: Обзор опасных материалов
description: В этой теме представлен обзор функций, которые относятся к обработке и документированию опасных материалов во время управления информацией о продуктах и управления складом.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: ff285e7e8bcdd2a3197f0ccae569ac880b796028
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007599"
---
# <a name="hazardous-materials-overview"></a><span data-ttu-id="fa967-103">Обзор опасных материалов</span><span class="sxs-lookup"><span data-stu-id="fa967-103">Hazardous materials overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="fa967-104">Для поддержания соответствия требованиям к отгрузке и транспортировке организации, которые отгружают материалы, классифицированные как опасные товары, должны включить в их отгрузку дополнительные бумажные документы.</span><span class="sxs-lookup"><span data-stu-id="fa967-104">To remain compliant with shipping and transport regulations, organizations that ship materials that are classified as dangerous goods must include additional paperwork with their shipments.</span></span> <span data-ttu-id="fa967-105">Функция опасных материалов позволяет клиентам хранить сведения, имеющие отношение к выпущенным номенклатурам.</span><span class="sxs-lookup"><span data-stu-id="fa967-105">The hazardous materials feature lets customers store information that is related to released items.</span></span> <span data-ttu-id="fa967-106">Эти сведения могут быть затем использованы для подготовки документации по отгрузке.</span><span class="sxs-lookup"><span data-stu-id="fa967-106">This information can then be used to help prepare shipping documentation.</span></span> <span data-ttu-id="fa967-107">Организация, которая отправляет опасные товары, должна иметь собственные процессы и процедуры для управления процессом отгрузки.</span><span class="sxs-lookup"><span data-stu-id="fa967-107">An organization that ships dangerous goods must have its own processes and procedures for managing the shipping process.</span></span> <span data-ttu-id="fa967-108">Microsoft Dynamics 365 Supply Chain Management — это просто инструмент, который может помочь в создании необходимых документов.</span><span class="sxs-lookup"><span data-stu-id="fa967-108">Microsoft Dynamics 365 Supply Chain Management is just a tool that can help generate the required documents.</span></span>

<span data-ttu-id="fa967-109">На следующей схеме показаны шаги, необходимые для настройки и использования функции опасных материалов.</span><span class="sxs-lookup"><span data-stu-id="fa967-109">The following diagram illustrates the steps needed to set up and use the hazardous materials feature.</span></span>

<span data-ttu-id="fa967-110">![Настройка и использование функции опасных материалов](media/hazmat-overview.png "Настройка и использование функции опасных материалов")</span><span class="sxs-lookup"><span data-stu-id="fa967-110">![Setup and use of the hazardous materials feature](media/hazmat-overview.png "Setup and use of the hazardous materials feature")</span></span>

<span data-ttu-id="fa967-111">Функция опасных материалов настраивается в модуле "Управление сведениями о продукте" и содержит документы, которые могут быть распечатаны в модуле "Управление складом".</span><span class="sxs-lookup"><span data-stu-id="fa967-111">The hazardous materials feature is set up in Product information management and provides documents that can be printed through Warehouse management.</span></span> <span data-ttu-id="fa967-112">Таким образом, эти области в широком смысле являются двумя основными областями, в которых вы будете просматривать, настраивать и использовать функциональность этой функции:</span><span class="sxs-lookup"><span data-stu-id="fa967-112">Therefore, broadly speaking, those areas are the two main areas where you will review, set up, and use this feature's functionality:</span></span>

- <span data-ttu-id="fa967-113">**Управление сведениями о продукте** — настройте коды, которые будут применяться к выпущенному продукту.</span><span class="sxs-lookup"><span data-stu-id="fa967-113">**Product information management** – Set up the codes that will be applied to a released product.</span></span>
- <span data-ttu-id="fa967-114">**Управление складом** — работа с дополнительными документами по отгрузке, которые будут распечатаны для отгрузок.</span><span class="sxs-lookup"><span data-stu-id="fa967-114">**Warehouse management** – Work with additional shipping documents that will be printed for shipments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa967-115">Функции опасных материалов в Supply Chain Management обеспечивают сбор полезных полей информации о продукте и соответствующих функций, которые могут помочь в записи и ссылке на информацию, относящуюся к опасным продуктам.</span><span class="sxs-lookup"><span data-stu-id="fa967-115">The hazardous materials features in Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="fa967-116">Эти функции могут также помочь при разработке и печати документов отгрузки, в которых содержится некоторая из одной и той же информации о каких-либо отгружаемых вами опасных материалах.</span><span class="sxs-lookup"><span data-stu-id="fa967-116">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="fa967-117">Однако система не будет автоматически обеспечить ваше соответствия всем действующим нормативным требованиям в вашей стране или регионе.</span><span class="sxs-lookup"><span data-stu-id="fa967-117">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="fa967-118">Хотя эти средства предназначены для того, чтобы помочь обеспечить соответствие обычным нормативным требованиям, они не являются достаточными сами по себе и не гарантируются как таковые.</span><span class="sxs-lookup"><span data-stu-id="fa967-118">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="fa967-119">Ваша организация несет ответственность за знание всех действующих нормативных правил и за принятие всех необходимых мер для обеспечения соответствия им.</span><span class="sxs-lookup"><span data-stu-id="fa967-119">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="fa967-120">Управление сведениями о продукте</span><span class="sxs-lookup"><span data-stu-id="fa967-120">Product information management</span></span>

<span data-ttu-id="fa967-121">В управлении сведениями о продукте предоставляется диапазон таблиц настройки, в которые можно ввести справочные сведения для различных списков опасных товаров для дорожной, воздушной и морской транспортировки.</span><span class="sxs-lookup"><span data-stu-id="fa967-121">Product information management provides a range of setup tables where you can enter reference information for the various dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="fa967-122">При развертывании этой функциональности были упомянуты следующие общие нормативные правила:</span><span class="sxs-lookup"><span data-stu-id="fa967-122">The following common regulations were referenced when this functionality was developed:</span></span>

- <span data-ttu-id="fa967-123">**ADR** — правила, которые относятся к международной перевозке опасных товаров по дорогам</span><span class="sxs-lookup"><span data-stu-id="fa967-123">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="fa967-124">**CFR 49** — правила в США для перевозки опасных товаров</span><span class="sxs-lookup"><span data-stu-id="fa967-124">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="fa967-125">**IMDG** — кодекс International Marine Dangerous Goods (IMDG)</span><span class="sxs-lookup"><span data-stu-id="fa967-125">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="fa967-126">**IATA** — правила для опасных товаров международной ассоциации воздушного транспорта (IATA)</span><span class="sxs-lookup"><span data-stu-id="fa967-126">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="fa967-127">Каждый набор нормативных правил содержит стандартизированные списки опасных товаров и справочных кодов.</span><span class="sxs-lookup"><span data-stu-id="fa967-127">Each set of regulations provides standardized lists of dangerous goods and reference codes.</span></span> <span data-ttu-id="fa967-128">Поэтому, Supply Chain Management содержит таблицу ссылок для общих кодов в этих списках.</span><span class="sxs-lookup"><span data-stu-id="fa967-128">Therefore, Supply Chain Management provides a reference table for the common codes on those lists.</span></span> <span data-ttu-id="fa967-129">Каждый список также имеет уникальные коды, которые вы можете определить.</span><span class="sxs-lookup"><span data-stu-id="fa967-129">Each list also has some unique codes that you can define.</span></span>

<span data-ttu-id="fa967-130">Дополнительные сведения о настройке нормативных правил и значений для опасных материалов и порядке назначения значений соответствующим продуктам см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="fa967-130">For more information about how to set up regulations and values for hazardous materials, and how to assign the values to relevant products, see the following topics:</span></span>

- [<span data-ttu-id="fa967-131">Настройка опасных материалов</span><span class="sxs-lookup"><span data-stu-id="fa967-131">Set up hazardous materials</span></span>](hazmat-setup.md)
- [<span data-ttu-id="fa967-132">Опасные материалы в продуктах, заказах, отгрузках и загрузках</span><span class="sxs-lookup"><span data-stu-id="fa967-132">Hazardous materials in products, orders, shipments, and loads</span></span>](hazmat-items.md)

## <a name="warehouse-management"></a><span data-ttu-id="fa967-133">Управление складом</span><span class="sxs-lookup"><span data-stu-id="fa967-133">Warehouse management</span></span>

<span data-ttu-id="fa967-134">При подготовке отгрузки в модуле управления складом вы сможете напечатать несколько новых отчетов, использующих данные, настроенные в управлении сведениями о продуктах.</span><span class="sxs-lookup"><span data-stu-id="fa967-134">When you prepare a shipment in Warehouse management, you will be able to print several new reports that use the information that you set up in Product information management.</span></span> <span data-ttu-id="fa967-135">Дополнительные сведения о доступных отчетах и их использовании см. в разделе [Запросы и отчеты по опасным материалам](hazmat-reports.md).</span><span class="sxs-lookup"><span data-stu-id="fa967-135">For more information about the available reports and how to use them, see [Hazardous materials inquiries and reports](hazmat-reports.md).</span></span>
