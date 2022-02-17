---
title: Параметры интеграции зарплаты
description: В этой теме описываются параметры интеграции заработной платы Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-17
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 37d4dc52e7fe5ddd95f43d98267db819a275bd92
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069865"
---
# <a name="payroll-integration-parameters"></a>Параметры интеграции зарплаты


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Перед использованием интеграции зарплаты Dynamics 365 Human Resources необходимо настроить параметры, описанные в этой теме.

## <a name="enable-payroll-address"></a>Включить адрес заработной платы

Чтобы иметь возможность использовать адрес зарплаты, необходимо включить его в [форме общих параметров](hr-setup-shared-parameters.md) на вкладке интеграции зарплаты.

## <a name="define-the-identification-type"></a>Определение типа идентификации

Чтобы предоставить код типа идентификации в [сущности зарплаты сотрудника](hr-admin-integration-payroll-api-payroll-employee.md), необходимо [настроить параметры управления персоналом](hr-setup-shared-parameters.md) для каждой компании.

1. В рабочей области **Управление компенсациями** по ссылкам выберите **Параметры Human Resources**. 
2. На вкладке **Интеграция зарплаты** укажите значение следующих полей.

| Поле | описание |
| --- | --- |
| Использование типов идентификации при обработке зарплаты | Когда выбран этот параметр, выбранный код типа будет показан в сущности зарплаты сотрудника. |
| Тип документа | Тип идентификации, который должен быть представлен в поле **mshr_payrollemployeeentityid** [сущности зарплаты сотрудника](hr-admin-integration-payroll-api-payroll-employee.md). |

## <a name="see-also"></a>См. также

[Введение API интеграции заработной платы](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
