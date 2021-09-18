---
title: Максимальное число десятичных знаков в единицах складского учета равно 0
description: 'При попытке разноски складской проводки или резервирования запасов появляется сообщение: "Максимальное число десятичных знаков для единицы складского хранения равно 0".'
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9dec198e2d77efd2253c80e14d15791cc37f88e1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477455"
---
# <a name="maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Максимальное число десятичных знаков в единицах складского учета равно 0


## <a name="symptoms"></a>Симптомы

При попытке разноски складской проводки или резервирования запасов появляется следующее сообщение об ошибке:

> Максимальное число десятичных знаков в единицах складского учета равно 0.

Эта проблема возникает, когда количество складской проводки указывается в виде десятичного значения, которое меньше уровня точности, поддерживаемого данным полем. Например, количество *0,5* было определено для складской проводки, но поддерживаются только целые количества. Таким образом, значение должно быть равно *1* вместо *0,5*.

## <a name="resolution"></a>Решение

1. Выполните следующий сценарий в экземпляре SQL Server для округления количеств в складских проводках. Этот сценарий будет исправлять значения в таблице **inventTrans**.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Выполните проверку целостности запасов в наличии, когда включен параметр **исправления ошибок**. Эта проверка исправит значения в таблице **inventSum**.

> [!IMPORTANT]
> Настоятельно рекомендуется аккуратно изменять сценарий в соответствии с требованиями среды, проверять его в тестовой среде, а затем проверять полученные данные перед выполнением сценария в производственной среде.
