---
title: Создание контролируемых рекомендаций вручную
description: В этой теме объясняется, как менеджер по сбыту может вручную создавать списки продуктов для клиентов Microsoft Dynamics 365 Commerce и управлять ими.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f8142bb8a23e467ba38e3d22b070c2d275c95f506a3cc263dcd2986f60fb5860
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729898"
---
# <a name="manually-create-curated-recommendations"></a>Создание контролируемых рекомендаций вручную

[!include [banner](includes/banner.md)]

В этой теме объясняется, как менеджер по сбыту может вручную создавать списки рекомендаций по продуктам для клиентов Microsoft Dynamics 365 Commerce и управлять ими.

Проверенные списки представляют собой наборы отдельных материалов, созданных и проверенных людьми.  

## <a name="create-a-new-list"></a>Создание нового списка

Для создания проверенного списка рекомендаций продуктов выполните следующие действия.

1. Выберите **Retail и Commerce &gt; Рекомендации продуктов &gt; Списки рекомендаций**.
1. Выберите **Создать**.
1. В поле **Код списка** введите значение.
1. В поле **Имя списка** введите значение.
    - **Имя списка** является названием списка, которое будет отображаться в разделе проверенных списков модуля **Семейство продуктов**.
1. Чтобы добавить продукты в список, выберите **Добавить продукты**.
1. Чтобы изменить порядок продуктов в списке, введите значение в столбец **Порядок просмотра**.
    - Если два продукта имеют одинаковое значение порядок отображения, то окончательный порядок этих двух результатов также будет зависит от серверной части.
1. Выберите **Сохранить**, чтобы сохранить список.

## <a name="example-list"></a>Пример списка

![Пример проверенного списка в серверной части.](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор рекомендаций по продуктам](product-recommendations.md)

[Включение Azure Data Lake Storage в среде Dynamics 365 Commerce](enable-adls-environment.md)

[Включить рекомендации по продуктам](enable-product-recommendations.md)

[Включение персонализированных рекомендаций](personalized-recommendations.md)

[Отказ от персонализированных рекомендаций](personalization-gdpr.md)

[Включение рекомендаций "покупать похожие образы"](shop-similar-looks.md)

[Добавление рекомендаций по продуктам в POS](product.md)

[Добавление рекомендаций на экран проводок](add-recommendations-control-pos-screen.md)

[Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения](modify-product-recommendation-results.md)

[Создание рекомендаций с помощью демонстрационных данных](product-recommendations-demo-data.md)

[Вопросы и ответы по рекомендациям по продуктам](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]