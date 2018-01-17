---
title: "Синхронизация заголовков и строк счетов продажи из Finance and Operations в Sales"
description: "В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк накладных по продажам из Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition с Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 6db68236f512cc720e75c0d576ce4c49d6c87882
ms.contentlocale: ru-ru
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="68bd7-103">Синхронизация заголовков и строк счетов продажи из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="68bd7-103">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="68bd7-104">В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк накладных по продажам из Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition с Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="68bd7-104">The topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="68bd7-105">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="68bd7-105">Templates and tasks</span></span>

<span data-ttu-id="68bd7-106">Следующие шаблоны и базовые задачи используются для синхронизации заголовков и строк накладных по продажам из Finance and Operations в Sales:</span><span class="sxs-lookup"><span data-stu-id="68bd7-106">The following templates and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="68bd7-107">**Имя шаблона в интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="68bd7-107">**Name of the template in Data integration**</span></span> 

     - <span data-ttu-id="68bd7-108">Накладные по продажам (из Fin and Ops в Sales)</span><span class="sxs-lookup"><span data-stu-id="68bd7-108">Sales Invoices (Fin and Ops to Sales)</span></span>

- <span data-ttu-id="68bd7-109">**Имена задач в проекте интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="68bd7-109">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="68bd7-110">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="68bd7-110">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="68bd7-111">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="68bd7-111">SalesInvoiceLine</span></span>

<span data-ttu-id="68bd7-112">Задачи синхронизации, которые необходимо выполнить перед синхронизацией заголовков и строк накладных по продажам:</span><span class="sxs-lookup"><span data-stu-id="68bd7-112">Sync tasks required prior to Sales invoice header and lines synchronization:</span></span>
-   <span data-ttu-id="68bd7-113">Продукты (из Fin and Ops в Sales)</span><span class="sxs-lookup"><span data-stu-id="68bd7-113">Products (Fin and Ops to Sales)</span></span>
-   <span data-ttu-id="68bd7-114">Счета (из Sales в Fin and Ops) (если используются)</span><span class="sxs-lookup"><span data-stu-id="68bd7-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="68bd7-115">Контакты (из Sales в Fin and Ops) (если используются)</span><span class="sxs-lookup"><span data-stu-id="68bd7-115">Contacts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="68bd7-116">Заголовки и строки накладных по продажам (из Fin and Ops в Sales)</span><span class="sxs-lookup"><span data-stu-id="68bd7-116">Sales order header and lines (Fin and Ops to Sales)</span></span>

## <a name="entity-set"></a><span data-ttu-id="68bd7-117">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="68bd7-117">Entity set</span></span>

| <span data-ttu-id="68bd7-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="68bd7-118">Finance and Operations</span></span>                               | <span data-ttu-id="68bd7-119">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="68bd7-119">Common Data Service (CDS)</span></span>              | <span data-ttu-id="68bd7-120">Прод.</span><span class="sxs-lookup"><span data-stu-id="68bd7-120">Sales</span></span>          |
|------------------------------------------------------|------------------|----------------|
| <span data-ttu-id="68bd7-121">Заголовки счетов продажи клиентам, управляемых извне</span><span class="sxs-lookup"><span data-stu-id="68bd7-121">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="68bd7-122">SalesInvoice</span><span class="sxs-lookup"><span data-stu-id="68bd7-122">SalesInvoice</span></span>     | <span data-ttu-id="68bd7-123">Накладные</span><span class="sxs-lookup"><span data-stu-id="68bd7-123">Invoices</span></span>       |
| <span data-ttu-id="68bd7-124">Строки счетов продажи клиентам, управляемых извне</span><span class="sxs-lookup"><span data-stu-id="68bd7-124">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="68bd7-125">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="68bd7-125">SalesInvoiceLine</span></span> | <span data-ttu-id="68bd7-126">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="68bd7-126">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="68bd7-127">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="68bd7-127">Entity flow</span></span>

<span data-ttu-id="68bd7-128">Накладные по продажам создаются в Finance and Operations и синхронизируются в Sales.</span><span class="sxs-lookup"><span data-stu-id="68bd7-128">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="68bd7-129">Налоги, связанные с суммами в **заголовке накладной по продаже**, в настоящее время не включаются в синхронизацию из Finance and Operations в Sales.</span><span class="sxs-lookup"><span data-stu-id="68bd7-129">Tax related to charges on the **Sales invoice header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="68bd7-130">Это связано с тем, что в Sales не поддерживается налоговая информация на уровне заголовка.</span><span class="sxs-lookup"><span data-stu-id="68bd7-130">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="68bd7-131">Налоги, связанные с суммами на уровне строки, включаются.</span><span class="sxs-lookup"><span data-stu-id="68bd7-131">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="68bd7-132">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="68bd7-132">Prospect to cash solution for Sales</span></span>

