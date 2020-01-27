---
title: Что нового и что изменилось в Dynamics 365 Talent (14 марта 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/14/2019
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
ms.search.validFrom: 2019-03-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 79bb8c0ed3c3f3bee62a8bc384a9d3a15cfe881a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897611"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-14-2019"></a>Что нового и что изменилось в Dynamics 365 Talent (14 марта 2019 г.)

В этой теме описываются новые и измененные компоненты в Talent.

## <a name="changes-in-attract"></a>Изменения в Attract
Исправления незначительных ошибок включены в этот выпуск.

## <a name="changes-in-onboarding"></a>Изменения в Onboarding
Исправления незначительных ошибок включены в этот выпуск.

## <a name="changes-in-core-hr"></a>Изменения в Core HR
**Сборка 8.1.2186**

### <a name="performance-management-not-working-in-all-scenarios-when-using-duplicate-security-roles"></a>Управление производительностью не работает во всех случаях при использовании дубликатов ролей безопасности
Изменения, внесенные в данном выпуске, поддерживают сценарии управления производительностью при использовании готовых или дублированных ролей.

### <a name="mass-assign-checklists-to-workers"></a>Массовое назначение контрольных списков для работников
После этого изменения теперь можно выбрать несколько сотрудников и массово назначить этим сотрудников один или несколько контрольных списков. 

### <a name="platform-update-24-for-finance-and-operations"></a>Platform update 24 для Finance and Operations
Дополнительные сведения об обновлении платформы Platform Update 24 для Finance and Operations см. в разделе [Что нового и что изменилось в Finance and Operations с обновлением платформы Platform Update 24 (март 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24). Значительные изменения в платформе 24 включают: 

- Оповещения включены в Talent.
- Обновленная панель навигации теперь совместима с заголовком Office.

### <a name="office-location-update-switches-the-context-to-the-top-of-the-worker-list"></a>Обновление местоположения офиса переключает контекст на верхнюю часть списка рабочих
В текущем выпуске изменение расположения офиса будет больше не переключать контекст работника, которого вы просматриваете, когда назначаете расположение офиса.

### <a name="position-assignment-end-date-doesnt-display-correctly-on-worker-hire-and-transfer-actions"></a>Дата окончания назначения должности не отображается правильно для действий приема на работу и перевода работника
Даты окончания назначения должности теперь отображаются правильно на основании предпочтительного часового пояса пользователя при использовании действий.

### <a name="common-data-service-job-entity-doesnt-allow-job-type-and-job-function-fields-to-update"></a>Объект должности Common Data Service не допускает обновление полей "Тип должности" и "Должностные функции"
Объекты Common Data Service теперь правильно синхронизируются при обновлении с помощью Common Data Service.

## <a name="coming-soon"></a>Скоро

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Расширенная безопасность компенсации (фиксированной и переменной)
Во многих организациях менеджеры по компенсации и льготам могут иметь доступ только к определенным записям компенсаций. Они могут быть для руководителей или региональных сотрудников. С этим изменением отдел кадров можете управлять и обслуживать планы компенсации для различных групп сотрудников в организации. Можно назначить роли безопасности фиксированным и переменным планам, которые будут определять доступ к этим планам и данным о сотрудниках, относящихся к планам, таким как записи сведений о зарплате и премиях. Только роли, которым предоставлен доступ, могут обработать компенсацию для этих сотрудников.

###  <a name="email-support-for-alerts"></a>Поддержка по электронной почте для оповещений
С обновлением платформы Platform update 24 для Finance and Operations пользователи могут создавать правила оповещений, которые автоматически отправляют уведомления по электронной почте контактам при наступлении события.

### <a name="duplicate-employee-check-interface-changes"></a>Проверка дублирования сотрудника: изменения интерфейса
После этого изменения дубликаты определяются по мере ввода полей имени, и статус отображает число обнаруженных. Можно выбрать предоставленную ссылку, чтобы открыть новую страницу для оценки, следует ли использовать обнаруженное соответствие. Форма дубликатов не открывается автоматически во избежание прерывания ввода данных.
