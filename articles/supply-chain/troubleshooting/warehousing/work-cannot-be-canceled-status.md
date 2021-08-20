---
title: Работа не может быть из-за ее статуса
description: Работа не может быть из-за ее статуса
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
ms.openlocfilehash: f983501b490c5516525b4d5904603ed62e8799f9e6124e5672b36a12804ecb0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755986"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a>Работа не может быть из-за ее статуса

Код ошибки: WAX2190

## <a name="symptoms"></a>Симптомы

Система отобразит следующее сообщение об ошибке:

> Невозможно отменить работу %1, так как она имеет статус %2.

## <a name="cause"></a>Причина

Невозможно отменить работу в текущем состоянии.

У заголовка работы или строк работы нет ожидаемого значения **Статус работы**. В поле **Статус работы** в заголовке работы нет значения *Открыто* или *Выполняется*.

## <a name="resolution"></a>Приказ

Чтобы отменить работу, выполните следующие действия.

1. Перейдите **Управление складом \> Периодические задачи \> Очистка \> Отмена работы**.
1. В поле **Код работы** укажите код работы, которую необходимо отменить.
1. Нажмите **ОК**.
1. Выберите **Да** для подтверждения того, что вы хотите отменить работу.

Дополнительные сведения см. в разделе [Отмена работы склада для обработки исключений](../../warehousing/cancel-warehouse-work.md).
