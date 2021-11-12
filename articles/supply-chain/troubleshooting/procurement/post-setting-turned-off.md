---
title: Параметр "Выполнить разноску на счет накл. расходов в ГК" не включен
description: Эта проблема возникает, когда по заказу на покупку выставляется накладная, если параметр "Выполнить разноску на счет накл. расходов в ГК" включен на вкладке "Накладная" на странице "Параметры модуля расчетов с поставщиками".
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 592444958dad4624fdc9098dc58df0a2e49e63de
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477436"
---
# <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Параметр "Выполнить разноску на счет накл. расходов в ГК" не включен

## <a name="symptoms"></a>Симптомы

Эта проблема возникает, когда по заказу на покупку выставляется накладная, если параметр **Выполнить разноску на счет накл. расходов в ГК** имеет значение *Да* на вкладке **Накладная** на странице **Параметры модуля расчетов с поставщиками**.

## <a name="reproduce-the-issue"></a>Воспроизведение проблемы

Следующая процедура показывает один из способов воспроизведения проблемы.

1. Перейдите в раздел **Расчеты с поставщиками \> Настройка \> Параметры расчетов с поставщиками**.
1. На вкладке **Накладная** установите для параметра **Выполнить разноску на счет накл. расходов в ГК** значение *Да*.
1. Выберите **Управление запасами \> Настройка \> Разноска \> Разноска**.
1. На вкладке **Заказ на покупку** убедитесь, что удалены все строки в расходах на покупку для продукта.
1. Перейдите в раздел **Расчеты с поставщиками \> Заказы на покупку \> Все заказы на покупку**.
1. Создание заказа на покупку. В поле **Счет поставщика** выберите *1001 Офисные принадлежности ACME*.
1. Добавьте строку заказа на покупку со следующими параметрами:

    - **Код номенклатуры:** *D0011 лазерный проектор*
    - **Сайт:** *1*
    - **Склад:** *11*
    - **Количество:** *4*

1. В области действий на вкладке **Покупка** в группе **Действие** выберите **Подтвердить**.
1. В области действий на вкладке **Получить** в группе **Создать** выберите **Поступление продуктов**.
1. В диалоговом окне **Разноска поступления продуктов** в поле **Поступление продукта** введите произвольный номер, затем выберите **ОК**.
1. На панели операций на вкладке **Накладная** в группе **Создать** выберите **Накладная**.
1. В поле **Номер** введите произвольный номер в качестве номера накладной.
1. Обновите статус сопоставления и выполните разноску.
1. Обратите внимание, что теперь при создании накладной из заказа на покупку появляется следующая ошибка: "Номер счета для типа проводки расходов на закупку продукта не существует".

## <a name="resolution"></a>Решение

Это зависит от настроек параметров для накладных и групп накладных. Дополнительные сведения см. в следующей записи блога: [Учет накладных расходов на покупку и изменение запасов](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).