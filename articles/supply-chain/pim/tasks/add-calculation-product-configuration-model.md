---
title: Добавление расчета к модели конфигурации продукта
description: Ниже описан порядок добавления нового расчета в модель конфигурации продукта.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e703c6d505f1e2e77f454732301de7a6c130c58a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986511"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="2f89e-103">Добавление расчета к модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="2f89e-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2f89e-104">Ниже описан порядок добавления нового расчета в модель конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="2f89e-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="2f89e-105">Он показывает, как можно создать логическое выражение с помощью оператора "если" оператор для задания высоты динамика "10" для белых динамиков и "15" для всех других корпусов.</span><span class="sxs-lookup"><span data-stu-id="2f89e-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="2f89e-106">Процедура использует компонента динамика класса Hi-End в демонстрационной компании USMF.</span><span class="sxs-lookup"><span data-stu-id="2f89e-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="2f89e-107">Добавление расчета</span><span class="sxs-lookup"><span data-stu-id="2f89e-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="2f89e-108">Создание выражения расчета</span><span class="sxs-lookup"><span data-stu-id="2f89e-108">Create calculation expression</span></span>
1. <span data-ttu-id="2f89e-109">Щелкните "Изменить выражение".</span><span class="sxs-lookup"><span data-stu-id="2f89e-109">Click Edit expression.</span></span>
2. <span data-ttu-id="2f89e-110">В поле "ConstraintBody" введите в "If[CabinetFinish=="White", 10, 15]".</span><span class="sxs-lookup"><span data-stu-id="2f89e-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="2f89e-111">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="2f89e-111">Click Validate.</span></span>
4. <span data-ttu-id="2f89e-112">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="2f89e-112">Click Close.</span></span>
5. <span data-ttu-id="2f89e-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2f89e-113">Click OK.</span></span>

