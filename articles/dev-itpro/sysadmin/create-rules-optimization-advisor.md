---
title: "Создание правил для помощника по оптимизации"
description: "В этом разделе описывается добавление новых правил в помощник по оптимизации."
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e78427dacb0d2adfd0334115581d5a5a9cfd2921
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="03dec-103">Создание правил для помощника по оптимизации</span><span class="sxs-lookup"><span data-stu-id="03dec-103">Create rules for Optimization advisor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03dec-104">В этом разделе объясняется, как создавать новые правила для **помощника по оптимизации**.</span><span class="sxs-lookup"><span data-stu-id="03dec-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="03dec-105">Например, можно создать новое правило, определяющее, в каких случаях запросы предложений (RFQ) имеют пустой заголовок.</span><span class="sxs-lookup"><span data-stu-id="03dec-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="03dec-106">Использование заголовков для случаев упрощает их идентификацию и поиск.</span><span class="sxs-lookup"><span data-stu-id="03dec-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="03dec-107">Хотя этот пример довольно простой, он показывает, что может быть достигнуто с помощью правил оптимизации.</span><span class="sxs-lookup"><span data-stu-id="03dec-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="03dec-108">*Правило* представляет собой проверку, выполняемую для данных приложения.</span><span class="sxs-lookup"><span data-stu-id="03dec-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="03dec-109">Если условие, оцениваемое правилом, выполняется, создаются возможности для оптимизации процессов или улучшения данных.</span><span class="sxs-lookup"><span data-stu-id="03dec-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="03dec-110">Для этих возможностей можно выполнять действия, и, при необходимости, может быть измерено влияние этих действий.</span><span class="sxs-lookup"><span data-stu-id="03dec-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="03dec-111">Чтобы создать новое правило для **Помощника по оптимизации**, добавьте новый класс, который расширяет абстрактный класс **SelfHealingRule**, реализует интерфейс **IDiagnosticsRule** и снабжен атрибутом **DiagnosticRule**.</span><span class="sxs-lookup"><span data-stu-id="03dec-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="03dec-112">Класс также должен иметь метод, снабженный атрибутом **DiagnosticsRuleSubscription**.</span><span class="sxs-lookup"><span data-stu-id="03dec-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="03dec-113">В соответствии с соглашением это делается для метода **opportunityTitle**, который будет описан далее.</span><span class="sxs-lookup"><span data-stu-id="03dec-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="03dec-114">Этот новый класс может быть добавлен в пользовательскую модель с зависимостью от модели **SelfHealingRules**.</span><span class="sxs-lookup"><span data-stu-id="03dec-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="03dec-115">В следующем примере реализуемое правило называется **RFQTitleSelfHealingRule**.</span><span class="sxs-lookup"><span data-stu-id="03dec-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="03dec-116">Абстрактный класс **SelfHealingRule** содержит абстрактные методы, которые должны быть реализованы в производных классах.</span><span class="sxs-lookup"><span data-stu-id="03dec-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="03dec-117">Основным является метод **evaluate**, который возвращает список возможностей, идентифицированных правилом.</span><span class="sxs-lookup"><span data-stu-id="03dec-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="03dec-118">Возможности могут быть для юридического лица или они могут применяться ко всей системе.</span><span class="sxs-lookup"><span data-stu-id="03dec-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

```
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

<span data-ttu-id="03dec-119">В приведенном выше методе выполняется цикл по компаниям и выбираются случаи запроса предложений с пустыми заголовками в методе **findRFQCasesWithEmptyTitle**.</span><span class="sxs-lookup"><span data-stu-id="03dec-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="03dec-120">Если найден по крайней мере один такой случай, то создается возможность для конкретной компании с помощью метода **getOpportunityForCompany**.</span><span class="sxs-lookup"><span data-stu-id="03dec-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="03dec-121">Обратите внимание, что поле **Data** в таблице **SelfHealingOpportunity** имеет тип **Container**, и поэтому может содержать любые данные, относящиеся к логике, специфичной для этого правила.</span><span class="sxs-lookup"><span data-stu-id="03dec-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="03dec-122">Если задать для **OpportunityDate** текущую отметку времени, будет зарегистрировано время последней оценки возможности.</span><span class="sxs-lookup"><span data-stu-id="03dec-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="03dec-123">Возможности также могут быть по всем компаниям.</span><span class="sxs-lookup"><span data-stu-id="03dec-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="03dec-124">В этом случае цикл по компаниям не является обязательным, и возможность должна создаваться с помощью метода **getOpportunityAcrossCompanies**.</span><span class="sxs-lookup"><span data-stu-id="03dec-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="03dec-125">В следующем коде показан метод **findRFQCasesWithEmptyTitle**, который возвращает идентификаторы случаев запроса предложения, которые имеют пустые заголовки.</span><span class="sxs-lookup"><span data-stu-id="03dec-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

```
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

