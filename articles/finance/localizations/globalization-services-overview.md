---
title: Службы глобализации Dynamics 365
description: В этом разделе представлен обзор служб глобализации Microsoft Dynamics 365.
author: JaneA07
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2ef942f7f6dac2c321a51800ade0bf25f2162304
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018815"
---
# <a name="dynamics-365-globalization-services"></a><span data-ttu-id="1847e-103">Службы глобализации Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="1847e-103">Dynamics 365 globalization services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1847e-104">Следующие службы глобализации могут быть настроены для расширения возможностей, которые существуют в некоторых веб-службах Microsoft Dynamics 365:</span><span class="sxs-lookup"><span data-stu-id="1847e-104">The following globalization services can be configured to extend the capabilities that exist in some Microsoft Dynamics 365 online services:</span></span>

- <span data-ttu-id="1847e-105">**Служба Regulatory Configuration Service (RCS)** поддерживает настройку различных типов электронных документов и отчетов.</span><span class="sxs-lookup"><span data-stu-id="1847e-105">**Regulatory Configuration Service (RCS)** supports the configuration of different types of electronic documents and reports.</span></span> <span data-ttu-id="1847e-106">RCS предоставляет улучшенную версию конструктора электронной отчетности (ER), когда репозиторий конфигураций является автономной службой.</span><span class="sxs-lookup"><span data-stu-id="1847e-106">RCS provides an enhanced version of the Electronic reporting (ER) designer where the configuration repository is a standalone service.</span></span> <span data-ttu-id="1847e-107">Дополнительные сведения см. в [Regulatory Configuration Service](rcs-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1847e-107">For more information, see [Regulatory Configuration Service](rcs-overview.md).</span></span>
- <span data-ttu-id="1847e-108">**Электронное выставление накладных** объединяет в себе настраиваемые форматы преобразований, цифровых подписей и настраиваемых интеграций для связи с внешними веб-службами, включая обработку сертификатов и откликов.</span><span class="sxs-lookup"><span data-stu-id="1847e-108">**Electronic Invoicing** brings together configurable formats for transformations, digital signatures, and configurable integrations for connectivity with external web services, including certification and response handling.</span></span> <span data-ttu-id="1847e-109">Дополнительные сведения см. в [Электронное выставление накладных](e-invoicing-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1847e-109">For more information, see [Electronic Invoicing](e-invoicing-service-overview.md).</span></span>
- <span data-ttu-id="1847e-110">**Расчет налогов** обеспечивает расширенную гибкость за счет поддержки нескольких налоговых кодов, определения кода налога, конструктора расчета налога и ядра среды выполнения для обеспечения соответствия сложным налоговым нормам по всему миру.</span><span class="sxs-lookup"><span data-stu-id="1847e-110">**Tax Calculation** provides enhanced flexibility by supporting multiple tax IDs, tax code determination, the tax calculation designer, and a runtime engine to comply with complex tax regulations worldwide.</span></span> <span data-ttu-id="1847e-111">Дополнительные сведения см. в [Расчет налогов](global-tax-calcuation-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1847e-111">For more information, see [Tax Calculation](global-tax-calcuation-service-overview.md).</span></span>

<span data-ttu-id="1847e-112">Эти службы глобализации обеспечивают интеграцию со следующими веб-службами Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1847e-112">These globalization services provide out-of-box integration with the following Dynamics 365 online services.</span></span>

| <span data-ttu-id="1847e-113">Веб-служба</span><span class="sxs-lookup"><span data-stu-id="1847e-113">Online service</span></span> | <span data-ttu-id="1847e-114">RCS</span><span class="sxs-lookup"><span data-stu-id="1847e-114">RCS</span></span> | <span data-ttu-id="1847e-115">Электронное выставление накладных</span><span class="sxs-lookup"><span data-stu-id="1847e-115">Electronic Invoicing</span></span> | <span data-ttu-id="1847e-116">Расчет налогов (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="1847e-116">Tax Calculation (Preview)</span></span> |
|----------------|-----|----------------------|---------------------------|
| <span data-ttu-id="1847e-117">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="1847e-117">Dynamics 365 Finance</span></span> | <span data-ttu-id="1847e-118">Да</span><span class="sxs-lookup"><span data-stu-id="1847e-118">Yes</span></span> | <span data-ttu-id="1847e-119">Да</span><span class="sxs-lookup"><span data-stu-id="1847e-119">Yes</span></span> | <span data-ttu-id="1847e-120">Да</span><span class="sxs-lookup"><span data-stu-id="1847e-120">Yes</span></span> | 
| <span data-ttu-id="1847e-121">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1847e-121">Dynamics 365 Supply Chain Management</span></span> | <span data-ttu-id="1847e-122">Да</span><span class="sxs-lookup"><span data-stu-id="1847e-122">Yes</span></span> | <span data-ttu-id="1847e-123">Да</span><span class="sxs-lookup"><span data-stu-id="1847e-123">Yes</span></span> | <span data-ttu-id="1847e-124">Да</span><span class="sxs-lookup"><span data-stu-id="1847e-124">Yes</span></span> | 
| <span data-ttu-id="1847e-125">Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="1847e-125">Dynamics 365 Project Operations</span></span> | <span data-ttu-id="1847e-126">Да</span><span class="sxs-lookup"><span data-stu-id="1847e-126">Yes</span></span> | <span data-ttu-id="1847e-127">Да</span><span class="sxs-lookup"><span data-stu-id="1847e-127">Yes</span></span> | <span data-ttu-id="1847e-128">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1847e-128">Not applicable</span></span> | 
| <span data-ttu-id="1847e-129">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1847e-129">Dynamics 365 Commerce</span></span> | <span data-ttu-id="1847e-130">Да</span><span class="sxs-lookup"><span data-stu-id="1847e-130">Yes</span></span> | <span data-ttu-id="1847e-131">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1847e-131">Not applicable</span></span> | <span data-ttu-id="1847e-132">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1847e-132">Not applicable</span></span> | 

> [!NOTE]
> <span data-ttu-id="1847e-133">Из-за различий в доступности географического местоположения Azure (георепликации) для RCS, настройка этой службы может привести к тому, что данные клиента будут переданы вне георепликации, выбранной для применимой веб-службы Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1847e-133">Because of differences in the availability of Azure geographic locations (geos) for RCS, configuration of this service might cause customer data to be transferred outside the geo that is selected for the applicable Dynamics 365 online service.</span></span> <span data-ttu-id="1847e-134">Дополнительные сведения см. в [Dynamics 365 и Power Platform: доступность, расположение данных, язык и локализация](https://aka.ms/rcs/D365Productavailabilityguide).</span><span class="sxs-lookup"><span data-stu-id="1847e-134">For more information, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/rcs/D365Productavailabilityguide).</span></span>