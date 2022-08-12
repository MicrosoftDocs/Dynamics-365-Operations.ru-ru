---
title: Создание правил для помощника по оптимизации
description: В этой статье рассматривается, как добавлять новые правила в помощник по оптимизации.
author: roxanadiaconu
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: sericks
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 2774d18611b10a1f627d5fb6e109696a3ca5e5f8
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108574"
---
# <a name="create-rules-for-optimization-advisor"></a>Создание правил для помощника по оптимизации

[!include [banner](../includes/banner.md)]

В этой статье объясняется, как создавать новые правила для **помощника по оптимизации**. Например, можно создать новое правило, определяющее, в каких случаях запросы предложений (RFQ) имеют пустой заголовок. Использование заголовков для случаев упрощает их идентификацию и поиск. Хотя этот пример довольно простой, он показывает, что может быть достигнуто с помощью правил оптимизации. 

*Правило* представляет собой проверку, выполняемую для данных приложения. Если условие, оцениваемое правилом, выполняется, создаются возможности для оптимизации процессов или улучшения данных. Для этих возможностей можно выполнять действия, и, при необходимости, может быть измерено влияние этих действий. 

Чтобы создать новое правило для **Помощника по оптимизации**, добавьте новый класс, который расширяет абстрактный класс **SelfHealingRule**, реализует интерфейс **IDiagnosticsRule** и снабжен атрибутом **DiagnosticRule**. Класс также должен иметь метод, снабженный атрибутом **DiagnosticsRuleSubscription**. В соответствии с соглашением это делается для метода **opportunityTitle**, который будет описан далее. Этот новый класс может быть добавлен в пользовательскую модель с зависимостью от модели **SelfHealingRules**. В следующем примере реализуемое правило называется **RFQTitleSelfHealingRule**.

```xpp
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

Абстрактный класс **SelfHealingRule** содержит абстрактные методы, которые должны быть реализованы в производных классах. Основным является метод **evaluate**, который возвращает список возможностей, идентифицированных правилом. Возможности могут быть для юридического лица или они могут применяться ко всей системе.

```xpp
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

В приведенном выше методе выполняется цикл по компаниям и выбираются случаи запроса предложений с пустыми заголовками в методе **findRFQCasesWithEmptyTitle**. Если найден по крайней мере один такой случай, то создается возможность для конкретной компании с помощью метода **getOpportunityForCompany**. Обратите внимание, что поле **Data** в таблице **SelfHealingOpportunity** имеет тип **Container**, и поэтому может содержать любые данные, относящиеся к логике, специфичной для этого правила. Если задать для **OpportunityDate** текущую отметку времени, будет зарегистрировано время последней оценки возможности.  

Возможности также могут быть по всем компаниям. В этом случае цикл по компаниям не является обязательным, и возможность должна создаваться с помощью метода **getOpportunityAcrossCompanies**. 

В следующем коде показан метод **findRFQCasesWithEmptyTitle**, который возвращает идентификаторы случаев запроса предложения, которые имеют пустые заголовки.

```xpp
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

Также необходимо реализовать еще два метода, **opportunityTitle** и **opportunityDetails**. Первый возвращает краткий заголовок для возможности, второй возвращает подробное описание возможности, которое также может содержать данные.

Заголовок, возвращенный методом **opportunityTitle**, отображается в столбце **Возможность оптимизации** в рабочей области **Помощник по оптимизации**. Он также отображается как заголовок боковой области, в которой отображаются дополнительные сведения о возможности. В соответствии с соглашением этот метод имеет атрибут **DiagnosticRuleSubscription**, который принимает следующие аргументы: 

* **Область диагностики** — перечисление типа **DiagnosticArea**, которое описывает, к какой области приложения принадлежит правило, например **DiagnosticArea::SCM**. 

* **Имя правила** — строка с именем правила. Оно отображается в столбце **Имя правила** в форме **Правило проверки диагностики** (**DiagnosticsValidationRuleMaintain**). 

* **Частота запуска** — перечисление типа **DiagnosticRunFrequency**, описывающее, как часто должно запускаться правило, например **DiagnosticRunFrequency::Daily**. 

* **Описание правила** — строка с более подробным описанием правила. Оно отображается в столбце **Описание правила** в форме **Правило проверки диагностики** (**DiagnosticsValidationRuleMaintain**). 

> [!NOTE]
> Атрибут **DiagnosticRuleSubscription** является обязательным для работы правила. Как правило, он используется для **opportunityTitle**, но может быть добавлен в любой метод класса.

Ниже приведен пример реализации. Необработанные строки используются для упрощения, но в правильной реализации необходимо определить метки. 

```xpp
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

Описание, возвращенное методом **opportunityDetails**, отображается на боковой панели, содержащей дополнительные сведения о возможности. Он принимает аргумент **SelfHealingOpportunity**, который является полем **Data**, которое может использоваться для предоставления дополнительных сведений о возможности. В этом примере метод возвращает идентификаторы случаев запроса предложения с пустым заголовком. 

```xpp
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

Два оставшихся абстрактных метода, которые необходимо реализовать, это **provideHealingAction** и **securityMenuItem**. 

**provideHealingAction** возвращает значение true, если предусмотрено действие восстановления; в противном случае возвращается значение false. Если возвращается значение true, метод **performAction** должен быть реализован или возникает ошибка. Метод **performAction** принимает аргумент **SelfHealingOpportunity**, в котором данные могут использоваться для действия. В этом примере действие открывает **PurchRFQCaseTableListPage** для ручной коррекции. 

```xpp
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

В зависимости от особенностей правила может быть возможно выполнить автоматическое действие с использованием данных возможности. В этом примере система может автоматически генерировать заголовки для случаев запроса предложения. 

Метод **securityMenuItem** возвращает имя пункта меню действий таким образом, что правило является видимым только для пользователей, которые имеют доступ к этому пункту меню действия. Безопасность может требовать, чтобы определенные правила и возможности были доступны только авторизованным пользователям. В этом примере только пользователи, имеющие доступ к **PurchRFQCaseTitleAction**, могут просматривать эту возможность. Обратите внимание, что данный пункт меню действий был создан для данного примера и был добавлен в качестве точки входа для прав доступа **PurchRFQCaseTableMaintain**. 

> [!NOTE]
> Пункт меню должен быть пунктом меню действий для правильной работы безопасности. Другие типы пунктов меню, такие как **Пункты меню отображения**, не будет правильно работать.

```xpp
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

После компиляции правила выполните следующее задание, чтобы оно отображалось в пользовательском интерфейсе.

```xpp
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

Правило будет отображаться в форме **Правило проверки диагностики**, доступной из **Администрирование системы** > **Периодические задачи** > **Ведение правила проверки диагностики**. Для его повторного вычисления выберите **Администрирование системы** > **Периодические задачи** > **Расписание правила проверки диагностики**, выберите частоту правила, например **Ежедневно**. Нажмите кнопку **ОК**. Выберите **Администрирование системы** > **Помощник по оптимизации** для просмотра новой возможности. 

В следующем примере показан фрагмент кода со схемой правила, включая все необходимые методы и атрибуты. Он поможет начать работу по созданию новых правил. Метки и пункты меню действий, которые используются в примере, используются только для демонстрационных целей.

```xpp
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

Для получения дополнительных сведений посмотрите короткое видео на YouTube: [Помощник по оптимизации в Dynamics 365 Finance](https://www.youtube.com/watch?v=MRsAzgFCUSQ)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
