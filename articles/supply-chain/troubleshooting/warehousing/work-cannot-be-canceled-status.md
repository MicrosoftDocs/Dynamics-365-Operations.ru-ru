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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924263"
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
