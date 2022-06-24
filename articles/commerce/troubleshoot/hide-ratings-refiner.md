---
title: Уточнение оценок отображается на страницах результатов поиска и категорий, когда решение оценок и отзывов не включено
description: В этой статье содержатся инструкции по устранению неполадок, связанных с отображением уточнения оценок на страницах результатов поиска и категорий, если для узла электронной коммерции не активировано решение оценки и отзывов Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 09/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c35e176fc5673de194a81a3a4694a83f7bc9aa00
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885066"
---
# <a name="ratings-refiner-appears-on-search-results-and-category-pages-when-the-ratings-and-reviews-solution-isnt-enabled"></a>Уточнение оценок отображается на страницах результатов поиска и категорий, когда решение оценок и отзывов не включено

[!include [banner](../includes/banner.md)]

В этой статье содержатся инструкции по устранению неполадок, связанных с отображением уточнения оценок на страницах результатов поиска и категорий, если для узла электронной коммерции не активировано решение оценки и отзывов Microsoft Dynamics 365 Commerce.

## <a name="description"></a>описание

Уточнение оценок отображается на страницах результатов поиска и категорий в канале электронной коммерции, в котором не используются решения оценок и отзывов.

## <a name="resolution"></a>Решение

### <a name="enable-the-hide-rating-setting-in-commerce-site-builder"></a>Включение параметра "Скрывать оценки" в конфигураторе сайтов Commerce

Чтобы включить параметр **Скрывать оценки** в конфигураторе сайтов Commerce с тем, чтобы скрыть уточнение оценок на страницах результатов поиска и категорий, выполните следующие действия.

1. Перейдите к разделу **Параметры сайта \> Расширения**.
1. В разделе **Оценки и отзывы** установите флажок **Скрывать оценки**.
1. Выберите **Сохранить и опубликовать**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор оценок и отзывов](../ratings-reviews-overview.md)

[Соглашение на использование оценок и отзывов](../opt-in-ratings-reviews.md)
