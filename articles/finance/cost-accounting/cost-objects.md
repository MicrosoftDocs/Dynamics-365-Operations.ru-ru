---
title: Аналитики объекта затрат
description: Когда вы анализируете затраты, вы используете аналитики элемента затрат, чтобы определить направление потока затрат. Аналитики объекта затрат можно использовать для определения того, где необходимо назначить затраты. В этом разделе представлены сведения об аналитиках объекта затрат.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMCostObject
audience: Application User
ms.reviewer: roschlom
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 20ae6295389fa3cbaa7c90844d2a90f1e38387c4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818787"
---
# <a name="cost-object-dimensions"></a><span data-ttu-id="e1bf5-105">Аналитики объекта затрат</span><span class="sxs-lookup"><span data-stu-id="e1bf5-105">Cost object dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1bf5-106">Когда вы анализируете затраты, вы используете аналитики элемента затрат, чтобы определить направление потока затрат.</span><span class="sxs-lookup"><span data-stu-id="e1bf5-106">When you analyze costs, you use cost element dimensions to determine where costs flow to.</span></span> <span data-ttu-id="e1bf5-107">Аналитики объекта затрат можно использовать для определения того, где необходимо назначить затраты.</span><span class="sxs-lookup"><span data-stu-id="e1bf5-107">You use cost object dimensions to determine where you should assign costs.</span></span> <span data-ttu-id="e1bf5-108">В этом разделе представлены сведения об аналитиках объекта затрат.</span><span class="sxs-lookup"><span data-stu-id="e1bf5-108">This topic provides information about cost object dimensions.</span></span>

<span data-ttu-id="e1bf5-109">Объект затрат может быть любым типом объекта, который требуется оценить, распределить на него затраты или измерить напрямую.</span><span class="sxs-lookup"><span data-stu-id="e1bf5-109">A cost object can be any type of object that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="e1bf5-110">Типичные объекты затрат включают продукты, проекты, ресурсы, подразделения, центры затрат и географические регионы.</span><span class="sxs-lookup"><span data-stu-id="e1bf5-110">Typical cost objects include products, projects, resources, departments, cost centers, and geographical regions.</span></span> <span data-ttu-id="e1bf5-111">Руководство использует объекты затраты для определения количественной меры затрат, а также и для проведения анализа прибыльности.</span><span class="sxs-lookup"><span data-stu-id="e1bf5-111">Management uses cost objects to quantify costs and also to drive profitability analysis.</span></span>

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a><span data-ttu-id="e1bf5-112">Аналитики объектов затрат и члены аналитик объектов затрат</span><span class="sxs-lookup"><span data-stu-id="e1bf5-112">Cost object dimensions and cost object dimension members</span></span>
<span data-ttu-id="e1bf5-113">Объекты затрат известны как *аналитики объектов затрат*.</span><span class="sxs-lookup"><span data-stu-id="e1bf5-113">Cost objects are known as *cost object dimensions*.</span></span> <span data-ttu-id="e1bf5-114">После того как вы решили, на какой объект должна ссылаться аналитика объекта затрат, необходимо указать отдельные значения аналитики или импортировать их в модуль "Учет затрат" из других исходных систем.</span><span class="sxs-lookup"><span data-stu-id="e1bf5-114">After you’ve decided which entity the cost object dimension should refer to, you must specify the individual dimension values or import them into Cost accounting from other source systems.</span></span> <span data-ttu-id="e1bf5-115">Эти отдельные значения аналитики называются *членами аналитики объекта затрат*.</span><span class="sxs-lookup"><span data-stu-id="e1bf5-115">These individual dimension values are known as *cost object dimension members*.</span></span> <span data-ttu-id="e1bf5-116">Например, вы хотите использовать финансовую аналитику, которая называется "Центр затрат" как аналитику объекта затрат.</span><span class="sxs-lookup"><span data-stu-id="e1bf5-116">For example, you want to use the financial dimension that is named Cost center as the cost object dimension.</span></span> <span data-ttu-id="e1bf5-117">Чтобы посмотреть, как затраты переносятся в отдельные центры затрат, необходимо импортировать члены аналитики объекта затрат.</span><span class="sxs-lookup"><span data-stu-id="e1bf5-117">To see how costs flow to the individual cost centers, you must import the cost object dimension members.</span></span> <span data-ttu-id="e1bf5-118">В этом случае члены аналитики объекта затрат являются фактическими центрами затрат, такими как продажи, производство, администрирование и географические местоположения.</span><span class="sxs-lookup"><span data-stu-id="e1bf5-118">In this case, the cost object dimension members are the actual cost centers, such as Sales, Production, Administration, and Geographic locations.</span></span> <span data-ttu-id="e1bf5-119">Следующий снимок экрана показывает пример центров затрат как аналитик объекта затрат со своими фактическими центрами затрат в качестве членов аналитики объекта затрат.</span><span class="sxs-lookup"><span data-stu-id="e1bf5-119">The following screenshot shows an example of Cost Centers as the cost object dimension with its actual cost centers as cost object dimension members.</span></span> 

<span data-ttu-id="e1bf5-120">[![Снимок экрана, отображающий центры затрат как аналитику объекта затрат](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="e1bf5-120">[![Screenshot showing Cost Centers as cost object dimension](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span></span>

## <a name="import-cost-object-dimension-members-through-data-connectors"></a><span data-ttu-id="e1bf5-121">Импорт членов аналитики объекта затрат через соединители данных</span><span class="sxs-lookup"><span data-stu-id="e1bf5-121">Import cost object dimension members through data connectors</span></span>
<span data-ttu-id="e1bf5-122">Чтобы упростить импорт членов аналитики объекта затрат используются соединители данных для извлечения значений из объектов, которые необходимо использовать в качестве аналитик объекта затрат.</span><span class="sxs-lookup"><span data-stu-id="e1bf5-122">To make the import of cost object dimension members easier, you use data connectors to retrieve the values from the entities that you want to use as cost object dimensions.</span></span> <span data-ttu-id="e1bf5-123">Можно использовать предварительно подготовленные соединители данных или пользовательские соединители данных, собранные вами.</span><span class="sxs-lookup"><span data-stu-id="e1bf5-123">You can use either the pre-built data connectors or custom data connectors that you build.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]