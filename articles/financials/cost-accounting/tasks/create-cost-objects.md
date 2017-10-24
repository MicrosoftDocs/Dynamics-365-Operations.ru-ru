--- 
title: "Создание объектов затрат"
description: "Эта процедура показывает порядок создания объектов затрат путем импорта финансовой аналитики центра затрат Dynamics 365 for Finance and Operations, Enterprise edition в модуль учета затрат через соединитель данных."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5d43274aed2edbb91fd4e399cb8d45e91646b055
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="create-cost-objects"></a><span data-ttu-id="37b9e-103">Создание объектов затрат</span><span class="sxs-lookup"><span data-stu-id="37b9e-103">Create cost objects</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37b9e-104">Эта процедура показывает порядок создания объектов затрат путем импорта финансовой аналитики центра затрат Dynamics 365 for Finance and Operations, Enterprise edition в модуль учета затрат через соединитель данных.</span><span class="sxs-lookup"><span data-stu-id="37b9e-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="37b9e-105">В качестве демонстрационной компании для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="37b9e-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="37b9e-106">Эта процедура предназначена для функции "Учет затрат", которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="37b9e-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="37b9e-107">Создание новых объектов затрат</span><span class="sxs-lookup"><span data-stu-id="37b9e-107">Create new cost objects</span></span>
1. <span data-ttu-id="37b9e-108">Перейдите в раздел "Учет затрат" > "Аналитики" > "Аналитики объекта затрат".</span><span class="sxs-lookup"><span data-stu-id="37b9e-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="37b9e-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="37b9e-109">Click New.</span></span>
3. <span data-ttu-id="37b9e-110">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="37b9e-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="37b9e-111">В поле "Соединитель данных для элементов аналитик" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="37b9e-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="37b9e-112">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="37b9e-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="37b9e-113">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="37b9e-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="37b9e-114">Настройка соединителя данных</span><span class="sxs-lookup"><span data-stu-id="37b9e-114">Configure the data connector</span></span>
1. <span data-ttu-id="37b9e-115">Щелкните "Настроить поставщика элементов аналитики".</span><span class="sxs-lookup"><span data-stu-id="37b9e-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="37b9e-116">Выберите CostCenter для импорта аналитики CostCenter в модуль учета затрат.</span><span class="sxs-lookup"><span data-stu-id="37b9e-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="37b9e-117">В поле "Имя аналитики" выберите "Центр затрат".</span><span class="sxs-lookup"><span data-stu-id="37b9e-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="37b9e-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="37b9e-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="37b9e-119">Импорт центров затрат</span><span class="sxs-lookup"><span data-stu-id="37b9e-119">Import cost centers</span></span>
1. <span data-ttu-id="37b9e-120">Щелкните "Импорт элементов аналитики".</span><span class="sxs-lookup"><span data-stu-id="37b9e-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="37b9e-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="37b9e-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="37b9e-122">Просмотр импортированных центров затрат</span><span class="sxs-lookup"><span data-stu-id="37b9e-122">View the imported cost centers</span></span>
1. <span data-ttu-id="37b9e-123">Щелкните "Просмотр элементов аналитики".</span><span class="sxs-lookup"><span data-stu-id="37b9e-123">Click View dimension members.</span></span>


