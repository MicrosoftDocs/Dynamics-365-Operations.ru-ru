---
title: Налоговая группа по умолчанию и скидка по оплате не заполняются из счета в накладной
description: Налоговая группа по умолчанию и скидка по оплате по умолчанию не заполняются из счета в накладной
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
ms.openlocfilehash: bb984eb17209dc92e336df5ad475bb0f70c6e35c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477409"
---
# <a name="default-tax-group-and-cash-discount-arent-filled-in-from-the-invoice-account"></a>Налоговая группа по умолчанию и скидка по оплате не заполняются из счета в накладной

## <a name="symptoms"></a>Симптомы

При использовании счета в накладной, отличающегося от счета клиента, налоговая группа по умолчанию и используемая по умолчанию скидка по оплате не заполняется из счета по накладной при создании заказа на покупку.

## <a name="resolution"></a>Решение

Такое поведение предусмотрено разработчиками. Значения по умолчанию для налоговой группы, скидок по оплате и другой ценовой информации основываются на счете клиента, а не на счете в накладной.
