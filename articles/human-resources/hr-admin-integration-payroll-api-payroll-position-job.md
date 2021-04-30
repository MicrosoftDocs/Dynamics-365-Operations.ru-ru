---
title: Задание позиции зарплаты
description: В этом разделе представлены сведения и пример запроса для сущности задания позиции заработной платы в Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 72f3109f5bea36a390b04b7165fc3831d777b640
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882064"
---
# <a name="payroll-position-job"></a>Задание позиции зарплаты

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе представлены сведения и пример запроса для сущности связи задания позиции заработной платы в Dynamics 365 Human Resources.

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код задания**<br>mshr_jobid<br>*Строка* | Только чтение<br>Требуется |ИД задания. |
| **Действительно с**<br>mshr_validto<br>*Смещение даты и времени* | Только для чтения <br>Требуется | Дата, начиная с которой действует связь задания. |
| **Действительно до**<br>mshr_validto<br>*Смещение даты и времени* | Только для чтения <br>Требуется | Дата, до которой действует связь задания и должности.  |
| **Код должности**<br>mshr_positionid<br>*Строка* | Только для чтения<br>Требуется | Код должности. |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Требуется<br>Создано системой |  |
| **Значение идентификатора задания должности**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity |ИД задания, связанный с должностью.|
| **Значение идентификатора План фиксированной компенсации**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity  | ИД плана фиксированной компенсации, связанный с должностью. |
| **ИД сущности задания позиции заработной платы**<br>mshr_payrollpositionjobentityid<br>*Guid* | Требуется<br>Создано системой. | Создаваемое системой значение GUID для уникальной идентификации задания.  |

