--- 
title: "Создание последовательности писем-напоминаний"
description: "Используйте это руководство по задаче для создания последовательности писем-напоминаний."
author: mikefalkner
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: db5264f6d8d7723ff01d13e99728c2bfebcb4515
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="212ce-103">Создание последовательности писем-напоминаний</span><span class="sxs-lookup"><span data-stu-id="212ce-103">Create a collection letter sequence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="212ce-104">Используйте это руководство по задаче для создания последовательности писем-напоминаний.</span><span class="sxs-lookup"><span data-stu-id="212ce-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="212ce-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="212ce-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="212ce-106">Перейдите в раздел "Кредит и сборы" > "Настройка" > "Настройка последовательности писем-напоминаний".</span><span class="sxs-lookup"><span data-stu-id="212ce-106">Go to Credit and collections > Setup > Set up collection letter sequence.</span></span>
2. <span data-ttu-id="212ce-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="212ce-107">Click New.</span></span>
3. <span data-ttu-id="212ce-108">В поле "Последовательность писем-напоминаний" введите код последовательности, который будет представлять последовательность.</span><span class="sxs-lookup"><span data-stu-id="212ce-108">In the Collection letter sequence field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="212ce-109">Он будет использоваться при настройке профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="212ce-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="212ce-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="212ce-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="212ce-111">Поле "Условия оплаты" является необязательным.</span><span class="sxs-lookup"><span data-stu-id="212ce-111">The terms of payment is optional.</span></span> <span data-ttu-id="212ce-112">Если здесь ввести значение, в накладной сбора за письмо-напоминание будут использовать эти условия оплаты вместо условий оплаты, сохраненных с клиентом.</span><span class="sxs-lookup"><span data-stu-id="212ce-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="212ce-113">В поле "Код письма-напоминания" выберите код первого письма-напоминания, которое требуется отправить.</span><span class="sxs-lookup"><span data-stu-id="212ce-113">In the collection letter code field, select the code for the first collection letter that you want to send.</span></span>
    * <span data-ttu-id="212ce-114">Первое письмо-напоминание будет создано в соответствии с датой оплаты в накладной, значения для льготного периода, введенного в поле "Дни" для этой строки и другими сведениями для нее.</span><span class="sxs-lookup"><span data-stu-id="212ce-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="212ce-115">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="212ce-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="212ce-116">В качестве валюты для сбора по умолчанию используется валюта клиента.</span><span class="sxs-lookup"><span data-stu-id="212ce-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="212ce-117">Этот код валюты может отличаться от валюты накладной.</span><span class="sxs-lookup"><span data-stu-id="212ce-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="212ce-118">Нажмите кнопку "Добавить", чтобы добавить следующее письмо-напоминание, которое будет отправлено в последовательности.</span><span class="sxs-lookup"><span data-stu-id="212ce-118">Click Add to add the next collection letter that will be sent in the sequence</span></span>
    * <span data-ttu-id="212ce-119">Во многих случаях первое письмо-напоминание будет просто предупреждением.</span><span class="sxs-lookup"><span data-stu-id="212ce-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="212ce-120">Можно добавить сборы при необходимости.</span><span class="sxs-lookup"><span data-stu-id="212ce-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="212ce-121">В поле "Код письма-напоминания" выберите код следующего письма-напоминания, которое будет отправлено в последовательности.</span><span class="sxs-lookup"><span data-stu-id="212ce-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="212ce-122">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="212ce-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="212ce-123">В поле "Счет ГК" выберите счет выручки, который будет использоваться для сборов.</span><span class="sxs-lookup"><span data-stu-id="212ce-123">In the main account field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="212ce-124">Введите сбор, который будет взиматься при разноске этого письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="212ce-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="212ce-125">В поле "Налоговая группа номенклатур" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="212ce-125">In the Item sales tax group field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="212ce-126">Выберите налоговую группу номенклатур, если необходимо рассчитать налоги на сборы.</span><span class="sxs-lookup"><span data-stu-id="212ce-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="212ce-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="212ce-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="212ce-128">Введите минимальное необходимое просроченное сальдо для отправки письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="212ce-128">Enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="212ce-129">Введите число дней допустимого льготного периода.</span><span class="sxs-lookup"><span data-stu-id="212ce-129">Enter the number of grace days that you will allow.</span></span>
    * <span data-ttu-id="212ce-130">Это количество дней после срока выполнения, по прошествии которых можно создать письмо-напоминание.</span><span class="sxs-lookup"><span data-stu-id="212ce-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="212ce-131">Срок выполнения, используемый для расчета, зависит от положения письма-напоминания в последовательности писем-напоминаний:   ⦁    Льготный период для письма-напоминания 1 относится к сроку выполнения в накладной.</span><span class="sxs-lookup"><span data-stu-id="212ce-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:   ⦁    The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>  <span data-ttu-id="212ce-132">⦁ Льготный период для письма-напоминания 2 и выше относится к дате разноски или печати предыдущего письма-напоминания в зависимости от выбора в поле "Обновить код письма-напоминания" на странице "Параметры расчетов с клиентами".</span><span class="sxs-lookup"><span data-stu-id="212ce-132">⦁ The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="212ce-133">Нажмите кнопку "Добавить", чтобы добавить последнее письмо-напоминание в последовательности.</span><span class="sxs-lookup"><span data-stu-id="212ce-133">Click Add to add the last collection letter in the sequence.</span></span>
    * <span data-ttu-id="212ce-134">Для последовательности писем-напоминаний может быть добавлено до пяти кодов писем-напоминаний.</span><span class="sxs-lookup"><span data-stu-id="212ce-134">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="212ce-135">В поле "Код письма-напоминания" выберите код следующего письма-напоминания, которое будет отправлено в последовательности.</span><span class="sxs-lookup"><span data-stu-id="212ce-135">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="212ce-136">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="212ce-136">In the Description field, type a value.</span></span>
