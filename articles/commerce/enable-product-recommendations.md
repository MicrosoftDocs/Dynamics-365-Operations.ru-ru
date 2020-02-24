---
title: Включить рекомендации по продуктам
description: В этой теме объясняется, как создать рекомендации продуктов, которые основаны на искусственном интеллекте и машинном обучении (AI-ML), доступном клиентам Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024964"
---
# <a name="enable-product-recommendations"></a>Включить рекомендации по продуктам

[!include [banner](includes/banner.md)]

В этой теме объясняется, как создать рекомендации продуктов, которые основаны на искусственном интеллекте и машинном обучении (AI-ML), доступном клиентам Microsoft Dynamics 365 Commerce. Дополнительные сведения о списках рекомендаций продуктов см. в разделе [Обзор рекомендаций продуктов](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Предварительная проверка рекомендаций

Перед включением обратите внимание, что рекомендации продуктов поддерживаются только для клиентов Commerce, перенесших свои хранилища с помощью Azure Data Lake Storage (ADLS). 

Инструкции по включению ADLS см. в разделе [Включение ADLS в среде Dynamics 365](enable-ADLS-environment.md).

Кроме того, убедитесь, что измерения RetailSale включены. Для получения дополнительных сведений об этом процессе настройки перейдите [сюда.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>Включение рекомендаций

Чтобы включить рекомендации продуктов, сделайте следующее.

1. Выберите **Retail и Commerce &gt; Рекомендации продуктов &gt; Параметры рекомендаций**.
1. В списке общих параметров выберите **Списки рекомендаций**.
1. Для параметра **Включить рекомендации** выберите значение **Да**.

![включить рекомендации по продуктам](./media/enableproductrecommendations.png)

> [!NOTE]
> Эта процедура запускает процесс создания списков рекомендаций продуктов. До того, как списки будут доступны для просмотра на POS-терминале или в Dynamics 365 Commerce, может потребоваться несколько часов.

## <a name="configure-recommendation-list-parameters"></a>Настройка параметров списка рекомендаций

По умолчанию список рекомендаций продуктов на основе AI-ML предоставляет предлагаемые значения. Предлагаемые по умолчанию значения можно изменить в соответствии с потоком бизнеса. Дополнительные сведения об изменении параметров по умолчанию см. в разделе [Управление результатами рекомендаций продуктов на основе AI-ML](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Отображение рекомендаций на POS-устройствах

После включения рекомендаций в операционных отделах организации Commerce необходимо добавить панель рекомендаций на экран управления POS через инструмент макета. Для получения сведений об этом процессе см. [Добавление элемента управления рекомендациями на экране проводки на устройствах POS](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Включение персонализированных рекомендаций

Дополнительные сведения о получении персонализированных рекомендаций см. в разделе [Включение персонализированных рекомендаций](personalized-recommendations.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор рекомендаций по продуктам](product-recommendations.md)

[Включение персонализированных рекомендаций](personalized-recommendations.md)

[Добавление списков рекомендации продуктов на страницы](add-reco-list-to-page.md)

[Добавление панели рекомендаций к POS-устройствам](add-recommendations-control-pos-screen.md)

[Обзор модуля семейства продуктов](product-collection-module-overview.md)

[Включение ADLS в среде Dynamics 365](enable-ADLS-environment.md)

