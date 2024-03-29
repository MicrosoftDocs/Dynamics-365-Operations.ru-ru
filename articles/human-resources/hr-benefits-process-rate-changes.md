---
title: Обработка изменений рейтинга
description: В этой статье объясняется, как обрабатывать изменения в ставках льгот в Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a60753db77511e60cce7153c0723778d01bbd4fe
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324679"
---
# <a name="process-rate-changes"></a>Обработка изменений рейтинга

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье объясняется, как обрабатывать изменения в ставках льгот в Microsoft Dynamics 365 Human Resources, когда в новом или существующем плане льгот изменились параметры правил приемлемости. Если новое правило допустимости создано и назначено плану, система рекомендует снова выполнить проверку допустимости для проверки того, имеют ли работники право на план на основе новых параметров допустимости. 

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
