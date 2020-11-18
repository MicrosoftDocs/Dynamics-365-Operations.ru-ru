---
title: Модуль выбора сайта
description: В этом разделе описываются модуль выбора сайта, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: bd54695f54b501631f916328c05bfd47e538d50d
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055838"
---
# <a name="site-selector-module"></a>Модуль выбора сайта

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

В этом разделе описываются модуль выбора сайта, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Обзор

Если предприятие имеет различные сайты для рынков, регионов и языковых стандартов, пользователям сайта необходим простой способ переключения между сайтами и выбора предпочтительного сайта для покупок. Для поддержки этого сценария модуль выбора сайта позволяет пользователям возможность просматривать несколько сайтов.

Модуль выбора сайтов должен быть сконфигурирован с помощью списка сайтов (рынков, регионов или языковых стандартов), которые могут просматривать пользователи сайта.

> [!NOTE]
> Модуль выбора сайта доступен в выпуске Dynamics 365 Commerce 10.0.14.

На следующем рисунке показан пример модуля выбора сайта, который указан в заголовке страницы сайта.

![Пример модуля выбора сайтов в заголовке страницы сайта](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a>Свойства модуля выбора сайта

| Имя свойства | значение                 | описание |
|---------------|-----------------------|-------------|
| Заголовок       | Текст                  | Заголовок модуля. |
| Параметры сайта  | Имя, изображение, URL-адрес      | Это свойство определяет имя, ссылку на домашнюю страницу сайта и необязательное изображение, которое будет отображаться для каждого сайта, включенного в модуль. Изображение может быть флагом или некоторым представлением рынка, региона или языкового стандарта. |

## <a name="add-a-site-selector-module-to-a-page"></a>Добавление модуля выбора сайта на страницу

Модуль выбора сайта может быть добавлен в [модуль заголовка](author-header-module.md) в гнезде выбора сайта. После его добавления можно определить заголовок модуля и параметры сайта.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор библиотеки модулей](starter-kit-overview.md)

[Модуль верхнего колонтитула](author-header-module.md)

[Модуль иерархической навигации](add-breadcrumb.md)

[Модуль меню навигации](nav-menu-module.md)