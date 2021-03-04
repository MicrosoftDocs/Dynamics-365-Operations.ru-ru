---
title: Включение обнаружения магазинов на основе местоположения
description: В этом разделе описывается, как включить обнаружение магазинов на основе местоположения для сайта Dynamics 365 Commerce.
author: brianshook
manager: annbe
ms.date: 07/02/2020
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
ms.openlocfilehash: f87d29a8cffb70e4dea211cea7538e5e4c85295c
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517314"
---
# <a name="enable-location-based-store-detection"></a>Включение обнаружения магазинов на основе местоположения


[!include [banner](includes/banner.md)]

В этом разделе описывается, как включить обнаружение магазинов на основе местоположения для сайта Dynamics 365 Commerce.

## <a name="overview"></a>Обзор

Обнаружение магазинов на основе местоположения в Commerce позволяет предоставлять соответствующее содержимое сайта клиентам на основе их местоположения. Если обнаружение магазинов на основе местоположения включено, служба отображения Commerce использует информацию о стране/регионе из IP-адреса веб-браузера клиента, чтобы направлять пользователя в оптимальную доступную географическую конфигурацию сайта.

## <a name="privacy-notice"></a>Уведомление о конфиденциальности

При включении функции обнаружения магазинов на основе местоположения сведения из браузера клиента отправляются в службу определения местоположения Microsoft. Эти сведения затем используются для предоставления содержимого клиенту, которое имеют отношение к его местоположению. Как сведения, которые отправляются из браузера клиента, так и сведения на основе местоположения, возвращаемые клиенту, должны соответствовать политике конфиденциальности и cookie-файлов.

## <a name="turn-on-location-based-store-detection"></a>Включение обнаружения магазинов на основе местоположения

Чтобы включить обнаружение магазинов на основе местоположения в Commerce, выполните следующие действия.

1. В средстве разработки перейдите на ваш сайт.
1. В области переходов слева выберите **Управление сайтом**.
1. Выберите **Параметры сайта**.
1. Установите для параметра **Включить обнаружение магазинов на основе местоположения** значение **Вкл.**

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка доменного имени](configure-your-domain-name.md)

[Развертывание нового клиента электронной коммерции](deploy-ecommerce-site.md)

[Создание сайта электронной коммерции](create-ecommerce-site.md)

[Связывание сайта Dynamics 365 Commerce с интернет-каналом](associate-site-online-store.md)

[Управление файлами robots.txt](manage-robots-txt-files.md)

[Пакетная отправка перенаправлений URL-адресов](upload-bulk-redirects.md)

[Настройка клиента B2C в Commerce](set-up-B2C-tenant.md)

[Настройка специальных страниц для входа пользователей](custom-pages-user-logins.md)

[Настройка нескольких клиентов B2C в среде Commerce](configure-multi-B2C-tenants.md)

[Добавление поддержки сети доставки контента (CDN)](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]