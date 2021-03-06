---
title: Модель ЛИФО с физической стоимостью и маркировкой
description: Метод ЛИФО - это складская модель, в которой последние (самые новые) приходы расходуются первыми. Расходы из запасов сопоставляются с последними приходами в запасах на дату складской проводки.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.assetid: 49c492b0-b018-44e0-928f-9671e54eee20
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 294c7bbb328c31c6c3fdc16a72267224d7c71b27
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809742"
---
# <a name="lifo-with-physical-value-and-marking"></a>Модель ЛИФО с физической стоимостью и маркировкой

[!include [banner](../includes/banner.md)]

Метод ЛИФО - это складская модель, в которой последние (самые новые) приходы расходуются первыми. Расходы из запасов сопоставляются с последними приходами в запасах на дату складской проводки. 

В складской модели ЛИФО (последним пришел, первым ушел) последние (самые поздние) приходы становятся первыми расходами. Расходы со склада сопоставляются с последними приходами на склад с учетом даты складской проводки. Когда вы используете ЛИФО, вы не обязаны использовать правило ЛИФО. Вместо этого при можно пометить проводки по запасам так, чтобы конкретный расход номенклатуры сопоставлялся с конкретным приходом. Мы рекомендуем периодически выполнять закрытие запасов при использовании складской модели ЛИФО. 

Следующие примеры показывают эффект использования ЛИФО с тремя конфигурациями:

-   ЛИФО без параметра **Включать физическую стоимость**
-   ЛИФО с параметром **Включать физическую стоимость**
-   ЛИФО с пометкой

## <a name="lifo-without-the-include-physical-value-option"></a>ЛИФО без параметра "Включать физическую стоимость"
В этом примере группа моделей номенклатур маркируется для включения физической стоимости. Следующая иллюстрация показывает эти проводки:

-   1a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 10,00 долларов США.
-   1b. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 10,00 долларов США.
-   2a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 20,00 долларов США.
-   2b. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 20,00 долларов США.
-   3a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 25,00 долларов США.
-   4a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 30,00 долларов США.
-   4b. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 30,00 долларов США.
-   5a. Физический расход запасов в количестве равном 1 при себестоимости каждой единицы USD 20,00 (скользящее среднее финансово обновленных проводок).
-   5б. Финансовый расход со склада для количества 1 с себестоимостью единицы USD 20,00 (текущее среднее финансово обновленных проводок).
-   6. Выполняется закрытие запасов. На основании метода ЛИФО последний финансово обновленный расход будет сопоставлен последнему финансово обновленному приходу. Для проводки расхода будет выполнена корректировка в размере USD 10,00.

Новая текущая средняя себестоимость отражает среднее финансово обновленных проводок, USD 15,00. Следующая иллюстрация показывает влияния складской модели ЛИФО для этой серии проводок, когда параметр **Включать физическую стоимость** не используется. 

![LIFO без Включать физическую стоимость](./media/lifowithoutincludephysicalvalue.gif) 

**Ключ к схеме**

- Складские проводки представлены вертикальными стрелками.
- Приходы на склад представлены вертикальными стрелками над осью времени.
- Расходы со склада представлены вертикальными стрелками под осью времени.
- Над (или под) каждой вертикальной стрелкой указано значение складской проводки в формате Количество@Цена за единицу.
- Значение складской проводки, заключенное в скобки, указывает на то, что проводка по запасам физически разнесена в запасы.
- Значение проводки по запасам, не заключенное в скобки, указывает на то, что проводка по запасам финансово разнесена в запасы.
- Каждая новая проводка прихода или расхода обозначается новой меткой.
- Каждая вертикальная стрелка обозначается последовательным идентификатором, например *1a*. Идентификаторы определяют последовательность разноски проводок по запасам по оси времени.
- Закрытия склада представлены вертикальной красной пунктирной линией и меткой *Закрытие склада*.
- Сопоставления, которые выполняются путем закрытия склада, представлены красными стрелками, нанесенными пунктиром в диагональном направлении от прихода к расходу.

