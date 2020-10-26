---
title: Создание конфигураций на основе аналитик
description: В этой процедуре показано, как определить конфигурацию для продукта на основе аналитик.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c3e5cd2677480b14739f963cf4a74efaa7f2bd2a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986247"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="9350b-103">Создание конфигураций на основе аналитик</span><span class="sxs-lookup"><span data-stu-id="9350b-103">Create dimension-based configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9350b-104">В этой процедуре показано, как определить конфигурацию для продукта на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="9350b-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="9350b-105">Это последняя процедура в этой серии, в которой поясняется, как строить сочетания для конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="9350b-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="9350b-106">Выполнение этой процедуры зависит от данных, созданных в ходе предыдущих семи записей.</span><span class="sxs-lookup"><span data-stu-id="9350b-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="9350b-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="9350b-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="9350b-108">Поиск шаблона продукта на основе аналитик</span><span class="sxs-lookup"><span data-stu-id="9350b-108">Find the dimension-based product master</span></span>
1. <span data-ttu-id="9350b-109">Щелкните "Обслуживание выпущенного продукта".</span><span class="sxs-lookup"><span data-stu-id="9350b-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="9350b-110">Щелкните "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="9350b-110">Click Released products.</span></span>
3. <span data-ttu-id="9350b-111">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9350b-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9350b-112">Выберите шаблон продукта на основе аналитик, созданный в первой записи в этой последовательности из 8 записей.</span><span class="sxs-lookup"><span data-stu-id="9350b-112">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="9350b-113">Создание конфигураций</span><span class="sxs-lookup"><span data-stu-id="9350b-113">Create configurations</span></span>
1. <span data-ttu-id="9350b-114">На панели действий "Инжиниринг" щелкните "Ведение конфигураций".</span><span class="sxs-lookup"><span data-stu-id="9350b-114">On the Engineering Action Pane, click Maintain configurations.</span></span>
2. <span data-ttu-id="9350b-115">Щелкните Настроить.</span><span class="sxs-lookup"><span data-stu-id="9350b-115">Click Configure.</span></span>
3. <span data-ttu-id="9350b-116">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9350b-116">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="9350b-117">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9350b-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="9350b-118">Выберите любые номенклатуры в первой конфигурационной группе.</span><span class="sxs-lookup"><span data-stu-id="9350b-118">Select any of the items in the first configuration group.</span></span>  
5. <span data-ttu-id="9350b-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="9350b-119">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="9350b-120">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9350b-120">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="9350b-121">Выберите любую номенклатуру из второй конфигурационной группы.</span><span class="sxs-lookup"><span data-stu-id="9350b-121">Select any item from the second configuration group.</span></span>  
7. <span data-ttu-id="9350b-122">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9350b-122">Click OK.</span></span>
8. <span data-ttu-id="9350b-123">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9350b-123">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="9350b-124">В поле "Конфигурация" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9350b-124">In the Configuration field, type a value.</span></span>
    * <span data-ttu-id="9350b-125">Введите имя конфигурации, с помощью которого проще идентифицировать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="9350b-125">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
10. <span data-ttu-id="9350b-126">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9350b-126">In the Description field, type a value.</span></span>
    * <span data-ttu-id="9350b-127">Введите описание конфигурации, чтобы объяснить ее содержимое.</span><span class="sxs-lookup"><span data-stu-id="9350b-127">Enter a description of the configuration to explain what it contains.</span></span>  
11. <span data-ttu-id="9350b-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9350b-128">Click OK.</span></span>

