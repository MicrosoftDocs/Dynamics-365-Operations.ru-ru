---
title: Что нового и что изменилось в Dynamics 365 Talent (16 июля 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/16/2019
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
ms.search.validFrom: 2019-07-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: cd7f288e5c1015f4266db527adfcd62a5dbbc95f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528108"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-16-2019"></a>Что нового и что изменилось в Dynamics 365 Talent (16 июля 2019 г.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Изменения в Attract
Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>Скоро появится в Attract
#### <a name="job-approvals-appear-on-the-home-page"></a>Утверждения должностей отображаются на домашней странице

Утверждения отображаются в разделе **Утверждения** на панели мониторинга. Утверждающие могут просмотреть свои утверждения в разделе **Назначено вам**, который отображает код должности, название должности, других утверждающих и дату назначения должности. Пользователи, которые отправляют должности на утверждение, могут просматривать свои должности в разделе **Запрошено вами**, в котором отображаются утверждающие, которые все еще должны утвердить отправленную должность.

## <a name="changes-in-onboard"></a>Изменения в Onboard
Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Изменения в Core HR
Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2390.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Объекты Common Data Service, которые сейчас поддерживают настраиваемые поля

- BusinessProcessCalendar                     
- BusinessProcessGroupAssignment         
- BusinessProcessStage                          
- BusinessProcessTemplateHeader          
- BusinessProcessTemplateTask            
- HcmBenefitOption                              
- HcmBenefitType                                  
- HcmCompensationGrid                            
- HcmCompensationLevel                          
- HcmCompensationPayFrequency                 
- HcmCompensationReferencePointSetup        
- HcmCompensationReferencePointSetupLine 
- HcmCompensationRegion                     
- HcmCompFixedPlanTable                     
- HcmEmployment                                
- HcmEthnicOrigin                                
- HcmFixedCompensationEvent                 
- HcmJob                                           
- HcmJobFunction
- HcmJobType
- HcmLanguageCode
- HcmPayrollCalculationFrequency
- HcmPosition
- HcmPositionType
- HcmSkillType
- HcmVeteranStatus
- HcmWorkCalendarHoliday
- HcmWorkCalendarHolidayLine
- HcmWorker
- HcmWorkerPersonalDetail
- LeaveType
- OMDepartment
- OMLegalEntity
- PayCycle
- PayPeriod
- PayrollBenefitCalculationRate
- PayrollBenefitCalculationRateDetail
- PayrollEarningCode

### <a name="unable-to-see-goals-and-reviews-in-manager-self-service"></a>Не удается просмотреть цели и обзоры на портале самообслуживания менеджера

Текущие изменения этой недели позволяют отображать и изменять цели и обзоры руководителей промежуточных уровней на портале самообслуживания руководителей.

### <a name="goal-form-cannot-be-closed-after-a-user-edits-any-goal-field"></a>Форму цели невозможно закрыть после того, как пользователь изменит какое-либо поле цели

В этом выпуске исправлена проблема, при которой форма цели не закрывается при выборе команды **Закрыть**.

### <a name="creating-new-goals-and-saving-displays-error"></a>Создание новых целей и сохранение выводит сообщение об ошибке

В этом выпуске исправляется проблема при сохранении целей на портале самообслуживания сотрудников и менеджеров.

### <a name="unable-to-add-a-field-to-position-details"></a>Не удается добавить поле к сведениям о должности 

В этом выпуске настраиваемые поля теперь поддерживаются в сведениях о должности.
 
### <a name="unable-to-set-up-expiring-date-on-the-earning-code-through-data-management"></a>Невозможно настроить дату истечения срока действия кода дохода через управление данными

Теперь изменения позволяют установить даты истечения срока действия для кодов доходов в управлении данными.

### <a name="new-custom-fields-dont-sync-quickly-enough"></a>Новые настраиваемые поля не синхронизируются достаточно быстро

Улучшена производительность синхронизации настраиваемых полей с Common Data Service в выпуске данной недели.

### <a name="entity-export-to-database-jobs-fail-with-error-message-format-of-the-initialization-string-does-not-conform-to-specification-starting-at-index-0"></a>При экспорте объекта в задания базы данных происходит сбой с сообщением об ошибке: "Формат строки инициализации не соответствует спецификации, начинающейся с индекса 0".

В этой версии исправляется проблема, в которой пакетные задания базы данных завершаются сбоем. Для обновления вручную:

1. Перейдите в раздел **Управление данными**.
2. Выберите **Настроить экспорт объекта в базу данных**.
3. Повторно введите строку подключения к целевой базе данных и выберите **Сохранить**.

### <a name="smtp-email-configuration-suddenly-fails-with-error-message-the-smtp-server-requires-a-secure-connection-or-the-client-was-not-authenticated"></a>Конфигурация электронной почты SMTP внезапно перестает работать с сообщением об ошибке: "SMTP-сервер требует безопасного подключения, или клиент не прошел проверку подлинности".

В этом выпуске исправлена конфигурация электронной почты SMTP, которая может внезапно привести к отказу. Для обновления вручную:

1. Выберите **Администрирование системы**.
2. Выберите **Параметры электронной почты**.
3. Выберите **Параметры SMTP**. 
4. Повторно введите имя пользователя и пароль, используемые для SMTP-сервера, и выберите **Сохранить**.

## <a name="in-preview"></a>В режиме предварительного просмотра

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Предварительные версии функций доступны только в экземплярах "песочницы"

При подготовке нового экземпляра Talent можно указать, имеет ли данный экземпляр тип **Производство** или **Песочница**. Экземпляры типа **Песочница** позволяют заблаговременно тестировать новые возможности. Все существующие экземпляры Talent будут обновлены до типа экземпляра **Производство**. Если необходимо обновить один из существующих экземпляров до типа экземпляра **Песочница**, обратитесь в [службу поддержки](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), чтобы инициировать запрос на изменение.

Дополнительные сведения о порядке публикации изменений см. в разделе [Подготовка Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Ограничение типов отпусков в запросах времени отсутствия

Организации могут предложить сотрудникам много различных типов отпусков. Однако может быть недопустимо, чтобы сотрудники могли подавать запросы на время отсутствие для некоторых типов отпусков. Эти типы отпусков могут управляться вместо этого отделом кадров. В этом выпуске можно настроить, для каких типов отпусков сотрудники могут отправлять запросы времени отсутствия. 

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Просмотр информации о производительности для прямых и расширенных подчиненных на портале самообслуживания менеджера

Новый параметр позволит менеджерам просматривать производительность как своих прямых подчиненных, так и их расширенных подчиненных. В настоящее время линейные менеджеры могут назначать и обновлять цели производительности и выпускать новые обзоры. Кроме того, прямые менеджеры и их сотрудники могут вести поддержку и обновлять журналы производительности, чтобы обеспечить плавность процесса проверки производительности. Когда это изменение будет реализовано, менеджеры смогут просматривать и вести сведения о производительности для расширенных подчиненных в дополнение к их прямым подчиненным.


[!INCLUDE[footer-include](../includes/footer-banner.md)]