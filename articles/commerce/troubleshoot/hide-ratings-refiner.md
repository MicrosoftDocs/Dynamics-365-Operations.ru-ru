---
title: Уточнение оценок отображается на страницах результатов поиска и категорий, когда решение оценок и отзывов не включено
description: В этой статье содержатся инструкции по устранению неполадок, связанных с отображением уточнения оценок на страницах результатов поиска и категорий, если для узла электронной коммерции не активировано решение оценки и отзывов Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 09/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
manager: annbe
ms.openlocfilehash: 28a3cefd6aab81f5e7907bda457763f2306e5a1d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267386"
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
