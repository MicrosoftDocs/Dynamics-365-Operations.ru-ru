---
title: "Синхронизация заголовков и строк заказов на продажу непосредственно из Finance and Operations в Sales"
description: "В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк заказа на продажу непосредственно из Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition в Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="3dabf-103">Синхронизация заголовков и строк заказов на продажу непосредственно из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="3dabf-103">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3dabf-104">В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк заказа на продажу непосредственно из Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition в Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="3dabf-104">This topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="3dabf-105">Поток данных в решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="3dabf-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="3dabf-106">Решение "Перспективный клиент в наличные деньги" использует функцию интеграции данных для синхронизации данных между экземплярами Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="3dabf-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="3dabf-107">Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных об организациях, контактах, продуктах, предложениях по продажам, заказах на продажу и накладных по продажам между Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="3dabf-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="3dabf-108">На следующем рисунке показано, как данные синхронизируются между Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="3dabf-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="3dabf-109">[![Поток данных в решение "Перспективный клиент в наличные деньги"](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="3dabf-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="3dabf-110">Шаблоны и задачи</span><span class="sxs-lookup"><span data-stu-id="3dabf-110">Templates and tasks</span></span>

<span data-ttu-id="3dabf-111">Чтобы получить доступ к доступным шаблонам, откройте [Центр администрирования PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="3dabf-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="3dabf-112">Выберите **Проекты**, затем в правом верхнем углу выберите **Создать проект**, чтобы выбрать общие шаблоны.</span><span class="sxs-lookup"><span data-stu-id="3dabf-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="3dabf-113">Следующий шаблон и базовые задачи используются для синхронизации заголовков и строк заказов на продажу из Finance and Operations в Sales:</span><span class="sxs-lookup"><span data-stu-id="3dabf-113">The following template and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="3dabf-114">**Имя шаблона в интеграции данных:** "Заказы на продажу (из Fin and Ops в Sales) — напрямую"</span><span class="sxs-lookup"><span data-stu-id="3dabf-114">**Name of the template in Data integration:** Sales Orders (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="3dabf-115">**Имена задач в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="3dabf-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="3dabf-116">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="3dabf-116">OrderHeader</span></span>
    - <span data-ttu-id="3dabf-117">OrderLine</span><span class="sxs-lookup"><span data-stu-id="3dabf-117">OrderLine</span></span>

<span data-ttu-id="3dabf-118">Перед синхронизацией заголовков и строк накладных по продаже требуются следующие задачи синхронизации:</span><span class="sxs-lookup"><span data-stu-id="3dabf-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="3dabf-119">Продукты (из Fin and Ops в Sales) — напрямую</span><span class="sxs-lookup"><span data-stu-id="3dabf-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="3dabf-120">Счета (из Sales в Fin and Ops) — напрямую (если используются)</span><span class="sxs-lookup"><span data-stu-id="3dabf-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="3dabf-121">Из контактов в клиенты (из Sales в Fin and Ops) - напрямую (если используются)</span><span class="sxs-lookup"><span data-stu-id="3dabf-121">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="3dabf-122">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="3dabf-122">Entity set</span></span>

| <span data-ttu-id="3dabf-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3dabf-123">Finance and Operations</span></span>  | <span data-ttu-id="3dabf-124">Прод.</span><span class="sxs-lookup"><span data-stu-id="3dabf-124">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="3dabf-125">Заголовки заказов на продажу CDS</span><span class="sxs-lookup"><span data-stu-id="3dabf-125">CDS sales order headers</span></span> | <span data-ttu-id="3dabf-126">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="3dabf-126">SalesOrders</span></span>       |
| <span data-ttu-id="3dabf-127">Строки заказа на продажу CDS</span><span class="sxs-lookup"><span data-stu-id="3dabf-127">CDS sales order lines</span></span>   | <span data-ttu-id="3dabf-128">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="3dabf-128">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="3dabf-129">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="3dabf-129">Entity flow</span></span>

<span data-ttu-id="3dabf-130">Заказы на продажу создаются в Finance and Operations и синхронизируются в Sales.</span><span class="sxs-lookup"><span data-stu-id="3dabf-130">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="3dabf-131">Фильтры в шаблоне позволяют помочь гарантировать, что в синхронизацию включаются только необходимые заказы на продажу:</span><span class="sxs-lookup"><span data-stu-id="3dabf-131">Filters in the template help guarantee that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="3dabf-132">В заказе на продажу как заказывающий клиент, так и клиент для выставления накладной, которые были взяты из Sales, будут включены в синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="3dabf-132">On the sales order, both the ordering customer and the invoicing customer that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="3dabf-133">В Finance and Operations поля **OrderingCustomerIsExternallyMaintained** и **InvoiceCustomerIsExternallyMaintained** используются для отслеживания синхронизации в информационных объектах.</span><span class="sxs-lookup"><span data-stu-id="3dabf-133">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to track the synchronization in the data entities.</span></span>
- <span data-ttu-id="3dabf-134">Заказ на продажу в Finance and Operations должен быть подтвержден.</span><span class="sxs-lookup"><span data-stu-id="3dabf-134">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="3dabf-135">С Sales синхронизируются только подтвержденные заказы на продажу или заказы на продажу с более высоким статусом обработки, например **Отгружено** или **Выставлена накладная**.</span><span class="sxs-lookup"><span data-stu-id="3dabf-135">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="3dabf-136">После того, как заказ на продажу создан или изменен, необходимо выполнить в Finance and Operations пакетное задание **Рассчитать итоги продаж**.</span><span class="sxs-lookup"><span data-stu-id="3dabf-136">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="3dabf-137">Только заказы на продажу, для которых рассчитаны итоговые значения продаж, будут синхронизироваться с Sales.</span><span class="sxs-lookup"><span data-stu-id="3dabf-137">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="3dabf-138">В настоящее время налоги, связанные с суммами в заголовке заказа на продажу, не включаются в синхронизацию из Finance and Operations в Sales.</span><span class="sxs-lookup"><span data-stu-id="3dabf-138">Currently, tax that is related to charges on the sales order header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="3dabf-139">Sales не поддерживает налоговую информацию на уровне заголовка.</span><span class="sxs-lookup"><span data-stu-id="3dabf-139">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="3dabf-140">Однако налог, который относится к расходам на уровне строки, включается в синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="3dabf-140">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="3dabf-141">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="3dabf-141">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="3dabf-142">В сущность **Заказ** добавлены новые поля, которые отображаются на странице:</span><span class="sxs-lookup"><span data-stu-id="3dabf-142">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="3dabf-143">**Хранится во внешней системе** — задайте значение **Да**, когда заказ поступает из Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3dabf-143">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="3dabf-144">**Состояние обработки** — в этом поле отображается статус обработки заказа в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3dabf-144">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="3dabf-145">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3dabf-145">The following values are available:</span></span>

    - <span data-ttu-id="3dabf-146">Активен</span><span class="sxs-lookup"><span data-stu-id="3dabf-146">Active</span></span>
    - <span data-ttu-id="3dabf-147">Подтверждено</span><span class="sxs-lookup"><span data-stu-id="3dabf-147">Confirmed</span></span>
    - <span data-ttu-id="3dabf-148">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="3dabf-148">Packing Slip</span></span>
    - <span data-ttu-id="3dabf-149">Выставлено накладных</span><span class="sxs-lookup"><span data-stu-id="3dabf-149">Invoiced</span></span>
    - <span data-ttu-id="3dabf-150">Скомплектовано</span><span class="sxs-lookup"><span data-stu-id="3dabf-150">Picked</span></span>
    - <span data-ttu-id="3dabf-151">Частично скомплектовано</span><span class="sxs-lookup"><span data-stu-id="3dabf-151">Partially Picked</span></span>
    - <span data-ttu-id="3dabf-152">Частично упаковано</span><span class="sxs-lookup"><span data-stu-id="3dabf-152">Partially Packed</span></span>
    - <span data-ttu-id="3dabf-153">Отгружено</span><span class="sxs-lookup"><span data-stu-id="3dabf-153">Shipped</span></span>
    - <span data-ttu-id="3dabf-154">Частично отправлено</span><span class="sxs-lookup"><span data-stu-id="3dabf-154">Partially Shipped</span></span>
    - <span data-ttu-id="3dabf-155">Частично выставлен счет</span><span class="sxs-lookup"><span data-stu-id="3dabf-155">Partially Invoiced</span></span>
    - <span data-ttu-id="3dabf-156">Отменено</span><span class="sxs-lookup"><span data-stu-id="3dabf-156">Cancelled</span></span>

<span data-ttu-id="3dabf-157">Параметр **Все продукты хранятся во внешней системе** используется в других сценариях с заказами на продажу (например, при синхронизации из Sales в Finance and Operation) для согласованного отслеживания того, состоит ли заказ на продажу исключительно из продуктов, хранящихся во внешней системе.</span><span class="sxs-lookup"><span data-stu-id="3dabf-157">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (for example, synchronization from Sales to Finance and Operation) to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="3dabf-158">Если заказ на продажу состоит исключительно из управляемых извне продуктов, продукты управляются в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3dabf-158">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="3dabf-159">Эта настройка помогает гарантировать, что вы не будете пытаться синхронизировать строки заказа на продажу, содержащие продукты, которые неизвестны для Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3dabf-159">This setting helps guarantee that you don't try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="3dabf-160">Кнопки **Создать накладную**, **Отменить заказ**, **Пересчитать**, **Получить продукты** и **Искать адрес** на странице **Заказ на продажу** скрываются для заказов, хранящихся во внешней системе, потому что накладные будут создаваться в Finance and Operations и синхронизироваться в Sales.</span><span class="sxs-lookup"><span data-stu-id="3dabf-160">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="3dabf-161">Страница заказа не может редактироваться, потому что информация заказа на продажу будет синхронизироваться из Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3dabf-161">The order page can't be edited, because sales order information will be synchronized from Finance and Operations.</span></span>

<span data-ttu-id="3dabf-162">Статус заказа на продажу будет оставаться **Активный**, чтобы помочь гарантировать, что изменения из Finance and Operations будут передаваться в заказ на продажу в Sales.</span><span class="sxs-lookup"><span data-stu-id="3dabf-162">The status of a sales order will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="3dabf-163">Для управления таким поведением задайте для **Statecode \[Статус\]** значение по умолчанию **Active** в проекте интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="3dabf-163">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="3dabf-164">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="3dabf-164">Preconditions and mapping setup</span></span>

<span data-ttu-id="3dabf-165">Перед синхронизацией заказов на продажу необходимо обновить следующие параметры в системах.</span><span class="sxs-lookup"><span data-stu-id="3dabf-165">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="3dabf-166">Настройка в Sales</span><span class="sxs-lookup"><span data-stu-id="3dabf-166">Setup in Sales</span></span>

- <span data-ttu-id="3dabf-167">Убедитесь, что настроены разрешения для группы, которой назначен пользователь, из вашего набора подключений Sales.</span><span class="sxs-lookup"><span data-stu-id="3dabf-167">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="3dabf-168">Если вы используете демонстрационные данные, обычно пользователь имеет доступ администратора, но группа не имеет доступа администратора.</span><span class="sxs-lookup"><span data-stu-id="3dabf-168">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="3dabf-169">Если группа также не имеет доступа администратора при запуске проекта из интеграции данных, вы получите сообщение об ошибке, в котором будет указано, что рабочая группа-участник отсутствует.</span><span class="sxs-lookup"><span data-stu-id="3dabf-169">If the team doesn't also have admin access, when you run the project from Data integration, you will receive an error message that states that Principal team is missing.</span></span>

    <span data-ttu-id="3dabf-170">Откройте **Параметры** > **Безопасность** > **Группы**, выберите необходимую группу, выберите **Управление ролями** и выберите роль с требуемыми разрешениями, например **Системный администратор**.</span><span class="sxs-lookup"><span data-stu-id="3dabf-170">Go to **Settings** > **Security** > **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="3dabf-171">Откройте **Параметры** > **Администрирование** > **Параметры системы** > **Продажи** и убедитесь, что используются следующие настройки:</span><span class="sxs-lookup"><span data-stu-id="3dabf-171">Go to **Settings** > **Administration** > **System settings** > **Sales**, and makes sure that the following settings are used:</span></span>

    - <span data-ttu-id="3dabf-172">Для параметра **Использовать системный расчет цен** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="3dabf-172">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="3dabf-173">Для параметра **Способ расчета скидки** установлено значение **Номенклатура строки**.</span><span class="sxs-lookup"><span data-stu-id="3dabf-173">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="3dabf-174">Настройка в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3dabf-174">Setup in Finance and Operations</span></span>

<span data-ttu-id="3dabf-175">Откройте **Продажи и маркетинг** > **Периодические задачи** > **Рассчитать итоги продаж** и настройте задание для выполнения в качестве пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="3dabf-175">Go to **Sales and marketing** > **Periodic tasks** > **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="3dabf-176">Задайте для параметра **Рассчитанные итоги для заказов на продажу** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="3dabf-176">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="3dabf-177">Этот шаг важен, так как только заказы на продажу, для которых рассчитаны итоговые значения продаж, будут синхронизироваться с Sales.</span><span class="sxs-lookup"><span data-stu-id="3dabf-177">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="3dabf-178">Частота пакетного задания должна соответствовать частоте синхронизации заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="3dabf-178">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="3dabf-179">Настройка в проекте интеграции данных</span><span class="sxs-lookup"><span data-stu-id="3dabf-179">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="3dabf-180">Задача SalesHeader</span><span class="sxs-lookup"><span data-stu-id="3dabf-180">SalesHeader task</span></span>

- <span data-ttu-id="3dabf-181">Убедитесь, что существует необходимое сопоставление для **InvoiceCountryRegionId** в **BillingAddress\_Country** и для **DeliveryCountryRegionId** в **DeliveryAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="3dabf-181">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country** and for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="3dabf-182">Значение шаблона является схемой значений, где сопоставляются нескольких стран или регионов.</span><span class="sxs-lookup"><span data-stu-id="3dabf-182">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="3dabf-183">Для создания заказов в Sales требуется прайс-лист.</span><span class="sxs-lookup"><span data-stu-id="3dabf-183">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="3dabf-184">Обновите схему сопоставления для **pricelevelid.name \[имя прайс-листа\]** на прайс-лист, используемый в Sales для данной валюты.</span><span class="sxs-lookup"><span data-stu-id="3dabf-184">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="3dabf-185">Можно использовать прайс-лист по умолчанию для одной валюты.</span><span class="sxs-lookup"><span data-stu-id="3dabf-185">You can use the default price list for a single currency.</span></span> <span data-ttu-id="3dabf-186">Если имеются прайс-листы в нескольких валютах, можно использовать схему сопоставления.</span><span class="sxs-lookup"><span data-stu-id="3dabf-186">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="3dabf-187">Значение по умолчанию шаблона для **pricelevelid.name \[Имя прайс-листа\]** — **CRM Service USA (sample)**.</span><span class="sxs-lookup"><span data-stu-id="3dabf-187">The default template value for **pricelevelid.name \[Price list name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="3dabf-188">Задача SalesLine</span><span class="sxs-lookup"><span data-stu-id="3dabf-188">SalesLine task</span></span>

- <span data-ttu-id="3dabf-189">Убедитесь в наличии необходимого сопоставления для **DeliveryCountryRegionId** в **DeliveryAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="3dabf-189">Make sure that the required mapping exists for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="3dabf-190">Значение шаблона является схемой значений, где сопоставляются нескольких стран или регионов.</span><span class="sxs-lookup"><span data-stu-id="3dabf-190">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="3dabf-191">Убедитесь, что существует требуемая схема сопоставления значений для **SalesUnitSymbol** в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3dabf-191">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="3dabf-192">Значение шаблона, которое имеет сопоставление значений, определено для **SalesUnitSymbol** в **Quantity\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="3dabf-192">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3dabf-193">Сопоставление шаблона в интеграции данных</span><span class="sxs-lookup"><span data-stu-id="3dabf-193">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="3dabf-194">Поля **Условия оплаты**, **Условия фрахта**, **Условия поставки**, **Способ доставки** и **Режим доставки** не включены в сопоставления по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3dabf-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="3dabf-195">Чтобы сопоставить эти поля, необходимо настроить преобразование значений, характерное для данных в организациях, между которыми синхронизируется объект.</span><span class="sxs-lookup"><span data-stu-id="3dabf-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="3dabf-196">На следующем рисунке показан пример сопоставления шаблона в интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="3dabf-196">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="3dabf-197">Сопоставление показывает, какие данные полей будут синхронизированы из Sales в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3dabf-197">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="orderheader"></a><span data-ttu-id="3dabf-198">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="3dabf-198">OrderHeader</span></span>

![Сопоставление шаблона в интеграторе данных](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a><span data-ttu-id="3dabf-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="3dabf-200">OrderLine</span></span>

![Сопоставление шаблона в интеграторе данных](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="3dabf-202">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="3dabf-202">Related topics</span></span>

[<span data-ttu-id="3dabf-203">Решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="3dabf-203">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="3dabf-204">Синхронизация организаций непосредственно из Sales с клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3dabf-204">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="3dabf-205">Прямая синхронизация продуктов из Finance and Operations с продуктами в Sales</span><span class="sxs-lookup"><span data-stu-id="3dabf-205">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="3dabf-206">Синхронизация контактов непосредственно из Sales с контактами и клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3dabf-206">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="3dabf-207">Синхронизация заголовков и строк счетов продажи непосредственно из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="3dabf-207">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




