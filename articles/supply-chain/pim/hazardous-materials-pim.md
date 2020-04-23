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
ms.openlocfilehash: 5006f06d90ddcc314a51878e9e21337de7d493e7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208477"
---
# <a name="hazardous-materials"></a><span data-ttu-id="a9f12-103">Опасные материалы</span><span class="sxs-lookup"><span data-stu-id="a9f12-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9f12-104">Сведения об опасных материалах настраиваются в разделе "Управление сведениями о продуктах".</span><span class="sxs-lookup"><span data-stu-id="a9f12-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="a9f12-105">Этот модуль также содержит документы, которые могут быть распечатаны в модуле управления складом.</span><span class="sxs-lookup"><span data-stu-id="a9f12-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="a9f12-106">При отгрузке материалов, которые классифицируются как опасные, в отгрузку должны быть включены дополнительные документы.</span><span class="sxs-lookup"><span data-stu-id="a9f12-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="a9f12-107">Функция опасных материалов позволяет клиентам хранить сведения классификации и связывать их с выпускаемым в производство номенклатурами.</span><span class="sxs-lookup"><span data-stu-id="a9f12-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="a9f12-108">Эти сведения могут быть затем использованы для подготовки документации по отгрузке.</span><span class="sxs-lookup"><span data-stu-id="a9f12-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9f12-109">Чтобы помочь в управлении отгрузкой опасных товаров, Microsoft Dynamics 365 Supply Chain Management предоставляет дополнительные справочные сведения, которые относятся к продуктам.</span><span class="sxs-lookup"><span data-stu-id="a9f12-109">To help manage shipments of dangerous goods, Microsoft Dynamics 365 Supply Chain Management lets you set up additional reference information that is related to products.</span></span> <span data-ttu-id="a9f12-110">Можно также настроить дополнительные документы отгрузки.</span><span class="sxs-lookup"><span data-stu-id="a9f12-110">You can also set up additional shipment documents.</span></span> <span data-ttu-id="a9f12-111">Однако система необязательно соответствует нормативным требованиям вашей страны или региона.</span><span class="sxs-lookup"><span data-stu-id="a9f12-111">However, the system isn't automatically compliant with your country's or region's regulations.</span></span> <span data-ttu-id="a9f12-112">Вместо этого инструмент может помочь вашей общей программе.</span><span class="sxs-lookup"><span data-stu-id="a9f12-112">Instead, it's a tool that can help your overall program.</span></span>

<span data-ttu-id="a9f12-113">Перед использованием этой функции необходимо выполнить следующие действия по настройке:</span><span class="sxs-lookup"><span data-stu-id="a9f12-113">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="a9f12-114">**Управление сведениями о продукте**: настройте коды, которые могут применяться к выпущенным продуктам.</span><span class="sxs-lookup"><span data-stu-id="a9f12-114">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="a9f12-115">**Управление складом**: использование дополнительных документов отгрузки для печати сведений об отгрузке.</span><span class="sxs-lookup"><span data-stu-id="a9f12-115">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="a9f12-116">Управление сведениями о продукте</span><span class="sxs-lookup"><span data-stu-id="a9f12-116">Product information management</span></span>

<span data-ttu-id="a9f12-117">В управлении сведениями о продукте имеется диапазон таблиц настройки, в которые можно добавлять справочные сведения, предоставляемые в списках опасных товаров для дорожной, воздушной и морской транспортировки.</span><span class="sxs-lookup"><span data-stu-id="a9f12-117">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="a9f12-118">Вот некоторые примеры нормативных требований:</span><span class="sxs-lookup"><span data-stu-id="a9f12-118">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="a9f12-119">**ADR** — правила, которые относятся к международной перевозке опасных товаров по дорогам</span><span class="sxs-lookup"><span data-stu-id="a9f12-119">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="a9f12-120">**CFR 49** — правила в США для перевозки опасных товаров</span><span class="sxs-lookup"><span data-stu-id="a9f12-120">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="a9f12-121">**IMDG** — кодекс International Marine Dangerous Goods (IMDG)</span><span class="sxs-lookup"><span data-stu-id="a9f12-121">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="a9f12-122">**IATA** — правила для опасных товаров международной ассоциации воздушного транспорта (IATA)</span><span class="sxs-lookup"><span data-stu-id="a9f12-122">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="a9f12-123">Каждое из этих правил имеет список опасных товаров, содержащий справочные коды.</span><span class="sxs-lookup"><span data-stu-id="a9f12-123">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="a9f12-124">Списки для каждого типа транспорта комбинируются в общих международных классификациях.</span><span class="sxs-lookup"><span data-stu-id="a9f12-124">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="a9f12-125">Supply Chain Management содержит таблицу ссылок для общих кодов в этих списках.</span><span class="sxs-lookup"><span data-stu-id="a9f12-125">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="a9f12-126">Каждый список также имеет уникальные коды, которые могут быть определены.</span><span class="sxs-lookup"><span data-stu-id="a9f12-126">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="a9f12-127">Чтобы начать настройку этих сведений, создайте правило, которое можно использовать для настройки исходных параметров.</span><span class="sxs-lookup"><span data-stu-id="a9f12-127">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="a9f12-128">Управление складом</span><span class="sxs-lookup"><span data-stu-id="a9f12-128">Warehouse management</span></span>

<span data-ttu-id="a9f12-129">Когда отгрузка подготовлена, можно напечатать несколько новых отчетов.</span><span class="sxs-lookup"><span data-stu-id="a9f12-129">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="a9f12-130">В этих отчетах используются данные, настроенные в управлении сведениями о продуктах.</span><span class="sxs-lookup"><span data-stu-id="a9f12-130">These reports use the information that you set up in Product information management.</span></span>
