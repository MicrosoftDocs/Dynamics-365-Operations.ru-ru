---
title: Учет периодических журналов
description: Периодические журналы иногда называются повторяющимися журналами, поскольку сумма, текст и другие сведения повторяются при каждом извлечении периодического журнала.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 241023c36723fa2dba5646e997b649741142c0ad
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834958"
---
# <a name="post-periodic-journals"></a><span data-ttu-id="cb66a-103">Учет периодических журналов</span><span class="sxs-lookup"><span data-stu-id="cb66a-103">Post periodic journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cb66a-104">Периодические журналы иногда называются повторяющимися журналами, поскольку сумма, текст и другие сведения повторяются при каждом извлечении периодического журнала.</span><span class="sxs-lookup"><span data-stu-id="cb66a-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="cb66a-105">При создании периодического журнала следует указать интервал периода повторения, например в днях или месяцах.</span><span class="sxs-lookup"><span data-stu-id="cb66a-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="cb66a-106">В этом руководстве по задаче будет создан периодический журнал с ежемесячным повторением.</span><span class="sxs-lookup"><span data-stu-id="cb66a-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>



1. <span data-ttu-id="cb66a-107">Перейдите в раздел "Главная книга" > "Периодические задачи" > "Периодические журналы".</span><span class="sxs-lookup"><span data-stu-id="cb66a-107">Go to General ledger > Periodic tasks > Periodic journals.</span></span>
2. <span data-ttu-id="cb66a-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="cb66a-108">Click New.</span></span>
3. <span data-ttu-id="cb66a-109">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="cb66a-109">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="cb66a-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="cb66a-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="cb66a-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cb66a-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="cb66a-112">Описанием будет имя периодического журнала при дальнейшем извлечении, поэтому присвойте ему соответствующее имя.</span><span class="sxs-lookup"><span data-stu-id="cb66a-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>  
6. <span data-ttu-id="cb66a-113">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="cb66a-113">Click Lines.</span></span>
    * <span data-ttu-id="cb66a-114">Периодический журнал обычно включает несколько строк журнала.</span><span class="sxs-lookup"><span data-stu-id="cb66a-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="cb66a-115">Однако в этом руководстве по задаче будет добавлена только одна строка.</span><span class="sxs-lookup"><span data-stu-id="cb66a-115">this task guide will however only add one line.</span></span>  
7. <span data-ttu-id="cb66a-116">В поле "Дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="cb66a-116">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="cb66a-117">В поле "Дата" указана дата разноски для следующего перемещения в ежедневный журнал.</span><span class="sxs-lookup"><span data-stu-id="cb66a-117">The Date field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="cb66a-118">В случае журналов, которые будут извлекаться каждый месяц, рекомендуется использовать дату в месяце его разноски, обычно это первая или последняя дата в периоде.</span><span class="sxs-lookup"><span data-stu-id="cb66a-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="cb66a-119">Можно оставить поле даты пустым и указать дату при извлечении журнала с помощью поля "Пустая дата".</span><span class="sxs-lookup"><span data-stu-id="cb66a-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span>    <span data-ttu-id="cb66a-120">Поле автоматически обновляется для отображения следующей повторяющейся даты извлечения проводок.</span><span class="sxs-lookup"><span data-stu-id="cb66a-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span>  
8. <span data-ttu-id="cb66a-121">В поле "Счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="cb66a-121">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="cb66a-122">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cb66a-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="cb66a-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="cb66a-123">Close the page.</span></span>
11. <span data-ttu-id="cb66a-124">В поле "Дебет" введите число.</span><span class="sxs-lookup"><span data-stu-id="cb66a-124">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="cb66a-125">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="cb66a-125">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="cb66a-126">В поле "Единица измерения" выберите "Месяцы".</span><span class="sxs-lookup"><span data-stu-id="cb66a-126">In the Unit field, select 'Months'.</span></span>
14. <span data-ttu-id="cb66a-127">В поле "Число единиц" введите значение "1".</span><span class="sxs-lookup"><span data-stu-id="cb66a-127">In the Number of units field, enter '1'.</span></span>
15. <span data-ttu-id="cb66a-128">В поле "Последняя дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="cb66a-128">In the Last date field, enter a date.</span></span>
    * <span data-ttu-id="cb66a-129">Ввод последней даты в предыдущем периоде поможет предотвратить создание повторяющегося журнала по ошибке в неправильном начальном периоде.</span><span class="sxs-lookup"><span data-stu-id="cb66a-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="cb66a-130">Последняя дата в дальнейшем будет обновляться при каждом извлечении периодического журнала.</span><span class="sxs-lookup"><span data-stu-id="cb66a-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span>  
16. <span data-ttu-id="cb66a-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="cb66a-131">Click Save.</span></span>
17. <span data-ttu-id="cb66a-132">Перейдите на панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cb66a-132">Go to Default dashboard.</span></span>
18. <span data-ttu-id="cb66a-133">Перейдите в раздел "Главная книга" > "Записи в журнале" > "Общие журналы".</span><span class="sxs-lookup"><span data-stu-id="cb66a-133">Go to General ledger > Journal entries > General journals.</span></span>
19. <span data-ttu-id="cb66a-134">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="cb66a-134">Click New.</span></span>
20. <span data-ttu-id="cb66a-135">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="cb66a-135">In the Name field, enter or select a value.</span></span>
21. <span data-ttu-id="cb66a-136">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="cb66a-136">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="cb66a-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="cb66a-137">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="cb66a-138">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cb66a-138">In the Description field, type a value.</span></span>
24. <span data-ttu-id="cb66a-139">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="cb66a-139">Click Lines.</span></span>
25. <span data-ttu-id="cb66a-140">Щелкните "Периодический журнал".</span><span class="sxs-lookup"><span data-stu-id="cb66a-140">Click Period journal.</span></span>
26. <span data-ttu-id="cb66a-141">Щелкните "Восстановить журнал".</span><span class="sxs-lookup"><span data-stu-id="cb66a-141">Click Retrieve journal.</span></span>
27. <span data-ttu-id="cb66a-142">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="cb66a-142">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="cb66a-143">Дата окончания служит в качестве даты прекращения для строк периодического ваучера.</span><span class="sxs-lookup"><span data-stu-id="cb66a-143">The To date serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="cb66a-144">На основании настройки повторения, последней даты и даты окончания одна и та же строка может быть включена в итоговый журнал несколько раз.</span><span class="sxs-lookup"><span data-stu-id="cb66a-144">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="cb66a-145">Дата окончания автоматически обновляется на основании даты сеанса последнего переноса периодической строки в журнал.</span><span class="sxs-lookup"><span data-stu-id="cb66a-145">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span>  
28. <span data-ttu-id="cb66a-146">В поле "Номер периодического журнала" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="cb66a-146">In the Periodic journal number field, enter or select a value.</span></span>
29. <span data-ttu-id="cb66a-147">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="cb66a-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="cb66a-148">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="cb66a-148">Click OK.</span></span>
    * <span data-ttu-id="cb66a-149">Периодический журнал теперь можно извлечь, утвердить или разнести в зависимости от требований и настройки.</span><span class="sxs-lookup"><span data-stu-id="cb66a-149">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>  

