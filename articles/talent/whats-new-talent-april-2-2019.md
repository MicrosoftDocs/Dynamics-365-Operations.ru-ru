---
title: Что нового или что изменилось в Dynamics 365 Talent (2 апреля 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/02/2019
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
ms.search.validFrom: 2019-04-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 04b5a006d4580fe419d81986a90851bc8d611722
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528227"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-2-2019"></a>Что нового или что изменилось в Dynamics 365 Talent (2 апреля 2019 г.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой теме описываются новые и измененные компоненты Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Изменения в Attract

### <a name="approval-emails-in-attract"></a>Сообщения электронной почты об утверждении в Attract
Новые сообщения электронной почты улучшают прозрачность процесса утверждения. Сообщения электронной почты отправляются утверждающим при возникновении одного из следующих сценариев:

- Инициатор запроса отправляет должность на утверждение.
- Должность отклонена или утверждена.
- Утверждающее лицо не обработало запрос утверждение в течение 24 часов.

Можно настроить содержание сообщений электронной почты об утверждении с новыми шаблонами.

### <a name="application-and-profile-attachments"></a>Вложения для заявлений и профилей
Улучшения на вкладке **Документы** в заявлениях и профилях кадровых пулов теперь отображают как название, так и тип документа.

## <a name="changes-in-onboard"></a>Изменения в Onboard
Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.

## <a name="coming-soon-attract-and-onboard"></a>Скоро появится (Attract и Onboard)

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Интеграция Lifecycle Services (LCS) с функцией сообщения о проблеме
В Attract и Onboard проблемы, зарегистрированные конечными пользователями через функцию сообщения о проблеме, теперь автоматически создают проблемы технической поддержки в проекте LCS клиента. Администраторы могут затем сортировать проблемы и передавать их в корпорацию Майкрософт при необходимости. Это согласуется с тем, как Core HR обрабатывает проблемы технической поддержки конечных пользователей.

## <a name="changes-in-core-hr"></a>Изменения в Core HR
Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2216.

### <a name="platform-update-25-for-finance-and-operations"></a>Обновление платформы 25 для Finance and Operations
Дополнительные сведения об обновлении платформы Platform update 25 для Finance and Operations см. в разделе [Предварительные версии функций в Dynamics 365 for Finance and Operations Platform Update 25 (апрель 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-25).

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Расширенная безопасность компенсации (фиксированной и переменной)
Во многих организациях менеджеры по компенсации и льготам могут иметь доступ только к определенным записям компенсаций. Эти записи могут включать записи для руководителей или региональных сотрудников. Это изменение позволяет отделу кадров управлять и обслуживать планы компенсации для различных групп сотрудников в организации. Можно назначить роли безопасности для фиксированных и переменных планов. Эти роли безопасности определяют доступ к планам и соответствующим данным сотрудников, таким как записи зарплаты или премий, чтобы только эти роли может обрабатывать компенсацию для групп сотрудников.

### <a name="upgrade-to-common-data-service"></a>Обновление до Common Data Service
Крайние сроки для обновления до Common Data Service быстро приближаются. Войдите в центр администрирования Microsoft Power Apps для определения, необходимо ли обновить вашу базу данных. Дополнительные сведения о крайних сроках и необходимых действиях по обновлению см. в разделе [Обновление до Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>В режиме предварительного просмотра

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Разрешить указывать коды причины для типов отпусков
Организациям могут потребоваться дополнительные сведения о запросах выходных. Теперь можно задать коды причин для типов отпуска и дать рабочим возможность выбрать код причины в их запросе выходных.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Требование кодов причин для определенных типов отпусков для запросов отпусков
Организации могут требовать коды причины для определенных типов отпусков, когда сотрудники отправляют запрос выходных. Это может быть из-за политики компании или нормативных требований. Теперь можно указать, какие типы отпусков требуют код причины, и можно потребовать, чтобы сотрудники указывали код причины для данного типа отпуска в их запросах отпусков.

## <a name="coming-soon"></a>Скоро

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Улучшения интерфейса пользователя для проверки дубликатов сотрудников
После этого изменения дубликаты определяются по мере ввода полей имени, и статус отображает число обнаруженных дубликатов. Можно выбрать предоставленную ссылку, чтобы открыть новую страницу для оценки, следует ли использовать обнаруженное соответствие. Во избежание прерывания ввода данных форма дубликатов не открывается автоматически.

###  <a name="email-support-for-alerts"></a>Поддержка по электронной почте для оповещений
С обновлением платформы Platform update 25 для Finance and Operations пользователи могут создавать правила оповещений, которые автоматически посылают уведомления по электронной почте контактам при наступлении события. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]