---
title: Обзор каналов
description: Этот раздел содержит обзор каналов в Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8ac188832bdaeba430eed7f08e91a9c2214a0e15
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219109"
---
# <a name="channels-overview"></a>Обзор каналов


[!include [banner](includes/banner.md)]

Этот раздел содержит обзор каналов в Microsoft Dynamics 365 Commerce. Она содержит сведения о задачах, которую следует выполнить как до, так и после настройки каждого канала.

## <a name="types-of-channels"></a>Типы каналов

Dynamics 365 Commerce поддерживает три различных типа каналов: розница, центр обработки вызовов и интернет-каналы.

### <a name="retail-channels"></a>Каналы розничной торговли

Каналы розничной торговли представляют собой стандартные физические магазины. У каждого магазина свои кассы POS, приходные и расходные счета и персонал. 

### <a name="call-center-channels"></a>Каналы центра обработки вызовов

Каналы центра обработки вызовов представляют порядок и управление клиентами в центре обработки вызовов.

### <a name="online-channels"></a>Интерактивные каналы

Интернет-каналы представляют собой интернет-магазины электронной коммерции. После создания интернет-канала необходимо создать сайт с помощью построителя сайтов Microsoft Dynamics 365 Commerce или другого решения электронной коммерции сторонних производителей.

## <a name="channel-setup-basics"></a>Основы настройки канала

Настройка канала выполняется в инструменте Commerce. У каждого канала могут быть собственные методы оплаты, ценовые группы, иерархии продуктов, ассортименты и набор продуктов. После создания канала назначаются продукты, которые должны использоваться и продаваться в магазине. Каждый тип канала имеет уникальный набор функций, которые могут может потребоваться настроить. Например, каналу розничной торговли требуется назначить сотрудников, кассы и клиентов. После создания нового канала его необходимо назначить организационной иерархии.

## <a name="channel-setup-prerequisites"></a>Необходимые условия для настройки каналов

Перед настройкой канала необходимо выполнить некоторые условия на основе типа канала. Дополнительные сведения см. в разделе [Необходимые условия для настройки каналов](channels-prerequisites.md).

## <a name="set-up-a-channel"></a>Настройка канала

После выполнения необходимых условий дальнейшие инструкции см. по следующим ссылкам.

- [Настройка канала розничной торговли](channel-setup-retail.md)
- [Настройка канала центра обработки вызовов](channel-setup-callcenter.md)
- [Настройка интернет-канала](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a>Дополнительные ресурсы

[Необходимые условия для настройки каналов](channels-prerequisites.md)

[Настройка канала розничной торговли](channel-setup-retail.md)
    
[Настройка интернет-канала](channel-setup-online.md)

[Настройка канала центра обработки вызовов](channel-setup-callcenter.md)

[Настройка организационных иерархий](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]