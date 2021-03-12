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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3d2ef7d6549bdeb3ba2afd2a594f36b47c912db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990775"
---
# <a name="create-cost-objects"></a><span data-ttu-id="78695-103">Создание объектов затрат</span><span class="sxs-lookup"><span data-stu-id="78695-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78695-104">Эта процедура демонстрирует порядок создания объектов затрат путем импорта финансовой аналитики центра затрат в модуль учета затрат через соединитель данных.</span><span class="sxs-lookup"><span data-stu-id="78695-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="78695-105">В качестве демонстрационной компании для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="78695-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="78695-106">Создание новых объектов затрат</span><span class="sxs-lookup"><span data-stu-id="78695-106">Create new cost objects</span></span>
1. <span data-ttu-id="78695-107">Перейдите в раздел "Учет затрат" > "Аналитики" > "Аналитики объекта затрат".</span><span class="sxs-lookup"><span data-stu-id="78695-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="78695-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="78695-108">Click New.</span></span>
3. <span data-ttu-id="78695-109">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="78695-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="78695-110">В поле "Соединитель данных для элементов аналитик" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="78695-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="78695-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="78695-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="78695-112">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="78695-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="78695-113">Настройка соединителя данных</span><span class="sxs-lookup"><span data-stu-id="78695-113">Configure the data connector</span></span>
1. <span data-ttu-id="78695-114">Щелкните "Настроить поставщика элементов аналитики".</span><span class="sxs-lookup"><span data-stu-id="78695-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="78695-115">Выберите CostCenter для импорта аналитики CostCenter в модуль учета затрат.</span><span class="sxs-lookup"><span data-stu-id="78695-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="78695-116">В поле "Имя аналитики" выберите "Центр затрат".</span><span class="sxs-lookup"><span data-stu-id="78695-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="78695-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="78695-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="78695-118">Импорт центров затрат</span><span class="sxs-lookup"><span data-stu-id="78695-118">Import cost centers</span></span>
1. <span data-ttu-id="78695-119">Щелкните "Импорт элементов аналитики".</span><span class="sxs-lookup"><span data-stu-id="78695-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="78695-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="78695-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="78695-121">Просмотр импортированных центров затрат</span><span class="sxs-lookup"><span data-stu-id="78695-121">View the imported cost centers</span></span>
1. <span data-ttu-id="78695-122">Щелкните "Просмотр элементов аналитики".</span><span class="sxs-lookup"><span data-stu-id="78695-122">Click View dimension members.</span></span>

