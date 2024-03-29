---
title: Взвешенное среднее с физической стоимостью и маркировкой
description: Средневзвешенная стоимость - это складская модель, действующая на основании принципа средневзвешенного значения, когда запасы на складе оцениваются по средней стоимости продукции, поступившей на склад до конца отчетного периода, плюс запасы, имеющиеся в наличии с предыдущего периода.
author: JennySong-SH
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65501
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c80dcdc08432bb68478827c8763735e644aa4a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675301"
---
# <a name="weighted-average-with-physical-value-and-marking"></a>Взвешенное среднее с физической стоимостью и маркировкой

[!include [banner](../includes/banner.md)]

Взвешенное среднее — это складская модель, основанная на среднем значении, которое является результатом умножения каждого компонента (проводки по номенклатуре) на коэффициент (себестоимость) с учетом его важности (количества). Или по другому: взвешенное среднее — это складская модель, которая назначает затраты на проводки расхода на основе среднего значения всех складских запасов, полученных за период, а также всех запасов в наличии из предыдущего периода.

При выполнении закрытия запасов с использованием складской модели взвешенного среднего можно создать сопоставление двумя способами. Обычно все приходы сопоставляются с виртуальным расходом, в котором учитываются полученное количество и стоимость. Этот виртуальный расход имеет соответствующий виртуальный приход, из которого выполняется согласование расходов. Таким образом, все расходы получают одинаковую среднюю стоимость. Виртуальный расход и приход отображаются как виртуальное перемещение, называемое *перемещением закрытия склада для взвешенного среднего*. Этот метод сопоставления называется *суммарным сопоставлением со взвешенным средним*. Если существует только один приход, все расходы могут быть сопоставлены с ним, и виртуальное перемещение не будет создано. Этот метод сопоставления называется *прямым сопоставлением*. Любые запасы в наличии после закрытия запасов оцениваются по взвешенному среднему из предыдущего периода и включаются в расчет взвешенного среднего в следующем периоде.

Можно переопределить принцип взвешенного среднего, отметив проводки по запасам так, чтобы конкретный приход номенклатуры сопоставлялся с конкретным расходом. Периодическое закрытие запасов требуется при использовании складской модели взвешенного среднего для создания сопоставлений и корректировки значения выпусков в соответствии с принципом взвешенного среднего. До тех пор, пока не будет запущен процесс закрытия запасов, проводки расхода оцениваются по скользящему среднему, когда были выполнены физические и финансовые обновления. Если не используется маркировка, скользящее среднее вычисляется, когда выполняется физическое или финансовое обновление.

Калькуляция в методе средневзвешенной стоимости запасов производится по ниже приведенной формуле:

- Средневзвешенное значение = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q *n* × P *n*\]) ÷ (Q1 + Q2 + Q *n*)

Q = количество по проводке  
P = цена по проводке

Сопоставления представляют собой разноски закрытия запасов, корректирующие расход в соответствии с правильным средневзвешенным значением на дату закрытия. Следующие примеры иллюстрируют эффект использования средневзвешенного значения с пятью различными конфигурациями:

- Прямое сопоставление средневзвешенной стоимости без параметра **Включать физическую стоимость**
- Суммированное сопоставление средневзвешенной стоимости без параметра **Включать физическую стоимость**
- Прямое сопоставление средневзвешенной стоимости с параметром **Включать физическую стоимость**
- Суммированное сопоставление средневзвешенной стоимости с включенным параметром **Включать физическую стоимость**
- Средневзвешенное значение с маркировкой

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Прямое сопоставление средневзвешенной стоимости без включения физической стоимости

Принцип прямого сопоставления создает сопоставления непосредственно между приходом и расходом без создания дополнительных складских проводок. Система использует принцип прямого сопоставления в следующих ситуациях:

- Один приход и один или более расходов были разнесены в данном периоде.
- В данном периоде были разнесены только расходы, и запасы содержат номенклатуры в наличии из предыдущего закрытия.

В этом примере снят флажок **Включать физическую стоимость** в разделе **Группа моделей номенклатуры** для выпущенного продукта. Следующая иллюстрация показывает эти проводки:

- 1a. Физический приход запасов в количестве равном 10 при себестоимости каждой единицы 10,00 долларов США.
- 1b. Финансовый приход запасов в количестве равном 10 при себестоимости каждой единицы 10,00 долларов США.
- 2a. Физический приход запасов в количестве равном 10 при себестоимости каждой единицы 20,00 долларов США.
- 3a. Физический расход запасов в количестве равном 1 при себестоимости USD 10,00 (скользящее среднее финансово разнесенных проводок).
- 3b. Физический расход запасов в количестве равном 1 при себестоимости USD 10,00 (скользящее среднее финансово разнесенных проводок).
- 4a. Физический расход запасов в количестве равном 1 при себестоимости 10,00 долларов США каждый (скользящее среднее финансово разнесенных проводок).
- 4b. Физический расход запасов в количестве равном 1 при себестоимости 10,00 долларов США каждый (скользящее среднее финансово разнесенных проводок).
- 5a. Физический расход запасов в количестве равном 1 при себестоимости 10,00 долларов США каждый (скользящее среднее финансово разнесенных проводок).
- 6\. Выполняется закрытие запасов. В зависимости от метода взвешенного среднего, система использует метод прямого сопоставления, поскольку только одна приемка финансово обновляется в периоде. В этом примере создается одно сопоставление между 1b и 3b, и другое между 1b и 4b. Корректировка не выполняется, поскольку скользящее среднее совпадает с взвешенным средним значением.

Нижеследующая диаграмма иллюстрирует серию проводок, которые оказывают влияние на выбор складской модели с средневзвешенным значением и принцип прямого сопоставления без параметра **Включать физическую стоимость**.

![DS взвешенного среднего без «Включать физическую стоимость».](media/weighted-average-direct-settlement-without-include-physical-value.png)

**Ключ к схеме**

- Складские проводки представлены вертикальными стрелками.
- Физические проводки представлены в виде укороченных серых стрелок.
- Финансовые проводки представлены в виде более длинных черных стрелок.
- Приходы на склад представлены вертикальными стрелками над осью.
- Расходы со склада представлены вертикальными стрелками под осью.
- Каждая новая проводка прихода или расхода обозначается новой меткой.
- Каждая вертикальная стрелка обозначается последовательным идентификатором, например *1a*. Идентификаторы определяют последовательность разноски проводок по запасам по оси времени.
- Каждая дата в схеме отделяется тонкой черной вертикальной линией. Дата отмечается в нижней части диаграммы.
- Закрытия запасов представлены вертикальной красной пунктирной линией.
- Сопоставления, которые выполняются путем закрытия склада, представлены красными стрелками, нанесенными пунктиром в диагональном направлении от прихода к расходу.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Суммированное сопоставление средневзвешенной стоимости без параметра Включать физическую стоимость

Когда в периоде есть несколько приходов, взвешенное среднее основано на принципе суммарного сопоставления, в котором все приходы в течение периода закрытия суммируются в проводку, которая называется *закрытием запасов для взвешенного среднего*. Все приходы за период будут сопоставлены расходу вновь созданной проводки запасов. Все расходы за период будут сопоставлены приходу новой проводки запасов. Если есть значение оставшихся запасов в наличии после закрытия запасов, значение запасов в наличии включается в проводку прихода проводок закрытия запасов со взвешенным средним.

Следующие проводки проиллюстрированы на следующем графике:

- 1a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 10,00 долларов США.
- 1b. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 10,00 долларов США.
- 2a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 20,00 долларов США.
- 2b. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 22,00 долларов США.
- 3a. Физический расход запасов в количестве равном 1 при себестоимости USD 16,00 (скользящее среднее финансово разнесенных проводок).
- 3b. Физический расход запасов в количестве равном 1 при себестоимости USD 16,00 (скользящее среднее финансово разнесенных проводок).
- 4a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 25,00 долларов США.
- 5a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 30,00 долларов США.
- 5б. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 30,00 долларов США.
- 6a. Физический расход запасов в количестве равном 1 при себестоимости USD 23,00 (скользящее среднее финансово разнесенных проводок).
- 7. Выполняется закрытие запасов.
- 7a. Создан финансовый расход проводки закрытия запасов по средневзвешенной стоимости для суммирования сопоставлений всех финансовых приходов на склад.
  - Проводка 1b сопоставляется для количества 1 с суммой, сопоставленной с 10,00 долл. США.
  - Проводка 2b сопоставляется для количества 1 с суммой, сопоставленной с 22,00 долл. США.
  - Проводка 5b сопоставляется для количества 1 с суммой, сопоставленной с 30,00 долл. США.
  - Проводка 7a. создается для количества 3 с суммой, сопоставленной с 62,00 долл. США. Эта проводка засчитывает сумму трех проводок прихода, которые финансово обновляются за период.