<span data-ttu-id="03dec-126">Также необходимо реализовать еще два метода, **opportunityTitle** и **opportunityDetails**.</span><span class="sxs-lookup"><span data-stu-id="03dec-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="03dec-127">Первый возвращает краткий заголовок для возможности, второй возвращает подробное описание возможности, которое также может содержать данные.</span><span class="sxs-lookup"><span data-stu-id="03dec-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="03dec-128">Заголовок, возвращенный методом **opportunityTitle**, отображается в столбце **Возможность оптимизации** в рабочей области **Помощник по оптимизации**.</span><span class="sxs-lookup"><span data-stu-id="03dec-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="03dec-129">Он также отображается как заголовок боковой области, в которой отображаются дополнительные сведения о возможности.</span><span class="sxs-lookup"><span data-stu-id="03dec-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="03dec-130">В соответствии с соглашением этот метод имеет атрибут **DiagnosticRuleSubscription**, который принимает следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="03dec-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="03dec-131">**Область диагностики** — перечисление типа **DiagnosticArea**, которое описывает, к какой области приложения принадлежит правило, например **DiagnosticArea::SCM**.</span><span class="sxs-lookup"><span data-stu-id="03dec-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="03dec-132">**Имя правила** — строка с именем правила.</span><span class="sxs-lookup"><span data-stu-id="03dec-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="03dec-133">Оно отображается в столбце **Имя правила** в форме **Правило проверки диагностики** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="03dec-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="03dec-134">**Частота запуска** — перечисление типа **DiagnosticRunFrequency**, описывающее, как часто должно запускаться правило, например **DiagnosticRunFrequency::Daily**.</span><span class="sxs-lookup"><span data-stu-id="03dec-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="03dec-135">**Описание правила** — строка с более подробным описанием правила.</span><span class="sxs-lookup"><span data-stu-id="03dec-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="03dec-136">Оно отображается в столбце **Описание правила** в форме **Правило проверки диагностики** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="03dec-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="03dec-137">Атрибут **DiagnosticRuleSubscription** является обязательным для работы правила.</span><span class="sxs-lookup"><span data-stu-id="03dec-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="03dec-138">Как правило, он используется для **opportunityTitle**, но может быть добавлен в любой метод класса.</span><span class="sxs-lookup"><span data-stu-id="03dec-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="03dec-139">Ниже приведен пример реализации.</span><span class="sxs-lookup"><span data-stu-id="03dec-139">The following is an example implementation.</span></span> <span data-ttu-id="03dec-140">Необработанные строки используются для упрощения, но в правильной реализации необходимо определить метки.</span><span class="sxs-lookup"><span data-stu-id="03dec-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

```
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

<span data-ttu-id="03dec-141">Описание, возвращенное методом **opportunityDetails**, отображается на боковой панели, содержащей дополнительные сведения о возможности.</span><span class="sxs-lookup"><span data-stu-id="03dec-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="03dec-142">Он принимает аргумент **SelfHealingOpportunity**, который является полем **Data**, которое может использоваться для предоставления дополнительных сведений о возможности.</span><span class="sxs-lookup"><span data-stu-id="03dec-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="03dec-143">В этом примере метод возвращает идентификаторы случаев запроса предложения с пустым заголовком.</span><span class="sxs-lookup"><span data-stu-id="03dec-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

```
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

