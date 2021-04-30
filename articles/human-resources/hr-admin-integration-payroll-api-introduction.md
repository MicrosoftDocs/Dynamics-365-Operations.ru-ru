---
title: Введение API интеграции заработной платы
description: В этом разделе описывается API интеграции заработной платы Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61b90c566325bb8d83b09fceebc721cfb14d3fc8
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891134"
---
# <a name="payroll-integration-api-introduction"></a><span data-ttu-id="9641c-103">Введение API интеграции заработной платы</span><span class="sxs-lookup"><span data-stu-id="9641c-103">Payroll integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9641c-104">В этом документе описывается API интеграции заработной платы Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9641c-104">This document describes the Dynamics 365 Human Resources Payroll integration API.</span></span> <span data-ttu-id="9641c-105">API позволяет упростить сквозную интеграцию между модулями Human Resources и партнерскими системами расчета заработной платы.</span><span class="sxs-lookup"><span data-stu-id="9641c-105">The API enables streamlined end-to-end integrations between Human Resources and partnering payroll systems.</span></span> <span data-ttu-id="9641c-106">Интегрированный опыт начинает работать в модуле Human Resources с профилем сотрудника, зарплатой и вычетом, а также информацией о вкладе.</span><span class="sxs-lookup"><span data-stu-id="9641c-106">The integrated experience begins in Human Resources with the employee profile, salary and deduction, and contribution information.</span></span> <span data-ttu-id="9641c-107">При приеме на работу сотрудника и вводе требуемого профиля и информации о зарплате в Human Resources система заработной платы извлекает эту информацию для использования при обработке заработной платы.</span><span class="sxs-lookup"><span data-stu-id="9641c-107">When you hire an employee and enter the required profile and pay information into Human Resources, the payroll system pulls this information to use when processing payroll.</span></span> <span data-ttu-id="9641c-108">Все обновления, сделанные для сотрудника или информации о зарплате, также извлекаются для использования в последующих запусках платежей.</span><span class="sxs-lookup"><span data-stu-id="9641c-108">Any updates made to the employee or pay information are also pulled for use in later pay runs.</span></span>

![Поток интеграции зарплаты](media/hr-admin-integration-payroll-api-introduction-flow.png)

<span data-ttu-id="9641c-110">Для включения интеграции модуль Human Resources включает следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="9641c-110">To enable the integration, Human Resources includes the following components:</span></span>

- <span data-ttu-id="9641c-111">Функции для маркировки сотрудника как готового к оплате</span><span class="sxs-lookup"><span data-stu-id="9641c-111">Functionality to mark an employee as ready to pay</span></span>
- <span data-ttu-id="9641c-112">API интеграции, открывающий новые функции для интеграции приложений</span><span class="sxs-lookup"><span data-stu-id="9641c-112">An integration API opening up the new functionality to integrating applications</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="9641c-113">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="9641c-113">Microsoft Dataverse</span></span>

