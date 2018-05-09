---
title: "Синхронизация заголовков и строк предложений по продажам напрямую из Sales с Finance and Operations"
description: "В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк предложений по продаже непосредственно из Microsoft Dynamics 365 for Sales в Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a18c8f2c335dee723c104648f8c7c1b79ea569d5
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="e0e6c-103">Синхронизация заголовков и строк предложений по продажам напрямую из Sales с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e0e6c-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0e6c-104">В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк предложений по продаже непосредственно из Microsoft Dynamics 365 for Sales в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="e0e6c-105">Перед использованием решения "Перспективный клиент в наличные деньги" следует ознакомиться с разделом [Интеграция данных Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="e0e6c-105">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="e0e6c-106">Шаблон и задачи</span><span class="sxs-lookup"><span data-stu-id="e0e6c-106">Template and tasks</span></span>

<span data-ttu-id="e0e6c-107">Следующий шаблон и базовые задачи используются для синхронизации заголовков и строк предложений по продажам напрямую из Sales с Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="e0e6c-107">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="e0e6c-108">**Имя шаблона в интеграции данных:** "Предложения по продажам (из Sales в Fin and Ops) — напрямую"</span><span class="sxs-lookup"><span data-stu-id="e0e6c-108">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="e0e6c-109">**Имена задач в проекте интеграции данных:**</span><span class="sxs-lookup"><span data-stu-id="e0e6c-109">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="e0e6c-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e0e6c-110">QuoteHeader</span></span>
    - <span data-ttu-id="e0e6c-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e0e6c-111">QuoteLine</span></span>

<span data-ttu-id="e0e6c-112">Перед синхронизацией заголовков и строк предложений по продажам требуются следующие задачи синхронизации:</span><span class="sxs-lookup"><span data-stu-id="e0e6c-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="e0e6c-113">Продукты (из Fin and Ops в Sales) — напрямую</span><span class="sxs-lookup"><span data-stu-id="e0e6c-113">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="e0e6c-114">Счета (из Sales в Fin and Ops) — напрямую (если используются)</span><span class="sxs-lookup"><span data-stu-id="e0e6c-114">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="e0e6c-115">Из контактов в клиенты (из Sales в Fin and Ops) - напрямую (если используются)</span><span class="sxs-lookup"><span data-stu-id="e0e6c-115">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="e0e6c-116">Набор объектов</span><span class="sxs-lookup"><span data-stu-id="e0e6c-116">Entity set</span></span>

| <span data-ttu-id="e0e6c-117">Прод.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-117">Sales</span></span>        | <span data-ttu-id="e0e6c-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e0e6c-118">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="e0e6c-119">Цитаты</span><span class="sxs-lookup"><span data-stu-id="e0e6c-119">Quotes</span></span>       | <span data-ttu-id="e0e6c-120">Заголовок предложения по продажам CDS</span><span class="sxs-lookup"><span data-stu-id="e0e6c-120">CDS sales quotation header</span></span> |
| <span data-ttu-id="e0e6c-121">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="e0e6c-121">QuoteDetails</span></span> | <span data-ttu-id="e0e6c-122">Строки предложения по продаже CDS</span><span class="sxs-lookup"><span data-stu-id="e0e6c-122">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="e0e6c-123">Поток объектов</span><span class="sxs-lookup"><span data-stu-id="e0e6c-123">Entity flow</span></span>

<span data-ttu-id="e0e6c-124">Предложения по продажам создаются в Sales и синхронизируются с Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-124">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="e0e6c-125">Предложения по продажам из Sales синхронизируются, только если выполняются следующие условия:</span><span class="sxs-lookup"><span data-stu-id="e0e6c-125">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="e0e6c-126">Все предлагаемые продукты в предложении по продаже управляются извне.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-126">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="e0e6c-127">После нажатия кнопки **Активировать предложение** это предложение по продажам становится активным.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-127">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e0e6c-128">Решение "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="e0e6c-128">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="e0e6c-129">Добавлено поле **Имеет только управляемые извне продукты** к объекту **Предложение по продаже** для постоянного отслеживания того, состоит ли предложение по продаже полностью из управляемых извне продуктов.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-129">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="e0e6c-130">Если предложение по продаже содержит только управляемые извне продукты, продукты управляются в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-130">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="e0e6c-131">Это поведение помогает гарантировать, что вы не будете пытаться синхронизировать строки предложения по продаже, которые содержат продукты, неизвестные для Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-131">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="e0e6c-132">Все предлагаемые продукты в предложении по продажам обновляются сведениями **Имеет только управляемые извне продукты** из заголовка предложения по продажам.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-132">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="e0e6c-133">Эти сведения находятся в поле **Предложения имеет только управляемые извне продукты** в объекте **QuoteDetails**.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-133">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="e0e6c-134">Скидка может быть добавлена для продукта предложения с расценками и будет синхронизирована с Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-134">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="e0e6c-135">Поля **Скидка**, **Расходы** и **Налог** в заголовке управляются настройкой в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-135">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="e0e6c-136">В настоящее время эта настройка не поддерживает сопоставление интеграции.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-136">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="e0e6c-137">В текущем дизайне поля **Цена**, **Скидка**, **Расходы** и **Налог** управляются и обрабатываются в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-137">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="e0e6c-138">В Sales решение делает следующие поля доступными только для чтения, поскольку значения не синхронизируются с Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="e0e6c-138">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="e0e6c-139">Доступные только для чтения поля в заголовке предложения по продаже: **% скидки**, **Скидка** и **Сумма транспортировки**</span><span class="sxs-lookup"><span data-stu-id="e0e6c-139">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="e0e6c-140">Поля только для чтения в продуктах предложения с расценками: **Налог**</span><span class="sxs-lookup"><span data-stu-id="e0e6c-140">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="e0e6c-141">Предварительные условия и настройка сопоставления</span><span class="sxs-lookup"><span data-stu-id="e0e6c-141">Preconditions and mapping setup</span></span>