<span data-ttu-id="03dec-144">Два оставшихся абстрактных метода, которые необходимо реализовать, это **provideHealingAction** и **securityMenuItem**.</span><span class="sxs-lookup"><span data-stu-id="03dec-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="03dec-145">**provideHealingAction** возвращает значение true, если предусмотрено действие восстановления; в противном случае возвращается значение false.</span><span class="sxs-lookup"><span data-stu-id="03dec-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="03dec-146">Если возвращается значение true, метод **performAction** должен быть реализован или возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="03dec-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="03dec-147">Метод **performAction** принимает аргумент **SelfHealingOpportunity**, в котором данные могут использоваться для действия.</span><span class="sxs-lookup"><span data-stu-id="03dec-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="03dec-148">В этом примере действие открывает **PurchRFQCaseTableListPage** для ручной коррекции.</span><span class="sxs-lookup"><span data-stu-id="03dec-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

```
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

<span data-ttu-id="03dec-149">В зависимости от особенностей правила может быть возможно выполнить автоматическое действие с использованием данных возможности.</span><span class="sxs-lookup"><span data-stu-id="03dec-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="03dec-150">В этом примере система может автоматически генерировать заголовки для случаев запроса предложения.</span><span class="sxs-lookup"><span data-stu-id="03dec-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="03dec-151">Метод **securityMenuItem** возвращает имя пункта меню действий таким образом, что правило является видимым только для пользователей, которые имеют доступ к этому пункту меню действия.</span><span class="sxs-lookup"><span data-stu-id="03dec-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="03dec-152">Безопасность может требовать, чтобы определенные правила и возможности были доступны только авторизованным пользователям.</span><span class="sxs-lookup"><span data-stu-id="03dec-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="03dec-153">В этом примере только пользователи, имеющие доступ к **PurchRFQCaseTitleAction**, могут просматривать эту возможность.</span><span class="sxs-lookup"><span data-stu-id="03dec-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="03dec-154">Обратите внимание, что данный пункт меню действий был создан для данного примера и был добавлен в качестве точки входа для прав доступа **PurchRFQCaseTableMaintain**.</span><span class="sxs-lookup"><span data-stu-id="03dec-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

> [!NOTE]
> <span data-ttu-id="03dec-155">Пункт меню должен быть пунктом меню действий для правильной работы безопасности.</span><span class="sxs-lookup"><span data-stu-id="03dec-155">The menu item must be an action menu item for security to work correctly.</span></span> <span data-ttu-id="03dec-156">Другие типы пунктов меню, такие как **Пункты меню отображения**, не будет правильно работать.</span><span class="sxs-lookup"><span data-stu-id="03dec-156">Other menu item types, such as **Display menu items** will not work correctly.</span></span>

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="03dec-157">После компиляции правила выполните следующее задание, чтобы оно отображалось в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="03dec-157">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

```
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

<span data-ttu-id="03dec-158">Правило будет отображаться в форме **Правило проверки диагностики**, доступной из **Администрирование системы** > **Периодические задачи** > **Ведение правила проверки диагностики**.</span><span class="sxs-lookup"><span data-stu-id="03dec-158">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="03dec-159">Для его повторного вычисления выберите **Администрирование системы** > **Периодические задачи** > **Расписание правила проверки диагностики**, выберите частоту правила, например **Ежедневно**.</span><span class="sxs-lookup"><span data-stu-id="03dec-159">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="03dec-160">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="03dec-160">Click **OK**.</span></span> <span data-ttu-id="03dec-161">Выберите **Администрирование системы** > **Помощник по оптимизации** для просмотра новой возможности.</span><span class="sxs-lookup"><span data-stu-id="03dec-161">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="03dec-162">В следующем примере показан фрагмент кода со схемой правила, включая все необходимые методы и атрибуты.</span><span class="sxs-lookup"><span data-stu-id="03dec-162">The following example is a code snippet with the skeleton of a rule including all the required methods and attributes.</span></span> <span data-ttu-id="03dec-163">Он поможет начать работу по созданию новых правил.</span><span class="sxs-lookup"><span data-stu-id="03dec-163">It helps you get started with writing new rules.</span></span> <span data-ttu-id="03dec-164">Метки и пункты меню действий, которые используются в примере, используются только для демонстрационных целей.</span><span class="sxs-lookup"><span data-stu-id="03dec-164">The labels and action menu items that are used in the example are only used for demonstration purpose.</span></span>

```
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

<span data-ttu-id="03dec-165">Для получения дополнительных сведений просмотрите короткое видео на YouTube:</span><span class="sxs-lookup"><span data-stu-id="03dec-165">For more information, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/MRsAzgFCUSQ]

