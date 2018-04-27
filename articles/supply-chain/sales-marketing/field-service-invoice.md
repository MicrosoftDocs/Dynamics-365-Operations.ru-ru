---
title: "Синхронизация накладных соглашения в Field Service с накладными с произвольным текстом в Finance and Operations"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации накладных по соглашению в Microsoft Dynamics 365 for Field Service с накладными с произвольным текстом в Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 1863814d6dd645da8602495858d024fbad2e7149
ms.contentlocale: ru-ru
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a><span data-ttu-id="93a36-103">Синхронизация накладных соглашения в Field Service с накладными с произвольным текстом в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="93a36-103">Synchronize agreement invoices in Field Service to free text invoices in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="93a36-104">В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации накладных по соглашению в Microsoft Dynamics 365 for Field Service с накладными с произвольным текстом в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="93a36-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Microsoft Dynamics 365 for Field Service to free text invoices in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="93a36-105">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="93a36-105">Templates and tasks</span></span>

<span data-ttu-id="93a36-106">Следующий шаблон и базовые задачи используются для выполнения синхронизации накладных по соглашению из Field Service с накладными с произвольным текстом в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="93a36-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Finance and Operations.</span></span>

<span data-ttu-id="93a36-107">**Имя шаблона в интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="93a36-107">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="93a36-108">Накладные по соглашению (из Field Service в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="93a36-108">Agreement invoices (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="93a36-109">**Имена задач в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="93a36-109">**Names of the tasks in the Data integration project:**</span></span>

- <span data-ttu-id="93a36-110">Заголовки накладной</span><span class="sxs-lookup"><span data-stu-id="93a36-110">Invoice headers</span></span>
- <span data-ttu-id="93a36-111">Строки накладной</span><span class="sxs-lookup"><span data-stu-id="93a36-111">Invoice lines</span></span>

<span data-ttu-id="93a36-112">Перед синхронизацией накладных по соглашению требуется следующая синхронизация:</span><span class="sxs-lookup"><span data-stu-id="93a36-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="93a36-113">Организации (из Sales в Fin and Ops) — напрямую</span><span class="sxs-lookup"><span data-stu-id="93a36-113">Accounts (Sales to Fin and Ops) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="93a36-114">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="93a36-114">Entity set</span></span>

| <span data-ttu-id="93a36-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="93a36-115">Field Service</span></span>  | <span data-ttu-id="93a36-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="93a36-116">Finance and Operations</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="93a36-117">накладные</span><span class="sxs-lookup"><span data-stu-id="93a36-117">invoices</span></span>       | <span data-ttu-id="93a36-118">Заголовки накладных с произвольным текстом клиента CDS</span><span class="sxs-lookup"><span data-stu-id="93a36-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="93a36-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="93a36-119">invoicedetails</span></span> | <span data-ttu-id="93a36-120">Строки накладных с произвольным текстом клиента CDS</span><span class="sxs-lookup"><span data-stu-id="93a36-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="93a36-121">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="93a36-121">Entity flow</span></span>

<span data-ttu-id="93a36-122">Накладные, которые создаются из соглашения в Field Service, можно синхронизировать с Finance and Operations через проект интеграцию данных службы Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="93a36-122">Invoices that are created from an agreement in Field Service can be synchronized to Finance and Operations via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="93a36-123">Обновления в этих накладных будут синхронизированы с накладными с произвольным текстом в Finance and Operations, если накладные с произвольным текстом имеют состояние учета **В процессе**.</span><span class="sxs-lookup"><span data-stu-id="93a36-123">Updates to these invoices will be synchronized to the free text invoices in Finance and Operations if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="93a36-124">После того как накладные с произвольным текстом разносятся в Finance and Operations и статус учета обновляется на **Завершено**, вы больше не сможете синхронизировать обновления из Field Service.</span><span class="sxs-lookup"><span data-stu-id="93a36-124">After the free text invoices are posted in Finance and Operations, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="93a36-125">Решение Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="93a36-125">Field Service CRM solution</span></span>

<span data-ttu-id="93a36-126">Поле **Имеет строки с происхождением из соглашения** было добавлено в объект **Накладная**.</span><span class="sxs-lookup"><span data-stu-id="93a36-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="93a36-127">Это поле помогает гарантировать, что синхронизируются только накладные, созданные из соглашения.</span><span class="sxs-lookup"><span data-stu-id="93a36-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="93a36-128">Значение равно **true**, если накладная содержит по крайней мере одну строку накладной, которая происходит из соглашения.</span><span class="sxs-lookup"><span data-stu-id="93a36-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="93a36-129">Поле **Имеет происхождение из соглашения** было добавлено в объект **Строка накладной**.</span><span class="sxs-lookup"><span data-stu-id="93a36-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="93a36-130">Это поле помогает гарантировать, что синхронизируются только строки накладных, созданные из соглашения.</span><span class="sxs-lookup"><span data-stu-id="93a36-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="93a36-131">Значение равно **true**, если строка накладной происходит из соглашения.</span><span class="sxs-lookup"><span data-stu-id="93a36-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="93a36-132">**Дата накладной** является обязательным полем в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="93a36-132">**Invoice date** is a mandatory field in Finance and Operations.</span></span> <span data-ttu-id="93a36-133">Таким образом, это поле должно иметь какое-то значение в Field Service, прежде чем произойдет синхронизация.</span><span class="sxs-lookup"><span data-stu-id="93a36-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="93a36-134">Для выполнения этого условия добавлена следующая логика:</span><span class="sxs-lookup"><span data-stu-id="93a36-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="93a36-135">Если поел **Дата накладной** не заполнено в объекте **Накладная** (то есть, если оно не имеет никакого значения), для него задается текущая дата при добавлении строки накладной, происходящей из соглашения.</span><span class="sxs-lookup"><span data-stu-id="93a36-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="93a36-136">Пользователь может изменить поле **Дата накладной**.</span><span class="sxs-lookup"><span data-stu-id="93a36-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="93a36-137">Тем не менее, когда пользователь пытается сохранить накладную, которая происходит из соглашения, он или она получает ошибку бизнес-процесса, если поле **Дата накладной** не заполнено в накладной.</span><span class="sxs-lookup"><span data-stu-id="93a36-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="93a36-138">Необходимые условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="93a36-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="93a36-139">В Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="93a36-139">In Finance and Operations</span></span>

<span data-ttu-id="93a36-140">Исходная накладная должна быть настроена для интеграции, чтобы отличать накладные с произвольным текстом в Finance and Operations, которые создаются из накладных по соглашениям в Field Service.</span><span class="sxs-lookup"><span data-stu-id="93a36-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Finance and Operations that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="93a36-141">Когда накладная имеет источник накладной типа **Интеграция накладных договора**, поле **Внешний номер накладной** будет отображаться в заголовке **Накладная заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="93a36-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="93a36-142">Помимо появления в заголовке накладной, информация **Внешний номер накладной** может использоваться, чтобы помочь гарантировать, что накладные, которые созданы из накладных по договору Field Service, отфильтровывались во время синхронизации накладных из Finance and Operations в Field Service.</span><span class="sxs-lookup"><span data-stu-id="93a36-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Finance and Operations to Field Service.</span></span>

1. <span data-ttu-id="93a36-143">Выберите **Расчеты с клиентами** \> **Настройка** \> **Коды источников накладных**.</span><span class="sxs-lookup"><span data-stu-id="93a36-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="93a36-144">Выберите **Создать** для создания нового происхождения накладных.</span><span class="sxs-lookup"><span data-stu-id="93a36-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="93a36-145">В поле **Источник накладной** введите имя источника накладной, например **FS**.</span><span class="sxs-lookup"><span data-stu-id="93a36-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="93a36-146">В поле **Описание** введите описание, например **Накладная по договору Field Service**.</span><span class="sxs-lookup"><span data-stu-id="93a36-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="93a36-147">Установите флажок **Назначение типа источника**.</span><span class="sxs-lookup"><span data-stu-id="93a36-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="93a36-148">Задайте в поле **Тип источника накладной** значение **Интеграция накладных договора**.</span><span class="sxs-lookup"><span data-stu-id="93a36-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="93a36-149">Выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="93a36-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="93a36-150">В проекте интеграции данных</span><span class="sxs-lookup"><span data-stu-id="93a36-150">In the Data Integration project</span></span>

<span data-ttu-id="93a36-151">Задача: **Строки накладной**</span><span class="sxs-lookup"><span data-stu-id="93a36-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="93a36-152">Убедитесь, что значение по умолчанию для поля Finance and Operations **Отображаемое значение счета ГК** обновлено в соответствии с нужным значением.</span><span class="sxs-lookup"><span data-stu-id="93a36-152">Make sure that the default value for the Finance and Operations field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="93a36-153">Значение шаблона по умолчанию — **401100**.</span><span class="sxs-lookup"><span data-stu-id="93a36-153">The default template value is **401100**.</span></span>

