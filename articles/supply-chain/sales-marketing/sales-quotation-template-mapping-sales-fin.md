---
title: Синхронизация заголовков и строк предложений по продажам напрямую из Sales с Finance and Operations
description: В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк предложений по продаже непосредственно из Microsoft Dynamics 365 for Sales в Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
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
ms.openlocfilehash: efe943f5c874ed041ce7984272ebc19f57cca6ef
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "313804"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="2ac4b-103">Синхронизация заголовков и строк предложений по продаже непосредственно из Sales с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2ac4b-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ac4b-104">В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк предложений по продаже непосредственно из Microsoft Dynamics 365 for Sales в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="2ac4b-105">Перед использованием решения "Перспективный клиент в наличные деньги" следует ознакомиться с разделом [Интеграция данных в Common Data Service для приложений](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="2ac4b-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="2ac4b-106">Поток данных в решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="2ac4b-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="2ac4b-107">Решение "Перспективный клиент в наличные деньги" использует функцию интеграции данных для синхронизации данных между экземплярами Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="2ac4b-108">Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных для организаций, контактов, продуктов, предложений по продажам, заказов на продажу и накладных по продажам между Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="2ac4b-109">На следующем рисунке показано, как данные синхронизируются между Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="2ac4b-110">[![Поток данных в решение "Перспективный клиент в наличные деньги"](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="2ac4b-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="2ac4b-111">Шаблон и задачи</span><span class="sxs-lookup"><span data-stu-id="2ac4b-111">Template and tasks</span></span>

<span data-ttu-id="2ac4b-112">Следующий шаблон и базовые задачи используются для синхронизации заголовков и строк предложений по продажам напрямую из Sales с Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="2ac4b-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="2ac4b-113">**Имя шаблона в интеграции данных:** "Предложения по продажам (из Sales в Fin and Ops) — напрямую"</span><span class="sxs-lookup"><span data-stu-id="2ac4b-113">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="2ac4b-114">**Имена задач в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="2ac4b-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="2ac4b-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="2ac4b-115">QuoteHeader</span></span>
    - <span data-ttu-id="2ac4b-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="2ac4b-116">QuoteLine</span></span>

<span data-ttu-id="2ac4b-117">Перед синхронизацией заголовков и строк предложений по продажам требуются следующие задачи синхронизации:</span><span class="sxs-lookup"><span data-stu-id="2ac4b-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="2ac4b-118">Продукты (из Fin and Ops в Sales) — напрямую</span><span class="sxs-lookup"><span data-stu-id="2ac4b-118">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="2ac4b-119">Счета (из Sales в Fin and Ops) — напрямую (если используются)</span><span class="sxs-lookup"><span data-stu-id="2ac4b-119">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="2ac4b-120">Из контактов в клиенты (из Sales в Fin and Ops) - напрямую (если используются)</span><span class="sxs-lookup"><span data-stu-id="2ac4b-120">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="2ac4b-121">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="2ac4b-121">Entity set</span></span>

| <span data-ttu-id="2ac4b-122">Прод.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-122">Sales</span></span>        | <span data-ttu-id="2ac4b-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2ac4b-123">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="2ac4b-124">Цитаты</span><span class="sxs-lookup"><span data-stu-id="2ac4b-124">Quotes</span></span>       | <span data-ttu-id="2ac4b-125">Заголовок предложения по продажам CDS</span><span class="sxs-lookup"><span data-stu-id="2ac4b-125">CDS sales quotation header</span></span> |
| <span data-ttu-id="2ac4b-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="2ac4b-126">QuoteDetails</span></span> | <span data-ttu-id="2ac4b-127">Строки предложения по продаже CDS</span><span class="sxs-lookup"><span data-stu-id="2ac4b-127">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="2ac4b-128">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="2ac4b-128">Entity flow</span></span>

<span data-ttu-id="2ac4b-129">Предложения по продажам создаются в Sales и синхронизируются с Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-129">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="2ac4b-130">Предложения по продажам из Sales синхронизируются, только если выполняются следующие условия:</span><span class="sxs-lookup"><span data-stu-id="2ac4b-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="2ac4b-131">Все предлагаемые продукты в предложении по продаже управляются извне.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="2ac4b-132">После нажатия кнопки **Активировать предложение** это предложение по продажам становится активным.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="2ac4b-133">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="2ac4b-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="2ac4b-134">Добавлено поле **Имеет только управляемые извне продукты** к объекту **Предложение по продаже** для постоянного отслеживания того, состоит ли предложение по продаже полностью из управляемых извне продуктов.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="2ac4b-135">Если предложение по продаже содержит только управляемые извне продукты, продукты управляются в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-135">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="2ac4b-136">Это поведение помогает гарантировать, что вы не будете пытаться синхронизировать строки предложения по продаже, которые содержат продукты, неизвестные для Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="2ac4b-137">Все предлагаемые продукты в предложении по продажам обновляются сведениями **Имеет только управляемые извне продукты** из заголовка предложения по продажам.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="2ac4b-138">Эти сведения находятся в поле **Предложения имеет только управляемые извне продукты** в объекте **QuoteDetails**.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="2ac4b-139">Скидка может быть добавлена для продукта предложения с расценками и будет синхронизирована с Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-139">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="2ac4b-140">Поля **Скидка**, **Расходы** и **Налог** в заголовке управляются настройкой в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="2ac4b-141">В настоящее время эта настройка не поддерживает сопоставление интеграции.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="2ac4b-142">В текущем дизайне поля **Цена**, **Скидка**, **Расходы** и **Налог** управляются и обрабатываются в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="2ac4b-143">В Sales решение делает следующие поля доступными только для чтения, поскольку значения не синхронизируются с Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="2ac4b-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="2ac4b-144">Доступные только для чтения поля в заголовке предложения по продаже: **% скидки**, **Скидка** и **Сумма транспортировки**</span><span class="sxs-lookup"><span data-stu-id="2ac4b-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="2ac4b-145">Поля только для чтения в продуктах предложения с расценками: **Налог**</span><span class="sxs-lookup"><span data-stu-id="2ac4b-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="2ac4b-146">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="2ac4b-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="2ac4b-147">Перед синхронизацией предложений по продажам необходимо обновить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="2ac4b-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="2ac4b-148">Настройка в Sales</span><span class="sxs-lookup"><span data-stu-id="2ac4b-148">Setup in Sales</span></span>

