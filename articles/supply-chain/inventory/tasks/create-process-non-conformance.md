---
title: Создание и обработка соответствия
description: В этой теме рассматривается порядок управления несоответствием на основании существующего заказа контроля качества.
author: perlynne
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4f7e61adf37e74bdb082270b689cf0375ccc7f7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833961"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="f0f74-103">Создание и обработка соответствия</span><span class="sxs-lookup"><span data-stu-id="f0f74-103">Create and process a conformance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f0f74-104">В этой теме рассматривается порядок управления несоответствием на основании существующего заказа контроля качества.</span><span class="sxs-lookup"><span data-stu-id="f0f74-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="f0f74-105">Эту запись можно выполнить в компании демонстрации USMF и использовать предложенные значения.</span><span class="sxs-lookup"><span data-stu-id="f0f74-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="f0f74-106">Обычно эта процедура выполняется сотрудником отдела контроля качества.</span><span class="sxs-lookup"><span data-stu-id="f0f74-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="f0f74-107">В качестве предварительного условия выполните инструкции из раздела [Контроль качества товаров](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="f0f74-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="f0f74-108">Чтобы обработать утверждение несоответствия, пользователь, запустивший запись задачи, должен иметь значение "Имя", назначенное на странице "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="f0f74-108">To process the approval of a nonconformance, the user who runs the task recording must have a "Name" value assigned on the Users page.</span></span> <span data-ttu-id="f0f74-109">Для использования примечаний к документам у пользователя также должна быть активирована функция "Работа с документами" (в параметрах пользователя).</span><span class="sxs-lookup"><span data-stu-id="f0f74-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="f0f74-110">Выбор заказа контроля качества</span><span class="sxs-lookup"><span data-stu-id="f0f74-110">Select a quality order</span></span>
1. <span data-ttu-id="f0f74-111">В области перехода перейдите к **Модули > Управление запасами > Периодические задачи > Управление качеством > Заказы на контроль качества**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="f0f74-112">В списке выберите заказ контроля качества, который был создан в разделе [Контроль качества товаров](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="f0f74-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="f0f74-113">Создание несоответствия</span><span class="sxs-lookup"><span data-stu-id="f0f74-113">Create a nonconformance</span></span>
1. <span data-ttu-id="f0f74-114">На панели операций выберите **Запросы**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-114">On the Action Pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="f0f74-115">Выберите **Несоответствия**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="f0f74-116">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-116">Select **New**.</span></span>
4. <span data-ttu-id="f0f74-117">В раскрывающемся меню поля **Тип проблемы** выберите проблему, которая была обнаружена во время процесса проверки.</span><span class="sxs-lookup"><span data-stu-id="f0f74-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="f0f74-118">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="f0f74-119">Утверждение/отклонение несоответствия</span><span class="sxs-lookup"><span data-stu-id="f0f74-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="f0f74-120">Выберите **Функции**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-120">Select **Functions**.</span></span>
2. <span data-ttu-id="f0f74-121">Выберите **Утвердить несоответствие**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="f0f74-122">В этом примере утвердите несоответствие.</span><span class="sxs-lookup"><span data-stu-id="f0f74-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="f0f74-123">Утвержденные несоответствия могут быть связаны с сопутствующими операциями для записи работы, которая выполняется в рамках обработки несоответствия и, как в этой теме, обработки исправления.</span><span class="sxs-lookup"><span data-stu-id="f0f74-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="f0f74-124">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="f0f74-125">Создание действия исправления</span><span class="sxs-lookup"><span data-stu-id="f0f74-125">Create a correction action</span></span>
1. <span data-ttu-id="f0f74-126">Выберите **Коррекции**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="f0f74-127">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-127">Select **New**.</span></span>
3. <span data-ttu-id="f0f74-128">В поле **Табельный номер** в новой строке выберите требуемую запись из раскрывающегося меню.</span><span class="sxs-lookup"><span data-stu-id="f0f74-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="f0f74-129">Щелкните **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-129">Click **Select**.</span></span>
5. <span data-ttu-id="f0f74-130">Выберите **Привязать**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-130">Select **Attach**.</span></span> <span data-ttu-id="f0f74-131">Создайте примечание об исправлении.</span><span class="sxs-lookup"><span data-stu-id="f0f74-131">Create a note about the correction.</span></span> <span data-ttu-id="f0f74-132">В этом примере действие — обратиться к поставщику, чтобы обсудить случай несоответствия.</span><span class="sxs-lookup"><span data-stu-id="f0f74-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="f0f74-133">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-133">Select **New**.</span></span>
7. <span data-ttu-id="f0f74-134">Выберите **Примечание**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-134">Select **Note**.</span></span> <span data-ttu-id="f0f74-135">В зависимости от настройки отчета, можно печатать различные типы документов в отчетах, связанных с управлением несоответствиями.</span><span class="sxs-lookup"><span data-stu-id="f0f74-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="f0f74-136">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="f0f74-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="f0f74-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f0f74-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="f0f74-138">Ведение исправления</span><span class="sxs-lookup"><span data-stu-id="f0f74-138">Maintain a correction</span></span>
1. <span data-ttu-id="f0f74-139">Выберите **Отметить как завершенное**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="f0f74-140">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-140">Select **OK**.</span></span>
3. <span data-ttu-id="f0f74-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f0f74-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="f0f74-142">Закрытие несоответствия</span><span class="sxs-lookup"><span data-stu-id="f0f74-142">Close a nonconformance</span></span>
1. <span data-ttu-id="f0f74-143">Выберите **Функции**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-143">Select **Functions**.</span></span>
2. <span data-ttu-id="f0f74-144">Выберите **Закрыть несоответствие**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="f0f74-145">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="f0f74-145">Select **Yes**.</span></span>
4. <span data-ttu-id="f0f74-146">Закройте страницы.</span><span class="sxs-lookup"><span data-stu-id="f0f74-146">Close the pages.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]