---
title: Вопросы и ответы по финансовой отчетности
description: В этом разделе перечислены вопросы, касающиеся финансовой отчетности, которые возникли у других пользователей.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a0718db77399901acc8c88278c5b373b77b3cb16
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811318"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="64128-103">Вопросы и ответы по финансовой отчетности</span><span class="sxs-lookup"><span data-stu-id="64128-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="64128-104">В этом разделе перечислены вопросы, касающиеся финансовой отчетности, которые возникли у других пользователей.</span><span class="sxs-lookup"><span data-stu-id="64128-104">This topic lists questions related to financial reporting that other users have had.</span></span> 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="64128-105">Как ограничить доступ к отчету с помощью средств безопасности дерева?</span><span class="sxs-lookup"><span data-stu-id="64128-105">How do I restrict access to a report using Tree security?</span></span>

<span data-ttu-id="64128-106">Сценарий: демонстрационная компания USMF имеет балансовый отчет, который не должен быть виден всем пользователям финансовой отчетности в D365.</span><span class="sxs-lookup"><span data-stu-id="64128-106">Scenario: The USMF demo company has a Balance sheet report that it doesn’t want all Financial reporting users to be able to view in D365.</span></span> <span data-ttu-id="64128-107">Решение: можно использовать средства безопасности дерева для ограничения доступа к одному отчету, чтобы доступ к отчету имели только определенные пользователи.</span><span class="sxs-lookup"><span data-stu-id="64128-107">Solution: You can utilize Tree security to restrict access to a single report so that only certain users can access the report.</span></span> 

1.  <span data-ttu-id="64128-108">Вход в конструктор финансовых отчетов</span><span class="sxs-lookup"><span data-stu-id="64128-108">Log into Financial Reporter Report Designer</span></span>

2.  <span data-ttu-id="64128-109">Создание нового "Определения дерева" (Файл | Создать | Определение дерева).</span><span class="sxs-lookup"><span data-stu-id="64128-109">Create a new Tree Definition (File | New | Tree Definition) a.</span></span>    <span data-ttu-id="64128-110">Дважды щелкните строку **Сводка** в столбце **Безопасность блоков**.</span><span class="sxs-lookup"><span data-stu-id="64128-110">Double-click the **Summary** line in the **Unit Security** column.</span></span>
  <span data-ttu-id="64128-111">i.</span><span class="sxs-lookup"><span data-stu-id="64128-111">i.</span></span>    <span data-ttu-id="64128-112">Щелкните пользователей и группы.</span><span class="sxs-lookup"><span data-stu-id="64128-112">Click Users and Groups.</span></span>  
          <span data-ttu-id="64128-113">1. Выберите пользователей или группу, которым требуется доступ к этому отчету.</span><span class="sxs-lookup"><span data-stu-id="64128-113">1.    Select the User(s) or Group that would like to access this report.</span></span> 
          
