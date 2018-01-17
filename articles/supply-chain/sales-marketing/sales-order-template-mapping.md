---
title: "Синхронизация заголовков и строк заказов на продажу из Finance and Operations в Sales"
description: "В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк заказов на продажу из Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition с Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.openlocfilehash: d7e4c435a3344f6a5d66e1889b633d80cda085eb
ms.contentlocale: ru-ru
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="878d1-103">Синхронизация заголовков и строк заказов на продажу из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="878d1-103">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="878d1-104">В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк заказов на продажу из Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition с Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="878d1-104">The topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="878d1-105">Шаблон и задачи</span><span class="sxs-lookup"><span data-stu-id="878d1-105">Template and tasks</span></span>

<span data-ttu-id="878d1-106">Следующие шаблоны и базовые задачи используются для синхронизации заголовков и строк заказов на продажу из Finance and Operations в Sales:</span><span class="sxs-lookup"><span data-stu-id="878d1-106">The following templates and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="878d1-107">**Имя шаблона в интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="878d1-107">**Name of template in Data integration**</span></span> 

    - <span data-ttu-id="878d1-108">Заказы на продажу (из Fin and Ops в Sales)</span><span class="sxs-lookup"><span data-stu-id="878d1-108">Sales Orders (Fin and Ops to Sales)</span></span>
    
- <span data-ttu-id="878d1-109">**Имена задач в проекте интеграции данных**</span><span class="sxs-lookup"><span data-stu-id="878d1-109">**Names of tasks in Data integration project**</span></span>

    - <span data-ttu-id="878d1-110">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="878d1-110">OrderHeader</span></span>
    - <span data-ttu-id="878d1-111">OrderLine</span><span class="sxs-lookup"><span data-stu-id="878d1-111">OrderLine</span></span>

<span data-ttu-id="878d1-112">Задачи синхронизации, которые необходимо выполнить перед синхронизацией заголовков и строк накладных по продажам:</span><span class="sxs-lookup"><span data-stu-id="878d1-112">Sync tasks required prior to Sales invoice header and lines sync:</span></span>

- <span data-ttu-id="878d1-113">Продукты (из Fin and Ops в Sales)</span><span class="sxs-lookup"><span data-stu-id="878d1-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="878d1-114">Счета (из Sales в Fin and Ops) (если используются)</span><span class="sxs-lookup"><span data-stu-id="878d1-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="878d1-115">Из контактов в клиенты (из Sales в Fin and Ops) (если используются)</span><span class="sxs-lookup"><span data-stu-id="878d1-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="878d1-116">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="878d1-116">Entity set</span></span>

| <span data-ttu-id="878d1-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="878d1-117">Finance and Operations</span></span> |    <span data-ttu-id="878d1-118">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="878d1-118">Common Data Service (CDS)</span></span>         |     <span data-ttu-id="878d1-119">Прод.</span><span class="sxs-lookup"><span data-stu-id="878d1-119">Sales</span></span>      |
|------------------------|----------------|----------------|
| <span data-ttu-id="878d1-120">Заголовки заказов на продажу CDS</span><span class="sxs-lookup"><span data-stu-id="878d1-120">CDS sales order headers</span></span>| <span data-ttu-id="878d1-121">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="878d1-121">SalesOrder</span></span>     | <span data-ttu-id="878d1-122">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="878d1-122">SalesOrders</span></span> |
| <span data-ttu-id="878d1-123">Строки заказа на продажу CDS</span><span class="sxs-lookup"><span data-stu-id="878d1-123">CDS sales order lines</span></span>  | <span data-ttu-id="878d1-124">SalesOrderLine</span><span class="sxs-lookup"><span data-stu-id="878d1-124">SalesOrderLine</span></span> | <span data-ttu-id="878d1-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="878d1-125">SalesOrderDetails</span></span>|

## <a name="entity-flow"></a><span data-ttu-id="878d1-126">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="878d1-126">Entity flow</span></span>

