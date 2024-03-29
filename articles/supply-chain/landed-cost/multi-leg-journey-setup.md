---
title: Настройка пути с несколькими отрезками
description: В этой статье описывается, как настроить пути с несколькими отрезками для модуля "Стоимость на складе".
author: Weijiesa
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMLegTable, ITMJourneyTable, ITMActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: dcb536c03d09d51b247d9060d87db64e2b80383b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905844"
---
# <a name="multi-leg-journey-setup"></a>Настройка пути с несколькими отрезками

[!include [banner](../../includes/banner.md)]

В этой статье описывается, как настроить пути с несколькими отрезками для модуля **Стоимость на складе**.

## <a name="legs"></a>Участки пути

Отрезки используются для идентификации отдельных частей пути. Каждый отрезок создается путем выбора портов отгрузки "из" и "в" и метода транспортировки, используемого для этого отрезка. Время упреждения может быть связано с каждым отрезком. Время упреждения может помочь отслеживать отгрузку и может также использоваться для расчета ожидаемой даты поставки товаров в рейсе. Кроме того, когда отрезок пути завершен, статус рейса, контейнера отгрузки и связанных строк заказа на покупку можно обновить с помощью настройки управления отслеживанием. Отрезки могут использоваться одним шаблоном пути или могут быть повторно использованы в нескольких шаблонах пути. Загрузка контейнера, таможенные процедуры и местная транспортировка обычно настраиваются как отрезки, и для них используется не конкретный порт отгрузки.

Для работы с отрезками перейдите **Стоимость на складе \> Настройка пути с несколькими отрезками \> Отрезки**. Там можно просматривать, открывать, создавать и удалять записи для отрезков. В следующей таблице описываются поля, которые доступны для каждой записи.

| Поле | описание |
|---|---|
| Участок пути | Введите уникальное идентификационное имя/номер для отрезка пути. |
| описание | Введите описание отрезка журнала. Обычно это описание определяет порты "в" и "из" или этап пути. |
| Порт отправления | Введите место происхождения товаров в отрезке. |
| Порт назначения | Введите место назначения товаров в отрезке. |
| Способ доставки | Введите способ транспортировки для отрезка. |

## <a name="journey-templates"></a>Шаблоны пути

Шаблон пути определяет путь с несколькими отрезками между двумя портами, в которые перемещаются товары во время рейса. Отрезки пути комбинируются для определения количества времени, которое потребуется для перемещения товаров от места происхождения поставщика до конечного склада назначения. Когда отрезки вносятся в шаблон пути в конкретном заказе, время упреждения будет определять дату каждого отрезка и статус рейса, контейнера и строк покупки для рейса. [Центр управления отслеживания](delivery-information-setup.md) используется для настройки времени упреждения, связанного с каждым отрезком, из которых состоит шаблон пути. Шаблон пути также используется при настройке автоматических затрат рейса. Когда определяется путь, затраты, связанные с транспортировкой товаров, могут быть определены на странице автоматических затрат.

Для работы с шаблонами пути перейдите **Стоимость на складе \> Настройка пути с несколькими отрезками \> Шаблоны пути**. Там можно просматривать, открывать, создавать и удалять шаблоны пути.

Для каждого шаблона пути установите следующие поля в заголовке.

| Поле | описание |
|---|---|
| Шаблон пути | Введите уникальное идентификационное имя/номер для шаблона пути. Шаблон пути обычно описывает место происхождения и место назначения для пути. |
| описание | Введите описание шаблона пути. Описание обычно указывает на порты "в" и "из" и тип перемещения. |

В разделе **Строки** добавьте строку для каждого отрезка пути и разместите строки в порядке. Для изменения порядка строк можно использовать стрелки **вверх** и **вниз** на панели инструментов. В следующей таблице описываются поля, которые доступны для каждой строки.

| Поле | описание |
|---|---|
| Участок пути | Выберите отрезок для добавления в путь. |
| описание | Описание отрезка. |
| Порт отправления | Порт, который является местом происхождения товаров в отрезке. Этот порт является портом "в", используемым для определения автоматических затрат для рейса. |
| Порт назначения | Окончательный порт назначения товаров в отрезке. |
| Способ поставки | Способ доставки, используемый для отрезка. |
| Порт отправления пути | Если порт, указанный для отрезка, используется для определения автоматических затрат, установите этот флажок, чтобы указать, что он является портом, из которого начинается путь. Этот порт будет отображаться в заголовке рейса. |
| Порт назначения пути | Если порт, указанный для отрезка, используется для определения автоматических затрат, установите этот флажок, чтобы указать, что он является портом, в котором заканчивается путь. Этот порт будет отображаться в заголовке рейса. |
| Компания по отгрузке | Выберите транспортную компанию, которая используется для этого отрезка. |

## <a name="activities"></a>Мероприятия

Настройки на странице **Мероприятия** определяют типы мероприятий, которые могут выполняться в порту назначения отрезка. Пользователи, работающие на странице **Все контейнеры отгрузки**, могут выбирать среди этих значений при оценке длительности каждого мероприятия и регистрации фактической длительности для сравнения.

Для настройки мероприятий перейдите **Стоимость на складе \> Настройка путей с несколькими отрезками \> Мероприятия**. Здесь можно использовать кнопки на панели операций для добавления, удаления и редактирования мероприятий.

В следующей таблице описываются поля, которые доступны для каждого мероприятия в сетке.

| Поле | описание |
|---|---|
| Деятельность | Имя мероприятия. |
| описание | Описание мероприятия. |
| Компания по отгрузке | Счет поставщика транспортной компании, связанный с мероприятием. |
