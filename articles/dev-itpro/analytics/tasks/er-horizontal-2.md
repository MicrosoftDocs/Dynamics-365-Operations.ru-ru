--- 
title: "Выполнение форматов для динамического добавления столбцов в отчеты Excel в виде горизонтально разворачивающихся диапазонов"
description: "Следующие шаги описывают, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для создания отчетов в виде файлов листов OPENXML (Excel), в которых необходимые столбцы можно создавать динамически как горизонтально расширяемые диапазоны."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: c7d563da9a02c91cce17cfa1d4a6915dd768ac3d
ms.contentlocale: ru-ru
ms.lasthandoff: 08/09/2018

---
# <a name="run-formats-to-dynamically-add-columns-to-excel-reports-as-horizontally-expandable-ranges"></a><span data-ttu-id="b96f5-103">Выполнение форматов для динамического добавления столбцов в отчеты Excel в виде горизонтально разворачивающихся диапазонов</span><span class="sxs-lookup"><span data-stu-id="b96f5-103">Run formats to dynamically add columns to Excel reports as horizontally expandable ranges</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b96f5-104">Следующие шаги описывают, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для создания отчетов в виде файлов листов OPENXML (Excel), в которых необходимые столбцы можно создавать динамически как горизонтально расширяемые диапазоны.</span><span class="sxs-lookup"><span data-stu-id="b96f5-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="b96f5-105">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="b96f5-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="b96f5-106">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel (Часть 1. Разработка формата)".</span><span class="sxs-lookup"><span data-stu-id="b96f5-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="b96f5-107">Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="b96f5-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="b96f5-108">Найдите созданный формат</span><span class="sxs-lookup"><span data-stu-id="b96f5-108">Find created format</span></span>
1. <span data-ttu-id="b96f5-109">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="b96f5-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="b96f5-110">В дереве разверните узел "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="b96f5-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="b96f5-111">В дереве выберите "Пример модели финансовых аналитик\Пример отчета с горизонтально расширяемыми диапазонами".</span><span class="sxs-lookup"><span data-stu-id="b96f5-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="b96f5-112">Выполните формат для создания выходных данных Excel</span><span class="sxs-lookup"><span data-stu-id="b96f5-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="b96f5-113">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="b96f5-113">Click Run.</span></span>
2. <span data-ttu-id="b96f5-114">В поле "Имя аналитики" введите "BusinessUnit;CostCenter;Department".</span><span class="sxs-lookup"><span data-stu-id="b96f5-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="b96f5-115">В поле "Имя аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b96f5-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="b96f5-116">Чтобы выбрать все аналитики для текущей компании, введите следующие сведения: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="b96f5-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="b96f5-117">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="b96f5-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="b96f5-118">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="b96f5-118">Click Filter.</span></span>
5. <span data-ttu-id="b96f5-119">Выберите строку для таблицы "Журнал ГК" и поля "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="b96f5-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="b96f5-120">В поле "Критерии" введите "00057..00058".</span><span class="sxs-lookup"><span data-stu-id="b96f5-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="b96f5-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="b96f5-121">00057..00058</span></span>  
7. <span data-ttu-id="b96f5-122">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b96f5-122">Click OK.</span></span>
8. <span data-ttu-id="b96f5-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b96f5-123">Click OK.</span></span>
    * <span data-ttu-id="b96f5-124">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="b96f5-124">Review the generated output.</span></span> <span data-ttu-id="b96f5-125">Обратите внимание, что вновь созданный файл Excel содержит то же число столбцов, которое было выбрано для финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="b96f5-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="b96f5-126">Заголовок отчета в этих столбцах представляет имена финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="b96f5-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="b96f5-127">Строки проводок в этих столбцах представляют финансовые аналитики.</span><span class="sxs-lookup"><span data-stu-id="b96f5-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="b96f5-128">Выполните этот отчет и выберите другие аналитики, чтобы убедиться, что отчет не зависит от количества выбранных аналитик или количества аналитик, настроенных для данного экземпляра Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b96f5-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations instance.</span></span>  


