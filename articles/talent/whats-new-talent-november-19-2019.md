---
title: Что нового и что изменилось в Dynamics 365 Talent (19 ноября 2019 г.)
description: В этой статье описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/19/2019
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
ms.search.validFrom: 2019-11-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6a26c0039b145f4b6a0940a60256ba7b6644a829
ms.sourcegitcommit: b95df4cea27d6a8f797e0bdd18952bec7dece4ad
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/22/2019
ms.locfileid: "2825010"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-19-2019"></a>Что нового и что изменилось в Dynamics 365 Talent (19 ноября 2019 г.)

[!include [banner](includes/banner.md)]

В этой статье описываются новые и измененные компоненты в Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Изменения в Attract

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Изменения в Onboard

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Изменения в Core HR

Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2621. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-31-for-finance-and-operations-apps"></a>Обновление платформы 31 для приложений Finance and Operations

Дополнительные сведения см. в разделе [Предварительные версии функций обновления платформы 31 для приложений Finance and Operations (январь 2020 г.)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31).

### <a name="feature-management-workspace-383856"></a>Рабочая область управления функциями (383856)

Рабочая область **Управление функциями** содержит список функций, предоставляемых в каждом выпуске. По умолчанию новые функции отключены. Можно использовать рабочую область для их включения и просмотра документации по ним. Дополнительные сведения об управлении функциями см. в разделе [Обзор управления функциями](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Все новые возможности остаются в виде предварительного просмотра по крайней мере на 30 дней, а обычно 30-60 дней. Основные функции обычно доступны в октябре и апрель каждого года, следующего за периодом предварительного просмотра. После отображения новых возможностей в рабочей области **Управление функциями** их можно включить. Некоторые функции могут быть включены по умолчанию.
 
Время от времени неотъемлемая функция будет включена по умолчанию и не может быть отключена (например, в рабочей области **Управление функциями**).
 
Когда функция обычно доступна, она может быть включена или выключена в производственных средах. Рабочая область **Управление функциями** показывает, что функция предварительного просмотра станет обязательной. Эта дата обычно приходится на 1 октября или 1 апреля, чтобы соответствовать полугодовым плановым выпускам. Вы не можете отключить обязательные функции. До тех пор, пока она не станет обязательной, можно включать и выключать функцию во всех средах.

### <a name="message-appears-when-canceled-action-exists-for-a-position-382887"></a>Сообщение появляется, когда для должности существует отмененное действие (382887)

Следующее сообщение больше не появляется при выборе определенной должности, и отмененное действие — все, что доступно для данной должности: **выполняется незавершенное действие для должности xxxxxx**.

### <a name="in-learning-analytics-the-course-type-and-status-display-incorrect-data-381151"></a>В аналитической службе тип "Курс" и статус отображают неверные данные (381151)

В выпуске этой недели обновлены аналитики обучения, чтобы отображать **Тип "Курс"** и **Статус**.

### <a name="personnel-number-should-display-in-the-new-worker-form-banner-383832"></a>Табельный номер должен отображаться в баннере формы нового сотрудника (383832)

В форме **Новый сотрудник** **Табельный номер** теперь отображается в баннере для быстрой ссылки.

### <a name="position-start-date-determines-the-job-record-to-use-when-retrieving-a-compensation-level-during-hire-350361"></a>Дата начала должности определяет запись задания, которая будет использоваться при получении уровня компенсации во время найма (350361)

В этом выпуске **Дата начала компенсации** определяет уровень, назначенный новому заданию.

### <a name="custom-pick-list-fields-in-the-position-table-arent-synchronized-to-common-data-service-387503"></a>Настраиваемые поля листа комплектации в таблице должностей не синхронизованы с Common Data Service (387503)

В этом выпуске элементы листа комплектации синхронизируются с Common Data Service.

### <a name="worker-address-entity-doesnt-synchronize-with-common-data-service-while-importing-new-data-349673"></a>Объект адреса работника не синхронизируется с Common Data Service при импорте новых данных (349673)

В выпуске этой недели данные адреса синхронизируются с Common Data Service при импорте новых данных.

## <a name="in-preview"></a>В режиме предварительного просмотра

### <a name="print-performance-reviews"></a>Печать оценок производительности

См. раздел [Печать оценок производительности](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) в Dynamics 365 волны 2 выпуска 2019 года.
