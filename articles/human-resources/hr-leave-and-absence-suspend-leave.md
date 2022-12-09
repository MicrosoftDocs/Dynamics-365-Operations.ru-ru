---
title: Приостановка отпуска
description: Можно приостановить отпуск сотрудника в Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SuspendLeave, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9c8262fb34175f6f9326d6be82c922b2170fc5a7
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805269"
---
# <a name="suspend-leave"></a>Приостановить отпуск

>[!Important]
>Функции, перечисленные в этой статье, в настоящее время доступны для клиентов в отдельной версии Dynamics 365 Human Resources. Некоторые или все функции будут доступны в составе будущего выпуска в инфраструктуре Finance после выпуска Finance 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Можно приостановить отпуск сотрудника, чтобы остановить обработку начислений отпусков для выбранных типов отпусков.

## <a name="suspend-leave-and-absence-for-an-employee"></a>Приостановка отпусков и отсутствия для сотрудника

1. В записи сотрудника выберите **Отпуск**.

2. Выберите **Приостановка отпуска**.

3. Выберите **Создать**.

4. В диалоговом окне **Приостановка начисления отпуска** выберите **Тип отпуска**, а также значения **Начальная дата** и **Конечная дата** для приостановки.

5. При необходимости можно добавить **Комментарий** к приостановке. 

Если начисления обрабатываются, когда отпуск сотрудника приостановлен, начисления не будут сделаны для приостановленных типов отпусков.

> [!NOTE]
> Запросы на отпуск приостанавливают запросы на отгулы, но запросы на отгулы не приостанавливают запросы на отпуска.

## <a name="see-also"></a>См. также

- [Обзор отпусков и отсутствия на работе](hr-leave-and-absence-overview.md)
- [Настройка типов отпусков и отсутствий](hr-leave-and-absence-types.md)
- [Начисление планов отпусков и отсутствий](hr-leave-and-absence-accrue.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