- <span data-ttu-id="2ac4b-149">Убедитесь, что настроены разрешения для группы, которой назначен пользователь, из вашего набора подключений в Sales.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="2ac4b-150">Если вы используете демонстрационные данные, обычно пользователь имеет доступ администратора, но группа не имеет доступа администратора.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="2ac4b-151">Если группа не имеет доступа администратора при запуске проекта из интеграции данных, вы получите сообщение об ошибке, в котором будет указано, что рабочая группа-участник отсутствует.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="2ac4b-152">Чтобы настроить разрешения для группы, откройте **Параметры** &gt; **Контроль доступа** &gt; **Группы** и выберите соответствующую группу.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="2ac4b-153">Выберите **Управление ролями**, выберите роль с требуемыми разрешениями, например **Системный администратор**.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="2ac4b-154">Откройте **Параметры** &gt; **Администрирование** &gt; **Параметры системы** &gt; **Продажи** и убедитесь, что используются следующие настройки:</span><span class="sxs-lookup"><span data-stu-id="2ac4b-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="2ac4b-155">Для параметра **Использовать системный расчет цен** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="2ac4b-156">Для параметра **Способ расчета скидки** установлено значение **Номенклатура строки**.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="2ac4b-157">Настройка в проекте интеграции данных</span><span class="sxs-lookup"><span data-stu-id="2ac4b-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="2ac4b-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="2ac4b-158">QuoteHeader</span></span>

- <span data-ttu-id="2ac4b-159">Убедитесь в наличии необходимого сопоставления для **Shipto\_country** в **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="2ac4b-160">В схеме значений можно определить значение по умолчанию, которое используется, если значение не заполнено.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="2ac4b-161">Просто оставьте левой сторону пустой, а с правой стороны задайте нужную страну или регион.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="2ac4b-162">Таким образом, нет необходимости вводить страну или регион для заказов внутри страницы.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="2ac4b-163">Значение шаблона является схемой значений, где сопоставляются нескольких стран или регионов, и где пустое значение равно значению **США**.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="2ac4b-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="2ac4b-164">QuoteLine</span></span>

- <span data-ttu-id="2ac4b-165">Убедитесь, что существует требуемая схема сопоставления значений для **SalesUnitSymbol** в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-165">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="2ac4b-166">Убедитесь в том, что требуемые единицы определены в Sales.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="2ac4b-167">Значение шаблона, которое имеет сопоставление значений, определено для **oumid.name** в **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="2ac4b-168">Дополнительно: можно добавить следующие сопоставления для гарантии того, что строки этого предложения по продажам будут импортироваться в Finance and Operations, если отсутствует информация по умолчанию от клиента или продукта:</span><span class="sxs-lookup"><span data-stu-id="2ac4b-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="2ac4b-169">**SiteId** — сайт необходим для создания предложений и строк заказов на продажу в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="2ac4b-170">Не существует значения шаблона по умолчанию для **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="2ac4b-171">**WarehouseId** — склад необходим для обработки предложений и строк заказов на продажу в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="2ac4b-172">Не существует значения шаблона по умолчанию для **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="2ac4b-173">Сопоставление шаблона в интеграторе данных</span><span class="sxs-lookup"><span data-stu-id="2ac4b-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="2ac4b-174">Поля **Скидка**, **Расходы** и **Налог** управляются сложной настройкой в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="2ac4b-175">В настоящее время эта настройка не поддерживает сопоставление интеграции.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="2ac4b-176">В текущем дизайне поля **Цена**, **Скидка**, **Расходы** и **Налог** обрабатываются в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="2ac4b-177">Поля **Условия оплаты**, **Условия фрахта**, **Условия поставки**, **Способ доставки** и **Режим доставки** не являются частью сопоставлений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="2ac4b-178">Чтобы сопоставить эти поля, необходимо настроить преобразование значений, характерное для данных в организациях, между которыми синхронизируется объект.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="2ac4b-179">На следующем рисунке показан пример сопоставления шаблона в интеграторе данных.</span><span class="sxs-lookup"><span data-stu-id="2ac4b-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="2ac4b-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="2ac4b-180">QuoteHeader</span></span>

![Сопоставление шаблона в интеграторе данных](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="2ac4b-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="2ac4b-182">QuoteLine</span></span>

![Сопоставление шаблона в интеграторе данных](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="2ac4b-184">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="2ac4b-184">Related topics</span></span>

[<span data-ttu-id="2ac4b-185">Решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="2ac4b-185">Prospect to cash</span></span>](prospect-to-cash.md)

