---
title: Настройка сведений об отгрузке
description: В этой теме описывается, как настроить информацию отгрузки для модуля "Стоимость на складе".
author: sherry-zheng
manager: tfehr
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 90794a154eb2a63f33277383cda80323dafd77b0
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500942"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="9567f-103">Настройка сведений об отгрузке</span><span class="sxs-lookup"><span data-stu-id="9567f-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="9567f-104">В этой теме описывается, как настроить информацию отгрузки для модуля **Стоимость на складе**.</span><span class="sxs-lookup"><span data-stu-id="9567f-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="9567f-105">Описание товаров</span><span class="sxs-lookup"><span data-stu-id="9567f-105">Description of goods</span></span>

<span data-ttu-id="9567f-106">Описания товаров помогают идентифицировать рейс, контейнер отгрузки или лист товаров, а также товары в нем.</span><span class="sxs-lookup"><span data-stu-id="9567f-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="9567f-107">Можно выбрать описание товаров в заголовке контейнера отгрузки или в заголовке листа.</span><span class="sxs-lookup"><span data-stu-id="9567f-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="9567f-108">Для работы с описаниями товаров перейдите **Стоимость на складе \> Настройка информации об отгрузке \> Описание товаров**.</span><span class="sxs-lookup"><span data-stu-id="9567f-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="9567f-109">Там можно просматривать, открывать, создавать и удалять записи для описаний товаров.</span><span class="sxs-lookup"><span data-stu-id="9567f-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="9567f-110">В следующей таблице описываются поля, которые доступны для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="9567f-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="9567f-111">Поле</span><span class="sxs-lookup"><span data-stu-id="9567f-111">Field</span></span> | <span data-ttu-id="9567f-112">описание</span><span class="sxs-lookup"><span data-stu-id="9567f-112">Description</span></span> |
|---|---|
| <span data-ttu-id="9567f-113">Описание товаров</span><span class="sxs-lookup"><span data-stu-id="9567f-113">Description of goods</span></span> | <span data-ttu-id="9567f-114">Введите уникальный идентификационное имя/номер для типа товаров, которые будут использовать это описание.</span><span class="sxs-lookup"><span data-stu-id="9567f-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="9567f-115">описание</span><span class="sxs-lookup"><span data-stu-id="9567f-115">Description</span></span> | <span data-ttu-id="9567f-116">Введите описание типа товаров в этой категории.</span><span class="sxs-lookup"><span data-stu-id="9567f-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="9567f-117">Суда</span><span class="sxs-lookup"><span data-stu-id="9567f-117">Vessels</span></span>

<span data-ttu-id="9567f-118">Судно — это уникальное имя судна или транспортного средства, которое используется транспортной компанией или агентством.</span><span class="sxs-lookup"><span data-stu-id="9567f-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="9567f-119">При создании рейса следует всегда выбрать или ввести для него судно.</span><span class="sxs-lookup"><span data-stu-id="9567f-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="9567f-120">Если часто используется одни и те же суда, то можно ускорить и упростить создание нового рейса путем создания записи судна для каждого из них, тем самым позволяя пользователям выбирать судно из списка, а не вводить имя или номер вручную каждый раз.</span><span class="sxs-lookup"><span data-stu-id="9567f-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="9567f-121">Для работы с судами отгрузки перейдите **Стоимость на складе \> Настройка информации об отгрузке \> Суда**.</span><span class="sxs-lookup"><span data-stu-id="9567f-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="9567f-122">Там можно просматривать, открывать, создавать и удалять записи для судов.</span><span class="sxs-lookup"><span data-stu-id="9567f-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="9567f-123">В следующей таблице описываются поля, которые доступны для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="9567f-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="9567f-124">Поле</span><span class="sxs-lookup"><span data-stu-id="9567f-124">Field</span></span> | <span data-ttu-id="9567f-125">описание</span><span class="sxs-lookup"><span data-stu-id="9567f-125">Description</span></span> |
|---|---|
| <span data-ttu-id="9567f-126">Судно</span><span class="sxs-lookup"><span data-stu-id="9567f-126">Vessel</span></span> | <span data-ttu-id="9567f-127">Введите уникальное идентификационное имя/номер для судна, которое будет использоваться для транспортировки товаров в рейсе.</span><span class="sxs-lookup"><span data-stu-id="9567f-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="9567f-128">описание</span><span class="sxs-lookup"><span data-stu-id="9567f-128">Description</span></span> | <span data-ttu-id="9567f-129">Введите описание судна.</span><span class="sxs-lookup"><span data-stu-id="9567f-129">Enter a description of the vessel.</span></span> <span data-ttu-id="9567f-130">Обычно это описание определяет название судна и транспортной компании/агента.</span><span class="sxs-lookup"><span data-stu-id="9567f-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="9567f-131">Способ поставки</span><span class="sxs-lookup"><span data-stu-id="9567f-131">Mode of delivery</span></span> | <span data-ttu-id="9567f-132">Выберите способа поставки, используемый транспортным средством (например, _воздух_, _океан_ или _поезд_).</span><span class="sxs-lookup"><span data-stu-id="9567f-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="9567f-133">Экспортеры</span><span class="sxs-lookup"><span data-stu-id="9567f-133">Exporters</span></span>