19. <span data-ttu-id="212ce-137">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="212ce-137">In the Main account field, specify the desired values.</span></span>
20. <span data-ttu-id="212ce-138">В поле "Сбор в валюте" введите число.</span><span class="sxs-lookup"><span data-stu-id="212ce-138">In the Fee in currency field, enter a number.</span></span>
21. <span data-ttu-id="212ce-139">В поле "Налоговая группа номенклатур" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="212ce-139">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="212ce-140">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="212ce-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="212ce-141">В поле "Минимальное просроченное сальдо" введите число.</span><span class="sxs-lookup"><span data-stu-id="212ce-141">In the Minimum overdue balance field, enter a number.</span></span>
24. <span data-ttu-id="212ce-142">В поле "Дни" введите число.</span><span class="sxs-lookup"><span data-stu-id="212ce-142">In the Days field, enter a number.</span></span>
25. <span data-ttu-id="212ce-143">Этот флажок следует установить, чтобы остановить дополнительную доставку и выставление накладных для клиента.</span><span class="sxs-lookup"><span data-stu-id="212ce-143">Select this check box to stop the customer from additional deliveries and invoicing.</span></span>
    * <span data-ttu-id="212ce-144">Чтобы разблокировать счет, выберите "Нет" в поле "Блокировка выставления накладных и поставки" на странице "Клиенты".</span><span class="sxs-lookup"><span data-stu-id="212ce-144">To unblock the account, select No in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="212ce-145">Разверните экспресс-вкладку "Примечание".</span><span class="sxs-lookup"><span data-stu-id="212ce-145">Expand the Note fasttab.</span></span>
27. <span data-ttu-id="212ce-146">Введите текст, который будет отображаться в письме-напоминании для выбранного кода письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="212ce-146">Enter the text to appear on the collection letter for the selected collection letter code.</span></span>
    * <span data-ttu-id="212ce-147">Этот текст можно перевести на несколько языков с помощью меню "Переводы" над полем примечания.</span><span class="sxs-lookup"><span data-stu-id="212ce-147">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  


