---
title: Проекты по массовому набору сотрудников
description: Проекты по массовому набору сотрудников позволяют специалисту по найму создавать нескольких должностей и эффективно нанимать сотрудников на эти должности.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMMassHireProject, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3d0747232ba4682afe4b28dc7d24ad2413448bb
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052853"
---
# <a name="mass-hire-projects"></a>Проекты по массовому набору сотрудников

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Проекты по массовому набору сотрудников позволяют специалисту по найму создавать нескольких должностей и эффективно нанимать сотрудников на эти должности.

## <a name="overview"></a>Обзор

Используйте проекты массового набора сотрудников, когда одновременно нанимается много работников, например, при найме для удовлетворения сезонного спроса. Создание проекта массового набора сотрудников может быть полезным, так как оно позволяет одновременно создать записи должностей, записи работников и назначения работников. При создании должностей для проекта массового набора сотрудников можно указать следующие сведения.

- Число создаваемых должностей
- Тип работника для сотрудников, нанимаемых на должности
- Подразделение и должность, связанные с вакансиями
- Аналог должности при полной занятости

## <a name="example"></a>Пример

В течение лета вы обычно нанимаете на частичную занятость 15-20 студентов, чтобы заполнить свободные должности стажеров в вашей компании. В этом году вам необходимо нанять пять бухгалтеров, пять обработчиков заказов и пять кассиров. Вместо создания каждой из записей должностей и работников по отдельности вы создаете один проект по массовому набору сотрудников под названием "SummerInterns" (Стажеры – лето). Даты начала и конца проекта соответствуют датам начала и конца срока действия должностей, для которых создается проект по массовому набору сотрудников.

На странице **Проекты по массовому набору сотрудников** выберите проект "SummerInterns", и после этого щелкните **Открыть проект**. В открытом проекте массового набора сотрудников щелкните **Создание должностей** и введите сведения о должности бухгалтера. Можно указать, что требуется создать пять должностей бухгалтеров с теми же сведениями для каждой должности, и нажать кнопку "ОК". Повторите эту процедуру для должностей обработчиков заказов и кассиров.

После выбора студентов для найма на должности стажеров вы введете сведения о каждом из студентов в **Сведения по должностям** для должностей, по которым производится прием на работу. После того, как будут введены все сведения по должностям, выберите должность на странице "Проекты по массовому набору сотрудников" и нажмите кнопку **Прием на работу**. Для каждой из должностей будет создана запись должности, также для каждого из нанимаемых лиц будет создана и назначена соответствующей должности запись работника.

## <a name="mass-hire-project-statuses"></a>Статусы проектов по массовому набору сотрудников

Проект по массовому набору сотрудников может иметь один из следующих статусов.

- Создан
- Открытое
- Закрыт

На странице **Проект по массовому набору сотрудников** щелкните **Открыть проект** или **Закрыть проект** для того, чтобы изменить статус проекта по массовому набору сотрудников. В следующей таблице приводятся сведения о том, какие действия над проектом возможны в зависимости от его статуса.

<table>
<thead>
<tr>
<th>Состояние</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr>
<td>Создан</td>
<td>Можно создавать и изменять информацию, но нельзя создавать должности для проекта. Это статус по умолчанию для новых проектов.</td>
</tr>
<tr>
<td>Открытое</td>
<td>Можно изменять сведения о проекте, создавать должности для проекта по массовому набору сотрудников, и нанимать людей на должности. Этот статус имеют активные проекты.</td>
</tr>
<tr>
<td>Закрыт</td>
<td>Добавлять должности в проект невозможно. Для добавления должностей в проект по массовому набору сотрудников откройте проект повторно. Этот статус используется для завершенных проектов.
<blockquote>[!NOTE] Перед закрытием проекта по массовому набору сотрудников все должности в проекте должны иметь либо статус "Создано", либо статус "Закрыто".</blockquote>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]