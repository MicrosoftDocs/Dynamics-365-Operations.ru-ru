---
title: Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 4. Выполнение отчета)
description: В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
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
ms.openlocfilehash: fb7f49310aa25ff7c17ab4bcd50e1842be84fe2d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684747"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="28f91-103">Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 4. Выполнение отчета)</span><span class="sxs-lookup"><span data-stu-id="28f91-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28f91-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="28f91-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="28f91-105">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="28f91-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="28f91-106">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 3. Разработка отчета)".</span><span class="sxs-lookup"><span data-stu-id="28f91-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="28f91-107">Также необходимо настроить типы документов по умолчанию на странице "Параметры электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="28f91-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="28f91-108">Типы документов по умолчанию также задаются при загрузке и импорте любой конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="28f91-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="28f91-109">Выполнение отчета</span><span class="sxs-lookup"><span data-stu-id="28f91-109">Run report</span></span>
1. <span data-ttu-id="28f91-110">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="28f91-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="28f91-111">В дереве разверните узел "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="28f91-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="28f91-112">В дереве выберите "Пример модели финансовых аналитик\Отчет журнала ГК".</span><span class="sxs-lookup"><span data-stu-id="28f91-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="28f91-113">Щелкните Выполнить.</span><span class="sxs-lookup"><span data-stu-id="28f91-113">Click Run.</span></span>
<span data-ttu-id="28f91-114">![Страница конфигураций электронной отчетности](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="28f91-114">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="28f91-115">В поле "Имя аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="28f91-115">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="28f91-116">Чтобы выбрать все аналитики в текущей компании, введите следующие сведения: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="28f91-116">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![Страница конфигураций электронной отчетности](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="28f91-118">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="28f91-118">Expand the Records to include section.</span></span>
7. <span data-ttu-id="28f91-119">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="28f91-119">Click Filter.</span></span>
8. <span data-ttu-id="28f91-120">Выберите строку для таблицы "Журнал ГК" и поля "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="28f91-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="28f91-121">В поле "Критерии" введите "00057".</span><span class="sxs-lookup"><span data-stu-id="28f91-121">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="28f91-122">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="28f91-122">Click OK.</span></span>
11. <span data-ttu-id="28f91-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="28f91-123">Click OK.</span></span>
<span data-ttu-id="28f91-124">![Страница конфигураций электронной отчетности](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="28f91-124">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="28f91-125">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="28f91-125">Review the generated output.</span></span> <span data-ttu-id="28f91-126">Для каждой проводки выбранной партии представлены финансовые аналитики из соответствующих аналитик.</span><span class="sxs-lookup"><span data-stu-id="28f91-126">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="28f91-127">Выполните этот отчет и выберите другие аналитики, чтобы убедиться, что отчет не зависит от количества выбранных аналитик или числе аналитик, настроенных для данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="28f91-127">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![Страница конфигураций электронной отчетности](../media/er-financial-dimensions-guides-run4.png)
