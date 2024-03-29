---
title: Настройка гибких программ кредитования
description: Можно использовать программы гибкого кредитования в Microsoft Dynamics 365 Human Resources для регистрации сотрудников в льготах в соответствии с предварительно определенным количеством кредитов по гибкому графику.
author: twheeloc
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitCreditPrograms, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ff3bd2c4d39a4411b5a5cb82e4281ff4af98ff0d
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336945"
---
# <a name="set-up-flex-credit-programs"></a>Настройка гибких программ кредитования

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Можно использовать программы гибкого кредитования в Microsoft Dynamics 365 Human Resources для регистрации сотрудников в льготах в соответствии с предварительно определенным количеством кредитов по гибкому графику. Сотрудники могут выбрать способ распределения гибких кредитов. Например, если на сотрудника распространяется страховой план здравоохранения супруги, он может использовать кредиты, которые в противном случае использовались бы на покрытие здравоохранения, для других льгот. 

1. В рабочей области **Управления льготами** в **Планы** выберите **Гибкие программы кредитования**.

2. Выберите **Создать**.

3. Укажите значения для следующих полей:

   | Поле | Описание |
   | --- | --- |
   | **Код кредита льготы** | Уникальный код гибкой кредитной программы. |
   | **Описание** | Описание программы гибкого кредитования. | 
   | **С даты** | Дата, в которую программа гибкого кредитования становится активной. |
   | **До даты** | Дата, в которую программа гибкого кредитования закрывается. Можно оставить значение по умолчанию (12/31/2154), чтобы указать на то, что программа гибкого кредитования не имеет запланированного окончания срока действия. |
   | **Итоговое значение по кредиту** | Число кредитов, которое потребуется использовать сотруднику для получения льгот. |
   | **Правило пропорции** | Правило использования для пропорции гибких кредитов, когда сотрудник принимается на работу в середине гибкого кредитного периода. </br></br><ul><li>**Нет** — сотрудник не получает кредитов по гибкому графику работы, если он принят на работу после начала периода действия кредитной программы по гибкому графику работы.</li><li>**Полный кредит** — сотрудник получает полную сумму кредитов по гибкому графику, независимо от того, когда он принят на работу.</li><li>**Пропорция** — сотрудник получает пропорциональную сумму кредитов по гибкому графику на основе даты их начала.</li></ul> |
   | **Формула расчета пропорции гибкого кредита** | Правило использования для пропорции гибких кредитов, когда сотрудник принимается на работу в середине периода льгот для программы гибкого кредитного периода. Пропорция базируется на дате начала трудоустройства. Это поле используется только если выбрано значение **Пропорция** в поле **Правило пропорции**. </br></br><ul><li>**Ежедневно** — пропорция количества кредитов по гибкому графику, который сотрудник получает на уровне дня. Общее число гибких кредитов делится на число дней в периоде. Например, если период льготы составляет 400 дней, система разделяет общее число кредитов по гибкому графику на 400 для расчета количества кредитов, полученных сотрудниками по гибкому графику работы в день.</li><li>**Текущий месяц** — пропорциональное количество кредитов по гибкому графику, которые сотрудник получает на уровне месяца, округляется до текущего месяца. Общее число гибких кредитов делится на число месяцев в периоде. Например, если период льготы составляет 15 месяцев, система разделяет общее число кредитов по гибкому графику на 15 для расчета количества кредитов, полученных сотрудниками по гибкому графику работы в месяц.</li><li>**Следующий месяц** — пропорциональное количество кредитов по гибкому графику, которые сотрудник получает на уровне месяца, округляется до следующего месяца. Общее число гибких кредитов делится на число месяцев в периоде. Например, если период льготы составляет 15 месяцев, система разделяет общее число кредитов по гибкому графику на 15 для расчета количества кредитов, полученных сотрудниками по гибкому графику работы в месяц.</li></ul> |
   


[!INCLUDE[footer-include](../includes/footer-banner.md)]
