---
title: Создание сайта электронной коммерции
description: В этой теме описываются шаги и сведения, необходимые для создания нового сайта электронной коммерции в построителе сайтов Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
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
ms.openlocfilehash: 7d552f29fd8f52b512a7c21b36b0a814cac50646
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517192"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="68e71-103">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="68e71-103">Create an e-commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="68e71-104">В этой теме описываются шаги и сведения, необходимые для создания нового сайта электронной коммерции в построителе сайтов Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="68e71-104">This topic describes the steps and information required to create a new e-commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="68e71-105">При наличии лицензии на возможности Dynamics 365 Commerce будет подготовлен построитель сайтов с начальным сайтом, который можно использовать в качестве основы для собственного сайта.</span><span class="sxs-lookup"><span data-stu-id="68e71-105">When you license the Dynamics 365 Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="68e71-106">Однако если необходимо начать с нуля или если необходимо создать второй сайт, необходимо создать новый сайт в среде разработки сайтов.</span><span class="sxs-lookup"><span data-stu-id="68e71-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="68e71-107">Настройка сайта</span><span class="sxs-lookup"><span data-stu-id="68e71-107">Set up your site</span></span>

<span data-ttu-id="68e71-108">Чтобы настроить сайт, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="68e71-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="68e71-109">Откройте среду построителя сайтов.</span><span class="sxs-lookup"><span data-stu-id="68e71-109">Open the site builder environment.</span></span> <span data-ttu-id="68e71-110">Ссылку на построитель сайтов в Microsoft Lifecycle Services (LCS) можно найти на странице функций среды для Commerce.</span><span class="sxs-lookup"><span data-stu-id="68e71-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="68e71-111">На домашней странице среды разработки сайта выберите пункт **Создать сайт**.</span><span class="sxs-lookup"><span data-stu-id="68e71-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="68e71-112">В диалоговом окне **Создать сайт** укажите следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="68e71-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="68e71-113">Поле</span><span class="sxs-lookup"><span data-stu-id="68e71-113">Field</span></span>                               | <span data-ttu-id="68e71-114">Описание</span><span class="sxs-lookup"><span data-stu-id="68e71-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="68e71-115">Имя сайта</span><span class="sxs-lookup"><span data-stu-id="68e71-115">Site name</span></span>                           | <span data-ttu-id="68e71-116">Введите отображаемое имя, которое должно использоваться для сайта в среде разработки сайта.</span><span class="sxs-lookup"><span data-stu-id="68e71-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="68e71-117">Это имя видимо только в среде разработки и не будет отображаться для клиентов.</span><span class="sxs-lookup"><span data-stu-id="68e71-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="68e71-118">Группа безопасности администратора сайта</span><span class="sxs-lookup"><span data-stu-id="68e71-118">Site administrator's security group</span></span> | <span data-ttu-id="68e71-119">Укажите группу безопасности Microsoft Azure Active Directory (Azure AD), которая управляет пользователями, имеющими роль администратора сайта на этом сайте.</span><span class="sxs-lookup"><span data-stu-id="68e71-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="68e71-120">Канал по умолчанию (номер операционной единицы)</span><span class="sxs-lookup"><span data-stu-id="68e71-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="68e71-121">Выберите интернет-магазин, для которого данный сайт будет выступать в качестве интернет-витрины.</span><span class="sxs-lookup"><span data-stu-id="68e71-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="68e71-122">Если необходимо, чтобы сайт электронной коммерции поддерживал несколько интернет-магазинов, необходимо связать магазины с сайтом в разделе **Параметры сайта** после настройки сайта.</span><span class="sxs-lookup"><span data-stu-id="68e71-122">If you want your e-commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="68e71-123">Язык по умолчанию</span><span class="sxs-lookup"><span data-stu-id="68e71-123">Default language</span></span>                            | <span data-ttu-id="68e71-124">Укажите язык по умолчанию для этого интернет-магазина и рынка.</span><span class="sxs-lookup"><span data-stu-id="68e71-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="68e71-125">Интернет-магазин может поддерживать несколько языков.</span><span class="sxs-lookup"><span data-stu-id="68e71-125">An online store can support multiple languages.</span></span> <span data-ttu-id="68e71-126">Если требуется поддержка нескольких языков для данного интернет-магазина или другого интернет-магазина, эту поддержку можно настроить в разделе **Параметры сайта** после настройки сайта.</span><span class="sxs-lookup"><span data-stu-id="68e71-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="68e71-127">Домен</span><span class="sxs-lookup"><span data-stu-id="68e71-127">Domain</span></span>                              | <span data-ttu-id="68e71-128">Выберите имя домена, которое будет доменом для данного интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="68e71-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="68e71-129">Если в LCS не было настроено ни одного домена, это поле можно оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="68e71-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="68e71-130">После настройки домена в LCS его необходимо добавить в интернет-магазин в разделе **Параметры сайта**.</span><span class="sxs-lookup"><span data-stu-id="68e71-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="68e71-131">Путь</span><span class="sxs-lookup"><span data-stu-id="68e71-131">Path</span></span>                              | <span data-ttu-id="68e71-132">Если сайт поддерживает несколько языков для данного имени домена, используйте поле пути для создания уникального URL-адреса сайта для этого сочетания домена и языка.</span><span class="sxs-lookup"><span data-stu-id="68e71-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="68e71-133">Если язык, указанный в поле **Язык по умолчанию**, является единственным языком, который будет поддерживаться для данного домена, или он будет по-прежнему использоваться по умолчанию после локализации сайта на дополнительные языки, рекомендуется оставить это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="68e71-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="68e71-134">После создания сайта можно убедиться, что он связан с интернет-магазином, выбрав вкладку **Продукты**. Должен отобразиться ассортимент продуктов, которые были выделены для интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="68e71-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="68e71-135">Можно также использовать раскрывающееся меню в левом верхнем углу страницы для получения доступа к распределенным продуктам по категориям.</span><span class="sxs-lookup"><span data-stu-id="68e71-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68e71-136">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="68e71-136">Additional resources</span></span>

[<span data-ttu-id="68e71-137">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="68e71-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="68e71-138">Развертывание нового клиента электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="68e71-138">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="68e71-139">Связывание сайта Dynamics 365 Commerce с интернет-каналом</span><span class="sxs-lookup"><span data-stu-id="68e71-139">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="68e71-140">Управление файлами robots.txt</span><span class="sxs-lookup"><span data-stu-id="68e71-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="68e71-141">Пакетная отправка перенаправлений URL-адресов</span><span class="sxs-lookup"><span data-stu-id="68e71-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="68e71-142">Настройка клиента B2C в Commerce</span><span class="sxs-lookup"><span data-stu-id="68e71-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="68e71-143">Настройка специальных страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="68e71-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="68e71-144">Настройка нескольких клиентов B2C в среде Commerce</span><span class="sxs-lookup"><span data-stu-id="68e71-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="68e71-145">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="68e71-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="68e71-146">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="68e71-146">Enable location-based store detection</span></span>](enable-store-detection.md)
