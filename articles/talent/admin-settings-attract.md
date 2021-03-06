---
title: Настройка информации об организации в Attract
description: В этой теме объясняется, как настроить информацию о компании и фирменную символику для Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: db3ec965f3a52810d5f310697b9ed830c3abe681
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462409"
---
# <a name="configure-company-information-in-attract"></a>Настройка информации об организации в Attract

[!include [banner](includes/banner.md)]

Центре администрирования в Microsoft Dynamics 365 Talent: Attract содержит параметры конфигурации, параметры интеграции и параметры настройки для приложения Attract.

## <a name="company-information"></a>Сведения о компании

Введите отображаемое имя для компании и добавьте эмблему компании. Отображаемое имя и эмблема могут затем использоваться в объявлениях о вакансии и во время адаптации.

## <a name="linkedin-integration"></a>Интеграция с LinkedIn

Настройка интеграции с модулем LinkedIn Recruiter System Connect(RSC). После подключения к LinkedIn, используя учетные данные LinkedIn, можно выполнить синхронизацию профиля LinkedIn, приложений, отзывов по собеседованиям и примечаний группы найма. Необходима полная лицензия агентства по найму LinkedIn. Дополнительные сведения о LinkedIn Recruiter см. в разделе [Recruiter System Connect (RSC) — вопросы и ответы](https://www.linkedin.com/help/recruiter/answer/90483).

## <a name="user-permissions"></a>Разрешения пользователей

Назначьте роли пользователям в вашей организации. Доступны следующие роли: **Администратор**, **Специалист по найму**, **Специалист по комплектации штата** и **Только для чтения**. Дополнительные сведения о разрешениях пользователя см. в разделе [Безопасность и управление ролями в Attract](./security-attract.md).

## <a name="feature-management"></a>Управление функциями

По мере добавления новых функций они могут выпускаться для общедоступного ознакомления. Функции общедоступной ознакомительной версии не соответствует всем требованиям к службам. Получив их, вы соглашаетесь предоставить доступ к своим данным внешним системам. Можно обнаружить, что для вашей организации не требуются все выпущенные новые функции. Функции общедоступной предварительной версии можно выключать и включать в зависимости от потребностей организации.

## <a name="template-management"></a>Управление шаблонами

Шаблон процесса содержит все действия, которые должны быть включены как часть процесса найма на работу. Ваша организация может разрешить создавать шаблоны процесса найма всем членам группы или только администраторам. Чтобы разрешить членам группы создавать свои собственные шаблоны процесса найма, включите функциональность управления шаблонами. Дополнительные сведения о шаблонах процессов см. в разделе [Создание шаблона процесса в Attract](./process-templates-attract.md).

## <a name="email-template-settings"></a>Параметры шаблонов электронной почты

Организации могут создавать шаблоны сообщений электронной почты для различных сценариев. Можно выбрать изображение заголовка для включения в шаблоны сообщений электронной почты. Затем выбранный заголовок появляется во всех шаблонах электронной почты. В нижнем колонтитуле шаблона можно добавить ссылку на заявление о конфиденциальности вашей организации и условия использования для обмена данными. Дополнительные сведения см. в разделе [Шаблоны электронной почты](./email-templates.md).

## <a name="offer-process"></a>Процесс предложения

Можно настроить процесс утверждения для предложений должностей. Например, можно указать, требуется ли утверждать предложение перед отправкой кандидату. Можно также требовать, чтобы утверждающие оставляли комментарий со своим решением.

Доступны два workflow-процесса утверждения: **Параллельный** и **Последовательный**.

- **Параллельный** — утверждения отправляются всем утверждающим одновременно.
- **Последовательный** — утверждения отправляются утверждающим в определенном порядке.

Можно также настроить параметры, которые относятся к опыту кандидата. Например, один вариант позволяет указать, могут ли кандидаты отклонить предложение без дополнительного обсуждения. Если для параметра **Разрешить кандидатам отклонять предложение без дополнительных обсуждений** задано значение **Нет**, кнопка **Отклонить предложение** будет доступна для кандидатов. Если для этого параметра задать значение **Да**, кандидаты могут отклонить предложение, выбрав причину, затем выбрав **Отклонить предложение**.

Можно также задавать и вводить дату окончания срока действия для предложений. Если для параметра **Требуется дата окончания срока действия всех предложений** задано значение **Да**, срок действия предложений истекает через количество часов или дней, указанных пользователем.

Дополнительные сведения об управлении предложениями см. в разделе [Настройка управления предложениями](./offer-setup.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]