- 7b. Создан финансовый приход "Проводка закрытия запасов по средневзвешенной стоимости" как зачет финансово разнесенных расходов.
  - Проводка 3b сопоставляется для количества 1 с суммой, сопоставленной с 20,67 долл. США. Эта проводка корректируется на 4,67 долл. США, чтобы довести исходное значение 16,00 долл. США до 20,67 долл. США, что является взвешенным средним по финансово разнесенным проводкам за период.
  - Проводка 7b. создается для количества 1 с суммой, сопоставленной с 20,67 долл. США для зачета 3b. Эта проводка засчитывает сумму одной проводки расхода, которые финансово обновляются за период.

Нижеследующая диаграмма иллюстрирует серию проводок, которые оказывают влияние на выбор Складской модели с средневзвешенным значением и принцип сводного сопоставления без параметра **Включать физическую стоимость**.

![SS взвешенного среднего без включения физической стоимости.](media/weighted-average-summarized-settlement-without-include-physical-value.png)

**Ключ к схеме**

- Складские проводки представлены вертикальными стрелками.
- Физические проводки представлены в виде укороченных серых стрелок.
- Финансовые проводки представлены в виде более длинных черных стрелок.
- Приходы на склад представлены вертикальными стрелками над осью.
- Расходы со склада представлены вертикальными стрелками под осью.
- Каждая новая проводка прихода или расхода обозначается новой меткой.
- Каждая вертикальная стрелка обозначается последовательным идентификатором, например *1a*. Идентификаторы определяют последовательность разноски проводок по запасам по оси времени.
- Каждая дата в схеме отделяется тонкой черной вертикальной линией. Дата отмечается в нижней части диаграммы.
- Закрытия запасов представлены вертикальной красной пунктирной линией.
- Сопоставления, которые выполняются путем закрытия склада, представлены красными стрелками, нанесенными пунктиром в диагональном направлении от прихода к расходу.

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Прямое сопоставление средневзвешенной стоимости с параметром Включать физическую стоимость

Параметр **Включать физическую стоимость** в модели закрытия запасов по средневзвешенной стоимости действует иначе, чем в предыдущих версиях программы. Если выбрать параметр **Включать физическую стоимость** для номенклатуры в форме **Группа номенклатурных моделей**, система будет использовать физически обновленные приходы, когда вычисляет оцененную себестоимость расхода или скользящее среднее. В течение периода расходы будут разноситься на основе этой расчетной себестоимости. Во время закрытия запасов при расчете средневзвешенного значения будут учитываться только финансово обновленные приходы.

Следующие проводки проиллюстрированы на следующем графике:

- 1a. Физический приход запасов в количестве равном 10 при себестоимости каждой единицы 10,00 долларов США.
- 1b. Финансовый приход запасов в количестве равном 10 при себестоимости каждой единицы 10,00 долларов США.
- 2a. Физический приход запасов в количестве равном 10 при себестоимости каждой единицы 20,00 долларов США.
- 3a. Физический расход запасов в количестве равном 1 при себестоимости USD 15,00 (скользящее среднее финансовых и физических разнесенных проводок).
- 3b. Финансовый расход запасов в количестве равном 1 при себестоимости USD 15,00 (скользящее среднее финансовых и физических разнесенных проводок).
- 4a. Физический расход запасов в количестве равном 1 при себестоимости 15,00 долларов каждый (скользящее среднее финансовых и физических разнесенных проводок).
- 4b. Финансовый расход запасов в количестве равном 1 при себестоимости 15,00 долларов США каждый (скользящее среднее финансовых и физических разнесенных проводок).
- 5a. Физический расход запасов в количестве равном 1 при себестоимости 15,00 долларов каждый (скользящее среднее финансовых и физических разнесенных проводок).
- 6\. Выполняется закрытие запасов. В зависимости от метода взвешенного среднего, система использует метод прямого сопоставления, поскольку только одна приемка финансово обновляется в периоде. В этом примере создается одно сопоставление между 1b и 3b, и другое между 1b и 4b. Проводки 3b и 4b, каждая из которых корректируется на -5,00 долларов США, чтобы довести значение до 10,00 долларов США.

Нижеследующая диаграмма иллюстрирует серию проводок, которые оказывают влияние на выбор Складской модели с средневзвешенным значением и принцип прямого сопоставления с параметром **Включать физическую стоимость**.

![DS взвешенного среднего с включенной физической стоимостью.](media/weighted-average-direct-settlement-with-include-physical-value.png)

**Ключ к схеме**

