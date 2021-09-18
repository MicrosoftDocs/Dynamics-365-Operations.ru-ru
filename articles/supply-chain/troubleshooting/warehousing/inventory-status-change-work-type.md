---
title: Невозможно выбрать изменение статуса запасов в качестве типа работы
description: Невозможно создать строку шаблона работы для изменения статуса запасов, так как тип работы используется только системными процессами. Выберите другой тип работы.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ad7f26f3235d15779583f9cdadeb4e6dca16242a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477450"
---
# <a name="cant-select-inventory-status-change-in-the-work-type-column"></a>Невозможно выбрать изменение статуса запасов в столбце типа работы

## <a name="symptoms"></a>Симптомы

При настройке Microsoft Dynamics 365 Supply Chain Management появляется следующее сообщение об ошибке:

> Невозможно создать строку шаблона работы для изменения статуса запасов, так как тип работы является недопустимым. Выберите другой тип работы.

## <a name="resolution"></a>Решение

Такое поведение предусмотрено разработчиками. Тип работы *Изменения статуса запасов* используется только в системных процессах. Это нельзя настроить. Так как список типов работы фиксируется как перечисление, дополнительные записи не могут быть отфильтрованы из выпадающего меню **Тип работы**.
