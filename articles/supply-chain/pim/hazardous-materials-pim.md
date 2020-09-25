---
title: Опасные материалы
description: В этой теме приводятся сведения о документах для опасных материалов и информации, которая хранится в вашей среде.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 54e5dca38b31c9310d44bdda5f5af14ca1515541
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802709"
---
# <a name="hazardous-materials"></a><span data-ttu-id="a7bd3-103">Опасные материалы</span><span class="sxs-lookup"><span data-stu-id="a7bd3-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a7bd3-104">Сведения об опасных материалах настраиваются в разделе "Управление сведениями о продуктах".</span><span class="sxs-lookup"><span data-stu-id="a7bd3-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="a7bd3-105">Этот модуль также содержит документы, которые могут быть распечатаны в модуле управления складом.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="a7bd3-106">При отгрузке материалов, которые классифицируются как опасные, в отгрузку должны быть включены дополнительные документы.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="a7bd3-107">Функция опасных материалов позволяет клиентам хранить сведения классификации и связывать их с выпускаемым в производство номенклатурами.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="a7bd3-108">Эти сведения могут быть затем использованы для подготовки документации по отгрузке.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7bd3-109">Функции опасных материалов в Microsoft Dynamics 365 Supply Chain Management обеспечивают сбор полезных полей информации о продукте и соответствующих функций, которые могут помочь в записи и ссылке на информацию, относящуюся к опасным продуктам.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-109">The hazardous materials features in Microsoft Dynamics 365 Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="a7bd3-110">Эти функции могут также помочь при разработке и печати документов отгрузки, в которых содержится некоторая из одной и той же информации о каких-либо отгружаемых вами опасных материалах.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-110">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="a7bd3-111">Однако система не будет автоматически обеспечить ваше соответствия всем действующим нормативным требованиям в вашей стране или регионе.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-111">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="a7bd3-112">Хотя эти средства предназначены для того, чтобы помочь обеспечить соответствие обычным нормативным требованиям, они не являются достаточными сами по себе и не гарантируются как таковые.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-112">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="a7bd3-113">Ваша организация несет ответственность за знание всех действующих нормативных правил и за принятие всех необходимых мер для обеспечения соответствия им.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-113">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

<span data-ttu-id="a7bd3-114">Перед использованием этой функции необходимо выполнить следующие действия по настройке:</span><span class="sxs-lookup"><span data-stu-id="a7bd3-114">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="a7bd3-115">**Управление сведениями о продукте**: настройте коды, которые могут применяться к выпущенным продуктам.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-115">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="a7bd3-116">**Управление складом**: использование дополнительных документов отгрузки для печати сведений об отгрузке.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-116">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="a7bd3-117">Управление сведениями о продукте</span><span class="sxs-lookup"><span data-stu-id="a7bd3-117">Product information management</span></span>

<span data-ttu-id="a7bd3-118">В управлении сведениями о продукте имеется диапазон таблиц настройки, в которые можно добавлять справочные сведения, предоставляемые в списках опасных товаров для дорожной, воздушной и морской транспортировки.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-118">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="a7bd3-119">Вот некоторые примеры нормативных требований:</span><span class="sxs-lookup"><span data-stu-id="a7bd3-119">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="a7bd3-120">**ADR** — правила, которые относятся к международной перевозке опасных товаров по дорогам</span><span class="sxs-lookup"><span data-stu-id="a7bd3-120">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="a7bd3-121">**CFR 49** — правила в США для перевозки опасных товаров</span><span class="sxs-lookup"><span data-stu-id="a7bd3-121">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="a7bd3-122">**IMDG** — кодекс International Marine Dangerous Goods (IMDG)</span><span class="sxs-lookup"><span data-stu-id="a7bd3-122">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="a7bd3-123">**IATA** — правила для опасных товаров международной ассоциации воздушного транспорта (IATA)</span><span class="sxs-lookup"><span data-stu-id="a7bd3-123">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="a7bd3-124">Каждое из этих правил имеет список опасных товаров, содержащий справочные коды.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-124">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="a7bd3-125">Списки для каждого типа транспорта комбинируются в общих международных классификациях.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-125">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="a7bd3-126">Supply Chain Management содержит таблицу ссылок для общих кодов в этих списках.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-126">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="a7bd3-127">Каждый список также имеет уникальные коды, которые могут быть определены.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-127">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="a7bd3-128">Чтобы начать настройку этих сведений, создайте правило, которое можно использовать для настройки исходных параметров.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-128">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="a7bd3-129">Управление складом</span><span class="sxs-lookup"><span data-stu-id="a7bd3-129">Warehouse management</span></span>

<span data-ttu-id="a7bd3-130">Когда отгрузка подготовлена, можно напечатать несколько новых отчетов.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-130">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="a7bd3-131">В этих отчетах используются данные, настроенные в управлении сведениями о продуктах.</span><span class="sxs-lookup"><span data-stu-id="a7bd3-131">These reports use the information that you set up in Product information management.</span></span>
