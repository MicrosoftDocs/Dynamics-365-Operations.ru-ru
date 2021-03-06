---
title: Что нового и что изменилось в Dynamics 365 Talent (23 июля 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2019
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
ms.search.validFrom: 2019-07-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 360574d3c8e0b349119e0987f2453a5d5be21e90
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528155"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-23-2019"></a>Что нового и что изменилось в Dynamics 365 Talent (23 июля 2019 г.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой теме описываются новые и измененные компоненты Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Изменения в Attract

### <a name="pdf-renderer-for-candidate-documents"></a>Средство подготовки PDF для документов кандидатов

Вместо того, чтобы загружать вложения, пользователи Attract могут теперь просматривать вложения PDF для кандидатов в средстве просмотра документов.

### <a name="signing-up-for-attract-user-research-group"></a>Регистрация в группе исследований пользователей Attract 

При планировании новых возможностей продукта или отправке предварительных функций мы будем искать пользователей, которые помогут информировать о нашем направлении. Заинтересованные пользователи теперь могут подписаться на участие в нашей группе исследований, используя ссылку подписки в приложении.

### <a name="job-approvals-appear-on-the-home-page"></a>Утверждения должностей отображаются на домашней странице

Утверждения отображаются в разделе **Утверждения** на панели мониторинга. Утверждающие могут просмотреть свои утверждения в разделе **Назначено вам**, который отображает код должности, название должности, других утверждающих и дату назначения должности. Пользователи, которые отправляют должности на утверждение, могут просматривать свои должности в разделе **Запрошено вами**, в котором отображаются утверждающие, которые все еще должны утвердить отправленную должность.

## <a name="changes-in-onboard"></a>Изменения в Onboard
Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Изменения в Core HR
Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2394.

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Поддержка объектов для настраиваемых полей в Common Data Service 

В этом выпуске **Рабочий календарь** и **День рабочего календаря** теперь поддерживают настраиваемые поля в Common Data Service.

### <a name="restrict-leave-types-in-time-off-requests"></a>Ограничение типов отпусков в запросах времени отсутствия

Организации могут предложить сотрудникам много различных типов отпусков. Однако может быть недопустимо, чтобы сотрудники могли подавать запросы на время отсутствие для некоторых типов отпусков. Эти типы отпусков могут управляться вместо этого отделом кадров. В этом выпуске можно настроить, для каких типов отпусков сотрудники могут отправлять запросы времени отсутствия. 

## <a name="in-preview"></a>В режиме предварительного просмотра

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Предварительные версии функций доступны только в экземплярах "песочницы"

При подготовке нового экземпляра Talent можно указать, имеет ли данный экземпляр тип **Производство** или **Песочница**. Экземпляры типа **Песочница** позволяют заблаговременно тестировать новые возможности. Все существующие экземпляры Talent будут обновлены до типа экземпляра **Производство**. Если необходимо обновить один из существующих экземпляров до типа экземпляра **Песочница**, обратитесь в [службу поддержки](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), чтобы инициировать запрос на изменение.

Дополнительные сведения о порядке публикации изменений см. в разделе [Подготовка Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Просмотр расширенной информации о производительности на портале самообслуживания менеджера

Новый параметр позволит менеджерам просматривать производительность как своих прямых подчиненных, так и их расширенных подчиненных. В настоящее время линейные менеджеры могут назначать и обновлять цели производительности и выпускать новые обзоры, которыми сотрудники совместно управляют. Кроме того, прямые менеджеры и их сотрудники могут вести поддержку и обновлять журналы производительности, чтобы обеспечить плавность процесса проверки производительности. Когда это изменение будет реализовано, менеджеры смогут просматривать и вести сведения о производительности для расширенных подчиненных в дополнение к их прямым подчиненным. 

## <a name="coming-soon"></a>Скоро

### <a name="region-support-for-canada-and-southeast-asia"></a>Поддержка региона для Канады и Юго-Восточной Азии

Мы рады сообщить, что регионы Канады и Юго-Восточной Азии будут доступны для Talent с 1 августа 2019. С помощью этого изменения можно создавать среды в регионах Канады и Азии, и все данные Talent будут поддерживаться исключительно в пределах этих мест. Можно создать среду в этих новых регионах, выбрав местоположение в диалоговом окне новой среды и использовать эту среду для подготовки Talent в LCS, так как это описывается в разделе [Подготовка Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

Миграция данных существующих проектов из других регионов в регионы Канада и Азия не поддерживается. Только новые проекты могут быть подготовлены в этих новых поддерживаемых регионах.


[!INCLUDE[footer-include](../includes/footer-banner.md)]