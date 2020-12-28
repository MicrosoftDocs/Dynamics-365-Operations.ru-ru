---
title: Синхронизация заголовков и строк предложений по продаже непосредственно из Sales с Supply Chain Management
description: В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк предложений по продаже непосредственно из Dynamics 365 Sales в Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: c7d4cacbf56243830633f4d0fd3c57071b08ab56
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527346"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a><span data-ttu-id="dc6c4-103">Синхронизация заголовков и строк предложений по продаже непосредственно из Sales с Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="dc6c4-103">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="dc6c4-104">В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк предложений по продаже непосредственно из Dynamics 365 Sales в Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="dc6c4-105">Перед использованием решения "Перспективный клиент в наличные деньги" следует ознакомиться с разделом [Интеграция данных в Common Data Service для приложений](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="dc6c4-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="dc6c4-106">Поток данных в решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="dc6c4-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="dc6c4-107">Решение "Перспективный клиент в наличные деньги" использует функцию интеграции данных для синхронизации данных между экземплярами Supply Chain Management и Sales.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="dc6c4-108">Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных для организаций, контактов, продуктов, предложений по продажам, заказов на продажу и накладных по продажам между Supply Chain Management и Sales.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="dc6c4-109">На следующем рисунке показано, как данные синхронизируются между Supply Chain Management и Sales.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="dc6c4-110">[![Поток данных в решение "Перспективный клиент в наличные деньги"](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="dc6c4-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="dc6c4-111">Шаблон и задачи</span><span class="sxs-lookup"><span data-stu-id="dc6c4-111">Template and tasks</span></span>

<span data-ttu-id="dc6c4-112">Следующий шаблон и базовые задачи используются для синхронизации заголовков и строк предложений по продажам напрямую из Sales с Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="dc6c4-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="dc6c4-113">**Имя шаблона в интеграции данных:** "Предложения по продажам (из Sales в Supply Chain Management) — напрямую"</span><span class="sxs-lookup"><span data-stu-id="dc6c4-113">**Name of the template in Data integration:** Sales Quotes (Sales to Supply Chain Management) - Direct</span></span>
- <span data-ttu-id="dc6c4-114">**Имена задач в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="dc6c4-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="dc6c4-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="dc6c4-115">QuoteHeader</span></span>
    - <span data-ttu-id="dc6c4-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="dc6c4-116">QuoteLine</span></span>

<span data-ttu-id="dc6c4-117">Перед синхронизацией заголовков и строк предложений по продажам требуются следующие задачи синхронизации:</span><span class="sxs-lookup"><span data-stu-id="dc6c4-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="dc6c4-118">Продукты (из Supply Chain Management в Sales) — напрямую</span><span class="sxs-lookup"><span data-stu-id="dc6c4-118">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="dc6c4-119">Счета (из Sales в Supply Chain Management) — напрямую (если используется)</span><span class="sxs-lookup"><span data-stu-id="dc6c4-119">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="dc6c4-120">Из контактов в клиенты (из Sales в Supply Chain Management) - напрямую (если используются)</span><span class="sxs-lookup"><span data-stu-id="dc6c4-120">Contacts to Customers (Sales to Supply Chain Management) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="dc6c4-121">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="dc6c4-121">Entity set</span></span>

| <span data-ttu-id="dc6c4-122">Прод.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-122">Sales</span></span>        | <span data-ttu-id="dc6c4-123">Управление цепочкой поставок</span><span class="sxs-lookup"><span data-stu-id="dc6c4-123">Supply Chain Management</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="dc6c4-124">Цитаты</span><span class="sxs-lookup"><span data-stu-id="dc6c4-124">Quotes</span></span>       | <span data-ttu-id="dc6c4-125">Заголовок предложения по продаже CDS</span><span class="sxs-lookup"><span data-stu-id="dc6c4-125">CDS sales quotation header</span></span> |
| <span data-ttu-id="dc6c4-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="dc6c4-126">QuoteDetails</span></span> | <span data-ttu-id="dc6c4-127">Строки предложения по продаже CDS</span><span class="sxs-lookup"><span data-stu-id="dc6c4-127">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="dc6c4-128">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="dc6c4-128">Entity flow</span></span>

