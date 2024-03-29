---
title: Иерархии Commerce
description: В этой статье описываются иерархии в Dynamics 365 Commerce.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.industry: Retail
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
ms.openlocfilehash: ce196acc8c4bced865b983b12d72f8bc6e4d02a0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271886"
---
# <a name="commerce-hierarchies"></a>Иерархии Commerce

[!include [banner](includes/banner.md)]

В этой статье описываются иерархии в Dynamics 365 Commerce.

Можно создать иерархию категорий для организации продукты, которые продаются через ваши каналы. Иерархии продуктов можно использовать для классификации или группировки продуктов. Эти продукты затем можно использовать для создания ассортиментов и программ лояльности клиентов. Можно также назначить атрибуты продукции и свойства, присваивать ценовую структуру, включить продукты в специальные акции, использовать продукцию для отчетности. Можно создать одну иерархию категорий, чтобы представить все продукты и категории в вашей организации, а затем воспользоваться этой иерархией категорий для достижения нескольких целей. Кроме того, можно создать несколько иерархий категорий для специальных целей, например продвижения продукции. При создании иерархии продукции необходимо назначить тип иерархии категорий, чтобы обозначить цель иерархии категорий. Например, только иерархии продуктов, которым назначен тип **Навигационная иерархия Commerce**, отображаются при просмотре продуктов по категориям через Интернет или в пункте продажи (POS).

## <a name="hierarchy-types"></a>Типы иерархии

В следующей таблице перечислены типы доступных иерархий категорий и указана цель каждого типа.

| Тип иерархии категорий       | Цель |
|-------------------------------|---------|
| Иерархия продуктов      | Воспользуйтесь иерархией этого типа для определения общей иерархии продуктов для вашей организации. Можно использовать данный тип иерархии для мерчендайзинга, ценообразования и специальных акций, отчетности и планирования ассортимента. Только одна иерархия продукции может быть присвоена этому типу иерархий. |
| Дополнительная иерархия | Этот тип иерархии используется для дополнительных иерархий категорий, которые требуется создать. Например, весной проводится специальная акция на купальники. Таким образом, нужно включить купальники в отдельную иерархию категорий и применить рекламные цены к разным категориям продуктов этой иерархии. |
| Навигационная иерархия   | Используйте этот тип иерархии, чтобы группировать и систематизировать продукты по категориям, чтобы эти продукты можно было просматривать по Интернету или в пункте продаж (POS). |

С помощью иерархии категорий можно структурировать продукты, настраивать и вести атрибуты и свойства продукции на уровне категорий. Эти атрибуты и свойства включают настройки для аналитик продукции и настройки пункта продаж (POS). Любые продукты, назначаемые категориям, автоматически наследуют определенные пользователем атрибуты и свойства. Можно также скопировать настройки свойств любой продукции на несколько продуктов в выбранной категории одновременно.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