-  <span data-ttu-id="68bd7-133">**Поле номера накладной** добавляется в объект **Накладная** и отображается на странице.</span><span class="sxs-lookup"><span data-stu-id="68bd7-133">An **Invoice number field** is added to the **Invoice** entity and displayed on the page.</span></span>
 
-  <span data-ttu-id="68bd7-134">Кнопка **Создать накладную** на странице **Заказ на продажу** скрывается, потому что накладные будут создаваться в Finance and Operations и синхронизироваться в Sales.</span><span class="sxs-lookup"><span data-stu-id="68bd7-134">The **Create invoice** button on the **Sales order** page is hidden because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="68bd7-135">Страница **Накладная** недоступна для редактирования, потому что накладные будут синхронизироваться из Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="68bd7-135">The **Invoice** page is non-editable because invoices will be synced from Finance and Operations.</span></span>
 
-  <span data-ttu-id="68bd7-136">**Статус заказа на продажу** меняется автоматически на **Выставлена накладная** после того как соответствующая накладная из Finance and Operations синхронизируется в Sales.</span><span class="sxs-lookup"><span data-stu-id="68bd7-136">The **Sales order status** changes automatically to **Invoiced** when the related invoice from Finance and Operations has been  synchronized to Sales.</span></span> <span data-ttu-id="68bd7-137">Кроме того владелец заказа на продажу, из которого была создана накладная, назначается в качестве владельца накладной.</span><span class="sxs-lookup"><span data-stu-id="68bd7-137">Also, the owner of the sales order from which the invoice was created is assigned as the owner of the invoice.</span></span> <span data-ttu-id="68bd7-138">Это дает владельцу заказа на продажу возможность просматривать накладную.</span><span class="sxs-lookup"><span data-stu-id="68bd7-138">This gives the owner of the sales order the ability to view the invoice.</span></span>
 
## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="68bd7-139">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="68bd7-139">Preconditions and mapping setup</span></span>

<span data-ttu-id="68bd7-140">Перед синхронизацией накладных по продажам необходимо задать в системах следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="68bd7-140">Before synchronizing sales invoices, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="68bd7-141">Настройка в Sales</span><span class="sxs-lookup"><span data-stu-id="68bd7-141">Setup in Sales</span></span>

- <span data-ttu-id="68bd7-142">Выбрав **Параметры** > **Администрирование** > **Параметры системы** > **Продажи** убедитесь, что для параметра **Использовать системный расчет цен** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="68bd7-142">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="68bd7-143">Выбрав **Параметры** > **Администрирование** > **Параметры системы** > **Продажи** убедитесь, что для параметра **Способ расчета скидки** установлено значение **Позиция строки**.</span><span class="sxs-lookup"><span data-stu-id="68bd7-143">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="68bd7-144">Настройка в проекте интеграции данных</span><span class="sxs-lookup"><span data-stu-id="68bd7-144">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="68bd7-145">Задача SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="68bd7-145">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="68bd7-146">Обновите сопоставление для **кода организации CDS** в **Источник** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="68bd7-146">Update the mapping for **CDS Organization ID** in **Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="68bd7-147">Значение шаблона по умолчанию для **SalesOrder_Organization_OrganizationId** — ORG001.</span><span class="sxs-lookup"><span data-stu-id="68bd7-147">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="68bd7-148">Значение шаблона по умолчанию для **Account_Organization_OrganizationId** — ORG001.</span><span class="sxs-lookup"><span data-stu-id="68bd7-148">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="68bd7-149">Значение шаблона по умолчанию для **Organization_OrganizationId** — ORG001.</span><span class="sxs-lookup"><span data-stu-id="68bd7-149">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="68bd7-150">Убедитесь, что в **Источник** > **CDS для InvoiceCountryRegionId** существует необходимое сопоставление с **BillingAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="68bd7-150">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span></span>

    -  <span data-ttu-id="68bd7-151">Значение шаблона — **ValueMap** с количеством сопоставленных стран.</span><span class="sxs-lookup"><span data-stu-id="68bd7-151">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="68bd7-152">Для создания накладных в Sales требуется **прайс-лист**.</span><span class="sxs-lookup"><span data-stu-id="68bd7-152">**Price list** is required to create invoices in Sales.</span></span> <span data-ttu-id="68bd7-153">Измените **ValueMap** в **CDS** > **Место назначения для pricelevelid.name [имя прайс-листа]** на **прайс-лист**, используемый в Sales для данной валюты.</span><span class="sxs-lookup"><span data-stu-id="68bd7-153">Update the **ValueMap** in **CDS** > **Destination for pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="68bd7-154">Можно использовать либо **прайс-лист** по умолчанию для одной валюты, либо **ValueMap** если у вас есть **прайс-листы** в нескольких валютах.</span><span class="sxs-lookup"><span data-stu-id="68bd7-154">You can either use the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>

    -  <span data-ttu-id="68bd7-155">Значение шаблона для **pricelevelid.name [имя прайс-листа]** — это **ValueMap** в зависимости от **валюты**.</span><span class="sxs-lookup"><span data-stu-id="68bd7-155">Template value for **pricelevelid.name [Price List Name]** is **ValueMap** based on **Currency**.</span></span>
    -  <span data-ttu-id="68bd7-156">usd: CRM Service USA (sample).</span><span class="sxs-lookup"><span data-stu-id="68bd7-156">usd: CRM Service USA (sample).</span></span> 

