---
title: "Методы амортизации и соглашения по амортизации"
description: "В этой статье представлен обзор соглашений по амортизации и методы амортизации, которые поддерживаются Microsoft Dynamics AX."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 51c053e6c130d20258e02284d097431a18bb38cb
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-methods-and-conventions"></a>Методы амортизации и соглашения по амортизации

В этой статье представлен обзор соглашений по амортизации и методы амортизации, которые поддерживаются Microsoft Dynamics AX.

Можно выбрать различные методы амортизации и соглашения. Назначение методов отнести амортизируемую стоимость основных средств к финансовым периодам. Общая цена приобретения основных средств, за вычетом ликвидационной стоимости, если она имеется. 

Если при использовании соглашений по амортизации будет изменена последняя дата начала амортизации для активов, который затем вызывает пропуск некоторых амортизаций, амортизации за последний год могут быть больше или меньше ожидаемых. Амортизация регулируется числом периодов амортизации, затронутых модификацией последней даты начала амортизации.

Например, если используется полугодовое соглашение по амортизации на три года, срок амортизации обычно составляет около 3,5 лет. При изменении последней даты начала амортизации в течение 3,5 лет в последнем году амортизации сдвигается число затронутых периодов. Если дата сдвигается на 3 месяцев, в последнем году сумма затрат составит 9 месяцев амортизации, когда обычно была бы стоимость 6 месяцев амортизации.

Можно выбрать из следующих соглашений по амортизации.


-   Полугодие
-   Полный месяц
-   Середина квартала
-   Середина месяца (1 число месяца)
-   Середина месяца (15 число месяца)
-   Полгода (начало года)
-   Половина года (следующий год)

Можно выбрать один из следующих методов амортизации:
-   Срок службы (прямолинейный метод)
-   Уменьшаемое сальдо
-   Ручная
-   Множитель
-   Себестоимость
-   Оставшийся срок службы прямолинейный метод)
-   Уменьшаемое сальдо в 200%
-   Уменьшаемое сальдо в 175%
-   Уменьшаемый остаток в 150%
-   Уменьшаемое сальдо в 125%

 



<a name="see-also"></a>См. также
--------

[Fixed asset depreciation](fixed-asset-depreciation.md)

[Straight line service life depreciation](Straight-line-service-life-depreciation.md)

[Reducing balance depreciation](reduce-balance-depreciation.md)

[Manual depreciation](manual-depreciation.md)

[Factor depreciation](factor-depreciation.md)

[Consumption depreciation](consumption-depreciation.md)

[Straight line life remaining depreciation](straight-line-life-remaining-depreciation.md)

[Амортизация уменьшаемого сальдо в 125%](125-percent-reducing-balance-depreciation.md)

[Амортизация уменьшаемого сальдо в 150%](150-percent-reducing-balance-depreciation.md)

[Амортизация уменьшаемого сальдо в 175%](175-percent-reducing-balance-depreciation.md)

[Амортизация уменьшаемого сальдо в 200%](200-percent-reducing-balance-depreciation.md)


