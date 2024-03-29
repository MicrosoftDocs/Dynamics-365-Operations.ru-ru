---
title: Шаблоны этапов
description: В этой статье объясняется, как настроить функциональность выставления счетов по этапам в выставлении счетов по подпискам.
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
ms.openlocfilehash: d3c2cf751e4998c73bc3816e5b81e8d5963c8e53
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856780"
---
# <a name="milestone-billing"></a>Выставление счетов по этапам

[!include [banner](../includes/banner.md)]

В этой статье объясняется, как определять шаблоны для функциональности выставления счетов по этапам в выставлении счетов по подпискам. Для каждой строки шаблона этапа можно определить процент или сумму распределения. Затем можно назначить шаблон этапа элементам графика выставления счетов, в которых используется функция выставления счетов по этапам.

## <a name="add-a-template"></a>Добавить шаблон

Чтобы добавить шаблон этапа, выполните следующие действия.

1. Перейдите к пункту **Выставление счетов по подпискам \> Периодическое выставление счетов по контракту \> Настройка \> Шаблоны этапов**.
2. Выберите **Создать**.
3. В поле **Шаблон этапа** введите уникальный код для нового шаблона.
4. В поле **Описание** введите описание.
5. В поле **Метод распределения** выберите метод распределения.
6. Необязательно: в поле **Общая сумма** укажите общую сумму для шаблона.
7. Чтобы добавить строку, выберите **Добавить**. Затем в поле **Код номенклатуры** выберите код номенклатуры для новой строки.
8. Выполните одно из следующих действий в зависимости от значения, выбранного в поле **Метод распределения**.

    - Если в качестве метода распределения выбрано значение **Процент**, в поле **Процент** укажите процент распределения для каждой строки. Если указать проценты, сумма процентов, показанная в поле **Общий процент**, должна равняться **100**.
    - Если в качестве метода распределения выбрано значение **Переменная сумма**, в поле **Сумма** укажите сумму для каждой строки.
    - Если в качестве метода распределения выбрано значение **Равная сумма**, нет необходимости указывать сумму. Каждая строка будет обновлена с правильным процентом и суммой на основе количества номенклатур, добавляемых к шаблону.

9. Нажмите **Сохранить**.

## <a name="delete-a-template"></a>Удаление шаблона

Чтобы удалить шаблон этапа, выполните следующие действия.

1. Выберите одну или несколько строк для удаления, затем выберите **Удалить**.
2. Когда выводится запрос подтверждения действия, выберите **Да**.

## <a name="milestone-template-fields"></a>Поля шаблона этапа

Страница **Шаблон этапа** содержит следующие поля.

| Поле | Описание |
|-------|-------------| 
| Шаблон этапа | Уникальный идентификатор шаблона этапа. |
| Описание | Описание шаблона этапа. |
| Метод распределения | <p>Выберите метод распределения:</p><ul><li>**Процент завершения** — совокупное значение завершения используется для каждой строки.</li><li>**Процент** — процентная сумма может быть указана для распределения. Сумма всех процентов должна равняться 100.</li><li>**Переменная сумма** — сумма может быть указана для распределения. Сумма распределения указывается на уровне проводки.</li><li>**Равная сумма** — проценты распределения автоматически рассчитываются и равномерно распределяются между номенклатурами в шаблоне.</li></ul> |
| Общая сумма | Укажите сумму этапа для шаблона. |
| **Линии** | |
| Код номенклатуры | Выберите код номенклатуры для шаблона этапа. |
| Имя продукта | Наименование номенклатуры. |
| Процент | <p>Введите процент распределения для строки:</p><ul><li>Если для поля **Метод распределения** установлено значение **Процент**, укажите процент для строки.</li><li>Если в поле **Метод распределения** задано значение **Равная сумма**, процент автоматически распределяется по равным процентам на основе количества номенклатур в шаблоне.</li></ul><p>Сумма всех процентов должна равняться 100.</p><p>Если значение **Итоговая сумма** указано в заголовке и вы изменяете значение **Процент** для строки, значение **Сумма** обновляется. И наоборот, при изменении значения **Сумма** значение **Процент** обновляется.</p> |
| Сумма | <p>Сумма распределения для строки:</p><ul><li>Если для поля **Метод распределения** установлено значение **Переменная сумма**, укажите сумму для строки.</li><li>Если в поле **Метод распределения** задано значение **Равная сумма**, сумма автоматически распределяется на равные суммы на основе количества номенклатур в шаблоне и значения **Итоговая сумма**, указанного в заголовке.</li></ul><p>Сумма всех сумм должна равняться значению **Итоговая сумма**, указанному в заголовке.</p><p>Если значение **Итоговая сумма** указано в заголовке и вы изменяете значение **Сумма** для строки, значение **Процент** обновляется. И наоборот, при изменении значения **Процент** значение **Сумма** обновляется.</p> |
| **Итого** | |
| Общий процент | Сумма процентов. Сумма всех процентов должна равняться 100. |
| Общая сумма | Сумма значений **Сумма** для всех строк. Эта сумма должна равняться значению **Итоговая сумма**, указанному в заголовке. |
| Сумма остатка | Оставшаяся сумма. Это значение рассчитывается как значение **Итоговая сумма** из заголовка минус сумма значений **Сумма** для всех строк.|

