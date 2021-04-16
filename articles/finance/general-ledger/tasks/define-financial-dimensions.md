---
title: Определение финансовых аналитик
description: В этом руководстве показано добавление финансовой аналитики на основе объекта и пользовательской финансовой аналитики.
author: aprilolson
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c93a67d0c4a8443eaf40b094770ed6ce29da527b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834460"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="3b5d8-103">Определение финансовых аналитик</span><span class="sxs-lookup"><span data-stu-id="3b5d8-103">Define financial dimensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3b5d8-104">В этом руководстве показано добавление финансовой аналитики на основе объекта и пользовательской финансовой аналитики.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="3b5d8-105">В данном руководстве используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="3b5d8-106">Создание финансовой аналитики с основой на объекте</span><span class="sxs-lookup"><span data-stu-id="3b5d8-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="3b5d8-107">Перейдите в раздел **Область переходов > Модули > Главная книга > План счетов > Аналитики > Финансовые аналитики**.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Dimensions > Financial dimensions**.</span></span>
2. <span data-ttu-id="3b5d8-108">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-108">Click **New**.</span></span>
3. <span data-ttu-id="3b5d8-109">В поле формы **Значения пользователя** выберите определенный системой объект, на котором будет основана финансовая аналитика.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-109">In the **User values form** field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="3b5d8-110">В поле **Наименование аналитики** введите значение для описания финансовой аналитики.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-110">In the **Dimension name** field, type a value to describe the financial dimension.</span></span> <span data-ttu-id="3b5d8-111">Имя может отличаться от заданного системой объекта, но не может содержать пробелы или специальные символы.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>
5. <span data-ttu-id="3b5d8-112">Нажмите кнопку **Активировать**.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-112">Click **Activate**.</span></span> <span data-ttu-id="3b5d8-113">При активации финансовой аналитики обновляется таблица с именем финансовой аналитики и удаляются удаленные аналитики.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="3b5d8-114">Можно ввести значения аналитики перед активацией финансовой аналитики, но финансовую аналитику нельзя использовать, пока она не активирована.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="3b5d8-115">Нажмите **Закрыть** в сообщении активации.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-115">Click **Close** on the activation message.</span></span>
7. <span data-ttu-id="3b5d8-116">Нажмите кнопку **Активировать**.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-116">Click **Activate**.</span></span> <span data-ttu-id="3b5d8-117">Активацию аналитики можно запланировать для пакетного выполнения в определенные дату и время.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="3b5d8-118">В области **Панель операций** щелкните **Значения аналитик**.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-118">On **Action pane**, click **Dimension values**.</span></span> <span data-ttu-id="3b5d8-119">Некоторые значения аналитики учитывают специфику компании.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-119">Some dimension values are company specific.</span></span> <span data-ttu-id="3b5d8-120">Можно проверить, учитывают ли они специфику компании, если название компании отображается в списке значений аналитики.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="3b5d8-121">Создание пользовательской финансовой аналитики</span><span class="sxs-lookup"><span data-stu-id="3b5d8-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="3b5d8-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-122">Close the page.</span></span>
2. <span data-ttu-id="3b5d8-123">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-123">Click **New**.</span></span>
3. <span data-ttu-id="3b5d8-124">В поле **Использовать значения из** выберите **Настраиваемая аналитика**.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-124">In the **Use values from** field, select **Custom dimension**.</span></span>
4. <span data-ttu-id="3b5d8-125">В поле **Наименование аналитики** введите значение для описания финансовой аналитики.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-125">In the **Dimension name** field, type a value to describe the financial dimension.</span></span>
    - <span data-ttu-id="3b5d8-126">Имя не может содержать пробелы и специальные символы.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-126">The name cannot contain spaces or special characters.</span></span>  
    - <span data-ttu-id="3b5d8-127">Можно также указать маску формата для ограничения объема и типа сведений, которые можно указать для значений аналитик.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    - <span data-ttu-id="3b5d8-128">Можно ввести символы, которые останутся одинаковыми для каждого значения аналитики, такие как буквы или дефис.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="3b5d8-129">Можно также ввести знак номера (#) и амперсанда (&) как местозаполнители для букв и цифр, которые изменятся каждый раз при создании значения аналитики.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="3b5d8-130">Используйте знак решетки (#) как заполнитель для номера и амперсанд (&) как заполнитель для букв.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="3b5d8-131">Пример: чтобы ограничить значение аналитики до букв CC, дефиса и трех цифр, введите CC-### как маску формата.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="3b5d8-132">Нажмите кнопку **Активировать**.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-132">Click **Activate**.</span></span> <span data-ttu-id="3b5d8-133">При активации финансовой аналитики обновляется таблица с именем финансовой аналитики и удаляются удаленные аналитики.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="3b5d8-134">Можно ввести значения аналитики перед активацией финансовой аналитики, но финансовую аналитику нельзя использовать, пока она не активирована.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>     
6. <span data-ttu-id="3b5d8-135">Нажмите кнопку **Активировать**.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-135">Click **Activate**.</span></span> <span data-ttu-id="3b5d8-136">Активацию аналитики можно запланировать для пакетного выполнения в определенные дату и время.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>      
7. <span data-ttu-id="3b5d8-137">В области **Панель операций** щелкните **Значения аналитик**.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-137">On **Action pane**, click **Dimension values**.</span></span>
8. <span data-ttu-id="3b5d8-138">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-138">Click **New**.</span></span>
9. <span data-ttu-id="3b5d8-139">В поле **Значение аналитики** введите наименование для своего значения финансовой аналитики.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-139">In the **Dimension value** field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="3b5d8-140">В поле **Описание** введите описание, которое описывает значение финансовой аналитики.</span><span class="sxs-lookup"><span data-stu-id="3b5d8-140">In the **Description** field, type a description that describes your financial dimension value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]