---
title: "Синхронизация заголовков и строк предложений по продажам из Sales с Finance and Operations"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк предложений по продажам из Microsoft Dynamics 365 for Sales с Microsoft Dynamics 365 for Finance and Operations, выпуск Enterprise."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 172a3da1b6d90a25ea9ebd14265e70e4a6f9bd70
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="242f9-103">Синхронизация заголовков и строк предложений по продажам из Sales с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="242f9-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="242f9-104">Перед использованием решения "Перспективный клиент в наличные деньги" ознакомьтесь с разделом [Интеграция данных Dynamics 365](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="242f9-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="242f9-105">В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк предложений по продажам из Microsoft Dynamics 365 for Sales (Sales) с Microsoft Dynamics 365 for Finance and Operations , выпуск Enterprise, (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="242f9-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="242f9-106">Шаблон и задачи</span><span class="sxs-lookup"><span data-stu-id="242f9-106">Template and tasks</span></span>

<span data-ttu-id="242f9-107">Следующие шаблоны и базовые задачи используются для синхронизации заголовков и строк предложений по продажам из Sales с Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="242f9-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="242f9-108">**Имя шаблона:** предложения по продажам (Sales в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="242f9-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="242f9-109">**Имена задач в проекте:**</span><span class="sxs-lookup"><span data-stu-id="242f9-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="242f9-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="242f9-110">QuoteHeader</span></span>
    - <span data-ttu-id="242f9-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="242f9-111">QuoteLine</span></span>

<span data-ttu-id="242f9-112">Перед синхронизацией заголовков и строк предложений по продажам требуются следующие задачи синхронизации:</span><span class="sxs-lookup"><span data-stu-id="242f9-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="242f9-113">Товары</span><span class="sxs-lookup"><span data-stu-id="242f9-113">Products</span></span>
- <span data-ttu-id="242f9-114">Счета (если используются)</span><span class="sxs-lookup"><span data-stu-id="242f9-114">Accounts (if used)</span></span>
- <span data-ttu-id="242f9-115">Контакты (если используются)</span><span class="sxs-lookup"><span data-stu-id="242f9-115">Contacts (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="242f9-116">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="242f9-116">Entity set</span></span>

| <span data-ttu-id="242f9-117">Прод.</span><span class="sxs-lookup"><span data-stu-id="242f9-117">Sales</span></span>        | <span data-ttu-id="242f9-118">CDS</span><span class="sxs-lookup"><span data-stu-id="242f9-118">CDS</span></span>           | <span data-ttu-id="242f9-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="242f9-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="242f9-120">Цитаты</span><span class="sxs-lookup"><span data-stu-id="242f9-120">Quotes</span></span>       | <span data-ttu-id="242f9-121">Предложение</span><span class="sxs-lookup"><span data-stu-id="242f9-121">Quotation</span></span>     | <span data-ttu-id="242f9-122">Заголовки предложений по продаже</span><span class="sxs-lookup"><span data-stu-id="242f9-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="242f9-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="242f9-123">QuoteDetails</span></span> | <span data-ttu-id="242f9-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="242f9-124">QuotationLine</span></span> | <span data-ttu-id="242f9-125">Строки предложения по продаже CDS</span><span class="sxs-lookup"><span data-stu-id="242f9-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="242f9-126">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="242f9-126">Entity flow</span></span>

<span data-ttu-id="242f9-127">Предложения по продажам создаются в Sales и синхронизируются с Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="242f9-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="242f9-128">Предложения по продажам из Sales синхронизируются, только если выполняются следующие условия:</span><span class="sxs-lookup"><span data-stu-id="242f9-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="242f9-129">Все продукты в строках предложения по продаже управляются извне.</span><span class="sxs-lookup"><span data-stu-id="242f9-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="242f9-130">Предложение по продаже активно или активировано.</span><span class="sxs-lookup"><span data-stu-id="242f9-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="242f9-131">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="242f9-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="242f9-132">Добавлено поле **Имеет только управляемые извне продукты** к объекту "Предложение по продаже" для постоянного отслеживания того, состоит ли предложение по продаже полностью из управляемых извне продуктов.</span><span class="sxs-lookup"><span data-stu-id="242f9-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="242f9-133">Если предложение по продаже содержит только управляемые извне продукты, продукты управляются в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="242f9-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="242f9-134">Это поведение помогает гарантировать, что вы не будете пытаться синхронизировать строки предложения по продаже с продуктами, которые неизвестны для Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="242f9-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="242f9-135">Все продукты и строки в предложении обновляются сведениями **Имеет только управляемые извне продукты** из заголовка предложения.</span><span class="sxs-lookup"><span data-stu-id="242f9-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="242f9-136">Эти сведения можно найти в поле **Предложения имеет только управляемые извне продукты** в объекте строки предложения.</span><span class="sxs-lookup"><span data-stu-id="242f9-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="242f9-137">Поля **Скидка**, **Расходы** и **Налог** управляются сложной настройкой в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="242f9-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="242f9-138">Эта настройка не поддерживает сопоставление интеграции в данный момент.</span><span class="sxs-lookup"><span data-stu-id="242f9-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="242f9-139">В текущем дизайне поля **Цена**, **Скидка**, **Расходы** и **Налог** управляются и обрабатываются в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="242f9-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="242f9-140">В Sales решение делает следующие поля доступными только для чтения, поскольку значения не синхронизируются с Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="242f9-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="242f9-141">**Доступные только для чтения поля в заголовке предложения по продаже:** "% скидки", "Скидка", "Сумма транспортировки"</span><span class="sxs-lookup"><span data-stu-id="242f9-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="242f9-142">**Доступные только для чтения поля в строках предложения по продаже:** "Налог"</span><span class="sxs-lookup"><span data-stu-id="242f9-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="242f9-143">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="242f9-143">Preconditions and mapping setup</span></span>

- <span data-ttu-id="242f9-144">Перед синхронизацией предложений по продажам в Sales перейдите в раздел **Параметры** &gt; **Администрирование** &gt; **Параметры системы** &gt; **Продажи** и убедитесь, что в поле **Метод расчета скидки** установлено значение **На единицу**.</span><span class="sxs-lookup"><span data-stu-id="242f9-144">Before you synchronize sales quotations, in Sales, go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="242f9-145">Этот параметр помогает гарантировать соответствие скидки номенклатуры строки из Sales с параметром в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="242f9-145">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="242f9-146">В противном случае скидка будет неправильной в Finance and Operations, поскольку Finance and Operations будет считывать скидку как скидку на единицу, даже если это скидка по строке в Sales.</span><span class="sxs-lookup"><span data-stu-id="242f9-146">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>
- <span data-ttu-id="242f9-147">В Finance and Operations перейдите в раздел **Расчеты с клиентами** &gt; **Настройка** &gt; **Параметры расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="242f9-147">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="242f9-148">На вкладке **Номерная серия** выберите номерную серию для предложений по продажам, а затем щелкните **Просмотр сведений**.</span><span class="sxs-lookup"><span data-stu-id="242f9-148">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="242f9-149">Затем в разделе **Общая Настройка** установите в поле **Вручную** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="242f9-149">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="242f9-150">В Finance and Operations перейдите в раздел **Расчеты с клиентами** &gt; **Настройка** &gt; **Параметры расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="242f9-150">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="242f9-151">Затем на вкладке **Отгрузки** установите для поля **Контроль даты поставки** значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="242f9-151">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="242f9-152">Этот параметр позволяет избежать сбоя синхронизации предложений по продажам.</span><span class="sxs-lookup"><span data-stu-id="242f9-152">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="242f9-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="242f9-153">QuoteHeader</span></span>

- <span data-ttu-id="242f9-154">Поле **Запрошенная дата доставки** является обязательным в Finance and Operations, и синхронизация завершится с ошибкой, если оставить его пустым.</span><span class="sxs-lookup"><span data-stu-id="242f9-154">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="242f9-155">Чтобы предотвратить эту проблему, если это поле пусто, используется дата по умолчанию из раздела **Источник &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="242f9-155">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="242f9-156">Дата должна быть обновлена до нужного значения.</span><span class="sxs-lookup"><span data-stu-id="242f9-156">The date should be updated to a preferred value.</span></span> <span data-ttu-id="242f9-157">В настоящее время невозможно ввести значение, такое как **Сегодня**, для представления текущей даты.</span><span class="sxs-lookup"><span data-stu-id="242f9-157">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="242f9-158">Необходимо ввести определенную дату.</span><span class="sxs-lookup"><span data-stu-id="242f9-158">You must enter a specific date.</span></span> <span data-ttu-id="242f9-159">Значение шаблона по умолчанию для поля **Запрошенная дата доставки** — **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="242f9-159">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="242f9-160">Поле **Код страны/региона адреса** является обязательным в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="242f9-160">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="242f9-161">Чтобы предотвратить ошибки синхронизации, можно указать значение по умолчанию, которое используется, если это поле пусто в Sales.</span><span class="sxs-lookup"><span data-stu-id="242f9-161">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="242f9-162">Это значение по умолчанию также является полезным, поскольку вам не нужно вручную вводить значение в поле **Страна/регион** для локальных адресов.</span><span class="sxs-lookup"><span data-stu-id="242f9-162">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="242f9-163">Не существует значения шаблона по умолчанию для **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="242f9-163">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="242f9-164">Обновите сопоставление для полей **Код организации CDS** в разделе **Источник &gt; CDS**, чтобы оно соответствовало значению **Организации CDS** в объекте "Организация":</span><span class="sxs-lookup"><span data-stu-id="242f9-164">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="242f9-165">Значение шаблона по умолчанию для **Organization_OrganizationId** — **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="242f9-165">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="242f9-166">Значение шаблона по умолчанию для **Account_Organization_OrganizationId** — **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="242f9-166">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="242f9-167">Значение шаблона по умолчанию для **InvoiceAccount_OrganizationId** — **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="242f9-167">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

### <a name="quoteline"></a><span data-ttu-id="242f9-168">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="242f9-168">QuoteLine</span></span>

- <span data-ttu-id="242f9-169">Обновите сопоставление для полей **Код организации CDS** в разделе **Источник &gt; CDS**, чтобы оно соответствовало значению **Организации CDS** в объекте "Организация":</span><span class="sxs-lookup"><span data-stu-id="242f9-169">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="242f9-170">Значение шаблона по умолчанию для **Organization_OrganizationId** — **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="242f9-170">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="242f9-171">Значение шаблона по умолчанию для **Product_Organization_Organization_OrganizationId** — **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="242f9-171">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="242f9-172">Значение шаблона по умолчанию для **Quotation_Organization_Organization_OrganizationId** — **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="242f9-172">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="242f9-173">Поле **Запрошенная дата доставки** является обязательным в Finance and Operations, и синхронизация завершится с ошибкой, если оставить его пустым.</span><span class="sxs-lookup"><span data-stu-id="242f9-173">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="242f9-174">Чтобы предотвратить эту проблему, если это поле пусто, используется дата по умолчанию из раздела **Источник &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="242f9-174">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="242f9-175">Дата должна быть обновлена до нужного значения.</span><span class="sxs-lookup"><span data-stu-id="242f9-175">The date should be updated to a preferred value.</span></span> <span data-ttu-id="242f9-176">В настоящее время невозможно ввести значение, такое как **Сегодня**, для представления текущей даты.</span><span class="sxs-lookup"><span data-stu-id="242f9-176">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="242f9-177">Необходимо ввести определенную дату.</span><span class="sxs-lookup"><span data-stu-id="242f9-177">You must enter a specific date.</span></span> <span data-ttu-id="242f9-178">Значение шаблона по умолчанию для поля **Запрошенная дата доставки** — **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="242f9-178">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="242f9-179">Можно добавить следующие сопоставления из раздела **CDS &gt; Назначение** для гарантии того, что строки этого предложения будут импортироваться в Finance and Operations, если отсутствует информация по умолчанию от клиента или продукта:</span><span class="sxs-lookup"><span data-stu-id="242f9-179">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="242f9-180">**SiteId** — сайт необходим для создания предложений и строк заказов на продажу в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="242f9-180">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="242f9-181">Не существует значения шаблона по умолчанию для **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="242f9-181">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="242f9-182">**WarehouseId** — склад необходим для обработки предложений и строк заказов на продажу в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="242f9-182">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="242f9-183">Не существует значения шаблона по умолчанию для **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="242f9-183">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="242f9-184">Убедитесь, что требуемое соответствие значений для единицы измерения продажи в Finance and Operations существует в сопоставлении **CDS &gt; Назначение** для **Quantity_UOM** как **SALESUNITSYMBOL**.</span><span class="sxs-lookup"><span data-stu-id="242f9-184">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="242f9-185">Сопоставление шаблона в интеграторе данных</span><span class="sxs-lookup"><span data-stu-id="242f9-185">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="242f9-186">Поля **Скидка**, **Расходы** и **Налог** управляются сложной настройкой в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="242f9-186">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="242f9-187">Эта настройка не поддерживает сопоставление интеграции в данный момент.</span><span class="sxs-lookup"><span data-stu-id="242f9-187">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="242f9-188">В текущем дизайне поля **Цена**, **Скидка**, **Расходы** и **Налог** обрабатываются в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="242f9-188">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="242f9-189">Поля **Условия оплаты**, **Условия фрахта**, **Условия поставки**, **Способ доставки** и **Режим доставки** не являются частью сопоставлений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="242f9-189">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="242f9-190">Чтобы сопоставить эти поля, необходимо настроить преобразование значений, характерное для данных в организациях, между которыми синхронизируется объект.</span><span class="sxs-lookup"><span data-stu-id="242f9-190">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="242f9-191">На следующем рисунке показан пример сопоставления шаблона в интеграторе данных.</span><span class="sxs-lookup"><span data-stu-id="242f9-191">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="242f9-192">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="242f9-192">QuoteHeader</span></span>

![Сопоставление шаблона в интеграторе данных](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Сопоставление шаблона в интеграторе данных](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="242f9-195">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="242f9-195">QuoteLine</span></span>

![Сопоставление шаблона в интеграторе данных](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Сопоставление шаблона в интеграторе данных](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="242f9-198">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="242f9-198">Related topics</span></span>

[<span data-ttu-id="242f9-199">Синхронизация продуктов из Finance and Operations с продуктами в Sales</span><span class="sxs-lookup"><span data-stu-id="242f9-199">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="242f9-200">Синхронизация контактов из Sales с клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="242f9-200">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="242f9-201">Синхронизация контактов из Sales с контактами или клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="242f9-201">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



