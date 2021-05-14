---
title: Создание конфигураций на основе аналитик
description: В этой процедуре показано, как определить конфигурацию для продукта на основе аналитик.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 584bb558ee0afeaffaeb003e9f1d1b0bca42d19d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920689"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="5344d-103">Создание конфигураций на основе аналитик</span><span class="sxs-lookup"><span data-stu-id="5344d-103">Create dimension-based configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5344d-104">В этой процедуре показано, как определить конфигурацию для продукта на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="5344d-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="5344d-105">Это последняя процедура в этой серии, в которой поясняется, как строить сочетания для конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="5344d-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="5344d-106">Выполнение этой процедуры зависит от данных, созданных в ходе предыдущих семи записей.</span><span class="sxs-lookup"><span data-stu-id="5344d-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="5344d-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="5344d-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="5344d-108">Поиск шаблона продукта на основе аналитик</span><span class="sxs-lookup"><span data-stu-id="5344d-108">Find the dimension-based product master</span></span>

1. <span data-ttu-id="5344d-109">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="5344d-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="5344d-110">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5344d-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5344d-111">Выберите шаблон продукта на основе аналитик, созданный в первой записи в этой последовательности из 8 записей.</span><span class="sxs-lookup"><span data-stu-id="5344d-111">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="5344d-112">Создание конфигураций</span><span class="sxs-lookup"><span data-stu-id="5344d-112">Create configurations</span></span>

1. <span data-ttu-id="5344d-113">На панели действий **Разработка** выберите **Ведение конфигураций**.</span><span class="sxs-lookup"><span data-stu-id="5344d-113">On the **Engineering** Action Pane, select **Maintain configurations**.</span></span>
1. <span data-ttu-id="5344d-114">Выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="5344d-114">Select **Configure**.</span></span>
1. <span data-ttu-id="5344d-115">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5344d-115">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5344d-116">В поле **Код номенклатуры** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="5344d-116">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="5344d-117">Выберите любые номенклатуры в первой конфигурационной группе.</span><span class="sxs-lookup"><span data-stu-id="5344d-117">Select any of the items in the first configuration group.</span></span>  
1. <span data-ttu-id="5344d-118">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="5344d-118">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="5344d-119">В поле **Код номенклатуры** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="5344d-119">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="5344d-120">Выберите любую номенклатуру из второй конфигурационной группы.</span><span class="sxs-lookup"><span data-stu-id="5344d-120">Select any item from the second configuration group.</span></span>  
1. <span data-ttu-id="5344d-121">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5344d-121">Select **OK**.</span></span>
1. <span data-ttu-id="5344d-122">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5344d-122">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5344d-123">В поле **Конфигурация** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5344d-123">In the **Configuration** field, type a value.</span></span>
    * <span data-ttu-id="5344d-124">Введите имя конфигурации, с помощью которого проще идентифицировать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="5344d-124">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
1. <span data-ttu-id="5344d-125">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5344d-125">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="5344d-126">Введите описание конфигурации, чтобы объяснить ее содержимое.</span><span class="sxs-lookup"><span data-stu-id="5344d-126">Enter a description of the configuration to explain what it contains.</span></span>  
1. <span data-ttu-id="5344d-127">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5344d-127">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]