<span data-ttu-id="64128-114">[![экран пользователя](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span><span class="sxs-lookup"><span data-stu-id="64128-114">[![user screen](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span></span>

<span data-ttu-id="64128-115">[![экран безопасности](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span><span class="sxs-lookup"><span data-stu-id="64128-115">[![security screen](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span></span>

  <span data-ttu-id="64128-116">b.</span><span class="sxs-lookup"><span data-stu-id="64128-116">b.</span></span>    <span data-ttu-id="64128-117">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="64128-117">Click **Save**.</span></span>
  
<span data-ttu-id="64128-118">[![кнопка "Сохранить"](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span><span class="sxs-lookup"><span data-stu-id="64128-118">[![save button](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span></span>

3.  <span data-ttu-id="64128-119">В определении отчета добавьте новое определение дерева</span><span class="sxs-lookup"><span data-stu-id="64128-119">In your Report Definition add your new Tree Definition</span></span>

<span data-ttu-id="64128-120">[![форма определения дерева](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span><span class="sxs-lookup"><span data-stu-id="64128-120">[![tree definition form](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span></span>

<span data-ttu-id="64128-121">A.</span><span class="sxs-lookup"><span data-stu-id="64128-121">A.</span></span>  <span data-ttu-id="64128-122">В определении дерева щелкните по параметру и в разделе "Выбор элемента аналитической структуры" проверьте "Включить все блоки"</span><span class="sxs-lookup"><span data-stu-id="64128-122">While in the Tree Definition click on Setting and under “Reporting unit selection” check “Include all units”</span></span>

<span data-ttu-id="64128-123">[![форма выбора элемента аналитической структуры](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span><span class="sxs-lookup"><span data-stu-id="64128-123">[![reporting unit selection form](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span></span>

<span data-ttu-id="64128-124">**До:** [![перед снимком экрана](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span><span class="sxs-lookup"><span data-stu-id="64128-124">**Before:** [![before screenshot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span></span>

<span data-ttu-id="64128-125">**После:** [![после снимка экрана](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span><span class="sxs-lookup"><span data-stu-id="64128-125">**After:** [![after screenshot](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span></span>

<span data-ttu-id="64128-126">Примечание: причина для вышеуказанного сообщения заключается в том, что у моего пользователя нет доступа к этому отчету после применения безопасности блока</span><span class="sxs-lookup"><span data-stu-id="64128-126">Note: Reason for the above message is my user does not have access to that report after applying Unit Security</span></span>



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a><span data-ttu-id="64128-127">Как определить, какие счета не соответствуют сальдо в D365?</span><span class="sxs-lookup"><span data-stu-id="64128-127">How do I determine which account(s) do not matching my balances in D365?</span></span>

<span data-ttu-id="64128-128">Вот несколько шагов, которые можно предпринять, если отчет не соответствует ожиданиям в D365, чтобы определить эти счета и отклонения.</span><span class="sxs-lookup"><span data-stu-id="64128-128">When you have a report that doesn't match what you would expect in D365, here are some steps you could take to identify those accounts and the variances.</span></span> 

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="64128-129">В конструкторе финансовых отчетов</span><span class="sxs-lookup"><span data-stu-id="64128-129">In Financial Reporter Report Designer</span></span>

1.  <span data-ttu-id="64128-130">Создание нового определения строки a.</span><span class="sxs-lookup"><span data-stu-id="64128-130">Create a new Row Definition a.</span></span>    <span data-ttu-id="64128-131">Щелкните Правка | Вставить строки из аналитик i.</span><span class="sxs-lookup"><span data-stu-id="64128-131">Click Edit | Insert Rows from Dimensions i.</span></span>  <span data-ttu-id="64128-132">Выберите MainAccount [![Выберите главный экран_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span><span class="sxs-lookup"><span data-stu-id="64128-132">Select MainAccount [![Select Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span></span>
    
    <span data-ttu-id="64128-133">ii.</span><span class="sxs-lookup"><span data-stu-id="64128-133">ii.</span></span> <span data-ttu-id="64128-134">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="64128-134">Click Ok b.</span></span>    <span data-ttu-id="64128-135">Сохраните определение строки</span><span class="sxs-lookup"><span data-stu-id="64128-135">Save the Row Definition</span></span>

2.  <span data-ttu-id="64128-136">Создание нового определения столбца [![Создание нового определения столбца](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span><span class="sxs-lookup"><span data-stu-id="64128-136">Create a new Column Definition     [![Create a new column definition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span></span>

3.  <span data-ttu-id="64128-137">Создание нового определения отчета a.</span><span class="sxs-lookup"><span data-stu-id="64128-137">Create a new Report Definition a.</span></span>    <span data-ttu-id="64128-138">Щелкните "Параметры" и снимите флажок [![Форма параметров](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span><span class="sxs-lookup"><span data-stu-id="64128-138">Click Settings and uncheck [![Settings form](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span></span>
   
4.  <span data-ttu-id="64128-139">Создание отчета.</span><span class="sxs-lookup"><span data-stu-id="64128-139">Generate the Report.</span></span> 

5.  <span data-ttu-id="64128-140">Экспорт отчета в Excel.</span><span class="sxs-lookup"><span data-stu-id="64128-140">Export the Report to Excel.</span></span>

### <a name="in-d365"></a><span data-ttu-id="64128-141">В D365:</span><span class="sxs-lookup"><span data-stu-id="64128-141">In D365:</span></span> 
1.  <span data-ttu-id="64128-142">Выберите Главная книга | Запросы и отчеты | Пробный баланс a.</span><span class="sxs-lookup"><span data-stu-id="64128-142">Click General Ledger | Inquiries and Reports | Trial Balance a.</span></span>    <span data-ttu-id="64128-143">Параметры i.</span><span class="sxs-lookup"><span data-stu-id="64128-143">Parameters i.</span></span>  <span data-ttu-id="64128-144">Начальная дата: начало финансового года ii.</span><span class="sxs-lookup"><span data-stu-id="64128-144">From Date: Start of Fiscal Year ii.</span></span> <span data-ttu-id="64128-145">Конечная дата: дата создания отчета для iii.</span><span class="sxs-lookup"><span data-stu-id="64128-145">To Date: Date you generated the report for iii.</span></span>    <span data-ttu-id="64128-146">Набор финансовых аналитик "Набор счета ГК" [![Форма счета ГК](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span><span class="sxs-lookup"><span data-stu-id="64128-146">Financial Dimension Set “Main Account set” [![Main Account Form](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span></span>
      
  <span data-ttu-id="64128-147">b.</span><span class="sxs-lookup"><span data-stu-id="64128-147">b.</span></span>    <span data-ttu-id="64128-148">Щелкните "Рассчитать"</span><span class="sxs-lookup"><span data-stu-id="64128-148">Click Calculate</span></span>

2.  <span data-ttu-id="64128-149">Экспорт отчета в Excel</span><span class="sxs-lookup"><span data-stu-id="64128-149">Export the report to Excel</span></span>

<span data-ttu-id="64128-150">Теперь можно скопировать данные из отчета FR Excel в отчет пробного баланса D365 и сравнить столбцы "Исходящее сальдо".</span><span class="sxs-lookup"><span data-stu-id="64128-150">You should now be able to copy the data from the FR Excel Report and to the D365 Trial Balance report and compare the “Closing Balance” columns.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]