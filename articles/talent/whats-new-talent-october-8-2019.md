---
title: Что нового и что изменилось в Dynamics 365 Talent (8 октября 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
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
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 159320dcbdf257862378b347172ef71832e293dc
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626070"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a>Что нового и что изменилось в Dynamics 365 Talent (8 октября 2019 г.)

[!include [banner](includes/banner.md)]

В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Изменения в Attract

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Изменения в Onboard

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Изменения в Core HR

Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2542. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a>Удаление открытой регистрации льгот из общедоступной предварительной версии

В сочетании с нашим объявлением в записи блога [Стратегические инвестиции в Core HR способствуют повышению производительности](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/) Корпорация Майкрософт удаляет функцию открытой регистрации льгот из общедоступной предварительной версии 18 октября 2019 года. Вместо этого в будущем будут выпущены новые функции. Производственное использование функции открытой регистрации льгот, которая в настоящее время находится в общедоступной предварительной версии, не будет поддерживаться. 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a>Интеграция Common Data Service теперь по умолчанию отключена для новых положений (343675)
 
При подготовке новых сред интеграция Common Data Service в данный момент отключена. Дополнительные сведения см. в разделе [Настройка интеграции Common Data Service](hr-common-data-service-integration.md).

### <a name="streamlined-employee-entry-and-navigation"></a>Упрощенный вход и навигация сотрудников

Функция для входа и навигации сотрудника доступна во всех средах. Чтобы включить эту функцию, перейдите к **Администрирование системы \> Ссылки\> Настройка \> Системные параметры \> Предварительные версии функций** и выберите **Расширенные форма и навигация по сотрудникам**. Затем эта функция включается для всех пользователей. Этот параметр можно отключить в любое время.

Дополнительные сведения см. в разделе [Упрощенный ввод данных сотрудника](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry) в Dynamics 365 волны 2 выпуска 2019 года.

### <a name="issue-attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a>Проблема: Attract и Onboard создают неактивных работников в Core HR (380517)

В выпуске этой недели исследуется проблема, в которой Attract и Onboard создают неактивных работников в Core HR.

### <a name="issue-the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a>Проблема: workflow-процесс завершается сбоем, когда менеджер входит в другую компанию при увольнении работника (346852)

Этот workflow-процесс больше не завершается сбоем в зависимости от юридического лица, в которое вошел менеджер.

### <a name="issue-missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a>Проблема: отсутствуют сведения о HcmOnboardingWorkerChecklistTaskEntity (349591)

Этот выпуск включает дополнительные сведения о **HcmOnboardingWorkerChecklistTaskEntity**. Далее приводятся некоторые примеры.

- **Имя группы**, если назначенный тип является **группой**
- **Имя сотрудника**, если назначенный тип является **сотрудником**
- **Имя менеджера**, если назначенный тип является **менеджером**

### <a name="issue-entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a>Проблема: объекты не перечисляются в алфавитном порядке в администрировании Common Data Service (377414)

Объекты теперь перечисляются в алфавитном порядке на странице **Администрирование CDS**.

### <a name="issue-changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a>Проблема: при изменении типа занятости с будущей датой не разрешается назначение должности (339958)

Это изменение позволяет назначать должности при изменении типов работников (например, с сотрудника на подрядчика).

### <a name="issue-updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a>Проблема: Обновление сущности банковской проводки отпуска в Common Data Service создает новую запись в Talent (352938)

Проводка отпуска теперь обновляется при обновлении Common Data Service для банковских проводок отпусков.

### <a name="issue-the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a>Проблема: в заголовке вложений для элементов обратной связи отображается описание обратной связи (343765)

Описание обратной связи больше не отображается в заголовке вложения.

### <a name="issue-compensation-workflow-comments-field-shows-incorrect-content-339297"></a>Проблема: в поле "Комментарии" workflow-процесса компенсации указано неверное содержание (339297)

Это изменение показывает содержимое поля **%HcmActionState.HcmWorkerActionComment.Comments%**.

### <a name="issue-workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a>Проблема: WorkCalendarEntity и WorkCalendarDayEntity не предоставляются через OData (376329)

В этом выпуске, **WorkCalendarEntity** и **WorkCalendarDayEntity** теперь доступны через протокол OData (Протокол открытых данных).

### <a name="issue-hcmworkerentity-is-slow-when-odata-is-used-375221"></a>Проблема: HCMWorkerEntity работает медленно при использовании OData (375221)

Изменения улучшают производительность **HCMWorkerEntity** при использовании конструктора книг Microsoft Excel.

### <a name="issue-manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a>Проблема: запись журнала производительности менеджера показывает ошибку после удаления журнала производительности и создания нового (336061)

В этом выпуске исправлена проблема, которая происходит после удаления одного журнала производительности и сразу после этого создается новый журнал. Это исправление изменяет поведение в портале самообслуживания менеджера.

## <a name="coming-soon"></a>Скоро

### <a name="print-performance-reviews"></a>Печать оценок производительности

См. раздел [Печать оценок производительности](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) в Dynamics 365 волны 2 выпуска 2019 года.
