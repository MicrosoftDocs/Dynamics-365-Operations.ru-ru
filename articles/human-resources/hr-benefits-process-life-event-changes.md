---
title: Обработка изменений в жизни
description: Обработка изменений жизненных событий в Microsoft Dynamics 365 Human Resources для изменений жизненных событий.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6bc8f02b32d7c66d045015d07b8cb1f1e958d8b13b1c9b5a6d7aa5bda300da89
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750252"
---
# <a name="process-life-event-changes"></a>Обработка изменений в жизни

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Обработка изменений жизненных событий в Microsoft Dynamics 365 Human Resources для двух изменений жизненных событий:

- Изменения дней рождения
- Изменения окончания срока действия переопределения правила допустимости 

1. В рабочей области **Управление льготами** в **Обработка** выберите **Обработка изменений жизненных событий**.

2. В диалоговом окне **Выполнение процесса изменения жизненного события** укажите значения для следующих полей:

   | Поле | Описание |
   | --- | --- |
   | Период регистрации | Период регистрации, для которого необходимо обработать изменения жизненного события. |
   | Информация о компании | Юридическое лицо, для которого необходимо обработать изменения жизненного события. |

3. Если необходимо выполнить процесс в фоновом режиме, выберите **Выполнить в фоновом режиме** и выполните следующие действия:

   1. Введите сведения для процесса.

   2. Чтобы настроить повторяющееся задание, выберите **Повторение**, введите сведения о повторении, а затем нажмите **ОК**.

   3. Чтобы настроить оповещение о заданиях, выберите **Оповещения**, выберите получаемые оповещения и нажмите **ОК**.

   4. Нажмите **ОК**. Процесс будет выполнен с заданными вами параметрами.

4. Нажмите **ОК**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]