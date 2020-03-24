---
title: Настройка описаний по умолчанию для автоматической разноски
description: В этом разделе описывается, как настроить текст по умолчанию, который используется для описания записей учета, которые автоматически разносятся в главную книгу. Можно установить текст описания по умолчанию с помощью текста в свободной форме или фиксированных переменных.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f5fc73f636a5cac25c259ce2cbae5c5407dca9b7
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117369"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="d54d0-104">Настройка описаний по умолчанию для автоматической разноски</span><span class="sxs-lookup"><span data-stu-id="d54d0-104">Set up default descriptions for automatic posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d54d0-105">В этом разделе описывается, как настроить текст по умолчанию, который используется для описания записей учета, которые автоматически разносятся в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="d54d0-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="d54d0-106">Можно установить текст описания по умолчанию с помощью текста в свободной форме или фиксированных переменных.</span><span class="sxs-lookup"><span data-stu-id="d54d0-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="d54d0-107">Для некоторых типов проводок в некоторых странах или регионах можно также включить текст из полей в базе данных Microsoft Dynamics AX, относящихся к этим типам проводок.</span><span class="sxs-lookup"><span data-stu-id="d54d0-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="d54d0-108">Список типов проводок, а также стран и регионов см. в разделе [Необязательно: добавление другого текста в описания по умолчанию](#optional-add-other-text-to-default-descriptions) далее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="d54d0-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="d54d0-109">Настройка описаний по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d54d0-109">Set up default descriptions</span></span>

1. <span data-ttu-id="d54d0-110">Перейдите в раздел **Управление организацией** \> **Настройка** \> **Описания по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="d54d0-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="d54d0-111">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d54d0-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="d54d0-112">В поле **Описание** выберите тип проводки, для которой требуется создать описание по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d54d0-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="d54d0-113">В поле **Язык** выберите язык, к которому применяется это описание.</span><span class="sxs-lookup"><span data-stu-id="d54d0-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="d54d0-114">В поле **Текст** введите описание по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d54d0-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="d54d0-115">Можно ввести текст в поле или использовать одну или несколько из следующих переменных с произвольным текстом:</span><span class="sxs-lookup"><span data-stu-id="d54d0-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="d54d0-116">**%1** — Добавить дату проводки.</span><span class="sxs-lookup"><span data-stu-id="d54d0-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="d54d0-117">**%2** — Добавить идентификатор, который соответствует типу документа, который разносится в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="d54d0-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="d54d0-118">Например, для тех типов проводок, связанных со счетами, переменная **%2** добавляет номер счета.</span><span class="sxs-lookup"><span data-stu-id="d54d0-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="d54d0-119">**%3** — Добавить идентификатор, который связан с типом документа, который разносится в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="d54d0-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="d54d0-120">Например, для типов проводок, связанных с накладными, переменная **%3** добавляет номер счета клиента.</span><span class="sxs-lookup"><span data-stu-id="d54d0-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="d54d0-121">Необязательно: добавление другого текста в описания по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d54d0-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="d54d0-122">Для некоторых типов проводок в некоторых странах или регионах описания по умолчанию могут включать текст из полей в ваших данных, которые связаны с этими типами проводок.</span><span class="sxs-lookup"><span data-stu-id="d54d0-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="d54d0-123">В следующих списках приводятся типы проводок, и страны и регионы, для которых доступен этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d54d0-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="d54d0-124">**Типы проводок**</span><span class="sxs-lookup"><span data-stu-id="d54d0-124">**Transaction types**</span></span>

