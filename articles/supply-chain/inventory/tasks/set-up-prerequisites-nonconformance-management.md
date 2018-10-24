--- 
title: "Настройка предварительных требований для управления несоответствиями"
description: "Используйте эту процедуру, чтобы включить процесс управления несоответствиями."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 0a4062acc91e024e3a0a41c0b3cb35ff5ffe2a4a
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-prerequisites-for-nonconformance-management"></a><span data-ttu-id="9f725-103">Настройка предварительных требований для управления несоответствиями</span><span class="sxs-lookup"><span data-stu-id="9f725-103">Set up prerequisites for nonconformance management</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f725-104">Используйте эту процедуру, чтобы включить процесс управления несоответствиями.</span><span class="sxs-lookup"><span data-stu-id="9f725-104">Use this procedure to enable nonconformance management processes.</span></span> <span data-ttu-id="9f725-105">Несоответствие описывает процедуру или номенклатуру, имеющую проблемы качества, причем это описание включает сведения об источнике и типе проблемы.</span><span class="sxs-lookup"><span data-stu-id="9f725-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="9f725-106">В этой процедуре используется компания с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="9f725-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="9f725-107">Обычно эта процедура выполняется менеджером по контролю качества.</span><span class="sxs-lookup"><span data-stu-id="9f725-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="9f725-108">Включение процессов управления качеством в компании</span><span class="sxs-lookup"><span data-stu-id="9f725-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="9f725-109">Перейдите в раздел "Управление запасами" > "Настройка" > "Параметры управления запасами и складами".</span><span class="sxs-lookup"><span data-stu-id="9f725-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="9f725-110">Перейдите на вкладку "Управление качеством".</span><span class="sxs-lookup"><span data-stu-id="9f725-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="9f725-111">Выберите значение "Да" в поле "Использовать управление качеством".</span><span class="sxs-lookup"><span data-stu-id="9f725-111">Select Yes in the Use quality management field.</span></span>
    * <span data-ttu-id="9f725-112">Выберите этот параметр, чтобы включить процесс управления качеством для компании.</span><span class="sxs-lookup"><span data-stu-id="9f725-112">Select this parameter to enable quality management processes for the company.</span></span>  
4. <span data-ttu-id="9f725-113">В поле "Почасовая ставка" введите число.</span><span class="sxs-lookup"><span data-stu-id="9f725-113">In the Hourly rate field, enter a number.</span></span>
    * <span data-ttu-id="9f725-114">В поле "Почасовая ставка" введите почасовую ставку в местной валюте.</span><span class="sxs-lookup"><span data-stu-id="9f725-114">Use the Hourly rate field to enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="9f725-115">Почасовая ставка используется для расчета затрат на операции, связанные с несоответствием.</span><span class="sxs-lookup"><span data-stu-id="9f725-115">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="9f725-116">Почасовая ставка и рассчитанные затраты предоставляют справочные сведения для несоответствия, и они не взаимодействуют с другими функциями.</span><span class="sxs-lookup"><span data-stu-id="9f725-116">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="9f725-117">Щелкните "Настройка отчетов".</span><span class="sxs-lookup"><span data-stu-id="9f725-117">Click Report setup.</span></span>
    * <span data-ttu-id="9f725-118">На этой странице можно определить типы примечаний отчетов по контролю качества, которые будут использоваться для различных типов отчетов по управлению качеством.</span><span class="sxs-lookup"><span data-stu-id="9f725-118">This page allows you define the quality report note types that will be used on different kinds of quality management reports.</span></span>  
6. <span data-ttu-id="9f725-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f725-119">Close the page.</span></span>
7. <span data-ttu-id="9f725-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f725-120">Close the page.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="9f725-121">Включение пользователя для обработки несоответствия</span><span class="sxs-lookup"><span data-stu-id="9f725-121">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="9f725-122">Перейдите в раздел "Администрирование системы" > "Пользователи" > "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="9f725-122">Go to System administration > Users > Users.</span></span>
    * <span data-ttu-id="9f725-123">Чтобы обработать утверждение несоответствия, пользователь, который утверждает или отклоняет несоответствия, должен иметь значение "Имя", назначенное на странице "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="9f725-123">To process the approval of a nonconformance the user who  approves or rejects nonconformances must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="9f725-124">Для использования примечаний к документам у пользователя также должна быть активирована функция "Работа с документами" (в параметрах пользователя).</span><span class="sxs-lookup"><span data-stu-id="9f725-124">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