<span data-ttu-id="9567f-134">Каждая запись экспортера определяет поставщика или экспортера, который может быть определен в качестве поставщика для рейса.</span><span class="sxs-lookup"><span data-stu-id="9567f-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="9567f-135">Экспортер может быть связан с рейсом и использоваться для отчетности.</span><span class="sxs-lookup"><span data-stu-id="9567f-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="9567f-136">Для работы с экспортерами перейдите **Стоимость на складе \> Настройка информации об отгрузке \> Экспортеры**.</span><span class="sxs-lookup"><span data-stu-id="9567f-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="9567f-137">Там можно просматривать, открывать, создавать и удалять записи для экспортеров.</span><span class="sxs-lookup"><span data-stu-id="9567f-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="9567f-138">В следующей таблице описываются поля, которые доступны для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="9567f-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="9567f-139">Поле</span><span class="sxs-lookup"><span data-stu-id="9567f-139">Field</span></span> | <span data-ttu-id="9567f-140">описание</span><span class="sxs-lookup"><span data-stu-id="9567f-140">Description</span></span> |
|---|---|
| <span data-ttu-id="9567f-141">Экспортер</span><span class="sxs-lookup"><span data-stu-id="9567f-141">Exporter</span></span> | <span data-ttu-id="9567f-142">Введите уникальное идентификационное имя/номер для экспортера товаров, которые будут транспортироваться в рейсе.</span><span class="sxs-lookup"><span data-stu-id="9567f-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="9567f-143">описание</span><span class="sxs-lookup"><span data-stu-id="9567f-143">Description</span></span> | <span data-ttu-id="9567f-144">Введите описание экспортера.</span><span class="sxs-lookup"><span data-stu-id="9567f-144">Enter a description of the exporter.</span></span> <span data-ttu-id="9567f-145">Обычно это описание определяет полное название транспортной компании/агента.</span><span class="sxs-lookup"><span data-stu-id="9567f-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="9567f-146">Товарные коды</span><span class="sxs-lookup"><span data-stu-id="9567f-146">Commodity codes</span></span>

<span data-ttu-id="9567f-147">Товарные коды используются для помощи в идентификации таможенных процедур и расчете ставок пошлин для товаров в рейсе.</span><span class="sxs-lookup"><span data-stu-id="9567f-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="9567f-148">Можно выбрать товарные коды на странице **Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="9567f-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="9567f-149">Для работы с товарными кодами перейдите **Стоимость на складе \> Настройка сведений об отгрузке \> Товарные коды**.</span><span class="sxs-lookup"><span data-stu-id="9567f-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="9567f-150">Там можно просматривать, открывать, создавать и удалять записи для товарных кодов.</span><span class="sxs-lookup"><span data-stu-id="9567f-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="9567f-151">В следующей таблице описываются поля, которые доступны для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="9567f-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="9567f-152">Поле</span><span class="sxs-lookup"><span data-stu-id="9567f-152">Field</span></span> | <span data-ttu-id="9567f-153">описание</span><span class="sxs-lookup"><span data-stu-id="9567f-153">Description</span></span> |
|---|---|
| <span data-ttu-id="9567f-154">Товарный код</span><span class="sxs-lookup"><span data-stu-id="9567f-154">Commodity code</span></span> | <span data-ttu-id="9567f-155">Введите уникальный код для данного типа товара.</span><span class="sxs-lookup"><span data-stu-id="9567f-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="9567f-156">описание</span><span class="sxs-lookup"><span data-stu-id="9567f-156">Description</span></span> | <span data-ttu-id="9567f-157">Введите описание кода типа товара.</span><span class="sxs-lookup"><span data-stu-id="9567f-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="9567f-158">Таможенное описание</span><span class="sxs-lookup"><span data-stu-id="9567f-158">Customs description</span></span>

<span data-ttu-id="9567f-159">Таможенные описания помогают определить товары для таможенных целей.</span><span class="sxs-lookup"><span data-stu-id="9567f-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="9567f-160">Можно выбрать таможенное описание на странице **Выпущенные продукты** или в строках заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="9567f-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="9567f-161">Для работы с таможенными описаниями перейдите **Стоимость на складе \> Настройка информации об отгрузке \> Таможенное описание**.</span><span class="sxs-lookup"><span data-stu-id="9567f-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="9567f-162">Там можно просматривать, открывать, создавать и удалять записи для таможенных описаний.</span><span class="sxs-lookup"><span data-stu-id="9567f-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="9567f-163">В следующей таблице описываются поля, которые доступны для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="9567f-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="9567f-164">Поле</span><span class="sxs-lookup"><span data-stu-id="9567f-164">Field</span></span> | <span data-ttu-id="9567f-165">описание</span><span class="sxs-lookup"><span data-stu-id="9567f-165">Description</span></span> |
|---|---|
| <span data-ttu-id="9567f-166">Таможенное описание</span><span class="sxs-lookup"><span data-stu-id="9567f-166">Customs description</span></span> | <span data-ttu-id="9567f-167">Введите уникальный код для данного типа таможенной классификации.</span><span class="sxs-lookup"><span data-stu-id="9567f-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="9567f-168">Часто этот код будет официальным описанием, предоставляемым таможенным органом для описания и качественной оценки товаров.</span><span class="sxs-lookup"><span data-stu-id="9567f-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="9567f-169">описание</span><span class="sxs-lookup"><span data-stu-id="9567f-169">Description</span></span> | <span data-ttu-id="9567f-170">Введите описание таможенной классификации.</span><span class="sxs-lookup"><span data-stu-id="9567f-170">Enter a description of the customs classification.</span></span> |
