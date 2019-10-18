---
title: Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 4. Выполнение отчета)
description: В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.
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
ms.openlocfilehash: aa5b726a7c400da09381944f3303f7ac4bb796aa
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182424"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4-run-the-report"></a><span data-ttu-id="9d49f-103">Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 4. Выполнение отчета)</span><span class="sxs-lookup"><span data-stu-id="9d49f-103">ER Use financial dimensions as a data source (Part 4: Run the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9d49f-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="9d49f-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="9d49f-105">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="9d49f-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="9d49f-106">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 3. Разработка отчета)".</span><span class="sxs-lookup"><span data-stu-id="9d49f-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="9d49f-107">Также необходимо настроить типы документов по умолчанию на странице "Параметры электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="9d49f-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="9d49f-108">Типы документов по умолчанию также задаются при загрузке и импорте любой конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="9d49f-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="9d49f-109">Выполнение отчета</span><span class="sxs-lookup"><span data-stu-id="9d49f-109">Run report</span></span>
1. <span data-ttu-id="9d49f-110">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="9d49f-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="9d49f-111">В дереве разверните узел "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="9d49f-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="9d49f-112">В дереве выберите "Пример модели финансовых аналитик\Отчет журнала ГК".</span><span class="sxs-lookup"><span data-stu-id="9d49f-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="9d49f-113">Щелкните Выполнить.</span><span class="sxs-lookup"><span data-stu-id="9d49f-113">Click Run.</span></span>
5. <span data-ttu-id="9d49f-114">В поле "Имя аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9d49f-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="9d49f-115">Чтобы выбрать все аналитики в текущей компании, введите следующие сведения:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="9d49f-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="9d49f-116">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="9d49f-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="9d49f-117">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="9d49f-117">Click Filter.</span></span>
8. <span data-ttu-id="9d49f-118">Выберите строку для таблицы "Журнал ГК" и поля "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="9d49f-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="9d49f-119">В поле "Критерии" введите "00057".</span><span class="sxs-lookup"><span data-stu-id="9d49f-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="9d49f-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9d49f-120">Click OK.</span></span>
11. <span data-ttu-id="9d49f-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9d49f-121">Click OK.</span></span>
    * <span data-ttu-id="9d49f-122">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="9d49f-122">Review the generated output.</span></span> <span data-ttu-id="9d49f-123">Обратите внимание, что для каждой проводки выбранной партии представлены финансовые аналитики из соответствующих аналитик.</span><span class="sxs-lookup"><span data-stu-id="9d49f-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="9d49f-124">Выполните этот отчет и выберите другие аналитики, чтобы убедиться, что отчет не зависит от количества выбранных аналитик или числе аналитик, настроенных для данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9d49f-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  

