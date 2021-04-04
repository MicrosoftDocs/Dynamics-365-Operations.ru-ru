---
title: Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 4. Выполнение отчета)
description: В этой теме описывается, как настроить модель электронной отчетности (ER) для использования финансовых аналитик в качестве источника данных для отчетов электронной отчетности. (Часть 4)
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: ae7cc1a60234ef09b80950cbf0c7f18b0d65709d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565222"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="ea7f7-104">Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 4. Выполнение отчета)</span><span class="sxs-lookup"><span data-stu-id="ea7f7-104">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ea7f7-105">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="ea7f7-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="ea7f7-106">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="ea7f7-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="ea7f7-107">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 3. Разработка отчета)".</span><span class="sxs-lookup"><span data-stu-id="ea7f7-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="ea7f7-108">Также необходимо настроить типы документов по умолчанию на странице "Параметры электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="ea7f7-108">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="ea7f7-109">Типы документов по умолчанию также задаются при загрузке и импорте любой конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="ea7f7-109">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="ea7f7-110">Выполнение отчета</span><span class="sxs-lookup"><span data-stu-id="ea7f7-110">Run report</span></span>
1. <span data-ttu-id="ea7f7-111">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="ea7f7-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ea7f7-112">В дереве разверните узел "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="ea7f7-112">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="ea7f7-113">В дереве выберите "Пример модели финансовых аналитик\Отчет журнала ГК".</span><span class="sxs-lookup"><span data-stu-id="ea7f7-113">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="ea7f7-114">Щелкните Выполнить.</span><span class="sxs-lookup"><span data-stu-id="ea7f7-114">Click Run.</span></span>
<span data-ttu-id="ea7f7-115">![Страница конфигураций электронной отчетности](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="ea7f7-115">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="ea7f7-116">В поле "Имя аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ea7f7-116">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="ea7f7-117">Чтобы выбрать все аналитики в текущей компании, введите следующие сведения: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="ea7f7-117">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![Страница конфигураций электронной отчетности](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="ea7f7-119">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="ea7f7-119">Expand the Records to include section.</span></span>
7. <span data-ttu-id="ea7f7-120">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="ea7f7-120">Click Filter.</span></span>
8. <span data-ttu-id="ea7f7-121">Выберите строку для таблицы "Журнал ГК" и поля "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="ea7f7-121">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="ea7f7-122">В поле "Критерии" введите "00057".</span><span class="sxs-lookup"><span data-stu-id="ea7f7-122">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="ea7f7-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ea7f7-123">Click OK.</span></span>
11. <span data-ttu-id="ea7f7-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ea7f7-124">Click OK.</span></span>
<span data-ttu-id="ea7f7-125">![Страница конфигураций электронной отчетности](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="ea7f7-125">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="ea7f7-126">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="ea7f7-126">Review the generated output.</span></span> <span data-ttu-id="ea7f7-127">Для каждой проводки выбранной партии представлены финансовые аналитики из соответствующих аналитик.</span><span class="sxs-lookup"><span data-stu-id="ea7f7-127">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="ea7f7-128">Выполните этот отчет и выберите другие аналитики, чтобы убедиться, что отчет не зависит от количества выбранных аналитик или числе аналитик, настроенных для данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ea7f7-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![Страница конфигураций электронной отчетности](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]