---
title: График индексов цен потребителя
description: В этой статье объясняется, как создать список графиков индекса потребительских цен (CPI), получаемых через Интернет, чтобы определить расходы на эскалацию в выставлении счетов по подпискам.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: f08b79ee00baab3713d9ccc24a7595b1de7a7768
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904883"
---
# <a name="consumer-price-index-schedule"></a>График индексов цен потребителя

[!include [banner](../includes/banner.md)]

В этой статье описывается порядок создания, удаления, просмотра и обработки графиков индекса потребительских цен (CPI). График CPI можно использовать для определения цен на потребительские товары и услуги, добавляемые в качестве строк графика выставления счетов. График CPI можно затем использовать в графике выставления счетов для эскалации и скидки в ценообразовании, либо можно выполнить обработку вручную, чтобы обновить суммы выставления счетов в графиках выставления счетов. Графики CPI можно ввести вручную или импортировать их, используя составную сущность графика CPI.

Чтобы добавить график CPI, выполните следующие действия.

1. На странице **График индекса потребительских цен** выберите **Создать**.
2. В поле **График индекса потребительских цен** введите уникальное имя.
3. В поле **Описание** введите описание.
4. На вкладке **График индекса потребительских цен** выберите **Добавить**.
5. В поле **Дата индекса потребительских цен** укажите дату, когда новый график CPI станет активным.
6. В поле **График индекса потребительских цен** введите имя, введенное на шаге 2.
7. Нажмите **Сохранить**.

Чтобы удалить дату графика CPI, выполните следующие действия.

1. На странице **График индекса потребительских цен** выберите одну или несколько строк, которые необходимо удалить, затем выберите **Удалить**.
2. Чтобы удалить весь график CPI, в области действий выберите **Удалить**. Нельзя удалить выбранный график CPI, если он связан с любым графиком выставления счетов.
3. В области действий выберите **Обработать**, чтобы обновить графики выставления счетов, использующие выбранный график CPI. Последние даты CPI и суммы графика будут использоваться для обновления цен графика выставления счетов.
4. На экспресс-вкладке **Обработка индекса потребительских цен** просмотрите обновленные поля **Код графика выставления счетов**, **Код номенклатуры**, **Дата начала выставления счетов**, **Дата окончания выставления счетов**, **Дата эскалации** и **Частота эскалации**.

После настройки графиков CPI они могут использоваться для изменения цен эскалации и скидок в графиках выставления счетов.

## <a name="cpi-calculation"></a>Расчет CPI

Для этих примеров период с 1 января 2020 по 31 декабря 2022. Базовая ставка CPI (значение CPI при запуске контракта) равно 105,65. На 1 января 2021 текущее значение CPI равно 110,5. На 1 января 2022 текущее значение CPI равно 114,25. Исходная сумма равна 1 000 долларов США.

**Пример 1**

На странице **Параметры выставления счетов по контракту** в поле **Вычисление индекса потребительских цен** значение **Базовый индекс потребительских цен**.

Для периода с 1 января 2021 первая сумма эскалации рассчитывается следующим образом на основе начальной суммы:

1 000 + (110,5 – 105,65) &divide; 105,65 &times; 1 000 = 1 045,91

Для периода с 1 января 2022 сумма эскалации рассчитывается следующим образом:

1 000 + (114,25 – 105,65) &divide; 105,65 &times; 1 000 = 1 081,40

**Пример 2**

На странице **Параметры выставления счетов по контракту** в поле **Вычисление индекса потребительских цен** значение **Предыдущий индекс потребительских цен**.

Для периода с 1 января 2021 первая сумма эскалации рассчитывается следующим образом на основе начальной суммы:

1 000 + (110,5 – 105,65) &divide; 105,65 &times; 1 000 = 1 045,91

Для периода с 1 января 2022 сумма эскалации рассчитывается следующим образом на основе первой суммы эскалации:

1 045,91 + (114,25 – 110,5) &divide; 110,5 &times; 1 045,91 = 1 081,40

> [!NOTE]
> Процесс эскалации всегда использует самое последнее значение CPI, независимо от даты индекса. Например, если эскалация производится в сентябре, а последнее значение CPI имеется за июль, используется индекс за июль. После ввода индекса за сентябрь изменения не выполняются.

## <a name="prorated-escalation"></a>Пропорциональная эскалация

Если эскалация происходит в середине периода выставления счетов, сумма увеличивается пропорционально. Например, период выставления счетов берется с 1 августа 2020 по 31 июля 2021. На дату CPI 1 сентября 2019 года значение CPI равно 244. На дату CPI 1 сентября 2020 года это значение CPI равно 250. Если предыдущая ставка равна 1 000, для расчета суммы выставления счетов за период используются следующие формулы:

* *Изменения CPI* = (250 – 244) &divide; 244 = 2,459%
* *Текущая ставка* = 1 000 &times; 2,459% = 1 024,59
* *Количество дней по текущей ставке* = 31 июля 2021 – 1 сентября 2020 = 334
* *Предыдущая ставка* = 1 000
* *Количество дней по предыдущей ставке* = 31 августа 2020 – 1 августа 2020 = 31
* *Общее количество дней в периоде выставления счетов* = 31 июля 2021 – 1 августа 2020 + 1 = 365
* *Сумма счета за этот период* = (1 000 &times; 31 &divide; 365) + (1 024,59 &times; 334 &divide; 365) = 1 022,50

## <a name="escalation-that-uses-the-cpi-and-percentage"></a>Эскалация, в которой используется CPI и процент

Эскалации можно выполнить, используя CPI. Значение CPI плюс 3 процента эскалации начинается с 1 января 2020 года и имеет годовую частоту.

- Сумма, выставленная за период с 1 января 2019 года по 31 декабря 2020 года составляет 4 000.
- Период выставления счетов, для которого будет выполнена эскалация, — с 1 января 2020 г. по 31 декабря 2020 г.
- На дату CPI 1 декабря 2018 года значение CPI равно 205,3. На дату CPI 1 декабря 2019 года значение CPI равно 219,6.

Если предыдущая ставка равна 4 000, сумма выставления счетов за этот период рассчитывается следующим образом:

- *Изменения CPI* = (219,6 – 205,3) &divide; 205,3 = 6,965%
- *Текущая ставка* = (4 000 &times; 6,965%) – 4000 = 278,60
- *Процент изменений* = (4 000 &times; 1,03) – 4 000 = 120
- *Сумма выставления счетов* = 4 000 + 278,6 + 120 = 4 398,6