## <a name="milestone-allocation"></a>Распределение этапа

Прежде чем приступить к использованию функций этапов, необходимо выполнить следующие задачи.

1. Добавьте один или несколько шаблонов этапов.
2. Создайте группу графика выставления счетов. Укажите **Этап** в качестве типа номенклатуры и выберите шаблон.
3. На странице **Настройка номенклатуры** (**Выставление счетов по подпискам \> Периодическое выставление счетов по контракту \> Настройка \> Номенклатуры**) выберите связь номенклатуры и шаблон этапа для настройки номенклатуры.

После создания шаблонов этапов, групп графиков выставления счетов и номенклатур можно создать график выставления счетов, в котором используется функция этапов.

Чтобы настроить график выставления счетов, использующий этапы, выполните следующие действия.

1. В списке **Все/активные графики выставления счетов** на странице **Графики выставления счетов** выберите **Создать**.
2. На странице **Все графики выставления счетов** создайте новый график выставления счетов и укажите счет клиента и дату начала.
3. В разделе **Строки графика выставления счетов** выберите **Добавить строку**. Затем добавьте код номенклатуры и задайте для поля **Тип номенклатуры** значение **Этап**.

    Если для номенклатуры настроен шаблон этапа по умолчанию, события этапов автоматически добавляются в строки графика выставления счетов. Конечные даты для строк этапов не заполнены.

    Если для номенклатуры не настроен шаблон этапа, выберите **Распределение этапа**. Затем на странице **Распределение этапов** выберите шаблон этапа и внесите необходимые обновления. Затем выберите **Закрыть**, чтобы вернуться к графику выставления счетов, и завершите создание графика выставления счетов.

4. Для создания счетов для графика выставления счетов необходимо обновить конечную дату для каждого события этапа. Для одного графика выставления счетов можно обновить конечную дату для события этапа в строках графика выставления счетов. Для обновления нескольких графиков выставления счетов выберите **Процесс обновления даты завершения**.
5. После обновления даты окончания можно создать накладную. Для одного графика выставления счетов выберите **Создать накладную** на странице **Все графики выставления счетов**. Для создания накладных для нескольких графиков выставления счетов выберите **Создать накладную** или **Создать пакетную обработку накладных** в разделе **Периодические задачи**.

## <a name="edit-milestone-allocation-on-a-billing-schedule-line"></a>Изменение распределения этапов в строке графика выставления счетов

Чтобы изменить распределения этапов в строке графика выставления счетов, выполните следующие действия.

1. На странице **Графики выставления счетов** > **Все или активные графики выставления счетов** в поле **Номер графика** выберите номер графика выставления счетов.
2. В разделе **Строки графика выставления счетов** введите номенклатуру, укажите **Этап** в качестве номенклатуры и выберите **Распределение этапов**.
3. В поле **Шаблон этапа** выберите шаблон этапа.
4. Выберите **Обработать**. Строки шаблона этапа автоматически добавляются к строкам графика выставления счетов.

## <a name="milestone-allocation-fields"></a>Поля распределения этапа

Страница **Распределение этапа** содержит следующие поля.

| Поле | Описание |
|-------|-------------|
| Родительская номенклатура | Кода номенклатуры родительского элемента. |
| Сумма без учета скидок и наценок | <p>Сумма без учета скидок и наценок для номенклатуры. Значение соответствует значению **Чистая сумма** строки графика выставления счетов.</p></p>Для родительского элемента этапа значением по умолчанию является значение **Итоговая сумма**, которая указана для шаблона этапа. Если итоговая сумма равна 0 (нулю), значением по умолчанию будет **Чистая сумма** строки графика выставления счетов.</p> |
| Шаблон этапа | Идентификатор шаблона этапа номенклатуры строки. |
| Описание шаблона | Описание шаблона этапа. |
| Метод распределения | Метод распределения, используемый для шаблона этапа. |
| **Линии** | Значения по умолчанию для всех строк основаны на выбранном шаблоне этапе. Их можно изменить в соответствии с требованиями. |
| Код номенклатуры | Код номенклатуры для шаблона распределения этапа. |
| Имя продукта | Имя продукта. |
| Процент | <p>Процент распределения для строки. Сумма всех процентов должна равняться 100.</p><p>При изменении значения **Процент** для строки значение **Чистая сумма** обновляется. И наоборот, при изменении значения **Чистая сумма** значение **Процент** обновляется.</p> |
| Чистая сумма | <p>Сумма распределения для строки. Сумма чистых сумм для всех строк должна равняться значению **Сумма без учета скидок и наценок**, указанному в заголовке.</p><p>При изменении значения **Чистая сумма** для строки значение **Процент** обновляется. И наоборот, при изменении значения **Процент** значение **Чистая сумма** обновляется.</p> |
| **Итого** | |
| Итоговый процент | Сумма значений **Процент** для всех строк. Эта сумма должна равняться 100. |
| Общая сумма | Сумма значений **Чистая сумма** для всех строк. Эта сумма должна равняться значению **Сумма без учета скидок и наценок**, указанному в заголовке. |
| Сумма остатка | Оставшаяся сумма. Это значение рассчитывается как значение **Сумма без учета скидок и наценок** из заголовка минус сумма значений **Чистая сумма** для всех строк. Конечная сумма должна быть равна 0 (нулю). |
