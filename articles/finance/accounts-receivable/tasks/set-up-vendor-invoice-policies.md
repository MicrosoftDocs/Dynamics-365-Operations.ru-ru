---
title: Настройка политик накладных поставщиков
description: В этом разделе описывается, как настроить политики накладных поставщика.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58518f5291b70c63506c20717034daff0268901b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143369"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="2052a-103">Настройка политик накладных поставщиков</span><span class="sxs-lookup"><span data-stu-id="2052a-103">Set up vendor invoice policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2052a-104">В этом разделе описывается, как настроить политики накладных поставщика.</span><span class="sxs-lookup"><span data-stu-id="2052a-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="2052a-105">Политики накладных поставщиков применяются при разноске накладной поставщика с помощью страницы "Накладная поставщика" и при открытии страницы "Нарушения политики" накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="2052a-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="2052a-106">Вы также можете настроить workflow-процесс накладной поставщика для выполнения политик накладных поставщиков при каждом отправлении накладной в workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="2052a-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="2052a-107">Политики накладных поставщиков не применяются к накладным, созданным в реестре или журнале накладных.</span><span class="sxs-lookup"><span data-stu-id="2052a-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="2052a-108">При проверке сопоставления накладных не используются политики накладных поставщиков, проверка настраивается на странице "Параметры модуля расчетов с поставщиками".</span><span class="sxs-lookup"><span data-stu-id="2052a-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="2052a-109">В данной записи используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="2052a-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="2052a-110">Эти шаги выполняются ролями менеджера по расчету с поставщиками или главного бухгалтера.</span><span class="sxs-lookup"><span data-stu-id="2052a-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="2052a-111">Перед началом работы убедитесь, что выбран конфигурационный ключ "Сопоставление накладных".</span><span class="sxs-lookup"><span data-stu-id="2052a-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="2052a-112">Подготовка к созданию политики накладных поставщиков</span><span class="sxs-lookup"><span data-stu-id="2052a-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="2052a-113">Выберите **Область перехода > Модули > Расчеты с поставщиками > Настройка > Параметры расчетов с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="2052a-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="2052a-114">Выберите вкладку **Проверка накладной**.</span><span class="sxs-lookup"><span data-stu-id="2052a-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="2052a-115">Установите или снимите флажок **Автоматически обновлять статус заголовка накладной**.</span><span class="sxs-lookup"><span data-stu-id="2052a-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="2052a-116">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2052a-116">Select **OK**.</span></span>
5. <span data-ttu-id="2052a-117">В поле **Разнести накладную с несоответствиями** выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="2052a-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="2052a-118">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2052a-118">Close the page.</span></span>
7. <span data-ttu-id="2052a-119">Перейдите к **Область перехода > Модули > Расчеты с поставщиками > Настройка политики > Политики накладных поставщика**.</span><span class="sxs-lookup"><span data-stu-id="2052a-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="2052a-120">Выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="2052a-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="2052a-121">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="2052a-121">Select **Add**.</span></span>
10. <span data-ttu-id="2052a-122">Закройте страницу и вернитесь на домашнюю страницу.</span><span class="sxs-lookup"><span data-stu-id="2052a-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="2052a-123">Создание типов правил политики для накладных поставщика</span><span class="sxs-lookup"><span data-stu-id="2052a-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="2052a-124">Перейдите к **Область перехода > Модули > Расчеты с поставщиками > Настройка политики > Типы правил политики для накладных поставщика**.</span><span class="sxs-lookup"><span data-stu-id="2052a-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="2052a-125">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="2052a-125">Select **New**.</span></span>
3. <span data-ttu-id="2052a-126">Введите значения в поля **Имя правила** и **Описание**.</span><span class="sxs-lookup"><span data-stu-id="2052a-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="2052a-127">В поле **Имя запроса** нажмите кнопку раскрывающегося списка, чтобы открыть поиск, затем выберите желаемую запись.</span><span class="sxs-lookup"><span data-stu-id="2052a-127">In the **Query name** field, select the drop-down button to open the lookup, then select the desired record.</span></span>
5. <span data-ttu-id="2052a-128">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2052a-128">Select **Save**.</span></span>
6. <span data-ttu-id="2052a-129">Закройте страницу и вернитесь на домашнюю страницу.</span><span class="sxs-lookup"><span data-stu-id="2052a-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="2052a-130">Определение политики накладных поставщиков</span><span class="sxs-lookup"><span data-stu-id="2052a-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="2052a-131">Перейдите к **Область перехода > Модули > Расчеты с поставщиками > Настройка политики > Политики накладных поставщика**.</span><span class="sxs-lookup"><span data-stu-id="2052a-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="2052a-132">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="2052a-132">Select **New**.</span></span>
3. <span data-ttu-id="2052a-133">Введите значения в поля **Имя** и **Описание**.</span><span class="sxs-lookup"><span data-stu-id="2052a-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="2052a-134">Разверните или сверните раздел **Организации политики**.</span><span class="sxs-lookup"><span data-stu-id="2052a-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="2052a-135">В дереве выберите **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="2052a-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="2052a-136">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="2052a-136">Select **Add**.</span></span>
7. <span data-ttu-id="2052a-137">Разверните или сверните раздел **Правила политики**.</span><span class="sxs-lookup"><span data-stu-id="2052a-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="2052a-138">Выберите **Создать правило политики**.</span><span class="sxs-lookup"><span data-stu-id="2052a-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="2052a-139">В поле **Описание правила политики** введите значение.</span><span class="sxs-lookup"><span data-stu-id="2052a-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="2052a-140">Выберите **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="2052a-140">Select **Filter**.</span></span>
11. <span data-ttu-id="2052a-141">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="2052a-141">Select **Add**.</span></span> <span data-ttu-id="2052a-142">Выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="2052a-142">Select the desired record.</span></span>
12. <span data-ttu-id="2052a-143">В полях **Таблица**, **Производная таблица** и **Поле** выберите или введите параметры из выпадающих меню.</span><span class="sxs-lookup"><span data-stu-id="2052a-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="2052a-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2052a-144">Close the page.</span></span>
14. <span data-ttu-id="2052a-145">В поле **Критерии** введите значение.</span><span class="sxs-lookup"><span data-stu-id="2052a-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="2052a-146">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2052a-146">Select **OK**.</span></span>
16. <span data-ttu-id="2052a-147">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2052a-147">Select **OK**.</span></span>
17. <span data-ttu-id="2052a-148">Закройте страницы и вернитесь на домашнюю страницу.</span><span class="sxs-lookup"><span data-stu-id="2052a-148">Close the pages to return to the home page.</span></span>

