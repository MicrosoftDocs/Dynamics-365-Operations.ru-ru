---
title: Параметры интеграции зарплаты
description: В этой статье описываются параметры интеграции модуля "Заработная плата" Dynamics 365 Human Resources.
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
ms.openlocfilehash: 7d784909fc8c5fa05557566b62b19802cd2acece
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896115"
---
# <a name="payroll-integration-parameters"></a>Параметры интеграции зарплаты


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Перед использованием интеграции модуля "Заработная плата" Dynamics 365 Human Resources необходимо настроить параметры, описанные в этой статье.

## <a name="enable-payroll-address"></a>Включить адрес заработной платы

Чтобы иметь возможность использовать адрес зарплаты, необходимо включить его в [форме общих параметров](hr-setup-shared-parameters.md) на вкладке интеграции зарплаты.

## <a name="define-the-identification-type"></a>Определение типа идентификации

Чтобы предоставить идентификатор типа идентификации в [сущности "Сотрудник с заработной платой"](hr-admin-integration-payroll-api-payroll-employee.md), необходимо [настроить параметры управления персоналом](hr-setup-shared-parameters.md) для каждой компании.

1. В рабочей области **Управление компенсациями** по ссылкам выберите **Параметры Human Resources**. 
2. На вкладке **Интеграция зарплаты** укажите значение следующих полей.

| Поле | описание |
| --- | --- |
| Использование типов идентификации при обработке зарплаты | Когда выбран этот параметр, выбранный идентификатор типа будет показан в сущности "Сотрудник с заработной платой". |
| Тип документа | Тип идентификации, который должен быть представлен в поле **mshr_payrollemployeeentityid** [сущности "Сотрудник с заработной платой"](hr-admin-integration-payroll-api-payroll-employee.md). |

## <a name="see-also"></a>См. также

[Введение API интеграции заработной платы](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
