---
title: Включение обнаружения магазинов на основе местоположения
description: В этом разделе описывается, как включить обнаружение магазинов на основе местоположения для сайта Dynamics 365 Commerce.
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a542d6987280451910b4ff3bcfb3a109a0e028c6
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697620"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="15969-103">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="15969-103">Enable location-based store detection</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="15969-104">В этом разделе описывается, как включить обнаружение магазинов на основе местоположения для сайта Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="15969-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="15969-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="15969-105">Overview</span></span>

<span data-ttu-id="15969-106">Обнаружение магазинов на основе местоположения в Commerce позволяет предоставлять соответствующее содержимое сайта клиентам на основе их местоположения.</span><span class="sxs-lookup"><span data-stu-id="15969-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="15969-107">Если обнаружение магазинов на основе местоположения включено, служба отображения Commerce использует информацию о стране/регионе из IP-адреса веб-браузера клиента, чтобы направлять пользователя в оптимальную доступную географическую конфигурацию сайта.</span><span class="sxs-lookup"><span data-stu-id="15969-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="15969-108">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="15969-108">Privacy notice</span></span>

<span data-ttu-id="15969-109">При включении функции обнаружения магазинов на основе местоположения сведения из браузера клиента отправляются в службу определения местоположения Microsoft.</span><span class="sxs-lookup"><span data-stu-id="15969-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="15969-110">Эти сведения затем используются для предоставления содержимого клиенту, которое имеют отношение к его местоположению.</span><span class="sxs-lookup"><span data-stu-id="15969-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="15969-111">Как сведения, которые отправляются из браузера клиента, так и сведения на основе местоположения, возвращаемые клиенту, должны соответствовать политике конфиденциальности и cookie-файлов.</span><span class="sxs-lookup"><span data-stu-id="15969-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="15969-112">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="15969-112">Turn on location-based store detection</span></span>

<span data-ttu-id="15969-113">Чтобы включить обнаружение магазинов на основе местоположения в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="15969-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="15969-114">В средстве разработки перейдите на ваш сайт.</span><span class="sxs-lookup"><span data-stu-id="15969-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="15969-115">В области переходов слева выберите **Управление сайтом**.</span><span class="sxs-lookup"><span data-stu-id="15969-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="15969-116">Выберите **Параметры сайта**.</span><span class="sxs-lookup"><span data-stu-id="15969-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="15969-117">Установите для параметра **Включить обнаружение магазинов на основе местоположения** значение **Вкл.**</span><span class="sxs-lookup"><span data-stu-id="15969-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15969-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="15969-118">Additional resources</span></span>

[<span data-ttu-id="15969-119">Обзор интернет-магазина</span><span class="sxs-lookup"><span data-stu-id="15969-119">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="15969-120">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="15969-120">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="15969-121">Развертывание нового сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="15969-121">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="15969-122">Связывание веб-сайта с каналом</span><span class="sxs-lookup"><span data-stu-id="15969-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="15969-123">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="15969-123">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="15969-124">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="15969-124">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="15969-125">Настройка специальных страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="15969-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
