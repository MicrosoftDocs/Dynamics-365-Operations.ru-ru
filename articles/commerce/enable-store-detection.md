---
title: Включение обнаружения магазинов на основе местоположения
description: В этом разделе описывается, как включить обнаружение магазинов на основе местоположения для сайта Dynamics 365 Commerce.
author: brianshook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 71e523cab20281d5db7efff40b5ef4f7293a4765
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799139"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="77cc3-103">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="77cc3-103">Enable location-based store detection</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="77cc3-104">В этом разделе описывается, как включить обнаружение магазинов на основе местоположения для сайта Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="77cc3-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="77cc3-105">Обнаружение магазинов на основе местоположения в Commerce позволяет предоставлять соответствующее содержимое сайта клиентам на основе их местоположения.</span><span class="sxs-lookup"><span data-stu-id="77cc3-105">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="77cc3-106">Если обнаружение магазинов на основе местоположения включено, служба отображения Commerce использует информацию о стране/регионе из IP-адреса веб-браузера клиента, чтобы направлять пользователя в оптимальную доступную географическую конфигурацию сайта.</span><span class="sxs-lookup"><span data-stu-id="77cc3-106">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="77cc3-107">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="77cc3-107">Privacy notice</span></span>

<span data-ttu-id="77cc3-108">При включении функции обнаружения магазинов на основе местоположения сведения из браузера клиента отправляются в службу определения местоположения Microsoft.</span><span class="sxs-lookup"><span data-stu-id="77cc3-108">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="77cc3-109">Эти сведения затем используются для предоставления содержимого клиенту, которое имеют отношение к его местоположению.</span><span class="sxs-lookup"><span data-stu-id="77cc3-109">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="77cc3-110">Как сведения, которые отправляются из браузера клиента, так и сведения на основе местоположения, возвращаемые клиенту, должны соответствовать политике конфиденциальности и cookie-файлов.</span><span class="sxs-lookup"><span data-stu-id="77cc3-110">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="77cc3-111">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="77cc3-111">Turn on location-based store detection</span></span>

<span data-ttu-id="77cc3-112">Чтобы включить обнаружение магазинов на основе местоположения в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="77cc3-112">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="77cc3-113">В средстве разработки перейдите на ваш сайт.</span><span class="sxs-lookup"><span data-stu-id="77cc3-113">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="77cc3-114">В области переходов слева выберите **Управление сайтом**.</span><span class="sxs-lookup"><span data-stu-id="77cc3-114">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="77cc3-115">Выберите **Параметры сайта**.</span><span class="sxs-lookup"><span data-stu-id="77cc3-115">Select **Site Settings**.</span></span>
1. <span data-ttu-id="77cc3-116">Установите для параметра **Включить обнаружение магазинов на основе местоположения** значение **Вкл.**</span><span class="sxs-lookup"><span data-stu-id="77cc3-116">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77cc3-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="77cc3-117">Additional resources</span></span>

[<span data-ttu-id="77cc3-118">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="77cc3-118">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="77cc3-119">Развертывание нового клиента электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="77cc3-119">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="77cc3-120">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="77cc3-120">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="77cc3-121">Связывание сайта Dynamics 365 Commerce с интернет-каналом</span><span class="sxs-lookup"><span data-stu-id="77cc3-121">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="77cc3-122">Управление файлами robots.txt</span><span class="sxs-lookup"><span data-stu-id="77cc3-122">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="77cc3-123">Пакетная отправка перенаправлений URL-адресов</span><span class="sxs-lookup"><span data-stu-id="77cc3-123">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="77cc3-124">Настройка клиента B2C в Commerce</span><span class="sxs-lookup"><span data-stu-id="77cc3-124">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="77cc3-125">Настройка специальных страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="77cc3-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="77cc3-126">Настройка нескольких клиентов B2C в среде Commerce</span><span class="sxs-lookup"><span data-stu-id="77cc3-126">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="77cc3-127">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="77cc3-127">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
