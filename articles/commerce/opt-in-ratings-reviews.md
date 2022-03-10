---
title: Соглашение на использование оценок и отзывов
description: В этой теме объясняется, как согласиться на использование оценок и отзывов на веб-сайте Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/16/2020
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
ms.openlocfilehash: 19c3e8b32654f7c4b7803c547e9d5692f9fc461b
ms.sourcegitcommit: 4d52c67f52ad0add63cd905df61367b344389069
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/16/2022
ms.locfileid: "8311937"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Соглашение на использование оценок и отзывов

[!include [banner](includes/banner.md)]

В этой теме объясняется, как согласиться на использование оценок и отзывов на веб-сайте Microsoft Dynamics 365 Commerce.

Решение оценок и отзывов — это омниканальное решение, которое можно сделать доступным в Dynamics 365 Commerce с помощью Microsoft Dynamics Lifecycle Services (LCS). LCS — это портал администрирования, который используется в розничных магазинах для управления средами от подготовки до выведения из эксплуатации.

Если вы хотите использовать решение с оценками и обзорами на веб-сайте Commerce, вы должны принять оценки и обзоры во время развертывания узла электронной коммерции Dynamics 365 Commerce.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Соглашение на использование оценок и отзывов

Чтобы согласиться на использование оценок и отзывов на веб-сайте, выполните следующие действия.

1. Выполните шаги раздела [Развертывание нового сайта электронной коммерции](deploy-ecommerce-site.md).
1. Пока вы все еще находитесь в LCS, перейдите к пункту **Настройка развертывания Retail \> Другие параметры**.
1. Установите для параметра **Включить службу оценок и отзывов** значение **Да**.
1. В поле **Группа безопасности AAD для модератора оценок и отзывов** введите идентификатор группы безопасности Microsoft Azure Active Directory (Azure AD), включающий модераторов оценок и отзывов.

    ![Соглашение на использование оценок и отзывов.](media/LCS_RnR_Preference_2.png)

1. Завершите процесс инициализации электронной коммерции.

> [!NOTE] 
> Если вы являетесь существующим клиентом Dynamics 365 Commerce, который уже развернул сайт электронной коммерции, не прибегая к оценкам и обзорам, а теперь хотите использовать оценки и обзоры из пакета Dynamics 365 Commerce, отправьте запрос на обслуживание. Сведения о том, как отправлять запрос на обслуживание, см. в разделе [Процесс отправки запросов на обслуживание](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор оценок и отзывов](ratings-reviews-overview.md)

[Управление оценками и отзывами](manage-reviews.md)

[Настройка оценок и отзывов](configure-ratings-reviews.md)

[Синхронизация оценок продуктов в Dynamics 365 Commerce](sync-product-ratings.md)

[Включение модератором публикации оценок и отзывов вручную](manual-publish-rating-reviews.md)

[Импорт и экспорт оценок и отзывов](import-export-reviews.md)

[Настройка проверки подлинности между службами](service-to-service-auth.md)

[Оценки и отзывы — Вопросы и ответы](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
