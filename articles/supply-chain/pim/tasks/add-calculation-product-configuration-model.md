---
title: Добавление расчета к модели конфигурации продукта
description: Ниже описан порядок добавления нового расчета в модель конфигурации продукта.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55f8fcfdafb2d5fb5a4d4800221fabf4b2111f86
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150271"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="0fa0f-103">Добавление расчета к модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="0fa0f-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0fa0f-104">Ниже описан порядок добавления нового расчета в модель конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="0fa0f-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="0fa0f-105">Он показывает, как можно создать логическое выражение с помощью оператора "если" оператор для задания высоты динамика "10" для белых динамиков и "15" для всех других корпусов.</span><span class="sxs-lookup"><span data-stu-id="0fa0f-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="0fa0f-106">Процедура использует компонента динамика класса Hi-End в демонстрационной компании USMF.</span><span class="sxs-lookup"><span data-stu-id="0fa0f-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="0fa0f-107">Добавление расчета</span><span class="sxs-lookup"><span data-stu-id="0fa0f-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="0fa0f-108">Создание выражения расчета</span><span class="sxs-lookup"><span data-stu-id="0fa0f-108">Create calculation expression</span></span>
1. <span data-ttu-id="0fa0f-109">Щелкните "Изменить выражение".</span><span class="sxs-lookup"><span data-stu-id="0fa0f-109">Click Edit expression.</span></span>
2. <span data-ttu-id="0fa0f-110">В поле "ConstraintBody" введите в "If[CabinetFinish=="White", 10, 15]".</span><span class="sxs-lookup"><span data-stu-id="0fa0f-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="0fa0f-111">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="0fa0f-111">Click Validate.</span></span>
4. <span data-ttu-id="0fa0f-112">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="0fa0f-112">Click Close.</span></span>
5. <span data-ttu-id="0fa0f-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="0fa0f-113">Click OK.</span></span>

