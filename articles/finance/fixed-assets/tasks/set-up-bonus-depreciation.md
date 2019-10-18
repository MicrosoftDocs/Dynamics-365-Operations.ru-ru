---
title: Настройка амортизационной премии
description: В этой процедуре показано, как создать амортизационную премию и связать ее с моделью стоимости ОС.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 788cddf4d822fe3d3d6a33e83d7b30f32f4b6b9c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179563"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="8422f-103">Настройка амортизационной премии</span><span class="sxs-lookup"><span data-stu-id="8422f-103">Set up bonus depreciation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8422f-104">В этой процедуре показано, как создать амортизационную премию и связать ее с моделью стоимости ОС.</span><span class="sxs-lookup"><span data-stu-id="8422f-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="8422f-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="8422f-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="8422f-106">Создание амортизационной премии</span><span class="sxs-lookup"><span data-stu-id="8422f-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="8422f-107">Перейдите в раздел "Основные средства" > "Настройка" > "Амортизационная премия".</span><span class="sxs-lookup"><span data-stu-id="8422f-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="8422f-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8422f-108">Click New.</span></span>
3. <span data-ttu-id="8422f-109">В поле "Амортизационная премия" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8422f-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="8422f-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8422f-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8422f-111">В поле "Процент" введите число.</span><span class="sxs-lookup"><span data-stu-id="8422f-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="8422f-112">Если процент не указан, настройте сумму.</span><span class="sxs-lookup"><span data-stu-id="8422f-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="8422f-113">Связь амортизационной премии с журналом группы основных средств</span><span class="sxs-lookup"><span data-stu-id="8422f-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="8422f-114">Перейдите в раздел "Основные средства" > "Настройка" > "Группы ОС".</span><span class="sxs-lookup"><span data-stu-id="8422f-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="8422f-115">В списке выберите группу основных средств, связанную с амортизационной премией.</span><span class="sxs-lookup"><span data-stu-id="8422f-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="8422f-116">Нажмите "Книги".</span><span class="sxs-lookup"><span data-stu-id="8422f-116">Click Books.</span></span>
4. <span data-ttu-id="8422f-117">В списке выберите книгу, связанную с амортизационной премией.</span><span class="sxs-lookup"><span data-stu-id="8422f-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="8422f-118">Щелкните "Амортизационная премия".</span><span class="sxs-lookup"><span data-stu-id="8422f-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="8422f-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8422f-119">Click New.</span></span>
7. <span data-ttu-id="8422f-120">В поле "Амортизационная премия" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8422f-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="8422f-121">Значения по умолчанию "Процент" и "Сумма" берутся из настройки амортизационной премии.</span><span class="sxs-lookup"><span data-stu-id="8422f-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="8422f-122">В поле "Приоритет" введите число.</span><span class="sxs-lookup"><span data-stu-id="8422f-122">In the Priority field, enter a number.</span></span>

