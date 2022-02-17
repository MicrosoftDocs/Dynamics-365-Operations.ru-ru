---
title: Настройка параметров управления льготами для компании
description: В этой теме описывается, как настроить параметры управления льготами по компаниям в Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 8/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f6b3f068c9d3198afa8cd10aaa14bbc7ec9ef3c4
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065826"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Настройка параметров управления льготами для компаний


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Для каждой организации, предлагающей льготы, необходимо настроить параметры сообщений электронной почты с подтверждением льгот.

## <a name="configure-confirmation-email-settings"></a>Настройка параметров подтверждающих сообщений электронной почты

1. В рабочей области **Управление льготами** в **Настройка** выберите **Параметры Human Resources**.

2. На вкладке **Управление льготами** укажите значения для следующих полей: 

   | Поле | описание |
   | --- | --- |
   | **Отправить подтверждение по электронной почте** | Если эта функция включена, сотрудники будут получать подтверждающие сообщения по электронной почте, когда они выходят из интерфейса регистрации льгот в системе **Дистанционное обслуживание сотрудников**. |
   | **Шаблон подтверждения по электронной почте** | Выберите шаблона электронной почты организации, который будет использоваться при отправке подтверждения регистрации. Если шаблон не выбран, будет отправлено следующее общее сообщение электронной почты:<br><br>%EmployeeFirstName%,<br><br>Поздравляем! Вы успешно завершили регистрацию на льготы.<br><br>Спасибо,<br>Льготы <наименование компании/организации>. |
   | **Адрес электронной почты отправителя по умолчанию** | Адрес электронной почты, который будет использоваться при отправке сообщения электронной почты с подтверждением. |

3. Нажмите **Сохранить**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