2. <span data-ttu-id="9f725-125">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="9f725-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9f725-126">Например, отфильтруйте поле "Имя" по значению Ricardo.</span><span class="sxs-lookup"><span data-stu-id="9f725-126">For example, filter on the Name field with a value of 'Ricardo'.</span></span>
    * <span data-ttu-id="9f725-127">Используйте фильтр для поиска пользователя, который будет утверждать или отклонять записи несоответствия.</span><span class="sxs-lookup"><span data-stu-id="9f725-127">Use the filter to find the user who will be approving or rejecting the nonconformance records.</span></span>  
3. <span data-ttu-id="9f725-128">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9f725-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9f725-129">Чтобы обработать утверждение несоответствия, убедитесь, что пользователь, который утверждает или отклоняет несоответствия, имеет значение "Имя", назначенное на странице "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="9f725-129">To process the approval of a nonconformance, make sure the user who approves or rejects nonconformances has a “Name” value assigned on the Users page.</span></span>  
4. <span data-ttu-id="9f725-130">Щелкните "Параметры пользователя".</span><span class="sxs-lookup"><span data-stu-id="9f725-130">Click User options.</span></span>
5. <span data-ttu-id="9f725-131">Перейдите на вкладку "Параметры".</span><span class="sxs-lookup"><span data-stu-id="9f725-131">Click the Preferences tab.</span></span>
6. <span data-ttu-id="9f725-132">Выберите значение "Да" в поле "Разрешить работу с документами".</span><span class="sxs-lookup"><span data-stu-id="9f725-132">Select Yes in the Enable document handling field.</span></span>
    * <span data-ttu-id="9f725-133">Для использования примечаний к документам у пользователя также должна быть активирована функция "Работа с документами" (в параметрах пользователя).</span><span class="sxs-lookup"><span data-stu-id="9f725-133">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
7. <span data-ttu-id="9f725-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f725-134">Close the page.</span></span>
8. <span data-ttu-id="9f725-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f725-135">Close the page.</span></span>
9. <span data-ttu-id="9f725-136">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f725-136">Close the page.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="9f725-137">Определение типов диагностики для обработки несоответствия</span><span class="sxs-lookup"><span data-stu-id="9f725-137">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="9f725-138">Перейдите в раздел "Управление запасами" > "Настройка" > "Управление качеством" > "Типы диагностики".</span><span class="sxs-lookup"><span data-stu-id="9f725-138">Go to Inventory management > Setup > Quality management > Diagnostic types.</span></span>
    * <span data-ttu-id="9f725-139">Используйте страницу Типы диагностики, чтобы определить классификацию диагностических действий.</span><span class="sxs-lookup"><span data-stu-id="9f725-139">Use the Diagnostic types page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="9f725-140">Коррекция устанавливает, какой тип диагностического действия должен быть предпринят для утвержденного несоответствия, кто его должен выполнять, а также запрошенную и планируемую дату завершения.</span><span class="sxs-lookup"><span data-stu-id="9f725-140">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="9f725-141">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9f725-141">Click New.</span></span>
3. <span data-ttu-id="9f725-142">В поле "Диагностика" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f725-142">In the Diagnostic field, type a value.</span></span>
4. <span data-ttu-id="9f725-143">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f725-143">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9f725-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f725-144">Close the page.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="9f725-145">Определение расходов по контролю качества для обработки несоответствия</span><span class="sxs-lookup"><span data-stu-id="9f725-145">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="9f725-146">Перейдите в раздел "Управление запасами" > "Настройка" > "Управление качеством" > "Расходы по контролю качества".</span><span class="sxs-lookup"><span data-stu-id="9f725-146">Go to Inventory management > Setup > Quality management > Quality charges.</span></span>
    * <span data-ttu-id="9f725-147">Используйте страницу "Расходы по контролю качества", чтобы определить классификацию расходов, которые будут использоваться в операциях, связанных с несоответствиями.</span><span class="sxs-lookup"><span data-stu-id="9f725-147">Use the Quality charges page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="9f725-148">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9f725-148">Click New.</span></span>
