---
title: Электронная отчетность — Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel (Часть 2. Выполнение формата)
description: В этой теме описывается, как настроить формат электронной отчетности (ER) для создания отчетов в виде файлов электронных таблиц OPENXML (Excel). (Часть 2)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee0b8c997549bca2cae5500c926ccba916a473b5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569541"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="9b1b0-104">Электронная отчетность — Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel (Часть 2. Выполнение формата)</span><span class="sxs-lookup"><span data-stu-id="9b1b0-104">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9b1b0-105">Следующие шаги описывают, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для создания отчетов в виде файлов листов OPENXML (Excel), в которых необходимые столбцы можно создавать динамически как горизонтально расширяемые диапазоны.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="9b1b0-106">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="9b1b0-107">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel (Часть 1. Разработка формата)".</span><span class="sxs-lookup"><span data-stu-id="9b1b0-107">To complete these steps, you must first complete the steps in the "ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)" procedure.</span></span>

<span data-ttu-id="9b1b0-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="9b1b0-109">Найдите созданный формат</span><span class="sxs-lookup"><span data-stu-id="9b1b0-109">Find created format</span></span>
1. <span data-ttu-id="9b1b0-110">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="9b1b0-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="9b1b0-111">В дереве разверните узел "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="9b1b0-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="9b1b0-112">В дереве выберите "Пример модели финансовых аналитик\Пример отчета с горизонтально расширяемыми диапазонами".</span><span class="sxs-lookup"><span data-stu-id="9b1b0-112">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="9b1b0-113">Выполните формат для создания выходных данных Excel</span><span class="sxs-lookup"><span data-stu-id="9b1b0-113">Execute format to create Excel output</span></span>
1. <span data-ttu-id="9b1b0-114">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="9b1b0-114">Click Run.</span></span>
2. <span data-ttu-id="9b1b0-115">В поле "Имя аналитики" введите "BusinessUnit;CostCenter;Department".</span><span class="sxs-lookup"><span data-stu-id="9b1b0-115">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="9b1b0-116">В поле "Имя аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-116">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="9b1b0-117">Чтобы выбрать все аналитики для текущей компании, введите следующие сведения: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="9b1b0-117">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="9b1b0-118">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="9b1b0-118">Expand the Records to include section.</span></span>
4. <span data-ttu-id="9b1b0-119">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="9b1b0-119">Click Filter.</span></span>
5. <span data-ttu-id="9b1b0-120">Выберите строку для таблицы "Журнал ГК" и поля "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="9b1b0-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="9b1b0-121">В поле "Критерии" введите "00057..00058".</span><span class="sxs-lookup"><span data-stu-id="9b1b0-121">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="9b1b0-122">00057..00058</span><span class="sxs-lookup"><span data-stu-id="9b1b0-122">00057..00058</span></span>  
7. <span data-ttu-id="9b1b0-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9b1b0-123">Click OK.</span></span>
8. <span data-ttu-id="9b1b0-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9b1b0-124">Click OK.</span></span>
    * <span data-ttu-id="9b1b0-125">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-125">Review the generated output.</span></span> <span data-ttu-id="9b1b0-126">Обратите внимание, что вновь созданный файл Excel содержит то же число столбцов, которое было выбрано для финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-126">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="9b1b0-127">Заголовок отчета в этих столбцах представляет имена финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-127">The report header in those columns represents financial dimensions' names.</span></span> <span data-ttu-id="9b1b0-128">Строки проводок в этих столбцах представляют финансовые аналитики.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-128">The transactions' lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="9b1b0-129">Выполните этот отчет и выберите другие аналитики, чтобы убедиться, что отчет не зависит от количества выбранных аналитик или числе аналитик, настроенных для данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9b1b0-129">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]