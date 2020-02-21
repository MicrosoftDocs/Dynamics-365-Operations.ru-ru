---
title: Возврат номенклатур по нескольким заказам и накладным клиента
description: В этом разделе описывается функциональность, обеспечивающая возвраты по нескольким заказам и накладным клиента в Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: c5f17424f0837344030f9ce2d2d037cde08c4e49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004466"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Возврат номенклатур по нескольким заказам и накладным клиента

[!include [banner](includes/banner.md)]


Возврат может выполняться по нескольким заказам и накладным. 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a>Настройка Commerce для поддержки возвратов по нескольким заказам и накладным клиента

1. Выберите **Параметры Commerce \> Клиентские заказы**.
1. Включите параметр **Разрешить возврат по нескольким заказам**. 

## <a name="process-returns"></a>Обработка возвратов

После включения этого параметра и синхронизации изменений с магазинами кассир в магазине может выбрать для клиента несколько заказов на продажу, чтобы обработать возврат.

При выборе заказов отображается список всех доступных для возврата продуктов по всем накладным для этих заказов. Кассир может затем выбрать возвращаемые продукты. Создается один заказ на возврат для всех выбранных продуктов.
