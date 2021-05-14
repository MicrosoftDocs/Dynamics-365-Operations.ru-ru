---
title: Добавление ограничения выражения к модели конфигурации продукта
description: Ниже описан порядок добавления нового выражения ограничения в модель конфигурации продукта.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920889"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="ed39c-103">Добавление ограничения выражения к модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="ed39c-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ed39c-104">Ниже описан порядок добавления нового выражения ограничения в модель конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="ed39c-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="ed39c-105">Он показывает, как можно предписывать, что защита углов должна применяться к динамику, если пользователь выбрал металлическую переднюю решетку.</span><span class="sxs-lookup"><span data-stu-id="ed39c-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="ed39c-106">Процедура использует компонента динамика класса Hi-End в демонстрационной компании USMF.</span><span class="sxs-lookup"><span data-stu-id="ed39c-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>

## <a name="create-an-expression-constraint"></a><span data-ttu-id="ed39c-107">Создание ограничения выражения</span><span class="sxs-lookup"><span data-stu-id="ed39c-107">Create an expression constraint</span></span>

1. <span data-ttu-id="ed39c-108">Перейдите в раздел **Управление сведениями о продукте \> Продукты \> Модели конфигурации продукта**.</span><span class="sxs-lookup"><span data-stu-id="ed39c-108">Go to **Product information management \> Products \> Product configuration models**.</span></span>
3. <span data-ttu-id="ed39c-109">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ed39c-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ed39c-110">В этом примере используется модель динамика класса Hi-End.</span><span class="sxs-lookup"><span data-stu-id="ed39c-110">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="ed39c-111">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ed39c-111">In the list, select the link in the selected row.</span></span>
5. <span data-ttu-id="ed39c-112">Разверните раздел **Ограничения**.</span><span class="sxs-lookup"><span data-stu-id="ed39c-112">Expand the **Constraints** section.</span></span>
6. <span data-ttu-id="ed39c-113">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="ed39c-113">Select **Add**.</span></span>
7. <span data-ttu-id="ed39c-114">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ed39c-114">Select **Create**.</span></span>
8. <span data-ttu-id="ed39c-115">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ed39c-115">In the **Name** field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="ed39c-116">Ввести выражение</span><span class="sxs-lookup"><span data-stu-id="ed39c-116">Enter expression</span></span>

1. <span data-ttu-id="ed39c-117">Выберите **Изменить выражение**.</span><span class="sxs-lookup"><span data-stu-id="ed39c-117">Select **Edit expression**.</span></span>
    * <span data-ttu-id="ed39c-118">Если вы разблокируете интерфейс в записи задач на этом этапе, можно использовать IntelliSense и список символов для построения выражения ограничения.</span><span class="sxs-lookup"><span data-stu-id="ed39c-118">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="ed39c-119">В поле **ConstraintBody** введите в "Implies[FrontGrill=="Metal", CornerProtection]".</span><span class="sxs-lookup"><span data-stu-id="ed39c-119">In the **ConstraintBody** field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="ed39c-120">Логика этого выражения гласит: если передняя решетка металлическая, должен быть выбран параметр защиты углов.</span><span class="sxs-lookup"><span data-stu-id="ed39c-120">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="ed39c-121">Выберите **Проверить**.</span><span class="sxs-lookup"><span data-stu-id="ed39c-121">Select **Validate**.</span></span>
    * <span data-ttu-id="ed39c-122">Функция проверки выполняется через выражение ограничения и проверяет наличие синтаксических ошибок.</span><span class="sxs-lookup"><span data-stu-id="ed39c-122">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="ed39c-123">Выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="ed39c-123">Select **Close**.</span></span>
5. <span data-ttu-id="ed39c-124">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ed39c-124">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]