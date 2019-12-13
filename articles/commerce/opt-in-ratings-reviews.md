---
title: Соглашение на использование оценок и отзывов
description: В этой теме объясняется, как согласиться на использование оценок и отзывов на веб-сайте Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697988"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Соглашение на использование оценок и отзывов

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

В этой теме объясняется, как согласиться на использование оценок и отзывов на веб-сайте Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Обзор

Решение оценок и отзывов — это омниканальное решение, которое можно сделать доступным в Dynamics 365 Commerce с помощью Microsoft Dynamics Lifecycle Services (LCS). LCS — это портал администрирования, который используется в розничных магазинах для управления средами от подготовки до выведения из эксплуатации.

Если вы хотите использовать решение оценок и отзывов на веб-сайте Commerce, вы должны сначала согласиться.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Соглашение на использование оценок и отзывов

Чтобы согласиться на использование оценок и отзывов на веб-сайте, выполните следующие действия.

1. Выполните шаги раздела [Развертывание нового сайта электронной коммерции](deploy-ecommerce-site.md).
1. Пока вы все еще находитесь в LCS, перейдите к пункту **Настройка развертывания Retail \> Другие параметры**.
1. Установите для параметра **Включить службу оценок и отзывов** значение **Да**.
1. В поле **Группа безопасности AAD для модератора оценок и отзывов (код объекта группы безопасности)** введите идентификатор группы безопасности Microsoft Azure Active Directory (Azure AD), включающий модераторов оценок и отзывов.

    ![Соглашение на использование оценок и отзывов](media/LCS_RnR_Preference.png)

1. Завершите процесс инициализации электронной коммерции.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор оценок и отзывов](ratings-reviews-overview.md)

[Управление оценками и отзывами](manage-reviews.md)

[Настройка оценок и отзывов](configure-ratings-reviews.md)

[Синхронизация оценок продуктов в Dynamics 365 Retail](sync-product-ratings.md)
