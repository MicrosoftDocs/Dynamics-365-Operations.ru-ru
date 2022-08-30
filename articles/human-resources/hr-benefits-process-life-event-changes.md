---
title: Обработка изменений событий в жизни
description: В этой статье объясняется, как обрабатывать изменения в жизненных событиях в Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f3d8fbe0270606688944b4465cb5846b8c8f9900
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323516"
---
# <a name="process-life-event-changes"></a>Обработка изменений событий в жизни

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
