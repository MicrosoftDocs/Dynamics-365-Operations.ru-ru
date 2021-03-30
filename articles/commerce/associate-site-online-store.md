---
title: Связывание веб-сайта Dynamics 365 Commerce с каналом продаж через Интернет
description: В этом разделе объясняется, как связать сайт Microsoft Dynamics 365 Commerce с одним или несколькими интернет-магазинами.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bb39b54e45e387067720dcbc5d9ccffbf8bf08b4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211530"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a><span data-ttu-id="df6be-103">Связывание веб-сайта Dynamics 365 Commerce с каналом продаж через Интернет</span><span class="sxs-lookup"><span data-stu-id="df6be-103">Associate a Dynamics 365 Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="df6be-104">В этом разделе объясняется, как связать сайт Microsoft Dynamics 365 Commerce с одним или несколькими интернет-магазинами.</span><span class="sxs-lookup"><span data-stu-id="df6be-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="df6be-105">После подготовки среды электронной коммерции Dynamics 365 Commerce с помощью портала Microsoft Dynamics Lifecycle Services (LCS) можно приступать к созданию первого веб-сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="df6be-105">After you've provisioned your Dynamics 365 Commerce e-commerce environment by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-commerce website.</span></span> <span data-ttu-id="df6be-106">В качестве части начального создания сайта вы связываете сайт с ранее созданным интернет-магазином.</span><span class="sxs-lookup"><span data-stu-id="df6be-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="df6be-107">На этом шаге сайт связывается с интернет-каналом и позволяет сайту показывать иерархию переходов, продукты, категории, цены, параметры доставки и все остальные, которые были определены в интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="df6be-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="df6be-108">Чтобы создать новый сайт и связать интернет-магазин с ним, в LCS выберите ссылку для среды разработки сайтов.</span><span class="sxs-lookup"><span data-stu-id="df6be-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="df6be-109">Затем на странице для среды разработки сайта выберите пункт **Создать сайт**.</span><span class="sxs-lookup"><span data-stu-id="df6be-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="df6be-110">В диалоговом окне **Создать сайт** необходимо предоставить некоторые базовые сведения о сайте.</span><span class="sxs-lookup"><span data-stu-id="df6be-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="df6be-111">Полное описание информации, которую необходимо предоставить, см. в разделе [Создание нового сайта электронной коммерции](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="df6be-111">For a complete explanation of the information that you must provide, see [Create a new e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="df6be-112">После создания сайта можно убедиться, что он связан с интернет-магазином, выбрав вкладку **Продукты**. Должен отобразиться ассортимент продуктов, которые были выделены для интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="df6be-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="df6be-113">Можно также использовать раскрывающееся поле в левом верхнем углу страницы для получения доступа к продуктам по категориям.</span><span class="sxs-lookup"><span data-stu-id="df6be-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df6be-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="df6be-114">Additional resources</span></span>

[<span data-ttu-id="df6be-115">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="df6be-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="df6be-116">Развертывание нового клиента электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="df6be-116">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="df6be-117">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="df6be-117">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="df6be-118">Управление файлами robots.txt</span><span class="sxs-lookup"><span data-stu-id="df6be-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="df6be-119">Пакетная отправка перенаправлений URL-адресов</span><span class="sxs-lookup"><span data-stu-id="df6be-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="df6be-120">Настройка клиента B2C в Commerce</span><span class="sxs-lookup"><span data-stu-id="df6be-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="df6be-121">Настройка специальных страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="df6be-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="df6be-122">Настройка нескольких клиентов B2C в среде Commerce</span><span class="sxs-lookup"><span data-stu-id="df6be-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="df6be-123">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="df6be-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="df6be-124">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="df6be-124">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]