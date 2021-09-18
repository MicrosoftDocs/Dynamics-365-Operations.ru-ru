---
title: Ошибка при повторной отправке заказа на покупку в бизнес-правило после изменения
description: Ошибка при повторной отправке заказа на покупку в бизнес-правило после изменения
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4b8465d198c440f27a4b3cc4268445e0aa450f5b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477463"
---
# <a name="error-on-resubmitting-a-purchase-order-to-a-workflow-after-a-change"></a>Ошибка при повторной отправке заказа на покупку в бизнес-правило после изменения


## <a name="symptoms"></a>Симптомы

При повторной отправке заказа на покупку после изменения в рабочий процесс возникает следующая ошибка:

> Остановлено (ошибка): исключение X++: изменения заказа на покупку PO0000569 разрешены только в состоянии "Черновик", когда управление изменениями активируется в<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

Эта проблема возникает только в том случае, если заказ на покупку был в состоянии *Подтверждено* до того, как были запрошены изменения. Если вы запрашиваете изменения, когда заказ на покупку находится в *утвержденном* состоянии, рабочий процесс может быть обработан успешно.

## <a name="resolution"></a>Решение

Эта проблема может возникнуть из-за несогласованности в распределениях заказов на покупку.

Чтобы разблокировать эту проблему и сбросить заказ на покупку в состояние *Черновик*, перейдите в раздел **Закупки и источники \> Периодические задачи \> Очистка \> Сброс распределения заказов на покупку**. Дополнительные сведения см. в следующей записи блога: [Устранение ошибок распределения заказов на покупку в Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Эта проблема будет исправлена в [этой статье базы знаний (KB) Майкрософт](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).
