---
title: Обзор среды предварительной версии Dynamics 365 Commerce
description: В этой теме содержится обзор среды предварительного просмотра Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ff96aeb5963df9ddee56783a089dad129bbb71c
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024691"
---
# <a name="dynamics-365-commerce-preview-environment-overview"></a><span data-ttu-id="2fab1-103">Обзор среды предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2fab1-103">Dynamics 365 Commerce preview environment overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2fab1-104">В этой теме содержится обзор среды предварительного просмотра Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2fab1-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="overview"></a><span data-ttu-id="2fab1-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="2fab1-105">Overview</span></span>

<span data-ttu-id="2fab1-106">Среда предварительного просмотра Commerce является необязательной сквозной средой предварительного просмотра Dynamics 365 Commerce, которая позволяет потенциальным клиентам попробовать продукт Commerce до его общего выпуска.</span><span class="sxs-lookup"><span data-stu-id="2fab1-106">The Commerce preview environment is an optional end-to-end preview environment of Dynamics 365 Commerce that lets potential customers try out the Commerce product before its general release to the public.</span></span>

<span data-ttu-id="2fab1-107">Помимо некоторых незначительных ограничений, которые не влияют на функции или функциональность, среда предварительного просмотра Commerce обеспечивает полное взаимодействие с Commerce и может быть использована клиентами и партнерами по реализации для оценки продукта, предоставления обратной связи и анализа соответствия и несоответствий.</span><span class="sxs-lookup"><span data-stu-id="2fab1-107">Aside from some minor limitations that don't affect features or functionality, the Commerce preview environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-preview-environment"></a><span data-ttu-id="2fab1-108">Ограничения среды предварительного просмотра Commerce</span><span class="sxs-lookup"><span data-stu-id="2fab1-108">Limitations of the Commerce preview environment</span></span>

<span data-ttu-id="2fab1-109">Хотя среда предварительного просмотра Commerce предоставляет полный набор функций и функциональных возможностей Commerce, существуют некоторые незначительные ограничения:</span><span class="sxs-lookup"><span data-stu-id="2fab1-109">Although the Commerce preview environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="2fab1-110">Хотя сама среда предварительного просмотра Commerce не имеет географических ограничений, компоненты среды, такие как Retail Cloud Scale Unit (RCSU) и приложения электронной коммерции, могут быть предоставлены только в США.</span><span class="sxs-lookup"><span data-stu-id="2fab1-110">Although the Commerce preview environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, can be provisioned only in the United States.</span></span>
- <span data-ttu-id="2fab1-111">У среды предварительного просмотра Commerce есть 30-дневное ограничение с даты предоставления электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="2fab1-111">Use of the Commerce preview environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="2fab1-112">Среда предварительного просмотра Commerce может быть успешно развернута и инициализирована только в среде, использующей демо-топологию, где все компоненты среды развертываются на одной виртуальной машине (VM).</span><span class="sxs-lookup"><span data-stu-id="2fab1-112">The Commerce preview environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed in a single virtual machine (VM).</span></span> <span data-ttu-id="2fab1-113">Основным ограничением этой топологии OneBox VM является количество одновременных пользователей, которое может поддерживать среда предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="2fab1-113">The main limitation of this OneBox VM topology is the number of concurrent users that the preview environment can support.</span></span>
- <span data-ttu-id="2fab1-114">Среду предварительного просмотра Commerce можно оценивать только до общего выхода продукта Commerce.</span><span class="sxs-lookup"><span data-stu-id="2fab1-114">The Commerce preview environment can be evaluated only until the general availability (GA) of the Commerce product.</span></span> <span data-ttu-id="2fab1-115">Новые демо-среды будут доступны после общего выхода.</span><span class="sxs-lookup"><span data-stu-id="2fab1-115">New demo environments will be available after GA.</span></span>

## <a name="get-started"></a><span data-ttu-id="2fab1-116">Начало работы</span><span class="sxs-lookup"><span data-stu-id="2fab1-116">Get started</span></span>

<span data-ttu-id="2fab1-117">Для обеспечения среды предварительного просмотра Commerce см [Обеспечение среды предварительного просмотра Commerce](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="2fab1-117">To provision the Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2fab1-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2fab1-118">Additional resources</span></span>

[<span data-ttu-id="2fab1-119">Обеспечение среды предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2fab1-119">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="2fab1-120">Настройка среды предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2fab1-120">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="2fab1-121">Настройка дополнительных функций среды предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2fab1-121">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="2fab1-122">Вопросы и ответы по среде предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2fab1-122">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)
