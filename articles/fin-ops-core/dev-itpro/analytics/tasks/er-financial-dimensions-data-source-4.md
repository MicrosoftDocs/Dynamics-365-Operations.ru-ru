---
title: Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 4. Выполнение отчета)
description: В этой теме описывается, как настроить модель электронной отчетности (ER) для использования финансовых аналитик в качестве источника данных для отчетов электронной отчетности. (Часть 4)
author: NickSelin
ms.date: 05/27/2020
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
ms.openlocfilehash: 4a06936da71d7b05f312a99c8c11d148403d29c3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752396"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="3bccf-104">Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 4. Выполнение отчета)</span><span class="sxs-lookup"><span data-stu-id="3bccf-104">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3bccf-105">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="3bccf-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="3bccf-106">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="3bccf-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="3bccf-107">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 3. Разработка отчета)".</span><span class="sxs-lookup"><span data-stu-id="3bccf-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="3bccf-108">Также необходимо настроить типы документов по умолчанию на странице "Параметры электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="3bccf-108">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="3bccf-109">Типы документов по умолчанию также задаются при загрузке и импорте любой конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="3bccf-109">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="3bccf-110">Выполнение отчета</span><span class="sxs-lookup"><span data-stu-id="3bccf-110">Run report</span></span>
1. <span data-ttu-id="3bccf-111">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="3bccf-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="3bccf-112">В дереве разверните узел "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="3bccf-112">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="3bccf-113">В дереве выберите "Пример модели финансовых аналитик\Отчет журнала ГК".</span><span class="sxs-lookup"><span data-stu-id="3bccf-113">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="3bccf-114">Щелкните Выполнить.</span><span class="sxs-lookup"><span data-stu-id="3bccf-114">Click Run.</span></span>
<span data-ttu-id="3bccf-115">![Страница конфигураций электронной отчетности](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="3bccf-115">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="3bccf-116">В поле "Имя аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3bccf-116">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="3bccf-117">Чтобы выбрать все аналитики в текущей компании, введите следующие сведения: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="3bccf-117">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![Страница конфигураций электронной отчетности](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="3bccf-119">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="3bccf-119">Expand the Records to include section.</span></span>
7. <span data-ttu-id="3bccf-120">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="3bccf-120">Click Filter.</span></span>
8. <span data-ttu-id="3bccf-121">Выберите строку для таблицы "Журнал ГК" и поля "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="3bccf-121">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="3bccf-122">В поле "Критерии" введите "00057".</span><span class="sxs-lookup"><span data-stu-id="3bccf-122">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="3bccf-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3bccf-123">Click OK.</span></span>
11. <span data-ttu-id="3bccf-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3bccf-124">Click OK.</span></span>
<span data-ttu-id="3bccf-125">![Страница конфигураций электронной отчетности](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="3bccf-125">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="3bccf-126">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="3bccf-126">Review the generated output.</span></span> <span data-ttu-id="3bccf-127">Для каждой проводки выбранной партии представлены финансовые аналитики из соответствующих аналитик.</span><span class="sxs-lookup"><span data-stu-id="3bccf-127">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="3bccf-128">Выполните этот отчет и выберите другие аналитики, чтобы убедиться, что отчет не зависит от количества выбранных аналитик или числе аналитик, настроенных для данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3bccf-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![Страница конфигураций электронной отчетности](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]