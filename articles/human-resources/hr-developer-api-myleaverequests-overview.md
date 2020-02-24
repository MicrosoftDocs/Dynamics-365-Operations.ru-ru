---
title: Обзор MyLeaveRequests
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010331"
---
# <a name="myleaverequests-overview"></a>Обзор MyLeaveRequests

Объект MyLeaveRequests в Microsoft Dynamics 365 Human Resources предоставляет список запросов отпусков в системе с областью действия (ограниченной) для запросов, доступных текущему пользователю, запрашивающему объект.

## <a name="key"></a>Ключ

  | Имя свойства | Тип данных |
  |---------------|-----------|
  | dataAreaId    | Строка    |
  | RequestId     | Строка    |
  | LeaveType     | Строка    |
  | LeaveDate     | Дата      |
  
## <a name="properties"></a>Свойства

  | Имя свойства     | Тип данных | Обязательный |
  |-------------------|-----------|----------|
  | dataAreaId        | Строка    | Х        |
  | RequestId         | Строка    | Х        |
  | LeaveType         | Строка    | Х        |
  | LeaveDate         | Дата      | Х        |
  | ReasonCodeId      | Строка    |          |
  | PersonnelNumber   | Строка    | Х        |
  | RequestDate       | Дата      | Х        |
  | Комментарий           | Строка    |          |
  | Состояние            | Перечислимый тип      | Х        |
  | Сумма, руб.            | Действующий      |          |
  | HalfDayDefinition | Перечислимый тип      |          |

## <a name="actions"></a>Действия

 | Имя действия                               | Описание                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [submit](hr-developer-api-myleaverequests-submit.md)   | Отправка запроса, который должен обрабатываться workflow-процессом. |

## <a name="see-also"></a>См. также

- [Отправка запроса на отпуск в workflow-процесс](hr-developer-api-myleaverequests-submit.md)
- [Проверка подлинности](hr-developer-api-authentication.md)