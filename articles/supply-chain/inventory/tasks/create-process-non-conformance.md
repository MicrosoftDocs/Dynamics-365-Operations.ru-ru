---
title: Создание и обработка соответствия
description: В этой теме рассматривается порядок управления несоответствием на основании существующего заказа контроля качества.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bf20ed737707b7cf99023e3c78489caf4a68eab
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383627"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="943ff-103">Создание и обработка соответствия</span><span class="sxs-lookup"><span data-stu-id="943ff-103">Create and process a conformance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="943ff-104">В этой теме рассматривается порядок управления несоответствием на основании существующего заказа контроля качества.</span><span class="sxs-lookup"><span data-stu-id="943ff-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="943ff-105">Эту запись можно выполнить в компании демонстрации USMF и использовать предложенные значения.</span><span class="sxs-lookup"><span data-stu-id="943ff-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="943ff-106">Обычно эта процедура выполняется сотрудником отдела контроля качества.</span><span class="sxs-lookup"><span data-stu-id="943ff-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="943ff-107">В качестве предварительного условия выполните инструкции из раздела [Контроль качества товаров](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="943ff-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="943ff-108">Чтобы обработать утверждение несоответствия, пользователь, запустивший запись задачи, должен иметь значение "Имя", назначенное на странице "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="943ff-108">To process the approval of a nonconformance, the user who runs the task recording must have a "Name" value assigned on the Users page.</span></span> <span data-ttu-id="943ff-109">Для использования примечаний к документам у пользователя также должна быть активирована функция "Работа с документами" (в параметрах пользователя).</span><span class="sxs-lookup"><span data-stu-id="943ff-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="943ff-110">Выбор заказа контроля качества</span><span class="sxs-lookup"><span data-stu-id="943ff-110">Select a quality order</span></span>
1. <span data-ttu-id="943ff-111">В области перехода перейдите к **Модули > Управление запасами > Периодические задачи > Управление качеством > Заказы на контроль качества**.</span><span class="sxs-lookup"><span data-stu-id="943ff-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="943ff-112">В списке выберите заказ контроля качества, который был создан в разделе [Контроль качества товаров](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="943ff-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="943ff-113">Создание несоответствия</span><span class="sxs-lookup"><span data-stu-id="943ff-113">Create a nonconformance</span></span>
1. <span data-ttu-id="943ff-114">На панели операций выберите **Запросы**.</span><span class="sxs-lookup"><span data-stu-id="943ff-114">On the Action Pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="943ff-115">Выберите **Несоответствия**.</span><span class="sxs-lookup"><span data-stu-id="943ff-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="943ff-116">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="943ff-116">Select **New**.</span></span>
4. <span data-ttu-id="943ff-117">В раскрывающемся меню поля **Тип проблемы** выберите проблему, которая была обнаружена во время процесса проверки.</span><span class="sxs-lookup"><span data-stu-id="943ff-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="943ff-118">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="943ff-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="943ff-119">Утверждение/отклонение несоответствия</span><span class="sxs-lookup"><span data-stu-id="943ff-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="943ff-120">Выберите **Функции**.</span><span class="sxs-lookup"><span data-stu-id="943ff-120">Select **Functions**.</span></span>
2. <span data-ttu-id="943ff-121">Выберите **Утвердить несоответствие**.</span><span class="sxs-lookup"><span data-stu-id="943ff-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="943ff-122">В этом примере утвердите несоответствие.</span><span class="sxs-lookup"><span data-stu-id="943ff-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="943ff-123">Утвержденные несоответствия могут быть связаны с сопутствующими операциями для записи работы, которая выполняется в рамках обработки несоответствия и, как в этой теме, обработки исправления.</span><span class="sxs-lookup"><span data-stu-id="943ff-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="943ff-124">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="943ff-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="943ff-125">Создание действия исправления</span><span class="sxs-lookup"><span data-stu-id="943ff-125">Create a correction action</span></span>
1. <span data-ttu-id="943ff-126">Выберите **Коррекции**.</span><span class="sxs-lookup"><span data-stu-id="943ff-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="943ff-127">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="943ff-127">Select **New**.</span></span>
3. <span data-ttu-id="943ff-128">В поле **Табельный номер** в новой строке выберите требуемую запись из раскрывающегося меню.</span><span class="sxs-lookup"><span data-stu-id="943ff-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="943ff-129">Щелкните **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="943ff-129">Click **Select**.</span></span>
5. <span data-ttu-id="943ff-130">Выберите **Привязать**.</span><span class="sxs-lookup"><span data-stu-id="943ff-130">Select **Attach**.</span></span> <span data-ttu-id="943ff-131">Создайте примечание об исправлении.</span><span class="sxs-lookup"><span data-stu-id="943ff-131">Create a note about the correction.</span></span> <span data-ttu-id="943ff-132">В этом примере действие — обратиться к поставщику, чтобы обсудить случай несоответствия.</span><span class="sxs-lookup"><span data-stu-id="943ff-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="943ff-133">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="943ff-133">Select **New**.</span></span>
7. <span data-ttu-id="943ff-134">Выберите **Примечание**.</span><span class="sxs-lookup"><span data-stu-id="943ff-134">Select **Note**.</span></span> <span data-ttu-id="943ff-135">В зависимости от настройки отчета, можно печатать различные типы документов в отчетах, связанных с управлением несоответствиями.</span><span class="sxs-lookup"><span data-stu-id="943ff-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="943ff-136">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="943ff-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="943ff-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="943ff-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="943ff-138">Ведение исправления</span><span class="sxs-lookup"><span data-stu-id="943ff-138">Maintain a correction</span></span>
1. <span data-ttu-id="943ff-139">Выберите **Отметить как завершенное**.</span><span class="sxs-lookup"><span data-stu-id="943ff-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="943ff-140">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="943ff-140">Select **OK**.</span></span>
3. <span data-ttu-id="943ff-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="943ff-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="943ff-142">Закрытие несоответствия</span><span class="sxs-lookup"><span data-stu-id="943ff-142">Close a nonconformance</span></span>
1. <span data-ttu-id="943ff-143">Выберите **Функции**.</span><span class="sxs-lookup"><span data-stu-id="943ff-143">Select **Functions**.</span></span>
2. <span data-ttu-id="943ff-144">Выберите **Закрыть несоответствие**.</span><span class="sxs-lookup"><span data-stu-id="943ff-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="943ff-145">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="943ff-145">Select **Yes**.</span></span>
4. <span data-ttu-id="943ff-146">Закройте страницы.</span><span class="sxs-lookup"><span data-stu-id="943ff-146">Close the pages.</span></span>
