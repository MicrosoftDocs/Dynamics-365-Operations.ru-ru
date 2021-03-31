---
title: Настройка доменного имени
description: В этой теме объясняется, как настроить имя домена для сайта электронной коммерции Microsoft Dynamics 365.
author: psimolin
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8b7bc322b1a42190d5eec99f89a34025c34ba09f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220494"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="46a47-103">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="46a47-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="46a47-104">В этой теме объясняется, как настроить имя домена для сайта электронной коммерции Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="46a47-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="46a47-105">Добавление доменов во время инициализации электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="46a47-105">Add domains during e-commerce initialization</span></span>

<span data-ttu-id="46a47-106">Чтобы связать домены с вашей средой электронной коммерции Dynamics 365 Commerce, выполните инициализацию электронной коммерции, как описано в разделе [Развертывание нового клиента электронной коммерции](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="46a47-106">To associate domains with your Dynamics 365 Commerce e-commerce environment, initialize e-commerce as described in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="46a47-107">Во время инициализации вам необходимо предоставить информацию, которая будет использоваться для подготовки среды электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="46a47-107">During initialization, you're asked to provide information that will be used to provision your e-commerce environment.</span></span> <span data-ttu-id="46a47-108">В поле **Поддерживаемые имена узлов** добавьте все домены, которые планируется использовать в этой среде.</span><span class="sxs-lookup"><span data-stu-id="46a47-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="46a47-109">Несколько доменов следует разделять точками с запятой.</span><span class="sxs-lookup"><span data-stu-id="46a47-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="46a47-110">Таким образом, домены настраиваются во всех необходимых компонентах электронной коммерции, и они готовы к использованию при переключении трафика из сети доставки содержимого (CDN) или веб-сервера и направления его на внешний интерфейс электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="46a47-110">In this way, the domains are configured in all the required Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="46a47-111">Добавление доменов после инициализации электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="46a47-111">Add domains after e-commerce initialization</span></span>

<span data-ttu-id="46a47-112">Чтобы связать новые домены с вашей средой электронной коммерции после инициализации электронной коммерции необходимо отправить запрос на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="46a47-112">To associate new domains with your e-commerce environment after e-commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46a47-113">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="46a47-113">Additional resources</span></span>

[<span data-ttu-id="46a47-114">Развертывание нового клиента электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="46a47-114">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="46a47-115">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="46a47-115">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="46a47-116">Связывание сайта Dynamics 365 Commerce с интернет-каналом</span><span class="sxs-lookup"><span data-stu-id="46a47-116">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="46a47-117">Управление файлами robots.txt</span><span class="sxs-lookup"><span data-stu-id="46a47-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="46a47-118">Пакетная отправка перенаправлений URL-адресов</span><span class="sxs-lookup"><span data-stu-id="46a47-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="46a47-119">Настройка клиента B2C в Commerce</span><span class="sxs-lookup"><span data-stu-id="46a47-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="46a47-120">Настройка специальных страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="46a47-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="46a47-121">Настройка нескольких клиентов B2C в среде Commerce</span><span class="sxs-lookup"><span data-stu-id="46a47-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="46a47-122">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="46a47-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="46a47-123">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="46a47-123">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]