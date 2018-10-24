--- 
title: "Изучение/разрешение исключений"
description: "Политики накладных поставщиков применяются при разноске накладной поставщика с помощью страницы \"Накладная поставщика\" и при открытии страницы \"Нарушения политики\" накладной поставщика."
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 2c6f8c8dcf7a301c7fb2d095658ac96cd4a24dff
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="researchresolve-exceptions"></a><span data-ttu-id="17521-103">Изучение/разрешение исключений</span><span class="sxs-lookup"><span data-stu-id="17521-103">Research/Resolve exceptions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="17521-104">Политики накладных поставщиков применяются при разноске накладной поставщика с помощью страницы "Накладная поставщика" и при открытии страницы "Нарушения политики" накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="17521-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="17521-105">Вы также можете настроить workflow-процесс накладной поставщика для выполнения политик накладных поставщиков при каждом отправлении накладной в workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="17521-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="17521-106">Политики накладных поставщиков не применяются к накладным, созданным в реестре или журнале накладных.</span><span class="sxs-lookup"><span data-stu-id="17521-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="17521-107">При проверке сопоставления накладных не используются политики накладных поставщиков, проверка настраивается на странице "Параметры модуля расчетов с поставщиками".</span><span class="sxs-lookup"><span data-stu-id="17521-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="17521-108">В данной записи используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="17521-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="17521-109">Эти шаги выполняются ролями менеджера по расчету с поставщиками или главного бухгалтера.</span><span class="sxs-lookup"><span data-stu-id="17521-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="17521-110">Перед началом работы убедитесь, что выбран конфигурационный ключ "Сопоставление накладных".</span><span class="sxs-lookup"><span data-stu-id="17521-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="17521-111">Подготовка к созданию политики накладных поставщиков</span><span class="sxs-lookup"><span data-stu-id="17521-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="17521-112">Перейдите в раздел "Расчеты с поставщиками" > "Настройка" > "Параметры расчетов с поставщиками".</span><span class="sxs-lookup"><span data-stu-id="17521-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="17521-113">Перейдите на вкладку "Проверка накладной".</span><span class="sxs-lookup"><span data-stu-id="17521-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="17521-114">Установите или снимите флажок "Автоматически обновлять статус заголовка накладной".</span><span class="sxs-lookup"><span data-stu-id="17521-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="17521-115">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="17521-115">Click OK.</span></span>
5. <span data-ttu-id="17521-116">В поле "Разнести накладную с несоответствиями:" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="17521-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="17521-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="17521-117">Close the page.</span></span>
7. <span data-ttu-id="17521-118">Перейдите в раздел "Расчеты с поставщиками" > "Настройка политики" > "Политики накладных поставщиков".</span><span class="sxs-lookup"><span data-stu-id="17521-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="17521-119">Щелкните "Параметры".</span><span class="sxs-lookup"><span data-stu-id="17521-119">Click Parameters.</span></span>
9. <span data-ttu-id="17521-120">Нажмите кнопку "Добавить".</span><span class="sxs-lookup"><span data-stu-id="17521-120">Click btnAdd.</span></span>
10. <span data-ttu-id="17521-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="17521-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="17521-122">Создание типов правил политики для накладных поставщика</span><span class="sxs-lookup"><span data-stu-id="17521-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="17521-123">Перейдите в раздел "Расчеты с поставщиками" > "Настройка политики" > "Типы правил политики для накладных поставщиков".</span><span class="sxs-lookup"><span data-stu-id="17521-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="17521-124">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="17521-124">Click New.</span></span>
3. <span data-ttu-id="17521-125">В поле "Правило" введите значение.</span><span class="sxs-lookup"><span data-stu-id="17521-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="17521-126">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="17521-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="17521-127">В поле "Имя запроса" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="17521-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="17521-128">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="17521-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="17521-129">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="17521-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="17521-130">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="17521-130">Click Save.</span></span>
9. <span data-ttu-id="17521-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="17521-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="17521-132">Определение политики накладных поставщиков</span><span class="sxs-lookup"><span data-stu-id="17521-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="17521-133">Перейдите в раздел "Расчеты с поставщиками" > "Настройка политики" > "Политики накладных поставщиков".</span><span class="sxs-lookup"><span data-stu-id="17521-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="17521-134">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="17521-134">Click New.</span></span>
3. <span data-ttu-id="17521-135">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="17521-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="17521-136">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="17521-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="17521-137">Разверните или сверните раздел "Организации политики".</span><span class="sxs-lookup"><span data-stu-id="17521-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="17521-138">В дереве выберите "Contoso Entertainment System USA".</span><span class="sxs-lookup"><span data-stu-id="17521-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="17521-139">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="17521-139">Click Add.</span></span>
8. <span data-ttu-id="17521-140">Разверните или сверните раздел "Правила политики".</span><span class="sxs-lookup"><span data-stu-id="17521-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="17521-141">Щелкните "Создать правило политики".</span><span class="sxs-lookup"><span data-stu-id="17521-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="17521-142">В поле "Описание правила политики" введите значение.</span><span class="sxs-lookup"><span data-stu-id="17521-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="17521-143">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="17521-143">Click Filter.</span></span>
12. <span data-ttu-id="17521-144">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="17521-144">Click Add.</span></span>
13. <span data-ttu-id="17521-145">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="17521-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="17521-146">В поле "Таблица" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="17521-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="17521-147">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="17521-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="17521-148">В поле "Производная таблица" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="17521-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="17521-149">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="17521-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="17521-150">В поле "Поле" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="17521-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="17521-151">В поле "Поле" введите значение.</span><span class="sxs-lookup"><span data-stu-id="17521-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="17521-152">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="17521-152">Close the page.</span></span>
21. <span data-ttu-id="17521-153">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="17521-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="17521-154">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="17521-154">Click OK.</span></span>
23. <span data-ttu-id="17521-155">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="17521-155">Click OK.</span></span>
24. <span data-ttu-id="17521-156">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="17521-156">Close the page.</span></span>
25. <span data-ttu-id="17521-157">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="17521-157">Close the page.</span></span>


