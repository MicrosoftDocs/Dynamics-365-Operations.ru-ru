---
title: Что нового и что изменилось в Dynamics 365 Talent (6 мая 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c04af27bcc446b516f14125e71fb707bfd1d7708
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529716"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-6-2019"></a>Что нового и что изменилось в Dynamics 365 Talent (6 мая 2019 г.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой теме описываются новые и измененные компоненты Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Изменения в Attract

### <a name="select-optional-documents-upon-offer-creation"></a>Выбор дополнительных документов при создании предложения

После выбора шаблона пакета предложений Attract теперь предлагает выбрать применимые дополнительные документы из шаблона пакета. При подготовке предложения можно добавлять дополнительные документы.

## <a name="changes-in-onboard"></a>Изменения в Onboard

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Изменения в Core HR

Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2282. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-26-for-finance-and-operations"></a>Обновление платформы 26 для Finance and Operations

Дополнительные сведения об обновлении платформы Platform update 26 для Finance and Operations см. в разделе [Предварительные версии функций в Dynamics 365 Finance and Operations Platform Update 26 (май 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26). 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Поддержка сущностей Common Data Service для настраиваемых полей

В выпуске этой недели следующие сущности теперь поддерживают настраиваемые поля: частота расчета льгот, ставка расчета льгот, тип льготы, рабочий календарь, выходной рабочего календаря, цикл оплаты и типы идентификации работников.

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a>В массовой регистрации отпусков при изменении базы уровня "Дата трудового стажа" не обновляется исходная ставка начисления (318526)

При массовой регистрации сотрудников и изменении базы уровня первоначальное начисление теперь отражает выбранную базу уровня.

### <a name="workflow-showing-duplicate-place-holders-313636"></a>Рабочий процесс отображает повторяющиеся заполнители (313636)

Изменения в этом выпуске устраняют дублирование заполнителей при отправке уведомлений рабочего процесса.

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a>Поля аналитики не обновляются при использовании "Открыть в Excel" (176261)

В этом выпуске теперь можно обновить финансовую аналитику, используя команду **Открыть в Excel** на странице **Работник**. 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a>Адрес работника, созданный в Common Data Service, не синхронизируется с Talent (317555)

С этим изменением адреса, созданные в Common Data Service, обновляются в Talent: Core HR.


## <a name="in-preview"></a>В режиме предварительного просмотра

### <a name="new-page-to-validate-position-hierarchy-data"></a>Новая страница для проверки данных иерархии должностей

Отдел кадров и администраторы теперь могут проверять иерархию управления на наличие любых циклических ссылок, которые могли быть случайно импортированы. Эту новую страницу можно открыть по пути **Управление организацией > Ссылки > Должности > Проверка иерархии должностей**.

### <a name="specify-reason-codes-on-leave-types"></a>Указание кодов причин для типов отпусков

Организациям могут потребоваться дополнительные сведения о запросах выходных. Теперь можно задать коды причин для типов отпуска и позволить рабочим выбирать код причины в их запросе выходных.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Требование кодов причин для определенных типов отпусков для запросов отпусков

Организации могут требовать коды причины для определенных типов отпусков, когда сотрудники отправляют запросы выходных. Это требование может быть вызвано политикой компании или нормативными требованиями. Теперь можно указать, какие типы отпусков требуют код причины, и можно потребовать, чтобы сотрудники указывали код причины для данного типа отпуска в их запросах отпусков.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Предоставление отпуска и списка проводок отсутствия для отдела кадров

Возможность отслеживания времени отсутствия сотрудника и понимание того, как нерабочее время вычисляется, не только помогает отделу кадров отвечать на вопросы сотрудников, но и также помогает обеспечить точное назначение выходных для сотрудников. Отдел кадров теперь имеет новое представление проводок (гранты, начисления, корректировки и запросы), чтобы персонал отдела кадров мог просматривать причины в основе сальдо.

## <a name="coming-soon"></a>Скоро

### <a name="indicate-instance-type-when-provisioning-talent"></a>Указание типа экземпляра при подготовке Talent

При подготовке нового экземпляра Talent можно будет указать тип экземпляра **Производство** или **Песочница**, позволяя производить раннее тестирование новых функций. Все существующие экземпляры Talent будут обновлены до типа экземпляра "Производство". Если необходимо обновить один из существующих экземпляров до типа экземпляра "Песочница", обратитесь в службу поддержки, чтобы инициировать запрос на изменение.


[!INCLUDE[footer-include](../includes/footer-banner.md)]