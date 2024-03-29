---
title: Проекты по массовому набору сотрудников
description: В этой статье описываются проекты по массовому набору сотрудников, которые позволяют специалистам по найму создавать несколько позиций и эффективно нанимать сотрудников на эти позиции.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMMassHireProject, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2abf6ed80b7c5f728d7ff922afab8b425bde3df7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904198"
---
# <a name="mass-hire-projects"></a>Проекты по массовому набору сотрудников


[!INCLUDE [PEAP](../includes/peap-1.md)]

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

На странице **Проекты по массовому набору сотрудников** выберите проект **SummerInterns**, и затем выберите **Открыть проект**. В открытом проекте массового набора сотрудников выберите **Создание должностей** и введите сведения о должности бухгалтера. Можно указать, что требуется создать пять должностей бухгалтеров, и что одни и те же сведения должны использоваться для каждой должности. Затем выберите **OK**. Повторите эту процедуру для должностей обработчиков заказов и кассиров.

После выбора студентов для найма на должности стажеров вы введете сведения о каждом из студентов в сведения по должностям для должностей, по которым производится прием на работу. После того, как будут введены все сведения по должностям, выберите должность на странице **Проекты по массовому набору сотрудников** и нажмите кнопку **Прием на работу**. Для каждой из должностей будет создана запись должности, также для каждого из нанимаемых лиц будет создана и назначена соответствующей должности запись работника.

## <a name="mass-hire-project-statuses"></a>Статусы проектов по массовому набору сотрудников

Проект по массовому набору сотрудников может иметь один из следующих статусов.

- Создано
- Открыть
- Закрыто

На странице **Проект по массовому набору сотрудников** выберите **Открыть проект** или **Закрыть проект** для того, чтобы изменить статус проекта по массовому набору сотрудников. В следующей таблице приводятся сведения о том, какие действия над проектом возможны в зависимости от его статуса.

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
<td><p>Добавлять должности в проект невозможно. Для добавления должностей в проект по массовому набору сотрудников откройте проект повторно. Этот статус используется для завершенных проектов.</p>
<p><strong>Примечание.</strong> Перед закрытием проекта по массовому набору сотрудников все должности в проекте должны иметь либо статус <b>Создано</b>, либо статус <b>Закрыто</b>.</p>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