#### <a name="salesinvoiceline-task"></a><span data-ttu-id="68bd7-157">Задача SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="68bd7-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="68bd7-158">Убедитесь, что в **Источник** > **CDS** существует необходимое сопоставление для единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="68bd7-158">Ensure that the needed mapping exists in **Source** > **CDS for Unit of measure**.</span></span>

- <span data-ttu-id="68bd7-159">Убедитесь, что в **Источник** > **Сопоставление CDS** существует необходимая **ValueMap** для **SalesUnitSymbol** в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="68bd7-159">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span> 
    
    - <span data-ttu-id="68bd7-160">Значение шаблона с **ValueMap** определено для **SalesUnitSymbol с Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="68bd7-160">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>
    
-  <span data-ttu-id="68bd7-161">Обновите сопоставление для кода организации CDS **Источник** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="68bd7-161">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="68bd7-162">Значение шаблона по умолчанию для **SalesInvoicer_Organization_OrganizationId** — ORG001.</span><span class="sxs-lookup"><span data-stu-id="68bd7-162">Default template value for **SalesInvoicer_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="68bd7-163">Значение шаблона по умолчанию для **Product_Organization_OrganizationId** — ORG001.</span><span class="sxs-lookup"><span data-stu-id="68bd7-163">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>
 
## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="68bd7-164">Сопоставление шаблона в интеграторе данных</span><span class="sxs-lookup"><span data-stu-id="68bd7-164">Template mapping in Data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="68bd7-165">Поля **Условия оплаты**, **Условия фрахта**, **Условия поставки**, **Способ доставки** и **Режим доставки** не входят в сопоставления по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="68bd7-165">**Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** are not part of the default mappings.</span></span> <span data-ttu-id="68bd7-166">Для сопоставления этих полей необходимо настроить преобразование значений, характерное для данных в организациях, между которыми синхронизируется объект.</span><span class="sxs-lookup"><span data-stu-id="68bd7-166">Mapping of these fields requires value mapping to be set up, which is specific to the data in the organizations between which the entity is synchronized.</span></span>

<span data-ttu-id="68bd7-167">На следующем рисунке показан пример сопоставления шаблона в интеграторе данных.</span><span class="sxs-lookup"><span data-stu-id="68bd7-167">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Сопоставление шаблона в интеграторе данных](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Сопоставление шаблона в интеграторе данных](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Сопоставление шаблона в интеграторе данных](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Сопоставление шаблона в интеграторе данных](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="68bd7-172">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="68bd7-172">Related topics</span></span>

[<span data-ttu-id="68bd7-173">Синхронизация продуктов из Finance and Operations с продуктами в Sales</span><span class="sxs-lookup"><span data-stu-id="68bd7-173">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="68bd7-174">Синхронизация организаций из Finance and Operations с клиентами в Sales</span><span class="sxs-lookup"><span data-stu-id="68bd7-174">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="68bd7-175">Синхронизация контактов из Finance and Operations с контактами в Sales</span><span class="sxs-lookup"><span data-stu-id="68bd7-175">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="68bd7-176">Синхронизация заголовков и строк предложений по продажам из Sales с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="68bd7-176">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="68bd7-177">Синхронизация заголовков и строк заказов на продажу из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="68bd7-177">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)