<span data-ttu-id="dc6c4-129">Предложения по продажам создаются в Sales и синхронизируются с Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-129">Sales quotations are created in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="dc6c4-130">Предложения по продажам из Sales синхронизируются, только если выполняются следующие условия:</span><span class="sxs-lookup"><span data-stu-id="dc6c4-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="dc6c4-131">Все предлагаемые продукты в предложении по продаже управляются извне.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="dc6c4-132">После нажатия кнопки **Активировать предложение** это предложение по продажам становится активным.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="dc6c4-133">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="dc6c4-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="dc6c4-134">Добавлено поле **Имеет только управляемые извне продукты** к объекту **Предложение по продаже** для постоянного отслеживания того, состоит ли предложение по продаже полностью из управляемых извне продуктов.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="dc6c4-135">Если предложение по продаже содержит только управляемые извне продукты, продукты управляются в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-135">If a sales quotation has only externally maintained products, the products are maintained in Supply Chain Management.</span></span> <span data-ttu-id="dc6c4-136">Это поведение помогает гарантировать, что вы не будете пытаться синхронизировать строки предложения по продаже, которые содержат продукты, неизвестные для Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Supply Chain Management.</span></span>

<span data-ttu-id="dc6c4-137">Все предлагаемые продукты в предложении по продажам обновляются сведениями **Имеет только управляемые извне продукты** из заголовка предложения по продажам.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="dc6c4-138">Эти сведения находятся в поле **Предложения имеет только управляемые извне продукты** в объекте **QuoteDetails**.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="dc6c4-139">Скидка может быть добавлена для продукта предложения с расценками и будет синхронизирована с Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-139">A discount can be added to the quote product and will be synchronized to Supply Chain Management.</span></span> <span data-ttu-id="dc6c4-140">Поля **Скидка**, **Расходы** и **Налог** в заголовке управляются настройкой в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="dc6c4-141">В настоящее время эта настройка не поддерживает сопоставление интеграции.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="dc6c4-142">В текущем дизайне поля **Цена**, **Скидка**, **Расходы** и **Налог** управляются и обрабатываются в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in FSupply Chain Management.</span></span>

<span data-ttu-id="dc6c4-143">В Sales решение делает следующие поля доступными только для чтения, поскольку значения не синхронизируются с Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="dc6c4-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Supply Chain Management:</span></span>

- <span data-ttu-id="dc6c4-144">Доступные только для чтения поля в заголовке предложения по продаже: **% скидки**, **Скидка** и **Сумма транспортировки**</span><span class="sxs-lookup"><span data-stu-id="dc6c4-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="dc6c4-145">Поля только для чтения в продуктах предложения с расценками: **Налог**</span><span class="sxs-lookup"><span data-stu-id="dc6c4-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="dc6c4-146">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="dc6c4-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="dc6c4-147">Перед синхронизацией предложений по продажам необходимо обновить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="dc6c4-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="dc6c4-148">Настройка в Sales</span><span class="sxs-lookup"><span data-stu-id="dc6c4-148">Setup in Sales</span></span>

- <span data-ttu-id="dc6c4-149">Убедитесь, что настроены разрешения для группы, которой назначен пользователь, из вашего набора подключений в Sales.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="dc6c4-150">Если вы используете демонстрационные данные, обычно пользователь имеет доступ администратора, но группа не имеет доступа администратора.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="dc6c4-151">Если группа не имеет доступа администратора при запуске проекта из интеграции данных, вы получите сообщение об ошибке, в котором будет указано, что рабочая группа-участник отсутствует.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="dc6c4-152">Чтобы настроить разрешения для группы, откройте **Параметры** &gt; **Контроль доступа** &gt; **Группы** и выберите соответствующую группу.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="dc6c4-153">Выберите **Управление ролями**, выберите роль с требуемыми разрешениями, например **Системный администратор**.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="dc6c4-154">Откройте **Параметры** &gt; **Администрирование** &gt; **Параметры системы** &gt; **Продажи** и убедитесь, что используются следующие настройки:</span><span class="sxs-lookup"><span data-stu-id="dc6c4-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="dc6c4-155">Для параметра **Использовать системный расчет цен** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="dc6c4-156">Для параметра **Способ расчета скидки** установлено значение **Номенклатура строки**.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="dc6c4-157">Настройка в проекте интеграции данных</span><span class="sxs-lookup"><span data-stu-id="dc6c4-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="dc6c4-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="dc6c4-158">QuoteHeader</span></span>

