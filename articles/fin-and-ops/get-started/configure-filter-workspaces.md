---
title: "Конфигурация и фильтрация рабочих областей"
description: "Эта статья предоставляет обзор о том, как настроить и фильтровать рабочие области."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankTreasurerWorkspace, HcmBenefitWorkspace, BudgetPlanningWorkspace, BusinessProcessGenericWorkspace, RetailCatalogManagementWorkspace, RetailCategoryAndProductWorkspace, RetailChannelManagementWorkspace, HcmCompensationWorkspace, CAMCostAccountingLedgerAdminWorkspace, CostAdminWorkspace, CostAnalysisWorkspace, CAMCostControlWorkspace, CustomerCollectionManagerWorkspace, CustomerInvoiceWorkspace, CustPaymentWorkspace, DataManagementWorkspace, DataValidationWorkspace, ERWorkspace, LedgerPeriodCloseProjectWorkspace, AssetWorkspace, GeneralJournalEntryWorkspace, VendVendorPortalInvoiceWorkspace, BudgetTrackingWorkspace, ReqCreatePlanWorkspace, BusinessProcessGenericOwnerWorkspace, SelfHealingWorkspace, WHSOutboundWorkMonitoringWorkspace, WHSWavePlanningWorkspace, PayrollWorkspace, HcmWorkforceWorkspace, RetailDiscountPricingWorkspace, EcoResProductDiscreteManufacturingWorkspace, KanbanPrepareProductForLeanWorkspace, EcoResProductProcessManufacturingWorkspace, EcoResProductVariantMaintainWorkspace, JmgShopSupervisorWorkspace, ProjProjectManagementWorkspace, VendVendorPortalWorkspace, PurchOrderMaintainWorkspace, PurchOrderProcessReceiptsWorkspace, HcmRecruitmentWorkspace, EcoResProductMaintainWorkspace, FMClerkWorkspace, OpResLifecycleManagementWorkspace, RetailITWorkspace, RetailChannelOperationsWorkspace, RetailStoreManagementWorkspace, SalesOrderProcessingWorkspace, SalesReturnWorkspace, SystemAdministrationWorkspaceForm, VendVendorRequestForQuotationsWorkspace, VendVendorProfileManagementWorkspace, VendInvoiceWorkspace, VendPaymentWorkspace
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17491
ms.assetid: 541e6012-4680-4684-8494-e9b5ca4684ee
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c90384c798023ac4fcab06502d77f832a8e4c4c2
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="configure-and-filter-workspaces"></a>Конфигурация и фильтрация рабочих областей

[!include[banner](../includes/banner.md)]


Эта статья предоставляет обзор о том, как настроить и фильтровать рабочие области.

<a name="configuring-a-workspace"></a>Конфигурация рабочей области
-----------------------

Можно изменить вид и поведение определенных рабочих областей, обновив параметры, относящиеся ко всей рабочей области. Когда рабочую область можно настроить, в области действий включается кнопка, говорящая, что можно нажать на нее, чтобы внести изменения конфигурации. Например, на следующем рисунке, кнопка называется **Настроить мою рабочую область**. 

[![конфигурация-и-фильтрация-рабочих-областей](./media/configure-and-filter-workspaces.png)](./media/configure-and-filter-workspaces.png)   

Когда вы нажимаете кнопку, появляется диалоговое окно, в котором можно изменить предопределенные параметры для рабочей области. Параметры, доступные в этом диалоговом окне, отличаются в зависимости от рабочей области и зависят от определенных элементов управления и бизнес-данных, доступных в рабочей области. 

[![настроить-мою-рабочую-область](./media/configure-my-workspace.png)](./media/configure-my-workspace.png)

## <a name="filtering-a-workspace"></a>Фильтрация рабочей области
Многие рабочие области позволяют фильтровать содержимое, отображаемое в них. Элементы управления, которые доступные, могут позволить фильтровать содержание в рабочей области или только содержимое в конкретном разделе рабочей области. Фильтры в рабочих областях могут иметь вид окон поиска, полей со списком, полей с произвольным текстом или других типов элементов управления. Однако каждый тип фильтра имеют одинаковые влияния, как описано в следующих разделах.

### <a name="workspace-wide-filters"></a>Фильтры уровня рабочей области

Можно отфильтровать всю рабочую область с помощью фильтра уровня рабочей области. Фильтр уровня рабочей области будет расположен в левом правом углу рабочей области. При выборе определенного значения в раскрывающемся списке содержимое рабочей области будет отфильтровано на основании этого выбора. 

[![фильтр-рабочей-области](./media/workspace-filter.png)](./media/workspace-filter.png) 

При нажатии кнопки для открытия фильтра отобразится несколько вариантов. 

[![расширенный-фильтр-рабочей-области](./media/workspace-filter-expanded.png)](./media/workspace-filter-expanded.png) 

Выберите параметр для фильтрации рабочей области на основе этого параметра.

### <a name="workspace-section-filters"></a>Фильтры раздела рабочей области

Если индивидуальные разделы рабочей области имеют фильтры, можно фильтровать каждый раздел отдельно. На следующем рисунке фильтр (поле с текстом "Фильтр") — это пример фильтра поля с произвольным текстом. 

[![фильтры-раздела-рабочей-области](./media/workspace-section-filters.png)](./media/workspace-section-filters.png) 

Как и в случае с фильтром уровня рабочей области, выберите или введите значение в поле, чтобы фильтровать содержимое раздела.