<span data-ttu-id="d54d0-125">Можно добавить другой текст в описания по умолчанию для типов проводок, которые относятся к следующим типам документов.</span><span class="sxs-lookup"><span data-stu-id="d54d0-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="d54d0-126">Накладные клиентов</span><span class="sxs-lookup"><span data-stu-id="d54d0-126">Customer invoices</span></span>
- <span data-ttu-id="d54d0-127">Кредит-ноты клиента</span><span class="sxs-lookup"><span data-stu-id="d54d0-127">Customer credit notes</span></span>
- <span data-ttu-id="d54d0-128">Наличные платежи клиента</span><span class="sxs-lookup"><span data-stu-id="d54d0-128">Customer cash payments</span></span>
- <span data-ttu-id="d54d0-129">Платежи поставщику</span><span class="sxs-lookup"><span data-stu-id="d54d0-129">Vendor payments</span></span>
- <span data-ttu-id="d54d0-130">Заказы на продажу</span><span class="sxs-lookup"><span data-stu-id="d54d0-130">Sales orders</span></span>
- <span data-ttu-id="d54d0-131">Заказы на покупку</span><span class="sxs-lookup"><span data-stu-id="d54d0-131">Purchase orders</span></span>
- <span data-ttu-id="d54d0-132">Журналы запасов</span><span class="sxs-lookup"><span data-stu-id="d54d0-132">Inventory journals</span></span>
- <span data-ttu-id="d54d0-133">Сводное планирование</span><span class="sxs-lookup"><span data-stu-id="d54d0-133">Master planning (MRP)</span></span>
- <span data-ttu-id="d54d0-134">Основные средства</span><span class="sxs-lookup"><span data-stu-id="d54d0-134">Fixed assets</span></span>

<span data-ttu-id="d54d0-135">**Страны и регионы**</span><span class="sxs-lookup"><span data-stu-id="d54d0-135">**Countries and regions**</span></span>

<span data-ttu-id="d54d0-136">Этот параметр доступен для следующих стран и регионов.</span><span class="sxs-lookup"><span data-stu-id="d54d0-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="d54d0-137">Бразилия</span><span class="sxs-lookup"><span data-stu-id="d54d0-137">Brazil</span></span>
- <span data-ttu-id="d54d0-138">Китай</span><span class="sxs-lookup"><span data-stu-id="d54d0-138">China</span></span>
- <span data-ttu-id="d54d0-139">Чешская республика</span><span class="sxs-lookup"><span data-stu-id="d54d0-139">Czech Republic</span></span>
- <span data-ttu-id="d54d0-140">Восточная Европа</span><span class="sxs-lookup"><span data-stu-id="d54d0-140">Eastern Europe</span></span>
- <span data-ttu-id="d54d0-141">Венгрия</span><span class="sxs-lookup"><span data-stu-id="d54d0-141">Hungary</span></span>
- <span data-ttu-id="d54d0-142">Индия</span><span class="sxs-lookup"><span data-stu-id="d54d0-142">India</span></span>
- <span data-ttu-id="d54d0-143">Япония</span><span class="sxs-lookup"><span data-stu-id="d54d0-143">Japan</span></span>
- <span data-ttu-id="d54d0-144">Литва</span><span class="sxs-lookup"><span data-stu-id="d54d0-144">Lithuania</span></span>
- <span data-ttu-id="d54d0-145">Латвия</span><span class="sxs-lookup"><span data-stu-id="d54d0-145">Latvia</span></span>
- <span data-ttu-id="d54d0-146">Польша</span><span class="sxs-lookup"><span data-stu-id="d54d0-146">Poland</span></span>
- <span data-ttu-id="d54d0-147">Россия</span><span class="sxs-lookup"><span data-stu-id="d54d0-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="d54d0-148">Добавление текста в описания по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d54d0-148">Add text to default descriptions</span></span>

<span data-ttu-id="d54d0-149">После завершения действий в подразделе [Настройка описаний по умолчанию](#set-up-default-descriptions) ранее в этом разделе выполните следующие действия, чтобы добавить другой текст в описания по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d54d0-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="d54d0-150">На экспресс-вкладке **Параметры** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="d54d0-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="d54d0-151">В поле **Таблица ссылок** выберите таблицу базы данных, из которой нужно добавить данные параметра в описание.</span><span class="sxs-lookup"><span data-stu-id="d54d0-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="d54d0-152">В поле **Ссылочное поле** выберите поле, из которого нужно добавить данные параметра в описание.</span><span class="sxs-lookup"><span data-stu-id="d54d0-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="d54d0-153">Повторите шаги 1–3, чтобы добавить другие параметры.</span><span class="sxs-lookup"><span data-stu-id="d54d0-153">Repeat steps 1 through 3 to add more parameters.</span></span>
