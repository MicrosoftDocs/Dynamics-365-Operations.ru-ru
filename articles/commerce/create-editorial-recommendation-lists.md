---
title: Создание контролируемых рекомендаций вручную
description: В этой теме объясняется, как менеджер по сбыту может вручную создавать списки продуктов для клиентов Microsoft Dynamics 365 Commerce и управлять ими.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
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
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b39ef61e7dabdd8a53d5666926a95cb7b9e6b9a5
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127729"
---
# <a name="manually-create-curated-recommendations"></a>Создание контролируемых рекомендаций вручную

[!include [banner](includes/banner.md)]

В этой теме объясняется, как менеджер по сбыту может вручную создавать списки рекомендаций продуктов для клиентов Microsoft Dynamics 365 Commerce и управлять ими.

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

![Пример проверенного списка в серверной части](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор рекомендаций по продуктам](product-recommendations.md)

[Включение ADLS в среде Dynamics 365 Commerce](enable-adls-environment.md)

[Включить рекомендации по продуктам](enable-product-recommendations.md)

[Включение персонализированных рекомендаций](personalized-recommendations.md)

[Отказ от персонализированных рекомендаций](personalization-gdpr.md)

[Добавление списков рекомендаций на сайт электронной коммерции](add-reco-list-to-page.md)

[Добавление рекомендаций по продуктам в POS](product.md)

[Добавление рекомендаций на экран проводки](add-recommendations-control-pos-screen.md)

[Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения](modify-product-recommendation-results.md)

[Создание рекомендаций с помощью демонстрационных данных](product-recommendations-demo-data.md)

[Вопросы и ответы по рекомендациям по продуктам](faq-recommendations.md)
