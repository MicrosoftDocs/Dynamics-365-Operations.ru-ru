---
title: Синхронизация с ядром ценообразования Dynamics 365 Supply Chain Management по запросу
description: В этом разделе описывается, как использовать механизм ценообразования в Microsoft Dynamics 365 Supply Chain Management из Dynamics 365 Sales.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: ef4465144155130087b078f9f96911df38b62c41
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173185"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a>Синхронизация с ядром ценообразования Dynamics 365 Supply Chain Management по запросу

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management включает в себя механизм ценообразования, который обрабатывает торговые договора, прайс-листы, программы лояльности клиентов, рекламные акции и скидки. Механизм ценообразования использует сложные правила для определения наилучшей цены для данного предложения или заказа. При использовании двойной записи можно использовать как статическое ценообразование, так и механизм ценообразования из Dynamics 365 Supply Chain Management на страницах предложения и заказа в Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Использование механизма ценообразования из Supply Chain Management в Sales

1. В Sales выберите **Продажи \> Заказы**.
2. Выберите **Создать**, чтобы создать новый заказ, или выберите существующий заказ в списке **Мои заказы**.
3. Добавьте новую строку заказа.
4. При создании нового заказа выберите **Рассчитать цену заказа** на панели операций. При обновлении существующего заказа выберите **Пересчитать** на панели операций.

    Следующие поля автоматически заполняются:

    + Детальная сумма
    + % скидки
    + Скидка
    + Сумма без фрахта
    + Сумма фрахта
    + Итоговый налог
    + Итоговая сумма

## <a name="how-it-works"></a>Как это работает

При выборе пункта **Рассчитать цену заказа** в Sales функция **Итоговые значения** на вкладке **Заказ на продажу \> Просмотр** в Supply Chain Management вызывается для связанного заказа на продажу. Значения в итоговой сумме заказа в Sales используются для заполнения соответствующих полей в Supply Chain Management.

При расчете итога по заказу на продажу в Supply Chain Management в расчете оцениваются существующие торговые договоры и договоры продажи для клиента и продуктов, перечисленных в заказе на продажу. Эти сведения используются при расчете итоговых сумм. При выборе пункта **Рассчитать цену заказа** Sales автоматически отражает все настройки, выполненные в Supply Chain Management.

## <a name="limitations"></a>Ограничения

Когда поля в Sales заполнены, действуют следующие ограничения:

+ Настройка накладных расходов и распределения расходов в Supply Chain Management не воспроизводится в Sales.
+ В ценах не учитывается специальная розничная цена, указанная в поле **Канал розничной торговли** на странице строки заказа на продажу в Supply Chain Management.
+ Скидки, которые определены в разделе **Управление торговыми скидками** Supply Chain Management не рассматриваются.