## <a name="lifo-with-the-include-physical-value-option"></a>ЛИФО с параметром "Включать физическую стоимость"
Если установлен флажок **Включать физическую стоимость** для номенклатуры на странице **Группа номенклатурных моделей**, при вычислении скользящего среднего значения себестоимости система будет использовать как физические, так и финансовые проводки прихода. Когда это возможно, система будет также выполнять корректировку физически обновленных проводок расхода. Когда флажок **Включать физическую стоимость** снят, при закрытии запасов с использованием складской модели ЛИФО сопоставления будут производиться только с финансово обновленными проводками. 

Следующая иллюстрация показывает эти проводки:

-   1a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 10,00 долларов США.
-   1b. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 10,00 долларов США.
-   2a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 20,00 долларов США.
-   2b. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 20,00 долларов США.
-   3a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 25,00 долларов США.
-   4a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 30,00 долларов США.
-   4b. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 30,00 долларов США.
-   5a. Физический расход запасов в количестве равном 1 при себестоимости каждой единицы USD 21,25 (скользящее среднее финансовых и физических обновленных проводок).
-   5б. Финансовый расход со склада для количества 1 с себестоимостью единицы USD 21,25 (текущее среднее финансово и физически обновленных проводок).
-   6a. Физический расход запасов в количестве равном 1 при себестоимости каждой единицы 21,25 долларов США.
-   7. Выполняется закрытие запасов. На основании метода ЛИФО проводка последнего расхода будет скорректирована или сопоставлена последнему обновленному приходу.

Проводка 6a будет скорректирована по проводке прихода 4b. Система не выполнит сопоставление этих проводок, так как приход обновлен физически, но не финансово. Вместо этого для проводки физического расхода будет разнесена корректировка в сумме USD 8,75. Проводка 5b будет скорректирована по проводке физического прихода 3a. Система не выполнит сопоставление этих проводок, поскольку обе они не обновлены финансово. Вместо этого для этой проводки расхода будет выполнена корректировка в сумме USD –3,75. Новое скользящее среднее значение себестоимости отражает среднее значение по проводкам, обновленным финансово и физически, равное 20,00 долларов США. 

Следующая иллюстрация показывает влияния складской модели ЛИФО для этой серии проводок, когда параметр **Включать физическую стоимость** используется. 

![LIFO с Включать физическую стоимость](./media/lifowithincludephysicalvalue.gif) 

**Ключ к схеме**

- Складские проводки представлены вертикальными стрелками.
- Приходы на склад представлены вертикальными стрелками над осью времени.
- Расходы со склада представлены вертикальными стрелками под осью времени.
- Над (или под) каждой вертикальной стрелкой указано значение складской проводки в формате Количество@Цена за единицу.
- Значение складской проводки, заключенное в скобки, указывает на то, что проводка по запасам физически разнесена в запасы.
- Значение проводки по запасам, не заключенное в скобки, указывает на то, что проводка по запасам финансово разнесена в запасы.
- Каждая новая проводка прихода или расхода обозначается новой меткой.
- Каждая вертикальная стрелка обозначается последовательным идентификатором, например *1a*. Идентификаторы определяют последовательность разноски проводок по запасам по оси времени.
- Закрытия склада представлены вертикальной красной пунктирной линией и меткой *Закрытие склада*.
- Сопоставления, которые выполняются путем закрытия склада, представлены красными стрелками, нанесенными пунктиром в диагональном направлении от прихода к расходу.

## <a name="lifo-with-marking"></a>ЛИФО с пометкой
Пометка — это процесс, который позволяет связать (или пометить) проводку расхода с проводкой прихода. Пометить проводку можно до или после того, как она будет разнесена. Пометку можно использовать, когда необходима уверенность в точной стоимости запасов при разноске проводки или когда выполняется закрытие склада. Например, ваш отдел обслуживания клиентов принял срочный заказ от важного клиента. Поскольку это срочный заказ, для выполнения запроса клиента за данную номенклатуру придется заплатить больше. 