- <span data-ttu-id="dc6c4-159">Убедитесь в наличии необходимого сопоставления для **Shipto\_country** в **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="dc6c4-160">В схеме значений можно определить значение по умолчанию, которое используется, если значение не заполнено.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="dc6c4-161">Просто оставьте левой сторону пустой, а с правой стороны задайте нужную страну или регион.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="dc6c4-162">Таким образом, нет необходимости вводить страну или регион для заказов внутри страницы.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="dc6c4-163">Значение шаблона является схемой значений, где сопоставляются нескольких стран или регионов, и где пустое значение равно значению **США**.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="dc6c4-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="dc6c4-164">QuoteLine</span></span>

- <span data-ttu-id="dc6c4-165">Убедитесь, что требуемая схема сопоставления значений существует для **SalesUnitSymbol** в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-165">Make sure that the required value map exists for **SalesUnitSymbol** in Supply Chain Management.</span></span>
- <span data-ttu-id="dc6c4-166">Убедитесь в том, что требуемые единицы определены в Sales.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="dc6c4-167">Значение шаблона, которое имеет сопоставление значений, определено для **oumid.name** в **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="dc6c4-168">Дополнительно: можно добавить следующие сопоставления для гарантии того, что строки этого предложения по продажам будут импортироваться в Supply Chain Management, если отсутствует информация по умолчанию от клиента или продукта:</span><span class="sxs-lookup"><span data-stu-id="dc6c4-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Supply Chain Management if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="dc6c4-169">**SiteId** — сайт необходим для создания предложений и строк заказов на продажу в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="dc6c4-170">Не существует значения шаблона по умолчанию для **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="dc6c4-171">**WarehouseId** — склад необходим для обработки предложений и строк заказов на продажу в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="dc6c4-172">Не существует значения шаблона по умолчанию для **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="dc6c4-173">Сопоставление шаблона в интеграторе данных</span><span class="sxs-lookup"><span data-stu-id="dc6c4-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="dc6c4-174">Поля **Скидка**, **Расходы** и **Налог** управляются комплексной настройкой в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Supply Chain Management.</span></span> <span data-ttu-id="dc6c4-175">В настоящее время эта настройка не поддерживает сопоставление интеграции.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="dc6c4-176">В текущем дизайне поля **Цена**, **Скидка**, **Расходы** и **Налог** обрабатываются в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Supply Chain Management.</span></span>
> - <span data-ttu-id="dc6c4-177">Поля **Условия оплаты**, **Условия фрахта**, **Условия поставки**, **Способ доставки** и **Режим доставки** не являются частью сопоставлений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="dc6c4-178">Чтобы сопоставить эти поля, необходимо настроить преобразование значений, характерное для данных в организациях, между которыми синхронизируется объект.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="dc6c4-179">На следующем рисунке показан пример сопоставления шаблона в интеграторе данных.</span><span class="sxs-lookup"><span data-stu-id="dc6c4-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="dc6c4-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="dc6c4-180">QuoteHeader</span></span>

![Сопоставление шаблона в интеграторе данных](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="dc6c4-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="dc6c4-182">QuoteLine</span></span>

![Сопоставление шаблона в интеграторе данных](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="dc6c4-184">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="dc6c4-184">Related topics</span></span>

[<span data-ttu-id="dc6c4-185">Решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="dc6c4-185">Prospect to cash</span></span>](prospect-to-cash.md)

