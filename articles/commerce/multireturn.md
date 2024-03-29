---
title: Возврат номенклатур по нескольким заказам и накладным клиента
description: В этой статье описывается функциональность, обеспечивающая возвраты по нескольким заказам и накладным клиента в Dynamics 365 Commerce.
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 65ef700db5a81c49a962fd388af54e7811c088d2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890331"
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
