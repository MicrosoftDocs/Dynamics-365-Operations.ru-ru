---
title: Синхронизация заголовков и строк накладной по продаже непосредственно из Supply Chain Management с Sales
description: В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк накладных по продаже непосредственно из Dynamics 365 Supply Chain Management в Dynamics 365 Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: fb5073fe8db0b51c4ea378cac57097e15e88bf83
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814060"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="0e876-103">Синхронизация заголовков и строк накладных по продаже непосредственно из Finance and Operations с Sales</span><span class="sxs-lookup"><span data-stu-id="0e876-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e876-104">В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк накладных по продаже непосредственно из Dynamics 365 Supply Chain Management в Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="0e876-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="0e876-105">Поток данных в решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="0e876-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="0e876-106">Решение "Перспективный клиент в наличные деньги" использует функцию интеграции данных для синхронизации данных между экземплярами Supply Chain Management и Sales.</span><span class="sxs-lookup"><span data-stu-id="0e876-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="0e876-107">Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных об организациях, контактах, продуктах, предложениях по продажам, заказах на продажу и накладных по продажам между Supply Chain Management и Sales.</span><span class="sxs-lookup"><span data-stu-id="0e876-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="0e876-108">На следующем рисунке показано, как данные синхронизируются между Supply Chain Management и Sales.</span><span class="sxs-lookup"><span data-stu-id="0e876-108">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="0e876-109">[![Поток данных в решение "Перспективный клиент в наличные деньги"](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="0e876-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="0e876-110">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="0e876-110">Templates and tasks</span></span>

