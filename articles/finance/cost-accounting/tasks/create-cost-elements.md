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
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 87f93fd7c1c42045274d6b89847b27e93614d9a4
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976147"
---
# <a name="create-cost-elements"></a><span data-ttu-id="d78fd-103">Создание элементов затрат</span><span class="sxs-lookup"><span data-stu-id="d78fd-103">Create cost elements</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d78fd-104">Существует несколько способов создания элементов затрат в модуле учета затрат.</span><span class="sxs-lookup"><span data-stu-id="d78fd-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="d78fd-105">Эта процедура показывает порядок создания элементов издержек путем импорта счетов ГК через соединитель данных.</span><span class="sxs-lookup"><span data-stu-id="d78fd-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="d78fd-106">В качестве демонстрационной компании для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="d78fd-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="d78fd-107">Эта процедура для функции учета затрат, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="d78fd-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="d78fd-108">Создание новых элементов затрат</span><span class="sxs-lookup"><span data-stu-id="d78fd-108">Create new cost elements</span></span>
1. <span data-ttu-id="d78fd-109">Перейдите в раздел "Учет затрат" > "Аналитики" > "Аналитики элемента затрат".</span><span class="sxs-lookup"><span data-stu-id="d78fd-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="d78fd-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d78fd-110">Click New.</span></span>
3. <span data-ttu-id="d78fd-111">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d78fd-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d78fd-112">В поле "Соединитель данных для элементов аналитик" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d78fd-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="d78fd-113">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d78fd-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="d78fd-114">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d78fd-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="d78fd-115">Настройка соединителя данных</span><span class="sxs-lookup"><span data-stu-id="d78fd-115">Configure the data connector</span></span>
1. <span data-ttu-id="d78fd-116">Щелкните "Настроить поставщика элементов аналитики".</span><span class="sxs-lookup"><span data-stu-id="d78fd-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="d78fd-117">В поле "План счетов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d78fd-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="d78fd-118">Выбрать "Общие", чтобы использовать общий план счетов.</span><span class="sxs-lookup"><span data-stu-id="d78fd-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="d78fd-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d78fd-119">Click New.</span></span>
4. <span data-ttu-id="d78fd-120">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="d78fd-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d78fd-121">Фильтры можно применить к счетам для обеспечения соответствия указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="d78fd-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="d78fd-122">В поле "Со счета ГК" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d78fd-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="d78fd-123">В поле "На счет ГК" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d78fd-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="d78fd-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d78fd-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="d78fd-125">Импортировать счета ГК</span><span class="sxs-lookup"><span data-stu-id="d78fd-125">Import main accounts</span></span>
1. <span data-ttu-id="d78fd-126">Щелкните "Импорт элементов аналитики".</span><span class="sxs-lookup"><span data-stu-id="d78fd-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="d78fd-127">Счета ГК будут импортированы в модуль учета затрат и будут использоваться как элементы издержек.</span><span class="sxs-lookup"><span data-stu-id="d78fd-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="d78fd-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d78fd-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="d78fd-129">Просмотр импортированных счетов как элементов затрат</span><span class="sxs-lookup"><span data-stu-id="d78fd-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="d78fd-130">Щелкните "Просмотр элементов аналитики".</span><span class="sxs-lookup"><span data-stu-id="d78fd-130">Click View dimension members.</span></span>
    * <span data-ttu-id="d78fd-131">Просмотрите импортированные счета ГК как элементы издержек в компании, в которую могут поступать затраты.</span><span class="sxs-lookup"><span data-stu-id="d78fd-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  

