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
ms.openlocfilehash: cf307964a07c2b69eb5e4ef2cf9dc094482736d0970e333e84f674c9be6331c7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740535"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>В одном чеке печатается только одна этикетка для нескольких заголовков работы

Номер статьи базы знаний: 4614667

## <a name="symptoms"></a>Симптомы

Несколько заголовков работ создается для одного и того же целевого грузоместа в рамках одного события получения приложения склада. Однако при получении продукта будет напечатана только одна этикетка для грузоместа.

## <a name="resolution"></a>Приказ

Система работает в соответствии с разработанным поведением.

В текущей системе всегда генерируется отдельная метка для грузоместа, независимо от количества заголовков и существующих сочетаний заголовка и строки работы. Созданная метка включает информацию только для одной комбинации.

Чтобы обойти эту проблему, убедитесь, что создание заголовка работ всегда сопоставляется только с одним целевым грузоместом.