<span data-ttu-id="878d1-127">Заказы на продажу создаются в Finance and Operations и синхронизируются в Sales.</span><span class="sxs-lookup"><span data-stu-id="878d1-127">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="878d1-128">Фильтры в шаблоне позволяют гарантировать, что в синхронизацию включаются только необходимые заказы на продажу:</span><span class="sxs-lookup"><span data-stu-id="878d1-128">Filters in the template ensure that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="878d1-129">И оформление заказа, и выставление накладной клиенту, указанному в заказе на поставку, которые берут начало в Sales, будут включаться в синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="878d1-129">Both ordering and invoicing customer on the sales order that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="878d1-130">В Finance and Operations поля **OrderingCustomerIsExternallyMaintained** и **InvoiceCustomerIsExternallyMaintained** используются для отслеживания синхронизации в информационных объектах.</span><span class="sxs-lookup"><span data-stu-id="878d1-130">In Finance and Operations, the fields **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** are used to track the synchronization in the data entities.</span></span>

- <span data-ttu-id="878d1-131">**Заказ на продажу** в Finance and Operations должен быть подтвержден.</span><span class="sxs-lookup"><span data-stu-id="878d1-131">The **Sales order** in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="878d1-132">С Sales синхронизируются только подтвержденные заказы на продажу или заказы на продажу с более высоким статусом обработки, например "Отгружено" или "Выставлена накладная".</span><span class="sxs-lookup"><span data-stu-id="878d1-132">Only the confirmed sales orders or sales orders with higher processing status, for example, Shipped or Invoiced status, are synchronized to Sales.</span></span>

- <span data-ttu-id="878d1-133">После создания или изменения заказа на продажу необходимо выполнить в Finance and Operations пакетное задание **Рассчитать итоги продаж**.</span><span class="sxs-lookup"><span data-stu-id="878d1-133">After creating or modifying a sales order, the batch job **Calculate sales totals** in Finance and Operations must be executed.</span></span> <span data-ttu-id="878d1-134">Синхронизироваться в CDS и Sales будут только заказы на продажу с рассчитанными итогами продаж.</span><span class="sxs-lookup"><span data-stu-id="878d1-134">Only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="878d1-135">Налоги, связанные с суммами в **заголовке заказа на продажу**, в настоящее время не включаются в синхронизацию из Finance and Operations в Sales.</span><span class="sxs-lookup"><span data-stu-id="878d1-135">Tax related to charges on the **Sales order header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="878d1-136">Это связано с тем, что в Sales не поддерживается налоговая информация на уровне заголовка.</span><span class="sxs-lookup"><span data-stu-id="878d1-136">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="878d1-137">Налоги, связанные с суммами на уровне строки, включаются.</span><span class="sxs-lookup"><span data-stu-id="878d1-137">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="878d1-138">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="878d1-138">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="878d1-139">В объект **Заказ** добавляются новые поля и отображаются на странице:</span><span class="sxs-lookup"><span data-stu-id="878d1-139">New fields are added to the **Order** entity and displayed on the page:</span></span>

- <span data-ttu-id="878d1-140">**Хранится во внешней системе** — имеет значение **Да**, когда заказ поступает из Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="878d1-140">**Is Maintained Externally** - Set to **Yes** when the order is coming from Finance and Operations.</span></span>

- <span data-ttu-id="878d1-141">**Состояние обработки** — используется для отображения статуса обработки заказа в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="878d1-141">**Processing status** - Used to show the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="878d1-142">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="878d1-142">Values are:</span></span>

    - <span data-ttu-id="878d1-143">Активен</span><span class="sxs-lookup"><span data-stu-id="878d1-143">Active</span></span>
    - <span data-ttu-id="878d1-144">Подтверждено</span><span class="sxs-lookup"><span data-stu-id="878d1-144">Confirmed</span></span>
    - <span data-ttu-id="878d1-145">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="878d1-145">Packing Slip</span></span>
    - <span data-ttu-id="878d1-146">Выставлено накладных</span><span class="sxs-lookup"><span data-stu-id="878d1-146">Invoiced</span></span>
    - <span data-ttu-id="878d1-147">Скомплектовано</span><span class="sxs-lookup"><span data-stu-id="878d1-147">Picked</span></span>
    - <span data-ttu-id="878d1-148">Частично скомплектовано</span><span class="sxs-lookup"><span data-stu-id="878d1-148">Partially Picked</span></span>
    - <span data-ttu-id="878d1-149">Частично упаковано</span><span class="sxs-lookup"><span data-stu-id="878d1-149">Partially Packed</span></span>
    - <span data-ttu-id="878d1-150">Отгружено</span><span class="sxs-lookup"><span data-stu-id="878d1-150">Shipped</span></span>
    - <span data-ttu-id="878d1-151">Частично отправлено</span><span class="sxs-lookup"><span data-stu-id="878d1-151">Partially Shipped</span></span>
    - <span data-ttu-id="878d1-152">Частично выставлен счет</span><span class="sxs-lookup"><span data-stu-id="878d1-152">Partially Invoiced</span></span>
    - <span data-ttu-id="878d1-153">Отменено</span><span class="sxs-lookup"><span data-stu-id="878d1-153">Cancelled</span></span>

