---
title: Что нового и что изменилось в Dynamics 365 for Talent (27 августа 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8965636e539345be5ef0ad591f7017938efd322d
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529812"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a>Что нового и что изменилось в Dynamics 365 for Talent (27 августа 2019 г.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой теме описываются новые и измененные компоненты Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Изменения в Attract

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Изменения в Onboard

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Изменения в Core HR

Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2447. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Предварительные версии функций доступны только в экземплярах "песочницы"

При подготовке нового экземпляра Talent можно указать, имеет ли данный экземпляр тип Производство или Песочница. Экземпляры типа Песочница позволяют заблаговременно тестировать новые возможности. Все существующие экземпляры Talent будут обновлены до типа экземпляра Производство. Если необходимо обновить один из существующих экземпляров до типа экземпляра Песочница, обратитесь в службу поддержки, чтобы инициировать запрос на изменение.

Дополнительные сведения о порядке публикации изменений см. в разделе [Подготовка Talent](./provisioning-talent.md).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Просмотр расширенной информации о производительности на портале самообслуживания менеджера

Новый параметр позволит менеджерам просматривать производительность как своих прямых подчиненных, так и их расширенных подчиненных. В настоящее время линейные менеджеры могут назначать и обновлять цели производительности и выпускать новые обзоры. Кроме того, прямые менеджеры и их сотрудники могут вести поддержку и обновлять журналы производительности, чтобы обеспечить плавность процесса проверки производительности. Когда это изменение будет реализовано, менеджеры смогут просматривать и вести сведения о производительности для расширенных подчиненных в дополнение к их прямым подчиненным.

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a>Удаление юридических лиц не разрешено, если сотрудники существуют в компании (339849)

С этим изменением невозможно убрать или удалить компании, если для юридического лица существуют сотрудники и другие соответствующие данные.

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a>Аналитика бизнес-аналитики в модуле управления компенсациями не соответствуют рабочей области компенсации (322493)

В этом выпуске аналитика компенсаций корректируется таким образом, чтобы точно отражать планы, назначенные сотрудникам.

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a>Заполнитель рабочего процесса %company% отображает DAT при найме сотрудников через рабочий процесс (343905)

В этой версии местозаполнитель компании отображает юридическое лицо, связанное с занятостью нового сотрудника.

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a>Объект CDSJobPosition выводит сообщение об ошибке, когда устанавливается допустимое значение даты (349387)

В этом выпуске источники данных **Сведения о должности** и **Период должности** в объекте **CDSJobPosition** позволяют редактировать из Common Data Service в полях **Дата вступления в силу**. 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a>Для увольнения сотрудника последний отработанный день заполняется датой окончания назначения (332496)

Это изменение теперь по умолчанию задает для поля **Дата окончания назначения** значение **Дата окончания трудоустройства**. Можно изменить эти значения по умолчанию при вводе данных.

### <a name="legal-entities-arent-limited-with-hire-338871"></a>Юридические лица не ограничиваются при найме (338871)
 
Это изменение ограничивает процесс найма для отображения только тех юридических лиц, к которым пользователь имеет доступ.  

## <a name="in-preview"></a>В режиме предварительного просмотра

### <a name="streamlined-employee-entry-and-navigation"></a>Упрощенный вход и навигация сотрудников

Эта функция теперь доступна в изолированных и пробных средах. Чтобы включить эту функцию, выберите **Системный администратор > Ссылки > Настройка > Системные параметры > Предварительные версии функций**. Выберите **Расширенные форма и навигация по сотрудникам**. Это позволяет включить эти изменения для всех пользователей. Этот параметр можно отключить в любое время.

Дополнительные сведения см. в разделе [Упрощенный вход и навигация сотрудников](./streamlined-employee-entry.md).

## <a name="coming-soon"></a>Скоро

### <a name="platform-update-29"></a>Обновление платформы update 29

Дополнительные сведения об обновлении платформы Platform update 29 см. в разделе [Предварительные версии функций в Dynamics 365 for Finance and Operations Platform Update 29 (октябрь 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).


[!INCLUDE[footer-include](../includes/footer-banner.md)]