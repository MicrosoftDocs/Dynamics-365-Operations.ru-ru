--- 
title: "Определение финансовых аналитик"
description: "В этом руководстве показано добавление финансовой аналитики на основе объекта и пользовательской финансовой аналитики."
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: f2f3ed15af0b10e102a1c94e2efc6a63ab460e83
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="define-financial-dimensions"></a><span data-ttu-id="f5eaa-103">Определение финансовых аналитик</span><span class="sxs-lookup"><span data-stu-id="f5eaa-103">Define financial dimensions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5eaa-104">В этом руководстве показано добавление финансовой аналитики на основе объекта и пользовательской финансовой аналитики.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="f5eaa-105">В данном руководстве используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="f5eaa-106">Создание финансовой аналитики с основой на объекте</span><span class="sxs-lookup"><span data-stu-id="f5eaa-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="f5eaa-107">Перейдите в раздел "Главная книга" > "План счетов" > "Аналитики" > "Финансовые аналитики".</span><span class="sxs-lookup"><span data-stu-id="f5eaa-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="f5eaa-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f5eaa-108">Click New.</span></span>
3. <span data-ttu-id="f5eaa-109">В поле "Значения пользователя" выберите определенный системой объект, на котором будет основана финансовая аналитика.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-109">In the User values from field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="f5eaa-110">В поле "Наименование аналитики" введите значение для описания финансовой аналитики.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-110">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="f5eaa-111">Имя может отличаться от заданного системой объекта, но не может содержать пробелы или специальные символы.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>  
5. <span data-ttu-id="f5eaa-112">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-112">Click Activate.</span></span>
    * <span data-ttu-id="f5eaa-113">При активации финансовой аналитики обновляется таблица с именем финансовой аналитики и удаляются удаленные аналитики.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="f5eaa-114">Можно ввести значения аналитики перед активацией финансовой аналитики, но финансовую аналитику нельзя использовать, пока она не активирована.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="f5eaa-115">Нажмите "Закрыть" в сообщении активации.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-115">Click Close on the activation message.</span></span>
7. <span data-ttu-id="f5eaa-116">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-116">Click Activate.</span></span>
    * <span data-ttu-id="f5eaa-117">Активацию аналитики можно запланировать для пакетного выполнения в определенные дату и время.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="f5eaa-118">Щелкните "Значения аналитик".</span><span class="sxs-lookup"><span data-stu-id="f5eaa-118">Click Dimension values.</span></span>
    * <span data-ttu-id="f5eaa-119">Некоторые значения аналитики учитывают специфику компании.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-119">Some dimension values are company specific.</span></span> <span data-ttu-id="f5eaa-120">Можно проверить, учитывают ли они специфику компании, если название компании отображается в списке значений аналитики.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="f5eaa-121">Создание пользовательской финансовой аналитики</span><span class="sxs-lookup"><span data-stu-id="f5eaa-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="f5eaa-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-122">Close the page.</span></span>
2. <span data-ttu-id="f5eaa-123">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f5eaa-123">Click New.</span></span>
3. <span data-ttu-id="f5eaa-124">В поле "Использовать значения из" выберите <Custom dimension>.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-124">In the Use values from field, select <Custom dimension>.</span></span>
4. <span data-ttu-id="f5eaa-125">В поле "Наименование аналитики" введите значение для описания финансовой аналитики.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-125">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="f5eaa-126">Имя не может содержать пробелы и специальные символы.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-126">The name cannot contain spaces or special characters.</span></span>  
    * <span data-ttu-id="f5eaa-127">Можно также указать маску формата для ограничения объема и типа сведений, которые можно указать для значений аналитик.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    * <span data-ttu-id="f5eaa-128">Можно ввести символы, которые останутся одинаковыми для каждого значения аналитики, такие как буквы или дефис.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="f5eaa-129">Можно также ввести знак номера (#) и амперсанда (&) как местозаполнители для букв и цифр, которые изменятся каждый раз при создании значения аналитики.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="f5eaa-130">Используйте знак решетки (#) как заполнитель для номера и амперсанд (&) как заполнитель для букв.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="f5eaa-131">Пример: чтобы ограничить значение аналитики до букв CC, дефиса и трех цифр, введите CC-### как маску формата.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="f5eaa-132">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-132">Click Activate.</span></span>
    * <span data-ttu-id="f5eaa-133">При активации финансовой аналитики обновляется таблица с именем финансовой аналитики и удаляются удаленные аналитики.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="f5eaa-134">Можно ввести значения аналитики перед активацией финансовой аналитики, но финансовую аналитику нельзя использовать, пока она не активирована.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="f5eaa-135">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-135">Click Activate.</span></span>
    * <span data-ttu-id="f5eaa-136">Активацию аналитики можно запланировать для пакетного выполнения в определенные дату и время.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
7. <span data-ttu-id="f5eaa-137">Щелкните "Значения аналитик".</span><span class="sxs-lookup"><span data-stu-id="f5eaa-137">Click Dimension values.</span></span>
8. <span data-ttu-id="f5eaa-138">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f5eaa-138">Click New.</span></span>
9. <span data-ttu-id="f5eaa-139">В поле "Значение аналитики" введите наименование для своего значения финансовой аналитики.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-139">In the Dimension value field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="f5eaa-140">В поле "Описание" введите описание, которое описывает значение финансовой аналитики.</span><span class="sxs-lookup"><span data-stu-id="f5eaa-140">In the Description field, type a description that describes your financial dimension value.</span></span>


