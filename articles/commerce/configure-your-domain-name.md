---
title: Настройка доменного имени
description: В этой теме объясняется, как настроить имя домена для сайта электронной коммерции Microsoft Dynamics 365.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f73c034563fb1cc6b05091b4c47e2a788d1a8b6
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945544"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="eeff8-103">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="eeff8-103">Configure your domain name</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="eeff8-104">В этой теме объясняется, как настроить имя домена для сайта электронной коммерции Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="eeff8-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="eeff8-105">Добавление доменов во время инициализации электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="eeff8-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="eeff8-106">Чтобы связать домены с вашей средой электронной коммерции, выполните инициализацию электронной коммерции, как описано в разделе [Развертывание нового сайта электронной коммерции](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="eeff8-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="eeff8-107">Во время инициализации вам необходимо предоставить информацию, которая будет использоваться для подготовки среды электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="eeff8-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="eeff8-108">В поле **Поддерживаемые имена узлов** добавьте все домены, которые планируется использовать в этой среде.</span><span class="sxs-lookup"><span data-stu-id="eeff8-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="eeff8-109">Несколько доменов следует разделять точками с запятой.</span><span class="sxs-lookup"><span data-stu-id="eeff8-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="eeff8-110">Таким образом, домены настраиваются во всех необходимых компонентах электронной коммерции, и они готовы к использованию при переключении трафика из сети доставки содержимого (CDN) или веб-сервера и направления его на внешний интерфейс электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="eeff8-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="eeff8-111">Добавление доменов после инициализации электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="eeff8-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="eeff8-112">Чтобы связать новые домены с вашей средой электронной коммерции после инициализации электронной коммерции необходимо отправить запрос на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="eeff8-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eeff8-113">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="eeff8-113">Additional resources</span></span>

[<span data-ttu-id="eeff8-114">Развертывание нового сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="eeff8-114">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="eeff8-115">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="eeff8-115">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="eeff8-116">Связывание веб-сайта с каналом</span><span class="sxs-lookup"><span data-stu-id="eeff8-116">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="eeff8-117">Управление файлами robots.txt</span><span class="sxs-lookup"><span data-stu-id="eeff8-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="eeff8-118">Настройка специальных страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="eeff8-118">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="eeff8-119">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="eeff8-119">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="eeff8-120">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="eeff8-120">Enable location-based store detection</span></span>](enable-store-detection.md)
