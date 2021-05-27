---
title: В одном чеке печатается только одна этикетка для нескольких заголовков работы
description: В одном чеке печатается только одна этикетка для нескольких заголовков работы.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026846"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>В одном чеке печатается только одна этикетка для нескольких заголовков работы

Номер статьи базы знаний: 4614667

## <a name="symptoms"></a>Симптомы

Несколько заголовков работ создается для одного и того же целевого грузоместа в рамках одного события получения приложения склада. Однако при получении продукта будет напечатана только одна этикетка для грузоместа.

## <a name="resolution"></a>Приказ

Система работает в соответствии с разработанным поведением.

В текущей системе всегда генерируется отдельная метка для грузоместа, независимо от количества заголовков и существующих сочетаний заголовка и строки работы. Созданная метка включает информацию только для одной комбинации.

Чтобы обойти эту проблему, убедитесь, что создание заголовка работ всегда сопоставляется только с одним целевым грузоместом.
