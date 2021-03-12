---
title: Настройка параметров управления льготами для компаний
description: Настройка параметров управления льготами для компаний в Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "4984608"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Настройка параметров управления льготами для компаний

Для каждой организации, предлагающей льготы, необходимо настроить параметры сообщений электронной почты с подтверждением льгот.

## <a name="configure-confirmation-email-settings"></a>Настройка параметров подтверждающих сообщений электронной почты

1. В рабочей области **Управление льготами** в **Настройка** выберите **Параметры Human Resources**.

2. На вкладке **Управление льготами** укажите значения для следующих полей: 

   | Поле | описание |
   | --- | --- |
   | **Отправить подтверждение по электронной почте** | Если эта функция включена, сотрудники будут получать подтверждающие сообщения по электронной почте, когда они выходят из интерфейса регистрации льгот в системе дистанционного обслуживания сотрудников. |
   | **Шаблон подтверждения по электронной почте** | Выберите шаблона электронной почты организации, который будет использоваться при отправке подтверждения регистрации. Если шаблон не выбран, будет отправлено следующее общее сообщение электронной почты:<br><br>%EmployeeFirstName%,<br><br>Поздравляем! Вы успешно завершили регистрацию на льготы.<br><br>Спасибо,<br>Льготы <наименование компании/организации>. |
   | **Адрес электронной почты отправителя по умолчанию** | Адрес электронной почты, который будет использоваться при отправке сообщения электронной почты с подтверждением. |

3. Нажмите **Сохранить**.