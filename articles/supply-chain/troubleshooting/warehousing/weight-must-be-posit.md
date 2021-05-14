---
title: Вес должен быть положительным
description: Вес должен быть положительным
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924311"
---
# <a name="weight-must-be-positive"></a>Вес должен быть положительным

Код ошибки: WeightMustBePositive

## <a name="symptoms"></a>Симптомы

Система отобразит следующее сообщение об ошибке:

> Вес должен быть положительным.

## <a name="cause"></a>Причина

В поле **Вес брутто** установлено значение *0* (ноль) или отрицательное значение.

## <a name="resolution"></a>Приказ

Чтобы указать вес, выполните одно из следующих действий.

- В поле **Вес брутто** задайте значение. Затем выберите единицу измерения из раскрывающегося списка.
- Выберите **Получить вес системы** для расчета значения **Вес брутто**.
