---
title: Что нового и что изменилось в Dynamics 365 Talent (10 декабря 2019 г.)
description: В этой статье описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 12/10/2019
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
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 18f86f5d87b780d5d4ffc83330d389077987dda6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528179"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-10-2019"></a>Что нового и что изменилось в Dynamics 365 Talent (10 декабря 2019 г.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой теме описываются новые и измененные компоненты Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Изменения в Attract

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Изменения в Onboard

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Изменения в Core HR

Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2660. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Рабочая область управления функциями

Рабочая область **Управление функциями** содержит список функций, предоставляемых в каждом выпуске. По умолчанию новые функции отключены. Можно использовать рабочую область для их включения и просмотра документации по ним. Дополнительные сведения об управлении функциями см. в разделе [Обзор управления функциями](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Все новые возможности остаются в виде предварительного просмотра по крайней мере на 30 дней, а обычно 30-60 дней. Основные функции обычно доступны в октябре и апрель каждого года, следующего за периодом предварительного просмотра. После отображения новых возможностей в рабочей области **Управление функциями** их можно включить. Некоторые функции могут быть включены по умолчанию.
 
Время от времени неотъемлемая функция будет включена по умолчанию и не может быть отключена (например, в рабочей области **Управление функциями**).
 
Когда функция обычно доступна, она может быть включена или выключена в производственных средах. Рабочая область **Управление функциями** показывает, что функция предварительного просмотра станет обязательной. Эта дата обычно приходится на 1 октября или 1 апреля, чтобы соответствовать полугодовым плановым выпускам. Вы не можете отключить обязательные функции. До тех пор, пока она не станет обязательной, можно включать и выключать функцию во всех средах.

### <a name="streamlined-worker-form-has-moved-to-the-feature-management-workspace-390583"></a>Оптимизированная форма работника перенесена в рабочее пространство управления функциями (390583)

При этом изменении оптимизированная форма рабочего теперь может быть включена в рабочей области **управления функциями**. Эта функция была перемещена из формы **Системные параметры** в **Администрирование системы**.

### <a name="prevent-hcmworkerpayrollinfo-records-from-being-written-without-a-worker-value-394526"></a>Предотвращение записей HcmWorkerPayrollInfo от записи без значения работника (394526)

С этим выпуском записи **HcmWorkerPayrollInfo** больше не создаются без ссылки на сотрудников в этом сценарии. 

### <a name="message-log-associated-to-the-action-isnt-populated-when-the-action-fails-to-complete-374007"></a>Журнал сообщений, связанный с действием, не заполняется, когда выполнение действия не удалось (374007)

Этот выпуск включает в себя изменение заполнения журнала сообщений по действиям, когда действие завершается неудачей в определенных сценариях. 

### <a name="common-data-service-integration-batch-job-creation-388030"></a>Создание пакетного задания интеграции Common Data Service (388030)

С этим изменением пакетные задания для интеграции Common Data Service создаются при включении службы.

### <a name="additional-pick-list-values-to-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Дополнительные значения списка комплектации в настраиваемых полях не отображаются в Common Data Service после нажатия "Применить" в форме настраиваемых полей (379599)

С этим изменением новые значения списка комплектации, введенные в Talent, теперь синхронизируются с Common Data Service при применении изменений.

### <a name="update-to-common-data-service-for-then-leave-bank-transaction-entity-turns-into-an-insert-on-talent-side-352938"></a>Обновление до Common Data Service для банковской проводки отпуска превращается во вставку на стороне Talent (352938)

Это изменение исправляет проблему, когда обновление банковской транзакции отпуска создает новую запись в Talent.

## <a name="in-preview"></a>В режиме предварительного просмотра

Функции предварительной версии доступны только в средах **Песочница**.

### <a name="print-performance-reviews"></a>Печать оценок производительности

См. раздел [Печать оценок производительности](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) в Dynamics 365 волны 2 выпуска 2019 года.

