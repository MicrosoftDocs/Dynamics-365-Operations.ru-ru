---
title: Связывание веб-сайта Dynamics 365 Commerce с каналом продаж через Интернет
description: В этом разделе объясняется, как связать сайт Microsoft Dynamics 365 Commerce с одним или несколькими интернет-магазинами.
author: bicyclingfool
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 60ead45e6e2b7fea8f04371310ff4315205e11f6e0968e5f8bbc6a29c5f26e18
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737661"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a>Связывание веб-сайта Dynamics 365 Commerce с каналом продаж через Интернет

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