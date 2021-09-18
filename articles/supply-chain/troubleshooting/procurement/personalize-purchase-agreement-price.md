---
title: Невозможно добавить поле Единица измерения цены на страницу договора покупки
description: При открытии страницы "договора покупки" в режиме строкового вида невозможно настроить страницу, добавив поле "Единица измерения цены" в обзоре строки
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 56d2ce94fb4b74d982cb6a052cca71c18190cd04
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477388"
---
# <a name="you-cant-add-the-price-unit-field-to-the-purchase-agreement-page"></a>Невозможно добавить поле Единица измерения цены на страницу договора покупки

## <a name="symptoms"></a>Симптомы

При открытии страницы **договора покупки** в режиме строкового вида невозможно настроить страницу, добавив поле **Единица измерения цены** в обзоре строки.

## <a name="resolution"></a>Решение

Некоторые общие поля в структуре соглашений не могут включаться в персонализации. Это ограничение происходит из-за реализованной модели данных. Таким образом, нельзя персонализировать поле **Единица измерения цены**.
