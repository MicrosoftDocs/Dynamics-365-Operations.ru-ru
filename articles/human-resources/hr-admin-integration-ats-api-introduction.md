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
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="069b6-103">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="069b6-103">Applicant Tracking System integration API introduction</span></span>

<span data-ttu-id="069b6-104">В этом разделе описывается API-интерфейс Dynamics 365 Human Resources системы отслеживания кандидатов (АТС).</span><span class="sxs-lookup"><span data-stu-id="069b6-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="069b6-105">Целью API является обеспечение оптимизации интеграции между Dynamics 365 Human Resources и партнерскими системами ATS.</span><span class="sxs-lookup"><span data-stu-id="069b6-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![Поток интеграци ATS](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="069b6-107">Интегрированный опыт начинается в модуле Human Resources, когда менеджер по найму создает запрос на прием на работу.</span><span class="sxs-lookup"><span data-stu-id="069b6-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="069b6-108">Когда запрос активирован, ATS извлекает сведения о запросе для создания проекта набора персонала.</span><span class="sxs-lookup"><span data-stu-id="069b6-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="069b6-109">Затем она следует конвейеру набора персонала, чтобы выбрать и нанять кандидата на должности.</span><span class="sxs-lookup"><span data-stu-id="069b6-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="069b6-110">Наконец, ATS выполняет обратную интеграцию, отправляя запись выбранного кандидата в модуль Human Resources.</span><span class="sxs-lookup"><span data-stu-id="069b6-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="069b6-111">Затем запись кандидата может пройти несколько проверок адаптации и рабочих процессов для создания записи сотрудника.</span><span class="sxs-lookup"><span data-stu-id="069b6-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="069b6-112">Для включения интеграции модуль Human Resources добавил следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="069b6-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="069b6-113">Функциональность для создания запроса на набор персонала.</span><span class="sxs-lookup"><span data-stu-id="069b6-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="069b6-114">Расширенный профиль кандидата и соответствующие рабочие процессы.</span><span class="sxs-lookup"><span data-stu-id="069b6-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="069b6-115">API интеграции, открывающий новые функции для интеграции приложений.</span><span class="sxs-lookup"><span data-stu-id="069b6-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="069b6-116">Дополнительные сведения о настройке и использовании запроса на набор персонала и функции кандидата см. в разделе [Набор кандидатов на должности](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="069b6-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="069b6-117">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="069b6-117">Microsoft Dataverse</span></span>

<span data-ttu-id="069b6-118">Этот API построен на основе Microsoft Dataverse (ранее Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="069b6-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="069b6-119">Все взаимодействие RESTful с этим API осуществляется с помощью веб-API Microsoft Dataverse, использующего OData.</span><span class="sxs-lookup"><span data-stu-id="069b6-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="069b6-120">Этот API является подмножеством веб-API Dataverse.</span><span class="sxs-lookup"><span data-stu-id="069b6-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="069b6-121">Веб-API Dataverse определяет такие характеристики, как проверка подлинности, соглашения SLA, пакет, управление одновременным доступом и обработка ошибок.</span><span class="sxs-lookup"><span data-stu-id="069b6-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="069b6-122">Дополнительные общие сведения о веб-API Microsoft Dataverse см. в разделах:</span><span class="sxs-lookup"><span data-stu-id="069b6-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="069b6-123">Что такое Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="069b6-123">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="069b6-124">Использование веб-API Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="069b6-124">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="069b6-125">Руководство разработчика Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="069b6-125">Microsoft Dataverse developer guide</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform)

<span data-ttu-id="069b6-126">В приведенной выше документации содержится информация и руководство разработчика по использованию веб-API Dataverse, например, [управление проверкой подлинности](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [выполнение операций](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [использование Postman с помощью API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api) и [использование маркеров отслеживания изменений или разностного изменения](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) с API.</span><span class="sxs-lookup"><span data-stu-id="069b6-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="069b6-127">Наборы параметров</span><span class="sxs-lookup"><span data-stu-id="069b6-127">Option sets</span></span>

<span data-ttu-id="069b6-128">Модель данных для интерфейса API интеграции ATS, описанная в данном документе, включает наборы параметров, которые предоставляют перечисляемые значения, связанные со свойствами сущностей.</span><span class="sxs-lookup"><span data-stu-id="069b6-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="069b6-129">Подробные сведения о работе с наборами параметров в веб-API Dataverse см. в разделе [Создание и обновление наборов параметров с помощью веб-API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span><span class="sxs-lookup"><span data-stu-id="069b6-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="069b6-130">Наборы параметров определяются для каждой среды Dataverse.</span><span class="sxs-lookup"><span data-stu-id="069b6-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="069b6-131">Виртуальные таблицы для Human Resources в Dataverse</span><span class="sxs-lookup"><span data-stu-id="069b6-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="069b6-132">Конечные точки для API интеграции ATS используют возможности платформы виртуальных таблиц Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="069b6-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="069b6-133">По умолчанию виртуальные таблицы и связанные с ними конечные точки API не развертываются для сред Human Resources, позволяя организациям определять, какие конечные точки OData будут доступны для данной среды.</span><span class="sxs-lookup"><span data-stu-id="069b6-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="069b6-134">Для использования API-интерфейса необходимо создать виртуальные таблицы для сущностей Human Resources для данной среды.</span><span class="sxs-lookup"><span data-stu-id="069b6-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="069b6-135">Сведения о создании виртуальных таблиц для API см. в разделе [Настройка виртуальных таблиц Dataverse](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="069b6-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

## <a name="data-model"></a><span data-ttu-id="069b6-136">Модель данных</span><span class="sxs-lookup"><span data-stu-id="069b6-136">Data model</span></span>

<span data-ttu-id="069b6-137">Модель данных центрируется вокруг двух основных сущностей:</span><span class="sxs-lookup"><span data-stu-id="069b6-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="069b6-138">**RecruitingRequest** представляет запрос ATS для найма одной или нескольких открытых должностей. Пример запроса см. в разделе [Пример запроса по набору сотрудников](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="069b6-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="069b6-139">**CandidateToHire** представляет сведения о кандидате, который принял предложение на должность.</span><span class="sxs-lookup"><span data-stu-id="069b6-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="069b6-140">**Физическое лицо** представляет человека, который является кандидатом.</span><span class="sxs-lookup"><span data-stu-id="069b6-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="069b6-141">Физическое лицо может иметь в компании несколько ролей, таких как кандидат, работник, сотрудник или подрядчик.</span><span class="sxs-lookup"><span data-stu-id="069b6-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="069b6-142">Пример запроса см. в разделе [Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="069b6-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="069b6-143">На следующей схеме показаны отношения внутри API.</span><span class="sxs-lookup"><span data-stu-id="069b6-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="069b6-144">У нескольких типов есть внешние ключи для других, ранее существующих сущностей в модуле Human Resources, которые здесь не иллюстрируются.</span><span class="sxs-lookup"><span data-stu-id="069b6-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="069b6-145">В этом документе приводятся сведения о сущностях, предназначенных специально для сценариев интеграции набора персонала.</span><span class="sxs-lookup"><span data-stu-id="069b6-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="069b6-146">Однако в веб-API Dataverse для Dynamics 365 Human Resources имеется множество других сущностей, которые также могут быть связаны с интеграцией.</span><span class="sxs-lookup"><span data-stu-id="069b6-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="069b6-147">Например, можно также получить сведения о работниках, заданиях, должностях или других сущностях, не определенных здесь.</span><span class="sxs-lookup"><span data-stu-id="069b6-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="069b6-148">Многие из этих сущностей упоминаются в отношениях внешнего ключа или свойствах навигации.</span><span class="sxs-lookup"><span data-stu-id="069b6-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![Модель данных API интеграции ATS](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="069b6-150">Запрос набора персонала и связанные сущности и наборы параметров</span><span class="sxs-lookup"><span data-stu-id="069b6-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="069b6-151">Пример запроса:</span><span class="sxs-lookup"><span data-stu-id="069b6-151">Example query:</span></span> 

- [<span data-ttu-id="069b6-152">Пример запроса для запроса на набор персонала</span><span class="sxs-lookup"><span data-stu-id="069b6-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="069b6-153">Объекты:</span><span class="sxs-lookup"><span data-stu-id="069b6-153">Entities:</span></span>

- [<span data-ttu-id="069b6-154">Запрос на набор сотрудников</span><span class="sxs-lookup"><span data-stu-id="069b6-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="069b6-155">Позиция запроса на набор сотрудников</span><span class="sxs-lookup"><span data-stu-id="069b6-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="069b6-156">Навык в запросе по набору сотрудников</span><span class="sxs-lookup"><span data-stu-id="069b6-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="069b6-157">Образование в запросе по набору сотрудников</span><span class="sxs-lookup"><span data-stu-id="069b6-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="069b6-158">Местонахождение запроса на набор сотрудников</span><span class="sxs-lookup"><span data-stu-id="069b6-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="069b6-159">Наборы параметров:</span><span class="sxs-lookup"><span data-stu-id="069b6-159">Option sets:</span></span>

- [<span data-ttu-id="069b6-160">Состояние освобождения должности от доплат за сверхурочное время</span><span class="sxs-lookup"><span data-stu-id="069b6-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="069b6-161">Статус должности запроса набора персонала</span><span class="sxs-lookup"><span data-stu-id="069b6-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="069b6-162">Состояние запроса по набору сотрудников</span><span class="sxs-lookup"><span data-stu-id="069b6-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="069b6-163">Категория нормативных должностей</span><span class="sxs-lookup"><span data-stu-id="069b6-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="069b6-164">Кандидаты для приема на работу и соответствующие сущности и наборы параметров</span><span class="sxs-lookup"><span data-stu-id="069b6-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="069b6-165">Пример запроса:</span><span class="sxs-lookup"><span data-stu-id="069b6-165">Example query:</span></span>

- [<span data-ttu-id="069b6-166">Пример запроса кандидата для приема на работу</span><span class="sxs-lookup"><span data-stu-id="069b6-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="069b6-167">Объекты:</span><span class="sxs-lookup"><span data-stu-id="069b6-167">Entities:</span></span>

- [<span data-ttu-id="069b6-168">Кандидат для приема на работу</span><span class="sxs-lookup"><span data-stu-id="069b6-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="069b6-169">Физическое лицо</span><span class="sxs-lookup"><span data-stu-id="069b6-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="069b6-170">Образование физического лица</span><span class="sxs-lookup"><span data-stu-id="069b6-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="069b6-171">Опыт работы физического лица</span><span class="sxs-lookup"><span data-stu-id="069b6-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="069b6-172">Адрес физического лица</span><span class="sxs-lookup"><span data-stu-id="069b6-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="069b6-173">Контакт субъекта</span><span class="sxs-lookup"><span data-stu-id="069b6-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="069b6-174">Навык физического лица</span><span class="sxs-lookup"><span data-stu-id="069b6-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="069b6-175">Уровень рейтинга</span><span class="sxs-lookup"><span data-stu-id="069b6-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="069b6-176">Сертификат физического лица</span><span class="sxs-lookup"><span data-stu-id="069b6-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="069b6-177">Тип сертификата</span><span class="sxs-lookup"><span data-stu-id="069b6-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="069b6-178">Отбор для лица</span><span class="sxs-lookup"><span data-stu-id="069b6-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="069b6-179">Типы отбора</span><span class="sxs-lookup"><span data-stu-id="069b6-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="069b6-180">Идентификационный номер физического лица</span><span class="sxs-lookup"><span data-stu-id="069b6-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="069b6-181">Наборы параметров:</span><span class="sxs-lookup"><span data-stu-id="069b6-181">Option sets:</span></span>

- [<span data-ttu-id="069b6-182">Результат интеграции кандидата</span><span class="sxs-lookup"><span data-stu-id="069b6-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- [<span data-ttu-id="069b6-183">Пусто Да Нет</span><span class="sxs-lookup"><span data-stu-id="069b6-183">Blank Yes No</span></span>](hr-admin-integration-ats-api-blank-yes-no.md)
- [<span data-ttu-id="069b6-184">Статус выполнения</span><span class="sxs-lookup"><span data-stu-id="069b6-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="069b6-185">Тип контакта</span><span class="sxs-lookup"><span data-stu-id="069b6-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="069b6-186">Базис кредита образования</span><span class="sxs-lookup"><span data-stu-id="069b6-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="069b6-187">Род</span><span class="sxs-lookup"><span data-stu-id="069b6-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="069b6-188">Семейное положение</span><span class="sxs-lookup"><span data-stu-id="069b6-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="069b6-189">Месяцы года</span><span class="sxs-lookup"><span data-stu-id="069b6-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="069b6-190">Нет Да</span><span class="sxs-lookup"><span data-stu-id="069b6-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="069b6-191">Единица измерения периода</span><span class="sxs-lookup"><span data-stu-id="069b6-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="069b6-192">Частота отбора</span><span class="sxs-lookup"><span data-stu-id="069b6-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="069b6-193">Начальная дата создаваемой периодичности отбора</span><span class="sxs-lookup"><span data-stu-id="069b6-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="069b6-194">Тип уровня навыка</span><span class="sxs-lookup"><span data-stu-id="069b6-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="069b6-195">См. также</span><span class="sxs-lookup"><span data-stu-id="069b6-195">See also</span></span>

[<span data-ttu-id="069b6-196">Найм кандидатов на должность</span><span class="sxs-lookup"><span data-stu-id="069b6-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="069b6-197">Что такое Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="069b6-197">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="069b6-198">Использование веб-API Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="069b6-198">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="069b6-199">Создание и обновление наборов параметров с помощью веб-API</span><span class="sxs-lookup"><span data-stu-id="069b6-199">Create and update option sets using the Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>