<span data-ttu-id="0e876-111">Чтобы получить доступ к доступным шаблонам, откройте [Центр администрирования Power Apps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="0e876-111">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="0e876-112">Выберите **Проекты**, затем в правом верхнем углу выберите **Создать проект**, чтобы выбрать общие шаблоны.</span><span class="sxs-lookup"><span data-stu-id="0e876-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="0e876-113">Следующий шаблон и базовые задачи используются для синхронизации заголовков и строк накладных по продажам напрямую из Sales с Supply Chain Management в Sales:</span><span class="sxs-lookup"><span data-stu-id="0e876-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Supply Chain Management to Sales:</span></span>

- <span data-ttu-id="0e876-114">**Имя шаблона в интеграции данных:** "Накладные продаж (из Fin and Ops в Sales) - напрямую"</span><span class="sxs-lookup"><span data-stu-id="0e876-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="0e876-115">**Имена задач в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="0e876-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="0e876-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="0e876-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="0e876-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="0e876-117">SalesInvoiceLine</span></span>

<span data-ttu-id="0e876-118">Перед синхронизацией заголовков и строк накладных по продаже требуются следующие задачи синхронизации:</span><span class="sxs-lookup"><span data-stu-id="0e876-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="0e876-119">Продукты (из Supply Chain Management в Sales) — напрямую</span><span class="sxs-lookup"><span data-stu-id="0e876-119">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="0e876-120">Счета (из Sales в Supply Chain Management) — напрямую (если используется)</span><span class="sxs-lookup"><span data-stu-id="0e876-120">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="0e876-121">Контакты (из Sales в Supply Chain Management) — напрямую (если используется)</span><span class="sxs-lookup"><span data-stu-id="0e876-121">Contacts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="0e876-122">Заголовки и строки заказов на продажу (из Supply Chain Management в Sales) — напрямую</span><span class="sxs-lookup"><span data-stu-id="0e876-122">Sales order header and lines (Supply Chain Management to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="0e876-123">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="0e876-123">Entity set</span></span>

| <span data-ttu-id="0e876-124">Управление цепочкой поставок</span><span class="sxs-lookup"><span data-stu-id="0e876-124">Supply Chain Management</span></span>                              | <span data-ttu-id="0e876-125">Прод.</span><span class="sxs-lookup"><span data-stu-id="0e876-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="0e876-126">Заголовки счетов продажи клиентам, управляемых извне</span><span class="sxs-lookup"><span data-stu-id="0e876-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="0e876-127">Накладные</span><span class="sxs-lookup"><span data-stu-id="0e876-127">Invoices</span></span>       |
| <span data-ttu-id="0e876-128">Строки счетов продажи клиентам, управляемых извне</span><span class="sxs-lookup"><span data-stu-id="0e876-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="0e876-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="0e876-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="0e876-130">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="0e876-130">Entity flow</span></span>

<span data-ttu-id="0e876-131">Накладные по продажам создаются в Supply Chain Management и синхронизируются с Sales.</span><span class="sxs-lookup"><span data-stu-id="0e876-131">Sales invoices are created in Supply Chain Management and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="0e876-132">В настоящее время налоги, связанные с суммами в заголовке накладной по продаже, не включаются в синхронизацию из Supply Chain Management в Sales.</span><span class="sxs-lookup"><span data-stu-id="0e876-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Supply Chain Managements to Sales.</span></span> <span data-ttu-id="0e876-133">Sales не поддерживает налоговую информацию на уровне заголовка.</span><span class="sxs-lookup"><span data-stu-id="0e876-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="0e876-134">Однако налог, который относится к расходам на уровне строки, включается в синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="0e876-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="0e876-135">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="0e876-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="0e876-136">Поле **Номер накладной** было добавлено в объект **Накладная** и отображается на странице.</span><span class="sxs-lookup"><span data-stu-id="0e876-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="0e876-137">Кнопка **Создать накладную** на странице **Заказ на продажу** скрывается, потому что накладные будут создаваться в Supply Chain Management и синхронизироваться в Sales.</span><span class="sxs-lookup"><span data-stu-id="0e876-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="0e876-138">Страница **Накладная** недоступна для редактирования, потому что накладные будут синхронизироваться из Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0e876-138">The **Invoice** page can't be edited, because invoices will be synchronized from Supply Chain Management.</span></span>
- <span data-ttu-id="0e876-139">Значение **Статус заказа на продажу** меняется автоматически на **Выставлена накладная** после того как соответствующая накладная из Supply Chain Management синхронизируется в Sales.</span><span class="sxs-lookup"><span data-stu-id="0e876-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synchronized to Sales.</span></span> <span data-ttu-id="0e876-140">Кроме того, владелец заказа на продажу, из которого была создана накладная, назначается в качестве владельца накладной.</span><span class="sxs-lookup"><span data-stu-id="0e876-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="0e876-141">Таким образом, владелец заказа на продажу может просмотреть накладную.</span><span class="sxs-lookup"><span data-stu-id="0e876-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="0e876-142">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="0e876-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="0e876-143">Перед синхронизацией накладных по продажам необходимо обновить следующие параметры в системах.</span><span class="sxs-lookup"><span data-stu-id="0e876-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="0e876-144">Настройка в Sales</span><span class="sxs-lookup"><span data-stu-id="0e876-144">Setup in Sales</span></span>

<span data-ttu-id="0e876-145">Откройте **Параметры** > **Администрирование** > **Параметры системы** > **Продажи** и убедитесь, что используются следующие настройки:</span><span class="sxs-lookup"><span data-stu-id="0e876-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="0e876-146">Для параметра **Использовать системный расчет цен** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="0e876-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="0e876-147">Для параметра **Способ расчета скидки** установлено значение **Номенклатура строки**.</span><span class="sxs-lookup"><span data-stu-id="0e876-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="0e876-148">Настройка в проекте интеграции данных</span><span class="sxs-lookup"><span data-stu-id="0e876-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="0e876-149">Задача SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="0e876-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="0e876-150">Убедитесь в наличии необходимого сопоставления для **InvoiceCountryRegionId** в **BillingAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="0e876-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="0e876-151">Значение шаблона является схемой значений, где сопоставляются нескольких стран или регионов.</span><span class="sxs-lookup"><span data-stu-id="0e876-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="0e876-152">Для создания накладных в Sales требуется прайс-лист.</span><span class="sxs-lookup"><span data-stu-id="0e876-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="0e876-153">Обновите схему сопоставления для **pricelevelid.name \[имя прайс-листа\]** на прайс-лист, используемый в Sales для данной валюты.</span><span class="sxs-lookup"><span data-stu-id="0e876-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="0e876-154">Можно использовать прайс-лист по умолчанию для одной валюты.</span><span class="sxs-lookup"><span data-stu-id="0e876-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="0e876-155">Если имеются прайс-листы в нескольких валютах, можно использовать схему сопоставления.</span><span class="sxs-lookup"><span data-stu-id="0e876-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="0e876-156">Значение шаблона для **pricelevelid.name \[Имя прайс-листа\]** представляет собой схему сопоставления, основанную на валюте с USD = CRM Service USA (образец).</span><span class="sxs-lookup"><span data-stu-id="0e876-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="0e876-157">Задача SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="0e876-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="0e876-158">Убедитесь в наличии необходимого сопоставления для параметра **Единица измерения**.</span><span class="sxs-lookup"><span data-stu-id="0e876-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="0e876-159">Убедитесь, что существует требуемая схема сопоставления значений для **SalesUnitSymbol** в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0e876-159">Make sure that the required value map for **SalesUnitSymbol** in Supply Chain Management exists.</span></span>

    <span data-ttu-id="0e876-160">Значение шаблона, которое имеет сопоставление значений, определено для **SalesUnitSymbol** в **Quantity\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="0e876-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0e876-161">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="0e876-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="0e876-162">Поля **Условия оплаты**, **Условия фрахта**, **Условия поставки**, **Способ доставки** и **Режим доставки** не включены в сопоставления по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0e876-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="0e876-163">Чтобы сопоставить эти поля, необходимо настроить преобразование значений, характерное для данных в организациях, между которыми синхронизируется объект.</span><span class="sxs-lookup"><span data-stu-id="0e876-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="0e876-164">На следующем рисунке показан пример сопоставления шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="0e876-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="0e876-165">Сопоставление показывает, какие данные полей будут синхронизированы из Sales в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0e876-165">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="0e876-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="0e876-166">SalesInvoiceHeader</span></span>

![Сопоставление шаблона в интеграции данных](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="0e876-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="0e876-168">SalesInvoiceLine</span></span>

![Сопоставление шаблона в интеграции данных](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="0e876-170">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="0e876-170">Related topics</span></span>

[<span data-ttu-id="0e876-171">Продажа перспективному клиенту</span><span class="sxs-lookup"><span data-stu-id="0e876-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="0e876-172">Синхронизация организаций непосредственно из Sales с клиентами в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0e876-172">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="0e876-173">Синхронизация продуктов непосредственно из Supply Chain Management с продуктами в Sales</span><span class="sxs-lookup"><span data-stu-id="0e876-173">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="0e876-174">Синхронизация контактов непосредственно из Sales с контактами или клиентами в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0e876-174">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="0e876-175">Синхронизация заказов на продажу напрямую между Sales и Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0e876-175">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)