3. <span data-ttu-id="9f725-149">В поле "Код накладных расходов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f725-149">In the Charges code field, type a value.</span></span>
4. <span data-ttu-id="9f725-150">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f725-150">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9f725-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f725-151">Close the page.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="9f725-152">Определение операций для обработки несоответствия</span><span class="sxs-lookup"><span data-stu-id="9f725-152">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="9f725-153">Перейдите в раздел "Управление запасами" > "Настройка" > "Управление качеством" > "Операции".</span><span class="sxs-lookup"><span data-stu-id="9f725-153">Go to Inventory management > Setup > Quality management > Operations.</span></span>
    * <span data-ttu-id="9f725-154">Используйте страницу "Операции", чтобы определить классификацию работы, которая может быть выполнена для утвержденного несоответствия.</span><span class="sxs-lookup"><span data-stu-id="9f725-154">Use the Operations page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="9f725-155">При связи операции с несоответствием имеется возможность определить сведения о связанном материале, часах трудозатрат и накладных расходах, требуемых для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="9f725-155">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="9f725-156">Эти сведения составляют основу для расчета оценочной стоимости выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="9f725-156">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="9f725-157">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9f725-157">Click New.</span></span>
3. <span data-ttu-id="9f725-158">В поле "Операция" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f725-158">In the Operation field, type a value.</span></span>
4. <span data-ttu-id="9f725-159">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f725-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9f725-160">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f725-160">Close the page.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="9f725-161">Определение типов проблем для обработки несоответствия</span><span class="sxs-lookup"><span data-stu-id="9f725-161">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="9f725-162">Перейдите в раздел "Управление запасами" > "Настройка" > "Управление качеством" > "Типы проблемы".</span><span class="sxs-lookup"><span data-stu-id="9f725-162">Go to Inventory management > Setup > Quality management > Problem types.</span></span>
    * <span data-ttu-id="9f725-163">Используйте страницу "Типы проблем", чтобы определить классификацию проблем качества, возникающих для различных типов несоответствий.</span><span class="sxs-lookup"><span data-stu-id="9f725-163">Use the Problem types page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="9f725-164">Имеются следующие типы несоответствий: "Внутренний", "Клиент", "Поставщик", "Запрос на обслуживание", "Производство" и "Производство сопутствующих продуктов".</span><span class="sxs-lookup"><span data-stu-id="9f725-164">The nonconformance types include Internal, Customer, Vendor, Service request, Production, and Co-product production.</span></span> <span data-ttu-id="9f725-165">Один тип проблемы можно связать с несколькими типами несоответствий.</span><span class="sxs-lookup"><span data-stu-id="9f725-165">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="9f725-166">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9f725-166">Click New.</span></span>
3. <span data-ttu-id="9f725-167">В поле "Тип проблемы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f725-167">In the Problem type field, type a value.</span></span>
4. <span data-ttu-id="9f725-168">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f725-168">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9f725-169">Щелкните "Типы несоответствия".</span><span class="sxs-lookup"><span data-stu-id="9f725-169">Click Non conformance types.</span></span>
    * <span data-ttu-id="9f725-170">Используйте страницу "Типы несоответствия" для указания типа проблемы, который будет использоваться для одного или нескольких типов несоответствия.</span><span class="sxs-lookup"><span data-stu-id="9f725-170">Use the Non conformance types page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="9f725-171">Например, тип проблемы, относящийся к коду брака, может применяться ко всем типам несоответствия, в то время как тип проблемы о жалобах клиента может применяться только к типам несоответствия о клиентах или запросах на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9f725-171">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="9f725-172">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9f725-172">Click New.</span></span>
7. <span data-ttu-id="9f725-173">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9f725-173">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="9f725-174">В поле "Тип несоответствия" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="9f725-174">In the Non conformance type field, select an option.</span></span>
9. <span data-ttu-id="9f725-175">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f725-175">Close the page.</span></span>
10. <span data-ttu-id="9f725-176">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f725-176">Close the page.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="9f725-177">Определение зон карантина для обработки несоответствия</span><span class="sxs-lookup"><span data-stu-id="9f725-177">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="9f725-178">Перейдите в раздел "Управление запасами" > "Настройка" > "Управление качеством" > "Зоны карантина".</span><span class="sxs-lookup"><span data-stu-id="9f725-178">Go to Inventory management > Setup > Quality management > Quarantine zones.</span></span>
2. <span data-ttu-id="9f725-179">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9f725-179">Click New.</span></span>
3. <span data-ttu-id="9f725-180">В поле "Зона карантина" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f725-180">In the Quarantine zone field, type a value.</span></span>
4. <span data-ttu-id="9f725-181">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f725-181">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9f725-182">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f725-182">Close the page.</span></span>


