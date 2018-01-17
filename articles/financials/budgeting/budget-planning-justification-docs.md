---
title: "Документы обоснования бюджетного плана"
description: "Документы обоснования предоставляют описания для этих запросов бюджета, чтобы объяснить причину, по которой необходим конкретный бюджет."
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: eb616d6802e32d9dcbbeaf9c9866491c8a8d59c8
ms.contentlocale: ru-ru
ms.lasthandoff: 01/17/2018

---

# <a name="budget-planning-justification-documents"></a><span data-ttu-id="9e5d4-103">Документы обоснования бюджетного плана</span><span class="sxs-lookup"><span data-stu-id="9e5d4-103">Budget planning justification documents</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9e5d4-104">Документы обоснования предоставляют описания для этих запросов бюджета, чтобы объяснить причину, по которой необходим конкретный бюджет.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="9e5d4-105">Шаблон бюджетного плана создается менеджером бюджета в Microsoft Word и назначается текущему процессу планирования бюджета.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="9e5d4-106">Владельцы бюджета могут затем открыть шаблон, и данные будут автоматически заполнены в Word на основе их запроса бюджета.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="9e5d4-107">Затем они могут добавить дополнительный текст или данные перед сохранением и присоединить свои персональные документы обоснования к бюджетному плану.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="9e5d4-108">Настройка надстройки Microsoft Dynamics Office для Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="9e5d4-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="9e5d4-109">Откройте новый документ Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="9e5d4-110">Щелкните **Вставить** на ленте, затем щелкните **Магазин**.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="9e5d4-111">Найдите надстройку Microsoft Dynamics Office Add-in и щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="9e5d4-112">В Word в области справа щелкните **Добавить сведения о сервере**.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="9e5d4-113">Введите или вставьте URL-адрес сервера и нажмите кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="9e5d4-114">Определение шаблона обоснования в Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="9e5d4-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="9e5d4-115">После входа щелкните **Дизайн** в надстройке Microsoft Dynamics Office Add-in.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="9e5d4-116">Для сведений заголовка используйте кнопку **Добавить поля**.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="9e5d4-117">Выберите источник данных объекта BudgetPlanJustification и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="9e5d4-118">**Примечание:** Этот объект является обязательным для любого документа обоснования.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="9e5d4-119">Другие объекты могут использоваться, но отправка обратно в Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition не будет выполняться, если этот объект не будет включен.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-119">Other entities can be used but the upload back to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="9e5d4-120">Добавьте метки BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter и DocumentNumber в документ Word.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="9e5d4-121">**Примечание:** При необходимости вместо стандартных меток можно использовать свои собственные пользовательские метки.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="9e5d4-122">Щелкните **Готово** для завершения раздела заголовка.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="9e5d4-123">Для сведений уровня строки по суммам бюджетного плана щелкните **Добавить таблицу**.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="9e5d4-124">Снова выберите источник данных объекта BudgetPlanJustification и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="9e5d4-125">Добавьте поля для EffectiveDate, ScenarioName, AccountDisplayValue и AccountingCurrencyExpenseAmount.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="9e5d4-126">**Примечание:** Если комментарии могут добавляться в отдельные строки бюджетного плана, их можно добавить в таблицу здесь.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="9e5d4-127">Добавьте любые дополнительные инструкции конечному пользователю и задайте все необходимое форматирование или стили в документе.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="9e5d4-128">Сохраните документ на локальном компьютере и закройте файл перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="9e5d4-129">Настройка процесса бюджетного планирования для использования в шаблоне обоснования</span><span class="sxs-lookup"><span data-stu-id="9e5d4-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="9e5d4-130">В Finance and Operations откройте **Бюджетирование** &gt; **Настройка** &gt; **Бюджетное планирование** &gt; **Шаблоны документов обоснования**.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-130">In Finance and Operations, go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="9e5d4-131">Щелкните **Создать** и перейдите в только что созданный документ Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="9e5d4-132">Введите отображаемое имя и описание шаблона.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-132">Enter a template display name and description.</span></span> <span data-ttu-id="9e5d4-133">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-133">Click **OK**.</span></span>
4.  <span data-ttu-id="9e5d4-134">Перейдите в раздел **Бюджетирование** &gt; **Настройка** &gt; **Бюджетное** **планирование** &gt; **Конфигурация бюджетного планирования**.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="9e5d4-135">Выберите процесс, в котором следует использовать шаблон обоснования, и нажмите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="9e5d4-136">В поле **Шаблон документа обоснования** выберите соответствующий шаблон и сохраните.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="9e5d4-137">Изменение и сохранение персональных документов обоснования</span><span class="sxs-lookup"><span data-stu-id="9e5d4-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="9e5d4-138">В Finance and Operations создайте новый бюджетный план или откройте существующий бюджетный план.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-138">In Finance and Operations, create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="9e5d4-139">В раскрывающемся меню **Обоснование** выберите **Создать новое обоснование**.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="9e5d4-140">После заполнения сведений выберите отправку персонализированного документа из раскрывающегося меню **Обоснование**.</span><span class="sxs-lookup"><span data-stu-id="9e5d4-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>





