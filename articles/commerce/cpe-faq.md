---
title: Вопросы и ответы по ознакомительной среде Dynamics 365 Commerce
description: Эта тема дает ответы на часто задаваемые вопросы об ознакомительной среде Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 6b8d7d7364087dacf3b4479ab008609ecffeaacb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000983"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a><span data-ttu-id="1cfec-103">Вопросы и ответы по ознакомительной среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1cfec-103">Dynamics 365 Commerce evaluation environment FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1cfec-104">Эта тема дает ответы на часто задаваемые вопросы об ознакомительной среде Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1cfec-104">This topic provides answers to frequently asked questions about the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="1cfec-105">**Можем ли мы использовать ознакомительную среду Commerce в качестве магазина электронной коммерции для клиентов, которые в настоящее время реализуют Retail?**</span><span class="sxs-lookup"><span data-stu-id="1cfec-105">**Can we use the Commerce evaluation environment as an e-Commerce storefront for customers that currently implement Retail?**</span></span>

<span data-ttu-id="1cfec-106">№ п/п</span><span class="sxs-lookup"><span data-stu-id="1cfec-106">No.</span></span> <span data-ttu-id="1cfec-107">Ознакомительная среда Commerce предназначена только для ознакомления.</span><span class="sxs-lookup"><span data-stu-id="1cfec-107">The Commerce evaluation environment is only for evaluation.</span></span> <span data-ttu-id="1cfec-108">Если вам нужна среда для клиента, реализующего Retail, обратитесь в Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="1cfec-108">If you require an environment for a customer that implements Retail, contact Microsoft.</span></span>

<span data-ttu-id="1cfec-109">**Можно ли использовать ознакомительную среду Commerce для предоставления функций электронной коммерции поверх существующего приложения/среды, которая реализует Retail?**</span><span class="sxs-lookup"><span data-stu-id="1cfec-109">**Can the Commerce evaluation environment be used to provision the e-Commerce features on top of an existing application/environment that implements Retail?**</span></span>

<span data-ttu-id="1cfec-110">Нет (главным образом).</span><span class="sxs-lookup"><span data-stu-id="1cfec-110">No (mostly).</span></span> <span data-ttu-id="1cfec-111">Ознакомительные компоненты Commerce доступны только в тех средах, которые соответствуют конфигурациям, указанным в руководстве по предварительным условиям и подготовке.</span><span class="sxs-lookup"><span data-stu-id="1cfec-111">The Commerce evaluation components are available only to environments that match the configurations that are specified in the prerequisites and provisioning guide.</span></span> <span data-ttu-id="1cfec-112">Кроме того, требуемые базовые демонстрационные данные не будут доступны в средах, которые были развернуты в исходном выпуске ранее 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="1cfec-112">Additionally, the required base demo data won't be available in environments that were deployed with an initial release that is earlier than 10.0.8.</span></span> 

<span data-ttu-id="1cfec-113">**Какие затраты связаны с развертыванием ознакомительной среды Commerce в Microsoft Azure через Microsoft Dynamics Lifecycle Services (LCS)?**</span><span class="sxs-lookup"><span data-stu-id="1cfec-113">**What costs are involved in deploying the Commerce evaluation environment on Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span></span>

<span data-ttu-id="1cfec-114">Традиционная демонстрационная среда Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce Headquarters (виртуальная машина \[VM\]) будет размещена в вашей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="1cfec-114">A traditional Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce headquarters demo environment (virtual machine \[VM\]) will be hosted in your Azure subscription.</span></span> <span data-ttu-id="1cfec-115">Для оценки расходов можно использовать [калькулятор цен Azure](https://azure.microsoft.com/pricing/calculator/).</span><span class="sxs-lookup"><span data-stu-id="1cfec-115">You can use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to estimate this cost.</span></span>

<span data-ttu-id="1cfec-116">Другие компоненты, такие как Commerce Scale Unit, конструктор сайта Commerce и сайт электронной коммерции будут доступны как программное обеспечение как услуга (SaaS) и размещены в корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="1cfec-116">Other components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site will be available as software as a service (SaaS) and hosted by Microsoft.</span></span>

<span data-ttu-id="1cfec-117">**Какие географические регионы Azure в настоящее время поддерживаются для ознакомительной среды Commerce?**</span><span class="sxs-lookup"><span data-stu-id="1cfec-117">**Which Azure geographies are currently supported for the Commerce evaluation environment?**</span></span>

<span data-ttu-id="1cfec-118">Ознакомительная среда Commerce может быть развернута только в Северной Америке.</span><span class="sxs-lookup"><span data-stu-id="1cfec-118">The Commerce evaluation environment can be deployed only in the North America geography.</span></span>

<span data-ttu-id="1cfec-119">**Есть ли загружаемый виртуальный жесткий диск (VHD) с вариантом полной виртуальной машины OneBox?**</span><span class="sxs-lookup"><span data-stu-id="1cfec-119">**Is there a downloadable virtual hard disk (VHD) that has the complete OneBox virtual machine (VM) option?**</span></span>

<span data-ttu-id="1cfec-120">Dynamics 365 Commerce и Commerce Scale Unit — это полностью программное обеспечение как услуга (SaaS) и должны размещать в облаке.</span><span class="sxs-lookup"><span data-stu-id="1cfec-120">Dynamics 365 Commerce and Commerce Scale Unit are completely software as a service (SaaS) and must be cloud-hosted.</span></span>

<span data-ttu-id="1cfec-121">**Как долго может использоваться ознакомительная среда Commerce?**</span><span class="sxs-lookup"><span data-stu-id="1cfec-121">**How long can the Commerce evaluation environment be used?**</span></span>

<span data-ttu-id="1cfec-122">В ознакомительной среде Commerce имеется предельное время в 30 дней от даты, когда были подготовлены компоненты SaaS, такие как Commerce Scale Unit, конструктор сайтов Commerce site и сайт электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="1cfec-122">The Commerce evaluation environment has a 30-day time limit from the date when SaaS components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site are provisioned.</span></span>

<span data-ttu-id="1cfec-123">**Могу ли я продлить срок для ознакомительной среды Commerce?**</span><span class="sxs-lookup"><span data-stu-id="1cfec-123">**Can I extend the time limit for my Commerce evaluation environment?**</span></span>

<span data-ttu-id="1cfec-124">Расширение предела времени является исключением из нормы и рассматривается отдельно для каждого случая.</span><span class="sxs-lookup"><span data-stu-id="1cfec-124">Extension of the time limit is an exception to the norm and is considered on a case-by-case basis.</span></span> <span data-ttu-id="1cfec-125">Следует обратитесь за помощью к партнеру корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="1cfec-125">You should reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1cfec-126">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1cfec-126">Additional resources</span></span>

[<span data-ttu-id="1cfec-127">Обзор ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1cfec-127">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="1cfec-128">Подготовка ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1cfec-128">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="1cfec-129">Настройка ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1cfec-129">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="1cfec-130">Настройка BOPIS в ознакомительной среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1cfec-130">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="1cfec-131">Настройка дополнительных функций ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1cfec-131">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)