<span data-ttu-id="e0e6c-142">Перед синхронизацией предложений по продажам необходимо обновить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="e0e6c-142">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="e0e6c-143">Настройка в Sales</span><span class="sxs-lookup"><span data-stu-id="e0e6c-143">Setup in Sales</span></span>

- <span data-ttu-id="e0e6c-144">Убедитесь, что настроены разрешения для группы, которой назначен пользователь, из вашего набора подключений в Sales.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-144">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="e0e6c-145">Если вы используете демонстрационные данные, обычно пользователь имеет доступ администратора, но группа не имеет доступа администратора.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-145">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="e0e6c-146">Если группа не имеет доступа администратора при запуске проекта из интеграции данных, вы получите сообщение об ошибке, в котором будет указано, что рабочая группа-участник отсутствует.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-146">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="e0e6c-147">Чтобы настроить разрешения для группы, откройте **Параметры** &gt; **Контроль доступа** &gt; **Группы** и выберите соответствующую группу.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-147">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="e0e6c-148">Выберите **Управление ролями**, выберите роль с требуемыми разрешениями, например **Системный администратор**.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-148">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="e0e6c-149">Откройте **Параметры** &gt; **Администрирование** &gt; **Параметры системы** &gt; **Продажи** и убедитесь, что используются следующие настройки:</span><span class="sxs-lookup"><span data-stu-id="e0e6c-149">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="e0e6c-150">Для параметра **Использовать системный расчет цен** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-150">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="e0e6c-151">Для параметра **Способ расчета скидки** установлено значение **Номенклатура строки**.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-151">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="e0e6c-152">Настройка в проекте интеграции данных</span><span class="sxs-lookup"><span data-stu-id="e0e6c-152">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="e0e6c-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e0e6c-153">QuoteHeader</span></span>

- <span data-ttu-id="e0e6c-154">Убедитесь в наличии необходимого сопоставления для **Shipto\_country** в **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-154">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="e0e6c-155">В схеме значений можно определить значение по умолчанию, которое используется, если значение не заполнено.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-155">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="e0e6c-156">Просто оставьте левой сторону пустой, а с правой стороны задайте нужную страну или регион.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-156">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="e0e6c-157">Таким образом, нет необходимости вводить страну или регион для заказов внутри страницы.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-157">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="e0e6c-158">Значение шаблона является схемой значений, где сопоставляются нескольких стран или регионов, и где пустое значение равно значению **США**.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-158">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="e0e6c-159">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e0e6c-159">QuoteLine</span></span>

- <span data-ttu-id="e0e6c-160">Убедитесь, что существует требуемая схема сопоставления значений для **SalesUnitSymbol** в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-160">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="e0e6c-161">Убедитесь в том, что требуемые единицы определены в Sales.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-161">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="e0e6c-162">Значение шаблона, которое имеет сопоставление значений, определено для **oumid.name** в **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-162">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="e0e6c-163">Дополнительно: можно добавить следующие сопоставления для гарантии того, что строки этого предложения по продажам будут импортироваться в Finance and Operations, если отсутствует информация по умолчанию от клиента или продукта:</span><span class="sxs-lookup"><span data-stu-id="e0e6c-163">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="e0e6c-164">**SiteId** — сайт необходим для создания предложений и строк заказов на продажу в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-164">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="e0e6c-165">Не существует значения шаблона по умолчанию для **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-165">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="e0e6c-166">**WarehouseId** — склад необходим для обработки предложений и строк заказов на продажу в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-166">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="e0e6c-167">Не существует значения шаблона по умолчанию для **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-167">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="e0e6c-168">Сопоставление шаблона в интеграторе данных</span><span class="sxs-lookup"><span data-stu-id="e0e6c-168">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="e0e6c-169">Поля **Скидка**, **Расходы** и **Налог** управляются сложной настройкой в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-169">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="e0e6c-170">В настоящее время эта настройка не поддерживает сопоставление интеграции.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-170">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="e0e6c-171">В текущем дизайне поля **Цена**, **Скидка**, **Расходы** и **Налог** обрабатываются в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-171">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="e0e6c-172">Поля **Условия оплаты**, **Условия фрахта**, **Условия поставки**, **Способ доставки** и **Режим доставки** не являются частью сопоставлений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-172">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="e0e6c-173">Чтобы сопоставить эти поля, необходимо настроить преобразование значений, характерное для данных в организациях, между которыми синхронизируется объект.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-173">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="e0e6c-174">На следующем рисунке показан пример сопоставления шаблона в интеграторе данных.</span><span class="sxs-lookup"><span data-stu-id="e0e6c-174">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="e0e6c-175">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="e0e6c-175">QuoteHeader</span></span>

![Сопоставление шаблона в интеграторе данных](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="e0e6c-177">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="e0e6c-177">QuoteLine</span></span>

![Сопоставление шаблона в интеграторе данных](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="e0e6c-179">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="e0e6c-179">Related topics</span></span>

[<span data-ttu-id="e0e6c-180">Решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="e0e6c-180">Prospect to cash</span></span>](prospect-to-cash.md)


