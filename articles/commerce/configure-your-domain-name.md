---
title: Настройка доменного имени
description: В этой статье объясняется, как настроить имя домена для сайта электронной коммерции Microsoft Dynamics 365.
author: josaw1
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.search.form: ''
ms.openlocfilehash: 298ce84008e60cc82a494320b6a41f35338508c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278633"
---
# <a name="configure-your-domain-name"></a>Настройка доменного имени


[!include [banner](includes/banner.md)]

В этой статье объясняется, как настроить имя домена для сайта электронной коммерции Microsoft Dynamics 365. 

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
