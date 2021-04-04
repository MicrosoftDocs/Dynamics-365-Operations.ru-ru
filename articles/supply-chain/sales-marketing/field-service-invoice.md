---
title: Синхронизация накладных договора в Field Service с накладными с произвольным текстом в Supply Chain Management
description: В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации накладных по соглашению в Dynamics 365 Field Service с накладными с произвольным текстом в Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 0942ce83060c186212d7f425f8dbd0a4ca2c09e7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252782"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="39333-103">Синхронизация накладных договора в Field Service с накладными с произвольным текстом в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="39333-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="39333-104">В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации накладных по соглашению в Dynamics 365 Field Service с накладными с произвольным текстом в Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="39333-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="39333-105">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="39333-105">Templates and tasks</span></span>

<span data-ttu-id="39333-106">Следующий шаблон и базовые задачи используются для выполнения синхронизации накладных по соглашению из Field Service с накладными с произвольным текстом в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="39333-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="39333-107">**Имя шаблона в интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="39333-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="39333-108">Накладные по договору (из Field Service в Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="39333-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="39333-109">**Имена задач в проекте интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="39333-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="39333-110">Заголовки накладной</span><span class="sxs-lookup"><span data-stu-id="39333-110">Invoice headers</span></span>
- <span data-ttu-id="39333-111">Строки накладной</span><span class="sxs-lookup"><span data-stu-id="39333-111">Invoice lines</span></span>

<span data-ttu-id="39333-112">Перед синхронизацией накладных по соглашению требуется следующая синхронизация:</span><span class="sxs-lookup"><span data-stu-id="39333-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="39333-113">Счета (из Sales в Supply Chain Management) — напрямую</span><span class="sxs-lookup"><span data-stu-id="39333-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="39333-114">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="39333-114">Entity set</span></span>

| <span data-ttu-id="39333-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="39333-115">Field Service</span></span>  | <span data-ttu-id="39333-116">Управление цепочкой поставок</span><span class="sxs-lookup"><span data-stu-id="39333-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="39333-117">накладные</span><span class="sxs-lookup"><span data-stu-id="39333-117">invoices</span></span>       | <span data-ttu-id="39333-118">Заголовки накладных с произвольным текстом клиента Dataverse</span><span class="sxs-lookup"><span data-stu-id="39333-118">Dataverse customer free text invoice headers</span></span> |
| <span data-ttu-id="39333-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="39333-119">invoicedetails</span></span> | <span data-ttu-id="39333-120">Строки накладных с произвольным текстом клиента Dataverse</span><span class="sxs-lookup"><span data-stu-id="39333-120">Dataverse customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="39333-121">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="39333-121">Entity flow</span></span>

<span data-ttu-id="39333-122">Накладные, которые создаются из соглашения в Field Service, можно синхронизировать с Supply Chain Management через проект интеграции данных службы Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="39333-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="39333-123">Обновления в этих накладных будут синхронизированы с накладными с произвольным текстом в Supply Chain Management, если накладные с произвольным текстом имеют состояние учета **В процессе**.</span><span class="sxs-lookup"><span data-stu-id="39333-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="39333-124">После того как накладные с произвольным текстом разносятся в Supply Chain Management и статус учета обновляется на **Завершено**, вы больше не сможете синхронизировать обновления из Field Service.</span><span class="sxs-lookup"><span data-stu-id="39333-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="39333-125">Решение Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="39333-125">Field Service CRM solution</span></span>

<span data-ttu-id="39333-126">Столбец **Имеет строки с происхождением из соглашения** был добавлен в таблицу **Накладная**.</span><span class="sxs-lookup"><span data-stu-id="39333-126">The **Has Lines With Agreement Origin** column has been added to the **Invoice** table.</span></span> <span data-ttu-id="39333-127">Этот столбец помогает гарантировать, что синхронизируются только накладные, созданные из соглашения.</span><span class="sxs-lookup"><span data-stu-id="39333-127">This column helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="39333-128">Значение равно **true**, если накладная содержит по крайней мере одну строку накладной, которая происходит из соглашения.</span><span class="sxs-lookup"><span data-stu-id="39333-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="39333-129">Столбец **Имеет происхождение из соглашения** был добавлен в таблицу **Строка накладной**.</span><span class="sxs-lookup"><span data-stu-id="39333-129">The **Has Agreement Origin** column has been added to the **Invoice Line** table.</span></span> <span data-ttu-id="39333-130">Этот столбец помогает гарантировать, что синхронизируются только строки накладной, созданные из соглашения.</span><span class="sxs-lookup"><span data-stu-id="39333-130">This column helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="39333-131">Значение равно **true**, если строка накладной происходит из соглашения.</span><span class="sxs-lookup"><span data-stu-id="39333-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="39333-132">**Дата накладной** является обязательным полем в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="39333-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="39333-133">Таким образом, этот столбец должен иметь какое-то значение в Field Service, прежде чем произойдет синхронизация.</span><span class="sxs-lookup"><span data-stu-id="39333-133">Therefore, the column must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="39333-134">Для выполнения этого условия добавлена следующая логика:</span><span class="sxs-lookup"><span data-stu-id="39333-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="39333-135">Если столбец **Дата накладной** не заполнен в таблице **Накладная** (то есть, если он не имеет никакого значения), для него задается текущая дата при добавлении строки накладной, происходящей из соглашения.</span><span class="sxs-lookup"><span data-stu-id="39333-135">If the **Invoice Date** column is blank on the **Invoice** table (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="39333-136">Пользователь может изменить столбец **Дата накладной**.</span><span class="sxs-lookup"><span data-stu-id="39333-136">The user can change the **Invoice Date** column.</span></span> <span data-ttu-id="39333-137">Тем не менее, когда пользователь пытается сохранить накладную, которая происходит из соглашения, он или она получает ошибку бизнес-процесса, если столбец **Дата накладной** не заполнен в накладной.</span><span class="sxs-lookup"><span data-stu-id="39333-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** column is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="39333-138">Необходимые условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="39333-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="39333-139">В Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="39333-139">In Supply Chain Management</span></span>

<span data-ttu-id="39333-140">Исходная накладная должна быть настроена для интеграции, чтобы отличать накладные с произвольным текстом в Supply Chain Management, которые создаются из накладных по соглашениям в Field Service.</span><span class="sxs-lookup"><span data-stu-id="39333-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="39333-141">Когда накладная имеет источник накладной типа **Интеграция накладных договора**, поле **Внешний номер накладной** будет отображаться в заголовке **Накладная заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="39333-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="39333-142">Помимо появления в заголовке накладной, информация **Внешний номер накладной** может использоваться, чтобы помочь гарантировать, что накладные, которые созданы из накладных по договору Field Service, отфильтровывались во время синхронизации накладных из Supply Chain Management в Field Service.</span><span class="sxs-lookup"><span data-stu-id="39333-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="39333-143">Выберите **Расчеты с клиентами** \> **Настройка** \> **Коды источников накладных**.</span><span class="sxs-lookup"><span data-stu-id="39333-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="39333-144">Выберите **Создать** для создания нового происхождения накладных.</span><span class="sxs-lookup"><span data-stu-id="39333-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="39333-145">В поле **Источник накладной** введите имя источника накладной, например **FS**.</span><span class="sxs-lookup"><span data-stu-id="39333-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="39333-146">В поле **Описание** введите описание, например **Накладная по договору Field Service**.</span><span class="sxs-lookup"><span data-stu-id="39333-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="39333-147">Установите флажок **Назначение типа источника**.</span><span class="sxs-lookup"><span data-stu-id="39333-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="39333-148">Задайте в поле **Тип источника накладной** значение **Интеграция накладных договора**.</span><span class="sxs-lookup"><span data-stu-id="39333-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="39333-149">Выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="39333-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="39333-150">В проекте интеграции данных</span><span class="sxs-lookup"><span data-stu-id="39333-150">In the Data Integration project</span></span>

<span data-ttu-id="39333-151">Задача: **Строки накладной**</span><span class="sxs-lookup"><span data-stu-id="39333-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="39333-152">Убедитесь, что значение по умолчанию для поля Supply Chain Management **Отображаемое значение счета ГК** обновлено в соответствии с нужным значением.</span><span class="sxs-lookup"><span data-stu-id="39333-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="39333-153">Значение шаблона по умолчанию — **401100**.</span><span class="sxs-lookup"><span data-stu-id="39333-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="39333-154">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="39333-154">Template mapping in Data integration</span></span>

<span data-ttu-id="39333-155">На следующем рисунке показано сопоставление шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="39333-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="39333-156">Накладные по договору (из Field Service в Supply Chain Management): заголовки накладных</span><span class="sxs-lookup"><span data-stu-id="39333-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="39333-157">[![Сопоставление шаблона в интеграции данных](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="39333-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="39333-158">Накладные по договору (из Field Service в Supply Chain Management): строки накладных</span><span class="sxs-lookup"><span data-stu-id="39333-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="39333-159">[![Сопоставление шаблона в интеграции данных](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="39333-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]