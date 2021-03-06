---
title: Профиль местоположения запрещает отрицательные запасы, но отрицательные запасы в наличии разрешаются
description: Параметр "Разрешить отрицательные запасы" для профиля местоположения имеет значение "Нет", но система по-прежнему допускает отрицательные запасы в наличии.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026845"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a>Профиль местоположения запрещает отрицательные запасы, но отрицательные запасы в наличии разрешаются

Номер статьи базы знаний: 4613622

## <a name="symptoms"></a>Симптомы

Параметр **Разрешить отрицательные запасы** для профиля местоположения имеет значение *Нет*, но система по-прежнему допускает отрицательные запасы в наличии.

## <a name="example-scenario"></a>Пример сценария

Для регулируемых правительством проводок система должна иметь возможность записи отрицательных запасов в убытки журнала. Требуется, чтобы номенклатура отображала отрицательные запасы, но только в определенных местоположениях, таких как "баки". Однако, если группа номенклатурных моделей разрешает отрицательные запасы, можно обнаружить, что не имеет значения, разрешены ли для местоположения отрицательные запасы. Если номенклатура настроена так, что отрицательные запасы не разрешены, не имеет значения, каким образом настроен профиль местоположения.

## <a name="resolution"></a>Приказ

Параметр **Разрешить отрицательные запасы** из профиля местоположения применяется только к складским процессам, таким как комплектация. Однако группы номенклатурных моделей, которые настроены на разрешение отрицательных запасов, влияют на все процессы модуля управления запасами и управления складом, а профиль местоположения не переопределяет настройку.

Можно указать, разрешены ли отрицательные запасы на складе. Настройте группы моделей номенклатуры таким образом, чтобы запретить отрицательные физические запасы, и установите только соответствующий склад, чтобы разрешить отрицательные запасы.
