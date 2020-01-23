---
title: Создание сайта электронной коммерции
description: В этой теме описываются задачи, связанные с созданием нового сайта электронной коммерции в Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 54259d3f5dfd8c8e1ff2caaadfac497cc0e133e0
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945843"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="3f100-103">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="3f100-103">Create an e-Commerce site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3f100-104">В этой теме описываются задачи, связанные с созданием нового сайта электронной коммерции в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3f100-104">This topic describes the tasks that are associated with the creation of a new e-Commerce site in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3f100-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="3f100-105">Overview</span></span>

<span data-ttu-id="3f100-106">Чтобы начать разработку сайта электронной коммерции, необходимо сначала создать новый сайт в среде разработки сайта.</span><span class="sxs-lookup"><span data-stu-id="3f100-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="3f100-107">Прежде чем можно будет создать новый сайт, необходимо создать по крайней мере один интернет-магазин в Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="3f100-107">Before you can create a new site, at least one online store must be created in Dynamics 365 Retail.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="3f100-108">Настройка сайта</span><span class="sxs-lookup"><span data-stu-id="3f100-108">Set up your site</span></span>

<span data-ttu-id="3f100-109">Чтобы настроить сайт, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3f100-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="3f100-110">В Microsoft Lifecycle Services (LCS) выберите ссылку для среды разработки сайта.</span><span class="sxs-lookup"><span data-stu-id="3f100-110">In Microsoft Lifecycle Services (LCS), select the link for the site authoring environment.</span></span> 
1. <span data-ttu-id="3f100-111">На домашней странице среды разработки сайта выберите пункт **Создать сайт**.</span><span class="sxs-lookup"><span data-stu-id="3f100-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="3f100-112">В диалоговом окне **Создать сайт** укажите следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="3f100-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="3f100-113">Поле</span><span class="sxs-lookup"><span data-stu-id="3f100-113">Field</span></span>                               | <span data-ttu-id="3f100-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3f100-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="3f100-115">Имя сайта</span><span class="sxs-lookup"><span data-stu-id="3f100-115">Site name</span></span>                           | <span data-ttu-id="3f100-116">Введите отображаемое имя, которое должно использоваться для сайта в среде разработки сайта.</span><span class="sxs-lookup"><span data-stu-id="3f100-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="3f100-117">Это имя видимо только в среде разработки и не будет отображаться для клиентов.</span><span class="sxs-lookup"><span data-stu-id="3f100-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="3f100-118">Группа безопасности администратора сайта</span><span class="sxs-lookup"><span data-stu-id="3f100-118">Site administrator's security group</span></span> | <span data-ttu-id="3f100-119">Укажите группу безопасности Microsoft Azure Active Directory (Azure AD), которая управляет пользователями, имеющими роль администратора сайта на этом сайте.</span><span class="sxs-lookup"><span data-stu-id="3f100-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="3f100-120">Канал по умолчанию (номер операционной единицы)</span><span class="sxs-lookup"><span data-stu-id="3f100-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="3f100-121">Выберите интернет-магазин, для которого данный сайт будет выступать в качестве интернет-витрины.</span><span class="sxs-lookup"><span data-stu-id="3f100-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="3f100-122">Если необходимо, чтобы сайт электронной коммерции поддерживал несколько интернет-магазинов, необходимо связать магазины с сайтом в разделе **Параметры сайта** после настройки сайта.</span><span class="sxs-lookup"><span data-stu-id="3f100-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="3f100-123">Язык по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3f100-123">Default language</span></span>                            | <span data-ttu-id="3f100-124">Укажите язык по умолчанию для этого интернет-магазина и рынка.</span><span class="sxs-lookup"><span data-stu-id="3f100-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="3f100-125">Интернет-магазин может поддерживать несколько языков.</span><span class="sxs-lookup"><span data-stu-id="3f100-125">An online store can support multiple languages.</span></span> <span data-ttu-id="3f100-126">Если требуется поддержка нескольких языков для данного интернет-магазина или другого интернет-магазина, эту поддержку можно настроить в разделе **Параметры сайта** после настройки сайта.</span><span class="sxs-lookup"><span data-stu-id="3f100-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="3f100-127">Домен</span><span class="sxs-lookup"><span data-stu-id="3f100-127">Domain</span></span>                              | <span data-ttu-id="3f100-128">Выберите имя домена, которое будет доменом для данного интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="3f100-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="3f100-129">Если в LCS не было настроено ни одного домена, это поле можно оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="3f100-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="3f100-130">После настройки домена в LCS его необходимо добавить в интернет-магазин в разделе **Параметры сайта**.</span><span class="sxs-lookup"><span data-stu-id="3f100-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="3f100-131">Путь</span><span class="sxs-lookup"><span data-stu-id="3f100-131">Path</span></span>                              | <span data-ttu-id="3f100-132">Если сайт поддерживает несколько языков для данного имени домена, используйте поле пути для создания уникального URL-адреса сайта для этого сочетания домена и языка.</span><span class="sxs-lookup"><span data-stu-id="3f100-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="3f100-133">Если язык, указанный в поле **Язык по умолчанию**, является единственным языком, который будет поддерживаться для данного домена, или он будет по-прежнему использоваться по умолчанию после локализации сайта на дополнительные языки, рекомендуется оставить это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="3f100-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="3f100-134">После создания сайта можно убедиться, что он связан с интернет-магазином, выбрав вкладку **Продукты**. Должен отобразиться ассортимент продуктов, которые были выделены для интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="3f100-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="3f100-135">Можно также использовать раскрывающееся меню в левом верхнем углу страницы для получения доступа к распределенным продуктам по категориям.</span><span class="sxs-lookup"><span data-stu-id="3f100-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3f100-136">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3f100-136">Additional resources</span></span>

[<span data-ttu-id="3f100-137">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="3f100-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="3f100-138">Развертывание нового сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="3f100-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="3f100-139">Связывание веб-сайта с каналом</span><span class="sxs-lookup"><span data-stu-id="3f100-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="3f100-140">Управление файлами robots.txt</span><span class="sxs-lookup"><span data-stu-id="3f100-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="3f100-141">Настройка специальных страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="3f100-141">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="3f100-142">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="3f100-142">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="3f100-143">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="3f100-143">Enable location-based store detection</span></span>](enable-store-detection.md)
