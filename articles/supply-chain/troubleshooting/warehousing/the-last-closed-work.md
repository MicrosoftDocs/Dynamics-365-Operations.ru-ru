---
title: Последняя закрытая строка работы должна быть размещением
description: Последняя закрытая строка работы должна быть размещением
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 221c64c89d0e8addbf44acab8e7561e5f3a27239
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474756"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a>Последняя закрытая строка работы должна быть размещением

Код ошибки: WAX1285

## <a name="symptoms"></a>Симптомы

Система отобразит следующее сообщение об ошибке:

> Последняя закрытая строка работы должна быть размещением.

## <a name="cause"></a>Причина

Невозможно отменить работу в текущем состоянии.

В строке последней работы поле **Статус работы** задается как *Закрыто*, но поле **Тип работы** не задано как *Размещение*.

## <a name="resolution"></a>Приказ

Чтобы отменить работу, выполните следующие действия.

1. Перейдите **Управление складом \> Периодические задачи \> Очистка \> Отмена работы**.
1. В поле **Код работы** укажите код работы, которую необходимо отменить.
1. Нажмите **ОК**.
1. Выберите **Да** для подтверждения того, что вы хотите отменить работу.

Дополнительные сведения см. в разделе [Отмена работы склада для обработки исключений](../../warehousing/cancel-warehouse-work.md).
