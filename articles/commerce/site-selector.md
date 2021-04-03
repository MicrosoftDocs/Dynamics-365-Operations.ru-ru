---
title: Модуль выбора сайта
description: В этом разделе описываются модуль выбора сайта, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e24590d4a8f172809704aab0d761f6db0fb0e11b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234349"
---
# <a name="site-selector-module"></a><span data-ttu-id="6be67-103">Модуль выбора сайта</span><span class="sxs-lookup"><span data-stu-id="6be67-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6be67-104">В этом разделе описываются модуль выбора сайта, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6be67-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6be67-105">Если предприятие имеет различные сайты для рынков, регионов и языковых стандартов, пользователям сайта необходим простой способ переключения между сайтами и выбора предпочтительного сайта для покупок.</span><span class="sxs-lookup"><span data-stu-id="6be67-105">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="6be67-106">Для поддержки этого сценария модуль выбора сайта позволяет пользователям возможность просматривать несколько сайтов.</span><span class="sxs-lookup"><span data-stu-id="6be67-106">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="6be67-107">Модуль выбора сайтов должен быть сконфигурирован с помощью списка сайтов (рынков, регионов или языковых стандартов), которые могут просматривать пользователи сайта.</span><span class="sxs-lookup"><span data-stu-id="6be67-107">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="6be67-108">Модуль выбора сайта доступен в выпуске Dynamics 365 Commerce 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="6be67-108">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="6be67-109">На следующем рисунке показан пример модуля выбора сайта, который указан в заголовке страницы сайта.</span><span class="sxs-lookup"><span data-stu-id="6be67-109">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Пример модуля выбора сайтов в заголовке страницы сайта](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="6be67-111">Свойства модуля выбора сайта</span><span class="sxs-lookup"><span data-stu-id="6be67-111">Site selector module properties</span></span>

| <span data-ttu-id="6be67-112">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="6be67-112">Property name</span></span> | <span data-ttu-id="6be67-113">значение</span><span class="sxs-lookup"><span data-stu-id="6be67-113">Value</span></span>                 | <span data-ttu-id="6be67-114">описание</span><span class="sxs-lookup"><span data-stu-id="6be67-114">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="6be67-115">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6be67-115">Heading</span></span>       | <span data-ttu-id="6be67-116">Текст</span><span class="sxs-lookup"><span data-stu-id="6be67-116">Text</span></span>                  | <span data-ttu-id="6be67-117">Заголовок модуля.</span><span class="sxs-lookup"><span data-stu-id="6be67-117">The heading for the module.</span></span> |
| <span data-ttu-id="6be67-118">Параметры сайта</span><span class="sxs-lookup"><span data-stu-id="6be67-118">Site options</span></span>  | <span data-ttu-id="6be67-119">Имя, изображение, URL-адрес</span><span class="sxs-lookup"><span data-stu-id="6be67-119">Name, Image, URL</span></span>      | <span data-ttu-id="6be67-120">Это свойство определяет имя, ссылку на домашнюю страницу сайта и необязательное изображение, которое будет отображаться для каждого сайта, включенного в модуль.</span><span class="sxs-lookup"><span data-stu-id="6be67-120">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="6be67-121">Изображение может быть флагом или некоторым представлением рынка, региона или языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="6be67-121">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="6be67-122">Добавление модуля выбора сайта на страницу</span><span class="sxs-lookup"><span data-stu-id="6be67-122">Add a site selector module to a page</span></span>

<span data-ttu-id="6be67-123">Модуль выбора сайта может быть добавлен в [модуль заголовка](author-header-module.md) в гнезде выбора сайта.</span><span class="sxs-lookup"><span data-stu-id="6be67-123">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="6be67-124">После его добавления можно определить заголовок модуля и параметры сайта.</span><span class="sxs-lookup"><span data-stu-id="6be67-124">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6be67-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6be67-125">Additional resources</span></span>

[<span data-ttu-id="6be67-126">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="6be67-126">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6be67-127">Модуль верхнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="6be67-127">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="6be67-128">Модуль иерархической навигации</span><span class="sxs-lookup"><span data-stu-id="6be67-128">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="6be67-129">Модуль меню навигации</span><span class="sxs-lookup"><span data-stu-id="6be67-129">Navigation menu module</span></span>](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]