---
title: Обработка изменений ставок
description: Процесс изменения ставок льгот в Microsoft Dynamics 365 Human Resources, когда для нового или существующего плана льгот есть изменения параметров правил допустимости.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c841f5d5d409c7e73cdc38988f8233747a11f837
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803833"
---
# <a name="process-rate-changes"></a>Обработка изменений ставок

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Процесс изменения ставок льгот в Microsoft Dynamics 365 Human Resources, когда для нового или существующего плана льгот есть изменения параметров правил допустимости. Если новое правило допустимости создано и назначено плану, система рекомендует снова выполнить проверку допустимости для проверки того, имеют ли работники право на план на основе новых параметров допустимости. 

1. В рабочей области **Управление льготами** в **Обработка** выберите **Обработка обновления изменения ставки**.

2. В диалоговом окне **Выполнение обработки обновления изменения ставки** укажите значения для следующих полей:

   | Поле | Описание |
   | --- | --- |
   | **Период регистрации** | Период регистрации, для которого необходимо обработать изменения ставки. |

3. Если необходимо выполнить процесс в фоновом режиме, выберите **Выполнить в фоновом режиме** и выполните следующие действия:

   1. Введите сведения для процесса.

   2. Чтобы настроить повторяющееся задание, выберите **Повторение**, введите сведения о повторении, а затем нажмите **ОК**.

   3. Чтобы настроить оповещение о заданиях, выберите **Оповещения**, выберите получаемые оповещения и нажмите **ОК**.

   4. Нажмите **ОК**. Процесс будет выполнен с заданными вами параметрами.

4. Нажмите **ОК**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]