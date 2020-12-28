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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b4e5f715efcac7f883df99508d282db904be0d80
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665231"
---
# <a name="site-selector-module"></a><span data-ttu-id="937f4-103">Модуль выбора сайта</span><span class="sxs-lookup"><span data-stu-id="937f4-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="937f4-104">В этом разделе описываются модуль выбора сайта, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="937f4-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="937f4-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="937f4-105">Overview</span></span>

<span data-ttu-id="937f4-106">Если предприятие имеет различные сайты для рынков, регионов и языковых стандартов, пользователям сайта необходим простой способ переключения между сайтами и выбора предпочтительного сайта для покупок.</span><span class="sxs-lookup"><span data-stu-id="937f4-106">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="937f4-107">Для поддержки этого сценария модуль выбора сайта позволяет пользователям возможность просматривать несколько сайтов.</span><span class="sxs-lookup"><span data-stu-id="937f4-107">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="937f4-108">Модуль выбора сайтов должен быть сконфигурирован с помощью списка сайтов (рынков, регионов или языковых стандартов), которые могут просматривать пользователи сайта.</span><span class="sxs-lookup"><span data-stu-id="937f4-108">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="937f4-109">Модуль выбора сайта доступен в выпуске Dynamics 365 Commerce 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="937f4-109">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="937f4-110">На следующем рисунке показан пример модуля выбора сайта, который указан в заголовке страницы сайта.</span><span class="sxs-lookup"><span data-stu-id="937f4-110">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Пример модуля выбора сайтов в заголовке страницы сайта](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="937f4-112">Свойства модуля выбора сайта</span><span class="sxs-lookup"><span data-stu-id="937f4-112">Site selector module properties</span></span>

| <span data-ttu-id="937f4-113">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="937f4-113">Property name</span></span> | <span data-ttu-id="937f4-114">значение</span><span class="sxs-lookup"><span data-stu-id="937f4-114">Value</span></span>                 | <span data-ttu-id="937f4-115">описание</span><span class="sxs-lookup"><span data-stu-id="937f4-115">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="937f4-116">Заголовок</span><span class="sxs-lookup"><span data-stu-id="937f4-116">Heading</span></span>       | <span data-ttu-id="937f4-117">Текст</span><span class="sxs-lookup"><span data-stu-id="937f4-117">Text</span></span>                  | <span data-ttu-id="937f4-118">Заголовок модуля.</span><span class="sxs-lookup"><span data-stu-id="937f4-118">The heading for the module.</span></span> |
| <span data-ttu-id="937f4-119">Параметры сайта</span><span class="sxs-lookup"><span data-stu-id="937f4-119">Site options</span></span>  | <span data-ttu-id="937f4-120">Имя, изображение, URL-адрес</span><span class="sxs-lookup"><span data-stu-id="937f4-120">Name, Image, URL</span></span>      | <span data-ttu-id="937f4-121">Это свойство определяет имя, ссылку на домашнюю страницу сайта и необязательное изображение, которое будет отображаться для каждого сайта, включенного в модуль.</span><span class="sxs-lookup"><span data-stu-id="937f4-121">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="937f4-122">Изображение может быть флагом или некоторым представлением рынка, региона или языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="937f4-122">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="937f4-123">Добавление модуля выбора сайта на страницу</span><span class="sxs-lookup"><span data-stu-id="937f4-123">Add a site selector module to a page</span></span>

<span data-ttu-id="937f4-124">Модуль выбора сайта может быть добавлен в [модуль заголовка](author-header-module.md) в гнезде выбора сайта.</span><span class="sxs-lookup"><span data-stu-id="937f4-124">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="937f4-125">После его добавления можно определить заголовок модуля и параметры сайта.</span><span class="sxs-lookup"><span data-stu-id="937f4-125">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="937f4-126">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="937f4-126">Additional resources</span></span>

[<span data-ttu-id="937f4-127">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="937f4-127">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="937f4-128">Модуль верхнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="937f4-128">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="937f4-129">Модуль иерархической навигации</span><span class="sxs-lookup"><span data-stu-id="937f4-129">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="937f4-130">Модуль меню навигации</span><span class="sxs-lookup"><span data-stu-id="937f4-130">Navigation menu module</span></span>](nav-menu-module.md)
