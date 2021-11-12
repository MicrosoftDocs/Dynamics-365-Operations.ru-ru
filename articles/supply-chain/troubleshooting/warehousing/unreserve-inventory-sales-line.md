---
title: Невозможно отменить резервирование запасов по строке заказа на продажу
description: При наличии открытой работы для строки продаж и попытке снять резервирование запасов в строке будет выведено сообщение об ошибке. Выполните или удалите работу, чтобы освободить резервирование.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1a042065dc4cd637aff58e55cf16179b7022f6ca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477425"
---
# <a name="cant-unreserve-inventory-on-a-sales-order-line"></a>Невозможно отменить резервирование запасов по строке заказа на продажу

## <a name="symptoms"></a>Симптомы

При наличии открытой работы для строки заказа на продажу и попытке снять резервирование запасов в этой строке появится следующее сообщение об ошибке:

> Не удается удалить резервирования в связи с наличием зависимой от них работы.

## <a name="resolution"></a>Решение

Выясните, существует ли открытая работа группы упаковки, чтобы переместить номенклатуру из станции упаковки в другое местоположение (например, *Дверь отсека*). Просмотрите записи на страницах **Журнал создания работ** и **Сведения о работе**, чтобы определить, что физически резервирует запасы, а затем выполните или удалите работу, чтобы освободить резервирование.