<span data-ttu-id="878d1-154">Параметр **Все продукты хранятся во внешней системе** используется в других сценариях с заказами на продажу (при синхронизации из Sales в Finance and Operation sync) для отслеживания того, состоит ли заказ на продажу исключительно из **продуктов, хранящихся во внешней системе** (в этом случае ведение продуктов осуществляется в Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="878d1-154">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (from Sales to Finance and Operation sync) to consistently keep track of whether the sales order is made up entirely of **Externally Maintained Products**, in which case products are maintained in Finance and Operations.</span></span> <span data-ttu-id="878d1-155">Это гарантирует, что вы не будете пытаться синхронизировать строки заказов на продажу с продуктами, которые неизвестны Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="878d1-155">This ensures that you don't try to sync sales order lines with products that are unknown to Finance and Operations.</span></span>
 
<span data-ttu-id="878d1-156">Кнопки **Создать накладную**, **Отменить заказ**, **Пересчитать**, **Получить продукты** и **Искать адрес** на странице **Заказ на продажу** для продуктов, хранящихся во внешней системе, скрываются, потому что накладные будут создаваться в Finance and Operations и синхронизироваться в Sales.</span><span class="sxs-lookup"><span data-stu-id="878d1-156">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products** and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="878d1-157">Страница заказа недоступна для редактирования, потому что информация заказа на продажу будет синхронизироваться из Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="878d1-157">The order page is non-editable because sales order information will be synced from Finance and Operations.</span></span>
 
<span data-ttu-id="878d1-158">**Статус заказа на продажу** будет оставаться активным, чтобы гарантировать, что изменения из Finance and Operations будут передаваться в **заказ на продажу** в Sales.</span><span class="sxs-lookup"><span data-stu-id="878d1-158">The **Sales order status** will remain active to ensure that changes from Finance and Operations can flow to the **Sales order** in Sales.</span></span> <span data-ttu-id="878d1-159">Это обеспечивается установкой **Statecode [Статус]** по умолчанию в значение **Active** в проекте интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="878d1-159">This is controlled by setting the default **Statecode [Status]** to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="878d1-160">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="878d1-160">Preconditions and mapping setup</span></span> 

<span data-ttu-id="878d1-161">Перед синхронизацией заказов на продажу необходимо задать в системах следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="878d1-161">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="878d1-162">Настройка в Sales</span><span class="sxs-lookup"><span data-stu-id="878d1-162">Setup in Sales</span></span>

- <span data-ttu-id="878d1-163">Убедитесь в наличии разрешений для группы, которой назначен пользователь (из вашего **набора подключений** Sales).</span><span class="sxs-lookup"><span data-stu-id="878d1-163">Ensure permissions for the team that the user (from your Sales **Connection set**) is assigned to.</span></span> <span data-ttu-id="878d1-164">Если вы используете демонстрационные данные, обычно пользователь — но не группа — имеет доступ администратора.</span><span class="sxs-lookup"><span data-stu-id="878d1-164">If you are using demo data, usually the user has admin access, but not the team.</span></span> <span data-ttu-id="878d1-165">Без этого при запуске проекта из интегратора данных вы получите сообщение об ошибке, что рабочая группа-участник отсутствует.</span><span class="sxs-lookup"><span data-stu-id="878d1-165">Without this you will get an error that Principal team is missing when running the project from Data integrator.</span></span> 

    - <span data-ttu-id="878d1-166">Выбрав **Параметры** > **Безопасность** > **Группы**, выберите необходимую группу, нажмите **Управление ролями** и выберите роль с требуемыми разрешениями, например "Системный администратор".</span><span class="sxs-lookup"><span data-stu-id="878d1-166">Under **Settings** > **Security** > **Teams**, select the relevant team, click **Manage Roles** and select a role with the desired permissions e.g. System Administrator.</span></span>

- <span data-ttu-id="878d1-167">Выбрав **Параметры** > **Администрирование** > **Параметры системы** > **Продажи** убедитесь, что для параметра **Использовать системный расчет цен** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="878d1-167">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="878d1-168">Выбрав **Параметры** > **Администрирование** > **Параметры системы** > **Продажи** убедитесь, что для параметра **Способ расчета скидки** установлено значение **Позиция строки**.</span><span class="sxs-lookup"><span data-stu-id="878d1-168">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="878d1-169">Настройка в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="878d1-169">Setup in Finance and Operations</span></span>

<span data-ttu-id="878d1-170">Задайте **Продажи и маркетинг** > **Периодические задачи** > **Рассчитать итоги продаж** для выполнения в качестве пакетного задания, установив параметр **Рассчитанные итоги для заказов на продажу** в значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="878d1-170">Set **Sales and marketing** > **Periodic tasks** > **Calculate sales totals** to run as a batch job, with **Calculate totals for sales orders** set to **Yes**.</span></span> <span data-ttu-id="878d1-171">Это важно, потому что синхронизироваться в CDS и Sales будут только заказы на продажу с рассчитанными итогами продаж.</span><span class="sxs-lookup"><span data-stu-id="878d1-171">This is important because only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span> <span data-ttu-id="878d1-172">Частота пакетного задания должна соответствовать частоте синхронизации заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="878d1-172">The frequency of the batch job should be alligned with the frequency of the sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="878d1-173">Настройка в проекте интеграции данных</span><span class="sxs-lookup"><span data-stu-id="878d1-173">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="878d1-174">Задача SalesHeader</span><span class="sxs-lookup"><span data-stu-id="878d1-174">SalesHeader task</span></span>

- <span data-ttu-id="878d1-175">Обновите сопоставление для кода организации CDS **Источник** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="878d1-175">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span>

    - <span data-ttu-id="878d1-176">Значение шаблона по умолчанию для **Account_Organization_OrganizationId** — ORG001.</span><span class="sxs-lookup"><span data-stu-id="878d1-176">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="878d1-177">Значение шаблона по умолчанию для **InvoiceAccount_Organization_OrganizationId** — ORG001.</span><span class="sxs-lookup"><span data-stu-id="878d1-177">Default template value for **InvoiceAccount_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="878d1-178">Значение шаблона по умолчанию для **Organization_OrganizationId** — ORG001.</span><span class="sxs-lookup"><span data-stu-id="878d1-178">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="878d1-179">Убедитесь, что существует необходимое сопоставление в **Источник** > **CDS для InvoiceCountryRegionId с BillingAddress_Country** и для **DeliveryCountryRegionId с DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="878d1-179">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** and for **DeliveryCountryRegionId to DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="878d1-180">Значение шаблона — **ValueMap** с количеством сопоставленных стран.</span><span class="sxs-lookup"><span data-stu-id="878d1-180">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="878d1-181">Для создания заказов в Sales требуется **прайс-лист**.</span><span class="sxs-lookup"><span data-stu-id="878d1-181">**Price list** is required to create orders in Sales.</span></span> <span data-ttu-id="878d1-182">Измените **ValueMap** в **CDS** > **Место назначения** для **pricelevelid.name [имя прайс-листа]** на **прайс-лист**, используемый в Sales для данной валюты.</span><span class="sxs-lookup"><span data-stu-id="878d1-182">Update the **ValueMap** in **CDS** > **Destination** for **pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="878d1-183">Можно использовать либо **прайс-лист** по умолчанию для одной валюты, либо **ValueMap** если у вас есть **прайс-листы** в нескольких валютах.</span><span class="sxs-lookup"><span data-stu-id="878d1-183">You can either used the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>
    
    - <span data-ttu-id="878d1-184">Значение по умолчанию шаблона для **pricelevelid.name [имя прайс-листа]** — CRM Service USA (sample).</span><span class="sxs-lookup"><span data-stu-id="878d1-184">Default template value for **pricelevelid.name [Price List Name]** is CRM Service USA (sample).</span></span> 

#### <a name="salesline-task"></a><span data-ttu-id="878d1-185">Задача SalesLine</span><span class="sxs-lookup"><span data-stu-id="878d1-185">SalesLine task</span></span>

- <span data-ttu-id="878d1-186">Обновите сопоставление для кода организации CDS **Источник** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="878d1-186">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 
    
    - <span data-ttu-id="878d1-187">Значение шаблона по умолчанию для **SalesOrder_Organization_OrganizationId** — ORG001.</span><span class="sxs-lookup"><span data-stu-id="878d1-187">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="878d1-188">Значение шаблона по умолчанию для **Product_Organization_OrganizationId** — ORG001.</span><span class="sxs-lookup"><span data-stu-id="878d1-188">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="878d1-189">Убедитесь, что в **Источник** > **CDS** существует необходимое сопоставление для **DeliveryCountryRegionId** с **DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="878d1-189">Ensure that the needed mapping exists in **Source** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="878d1-190">Значение шаблона — **ValueMap** с количеством сопоставленных стран.</span><span class="sxs-lookup"><span data-stu-id="878d1-190">Template value is **ValueMap** with a number of countries mapped.</span></span>
    
- <span data-ttu-id="878d1-191">Убедитесь, что в **Источник** > **Сопоставление CDS** существует необходимая **ValueMap** для **SalesUnitSymbol** в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="878d1-191">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span>

    - <span data-ttu-id="878d1-192">Значение шаблона с **ValueMap** определено для **SalesUnitSymbol с Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="878d1-192">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="878d1-193">Сопоставление шаблона в интеграторе данных</span><span class="sxs-lookup"><span data-stu-id="878d1-193">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="878d1-194">Поля **Условия оплаты**, **Условия фрахта**, **Условия поставки**, **Способ доставки** и **Режим доставки** не являются частью сопоставлений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="878d1-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="878d1-195">Чтобы сопоставить эти поля, необходимо настроить преобразование значений, характерное для данных в организациях, между которыми синхронизируется объект.</span><span class="sxs-lookup"><span data-stu-id="878d1-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="878d1-196">На следующем рисунке показан пример сопоставления шаблона в интеграторе данных.</span><span class="sxs-lookup"><span data-stu-id="878d1-196">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="orderheader"></a><span data-ttu-id="878d1-197">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="878d1-197">OrderHeader</span></span>

![Сопоставление шаблона в интеграторе данных](./media/sales-order-template-mapping-data-integrator-1.png)

![Сопоставление шаблона в интеграторе данных](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a><span data-ttu-id="878d1-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="878d1-200">OrderLine</span></span>

![Сопоставление шаблона в интеграторе данных](./media/sales-order-template-mapping-data-integrator-3.png)

![Сопоставление шаблона в интеграторе данных](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="878d1-203">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="878d1-203">Related topics</span></span>

[<span data-ttu-id="878d1-204">Синхронизация продуктов из Finance and Operations с продуктами в Sales</span><span class="sxs-lookup"><span data-stu-id="878d1-204">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="878d1-205">Синхронизация организаций из Finance and Operations с клиентами в Sales</span><span class="sxs-lookup"><span data-stu-id="878d1-205">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="878d1-206">Синхронизация контактов из Finance and Operations с контактами в Sales</span><span class="sxs-lookup"><span data-stu-id="878d1-206">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="878d1-207">Синхронизация заголовков и строк предложений по продажам из Sales с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="878d1-207">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="878d1-208">Синхронизация заголовков и строк счетов продажи из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="878d1-208">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


