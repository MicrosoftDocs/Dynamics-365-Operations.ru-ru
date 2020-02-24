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
ms.openlocfilehash: 304d8d2f05916295b9c6320561d6a25ff40df955
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003104"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="b487f-103">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="b487f-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b487f-104">В этом разделе описывается, как включить обнаружение магазинов на основе местоположения для сайта Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b487f-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="b487f-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="b487f-105">Overview</span></span>

<span data-ttu-id="b487f-106">Обнаружение магазинов на основе местоположения в Commerce позволяет предоставлять соответствующее содержимое сайта клиентам на основе их местоположения.</span><span class="sxs-lookup"><span data-stu-id="b487f-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="b487f-107">Если обнаружение магазинов на основе местоположения включено, служба отображения Commerce использует информацию о стране/регионе из IP-адреса веб-браузера клиента, чтобы направлять пользователя в оптимальную доступную географическую конфигурацию сайта.</span><span class="sxs-lookup"><span data-stu-id="b487f-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="b487f-108">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="b487f-108">Privacy notice</span></span>

<span data-ttu-id="b487f-109">При включении функции обнаружения магазинов на основе местоположения сведения из браузера клиента отправляются в службу определения местоположения Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b487f-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="b487f-110">Эти сведения затем используются для предоставления содержимого клиенту, которое имеют отношение к его местоположению.</span><span class="sxs-lookup"><span data-stu-id="b487f-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="b487f-111">Как сведения, которые отправляются из браузера клиента, так и сведения на основе местоположения, возвращаемые клиенту, должны соответствовать политике конфиденциальности и cookie-файлов.</span><span class="sxs-lookup"><span data-stu-id="b487f-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="b487f-112">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="b487f-112">Turn on location-based store detection</span></span>

<span data-ttu-id="b487f-113">Чтобы включить обнаружение магазинов на основе местоположения в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b487f-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b487f-114">В средстве разработки перейдите на ваш сайт.</span><span class="sxs-lookup"><span data-stu-id="b487f-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="b487f-115">В области переходов слева выберите **Управление сайтом**.</span><span class="sxs-lookup"><span data-stu-id="b487f-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="b487f-116">Выберите **Параметры сайта**.</span><span class="sxs-lookup"><span data-stu-id="b487f-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="b487f-117">Установите для параметра **Включить обнаружение магазинов на основе местоположения** значение **Вкл.**</span><span class="sxs-lookup"><span data-stu-id="b487f-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b487f-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b487f-118">Additional resources</span></span>

[<span data-ttu-id="b487f-119">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="b487f-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="b487f-120">Развертывание нового сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="b487f-120">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="b487f-121">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="b487f-121">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="b487f-122">Связывание веб-сайта с каналом</span><span class="sxs-lookup"><span data-stu-id="b487f-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="b487f-123">Управление файлами robots.txt</span><span class="sxs-lookup"><span data-stu-id="b487f-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="b487f-124">Настройка специальных страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="b487f-124">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="b487f-125">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="b487f-125">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
