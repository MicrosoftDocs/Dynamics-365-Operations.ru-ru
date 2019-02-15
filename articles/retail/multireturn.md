---
title: Возврат номенклатур по нескольким заказам и накладным клиента
description: В этой теме рассматривается функциональность, обеспечивающая возврат по нескольким заказам и накладным клиента в Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 1/08/2019
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
ms.openlocfilehash: d2cf6f92e90ef196827abb599c65c732615ec7bb
ms.sourcegitcommit: e72eae546d48d41d4b07ff78cfc0242c32b793e7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2019
ms.locfileid: "373076"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Возврат номенклатур по нескольким заказам и накладным клиента

[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

В Dynamics 365 for Finance and Operations версии 10.0 возвраты могут выполняться по нескольким заказам и накладным, тогда как в выпусках до 10.0 одновременная обработка была возможна только по одной накладной. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>Настройка Retail для поддержки возвратов по нескольким заказам и накладным клиента

1. Выберите **Параметры Retail \> Клиентские заказы**.
1. Включите параметр **Разрешить возврат по нескольким заказам**. 

## <a name="process-returns"></a>Обработка возвратов

После включения этого параметра и синхронизации изменений с магазинами кассир в магазине может выбрать для клиента несколько заказов на продажу, чтобы обработать возврат.

При выборе заказов отображается список всех доступных для возврата продуктов по всем накладным для этих заказов. Кассир может затем выбрать возвращаемые продукты. Создается один заказ на возврат для всех выбранных продуктов.
