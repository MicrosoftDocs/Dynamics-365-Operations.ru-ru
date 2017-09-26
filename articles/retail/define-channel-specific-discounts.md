---
title: "Определение скидок, специфичных для канала"
description: "Продавцы часто устанавливают различные скидки в различных каналах. В этом разделе рассматриваются понятия, которые необходимо знать для создания скидки для конкретного канала."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: d40c37628f03a7605e04b95339072a67806f2fa1
ms.contentlocale: ru-ru
ms.lasthandoff: 06/20/2017

---

# <a name="define-channel-specific-discounts"></a>Определение скидок, специфичных для канала

[!include[banner](includes/banner.md)]


Продавцы часто устанавливают различные скидки в различных каналах. В этом разделе рассматриваются понятия, которые необходимо знать для создания скидки для конкретного канала. 

<a name="channel-specific-discounts"></a>Скидки, специфичные для канала
--------------------------

Продавцы часто предлагаю различные скидки в различных каналах. Это может быть сделано для того, чтобы учесть конъюнктуру местного рынка, или для борьбы с конкурирующими розничными продавцами.

В Microsoft Dynamics 365 for Retail используются ценовые группы, чтобы определить специфические для канала скидки. Ценовые группы можно назначить одной или нескольким из следующих объектов: каналы, каталоги, назначения и программы лояльности. В этой статье обсуждаются каналы, но эти же концепции применимы к скидкам по каталогу, скидкам для назначений и скидкам по программам лояльности.

## <a name="price-groups"></a>Группы цен

[![Группы цен](./media/price-groups-1024x608.png)](./media/price-groups.png)

Диаграмма выше иллюстрирует отношение между объектами, которые могут находиться в проводке (канал, каталог, назначение, клиент, карточка лояльности) и различные типы скидок, которые можно настроить. Все проводки происходят в канале, поэтому канал гарантировано присутствует в проводке. Остальные объекты необязательные. На каждой из страниц справочника имеется ссылка на странице связанных ценовых групп, где можно просматривать и добавлять ценовые группы по мере необходимости. Ценовая группа используется для того, чтобы связать четыре различных типов объектов со скидками, корректировками цен и коммерческими соглашениями. Мы рекомендуем планировать стратегию того, как вы называете ваши ценовые группы, чтобы систематизировать их. Один вариант заключается в использовании буквенного или цифрового префикса или суффикса, чтобы различать разные типы. Например, 1-xxxxx для ценовых групп канала и 2-xxxxx для ценовых групп каталога. Предусмотрено четыре страницы запросов, которые фокусируются на каждом из розничных объектов, с которыми могут быть связаны скидки.

-   **Группы цен канала розничной торговли** — эта страница показывает список каналов и скидок, связанных совместно для каждой ценовой группы.
-   **Ценовые группы каталога** — эта страница показывает список каталогов и скидок, связанных совместно для каждой ценовой группы.
-   **Группы цен программ лояльности** — эта страница показывает список программ лояльности и скидок, связанных совместно для каждой ценовой группы.
-   **Ценовые группы назначений** — эта страница показывает список назначений и скидок, связанных совместно для каждой ценовой группы.

## <a name="example-channel-discount-set-up"></a>Пример настройки скидки для канала
Следующий пример иллюстрирует задачи, входящие в настройку скидки для канала.

1.  В этом примере имеется канал с названием **Хьюстоном**, и вы собираетесь создать новую скидку с названием **Снова в школу**.
2.  Поскольку стратегия ценообразования и скидок включает в себя возможность скидок для канала, при создании канала всегда создается специфическая для канала ценовая группа.
3.  Вы имеете ценовую группу **Хьюстон-ЦГ**, которая задана каналу **Хьюстон**.
4.  После создания новой скидки **Снова в школу** требуется нажать **Группы цен** вверху страницы **Скидка**. Открывается страница **Ценовые группы скидок**. Затем нажмите **Создать** и выберите ценовую группу **Хьюстон-ЦГ**.
5.  Теперь вы можете включить скидку и передать ее в канал.

 

<a name="see-also"></a>См. также
--------

[Корректировки цены и скидки](price-adjustments-discounts.md)



