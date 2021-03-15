---
title: Связывание сайта Dynamics 365 Commerce с интернет-каналом
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
ms.openlocfilehash: fc93441bd09deccdb8c7ecf955c0ec5177c0b31e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980031"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a>Связывание сайта Dynamics 365 Commerce с интернет-каналом

[!include [banner](includes/banner.md)]

В этом разделе объясняется, как связать сайт Microsoft Dynamics 365 Commerce с одним или несколькими интернет-магазинами. 

После подготовки среды электронной коммерции Dynamics 365 Commerce с помощью портала Microsoft Dynamics Lifecycle Services (LCS) можно приступать к созданию первого веб-сайта электронной коммерции. В качестве части начального создания сайта вы связываете сайт с ранее созданным интернет-магазином. На этом шаге сайт связывается с интернет-каналом и позволяет сайту показывать иерархию переходов, продукты, категории, цены, параметры доставки и все остальные, которые были определены в интернет-магазине.

Чтобы создать новый сайт и связать интернет-магазин с ним, в LCS выберите ссылку для среды разработки сайтов. Затем на странице для среды разработки сайта выберите пункт **Создать сайт**. В диалоговом окне **Создать сайт** необходимо предоставить некоторые базовые сведения о сайте. Полное описание информации, которую необходимо предоставить, см. в разделе [Создание нового сайта электронной коммерции](create-ecommerce-site.md).

После создания сайта можно убедиться, что он связан с интернет-магазином, выбрав вкладку **Продукты**. Должен отобразиться ассортимент продуктов, которые были выделены для интернет-магазина. Можно также использовать раскрывающееся поле в левом верхнем углу страницы для получения доступа к продуктам по категориям.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка доменного имени](configure-your-domain-name.md)

[Развертывание нового клиента электронной коммерции](deploy-ecommerce-site.md)

[Создание сайта электронной коммерции](create-ecommerce-site.md)

[Управление файлами robots.txt](manage-robots-txt-files.md)

[Пакетная отправка перенаправлений URL-адресов](upload-bulk-redirects.md)

[Настройка клиента B2C в Commerce](set-up-B2C-tenant.md)

[Настройка специальных страниц для входа пользователей](custom-pages-user-logins.md)

[Настройка нескольких клиентов B2C в среде Commerce](configure-multi-B2C-tenants.md)

[Добавление поддержки сети доставки контента (CDN)](add-cdn-support.md)

[Включение обнаружения магазинов на основе местоположения](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]