---
title: Невозможно зарезервировать номенклатуру RM, когда запущен производственный заказ
description: 'При выпуске производственного заказа может быть выведено сообщение об ошибке: "Не удается полностью зарезервировать номенклатуру RM." Убедитесь, что доступно полное количество, или зарезервируйте номенклатуры вручную.'
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 528895252d661bb012f49190c15853989833064d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477443"
---
# <a name="item-rm-cant-be-fully-reserved-when-a-production-order-is-released"></a>Невозможно полностью зарезервировать номенклатуру RM, когда запущен производственный заказ

## <a name="symptoms"></a>Симптомы

Если не все номенклатуры строки спецификации являются физически доступными, когда выпущен производственный заказ на склад, а в качестве политики **Выпуск на склад** задано значение *Требуется полное резервирование*, будет выведено следующее сообщение об ошибке:

> Не удается полностью зарезервировать номенклатуру RM. Убедитесь, что все количество доступно, или зарезервируйте номенклатуры вручную, если поле резервирования в строке спецификации имеет значение "Вручную" или "Запущено". Не удалось выпустить заказ на склад, так как не удалось зарезервировать часть материалов.

## <a name="resolution"></a>Решение

Такое поведение является намеренным и работает как ожидается. Для решения проблемы следуйте указаниям, приведенным в сообщении об ошибке: "Убедитесь, что доступно полное количество, или зарезервируйте номенклатуры вручную, если поле "Резервирование" в строке спецификации имеет значение "вручную" или "начато".