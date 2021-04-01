---
title: Добавление ограничения выражения к модели конфигурации продукта
description: Ниже описан порядок добавления нового выражения ограничения в модель конфигурации продукта.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81026d8622d3f03b3b87747800f4845cda823569
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256167"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="f4641-103">Добавление ограничения выражения к модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="f4641-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4641-104">Ниже описан порядок добавления нового выражения ограничения в модель конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="f4641-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="f4641-105">Он показывает, как можно предписывать, что защита углов должна применяться к динамику, если пользователь выбрал металлическую переднюю решетку.</span><span class="sxs-lookup"><span data-stu-id="f4641-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="f4641-106">Процедура использует компонента динамика класса Hi-End в демонстрационной компании USMF.</span><span class="sxs-lookup"><span data-stu-id="f4641-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="f4641-107">Создание ограничения выражения</span><span class="sxs-lookup"><span data-stu-id="f4641-107">Create an expression constraint</span></span>
1. <span data-ttu-id="f4641-108">Щелкните "Определение модели вариантов продукта".</span><span class="sxs-lookup"><span data-stu-id="f4641-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="f4641-109">Щелкните "Модели конфигурации продукта".</span><span class="sxs-lookup"><span data-stu-id="f4641-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="f4641-110">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="f4641-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f4641-111">В этом примере используется модель динамика класса Hi-End.</span><span class="sxs-lookup"><span data-stu-id="f4641-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="f4641-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f4641-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f4641-113">Разверните раздел "Ограничения".</span><span class="sxs-lookup"><span data-stu-id="f4641-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="f4641-114">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f4641-114">Click Add.</span></span>
7. <span data-ttu-id="f4641-115">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f4641-115">Click Create.</span></span>
8. <span data-ttu-id="f4641-116">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f4641-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="f4641-117">Ввести выражение</span><span class="sxs-lookup"><span data-stu-id="f4641-117">Enter expression</span></span>
1. <span data-ttu-id="f4641-118">Щелкните "Изменить выражение".</span><span class="sxs-lookup"><span data-stu-id="f4641-118">Click Edit expression.</span></span>
    * <span data-ttu-id="f4641-119">Если вы разблокируете интерфейс в записи задач на этом этапе, можно использовать IntelliSense и список символов для построения выражения ограничения.</span><span class="sxs-lookup"><span data-stu-id="f4641-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="f4641-120">В поле "ConstraintBody" введите в "Implies[FrontGrill=="Metal", CornerProtection]".</span><span class="sxs-lookup"><span data-stu-id="f4641-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="f4641-121">Логика этого выражения гласит: если передняя решетка металлическая, должен быть выбран параметр защиты углов.</span><span class="sxs-lookup"><span data-stu-id="f4641-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="f4641-122">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="f4641-122">Click Validate.</span></span>
    * <span data-ttu-id="f4641-123">Функция проверки выполняется через выражение ограничения и проверяет наличие синтаксических ошибок.</span><span class="sxs-lookup"><span data-stu-id="f4641-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="f4641-124">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="f4641-124">Click Close.</span></span>
5. <span data-ttu-id="f4641-125">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f4641-125">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]