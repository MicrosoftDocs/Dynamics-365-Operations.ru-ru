---
title: Электронная отчетность — Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel (Часть 2. Выполнение формата)
description: Следующие шаги описывают, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для создания отчетов в виде файлов листов OPENXML (Excel), в которых необходимые столбцы можно создавать динамически как горизонтально расширяемые диапазоны.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 33c1a3134659bb66a67166fec3d7f53af0aa4c6c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544434"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2-run-format"></a><span data-ttu-id="ca54e-103">Электронная отчетность — Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel (Часть 2. Выполнение формата)</span><span class="sxs-lookup"><span data-stu-id="ca54e-103">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2: Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca54e-104">Следующие шаги описывают, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для создания отчетов в виде файлов листов OPENXML (Excel), в которых необходимые столбцы можно создавать динамически как горизонтально расширяемые диапазоны.</span><span class="sxs-lookup"><span data-stu-id="ca54e-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="ca54e-105">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="ca54e-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="ca54e-106">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel (Часть 1. Разработка формата)".</span><span class="sxs-lookup"><span data-stu-id="ca54e-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="ca54e-107">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="ca54e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="ca54e-108">Найдите созданный формат</span><span class="sxs-lookup"><span data-stu-id="ca54e-108">Find created format</span></span>
1. <span data-ttu-id="ca54e-109">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="ca54e-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ca54e-110">В дереве разверните узел "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="ca54e-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="ca54e-111">В дереве выберите "Пример модели финансовых аналитик\Пример отчета с горизонтально расширяемыми диапазонами".</span><span class="sxs-lookup"><span data-stu-id="ca54e-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="ca54e-112">Выполните формат для создания выходных данных Excel</span><span class="sxs-lookup"><span data-stu-id="ca54e-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="ca54e-113">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="ca54e-113">Click Run.</span></span>
2. <span data-ttu-id="ca54e-114">В поле "Имя аналитики" введите "BusinessUnit;CostCenter;Department".</span><span class="sxs-lookup"><span data-stu-id="ca54e-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="ca54e-115">В поле "Имя аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ca54e-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="ca54e-116">Чтобы выбрать все аналитики для текущей компании, введите следующие сведения: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="ca54e-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="ca54e-117">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="ca54e-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="ca54e-118">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="ca54e-118">Click Filter.</span></span>
5. <span data-ttu-id="ca54e-119">Выберите строку для таблицы "Журнал ГК" и поля "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="ca54e-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="ca54e-120">В поле "Критерии" введите "00057..00058".</span><span class="sxs-lookup"><span data-stu-id="ca54e-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="ca54e-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="ca54e-121">00057..00058</span></span>  
7. <span data-ttu-id="ca54e-122">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ca54e-122">Click OK.</span></span>
8. <span data-ttu-id="ca54e-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ca54e-123">Click OK.</span></span>
    * <span data-ttu-id="ca54e-124">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="ca54e-124">Review the generated output.</span></span> <span data-ttu-id="ca54e-125">Обратите внимание, что вновь созданный файл Excel содержит то же число столбцов, которое было выбрано для финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="ca54e-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="ca54e-126">Заголовок отчета в этих столбцах представляет имена финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="ca54e-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="ca54e-127">Строки проводок в этих столбцах представляют финансовые аналитики.</span><span class="sxs-lookup"><span data-stu-id="ca54e-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="ca54e-128">Выполните этот отчет и выберите другие аналитики, чтобы убедиться, что отчет не зависит от количества выбранных аналитик или количества аналитик, настроенных для данного экземпляра Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="ca54e-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  

