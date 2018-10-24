--- 
title: "Электронная отчетность — Создание электронных документов для платежей с помощью конфигурации формата"
description: "В следующих шагах поясняется, как пользователь с ролью \"Системный администратор\" или \"Разработчик электронной отчетности\" может использовать новую конфигурацию формата электронной отчетности для создания электронных документов для обработки платежей."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: cf2ae8fb451eba1054bb94edbce009dcfa8c872c
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="8d057-103">Электронная отчетность — Создание электронных документов для платежей с помощью конфигурации формата</span><span class="sxs-lookup"><span data-stu-id="8d057-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8d057-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может использовать новую конфигурацию формата электронной отчетности для создания электронных документов для обработки платежей.</span><span class="sxs-lookup"><span data-stu-id="8d057-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="8d057-105">Эти шаги можно выполнить в демонстрационной компании GBSI.</span><span class="sxs-lookup"><span data-stu-id="8d057-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="8d057-106">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание конфигурации с форматом платежного документа".</span><span class="sxs-lookup"><span data-stu-id="8d057-106">To complete these steps, you must first complete the steps in the “Create a configuration with format of payment document” procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="8d057-107">Изменение конфигурации метода электронного платежа</span><span class="sxs-lookup"><span data-stu-id="8d057-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="8d057-108">Перейдите в раздел "Расчеты с поставщиками" > "Настройка платежей" > "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="8d057-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="8d057-109">Переключите раздел "Формат файла", чтобы развернуть его, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="8d057-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="8d057-110">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="8d057-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8d057-111">Например, отфильтруйте поле "Способ оплаты" по значению "Электронно".</span><span class="sxs-lookup"><span data-stu-id="8d057-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="8d057-112">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="8d057-112">Click Edit.</span></span>
5. <span data-ttu-id="8d057-113">Установите в поле "Общая электронная отчетность" значение "Да".</span><span class="sxs-lookup"><span data-stu-id="8d057-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="8d057-114">Выберите значение "Да", чтобы использовать шаблон общей электронной отчетности для создания файлов платежей.</span><span class="sxs-lookup"><span data-stu-id="8d057-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="8d057-115">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8d057-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8d057-116">Выберите конфигурацию формата BACS (Великобритания, вымышленный).</span><span class="sxs-lookup"><span data-stu-id="8d057-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="8d057-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8d057-117">Click Save.</span></span>
9. <span data-ttu-id="8d057-118">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8d057-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="8d057-119">Проверка формата созданных файлов платежей</span><span class="sxs-lookup"><span data-stu-id="8d057-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="8d057-120">Перейдите в раздел "Расчеты с поставщиками" > "Платежи" > "Журнал платежей".</span><span class="sxs-lookup"><span data-stu-id="8d057-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="8d057-121">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8d057-121">Click New.</span></span>
3. <span data-ttu-id="8d057-122">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="8d057-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="8d057-123">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8d057-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8d057-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8d057-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8d057-125">Выберите VendPay.</span><span class="sxs-lookup"><span data-stu-id="8d057-125">Select VendPay.</span></span>  
6. <span data-ttu-id="8d057-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8d057-126">Click Save.</span></span>
7. <span data-ttu-id="8d057-127">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="8d057-127">Click Lines.</span></span>
8. <span data-ttu-id="8d057-128">В поле "Компания" введите DEMF.</span><span class="sxs-lookup"><span data-stu-id="8d057-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="8d057-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="8d057-129">DEMF</span></span>  
9. <span data-ttu-id="8d057-130">В поле "Счет" укажите значения "DE-01001".</span><span class="sxs-lookup"><span data-stu-id="8d057-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="8d057-131">DE - 01001</span><span class="sxs-lookup"><span data-stu-id="8d057-131">DE-01001</span></span>  
10. <span data-ttu-id="8d057-132">В поле "Описание" введите "Платеж".</span><span class="sxs-lookup"><span data-stu-id="8d057-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="8d057-133">Платеж</span><span class="sxs-lookup"><span data-stu-id="8d057-133">Payment</span></span>  
11. <span data-ttu-id="8d057-134">В поле "Дебет" введите число.</span><span class="sxs-lookup"><span data-stu-id="8d057-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="8d057-135">В тысячах</span><span class="sxs-lookup"><span data-stu-id="8d057-135">1000</span></span>  
12. <span data-ttu-id="8d057-136">Перейдите на вкладку Платеж.</span><span class="sxs-lookup"><span data-stu-id="8d057-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="8d057-137">В поле "Способ оплаты" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8d057-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="8d057-138">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8d057-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8d057-139">Выберите значение "Электронно".</span><span class="sxs-lookup"><span data-stu-id="8d057-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="8d057-140">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8d057-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="8d057-141">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8d057-141">Click Save.</span></span>
17. <span data-ttu-id="8d057-142">Щелкните "Создать платежи".</span><span class="sxs-lookup"><span data-stu-id="8d057-142">Click Generate payments.</span></span>
18. <span data-ttu-id="8d057-143">В поле "Способ оплаты" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8d057-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="8d057-144">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8d057-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8d057-145">Выберите значение "Электронно".</span><span class="sxs-lookup"><span data-stu-id="8d057-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="8d057-146">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8d057-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8d057-147">Выберите значение "Электронно".</span><span class="sxs-lookup"><span data-stu-id="8d057-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="8d057-148">В поле "Имя файла" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8d057-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="8d057-149">Например, введите "платежи".</span><span class="sxs-lookup"><span data-stu-id="8d057-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="8d057-150">В поле "Банковский счет" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8d057-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="8d057-151">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8d057-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8d057-152">Выберите значение GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="8d057-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="8d057-153">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8d057-153">Click OK.</span></span>
25. <span data-ttu-id="8d057-154">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8d057-154">Click OK.</span></span>
    * <span data-ttu-id="8d057-155">Проанализируйте созданный файл платежа в формате XML.</span><span class="sxs-lookup"><span data-stu-id="8d057-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="8d057-156">Сравните его с созданным макетом документа и определенными атрибутами проводки по оплате.</span><span class="sxs-lookup"><span data-stu-id="8d057-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  