<span data-ttu-id="9641c-114">Этот API построен на основе Microsoft Dataverse (ранее Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="9641c-114">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="9641c-115">Все взаимодействие RESTful с этим API осуществляется с помощью веб-API Microsoft Dataverse, использующего OData.</span><span class="sxs-lookup"><span data-stu-id="9641c-115">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="9641c-116">Этот API является подмножеством веб-API Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9641c-116">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="9641c-117">Веб-API Dataverse определяет такие характеристики, как проверка подлинности, соглашения SLA, пакет, управление одновременным доступом и обработка ошибок.</span><span class="sxs-lookup"><span data-stu-id="9641c-117">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="9641c-118">Дополнительные общие сведения о веб-API Microsoft Dataverse см. в разделах:</span><span class="sxs-lookup"><span data-stu-id="9641c-118">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="9641c-119">Что такое Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="9641c-119">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="9641c-120">Использование веб-API Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="9641c-120">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="9641c-121">Руководство разработчика Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="9641c-121">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="9641c-122">В этой документации содержатся сведения и руководство разработчика по использованию веб-API Dataverse, включая следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="9641c-122">This documentation includes details and developer guidance for using the Dataverse Web API, including the following topics:</span></span>

- [<span data-ttu-id="9641c-123">Проверка подлинности в Microsoft Dataverse с веб-API</span><span class="sxs-lookup"><span data-stu-id="9641c-123">Authenticate to Microsoft Dataverse with the Web API</span></span>](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [<span data-ttu-id="9641c-124">Выполнение операций с помощью веб-API</span><span class="sxs-lookup"><span data-stu-id="9641c-124">Perform operations using the Web API</span></span>](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [<span data-ttu-id="9641c-125">Использование Postman в веб-интерфейсе API</span><span class="sxs-lookup"><span data-stu-id="9641c-125">Use Postman with the Web API</span></span>](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [<span data-ttu-id="9641c-126">Отслеживание изменений используется для синхронизации данных с внешними системами</span><span class="sxs-lookup"><span data-stu-id="9641c-126">Use change tracking to synchronize data with external systems</span></span>](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="9641c-127">Виртуальные таблицы для Human Resources в Dataverse</span><span class="sxs-lookup"><span data-stu-id="9641c-127">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="9641c-128">Конечные точки для API интеграции заработной платы используют возможности платформы виртуальных таблиц Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9641c-128">The endpoints for the Payroll integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="9641c-129">По умолчанию виртуальные таблицы и связанные с ними конечные точки API не развертываются для сред Human Resources, позволяя организациям определять, какие конечные точки OData будут доступны для данной среды.</span><span class="sxs-lookup"><span data-stu-id="9641c-129">By default, the virtual tables and their associated API endpoints aren't deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="9641c-130">Для использования API-интерфейса необходимо создать виртуальные таблицы для сущностей Human Resources для данной среды.</span><span class="sxs-lookup"><span data-stu-id="9641c-130">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span>

<span data-ttu-id="9641c-131">Сведения о создании виртуальных таблиц для API см. в разделе [Настройка виртуальных таблиц Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="9641c-131">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="9641c-132">Модель данных</span><span class="sxs-lookup"><span data-stu-id="9641c-132">Data model</span></span>

<span data-ttu-id="9641c-133">На следующей схеме показаны отношения внутри API.</span><span class="sxs-lookup"><span data-stu-id="9641c-133">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="9641c-134">У нескольких типов есть внешние ключи для других, ранее существующих сущностей в модуле Human Resources, которые здесь не иллюстрируются.</span><span class="sxs-lookup"><span data-stu-id="9641c-134">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="9641c-135">В этом документе приводятся сведения о сущностях, предназначенных специально для сценариев интеграции заработной платы.</span><span class="sxs-lookup"><span data-stu-id="9641c-135">This document provides information on entities that are specific to payroll integration scenarios.</span></span> <span data-ttu-id="9641c-136">Однако в веб-API Dataverse для Human Resources имеется множество других сущностей, которые также могут быть связаны с интеграцией.</span><span class="sxs-lookup"><span data-stu-id="9641c-136">However, there are many other entities in the Dataverse Web API for Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="9641c-137">Некоторые из этих сущностей упоминаются в отношениях внешнего ключа или свойствах навигации.</span><span class="sxs-lookup"><span data-stu-id="9641c-137">Some of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![Модель данных API интеграции заработной платы](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a><span data-ttu-id="9641c-139">Сотрудник заработной платы и связанные сущности</span><span class="sxs-lookup"><span data-stu-id="9641c-139">Payroll employee and related entities</span></span>

<span data-ttu-id="9641c-140">Объекты:</span><span class="sxs-lookup"><span data-stu-id="9641c-140">Entities:</span></span>

- [<span data-ttu-id="9641c-141">Сотрудник зарплаты</span><span class="sxs-lookup"><span data-stu-id="9641c-141">Payroll employee</span></span>](hr-admin-integration-payroll-api-payroll-employee.md)
- [<span data-ttu-id="9641c-142">Адрес работника зарплаты</span><span class="sxs-lookup"><span data-stu-id="9641c-142">Payroll worker address</span></span>](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [<span data-ttu-id="9641c-143">План фиксированной компенсации зарплаты</span><span class="sxs-lookup"><span data-stu-id="9641c-143">Payroll fixed compensation plan</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="9641c-144">Задание позиции зарплаты</span><span class="sxs-lookup"><span data-stu-id="9641c-144">Payroll position job</span></span>](hr-admin-integration-payroll-api-payroll-position-job.md)
- [<span data-ttu-id="9641c-145">Позиция зарплаты</span><span class="sxs-lookup"><span data-stu-id="9641c-145">Payroll position</span></span>](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a><span data-ttu-id="9641c-146">См. также</span><span class="sxs-lookup"><span data-stu-id="9641c-146">See also</span></span>

[<span data-ttu-id="9641c-147">Создание и проверка объектов зарплаты</span><span class="sxs-lookup"><span data-stu-id="9641c-147">Generate and review payroll entities</span></span>](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[<span data-ttu-id="9641c-148">Настройка параметров Human Resources</span><span class="sxs-lookup"><span data-stu-id="9641c-148">Configure Human Resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="9641c-149">Настройка общих параметров Human Resources</span><span class="sxs-lookup"><span data-stu-id="9641c-149">Configure Human Resources shared parameters</span></span>](hr-setup-shared-parameters.md)<br>
[<span data-ttu-id="9641c-150">Что такое Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="9641c-150">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="9641c-151">Использование веб-API Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="9641c-151">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]