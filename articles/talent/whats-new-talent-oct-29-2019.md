---
title: Что нового и что изменилось в Dynamics 365 Talent (29 октября 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e2d79ee9e182df4a4efe65beb685567b1e7446ce
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897450"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a>Что нового и что изменилось в Dynamics 365 Talent (29 октября 2019 г.)

В этой теме описываются новые и измененные компоненты Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Изменения в Attract

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Изменения в Onboard

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Изменения в Core HR

Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2586. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a>Удаление субъектов, не имеющих ролей, должно быть включено по умолчанию (371233)

При подготовке новой среды в Talent **Удалить субъекты, если роли не существуют** включено по умолчанию. При удалении работника связанный с ним субъект не удаляется, если этот параметр не включен. Это изменение ограничит повторяющиеся записи в глобальной адресной книге, когда требуется импортировать, изменить или повторно импортировать работников.

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a>Запросы на отпуск "Черновик" или "Отменено" должны удаляться в Common Data Service (376999)

Теперь это изменение позволяет удалять запросы на отпуск со статусом **Черновик** или **Отменено** в Common Data Service.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Дополнительные значения списка в настраиваемых полях не отображаются в Common Data Service после нажатия "Применить" в форме настраиваемых полей (379599)

При добавлении значений нового списка в существующее настраиваемое поле, которое уже было синхронизировано с Common Data Service, теперь они доступны в Common Data Serivce после применения изменений в форме **настраиваемых полей**.

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a>Применение контрольных списков адаптации для юридических лиц при наличии нескольких сотрудников (371270)

В выпуске этой недели можно применять контрольные списки к сотрудникам с более чем одной занятостью в **форме сотрудника > контрольные списки**.

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a>Удалена функция предварительного просмотра открытой регистрации льгот

В сочетании с нашим объявлением в записи блога [Стратегические инвестиции в Core HR способствуют повышению производительности](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) Корпорация Майкрософт удаляет функцию открытой регистрации льгот из общедоступной предварительной версии. В будущем будут выпущены новые функции. Использование функции регистрации открытых льгот не поддерживается.

## <a name="coming-soon"></a>Скоро

### <a name="print-performance-reviews"></a>Печать оценок производительности

См. раздел [Печать оценок производительности](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) в Dynamics 365 волны 2 выпуска 2019 года.

### <a name="feature-management-workspace"></a>Рабочая область управления функциями

Функции добавляются и обновляются в каждом выпуске. Опыт управления функциями предоставляет рабочую область, в которой можно просматривать список функций, которые были поставлены в каждом выпуске. По умолчанию новые функции отключены. Можно использовать рабочую область для их включения и просмотра документации по ним.

Для получения дополнительных сведений об изменениях, связанных с управлением функциями, см. раздел [Обзор управления функциями,](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
