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
ms.openlocfilehash: 27ec37e0c0644ff10ece4626d5c136bca3c52ef12f1c6de947afd03003a5368a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776784"
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
