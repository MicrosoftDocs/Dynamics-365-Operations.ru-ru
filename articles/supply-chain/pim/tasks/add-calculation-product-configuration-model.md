--- 
title: "Добавление расчета к модели конфигурации продукта"
description: "Ниже описан порядок добавления нового расчета в модель конфигурации продукта."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 123ae1315c95693af09d7d7c96a071d606ac98f8
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="d95d3-103">Добавление расчета к модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="d95d3-103">Add a calculation to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d95d3-104">Ниже описан порядок добавления нового расчета в модель конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="d95d3-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="d95d3-105">Он показывает, как можно создать логическое выражение с помощью оператора "если" оператор для задания высоты динамика "10" для белых динамиков и "15" для всех других корпусов.</span><span class="sxs-lookup"><span data-stu-id="d95d3-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="d95d3-106">Процедура использует компонента динамика класса Hi-End в демонстрационной компании USMF.</span><span class="sxs-lookup"><span data-stu-id="d95d3-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="d95d3-107">Добавление расчета</span><span class="sxs-lookup"><span data-stu-id="d95d3-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="d95d3-108">Создание выражения расчета</span><span class="sxs-lookup"><span data-stu-id="d95d3-108">Create calculation expression</span></span>
1. <span data-ttu-id="d95d3-109">Щелкните "Изменить выражение".</span><span class="sxs-lookup"><span data-stu-id="d95d3-109">Click Edit expression.</span></span>
2. <span data-ttu-id="d95d3-110">В поле "ConstraintBody" введите в "If[CabinetFinish=="White", 10, 15]".</span><span class="sxs-lookup"><span data-stu-id="d95d3-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="d95d3-111">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="d95d3-111">Click Validate.</span></span>
4. <span data-ttu-id="d95d3-112">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="d95d3-112">Click Close.</span></span>
5. <span data-ttu-id="d95d3-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d95d3-113">Click OK.</span></span>


