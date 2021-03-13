---
title: Электронная отчетность — Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel (Часть 2. Выполнение формата)
description: В этой теме описывается, как настроить формат электронной отчетности (ER) для создания отчетов в виде файлов электронных таблиц OPENXML (Excel). (Часть 2)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c13179f424d570b23615fe81ca5ddfb7afed582d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093484"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="c42ab-104">Электронная отчетность — Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel (Часть 2. Выполнение формата)</span><span class="sxs-lookup"><span data-stu-id="c42ab-104">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c42ab-105">Следующие шаги описывают, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для создания отчетов в виде файлов листов OPENXML (Excel), в которых необходимые столбцы можно создавать динамически как горизонтально расширяемые диапазоны.</span><span class="sxs-lookup"><span data-stu-id="c42ab-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="c42ab-106">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="c42ab-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="c42ab-107">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel (Часть 1. Разработка формата)".</span><span class="sxs-lookup"><span data-stu-id="c42ab-107">To complete these steps, you must first complete the steps in the "ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)" procedure.</span></span>

<span data-ttu-id="c42ab-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="c42ab-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="c42ab-109">Найдите созданный формат</span><span class="sxs-lookup"><span data-stu-id="c42ab-109">Find created format</span></span>
1. <span data-ttu-id="c42ab-110">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="c42ab-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c42ab-111">В дереве разверните узел "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="c42ab-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="c42ab-112">В дереве выберите "Пример модели финансовых аналитик\Пример отчета с горизонтально расширяемыми диапазонами".</span><span class="sxs-lookup"><span data-stu-id="c42ab-112">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="c42ab-113">Выполните формат для создания выходных данных Excel</span><span class="sxs-lookup"><span data-stu-id="c42ab-113">Execute format to create Excel output</span></span>
1. <span data-ttu-id="c42ab-114">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="c42ab-114">Click Run.</span></span>
2. <span data-ttu-id="c42ab-115">В поле "Имя аналитики" введите "BusinessUnit;CostCenter;Department".</span><span class="sxs-lookup"><span data-stu-id="c42ab-115">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="c42ab-116">В поле "Имя аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c42ab-116">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="c42ab-117">Чтобы выбрать все аналитики для текущей компании, введите следующие сведения: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="c42ab-117">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="c42ab-118">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="c42ab-118">Expand the Records to include section.</span></span>
4. <span data-ttu-id="c42ab-119">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="c42ab-119">Click Filter.</span></span>
5. <span data-ttu-id="c42ab-120">Выберите строку для таблицы "Журнал ГК" и поля "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="c42ab-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="c42ab-121">В поле "Критерии" введите "00057..00058".</span><span class="sxs-lookup"><span data-stu-id="c42ab-121">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="c42ab-122">00057..00058</span><span class="sxs-lookup"><span data-stu-id="c42ab-122">00057..00058</span></span>  
7. <span data-ttu-id="c42ab-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c42ab-123">Click OK.</span></span>
8. <span data-ttu-id="c42ab-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c42ab-124">Click OK.</span></span>
    * <span data-ttu-id="c42ab-125">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="c42ab-125">Review the generated output.</span></span> <span data-ttu-id="c42ab-126">Обратите внимание, что вновь созданный файл Excel содержит то же число столбцов, которое было выбрано для финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="c42ab-126">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="c42ab-127">Заголовок отчета в этих столбцах представляет имена финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="c42ab-127">The report header in those columns represents financial dimensions' names.</span></span> <span data-ttu-id="c42ab-128">Строки проводок в этих столбцах представляют финансовые аналитики.</span><span class="sxs-lookup"><span data-stu-id="c42ab-128">The transactions' lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="c42ab-129">Выполните этот отчет и выберите другие аналитики, чтобы убедиться, что отчет не зависит от количества выбранных аналитик или числе аналитик, настроенных для данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c42ab-129">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  

