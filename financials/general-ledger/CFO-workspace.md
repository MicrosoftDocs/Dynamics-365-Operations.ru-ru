---
title: "Добавление финансовых аналитик в рабочую область финансового директора"
description: "В этой теме объясняется, как добавить финансовые аналитики в рабочую область финансового директора, чтобы их можно было использовать для отчетов по ГК и бюджету."
author: aolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.2.0
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 05fd7ce5293b3a300aabc073a6e492c5804d1897
ms.contentlocale: ru-ru
ms.lasthandoff: 08/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="ec8a8-103">Добавление финансовых аналитик в рабочую область финансового директора</span><span class="sxs-lookup"><span data-stu-id="ec8a8-103">Add financial dimensions to the CFO workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ec8a8-104">В этой теме объясняется, как добавить финансовые аналитики в рабочую область финансового директора, чтобы их можно было использовать для отчетов по ГК и бюджету.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="ec8a8-105">Рабочая область финансового директора содержит вкладки **Обзор** и **Финансы**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-105">The CFO workspace has an **Overview** tab and a **Financial** tab.</span></span> <span data-ttu-id="ec8a8-106">Отчеты на этих двух вкладках обеспечиваются двумя измерениями: LedgerActivityMeasure и BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-106">The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="ec8a8-107">В Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, , обновление от июля 2017 г., существует связь между этими двумя измерениям и объектом DimensionCombinationEntity.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="ec8a8-108">Следовательно, можно выбрать аналитики.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-108">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="ec8a8-109">В Finance and Operations на странице **Entity Store** обновите измерения **LedgerActivityMeasure** и **BudgetActivityMeasure**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-109">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="ec8a8-110">В Microsoft Visual Studio откройте обозреватель приложений и выполните поиск по слову **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-110">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="ec8a8-111">В разделе **Ресурсы** откройте **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-111">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="ec8a8-112">Когда ресурс откроется в Microsoft Power BI Desktop выберите **Получить данные**, выберите **База данных SQL Server**, а затем выберите **Подключиться**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-112">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="ec8a8-113">Введите имя сервера и введите **AxDW** в качестве базы данных.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-113">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="ec8a8-114">Выберите **DirectQuery** и выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-114">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="ec8a8-115">Найдите и выберите **LedgerActivityMeasure\_DimensionCombination**, а затем выберите **Загрузить**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-115">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="ec8a8-116">В списке **Поля** переименуйте таблицу в **Финансовые аналитики**, чтобы ее было легко идентифицировать.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-116">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="ec8a8-117">Выберите **Управление связями**, а затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-117">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="ec8a8-118">В первом поле выберите **Действия ГК**, а затем выберите **LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-118">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="ec8a8-119">Во втором поле выберите **LedgerActivityMeasure\_DimensionCombination** (или **Финансовые аналитики**, если вы переименовали таблицу).</span><span class="sxs-lookup"><span data-stu-id="ec8a8-119">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="ec8a8-120">Выберите заголовок **DimensionCombinationRECID**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-120">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="ec8a8-121">В поле **Кратность** выберите **Многие к одному**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-121">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="ec8a8-122">Изменение значение в поле **Направление кросс-фильтра** на **Один**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-122">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="ec8a8-123">Выберите и **Активировать связь**, и **Предполагать целостность данных**, выберите **ОК**, а затем выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-123">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="ec8a8-124">[![Создание связи](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="ec8a8-124">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="ec8a8-125">В списке **Поля** вы должны видеть таблицу и доступные финансовые аналитики.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-125">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="ec8a8-126">Перетащите нужные финансовые аналитики на фильтры уровня отчета.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-126">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="ec8a8-127">Сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-127">Save your changes.</span></span>
15. <span data-ttu-id="ec8a8-128">В репозитории прикладных объектов (AOT) щелкните свой проект правой кнопкой мыши и выберите **Синхронизировать**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-128">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="ec8a8-129">Соберите проект, а затем откройте приложение для просмотра результатов.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-129">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="ec8a8-130">[![Готовая рабочая область](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="ec8a8-130">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

