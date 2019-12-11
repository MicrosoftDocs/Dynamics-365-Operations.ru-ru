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
ms.openlocfilehash: 7a988f533757cc3f8555fcf4fb724a22a5b014f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770466"
---
# <a name="configure-your-domain-name"></a>Настройка доменного имени

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

В этой теме объясняется, как настроить имя домена для сайта электронной коммерции Microsoft Dynamics 365. 

## <a name="add-domains-during-e-commerce-initialization"></a>Добавление доменов во время инициализации электронной коммерции

Чтобы связать домены с вашей средой электронной коммерции, выполните инициализацию электронной коммерции, как описано в разделе [Развертывание нового сайта электронной коммерции](deploy-ecommerce-site.md). Во время инициализации вам необходимо предоставить информацию, которая будет использоваться для подготовки среды электронной коммерции. В поле **Поддерживаемые имена узлов** добавьте все домены, которые планируется использовать в этой среде. Несколько доменов следует разделять точками с запятой. Таким образом, домены настраиваются во всех необходимых компонентах электронной коммерции, и они готовы к использованию при переключении трафика из сети доставки содержимого (CDN) или веб-сервера и направления его на внешний интерфейс электронной коммерции.

## <a name="add-domains-after-e-commerce-initialization"></a>Добавление доменов после инициализации электронной коммерции

Чтобы связать новые домены с вашей средой электронной коммерции после инициализации электронной коммерции необходимо отправить запрос на обслуживание.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор интернет-магазина](online-store-overview.md)

[Создание сайта электронной коммерции](create-ecommerce-site.md)

[Развертывание нового сайта электронной коммерции](deploy-ecommerce-site.md)

[Связывание веб-сайта с каналом](associate-site-online-store.md)

[Добавление поддержки сети доставки контента (CDN)](add-cdn-support.md)

[Включение обнаружения магазинов на основе местоположения](enable-store-detection.md)

[Настройка специальных страниц для входа пользователей](custom-pages-user-logins.md)
