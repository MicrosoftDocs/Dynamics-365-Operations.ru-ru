---
title: Что нового и что изменилось в Dynamics 365 Talent (5 ноября 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
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
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 48de07178acfaccf11e0a02b2848bf24e6ccc117
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896781"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a>Что нового и что изменилось в Dynamics 365 Talent (5 ноября 2019 г.)

В этой теме описываются новые и измененные компоненты Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Изменения в Attract

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Изменения в Onboard

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Изменения в Core HR

Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2598. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).

### <a name="copy-a-core-hr-instance"></a>Копирование экземпляра Core HR

В выпуске этой недели можно использовать Microsoft Dynamics Lifecycle Services (LCS) для копирования базы данных Microsoft Dynamics 365 Talent: Core HR в среду в песочнице. При наличии другой среды-песочницы можно также скопировать базу данных из этой среды в целевую среду-песочницу. Дополнительные сведения см.

- [Расширенное управление средой](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) в Dynamics 365: 2019, план волны выпуска 2

- [Копирование экземпляра Core HR](hr-copy-instance.md) в документацию Talent

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a>Пакетные задания интеграции Common Data Service не создаются, когда включена интеграция Common Data Service (388030)

Это изменение создает пакетные задания для интеграции Common Data Service, когда она активирована.

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a>HcmPersonImageEntity не изменяет размер изображения сотрудника при отправке (369469)

В выпуске этой недели изменены способы изменения размеров изображений для повышения производительности при импорте через управление данными.

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a>Дата, доступная для данной должности, может предшествовать дате активации (340103)

В этом изменении появляется предупреждение, если выбрана **Дата, доступная для данной должности**, которая раньше **Дата активации** для должности.

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a>Невозможно создать запрос на изменение компенсации в дистанционном обслуживании сотрудников для пошаговых планов (376872)

В этом выпуске исправлена проблема с запросом изменений компенсации через дистанционное обслуживание сотрудников для пошаговых планов. 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a>Код причины не синхронизируется с Common Data Service, если описание длиннее 30 символов, Core HR допускают 60 (352682)

При этом изменении коды причин размером более 30 символов будут обновлены в Common Data Service. Изменения, сделанные в Common Data Service, также будут отражены в Talent.

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a>Интеграция адреса из Talent в Finance and Operations (351961)

В этом выпуске исправлена проблема, когда адреса, обновляемые в Talent, не обновлялись в Finance and Operations. Изменения в блоках адресов будут обновлены.

## <a name="coming-soon"></a>Скоро

### <a name="print-performance-reviews"></a>Печать оценок производительности

См. раздел [Печать оценок производительности](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) в Dynamics 365 волны 2 выпуска 2019 года.

### <a name="feature-management-workspace"></a>Рабочая область управления функциями

Функции добавляются и обновляются в каждом выпуске. Опыт управления функциями предоставляет рабочую область, в которой можно просматривать список функций, которые были поставлены в каждом выпуске. По умолчанию новые функции отключены. Можно использовать рабочую область для их включения и просмотра документации по ним.

Для получения дополнительных сведений об изменениях, связанных с управлением функциями, см. раздел [Обзор управления функциями,](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
