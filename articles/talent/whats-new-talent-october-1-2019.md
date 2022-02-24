---
title: Что нового и что изменилось в Dynamics 365 Talent (1 октября 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 69c0a805027f215b2a2a42d826ee7a346cfdd511
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529668"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-1-2019"></a>Что нового и что изменилось в Dynamics 365 Talent (1 октября 2019 г.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой теме описываются новые и измененные компоненты Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Изменения в Attract

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Изменения в Onboard

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Изменения в Core HR

Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2509. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).

### <a name="streamlined-employee-entry-and-navigation"></a>Упрощенный вход и навигация сотрудников

Эта функция теперь доступна во всех средах. Чтобы включить эту функцию, выберите **Системный администратор > Ссылки > Настройка > Системные параметры > Предварительные версии функций**. Выберите **Расширенные форма и навигация по сотрудникам**. Это позволяет включить эти изменения для всех пользователей. Этот параметр можно отключить в любое время.

Дополнительные сведения см. в разделе [Упрощенный вход и навигация сотрудников](./streamlined-employee-entry.md). Чтобы посмотреть видео об этих изменениях, см. [обзор выпуска Dynamics 365 for Talent 2019 г., волна 2](https://aka.ms/ROGT19RW2ROV).

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>Предварительные версии функций можно включить в песочнице и в пробных средах

При подготовке нового экземпляра Talent можно указать, имеет ли данный экземпляр тип Производство или Песочница. Экземпляры типа Песочница позволяют заблаговременно попробовать новые возможности. Если необходимо обновить один из существующих экземпляров до типа экземпляра Песочница, обратитесь в службу поддержки, чтобы инициировать запрос на изменение.

Дополнительные сведения о порядке публикации изменений см. в разделе [Подготовка Talent](./provisioning-talent.md).

### <a name="compensation-date-defaults-to-a-different-date-than-the-position-assignment-337694"></a>Дата компенсаций по умолчанию устанавливается на дату, отличную от даты назначения на должность (337694)

С этим изменением дата начала компенсации по умолчанию устанавливается на дату начала назначения на должность.

### <a name="not-able-to-end-compensation-along-with-its-position-assignment-328993"></a>Не удается завершить компенсацию вместе с назначением на должность (328993)

С этим изменением можно завершить компенсацию при завершении назначения на должность с помощью команды **Окончить назначение** на странице **Назначения должности работника** с включенными действиями персонала.

### <a name="bank-account-validation-requires-routing-and-account-numbers-in-all-locations-340403"></a>Для проверки банковского счета требуется маршрутизация и номера счетов во всех местоположениях (340403)

С изменением на этой неделе был добавлен новый параметр конфигурации для отключения обязательной проверки параметров **Номер маршрутизации** и **Номер счета**. 

### <a name="attachments-are-not-enabled-in-mss-performance-journals-for-performance-feedback-341794"></a>В журналах производительности MSS не включены вложения для обратной связи по производительности (341794)

В выпуске этой недели вложения включены для элементов обратной связи на странице журнала производительности.

### <a name="leave-request-details-dont-sync-from-common-data-service-to-talent-369608"></a>Сведения запроса отпуска не синхронизируются из Common Data Service в Talent (369608)

В результате этих изменений сведения о запросе отпуска, который обновляется в Common Data Service, будут синхронизированы обратно с Talent.

### <a name="job-description-doesnt-display-for-the-job-in-the-skill-gap-analysis-page-369398"></a>Описание должности не отображается для должности на странице "Анализ несоответствия навыков" (369398)

В сборке этой недели описание будет отображено при выборе должности на странице **Анализ несоответствия навыков**.

## <a name="coming-soon"></a>Скоро

### <a name="print-performance-reviews"></a>Печать оценок производительности

Сотрудники, менеджеры и специалисты отдела кадров смогут распечатать обзор производительности сотрудников.
