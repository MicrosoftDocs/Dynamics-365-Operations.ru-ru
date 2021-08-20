---
title: Отмена работы, выполняемой пользователем, невозможна
description: Отмена работы, выполняемой пользователем, невозможна
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
ms.openlocfilehash: 1d7b0140d0c2724234a549ca4dfb23109012654abe0e60fcea1f98e8f17c153a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748699"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a>Отмена работы, выполняемой пользователем, невозможна

Код ошибки: WAX708

## <a name="symptoms"></a>Симптомы

Система отобразит следующее сообщение об ошибке:

> Нельзя отменить работу, которая отведена пользователю.

## <a name="cause"></a>Причина

Работа заблокирована пользователем и не может быть отменена. Чтобы подтвердить это, откройте код работы, а затем откройте вкладку **Общее**. Если работа заблокирована, в поле **Статус работы** будет указано значение *Выполняется*, а в поле **Кем заблокировано** — код пользователя.

## <a name="resolution"></a>Приказ

Чтобы отменить работу, выполните следующие действия.

1. Перейдите **Управление складом \> Периодические задачи \> Очистка \> Отмена работы**.
1. В поле **Код работы** укажите код работы, которую необходимо отменить.
1. Нажмите **ОК**.
1. Выберите **Да** для подтверждения того, что вы хотите отменить работу.

Дополнительные сведения см. в разделе [Отмена работы склада для обработки исключений](../../warehousing/cancel-warehouse-work.md).
