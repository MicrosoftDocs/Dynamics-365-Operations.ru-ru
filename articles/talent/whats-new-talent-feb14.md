---
title: Что нового и что изменилось в Dynamics 365 for Talent (14 февраля 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
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
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1db7d032eade3f996e0554e64d6ea0704a347ed8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518906"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a>Что нового и что изменилось в Dynamics 365 for Talent (14 февраля 2019 г.)

[!include [banner](includes/banner.md)]

В этой теме описываются новые и измененные компоненты в Talent.

## <a name="changes-in-attract"></a>Изменения в Attract
Исправления незначительных ошибок включены в этот выпуск.

## <a name="changes-in-onboarding"></a>Изменения в Onboarding
Исправления незначительных ошибок включены в этот выпуск.
 
## <a name="changes-in-core-hr"></a>Изменения в Core HR 
**Сборка 8.1.2146**

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a>Сущность фиксированной компенсации сотруднику не экспортирует все записи
После этого изменения сущность **Фиксированная компенсация сотрудникам** сейчас будет экспортировать все записи. Сущность может использоваться для создания и обновления существующих записей о фиксированной компенсации для сотрудников. 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a>Дата окончания занятости не учитывает заданные параметры предпочтительного часового пояса сотрудника
Даты окончания занятости сейчас учитывают предпочитаемый пользователем часовой пояс при создании или окончания занятости с компанией.
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a>Адреса из Великобритании в Analytics отображаются как адреса из восточной Швейцарии
В этом выпуске внесено изменение для исправления рассогласования адресов в отчете "Численность сотрудников по местоположению" в области **Управление персоналом**.
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a>Код увольнения не заполняется для записи назначения должности работника при завершении должности
Изменение внесено в код по умолчанию "Причина увольнения" при окончании назначения сотрудникам должности.

### <a name="new-entity-created-for-job-compensation-levels"></a>Создана новая сущность для уровней компенсации вакансии
Создана новая сущность платформы управления данными (DMF). Сущность позволяет создавать и обновлять уровни компенсации, значения рынка и обзорные сведения для каждой вакансии, которая определена в системе.
