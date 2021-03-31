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
# <a name="configure-your-domain-name"></a>Настройка доменного имени


[!include [banner](includes/banner.md)]

В этой теме объясняется, как настроить имя домена для сайта электронной коммерции Microsoft Dynamics 365. 

## <a name="add-domains-during-e-commerce-initialization"></a>Добавление доменов во время инициализации электронной коммерции

Чтобы связать домены с вашей средой электронной коммерции Dynamics 365 Commerce, выполните инициализацию электронной коммерции, как описано в разделе [Развертывание нового клиента электронной коммерции](deploy-ecommerce-site.md). Во время инициализации вам необходимо предоставить информацию, которая будет использоваться для подготовки среды электронной коммерции. В поле **Поддерживаемые имена узлов** добавьте все домены, которые планируется использовать в этой среде. Несколько доменов следует разделять точками с запятой. Таким образом, домены настраиваются во всех необходимых компонентах электронной коммерции, и они готовы к использованию при переключении трафика из сети доставки содержимого (CDN) или веб-сервера и направления его на внешний интерфейс электронной коммерции.

## <a name="add-domains-after-e-commerce-initialization"></a>Добавление доменов после инициализации электронной коммерции

Чтобы связать новые домены с вашей средой электронной коммерции после инициализации электронной коммерции необходимо отправить запрос на обслуживание.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Развертывание нового клиента электронной коммерции](deploy-ecommerce-site.md)

[Создание сайта электронной коммерции](create-ecommerce-site.md)

[Связывание сайта Dynamics 365 Commerce с интернет-каналом](associate-site-online-store.md)

[Управление файлами robots.txt](manage-robots-txt-files.md)

[Пакетная отправка перенаправлений URL-адресов](upload-bulk-redirects.md)

[Настройка клиента B2C в Commerce](set-up-B2C-tenant.md)

[Настройка специальных страниц для входа пользователей](custom-pages-user-logins.md)

[Настройка нескольких клиентов B2C в среде Commerce](configure-multi-B2C-tenants.md)

[Добавление поддержки сети доставки контента (CDN)](add-cdn-support.md)

[Включение обнаружения магазинов на основе местоположения](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]