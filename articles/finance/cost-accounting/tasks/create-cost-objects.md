---
title: Создание объектов затрат
description: Эта процедура демонстрирует порядок создания объектов затрат путем импорта финансовой аналитики центра затрат в модуль учета затрат через соединитель данных.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55f5f6e5048f70e744cb3dc82a2a279aae69b4af
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447337"
---
# <a name="create-cost-objects"></a><span data-ttu-id="c1696-103">Создание объектов затрат</span><span class="sxs-lookup"><span data-stu-id="c1696-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1696-104">Эта процедура демонстрирует порядок создания объектов затрат путем импорта финансовой аналитики центра затрат в модуль учета затрат через соединитель данных.</span><span class="sxs-lookup"><span data-stu-id="c1696-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="c1696-105">В качестве демонстрационной компании для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="c1696-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="c1696-106">Создание новых объектов затрат</span><span class="sxs-lookup"><span data-stu-id="c1696-106">Create new cost objects</span></span>
1. <span data-ttu-id="c1696-107">Перейдите в раздел "Учет затрат" > "Аналитики" > "Аналитики объекта затрат".</span><span class="sxs-lookup"><span data-stu-id="c1696-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="c1696-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c1696-108">Click New.</span></span>
3. <span data-ttu-id="c1696-109">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c1696-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c1696-110">В поле "Соединитель данных для элементов аналитик" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c1696-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="c1696-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c1696-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="c1696-112">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="c1696-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="c1696-113">Настройка соединителя данных</span><span class="sxs-lookup"><span data-stu-id="c1696-113">Configure the data connector</span></span>
1. <span data-ttu-id="c1696-114">Щелкните "Настроить поставщика элементов аналитики".</span><span class="sxs-lookup"><span data-stu-id="c1696-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="c1696-115">Выберите CostCenter для импорта аналитики CostCenter в модуль учета затрат.</span><span class="sxs-lookup"><span data-stu-id="c1696-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="c1696-116">В поле "Имя аналитики" выберите "Центр затрат".</span><span class="sxs-lookup"><span data-stu-id="c1696-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="c1696-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c1696-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="c1696-118">Импорт центров затрат</span><span class="sxs-lookup"><span data-stu-id="c1696-118">Import cost centers</span></span>
1. <span data-ttu-id="c1696-119">Щелкните "Импорт элементов аналитики".</span><span class="sxs-lookup"><span data-stu-id="c1696-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="c1696-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c1696-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="c1696-121">Просмотр импортированных центров затрат</span><span class="sxs-lookup"><span data-stu-id="c1696-121">View the imported cost centers</span></span>
1. <span data-ttu-id="c1696-122">Щелкните "Просмотр элементов аналитики".</span><span class="sxs-lookup"><span data-stu-id="c1696-122">Click View dimension members.</span></span>