Необходимо гарантировать, чтобы затраты на эту складскую номенклатуру были отражены в прибыли или себестоимости проданных товаров для данной накладной по заказу на продажу. При разноске заказа на покупку запасы получены по себестоимости равной 120,00 долларов США. Если этому документу заказа на продажу до разноски отборочной накладной или накладной присвоить метку, связывающую его с заказом на покупку, то себестоимость реализованной продукции составит 120,00 долларов США вместо текущего скользящего среднего значения себестоимости для данной номенклатуры. Если отборочная накладная или накладная по данному заказу на продажу разносится до выполнения маркировки, то себестоимость реализованной продукции будет разнесена в соответствии со скользящим средним значением себестоимости. 

До выполнения операции закрытия запасов этим двум проводкам все еще можно присвоить метки таким образом, чтобы связать их друг с другом. 

Можно пометить проводку расхода для проводки прихода до разноски проводки. Вы можете сделать это из строки заказа на продажу на странице **Сведения по заказам на продажу**. Вы можете просмотреть открытые проводки прихода на странице **Маркировка**. 

Можно также пометить проводку расхода для проводки прихода после разноски проводки. Вы можете сопоставить или пометить проводку расхода для открытой проводки прихода для инвентаризованной номенклатуры из журнала корректировки разнесенных запасов. 

Следующая иллюстрация показывает эти проводки:

-   1a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 10,00 долларов США.
-   1b. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 10,00 долларов США.
-   2a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 20,00 долларов США.
-   2b. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 20,00 долларов США.
-   3a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 25,00 долларов США.
-   4a. Физический приход запасов в количестве равном 1 при себестоимости каждой единицы 30,00 долларов США.
-   4b. Финансовый приход запасов в количестве равном 1 при себестоимости каждой единицы 30,00 долларов США.
-   5a. Физический расход запасов в количестве равном 1 при себестоимости каждой единицы 21,25 долларов США (скользящее среднее финансовых и физических обновленных проводок).
-   5б. Финансовый расход со склада для количества 1 помечен для прихода на склад 2b до разноски проводки. Эта проводка разносится с себестоимостью единицы USD 20,00.
-   6a. Физический расход запасов в количестве равном 1 при себестоимости каждой единицы 21,25 долларов США.
-   7. Выполняется закрытие запасов. Поскольку финансово обновленная проводка ФИФО помечена для существующего прихода, эти проводки сопоставляются друг с другом и корректировка не выполняется.

Новое скользящее среднее значение себестоимости отражает среднее значение по проводкам, обновленным финансово и физически, равное 27,50 долларов США. 

На следующей иллюстрации показаны результаты выбора складской модели ЛИФО для этой серии проводок, когда используется маркировка расходов и приходов. 

![LIFO с маркировкой](./media/lifowithmarking.gif) 

**Ключ к схеме**

- Складские проводки представлены вертикальными стрелками.
- Приходы на склад представлены вертикальными стрелками над осью времени.
- Расходы со склада представлены вертикальными стрелками под осью времени.
- Над (или под) каждой вертикальной стрелкой указано значение складской проводки в формате Количество@Цена за единицу.
- Значение складской проводки, заключенное в скобки, указывает на то, что проводка по запасам физически разнесена в запасы.
- Значение проводки по запасам, не заключенное в скобки, указывает на то, что проводка по запасам финансово разнесена в запасы.
- Каждая новая проводка прихода или расхода обозначается новой меткой.
- Каждая вертикальная стрелка обозначается последовательным идентификатором, например *1a*. Идентификаторы определяют последовательность разноски проводок по запасам по оси времени.
- Закрытия склада представлены вертикальной красной пунктирной линией и меткой *Закрытие склада*.
- Сопоставления, которые выполняются путем закрытия склада, представлены красными стрелками, нанесенными пунктиром в диагональном направлении от прихода к расходу.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]