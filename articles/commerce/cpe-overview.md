---
title: Обзор ознакомительной среды Dynamics 365 Commerce
description: В этой теме содержится обзор ознакомительной среды Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8e08c2f327771d7731b836840006d63b6ecb7dfc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000958"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="6fa26-103">Обзор ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6fa26-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6fa26-104">В этой теме содержится обзор ознакомительной среды Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6fa26-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="6fa26-105">Ознакомительные среды Commerce не являются общедоступными и предоставляются партнерам и клиентам по запросам по запросу.</span><span class="sxs-lookup"><span data-stu-id="6fa26-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="6fa26-106">Для получения дополнительных сведений обратитесь к своему контакту Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="6fa26-106">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="6fa26-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="6fa26-107">Overview</span></span>

<span data-ttu-id="6fa26-108">Ознакомительная среда Commerce является необязательной сквозной средой Dynamics 365 Commerce, которая позволяет партнерам и потенциальным клиентам попробовать продукт Commerce.</span><span class="sxs-lookup"><span data-stu-id="6fa26-108">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="6fa26-109">Ознакомительные среды частично предварительно настроены для уменьшения необходимых действий после подготовки.</span><span class="sxs-lookup"><span data-stu-id="6fa26-109">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="6fa26-110">Помимо некоторых незначительных ограничений, которые не влияют на функции или функциональность, ознакомительная среда Commerce обеспечивает полное взаимодействие с Commerce и может быть использована клиентами и партнерами по реализации для оценки продукта, предоставления обратной связи и анализа соответствия и несоответствий.</span><span class="sxs-lookup"><span data-stu-id="6fa26-110">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="6fa26-111">Ограничения ознакомительной среды Commerce</span><span class="sxs-lookup"><span data-stu-id="6fa26-111">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="6fa26-112">Хотя ознакомительная среда Commerce предоставляет полный набор функций и функциональных возможностей Commerce, существуют некоторые незначительные ограничения:</span><span class="sxs-lookup"><span data-stu-id="6fa26-112">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="6fa26-113">Хотя сама ознакомительная среда Commerce не имеет географических ограничений, компоненты среды, такие как Retail Cloud Scale Unit (RCSU) и приложения электронной коммерции, должны быть предоставлены только в США.</span><span class="sxs-lookup"><span data-stu-id="6fa26-113">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="6fa26-114">У ознакомительной среды Commerce есть 30-дневное ограничение с даты предоставления электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="6fa26-114">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="6fa26-115">Ознакомительная среда Commerce может быть успешно развернута и инициализирована только в среде, использующей демо-топологию, где все компоненты среды развертываются на одной виртуальной машине (VM), расположенной в облаке.</span><span class="sxs-lookup"><span data-stu-id="6fa26-115">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="6fa26-116">Основным ограничением этой топологии является количество одновременных пользователей, которое может поддерживать среда.</span><span class="sxs-lookup"><span data-stu-id="6fa26-116">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="6fa26-117">Начало работы</span><span class="sxs-lookup"><span data-stu-id="6fa26-117">Get started</span></span>

<span data-ttu-id="6fa26-118">Для обеспечения ознакомительной среды Commerce см [Обеспечение ознакомительной среды Commerce](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="6fa26-118">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6fa26-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6fa26-119">Additional resources</span></span>

[<span data-ttu-id="6fa26-120">Подготовка ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6fa26-120">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="6fa26-121">Настройка ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6fa26-121">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="6fa26-122">Настройка BOPIS в ознакомительной среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6fa26-122">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="6fa26-123">Настройка дополнительных функций ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6fa26-123">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="6fa26-124">Вопросы и ответы по ознакомительной среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6fa26-124">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)
