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
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: e5187c44aac881273900b2fc0ca91045a65cd838
ms.contentlocale: ru-ru
ms.lasthandoff: 09/12/2017

---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="bf4e5-103">Создание и обработка соответствия</span><span class="sxs-lookup"><span data-stu-id="bf4e5-103">Create and process a conformance</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bf4e5-104">Эта процедура используется для управление несоответствием на основании существующего заказа контроля качества.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="bf4e5-105">Эту запись можно выполнить в компании демонстрации USMF и использовать предложенные значения.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="bf4e5-106">Обычно эта процедура выполняется сотрудником отдела контроля качества.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="bf4e5-107">В качестве предварительного условия необходимо воспроизвести запись задачи "Контроль качества товаров".</span><span class="sxs-lookup"><span data-stu-id="bf4e5-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="bf4e5-108">Чтобы обработать утверждение несоответствия, пользователь, запустивший запись задачи, должен иметь значение "Имя", назначенное на странице "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="bf4e5-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="bf4e5-109">Для использования примечаний к документам у пользователя также должна быть активирована функция "Работа с документами" (в параметрах пользователя).</span><span class="sxs-lookup"><span data-stu-id="bf4e5-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="bf4e5-110">Выбор заказа контроля качества</span><span class="sxs-lookup"><span data-stu-id="bf4e5-110">Select a quality order</span></span>
1. <span data-ttu-id="bf4e5-111">Перейдите в раздел "Заказы контроля качества".</span><span class="sxs-lookup"><span data-stu-id="bf4e5-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="bf4e5-112">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bf4e5-113">Выберите заказ контроля качества, который был создан из записи задачи "Контроль качества товаров".</span><span class="sxs-lookup"><span data-stu-id="bf4e5-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="bf4e5-114">Создание несоответствия</span><span class="sxs-lookup"><span data-stu-id="bf4e5-114">Create a nonconformance</span></span>
1. <span data-ttu-id="bf4e5-115">Щелкните Запросы.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-115">Click Inquiries.</span></span>
2. <span data-ttu-id="bf4e5-116">Щелкните "Несоответствия".</span><span class="sxs-lookup"><span data-stu-id="bf4e5-116">Click Non conformances.</span></span>
3. <span data-ttu-id="bf4e5-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bf4e5-117">Click New.</span></span>
4. <span data-ttu-id="bf4e5-118">В поле "Тип проблемы" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bf4e5-119">Выберите проблему, которая была найдена в процессе проверки.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="bf4e5-120">В поле "Тип проблемы" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="bf4e5-121">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="bf4e5-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="bf4e5-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bf4e5-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="bf4e5-124">Утверждение/отклонение несоответствия</span><span class="sxs-lookup"><span data-stu-id="bf4e5-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="bf4e5-125">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-125">Click Functions.</span></span>
2. <span data-ttu-id="bf4e5-126">Щелкните "Утвердить несоответствие".</span><span class="sxs-lookup"><span data-stu-id="bf4e5-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="bf4e5-127">В этом примере утвердите несоответствие.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="bf4e5-128">Утвержденные несоответствия могут быть связаны с сопутствующими операциями для записи работы, которая выполняется в рамках обработки несоответствия и, как в этой записи задачи, обработки исправления.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="bf4e5-129">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="bf4e5-130">Создание действия исправления</span><span class="sxs-lookup"><span data-stu-id="bf4e5-130">Create a correction action</span></span>
1. <span data-ttu-id="bf4e5-131">Щелкните "Исправления".</span><span class="sxs-lookup"><span data-stu-id="bf4e5-131">Click Corrections.</span></span>
2. <span data-ttu-id="bf4e5-132">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bf4e5-132">Click New.</span></span>
3. <span data-ttu-id="bf4e5-133">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="bf4e5-134">В поле "Табельный номер" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="bf4e5-135">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="bf4e5-136">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-136">Click Select.</span></span>
7. <span data-ttu-id="bf4e5-137">Щелкните "Привязать".</span><span class="sxs-lookup"><span data-stu-id="bf4e5-137">Click Attach.</span></span>
    * <span data-ttu-id="bf4e5-138">Создайте примечание об исправлении.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-138">Create a note about the correction.</span></span> <span data-ttu-id="bf4e5-139">В этом примере действие — обратиться к поставщику, чтобы обсудить случай несоответствия.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="bf4e5-140">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bf4e5-140">Click New.</span></span>
9. <span data-ttu-id="bf4e5-141">Щелкните "Примечание".</span><span class="sxs-lookup"><span data-stu-id="bf4e5-141">Click Note.</span></span>
    * <span data-ttu-id="bf4e5-142">Обратите внимание, что в зависимости от настройки отчета, можно печатать различные типы документов в отчетах, связанных с управлением несоответствиями.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="bf4e5-143">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="bf4e5-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="bf4e5-145">Ведение исправления</span><span class="sxs-lookup"><span data-stu-id="bf4e5-145">Maintain a correction</span></span>
1. <span data-ttu-id="bf4e5-146">Щелкните "Отметить как завершенный".</span><span class="sxs-lookup"><span data-stu-id="bf4e5-146">Click Mark complete.</span></span>
2. <span data-ttu-id="bf4e5-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bf4e5-147">Click OK.</span></span>
3. <span data-ttu-id="bf4e5-148">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="bf4e5-149">Закрытие несоответствия</span><span class="sxs-lookup"><span data-stu-id="bf4e5-149">Close a nonconformance</span></span>
1. <span data-ttu-id="bf4e5-150">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-150">Click Functions.</span></span>
2. <span data-ttu-id="bf4e5-151">Щелкните "Закрыть несоответствие".</span><span class="sxs-lookup"><span data-stu-id="bf4e5-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="bf4e5-152">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-152">Click Yes.</span></span>
4. <span data-ttu-id="bf4e5-153">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-153">Close the page.</span></span>
5. <span data-ttu-id="bf4e5-154">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bf4e5-154">Close the page.</span></span>

