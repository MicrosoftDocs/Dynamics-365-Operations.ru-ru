---
title: Исправление уведомления о поставке не может быть обработано
description: При попытке скорректировать уведомление о поставке после ее разноски появляется сообщение об ошибке. На этой странице объясняется, как корректировать разнесенные отборочные накладные для номенклатур, включенных для WMS.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bb0d827adff8abd8762bf2de844cad5574628e4b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477442"
---
# <a name="delivery-note-correction-cant-be-processed"></a>Исправление уведомления о поставке не может быть обработано

## <a name="symptoms"></a>Симптомы

После разноски уведомления о поставке его невозможно отменить, так как кнопка **Отмена** недоступна. Вы также не можете скорректировать уведомление о поставке. При попытке вы получите следующее сообщение об ошибке:

> Исправление уведомления о поставке не может быть обработано. Уведомление о поставке содержит только номенклатуры, которые подлежат процессам управления складом, так как они не поддерживаются исправлением уведомления о поставке.

## <a name="resolution"></a>Решение

Для корректировки разнесенных отборочных накладных для номенклатур, включенных для расширенного управления складом (WMS), разноска должна выполняться из загрузки, а не напрямую из заказа.