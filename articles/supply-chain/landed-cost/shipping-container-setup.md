---
title: Грузовые контейнеры
description: В этой статье описывается, как настроить контейнеры отгрузки для модуля "Стоимость на складе".
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 345f815a4f85db30db18aba3f8a4d41835c2e3f2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860852"
---
# <a name="shipping-container-setup"></a>Настройка контейнера отгрузки

[!include [banner](../../includes/banner.md)]

В этой статье описывается, как настроить контейнеры отгрузки для модуля **Стоимость на складе**.

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a>Настройка типов контейнеров отгрузки

Типы контейнеров отгрузки определяют типы контейнеров отгрузки, которые доступны для использования во время отгрузки и рейсов.

Для работы с типами контейнеров отгрузки перейдите **Стоимость на складе \> Настройка контейнеров \> Типы контейнеров отгрузки**. Там можно просматривать, добавлять и удалять записи для типов контейнеров. В следующей таблице описываются поля, которые доступны для каждой записи.

| Поле | описание |
|---|---|
| Тип грузового контейнера | Введите уникальное идентификационное имя/номер для типа контейнера отгрузки. |
| описание | Введите описание типа контейнера отгрузки. |
| Объем | Введите максимальный объем, разрешенный в контейнерах отгрузки этого типа. |
| Вес | Введите максимальный вес, разрешенный в контейнерах отгрузки этого типа. |
| Возвращаемые | Укажите, могут ли контейнеры отгрузки этого типа возвращаться поставщику после их использования во время рейса. Если этот параметр задан как *Да*, то для возврата контейнеров отгрузки этого типа в порт происхождения могут применяться дополнительные затраты. |

## <a name="set-up-shipping-containers"></a>Настройка контейнеров отгрузки

Записи контейнеров отгрузки используются для определения всех контейнеров, используемых во время рейса. При создании рейса можно выбрать конкретный контейнер для него в списке всех записей контейнера отгрузки, которые были определены здесь. Эта функция особенно полезна, если ваша компания владеет собственными контейнерами отгрузки.

Нет необходимости вводить номера контейнеров отгрузки для контейнеров отгрузки, которые будут использоваться только один раз. Вместо этого можно добавить номер контейнера отгрузки при создании рейса.

Записи контейнеров отгрузки используются только в стоимости на складе. Они недоступны в стандартном модуле **Управление транспортировкой** (TMS).

Для работы с контейнерами отгрузки перейдите **Стоимость на складе \> Настройка контейнеров \> Контейнеры отгрузки**. Там можно просматривать, добавлять и удалять записи для контейнеров отгрузки. В следующей таблице описываются поля, которые доступны для каждой записи.

| Поле | описание |
|---|---|
| Грузовой контейнер | Введите уникальное идентификационное имя/номер для контейнера отгрузки. |
| Тип грузового контейнера | Выберите тип контейнера отгрузки. Дополнительные сведения см. в разделе [Настройка типов контейнеров отгрузки](#shipping-container-types) ранее в данной статье. |

> [!NOTE]
> - Настройка контейнера отгрузки необязательная. Обычно она используется только в том случае, если компания владеет собственными контейнерами отгрузки или часто использует одни и те же контейнеры отгрузки.
> - Для номеров контейнеров отгрузки не вычисляются контрольные разряды.

## <a name="set-up-unit-types"></a><a name="unit-types"></a>Настройка типов единиц

Типы единиц измерения определяют дополнительные методы группирования и идентификации для контейнеров отгрузки. Тип единицы измерения обычно используется для определения типа контейнера, в котором упакованы товары, например, палеты или барабаны. Тип единицы можно выбрать при настройке контейнера на странице **Все контейнеры отгрузки**.

Типы единиц используются только в стоимости на складе. Они недоступны в TMS.

Для работы с типами единиц перейдите **Стоимость на складе \> Настройка контейнеров \> Типы единиц**. Там можно просматривать, добавлять и удалять записи для типов единиц. В следующей таблице описываются поля, которые доступны для каждой записи.

| Поле | описание |
|---|---|
| Тип подразделения | Введите уникальное идентификационное имя/номер для типа единиц. |
| описание | Введите описание типа единиц. |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a>Настройка типов холодильников

Типы холодильников задают методы группирования и определения контейнеров отгрузки (обычно это контейнеры-рефрижераторы). Тип холодильников можно выбрать при настройке контейнера на странице **Все контейнеры отгрузки**.

Для работы с типами холодильников перейдите **Стоимость на складе \> Настройка контейнеров \> Типы холодильников**. Там можно просматривать, добавлять и удалять записи для типов холодильников. В следующей таблице описываются поля, которые доступны для каждой записи.

| Поле | описание |
|---|---|
| Тип охлаждения | Введите уникальное идентификационное имя/номер для типа холодильников. |
| описание | Введите описание типа холодильников. |