- Складские проводки представлены вертикальными стрелками.
- Физические проводки представлены в виде укороченных серых стрелок.
- Финансовые проводки представлены в виде более длинных черных стрелок.
- Приходы на склад представлены вертикальными стрелками над осью.
- Расходы со склада представлены вертикальными стрелками под осью.
- Каждая новая проводка прихода или расхода обозначается новой меткой.
- Каждая вертикальная стрелка обозначается последовательным идентификатором, например *1a*. Идентификаторы определяют последовательность разноски проводок по запасам по оси времени.
- Каждая дата в схеме отделяется тонкой черной вертикальной линией. Дата отмечается в нижней части диаграммы.
- Закрытия запасов представлены вертикальной красной пунктирной линией.
- Сопоставления, которые выполняются путем закрытия склада, представлены красными стрелками, нанесенными пунктиром в диагональном направлении от прихода к расходу.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Суммированное сопоставление средневзвешенной стоимости с включенным параметром Включать физическую стоимость

Параметр **Включать физическую стоимость** работает со средневзвешенной стоимостью иначе, чем в предыдущих версиях программы. Установите флажок **Включать физическую стоимость** для номенклатуры на странице **Группа номенклатурных моделей**. После этого система будет использовать физически обновленные приходы при вычислении оценочной себестоимости или скользящего среднего. В течение периода расходы будут разноситься на основе этой расчетной себестоимости. Во время закрытия запасов при расчете средневзвешенного значения будут учитываться только финансово обновленные приходы. Мы рекомендуем ежемесячное закрытие запасов при использовании складской модели средневзвешенного значения. В данном примере суммарного сопоставления средневзвешенной стоимости, для складской модели помечен параметр Включить физическую стоимость.

Следующие проводки проиллюстрированы на следующем графике:

- 1a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 10,00 долларов США.
- 1b. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 10,00 долларов США.
- 2a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 20,00 долларов США.
- 2b. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 22,00 долларов США.
- 3a. Физический расход запасов в количестве равном 1 при себестоимости USD 16,00 (скользящее среднее финансовых и физических разнесенных проводок).
- 3b. Финансовый расход запасов в количестве равном 1 при себестоимости USD 16,00 (скользящее среднее финансовых и физических разнесенных проводок).
- 4a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 25,00 долларов США.
- 5a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 30,00 долларов США.
- 5б. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 30,00 долларов США.
- 6a. Физический расход запасов в количестве равном 1 при себестоимости USD 23,67 (скользящее среднее финансовых и физических разнесенных проводок).
- 7. Выполняется закрытие запасов.
- 7a. Создан финансовый расход проводки закрытия запасов по средневзвешенной стоимости для суммирования сопоставлений всех финансовых приходов на склад.
  - Проводка 1b сопоставляется для количества 1 с суммой, сопоставленной с 10,00 долл. США.
  - Проводка 2b сопоставляется для количества 1 с суммой, сопоставленной с 22,00 долл. США.
  - Проводка 5b сопоставляется для количества 1 с суммой, сопоставленной с 30,00 долл. США.
  - Проводка 7a. создается для количества 3 с суммой, сопоставленной с 62,00 долл. США.  
- 7b. Создан финансовый приход "Проводка закрытия запасов по средневзвешенной стоимости" как зачет финансово закрытых проводок расходов.
  - Проводка 3b сопоставляется для количества 1 с суммой, сопоставленной с 20,67 долл. США. Эта проводка корректируется на 4,67 долл. США, чтобы довести исходное значение 16,00 долл. США до 20,67 долл. США, что является взвешенным средним по финансово разнесенным проводкам за период.
  - Проводка 7b. создается для количества 1 с суммой, сопоставленной с 20,67 долл. США для зачета 3b.

Нижеследующая диаграмма иллюстрирует серию проводок, которые оказывают влияние на выбор Складской модели с средневзвешенным значением и принцип сводного сопоставления без параметра **Включать физическую стоимость**.

![SS взвешенного среднего с включенной физической стоимостью.](media/weighted-average-summarized-settlement-with-include-physical-value.png)

**Ключ к схеме**

- Складские проводки представлены вертикальными стрелками.
- Физические проводки представлены в виде укороченных серых стрелок.
- Финансовые проводки представлены в виде более длинных черных стрелок.
- Приходы на склад представлены вертикальными стрелками над осью.
- Расходы со склада представлены вертикальными стрелками под осью.
- Каждая новая проводка прихода или расхода обозначается новой меткой.
- Каждая вертикальная стрелка обозначается последовательным идентификатором, например *1a*. Идентификаторы определяют последовательность разноски проводок по запасам по оси времени.
- Каждая дата в схеме отделяется тонкой черной вертикальной линией. Дата отмечается в нижней части диаграммы.
- Закрытия запасов представлены вертикальной красной пунктирной линией.
- Сопоставления, которые выполняются путем закрытия склада, представлены красными стрелками, нанесенными пунктиром в диагональном направлении от прихода к расходу.

