--- 
title: "Учет периодических журналов"
description: "Периодические журналы иногда называются повторяющимися журналами, поскольку сумма, текст и другие сведения повторяются при каждом извлечении периодического журнала."
author: aprilolson
manager: AnnBe
ms.date: 02/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 233d145a9d3441ffc2b816b8514e58988b517136
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="post-periodic-journals"></a><span data-ttu-id="d6f87-103">Учет периодических журналов</span><span class="sxs-lookup"><span data-stu-id="d6f87-103">Post periodic journals</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d6f87-104">Периодические журналы иногда называются повторяющимися журналами, поскольку сумма, текст и другие сведения повторяются при каждом извлечении периодического журнала.</span><span class="sxs-lookup"><span data-stu-id="d6f87-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="d6f87-105">При создании периодического журнала следует указать интервал периода повторения, например в днях или месяцах.</span><span class="sxs-lookup"><span data-stu-id="d6f87-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="d6f87-106">В этом руководстве по задаче будет создан периодический журнал с ежемесячным повторением.</span><span class="sxs-lookup"><span data-stu-id="d6f87-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>



1. <span data-ttu-id="d6f87-107">Перейдите в раздел "Главная книга" > "Периодические задачи" > "Периодические журналы".</span><span class="sxs-lookup"><span data-stu-id="d6f87-107">Go to General ledger > Periodic tasks > Periodic journals.</span></span>
2. <span data-ttu-id="d6f87-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d6f87-108">Click New.</span></span>
3. <span data-ttu-id="d6f87-109">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6f87-109">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="d6f87-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d6f87-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d6f87-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d6f87-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d6f87-112">Описанием будет имя периодического журнала при дальнейшем извлечении, поэтому присвойте ему соответствующее имя.</span><span class="sxs-lookup"><span data-stu-id="d6f87-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>  
6. <span data-ttu-id="d6f87-113">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="d6f87-113">Click Lines.</span></span>
    * <span data-ttu-id="d6f87-114">Периодический журнал обычно включает несколько строк журнала.</span><span class="sxs-lookup"><span data-stu-id="d6f87-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="d6f87-115">Однако в этом руководстве по задаче будет добавлена только одна строка.</span><span class="sxs-lookup"><span data-stu-id="d6f87-115">this task guide will however only add one line.</span></span>  
7. <span data-ttu-id="d6f87-116">В поле "Дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="d6f87-116">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="d6f87-117">В поле "Дата" указана дата разноски для следующего перемещения в ежедневный журнал.</span><span class="sxs-lookup"><span data-stu-id="d6f87-117">The Date field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="d6f87-118">В случае журналов, которые будут извлекаться каждый месяц, рекомендуется использовать дату в месяце его разноски, обычно это первая или последняя дата в периоде.</span><span class="sxs-lookup"><span data-stu-id="d6f87-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="d6f87-119">Можно оставить поле даты пустым и указать дату при извлечении журнала с помощью поля "Пустая дата".</span><span class="sxs-lookup"><span data-stu-id="d6f87-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span>    <span data-ttu-id="d6f87-120">Поле автоматически обновляется для отображения следующей повторяющейся даты извлечения проводок.</span><span class="sxs-lookup"><span data-stu-id="d6f87-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span>  
8. <span data-ttu-id="d6f87-121">В поле "Счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="d6f87-121">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="d6f87-122">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d6f87-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="d6f87-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d6f87-123">Close the page.</span></span>
11. <span data-ttu-id="d6f87-124">В поле "Дебет" введите число.</span><span class="sxs-lookup"><span data-stu-id="d6f87-124">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="d6f87-125">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="d6f87-125">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="d6f87-126">В поле "Единица измерения" выберите "Месяцы".</span><span class="sxs-lookup"><span data-stu-id="d6f87-126">In the Unit field, select 'Months'.</span></span>
14. <span data-ttu-id="d6f87-127">В поле "Число единиц" введите значение "1".</span><span class="sxs-lookup"><span data-stu-id="d6f87-127">In the Number of units field, enter '1'.</span></span>
15. <span data-ttu-id="d6f87-128">В поле "Последняя дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="d6f87-128">In the Last date field, enter a date.</span></span>
    * <span data-ttu-id="d6f87-129">Ввод последней даты в предыдущем периоде поможет предотвратить создание повторяющегося журнала по ошибке в неправильном начальном периоде.</span><span class="sxs-lookup"><span data-stu-id="d6f87-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="d6f87-130">Последняя дата в дальнейшем будет обновляться при каждом извлечении периодического журнала.</span><span class="sxs-lookup"><span data-stu-id="d6f87-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span>  
16. <span data-ttu-id="d6f87-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d6f87-131">Click Save.</span></span>
17. <span data-ttu-id="d6f87-132">Перейдите на панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d6f87-132">Go to Default dashboard.</span></span>
18. <span data-ttu-id="d6f87-133">Перейдите в раздел "Главная книга" > "Записи в журнале" > "Общие журналы".</span><span class="sxs-lookup"><span data-stu-id="d6f87-133">Go to General ledger > Journal entries > General journals.</span></span>
19. <span data-ttu-id="d6f87-134">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d6f87-134">Click New.</span></span>
20. <span data-ttu-id="d6f87-135">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6f87-135">In the Name field, enter or select a value.</span></span>
21. <span data-ttu-id="d6f87-136">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="d6f87-136">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="d6f87-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d6f87-137">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="d6f87-138">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d6f87-138">In the Description field, type a value.</span></span>
24. <span data-ttu-id="d6f87-139">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="d6f87-139">Click Lines.</span></span>
25. <span data-ttu-id="d6f87-140">Щелкните "Периодический журнал".</span><span class="sxs-lookup"><span data-stu-id="d6f87-140">Click Period journal.</span></span>
26. <span data-ttu-id="d6f87-141">Щелкните "Восстановить журнал".</span><span class="sxs-lookup"><span data-stu-id="d6f87-141">Click Retrieve journal.</span></span>
27. <span data-ttu-id="d6f87-142">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="d6f87-142">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="d6f87-143">Дата окончания служит в качестве даты прекращения для строк периодического ваучера.</span><span class="sxs-lookup"><span data-stu-id="d6f87-143">The To date serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="d6f87-144">На основании настройки повторения, последней даты и даты окончания одна и та же строка может быть включена в итоговый журнал несколько раз.</span><span class="sxs-lookup"><span data-stu-id="d6f87-144">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="d6f87-145">Дата окончания автоматически обновляется на основании даты сеанса последнего переноса периодической строки в журнал.</span><span class="sxs-lookup"><span data-stu-id="d6f87-145">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span>  
28. <span data-ttu-id="d6f87-146">В поле "Номер периодического журнала" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6f87-146">In the Periodic journal number field, enter or select a value.</span></span>
29. <span data-ttu-id="d6f87-147">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d6f87-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="d6f87-148">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d6f87-148">Click OK.</span></span>
    * <span data-ttu-id="d6f87-149">Периодический журнал теперь можно извлечь, утвердить или разнести в зависимости от требований и настройки.</span><span class="sxs-lookup"><span data-stu-id="d6f87-149">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>  


