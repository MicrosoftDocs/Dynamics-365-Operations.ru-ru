---
title: Обзор MyLeaveRequests
description: Объект MyLeaveRequests в Microsoft Dynamics 365 Human Resources предоставляет список запросов отпусков в системе с областью действия (ограниченной) для запросов, доступных текущему пользователю, запрашивающему объект.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 90698ddcc8fcf0eb975dffed0bdad11e6b277c90
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984704"
---
# <a name="myleaverequests-overview"></a>Обзор MyLeaveRequests

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]