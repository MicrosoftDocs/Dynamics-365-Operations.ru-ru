---
title: Отрицательные дни и динамические отрицательные дни
description: В этой статье содержатся сведения об отрицательных днях и динамических отрицательных днях, а также о том, как их можно использовать для помощи в бизнесе.
author: t-benebo
ms.date: 05/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2019-06-07
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bcaaf46a0ddd84cded721c5d02d4a45cd4745114
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740390"
---
<!-- KFM: Split this up. non-dynamic for deprecated MP, and "dynamic" for new standard PO. -->

# <a name="negative-days-and-dynamic-negative-days"></a>Отрицательные дни и динамические отрицательные дни

[!include [banner](../includes/banner.md)]

В этой статье содержатся сведения об отрицательных днях и динамических отрицательных днях, а также о том, как их можно использовать для помощи в бизнесе. *Временная граница отрицательных дней* представляет собой число дней, в течение которых вы готовы ожидать, прежде чем заказать новое пополнение в случае отрицательных запасов.

В этой статье приводится следующая информация:

- Порядок создания спланированных заказов
- Корреляция между временной границей отрицательных дней и временем упреждения для номенклатуры
- Как вычисляется временная граница динамических отрицательных дней, и как время упреждения номенклатуры учитывается в расчете
- Порядок интерпретации [предложений по улучшению времени выполнения планирования материальных потребностей (MRP) (сводное планирование)](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx), которые связаны с отрицательными днями

В этой статье используются три гипотетических сценария, которые помогут понять эту информацию. Различие между сценариями заключается в точке, в которой вы получаете спрос: до, во время или после периода времени упреждения для номенклатуры.

## <a name="scenario-1-you-get-demand-before-the-items-lead-time-period"></a>Сценарий 1: вы получаете спрос перед периодом времени упреждения для номенклатуры

Потребность может возникнуть либо относительно рано во времени упреждения для номенклатуры, либо непосредственно перед началом периода времени упреждения. Вот пример такого сценария:

- У номенклатуры "Демопродукт" время упреждения заказа на покупку составляет шесть дней.
- В день ноль (1 января) уровень запасов для номенклатуры "Демопродукт" равен 0 (нулю).
- В день ноль (1 января) вы получаете заказ на продажу для количества 10 номенклатуры "Демопродукт".
- На седьмой день (8 января) существует заказ на покупку 10 единиц номенклатуры "Демопродукт".

На следующем рисунке показано графическое представление этого сценария.

![Графическое представление сценария 1.](./media/negative-days-1.jpg)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Случай A. Отрицательные дни меньше времени упреждения номенклатуры

Если в качестве отрицательных дней указано число, меньшее, чем время упреждения, MRP выполняет поиск приходов номенклатуры "Демопродукт" в пределах временной границы отрицательных дней. Поскольку таких приходов не обнаруживается, программа MRP создает новый спланированный заказ на покупку. Этот спланированный заказ немедленно задерживается на шесть дней (время упреждения). Таким образом, он поступит 7 января. Существующий заказ на покупку получает сообщение действия **Отмена**, так как создание нового спланированного заказа на покупку сделало его избыточным.

На следующем рисунке показан снимок экрана этого случая.

![Снимок экрана случая A для сценария 1.](./media/negative-days-2.png)

На следующем рисунке показано графическое представление того, что происходит в этом случае.

![Графическое представление случая A для сценария 1.](./media/negative-days-3.png)

Если вы считаете производительности и планирование MRP нервными, этот случай не выполняется хорошо. MRP требуется создать новый спланированный заказ и необходимо рассчитать задержки и действия. На этим задачи требуется много времени. Этот случай также добавляет еще две проводки в ваш план. С другой стороны, заказ на продажу откладывается только на шесть дней, а не на семь.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Случай B. Отрицательные дни больше времени упреждения номенклатуры

Чтобы повысить производительность MRP, можно установить для отрицательных дней число, большее чем время упреждения номенклатуры. Так как вы не можете получить поставку в течение времени упреждения в этом случае, вы можете выполнить поиск приходов, пока такой поиск имеет смысл. Хотя время выполнения для MRP будет короче, следует следить за дополнительными задержками заказов.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Случай C. Автоматическая корреляция времени упреждения для номенклатуры с временной границей отрицательных дней

Для автоматической корреляции времени упреждения для номенклатуры с временной границей отрицательных дней используйте динамические отрицательные дни. Для использования динамических отрицательных дней откройте **Сводное планирование \> Настройка \> Параметры сводного планирования**, затем на вкладке **Общие** в разделе **Покрытие** установите для параметра **Использовать распространение отрицательных дней** значение **Да**. Затем MRP выполняет поиск поступлений в пределах временной границы динамических отрицательных дней. Эта временная граница рассчитывается по следующей формуле:

Временная граница динамических отрицательных дней = Время упреждения покупки + Временная граница отрицательных дней + (Текущая дата – Дата потребности)

(Если типом заказа по умолчанию для номенклатуры "Демопродукт" является **Производство** или **Перемещение**, время упреждения равно времени упреждения для параметра **Запасы**.)

Когда используются динамические отрицательные дни, временная граница, в которой система MRP выполняет поиск поступлений, теперь равна 6 + 2 + 0 = 8 дней. MRP находит существующий заказ на покупку и сопоставляет ему заказ на продажу. Новые спланированные заказы не создаются. Таким образом, время выполнения MRP короче. На следующем рисунке показаны чистые потребности для номенклатуры "Демопродукт".

![Чистые потребности для варианта C для сценария 1.](./media/negative-days-4.png)

На следующем рисунке показано графическое представление того, что происходит в этом случае.

![Графическое представление случая C для сценария 1.](./media/negative-days-5.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Случай D. Использование только динамических отрицательных дней

Если для отрицательных дней задать значение **0** (ноль) и использовать только динамические отрицательные дни, временная граница для динамических отрицательных дней равна 6 + 0 + 0 = 6 дней. В этом случае результат совпадает с результатом для случая A этого сценария. MRP требуется создать новый спланированный заказ и необходимо рассчитать задержки и действия. Эти задачи потребляют много времени и могут раздражать. Кроме того, имеется еще две проводки для обработки. Так как потребность не может быть покрыта вовремя для прибытия номенклатуры, в этом случае в план добавляются ненужные сложности.

На следующем рисунке показан снимок экрана для этого случая.

![Снимок экрана случая D для сценария 1.](./media/negative-days-6.png)

На следующем рисунке показано графическое представление того, что происходит в этом случае.

![Графическое представление случая D для сценария 1.](./media/negative-days-7.png)

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Случай E. Использование как отрицательных дней, превышающих время упреждения номенклатуры, так и временной границы для динамических отрицательных дней

Если для отрицательных дней указано число, большее, чем время упреждения для номенклатуры, а если также используется временная граница динамических отрицательных дней, то временная граница динамических отрицательных дней равна 6 + 6 + 0 = 12 дней. Такой подход может создать очень долгую временную границу, в которой система MRP должна искать результаты. Сведения о том, как случай E связан с ситуацией, когда для отрицательных дней задаются длительная временная граница, см. в разделе [Заключение](#conclusion) данной статьи.

## <a name="scenario-2-you-get-demand-during-the-items-lead-time-period"></a>Сценарий 2: вы получаете спрос во время упреждения для номенклатуры

В течение времени упреждения номенклатуры может возникнуть потребность. Вот пример такого сценария:

- У номенклатуры "Демопродукт" время упреждения заказа на покупку составляет шесть дней. 
- В день ноль (1 января) уровень запасов для номенклатуры "Демопродукт" равен 0 (нулю).
- На четвертый день (5 января), который находятся в пределах периода упреждения для номенклатуры, вы получаете заказ на продажу 10 единиц номенклатуры "Демопродукт".
- На седьмой день (8 января) имеется заказ на покупку 10 единиц номенклатуры "Демопродукт".

На следующем рисунке показано графическое представление этого сценария.

![Графическое представление сценария 2.](./media/negative-days-8.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Случай A. Отрицательные дни меньше времени упреждения номенклатуры

Если в качестве отрицательных дней указано число, меньшее, чем время упреждения, MRP выполняет поиск приходов номенклатуры "Демопродукт" в пределах временной границы отрицательных дней. Так как в этом случае система MRP не обнаруживает поступлений, создается новый спланированный заказ на покупку, в котором в качестве даты заказа используется текущая дата. Этот спланированный заказ немедленно задерживается на шесть дней (время упреждения). Таким образом, он поступит 7 января. Существующий заказ на покупку получает сообщение действия **Отмена**, так как создание нового спланированного заказа на покупку сделало его избыточным.

На следующем рисунке показан снимок экрана для этого случая.

![Снимок экрана случая A для сценария 2.](./media/negative-days-9.png)

На следующем рисунке показано графическое представление того, что происходит в этом случае.

![Графическое представление случая A для сценария 2.](./media/negative-days-10.png)

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Случай B. Отрицательные дни больше времени упреждения номенклатуры

Этот случай похож на случай B для сценария 1. Если для отрицательных дней указано число, большее, чем время упреждения для номенклатуры, новый спланированный заказ не создается. Заказ на продажу присоединяется к существующему заказу на покупку.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Случай C. Автоматическая корреляция времени упреждения для номенклатуры с временной границей отрицательных дней

Этот случай похож на случай C для сценария 1, так как динамические отрицательные дни работают так же, как и в этом случае. Временная граница динамических отрицательных дней теперь составляет 6 + 2 – 4 = 4 дня. При использовании такого подхода система MRP находит существующий заказ на покупку и присоединяет к нему заказ на продажу. Поскольку новые спланированные заказы не создаются, время выполнения MRP сокращается.

На следующем рисунке показан снимок экрана этого случая.

![Снимок экрана случая C для сценария 2.](./media/negative-days-11.png)

На следующем рисунке показано графическое представление того, что происходит в этом случае.

![Графическое представление случая C для сценария 2.](./media/negative-days-12.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Случай D. Использование только динамических отрицательных дней

Если для отрицательных дней задать значение **0** (ноль) и использовать только динамические отрицательные дни, временная граница для динамических отрицательных дней теперь равна 6 + 0 – 4 = 2 дня. В этом случае результат совпадает с результатом для случая A этого сценария. Графическое представление происходящего см. в случае A для этого сценария.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Случай E. Использование как отрицательных дней, превышающих время упреждения номенклатуры, так и временной границы для динамических отрицательных дней

Если для отрицательных дней указано число, большее, чем время упреждения для номенклатуры, а если также используется временная граница динамических отрицательных дней, то временная граница динамических отрицательных дней равна 6 + 6 – 4 = 8 дней. Такой подход может создать очень долгую временную границу, в которой система MRP должна искать результаты. Сведения о том, как случай E связан с ситуацией, когда для отрицательных дней задаются длительная временная граница, см. в разделе [Заключение](#conclusion) данной статьи.

## <a name="scenario-3-you-get-demand-after-the-items-lead-time-period"></a>Сценарий 3: вы получаете спрос после периода времени упреждения для номенклатуры

Потребность может возникать после времени упреждения для номенклатуры. Вот пример такого сценария:

- У номенклатуры "Демопродукт" время упреждения заказа на покупку составляет шесть дней.
- В день ноль (1 января) запасы для номенклатуры "Демопродукт" равны 0 (нулю).
- На седьмой день (8 января), который находятся за пределами периода упреждения для номенклатуры, вы получаете заказ на продажу 10 единиц номенклатуры "Демопродукт".
- На десятый день (11 января) имеется заказ на покупку 10 единиц номенклатуры "Демопродукт".

На следующем рисунке показано графическое представление этого сценария.

![Графическое представление сценария 3.](./media/negative-days-13.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Случай A. Отрицательные дни меньше времени упреждения номенклатуры

Если в качестве отрицательных дней указано число, меньшее времени упреждения номенклатуры, MRP ищет за два дня перед датой потребности по заказу на продажу. Поскольку ничего не найдено, система MRP создает спланированный заказ на покупку на 2 января. Этот спланированный заказ на покупку будет отгружаться точно вовремя, чтобы удовлетворить потребность по заказу на продажу. Существующий заказ на покупку получает сообщение о действии **Отмена**, так как он не нужен.

На следующем рисунке показан снимок экрана этого случая.

![Снимок экрана случая A для сценария 3.](./media/negative-days-14.png)

На следующем рисунке показано графическое представление того, что происходит в этом случае.

![Графическое представление случая A для сценария 3.](./media/negative-days-15.png)

> [!NOTE]
> На предыдущем снимке экрана дата потребности для заказа на покупку — 12 января. Так как этот снимок экрана был сделан в 2015 г, когда 11 января приходилось на воскресенье, система MRP переместила дату потребности на следующий рабочий день, который был в понедельник, 12 января. Тем не менее, заказ на покупку имеет дату поставки 11 января.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Случай B. Отрицательные дни больше времени упреждения номенклатуры

Если для отрицательных дней указано число, большее, чем время упреждения для номенклатуры, новый спланированный заказ не создается. Заказ на продажу сопоставляется с существующим заказом на покупку. Таким образом, заказ на продажу задерживается. При создании спланированного заказа можно вовремя отгрузить заказ на продажу.

На следующем рисунке показан снимок экрана этого случая.

![Снимок экрана случая B для сценария 3.](./media/negative-days-16.png)

На следующем рисунке показано графическое представление того, что происходит в этом случае.

![Графическое представление случая B для сценария 3.](./media/negative-days-17.png)

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Случай C. Автоматическая корреляция времени упреждения для номенклатуры с временной границей отрицательных дней

Этот случай похож на случай C для сценария 1, так как динамические отрицательные дни работают так же, если не лучше, чем в случае B для этого сценария.

Временная граница динамических отрицательных дней составляет 6 + 2 – 7 = 1 день. Однако в этом случае система все еще учитывает время упреждения отрицательных дней (2), поскольку система MRP учитывает максимальное значение между временем упреждения отрицательных дней и временем упреждения динамических отрицательных дней. Поэтому результат в этом случае совпадает с результатом для случая A этого сценария.

На следующем рисунке показано графическое представление того, что происходит в этом случае.

![Графическое представление случая C для сценария 3.](./media/negative-days-18.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Случай D. Использование только динамических отрицательных дней

Если для отрицательных дней задать значение **0** (ноль) и использовать только динамические отрицательные дни, временная граница для динамических отрицательных дней теперь равна 6 + 0 – 7 = –1 день. В этом случае система по-прежнему учитывает время упреждения отрицательных дней (2). Поэтому результат в этом случае совпадает с результатом для случая A этого сценария и имеет те же самые недостатки. Графическое представление происходящего см. в случае A для сценария 2.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Случай E. Использование как отрицательных дней, превышающих время упреждения номенклатуры, так и временной границы для динамических отрицательных дней

Этот случай совпадает с вариантом E для сценариев 1 и 2. Он обладает практически теми же преимуществами и недостатками.

## <a name="conclusion"></a>Заключение

Как показывают три сценария в этой статье, рекомендуется установить для отрицательных дней число, большее, чем время упреждения номенклатур в группе покрытия. Кроме того, рекомендуется использовать только динамические отрицательные дни и устанавливать для отрицательных дней число дней, которые вы готовы ожидать перед заказом нового пополнения, если имеется отрицательный запас (иными словами, число дней, на которое вы готовы дополнительно задержать потребность). Кроме того, номенклатуры в одной группе покрытия должны иметь аналогичные значения времени упреждения.

Если для отрицательных дней установить значение **0** (ноль) и не использовать динамические отрицательные дни, MRP всегда создает новый спланированный заказ для удовлетворения спроса. В этой ситуации важно работать с сообщениями по действиям, чтобы гарантировать, что запасы не будут накапливаться.

Может настроить отрицательные дни для длительной временной границ, а затем работать с сообщениями по действиям. Такой подход дает хороший результат планирования, но он немного медленнее. Его также может быть труднее анализировать, так как необходимо анализировать и применять сообщения по действиям. Рассмотрим пример:

- У номенклатуры "Демопродукт" время упреждения заказа на покупку составляет шесть дней.
- В день ноль (1 января) запасы для номенклатуры "Демопродукт" равны 0 (нулю).
- В день ноль (1 января) вы получаете заказ на продажу для количества 10 номенклатуры "Демопродукт".
- В девятый день (10 января) вы получаете заказ на продажу для количества 10 номенклатуры "Демопродукт".
- На одиннадцатый день (12 января) имеется заказ на покупку 10 единиц номенклатуры "Демопродукт".
- Отрицательные дни устанавливаются равными **20**, что намного превышает время упреждения номенклатуры.

На следующем рисунке показано графическое представление того, что происходит.

![Графическое рассмотрение примера.](./media/negative-days-19.png)

MRP дает следующие результаты.

![Пример результатов 1.](./media/negative-days-20.png)

На предыдущем снимке экрана дата потребности в заказе на продажу — 9 января вместо 10 января. Так как этот снимок экрана был сделан в 2015 г, когда 10 января приходилось на субботу, дата потребности заказа должна быть предыдущим рабочим днем, который был в пятницу, 9 января.

MRP создает спланированный заказ на покупку для удовлетворения спроса, запрошенного первым заказом на продажу, но затем также рекомендует отменить спланированный заказ, поскольку можно переместить существующий заказ на покупку и увеличить количество в нем.

Результаты не являются неправильными, но время выполнения MRP может быть больше, так как MRP требуется создать все задержки и предложения. Кроме того, планировщику может потребовать больше времени для понимания результатов MRP. Самое главное в этом случае: планировщику важно понимать и использовать сообщения по действиям.

Если сократить отрицательные дни до числа, близкого ко времени упреждения номенклатуры, и использовать динамические отрицательные дни, MRP выдаст следующие результаты.

![Пример результатов 2.](./media/negative-days-21.png)

MRP создает спланированный заказ, прикрепленный к первому заказу на продажу. Затем, как ожидается, второй заказ на продажу привязан к существующему заказу на покупку на основе настройки отрицательных дней. Этот результат планирования также правильный, и время выполнения MRP может быть короче. В этом случае нет необходимости понимать и знать, как работать с сообщениями по действиям.

Для обеспечения того, чтобы были введены правильные значения для бизнеса, необходимо учитывать как функциональность, так и время выполнения MRP. Поэтому может потребоваться действовать немного методом проб и ошибок, чтобы определить оптимальные значения.

## <a name="see-also"></a>См. также

Дополнительное обсуждение см. в исходной записи блога [Подробнее о (динамических) отрицательных днях](/archive/blogs/axmfg/more-about-dynamic-negative-days).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