## <a name="weighted-average-with-marking"></a>Средневзвешенное значение с маркировкой

Пометка — это процесс, который позволяет связать (или пометить) проводку расхода с проводкой прихода. Пометить проводку можно до или после того, как она будет разнесена. Пометку можно использовать, когда необходима уверенность в точной стоимости запасов при разноске проводки или когда выполняется закрытие запасов.

Например, ваш отдел обслуживания клиентов принял срочный заказ от важного клиента. Поскольку это срочный заказ, для выполнения запроса клиента за данную номенклатуру придется заплатить больше. Необходимо гарантировать, что затраты на эту складскую номенклатуру будут отражены в прибыли или себестоимости проданных товаров для данной накладной по заказу на продажу.

При разноске заказа на покупку запасы получены по себестоимости равной 120,00 долларов США. Предположим, этот документ заказа на продажу отмечен для заказа на покупку перед разноской отборочной накладной или накладной. Тогда себестоимость проданных товаров составит в долларах 120,00 вместо текущего скользящего среднего значения себестоимости номенклатуры. Если отборочная накладная или накладная по данному заказу на продажу разносится до выполнения маркировки, то себестоимость реализованной продукции будет разнесена в соответствии со скользящим средним значением себестоимости.

До выполнения операции закрытия запасов этим двум проводкам все еще можно присвоить метки таким образом, чтобы связать их друг с другом.

Проводка прихода отмечена для проводки расходов. Тогда метод оценки, выбранный для группы номенклатурных моделей номенклатуры, не будет применяться, и система сопоставит эти проводки друг с другом.

Можно пометить проводку расхода для проводки прихода до разноски проводки. Вы можете сделать это из строки заказа на продажу на странице **Сведения по заказам на продажу**. Открытые проводки прихода отображаются на странице **Маркировка**.

Можно пометить проводку расхода для проводки прихода после выполнения разноски проводки. Вы можете сопоставить или пометить проводку расхода для открытой проводки прихода для инвентаризованной номенклатуры из журнала корректировки разнесенных запасов.

Следующие проводки проиллюстрированы на следующем графике:

- 1a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 10,00 долларов США.
- 1b. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 10,00 долларов США.
- 2a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 20,00 долларов США.
- 2b. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 22,00 долларов США.
- 3a. Физический расход запасов в количестве равном 1 при себестоимости USD 16,00 (скользящее среднее финансово разнесенных проводок).
- 3b. Физический расход запасов в количестве равном 1 при себестоимости USD 16,00 (скользящее среднее финансово разнесенных проводок).
- 3c. Финансовый расход запасов для 3b отмечен как финансовый расход из запасов для 2b.
- 4a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 25,00 долларов США.
- 5a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 30,00 долларов США.
- 5б. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 30,00 долларов США.
- 6a. Физический расход запасов в количестве равном 1 при себестоимости USD 23,00 (скользящее среднее финансово разнесенных проводок).
- 7. Выполняется закрытие запасов. В зависимости от принципа маркировки, использующего метод взвешенного среднего, помеченные проводки сопоставляются друг с другом. В этом примере 3b сопоставляется с 2b, а корректировка для 6,00 долларов США разносится в 3b, чтобы вернуть значение в 22,00 долларов США. В этом примере не выполняется никаких дополнительных сопоставлений, поскольку закрытие создает сопоставления только для финансово обновленных проводок.

Нижеследующая диаграмма иллюстрирует серию проводок, которые оказывают влияние на выбор складской модели с средневзвешенной стоимостью и маркировкой.

![Взвешенное среднее с маркировкой.](media/weighted-average-with-marking.png)

**Ключ к схеме**

- Складские проводки представлены вертикальными стрелками.
- Физические проводки представлены в виде укороченных серых стрелок.
- Финансовые проводки представлены в виде более длинных черных стрелок.
- Приходы на склад представлены вертикальными стрелками над осью.
- Расходы со склада представлены вертикальными стрелками под осью.
- Каждая новая проводка прихода или расхода обозначается новой меткой.
- Каждая вертикальная стрелка обозначается последовательным идентификатором, например *1a*. Идентификаторы определяют последовательность разноски проводок по запасам по оси времени.
- Каждая дата в схеме отделяется тонкой черной вертикальной линией. Дата отмечается в нижней части диаграммы.
- Закрытия запасов представлены вертикальной красной пунктирной линией.
- Сопоставления, которые выполняются путем закрытия склада, представлены красными стрелками, нанесенными пунктиром в диагональном направлении от прихода к расходу.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
