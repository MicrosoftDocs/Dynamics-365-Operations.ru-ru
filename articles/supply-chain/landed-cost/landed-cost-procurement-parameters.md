---
title: Параметры модуля "Закупки и источники" для стоимости на складе
description: В этом разделе описывается, как настроить соответствующие параметры закупок и источников при использовании модуля стоимости на складе.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ccda3bd769a646e2390711883b8e40bec50e4d6a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020991"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a>Параметры модуля "Закупки и источники" для стоимости на складе

[!include [banner](../../includes/banner.md)]

На странице **Параметры модуля "Закупки и источники"** есть несколько настроек, которые особенно подходят при использовании модуля **Стоимость на складе**. Используйте диалоговое окно **Обновление строк заказа**, которое открывается со страницы **Параметры модуля "Закупки и источники"**, чтобы указать, должны ли строки заказа на покупку автоматически обновляться при внесении изменений в заголовок заказа на покупку.

Чтобы завершить эту настройку, выполните следующие действия.

1. Выберите **Закупки и источники \> Настройка \> Параметры модуля "Закупки и источники"**.
1. На вкладке **Общее** выберите ссылку **Обновление строк заказа**.
1. В диалоговом окне **Обновление строк заказа** перечислены поля в заголовке заказа, которые также могут применяться при автоматическом обновлении к соответствующим полям в строках заказа. Задайте в каждом поле в списке одно из следующих значений:

    - **Всегда** — строки заказа должны обновляться автоматически при обновлении заголовка заказа.
    - **Никогда** — строки заказа не должны никогда обновляться при обновлении заголовка заказа.
    - **Запрос** — пользователю будет предложено указать, следует ли обновлять строки заказа.
