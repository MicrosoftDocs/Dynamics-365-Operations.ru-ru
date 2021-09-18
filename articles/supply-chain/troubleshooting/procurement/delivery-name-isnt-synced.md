---
title: После изменения адреса доставки заказа на покупку имя доставки не синхронизируется
description: После изменения адреса поставки в заголовке заказа на покупку имя доставки не синхронизируется
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 588d1ef6250d249aa4fc9da4f5125e9a34c0255f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477384"
---
# <a name="the-delivery-name-isnt-synced-after-changing-a-purchase-order-delivery-address"></a>После изменения адреса доставки заказа на покупку имя доставки не синхронизируется

## <a name="symptoms"></a>Симптомы

Адрес в заголовке заказа на покупку обновляется до адреса, который не является адресом доставки. Хотя адрес обновляется в заказе на покупку, имя доставки не обновляется на основе обновленного адреса.

## <a name="resolution"></a>Решение

Такое поведение предусмотрено разработчиками. Выбранный адрес должен классифицироваться как адрес доставки. В противном случае имя доставки не обновляется в соответствии с выбранным адресом.
