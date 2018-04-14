---
title: "Создание и обработка соответствия"
description: "Эта процедура используется для управление несоответствием на основании существующего заказа контроля качества."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: adecf9b2ea29abaee378f1c02c64551c3aeede6d
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="e81fe-103">Создание и обработка соответствия</span><span class="sxs-lookup"><span data-stu-id="e81fe-103">Create and process a conformance</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e81fe-104">Эта процедура используется для управление несоответствием на основании существующего заказа контроля качества.</span><span class="sxs-lookup"><span data-stu-id="e81fe-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="e81fe-105">Эту запись можно выполнить в компании демонстрации USMF и использовать предложенные значения.</span><span class="sxs-lookup"><span data-stu-id="e81fe-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="e81fe-106">Обычно эта процедура выполняется сотрудником отдела контроля качества.</span><span class="sxs-lookup"><span data-stu-id="e81fe-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="e81fe-107">В качестве предварительного условия необходимо воспроизвести запись задачи "Контроль качества товаров".</span><span class="sxs-lookup"><span data-stu-id="e81fe-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="e81fe-108">Чтобы обработать утверждение несоответствия, пользователь, запустивший запись задачи, должен иметь значение "Имя", назначенное на странице "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="e81fe-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="e81fe-109">Для использования примечаний к документам у пользователя также должна быть активирована функция "Работа с документами" (в параметрах пользователя).</span><span class="sxs-lookup"><span data-stu-id="e81fe-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="e81fe-110">Выбор заказа контроля качества</span><span class="sxs-lookup"><span data-stu-id="e81fe-110">Select a quality order</span></span>
1. <span data-ttu-id="e81fe-111">Перейдите в раздел "Заказы контроля качества".</span><span class="sxs-lookup"><span data-stu-id="e81fe-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="e81fe-112">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="e81fe-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e81fe-113">Выберите заказ контроля качества, который был создан из записи задачи "Контроль качества товаров".</span><span class="sxs-lookup"><span data-stu-id="e81fe-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="e81fe-114">Создание несоответствия</span><span class="sxs-lookup"><span data-stu-id="e81fe-114">Create a nonconformance</span></span>
1. <span data-ttu-id="e81fe-115">Щелкните Запросы.</span><span class="sxs-lookup"><span data-stu-id="e81fe-115">Click Inquiries.</span></span>
2. <span data-ttu-id="e81fe-116">Щелкните "Несоответствия".</span><span class="sxs-lookup"><span data-stu-id="e81fe-116">Click Non conformances.</span></span>
3. <span data-ttu-id="e81fe-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="e81fe-117">Click New.</span></span>
4. <span data-ttu-id="e81fe-118">В поле "Тип проблемы" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e81fe-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e81fe-119">Выберите проблему, которая была найдена в процессе проверки.</span><span class="sxs-lookup"><span data-stu-id="e81fe-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="e81fe-120">В поле "Тип проблемы" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e81fe-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e81fe-121">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="e81fe-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e81fe-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="e81fe-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e81fe-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e81fe-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="e81fe-124">Утверждение/отклонение несоответствия</span><span class="sxs-lookup"><span data-stu-id="e81fe-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="e81fe-125">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="e81fe-125">Click Functions.</span></span>
2. <span data-ttu-id="e81fe-126">Щелкните "Утвердить несоответствие".</span><span class="sxs-lookup"><span data-stu-id="e81fe-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="e81fe-127">В этом примере утвердите несоответствие.</span><span class="sxs-lookup"><span data-stu-id="e81fe-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="e81fe-128">Утвержденные несоответствия могут быть связаны с сопутствующими операциями для записи работы, которая выполняется в рамках обработки несоответствия и, как в этой записи задачи, обработки исправления.</span><span class="sxs-lookup"><span data-stu-id="e81fe-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="e81fe-129">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="e81fe-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="e81fe-130">Создание действия исправления</span><span class="sxs-lookup"><span data-stu-id="e81fe-130">Create a correction action</span></span>
1. <span data-ttu-id="e81fe-131">Щелкните "Исправления".</span><span class="sxs-lookup"><span data-stu-id="e81fe-131">Click Corrections.</span></span>
2. <span data-ttu-id="e81fe-132">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="e81fe-132">Click New.</span></span>
3. <span data-ttu-id="e81fe-133">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="e81fe-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e81fe-134">В поле "Табельный номер" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e81fe-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e81fe-135">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="e81fe-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e81fe-136">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="e81fe-136">Click Select.</span></span>
7. <span data-ttu-id="e81fe-137">Щелкните "Привязать".</span><span class="sxs-lookup"><span data-stu-id="e81fe-137">Click Attach.</span></span>
    * <span data-ttu-id="e81fe-138">Создайте примечание об исправлении.</span><span class="sxs-lookup"><span data-stu-id="e81fe-138">Create a note about the correction.</span></span> <span data-ttu-id="e81fe-139">В этом примере действие — обратиться к поставщику, чтобы обсудить случай несоответствия.</span><span class="sxs-lookup"><span data-stu-id="e81fe-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="e81fe-140">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="e81fe-140">Click New.</span></span>
9. <span data-ttu-id="e81fe-141">Щелкните "Примечание".</span><span class="sxs-lookup"><span data-stu-id="e81fe-141">Click Note.</span></span>
    * <span data-ttu-id="e81fe-142">Обратите внимание, что в зависимости от настройки отчета, можно печатать различные типы документов в отчетах, связанных с управлением несоответствиями.</span><span class="sxs-lookup"><span data-stu-id="e81fe-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="e81fe-143">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e81fe-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="e81fe-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e81fe-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="e81fe-145">Ведение исправления</span><span class="sxs-lookup"><span data-stu-id="e81fe-145">Maintain a correction</span></span>
1. <span data-ttu-id="e81fe-146">Щелкните "Отметить как завершенный".</span><span class="sxs-lookup"><span data-stu-id="e81fe-146">Click Mark complete.</span></span>
2. <span data-ttu-id="e81fe-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e81fe-147">Click OK.</span></span>
3. <span data-ttu-id="e81fe-148">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e81fe-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="e81fe-149">Закрытие несоответствия</span><span class="sxs-lookup"><span data-stu-id="e81fe-149">Close a nonconformance</span></span>
1. <span data-ttu-id="e81fe-150">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="e81fe-150">Click Functions.</span></span>
2. <span data-ttu-id="e81fe-151">Щелкните "Закрыть несоответствие".</span><span class="sxs-lookup"><span data-stu-id="e81fe-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="e81fe-152">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="e81fe-152">Click Yes.</span></span>
4. <span data-ttu-id="e81fe-153">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e81fe-153">Close the page.</span></span>
5. <span data-ttu-id="e81fe-154">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e81fe-154">Close the page.</span></span>

