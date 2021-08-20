---
title: Соглашение на использование оценок и отзывов
description: В этой теме объясняется, как согласиться на использование оценок и отзывов на веб-сайте Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 051163f5a3f7070bdf8377b3ea6ab4e3689927fd6c46d5759b56fcbdada51906
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741096"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Соглашение на использование оценок и отзывов

[!include [banner](includes/banner.md)]

В этой теме объясняется, как согласиться на использование оценок и отзывов на веб-сайте Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Обзор

Решение оценок и отзывов — это омниканальное решение, которое можно сделать доступным в Dynamics 365 Commerce с помощью Microsoft Dynamics Lifecycle Services (LCS). LCS — это портал администрирования, который используется в розничных магазинах для управления средами от подготовки до выведения из эксплуатации.

Если вы хотите использовать решение с оценками и обзорами на веб-сайте Commerce, вы должны принять оценки и обзоры во время развертывания узла электронной коммерции Dynamics 365 Commerce.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Соглашение на использование оценок и отзывов

Чтобы согласиться на использование оценок и отзывов на веб-сайте, выполните следующие действия.

1. Выполните шаги раздела [Развертывание нового сайта электронной коммерции](deploy-ecommerce-site.md).
1. Пока вы все еще находитесь в LCS, перейдите к пункту **Настройка развертывания Retail \> Другие параметры**.
1. Установите для параметра **Включить службу оценок и отзывов** значение **Да**.
1. В поле **Группа безопасности AAD для модератора оценок и отзывов (код объекта группы безопасности)** введите идентификатор группы безопасности Microsoft Azure Active Directory (Azure AD), включающий модераторов оценок и отзывов.

    ![Соглашение на использование оценок и отзывов.](media/LCS_RnR_Preference.png)

1. Завершите процесс инициализации электронной коммерции.

> [!NOTE] 
> Если вы являетесь существующим клиентом Dynamics 365 Commerce, который уже развернул сайт электронной коммерции, не прибегая к оценкам и обзорам, а теперь хотите использовать оценки и обзоры из пакета Dynamics 365 Commerce, отправьте запрос на обслуживание. Сведения о том, как отправлять запрос на обслуживание, см. в разделе [Процесс отправки запросов на обслуживание](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор оценок и отзывов](ratings-reviews-overview.md)

[Управление оценками и отзывами](manage-reviews.md)

[Настройка оценок и отзывов](configure-ratings-reviews.md)

[Синхронизация оценок продуктов в Dynamics 365 Commerce](sync-product-ratings.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]