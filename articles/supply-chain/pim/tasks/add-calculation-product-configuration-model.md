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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2db8fb922b085a7f118822ef4fd974ac338f4d99
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="56a43-103">Добавление расчета к модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="56a43-103">Add a calculation to a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56a43-104">Ниже описан порядок добавления нового расчета в модель конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="56a43-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="56a43-105">Он показывает, как можно создать логическое выражение с помощью оператора "если" оператор для задания высоты динамика "10" для белых динамиков и "15" для всех других корпусов.</span><span class="sxs-lookup"><span data-stu-id="56a43-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="56a43-106">Процедура использует компонента динамика класса Hi-End в демонстрационной компании USMF.</span><span class="sxs-lookup"><span data-stu-id="56a43-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="56a43-107">Добавление расчета</span><span class="sxs-lookup"><span data-stu-id="56a43-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="56a43-108">Создание выражения расчета</span><span class="sxs-lookup"><span data-stu-id="56a43-108">Create calculation expression</span></span>
1. <span data-ttu-id="56a43-109">Щелкните "Изменить выражение".</span><span class="sxs-lookup"><span data-stu-id="56a43-109">Click Edit expression.</span></span>
2. <span data-ttu-id="56a43-110">В поле "ConstraintBody" введите в "If[CabinetFinish=="White", 10, 15]".</span><span class="sxs-lookup"><span data-stu-id="56a43-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="56a43-111">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="56a43-111">Click Validate.</span></span>
4. <span data-ttu-id="56a43-112">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="56a43-112">Click Close.</span></span>
5. <span data-ttu-id="56a43-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="56a43-113">Click OK.</span></span>


