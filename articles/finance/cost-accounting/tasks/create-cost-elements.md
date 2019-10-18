---
title: Создание элементов затрат
description: Существует несколько способов создания элементов затрат в модуле учета затрат.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cceec1d52e1b5b2a05525c8d96f46dece17363b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187805"
---
# <a name="create-cost-elements"></a><span data-ttu-id="a639f-103">Создание элементов затрат</span><span class="sxs-lookup"><span data-stu-id="a639f-103">Create cost elements</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a639f-104">Существует несколько способов создания элементов затрат в модуле учета затрат.</span><span class="sxs-lookup"><span data-stu-id="a639f-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="a639f-105">Эта процедура показывает порядок создания элементов издержек путем импорта счетов ГК через соединитель данных.</span><span class="sxs-lookup"><span data-stu-id="a639f-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="a639f-106">В качестве демонстрационной компании для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="a639f-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="a639f-107">Эта процедура для функции учета затрат, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="a639f-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="a639f-108">Создание новых элементов затрат</span><span class="sxs-lookup"><span data-stu-id="a639f-108">Create new cost elements</span></span>
1. <span data-ttu-id="a639f-109">Перейдите в раздел "Учет затрат" > "Аналитики" > "Аналитики элемента затрат".</span><span class="sxs-lookup"><span data-stu-id="a639f-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="a639f-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a639f-110">Click New.</span></span>
3. <span data-ttu-id="a639f-111">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a639f-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a639f-112">В поле "Соединитель данных для элементов аналитик" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a639f-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="a639f-113">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a639f-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="a639f-114">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a639f-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="a639f-115">Настройка соединителя данных</span><span class="sxs-lookup"><span data-stu-id="a639f-115">Configure the data connector</span></span>
1. <span data-ttu-id="a639f-116">Щелкните "Настроить поставщика элементов аналитики".</span><span class="sxs-lookup"><span data-stu-id="a639f-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="a639f-117">В поле "План счетов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a639f-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="a639f-118">Выбрать "Общие", чтобы использовать общий план счетов.</span><span class="sxs-lookup"><span data-stu-id="a639f-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="a639f-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a639f-119">Click New.</span></span>
4. <span data-ttu-id="a639f-120">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="a639f-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a639f-121">Фильтры можно применить к счетам для обеспечения соответствия указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="a639f-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="a639f-122">В поле "Со счета ГК" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a639f-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="a639f-123">В поле "На счет ГК" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a639f-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="a639f-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a639f-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="a639f-125">Импортировать счета ГК</span><span class="sxs-lookup"><span data-stu-id="a639f-125">Import main accounts</span></span>
1. <span data-ttu-id="a639f-126">Щелкните "Импорт элементов аналитики".</span><span class="sxs-lookup"><span data-stu-id="a639f-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="a639f-127">Счета ГК будут импортированы в модуль учета затрат и будут использоваться как элементы издержек.</span><span class="sxs-lookup"><span data-stu-id="a639f-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="a639f-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a639f-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="a639f-129">Просмотр импортированных счетов как элементов затрат</span><span class="sxs-lookup"><span data-stu-id="a639f-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="a639f-130">Щелкните "Просмотр элементов аналитики".</span><span class="sxs-lookup"><span data-stu-id="a639f-130">Click View dimension members.</span></span>
    * <span data-ttu-id="a639f-131">Просмотрите импортированные счета ГК как элементы издержек в компании, в которую могут поступать затраты.</span><span class="sxs-lookup"><span data-stu-id="a639f-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  

