--- 
title: "Добавление ограничения выражения к модели конфигурации продукта"
description: "Ниже описан порядок добавления нового выражения ограничения в модель конфигурации продукта."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 56f94b82f8b2642b12a993bde7d6bb323da79f98
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="76e96-103">Добавление ограничения выражения к модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="76e96-103">Add an expression constraint to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76e96-104">Ниже описан порядок добавления нового выражения ограничения в модель конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="76e96-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="76e96-105">Он показывает, как можно предписывать, что защита углов должна применяться к динамику, если пользователь выбрал металлическую переднюю решетку.</span><span class="sxs-lookup"><span data-stu-id="76e96-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="76e96-106">Процедура использует компонента динамика класса Hi-End в демонстрационной компании USMF.</span><span class="sxs-lookup"><span data-stu-id="76e96-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="76e96-107">Создание ограничения выражения</span><span class="sxs-lookup"><span data-stu-id="76e96-107">Create an expression constraint</span></span>
1. <span data-ttu-id="76e96-108">Щелкните "Определение модели вариантов продукта".</span><span class="sxs-lookup"><span data-stu-id="76e96-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="76e96-109">Щелкните "Модели конфигурации продукта".</span><span class="sxs-lookup"><span data-stu-id="76e96-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="76e96-110">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="76e96-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="76e96-111">В этом примере используется модель динамика класса Hi-End.</span><span class="sxs-lookup"><span data-stu-id="76e96-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="76e96-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="76e96-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="76e96-113">Разверните раздел "Ограничения".</span><span class="sxs-lookup"><span data-stu-id="76e96-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="76e96-114">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="76e96-114">Click Add.</span></span>
7. <span data-ttu-id="76e96-115">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="76e96-115">Click Create.</span></span>
8. <span data-ttu-id="76e96-116">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="76e96-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="76e96-117">Ввести выражение</span><span class="sxs-lookup"><span data-stu-id="76e96-117">Enter expression</span></span>
1. <span data-ttu-id="76e96-118">Щелкните "Изменить выражение".</span><span class="sxs-lookup"><span data-stu-id="76e96-118">Click Edit expression.</span></span>
    * <span data-ttu-id="76e96-119">Если вы разблокируете интерфейс в записи задач на этом этапе, можно использовать IntelliSense и список символов для построения выражения ограничения.</span><span class="sxs-lookup"><span data-stu-id="76e96-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="76e96-120">В поле "ConstraintBody" введите в "Implies[FrontGrill=="Metal", CornerProtection]".</span><span class="sxs-lookup"><span data-stu-id="76e96-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="76e96-121">Логика этого выражения гласит: если передняя решетка металлическая, должен быть выбран параметр защиты углов.</span><span class="sxs-lookup"><span data-stu-id="76e96-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="76e96-122">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="76e96-122">Click Validate.</span></span>
    * <span data-ttu-id="76e96-123">Функция проверки выполняется через выражение ограничения и проверяет наличие синтаксических ошибок.</span><span class="sxs-lookup"><span data-stu-id="76e96-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="76e96-124">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="76e96-124">Click Close.</span></span>
5. <span data-ttu-id="76e96-125">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="76e96-125">Click OK.</span></span>


