---
title: Введение в интерфейс API интеграции системы отслеживания кандидатов
description: В этом разделе описывается API-интерфейс Dynamics 365 Human Resources системы отслеживания кандидатов (АТС).
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 48e368fe69443a5105ddba78a887bf9159bfe52a
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125601"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a>Введение в интерфейс API интеграции системы отслеживания кандидатов

В этом разделе описывается API-интерфейс Dynamics 365 Human Resources системы отслеживания кандидатов (АТС). Целью API является обеспечение оптимизации интеграции между Dynamics 365 Human Resources и партнерскими системами ATS.

![Поток интеграци ATS](media/hr-admin-integration-ats-api-introduction-flow.png)

Интегрированный опыт начинается в модуле Human Resources, когда менеджер по найму создает запрос на прием на работу. Когда запрос активирован, ATS извлекает сведения о запросе для создания проекта набора персонала. Затем она следует конвейеру набора персонала, чтобы выбрать и нанять кандидата на должности. Наконец, ATS выполняет обратную интеграцию, отправляя запись выбранного кандидата в модуль Human Resources. Затем запись кандидата может пройти несколько проверок адаптации и рабочих процессов для создания записи сотрудника.

Для включения интеграции модуль Human Resources добавил следующие компоненты:

1.  Функциональность для создания запроса на набор персонала.
2.  Расширенный профиль кандидата и соответствующие рабочие процессы.
3.  API интеграции, открывающий новые функции для интеграции приложений.

Дополнительные сведения о настройке и использовании запроса на набор персонала и функции кандидата см. в разделе [Набор кандидатов на должности](hr-personnel-recruit.md).

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Этот API построен на основе Microsoft Dataverse (ранее Common Data Service). Все взаимодействие RESTful с этим API осуществляется с помощью веб-API Microsoft Dataverse, использующего OData. Этот API является подмножеством веб-API Dataverse. Веб-API Dataverse определяет такие характеристики, как проверка подлинности, соглашения SLA, пакет, управление одновременным доступом и обработка ошибок.

Дополнительные общие сведения о веб-API Microsoft Dataverse см. в разделах:

- [Что такое Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)
- [Использование веб-API Microsoft Dataverse](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)
- [Руководство разработчика Microsoft Dataverse](https://docs.microsoft.com/powerapps/developer/data-platform)

В приведенной выше документации содержится информация и руководство разработчика по использованию веб-API Dataverse, например, [управление проверкой подлинности](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [выполнение операций](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [использование Postman с помощью API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api) и [использование маркеров отслеживания изменений или разностного изменения](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) с API.

### <a name="option-sets"></a>Наборы параметров

Модель данных для интерфейса API интеграции ATS, описанная в данном документе, включает наборы параметров, которые предоставляют перечисляемые значения, связанные со свойствами сущностей. Подробные сведения о работе с наборами параметров в веб-API Dataverse см. в разделе [Создание и обновление наборов параметров с помощью веб-API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets). Наборы параметров определяются для каждой среды Dataverse.

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Виртуальные таблицы для Human Resources в Dataverse

Конечные точки для API интеграции ATS используют возможности платформы виртуальных таблиц Microsoft Dataverse. По умолчанию виртуальные таблицы и связанные с ними конечные точки API не развертываются для сред Human Resources, позволяя организациям определять, какие конечные точки OData будут доступны для данной среды. Для использования API-интерфейса необходимо создать виртуальные таблицы для сущностей Human Resources для данной среды. 

Сведения о создании виртуальных таблиц для API см. в разделе [Настройка виртуальных таблиц Dataverse](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

## <a name="data-model"></a>Модель данных

Модель данных центрируется вокруг двух основных сущностей:

- **RecruitingRequest** представляет запрос ATS для найма одной или нескольких открытых должностей. Пример запроса см. в разделе [Пример запроса по набору сотрудников](hr-admin-integration-ats-api-recruiting-request-example-query.md).
- **CandidateToHire** представляет сведения о кандидате, который принял предложение на должность. **Физическое лицо** представляет человека, который является кандидатом. Физическое лицо может иметь в компании несколько ролей, таких как кандидат, работник, сотрудник или подрядчик. Пример запроса см. в разделе [Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).

На следующей схеме показаны отношения внутри API. У нескольких типов есть внешние ключи для других, ранее существующих сущностей в модуле Human Resources, которые здесь не иллюстрируются. В этом документе приводятся сведения о сущностях, предназначенных специально для сценариев интеграции набора персонала. Однако в веб-API Dataverse для Dynamics 365 Human Resources имеется множество других сущностей, которые также могут быть связаны с интеграцией. Например, можно также получить сведения о работниках, заданиях, должностях или других сущностях, не определенных здесь. Многие из этих сущностей упоминаются в отношениях внешнего ключа или свойствах навигации.

![Модель данных API интеграции ATS](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a>Запрос набора персонала и связанные сущности и наборы параметров

Пример запроса: 

- [Пример запроса для запроса на набор персонала](hr-admin-integration-ats-api-recruiting-request-example-query.md)

Объекты:

- [Запрос на набор сотрудников](hr-admin-integration-ats-api-recruiting-request.md)
- [Позиция запроса на набор сотрудников](hr-admin-integration-ats-api-recruiting-request-position.md)
- [Навык в запросе по набору сотрудников](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [Образование в запросе по набору сотрудников](hr-admin-integration-ats-api-recruiting-request-education.md)
- [Местонахождение запроса на набор сотрудников](hr-admin-integration-ats-api-recruiting-request-location.md)

Наборы параметров:

- [Состояние освобождения должности от доплат за сверхурочное время](hr-admin-integration-ats-api-job-exempt-status.md)
- [Статус должности запроса набора персонала](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [Состояние запроса по набору сотрудников](hr-admin-integration-ats-api-recruiting-request-status.md)
- [Категория нормативных должностей](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a>Кандидаты для приема на работу и соответствующие сущности и наборы параметров

Пример запроса:

- [Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

Объекты:

- [Кандидат для приема на работу](hr-admin-integration-ats-api-candidate-to-hire.md)
- [Физическое лицо](hr-admin-integration-ats-api-person.md)
- [Образование физического лица](hr-admin-integration-ats-api-person-education.md)
- [Опыт работы физического лица](hr-admin-integration-ats-api-person-professional-experience.md)
- [Адрес физического лица](hr-admin-integration-ats-api-person-address.md)
- [Контакт субъекта](hr-admin-integration-ats-api-party-contact.md)
- [Навык физического лица](hr-admin-integration-ats-api-person-skill.md)
- [Уровень рейтинга](hr-admin-integration-ats-api-rating-level.md)
- [Сертификат физического лица](hr-admin-integration-ats-api-person-certificate.md)
- [Тип сертификата](hr-admin-integration-ats-api-certificate-type.md)
- [Отбор для лица](hr-admin-integration-ats-api-person-screening.md)
- [Типы отбора](hr-admin-integration-ats-api-screening-types.md)
- [Идентификационный номер физического лица](hr-admin-integration-ats-api-person-identification-number.md)

Наборы параметров:

- [Результат интеграции кандидата](hr-admin-integration-ats-api-applicant-integration-result.md)
- [Пусто Да Нет](hr-admin-integration-ats-api-blank-yes-no.md)
- [Статус выполнения](hr-admin-integration-ats-api-completion-status.md)
- [Тип контакта](hr-admin-integration-ats-api-contact-type.md)
- [Базис кредита образования](hr-admin-integration-ats-api-education-credit-basis.md)
- [Род](hr-admin-integration-ats-api-gender.md)
- [Семейное положение](hr-admin-integration-ats-api-marital-status.md)
- [Месяцы года](hr-admin-integration-ats-api-months-of-year.md)
- [Нет Да](hr-admin-integration-ats-api-no-yes.md)
- [Единица измерения периода](hr-admin-integration-ats-api-period-unit.md)
- [Частота отбора](hr-admin-integration-ats-api-screening-frequency.md)
- [Начальная дата создаваемой периодичности отбора](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [Тип уровня навыка](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a>См. также

[Найм кандидатов на должность](hr-personnel-recruit.md)<br>
[Что такое Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[Использование веб-API Microsoft Dataverse](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)<br>
[Создание и обновление наборов параметров с помощью веб-API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]