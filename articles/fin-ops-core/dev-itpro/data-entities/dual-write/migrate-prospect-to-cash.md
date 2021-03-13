---
title: Миграция данных продажи перспективному клиенту из интегратора данных в двойную запись
description: В этой теме описывается, как перенести данные продажи перспективному клиенту из интегратора данных в двойную запись.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-01-04
ms.openlocfilehash: f1478f0246e7f1ff8bd72232cbaf4c2034cf4edb
ms.sourcegitcommit: 6af7b37b1c8950ad706e684cc13a79e662985b34
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/14/2021
ms.locfileid: "4959854"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a><span data-ttu-id="99e15-103">Миграция данных продажи перспективному клиенту из интегратора данных в двойную запись</span><span class="sxs-lookup"><span data-stu-id="99e15-103">Migrate Prospect to cash data from Data Integrator to dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99e15-104">Чтобы перенести ваши данные продажи перспективному клиенту из интегратора данных в двойную запись, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="99e15-104">To migrate your Prospect to cash data from Data Integrator to dual-write, follow these steps.</span></span>

1. <span data-ttu-id="99e15-105">Выполните задания интегратора данных продажи перспективному клиенту для выполнения последней полной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="99e15-105">Run the Prospect to cash Data Integrator jobs to do one final full synchronization.</span></span> <span data-ttu-id="99e15-106">Таким образом вы обеспечите, что обе системы (приложения Finance and Operations и приложение для взаимодействия с клиентами) имеют все данные.</span><span class="sxs-lookup"><span data-stu-id="99e15-106">In this way, you ensure that both systems (Finance and Operations apps and customer engagement apps) have all the data.</span></span>
2. <span data-ttu-id="99e15-107">Чтобы избежать возможной потери данных, экспортируйте данные продажи перспективному клиенту из Microsoft Dynamics 365 Sales в файл Excel или файл с разделителями-запятыми (CSV).</span><span class="sxs-lookup"><span data-stu-id="99e15-107">To help prevent potential data loss, export the Prospect to cash data from Microsoft Dynamics 365 Sales to an Excel file or a comma-separated values (CSV) file.</span></span> <span data-ttu-id="99e15-108">Экспортируйте данные из следующих сущностей:</span><span class="sxs-lookup"><span data-stu-id="99e15-108">Export data from the following entities:</span></span>

    - [<span data-ttu-id="99e15-109">Счет</span><span class="sxs-lookup"><span data-stu-id="99e15-109">Account</span></span>](#account-table)
    - [<span data-ttu-id="99e15-110">Контактное лицо</span><span class="sxs-lookup"><span data-stu-id="99e15-110">Contact</span></span>](#contact-table)
    - [<span data-ttu-id="99e15-111">Счет-фактура</span><span class="sxs-lookup"><span data-stu-id="99e15-111">Invoice</span></span>](#invoice-table)
    - <span data-ttu-id="99e15-112">Продукты накладной</span><span class="sxs-lookup"><span data-stu-id="99e15-112">Invoice products</span></span>
    - [<span data-ttu-id="99e15-113">Заказ</span><span class="sxs-lookup"><span data-stu-id="99e15-113">Order</span></span>](#order-table)
    - [<span data-ttu-id="99e15-114">Заказ продуктов</span><span class="sxs-lookup"><span data-stu-id="99e15-114">Order products</span></span>](#order-products-table)
    - [<span data-ttu-id="99e15-115">Товары</span><span class="sxs-lookup"><span data-stu-id="99e15-115">Products</span></span>](#products-table)
    - [<span data-ttu-id="99e15-116">Предложение с расценками</span><span class="sxs-lookup"><span data-stu-id="99e15-116">Quote</span></span>](#quote-and-quote-product-tables)
    - [<span data-ttu-id="99e15-117">Продукты предложения с расценками</span><span class="sxs-lookup"><span data-stu-id="99e15-117">Quote products</span></span>](#quote-and-quote-product-tables)

3. <span data-ttu-id="99e15-118">Удалите решение продажи перспективному клиенту из среды Sales.</span><span class="sxs-lookup"><span data-stu-id="99e15-118">Uninstall the Prospect to cash solution from the Sales environment.</span></span> <span data-ttu-id="99e15-119">На этом шаге удаляются столбцы и соответствующие данные, которые были введены решением продажи перспективному клиенту.</span><span class="sxs-lookup"><span data-stu-id="99e15-119">This step removes the columns and corresponding data that the Prospect to cash solution introduced.</span></span>
4. <span data-ttu-id="99e15-120">Установите решение двойной записи.</span><span class="sxs-lookup"><span data-stu-id="99e15-120">Install the dual-write solution.</span></span>
5. <span data-ttu-id="99e15-121">Создайте подключение двойной записи между приложением Finance and Operations и приложением для взаимодействия с клиентами для одного или нескольких юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="99e15-121">Create a dual-write connection between the Finance and Operations app and the customer engagement app for one or more legal entities.</span></span>
6. <span data-ttu-id="99e15-122">Включите сопоставление таблиц двойной записи и выполните начальную синхронизацию для нужных ссылочных данных.</span><span class="sxs-lookup"><span data-stu-id="99e15-122">Enable dual-write table maps, and run the initial synchronization for the required reference data.</span></span> <span data-ttu-id="99e15-123">(Дополнительные сведения см. в разделе [Рекомендации по первоначальной синхронизации](initial-sync-guidance.md).) Примерами необходимых данных являются группы клиентов, условия оплаты и графики оплаты.</span><span class="sxs-lookup"><span data-stu-id="99e15-123">(For more information, see [Considerations for initial synchronization](initial-sync-guidance.md).) Examples of required data include customer groups, payment terms, and payment schedules.</span></span> <span data-ttu-id="99e15-124">Не активируйте сопоставления двойной записи для таблиц, для которых требуется инициализация, например для таблиц счетов, предложений с расценками, строк предложений с расценками, заказов и строк заказа.</span><span class="sxs-lookup"><span data-stu-id="99e15-124">Don't enable the dual-write maps for tables that require initialization, such as the account, quote, quote line, order, and order line tables.</span></span>
7. <span data-ttu-id="99e15-125">В приложении взаимодействия с клиентами перейдите в раздел **Дополнительные параметры \> Параметры системы \> Управление данными \> Правила обнаружения повторяющихся записей** и отключите все правила.</span><span class="sxs-lookup"><span data-stu-id="99e15-125">In the customer engagement app, go to **Advanced Settings \> System Settings \> Data Management \> Duplicate detection rules**, and disable all the rules.</span></span>
8. <span data-ttu-id="99e15-126">Инициализируйте таблицы, перечисленные на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="99e15-126">Initialize the tables that are listed in step 2.</span></span> <span data-ttu-id="99e15-127">Инструкции см. в остальных разделах данной темы.</span><span class="sxs-lookup"><span data-stu-id="99e15-127">For instructions, see the remaining sections of this topic.</span></span>
9. <span data-ttu-id="99e15-128">Откройте приложение Finance and Operations и включите сопоставления таблиц, такие как сопоставления таблиц счетов, предложений с расценками, строк предложения с расценками, заказов и строк заказа.</span><span class="sxs-lookup"><span data-stu-id="99e15-128">Open the Finance and Operations app, and enable the table maps, such as the account, quote, quote line, order, and order line table maps.</span></span> <span data-ttu-id="99e15-129">Затем выполните начальную синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="99e15-129">Then run the initial synchronization.</span></span> <span data-ttu-id="99e15-130">(Дополнительные сведения см. в разделе [Рекомендации по первоначальной синхронизации](initial-sync-guidance.md) .) В ходе этого процесса будут синхронизироваться дополнительные сведения из приложения Finance and Operations, такие как статус обработки, адреса доставки и выставления счетов, сайты и склады.</span><span class="sxs-lookup"><span data-stu-id="99e15-130">(For more information, see [Considerations for initial synchronization](initial-sync-guidance.md).) This process will sync additional information from the Finance and Operations app, such as processing status, shipping and billing addresses, sites, and warehouses.</span></span>

## <a name="account-table"></a><span data-ttu-id="99e15-131">Таблица учетной записи</span><span class="sxs-lookup"><span data-stu-id="99e15-131">Account table</span></span>

1. <span data-ttu-id="99e15-132">В столбце **Компания** введите название компании, например **USMF**.</span><span class="sxs-lookup"><span data-stu-id="99e15-132">In the **Company** column, enter the company name, such as **USMF**.</span></span>
2. <span data-ttu-id="99e15-133">В столбце **Тип отношений** введите **Клиент** как статическое значение.</span><span class="sxs-lookup"><span data-stu-id="99e15-133">In the **Relationship Type** column, enter **Customer** as a static value.</span></span> <span data-ttu-id="99e15-134">Может быть нежелательно классифицировать каждую учетную запись в качестве клиента в бизнес-логике.</span><span class="sxs-lookup"><span data-stu-id="99e15-134">You might not want to classify every account record as a customer in your business logic.</span></span>
3. <span data-ttu-id="99e15-135">В столбце **Код группы клиентов** введите номер группы клиентов из приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="99e15-135">In the **Customer Group ID** column, enter the customer group number from the Finance and Operations app.</span></span> <span data-ttu-id="99e15-136">Значение по умолчанию из решение продажи перспективным клиентам равно **10**.</span><span class="sxs-lookup"><span data-stu-id="99e15-136">The default value from the Prospect to cash solution is **10**.</span></span>
4. <span data-ttu-id="99e15-137">Если вы используете решения продаж перспективным клиентам без какой-либо настройки параметра **Номер счета**, введите значение **Номер счета** в столбец **Номер субъекта**.</span><span class="sxs-lookup"><span data-stu-id="99e15-137">If you're using the Prospect to cash solution without any customization of **Account Number**, enter an **Account Number** value in the **Party Number** column.</span></span> <span data-ttu-id="99e15-138">Если у вас есть настройки и номер субъекта неизвестен, извлеките эту информацию из приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="99e15-138">If there are customizations, and you don't know the party number, pull this information from the Finance and Operations app.</span></span>

## <a name="contact-table"></a><span data-ttu-id="99e15-139">Таблица контактов</span><span class="sxs-lookup"><span data-stu-id="99e15-139">Contact table</span></span>

1. <span data-ttu-id="99e15-140">В столбце **Компания** введите название компании, например **USMF**.</span><span class="sxs-lookup"><span data-stu-id="99e15-140">In the **Company** column, enter the company name, such as **USMF**.</span></span>
2. <span data-ttu-id="99e15-141">Настройте следующие столбцы на основе значения **IsActiveCustomer** в CSV-файле:</span><span class="sxs-lookup"><span data-stu-id="99e15-141">Set the following columns, based on the **IsActiveCustomer** value in the CSV file:</span></span>

    - <span data-ttu-id="99e15-142">Если параметр **IsActiveCustomer** имеет значение **Да** в CSV-файле, установите для столбца **Для продажи** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="99e15-142">If **IsActiveCustomer** is set to **Yes** in the CSV file, set the **Sellable** column to **Yes**.</span></span> <span data-ttu-id="99e15-143">В столбце **Код группы клиентов** введите номер группы клиентов из приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="99e15-143">In the **Customer Group ID** column, enter the customer group number from the Finance and Operations app.</span></span> <span data-ttu-id="99e15-144">Значение по умолчанию из решение продажи перспективным клиентам равно **10**.</span><span class="sxs-lookup"><span data-stu-id="99e15-144">The default value from the Prospect to cash solution is **10**.</span></span>
    - <span data-ttu-id="99e15-145">Если в CSV-файле для параметра **IsActiveCustomer** установлено значение **Нет**, установите для столбца **Для продажи** значение **Нет** и установите для столбца **Контакт для** значение **Клиент**.</span><span class="sxs-lookup"><span data-stu-id="99e15-145">If **IsActiveCustomer** is set to **No** in the CSV file, set the **Sellable** column to **No**, and set the **Contact For** column to **Customer**.</span></span>

3. <span data-ttu-id="99e15-146">Если вы используете решение продаж перспективным клиентам без какаой-либо настройки параметра **Номер контакта**, установите следующие столбцы:</span><span class="sxs-lookup"><span data-stu-id="99e15-146">If you're using the Prospect to cash solution without any customization of **Contact Number**, set the following columns:</span></span>

    - <span data-ttu-id="99e15-147">Перенесите номер контакта из CSV-файла (**msdynce\_contactnumber**) в номер контакта в таблице **Контакт** (**msdyn\_contactnumber**).</span><span class="sxs-lookup"><span data-stu-id="99e15-147">Migrate the contact number from the CSV file (**msdynce\_contactnumber**) to the contact number in the **Contact** table (**msdyn\_contactnumber**).</span></span>
    - <span data-ttu-id="99e15-148">Используйте значения из таблицы **Номер контакта** в столбце **Номер субъекта**.</span><span class="sxs-lookup"><span data-stu-id="99e15-148">Use values from the **Contact Number** table in the **Party Number** column.</span></span>
    - <span data-ttu-id="99e15-149">Используйте значения из таблицы **Номер контакта** в столбце **Номер счета/Код контактного лица**.</span><span class="sxs-lookup"><span data-stu-id="99e15-149">Use values from the **Contact Number** table in the **Account Number/Contact Person ID** column.</span></span>

## <a name="invoice-table"></a><span data-ttu-id="99e15-150">Таблица накладных</span><span class="sxs-lookup"><span data-stu-id="99e15-150">Invoice table</span></span>

<span data-ttu-id="99e15-151">Поскольку данные из таблицы **Накладная** предназначены для передачи в одном направлении, из приложения Finance and Operations в приложение для взаимодействия с клиентами, инициализация не требуется.</span><span class="sxs-lookup"><span data-stu-id="99e15-151">Because data from the **Invoice** table is designed to flow one way, from the Finance and Operations app to the customer engagement app, initialization isn't required.</span></span> <span data-ttu-id="99e15-152">Выполните начальную синхронизацию, чтобы перенести все необходимые данные из приложения Finance and Operations в приложение для взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="99e15-152">Run the initial synchronization to migrate all the required data from the Finance and Operations app to the customer engagement app.</span></span> <span data-ttu-id="99e15-153">Дополнительные сведения см. в разделе [Рекомендации по первоначальной синхронизации](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="99e15-153">For more information, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>

## <a name="order-table"></a><span data-ttu-id="99e15-154">Таблица заказов</span><span class="sxs-lookup"><span data-stu-id="99e15-154">Order table</span></span>

1. <span data-ttu-id="99e15-155">В столбце **Компания** введите название компании, например **USMF**.</span><span class="sxs-lookup"><span data-stu-id="99e15-155">In the **Company** column, enter the company name, such as **USMF**.</span></span>
2. <span data-ttu-id="99e15-156">Скопируйте значение столбца **Код заказа** в CSV-файле в столбец **Номер заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="99e15-156">Copy the value of the **Order ID** column in the CSV file to the **Sales Order Number** column.</span></span>
3. <span data-ttu-id="99e15-157">Скопируйте значение столбца **Клиент** в CSV-файле в столбец **Номер накладной клиента**.</span><span class="sxs-lookup"><span data-stu-id="99e15-157">Copy the value of the **Customer** column in the CSV file to the **Invoice customer number** column.</span></span>
4. <span data-ttu-id="99e15-158">Скопируйте значение из столбца **Поставка в страну/регион** в CSV-файле в столбец **Поставка в страну/регион**.</span><span class="sxs-lookup"><span data-stu-id="99e15-158">Copy the value of the **Ship To Country/Region** column in the CSV file to the **Ship To Country/Region** column.</span></span> <span data-ttu-id="99e15-159">Примерами этого значения являются **US** и **США**.</span><span class="sxs-lookup"><span data-stu-id="99e15-159">Examples of this value include **US** and **United States**.</span></span>
5. <span data-ttu-id="99e15-160">Задайте столбец **Запрошенная дата поступления**.</span><span class="sxs-lookup"><span data-stu-id="99e15-160">Set the **Requested Receipt Date** column.</span></span> <span data-ttu-id="99e15-161">Если дата поступления не используется, используйте столбцы **Запрошенная дата поставки**, **Дата исполнения** и **Дата отправки** в CSV-файле.</span><span class="sxs-lookup"><span data-stu-id="99e15-161">If you aren't using a receipt date, use the **Requested Delivery Date**, **Date Fulfilled**, and **Date Submitted** columns in the CSV file.</span></span> <span data-ttu-id="99e15-162">Примером этого значения является **2020-03-27T00:00:00Z**.</span><span class="sxs-lookup"><span data-stu-id="99e15-162">An example of this value is **2020-03-27T00:00:00Z**.</span></span>
6. <span data-ttu-id="99e15-163">Установите столбец **Язык**.</span><span class="sxs-lookup"><span data-stu-id="99e15-163">Set the **Language** column.</span></span> <span data-ttu-id="99e15-164">Примером этого значения является **en-us**.</span><span class="sxs-lookup"><span data-stu-id="99e15-164">An example of this value is **en-us**.</span></span>
7. <span data-ttu-id="99e15-165">Задайте столбец **Тип заказа**, используя столбец **На основе номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="99e15-165">Set the **Order Type** column by using the **Item-based** column.</span></span>

## <a name="order-products-table"></a><span data-ttu-id="99e15-166">Таблица продуктов заказа</span><span class="sxs-lookup"><span data-stu-id="99e15-166">Order products table</span></span>

- <span data-ttu-id="99e15-167">В столбце **Компания** введите название компании, например **USMF**.</span><span class="sxs-lookup"><span data-stu-id="99e15-167">In the **Company** column, enter the company name, such as **USMF**.</span></span>

## <a name="products-table"></a><span data-ttu-id="99e15-168">Таблица продуктов</span><span class="sxs-lookup"><span data-stu-id="99e15-168">Products table</span></span>

<span data-ttu-id="99e15-169">Поскольку данные из таблицы **Продукты** предназначены для передачи в одном направлении, из приложения Finance and Operations в приложение для взаимодействия с клиентами, инициализация не требуется.</span><span class="sxs-lookup"><span data-stu-id="99e15-169">Because data from the **Products** table is designed to flow one way, from the Finance and Operations app to the customer engagement app, initialization isn't required.</span></span> <span data-ttu-id="99e15-170">Выполните начальную синхронизацию, чтобы перенести все необходимые данные из приложения Finance and Operations в приложение для взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="99e15-170">Run the initial synchronization to migrate all the required data from the Finance and Operations app to the customer engagement app.</span></span> <span data-ttu-id="99e15-171">Дополнительные сведения см. в разделе [Рекомендации по первоначальной синхронизации](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="99e15-171">For more information, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>

## <a name="quote-and-quote-product-tables"></a><span data-ttu-id="99e15-172">Таблицы предложений с расценками и продуктов предложений с расценками</span><span class="sxs-lookup"><span data-stu-id="99e15-172">Quote and Quote product tables</span></span>

<span data-ttu-id="99e15-173">Для таблицы **Предложение с расценками** следуйте инструкциям в разделе [Таблица заказов](#order-table) ранее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="99e15-173">For the **Quote** table, follow the instructions in the [Order table](#order-table) section earlier in this topic.</span></span> <span data-ttu-id="99e15-174">Для таблицы **Продукт предложения с расценками** следуйте инструкциям в разделе [Таблица продуктов заказа](#order-products-table) ранее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="99e15-174">For the **Quote product** table, follow the instructions in the [Order products table](#order-products-table) section.</span></span>