---
title: Обработка жизненных событий
description: Во время жизненного цикла сотрудников в Microsoft Dynamics 365 Human Resources каждый сотрудник может столкнуться с различными изменениями жизненных событий.
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
ms.openlocfilehash: ef160af483f81b8c1e60a274029b77c3cd34f924
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324799"
---
# <a name="process-life-events"></a>Обработка жизненных событий

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Во время жизненного цикла сотрудников в Microsoft Dynamics 365 Human Resources каждый сотрудник может столкнуться с различными изменениями жизненных событий. Например, свадьба, изменение трудоустройства или изменение иждивенца/бенефициара. Для использования жизненных событий необходимо включить жизненные события на странице **параметров льгот**, настроить типы жизненных событий, а также настроить параметры жизненных событий для типов планов.

Прежде чем обрабатывать жизненные события, необходимо запустить открытую регистрацию как минимум один раз во время найма на работу. В США открытая регистрация обычно выполняется раз в год. За пределами США открытая регистрация может выполняться во время найма. Работнику не нужно выбирать план льгот для обработки жизненных событий, но они должны быть включены в открытую обработку регистрации. 

При наличии работников с жизненными событиями, которые выполняются на будущую дату, используйте обработку жизненных событий. Это событие будет обрабатывать все необработанные жизненные события, которые не были обработаны (такие как будущие жизненные события или добавленные жизненные события, которые не относятся к сотрудникам, например новая льгота). Жизненные события реального времени являются скрытыми.

Например, если сегодня 1 февраля, а 14 февраля для работника Joe Smith планируется изменить юридические лица, то при выполнении обработки жизненного события на 15 февраля система обрабатывает все события до 15 февраля. 

1. В рабочей области **Управление льготами** в **Обработка** выберите **Обработка жизненных событий**.

2. В диалоговом окне **Выполнение процесса жизненного события** укажите значения для следующих полей:

   | Поле | Описание |
   | --- | --- |
   | **Период регистрации** | Период регистрации, для которого необходимо обработать жизненные события. |
   | **Информация о компании** | Юридическое лицо, для которого необходимо обработать жизненные события. |
   | **Дата жизненного события** | Система обрабатывает все события в течение периода регистрации, которые выполняются до этой даты. |
   | **Рабочий** | Работник, для которого необходимо обработать жизненные события. Если оставить это поле пустым, жизненные события будут обработаны для всех работников. |

3. Если необходимо выполнить процесс в фоновом режиме, выберите **Выполнить в фоновом режиме** и выполните следующие действия:

   1. Введите сведения для процесса.

   2. Чтобы настроить повторяющееся задание, выберите **Повторение**, введите сведения о повторении, а затем нажмите **ОК**.

   3. Чтобы настроить оповещение о заданиях, выберите **Оповещения**, выберите получаемые оповещения и нажмите **ОК**.

   4. Нажмите **ОК**. Процесс будет выполнен с заданными вами параметрами.

4. Нажмите **ОК**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
