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
ms.openlocfilehash: bbc5797df2b7465b36ec5ea546a67441626daeb1c72f82dfca4eb7db3503b713
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760282"
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
