---
title: Обзор MyLeaveRequests
description: Объект MyLeaveRequests в Microsoft Dynamics 365 Human Resources предоставляет список запросов отпусков в системе с областью действия (ограниченной) для запросов, доступных текущему пользователю, запрашивающему объект.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465518"
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