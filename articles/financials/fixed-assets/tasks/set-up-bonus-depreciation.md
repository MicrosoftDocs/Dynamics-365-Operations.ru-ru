--- 
title: "Настройка амортизационной премии"
description: "В этой процедуре показано, как создать амортизационную премию и связать ее с моделью стоимости ОС."
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7e6ebb13084626b477b6e0b24acdc09e2c0d3d6d
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="43fd6-103">Настройка амортизационной премии</span><span class="sxs-lookup"><span data-stu-id="43fd6-103">Set up bonus depreciation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43fd6-104">В этой процедуре показано, как создать амортизационную премию и связать ее с моделью стоимости ОС.</span><span class="sxs-lookup"><span data-stu-id="43fd6-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="43fd6-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="43fd6-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="43fd6-106">Создание амортизационной премии</span><span class="sxs-lookup"><span data-stu-id="43fd6-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="43fd6-107">Перейдите в раздел "Основные средства" > "Настройка" > "Амортизационная премия".</span><span class="sxs-lookup"><span data-stu-id="43fd6-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="43fd6-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="43fd6-108">Click New.</span></span>
3. <span data-ttu-id="43fd6-109">В поле "Амортизационная премия" введите значение.</span><span class="sxs-lookup"><span data-stu-id="43fd6-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="43fd6-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="43fd6-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="43fd6-111">В поле "Процент" введите число.</span><span class="sxs-lookup"><span data-stu-id="43fd6-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="43fd6-112">Если процент не указан, настройте сумму.</span><span class="sxs-lookup"><span data-stu-id="43fd6-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="43fd6-113">Связь амортизационной премии с журналом группы основных средств</span><span class="sxs-lookup"><span data-stu-id="43fd6-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="43fd6-114">Перейдите в раздел "Основные средства" > "Настройка" > "Группы ОС".</span><span class="sxs-lookup"><span data-stu-id="43fd6-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="43fd6-115">В списке выберите группу основных средств, связанную с амортизационной премией.</span><span class="sxs-lookup"><span data-stu-id="43fd6-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="43fd6-116">Нажмите "Книги".</span><span class="sxs-lookup"><span data-stu-id="43fd6-116">Click Books.</span></span>
4. <span data-ttu-id="43fd6-117">В списке выберите книгу, связанную с амортизационной премией.</span><span class="sxs-lookup"><span data-stu-id="43fd6-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="43fd6-118">Щелкните "Амортизационная премия".</span><span class="sxs-lookup"><span data-stu-id="43fd6-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="43fd6-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="43fd6-119">Click New.</span></span>
7. <span data-ttu-id="43fd6-120">В поле "Амортизационная премия" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="43fd6-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="43fd6-121">Значения по умолчанию "Процент" и "Сумма" берутся из настройки амортизационной премии.</span><span class="sxs-lookup"><span data-stu-id="43fd6-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="43fd6-122">В поле "Приоритет" введите число.</span><span class="sxs-lookup"><span data-stu-id="43fd6-122">In the Priority field, enter a number.</span></span>


