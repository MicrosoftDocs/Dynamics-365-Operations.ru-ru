---
title: Физическое оставшееся количество в единице не должно быть нулевым
description: При создании отборочной накладной данные, которые поставляются в нее, имеют ненулевое количество запасов, но нулевое количество продаж.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248800"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a>Физическое оставшееся количество в единице не должно быть нулевым

Код ошибки: SYS19591

## <a name="symptoms"></a>Симптомы

При создании отборочной накладной данные, которые поставляются в нее, имеют ненулевое количество запасов, но нулевое количество продаж.

При попытке создать отборочную накладную система выводит следующее сообщение об ошибке:

> Физический остаток по складу в ед. изм. учета %1 должен быть отличен от нуля.

Поэтому невозможно создать отборочную накладную для загрузки.

## <a name="cause"></a>Причина

Система оценивает физическое оставшееся количество в единице измерения складского учета и физическое оставшееся количество в единице отгрузки. Если система обнаружит, что физическое оставшееся количество в единице отгрузки составляет 0 (ноль), но физическое оставшееся количество в единице измерения складского учета не равно 0, вы не можете создать отборочную накладную. Например, эта проблема может возникнуть, если единица измерения продажи и единица измерения складского учета для номенклатуры отличаются, а конверсия между единицами не является точной.

## <a name="resolution"></a>Решение

Загрузка или отгрузка в данный момент находится в состоянии, когда создание отборочной накладной завершается сбоем. Для решения продляемы необходимо выполнить одну или несколько из следующих задач:

- Проверьте строки загрузки и убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.
- Просмотрите строки загрузки и внесите коррективы, чтобы убедиться, что количество может быть чисто преобразовано без проблем округления.
- Просмотрите строки загрузки и внесите коррективы, чтобы убедиться, что единица измерения и количество приведены в соответствие с десятичной точностью единицы.
- Убедитесь, что единица измерения складского учета меньше единицы измерения продажи.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Проверьте строки загрузки и убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.

С помощью следующей процедуры проверьте строки загрузки и убедитесь, что вся связанная работа завершена в окончательной ячейке отгрузки, и что количества совпадают.

1. Выберите **Управление складом \> Загрузки \> Все загрузки**.
1. Выберите загрузку, для которой невозможно подтвердить отгрузку.
1. На экспресс-вкладке **Строки загрузки** проверьте строку загрузки.
1. Запишите значение поля **Созданное количество работы**.
1. В области действий на вкладке **Загрузки** в группе **Связанные сведения** выберите **Работа**.
1. Убедитесь, что работа завершена в конечной ячейке отгрузки и что скомплектованное количество работы совпадает с созданным количеством работы в строке загрузки.
1. Повторите эту процедуру для всех строк загрузки, чтобы обеспечить соблюдение всех критериев.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a>Просмотрите строки загрузки и внесите коррективы, чтобы убедиться, что количество может быть чисто преобразовано без проблем округления.

С помощью следующей процедуры проверьте строки загрузки и внесите коррективы, чтобы убедиться, что количество может быть чисто преобразовано без проблем округления.

1. Выберите **Управление складом \> Загрузки \> Все загрузки**.
1. Выберите загрузку, для которой не может быть создана отборочная накладная.
1. На панели действий на вкладке **Отгрузка и получение** в группе **Реверсирование** выберите **Реверсировать подтверждение отгрузки**.
1. На вкладке **Строки загрузки** выберите строку загрузки для номенклатуры, которая превышает перепоставку.
1. Выберите **Уменьшить скомплектованное количество** для корректировки скомплектованного количества.
1. На вкладке  **Сведения строки** выберите **Заказ**.
1. В поле **Количество** установите значение для скомплектованного количества (то есть значение в поле **Созданное количество работы**), чтобы можно было продолжить создание отборочной накладной.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>Просмотрите строки загрузки и внесите коррективы, чтобы убедиться, что единица измерения и количество приведены в соответствие с десятичной точностью единицы.

С помощью следующей процедуры проверьте строки загрузки и внесите коррективы, чтобы убедиться, что единица измерения и количество приведены в соответствие с десятичной точностью единицы.

1. Выберите **Управление складом \> Загрузки \> Все загрузки**.
1. Выберите загрузку, для которой не может быть создана отборочная накладная.
1. На экспресс-вкладке **Строки загрузки** выберите строку загрузки для номенклатуры, которая вызывает проблему. Запишите значение полей **Количество** и **Единица измерения**.
1. Перейдите в раздел **Управление организацией \> Единицы \> Единицы**.
1. Выберите единицу, для которой не может быть создана отборочная накладная.
1. При необходимости скорректируйте значение в поле **Десятичная точность**.

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a>Убедитесь, что единица измерения складского учета меньше единицы измерения продажи.

Убедитесь, что единица измерения складского учета меньше единицы измерения продажи. Рассмотрите перенастройку единицы измерения для номенклатуры по мере необходимости.
