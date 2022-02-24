---
title: Что нового и что изменилось в Dynamics 365 Talent (31 января 2019 г.)
description: В этой теме описываются новые или измененные компоненты Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8e8c11e460a4678efea81f8d3d1eec96b673d329
ms.sourcegitcommit: 53174ed4e7cc4e1ba07cdfc39207e7296ef87c1f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/07/2020
ms.locfileid: "4690060"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a>Что нового и что изменилось в Dynamics 365 Talent (31 января 2019 г.)

В этой теме описываются новые и измененные компоненты Dynamics 365 Talent.

**Сборка 8.1.2128**

## <a name="core-hr-changes"></a>Изменения Core HR

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>Отгул, взятый на карточке отпусков людей, не учитывает даты плана отпусков
Для планов отпусков, которые не выполняются в календарный год, карточка **Взято** теперь отображает отгулы, взятые в год, определенный планом отпусков. Например, если год отпусков в организации начинается 1 июня и заканчивается 30 мая, а сотрудник взял три дня отгулов в декабре, на карточке **Взято** 15 января будет отображаться 3 дня. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Суммы начисления не совпадают с базисом даты уровня
Были добавлены новые параметры для отпуска и отсутствия (параметры **Управление персоналом**), чтобы клиенты могли определять, когда вступают в силу месяцы даты службы сотрудников. Для некоторых организаций эта дата является концом месяца, но для других это может быть начало следующего месяца. Например, одна организация может начислять отпускное время 31 декабря, в то время как другая может начислять отпускное время 1 января. Этот параметр позволяет выбрать, когда должно производиться начисление. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Действия приема на работу застопориваются в состоянии "Workflow-процесс завершен"
Были внесены изменения для устранения проблемы, когда небольшое количество workflow-процессов завершалось с состоянием "Workflow-процесс завершен". Новые workflow-процессы теперь должны переходить в состояние "Завершено" при завершении workflow-процесса. Любые workflow-процессы в состоянии "Workflow-процесс завершен" будут переведены в состояние ошибки для обновления или удаления по мере необходимости. 
