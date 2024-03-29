---
title: Настройка ставок, привязанных к индексу
description: В этой статье описывается, как настроить ставки, привязанные к индексу. Ставки, привязанные к индексам, требуются, если ваша организация связывает суммы платежей арендной платы с набором ставок, привязанных к индексу.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRateType
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e700c6c0c66b855a3e329302ac27681f4d0144a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883397"
---
# <a name="set-up-index-rates"></a>Настройка ставок, привязанных к индексу

[!include [banner](../includes/banner.md)]

Если платежи по аренде зависят от индекса, в системе можно добавлять и поддерживать типы ставок, привязанных к индексу. Чтобы переоценить платежи аренды со страницы **Тип ставки, привязанной к индексу**, процесс переоценки ставок, привязанных к индексу, использует самую последнюю ставку, привязанную к индексу, из даты переоценки.

Чтобы добавить типы ставок, привязанных к индексу, и ставки, привязанные к индексу, выполните следующие действия.

1. Перейдите в раздел **Аренда активов \> Настройка \> Типы ставок, привязанных к индексу**.
2. Выберите **Создать**.
3. В соответствующих полях введите тип ставки и имя ставки, привязанной к индексу.
4. Чтобы добавить новое значение ставки, привязанной к индексу, выберите тип ставки, привязанной к индексу, и затем выберите **Добавить**.
5. Выберите дату начала действия ставки и выберите значение ставки.

В качестве метода оценки индекса необходимо выбрать **Разница значений ставки, привязанной к индексу** или **Значение ставки, привязанной к индексу**.

- Выберите метод **Разница значений ставки, привязанной к индексу** для расчета нового платежа по аренде, основанный на разнице между ставкой, привязанной к индексу, на начальную дату и последней ставкой, привязанной к индексу. Ставка, привязанная к индексу, определяется в поле **Ставка, привязанная к индексу (%)**.
- Выберите метод **Значение ставки, привязанной к индексу** для расчета платежа по аренде с использованием процентного значения, указанного в поле **Ставка индекса (%)**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
