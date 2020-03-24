---
title: Настройка самообслуживания сотрудников
description: В Microsoft Dynamics 365 Human Resources можно настроить плитки для переходов верхнего уровня в модуле дистанционного обслуживания сотрудников.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17918fc7b894929c92c54b59b7440ab8aef980bd
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092668"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="24ced-103">Настройка самообслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="24ced-103">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="24ced-104">В Microsoft Dynamics 365 Human Resources можно настроить плитки для переходов верхнего уровня в модуле дистанционного обслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="24ced-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="24ced-105">Плитки плана льгот направляют пользователей в планы льгот, для которых они могут быть зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="24ced-105">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="24ced-106">Настройка плитки ролевого центра</span><span class="sxs-lookup"><span data-stu-id="24ced-106">Set up a role center tile</span></span>

1. <span data-ttu-id="24ced-107">В рабочей области **Управление льготами** в **Настройка** выберите **Параметры дистанционного обслуживания сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="24ced-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="24ced-108">Выберите вкладку **Настройка плитки ролевого центра**, а затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="24ced-108">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="24ced-109">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="24ced-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="24ced-110">Поле</span><span class="sxs-lookup"><span data-stu-id="24ced-110">Field</span></span> | <span data-ttu-id="24ced-111">Описание</span><span class="sxs-lookup"><span data-stu-id="24ced-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="24ced-112">Идентификатор плитки</span><span class="sxs-lookup"><span data-stu-id="24ced-112">Tile ID</span></span> | <span data-ttu-id="24ced-113">Уникальный идентификатор для плитки.</span><span class="sxs-lookup"><span data-stu-id="24ced-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="24ced-114">Текст метки плитки</span><span class="sxs-lookup"><span data-stu-id="24ced-114">Tile label text</span></span> | <span data-ttu-id="24ced-115">Текст, который будет отображаться для плитки при дистанционном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="24ced-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="24ced-116">Описание</span><span class="sxs-lookup"><span data-stu-id="24ced-116">Description</span></span> | <span data-ttu-id="24ced-117">Описание плитки.</span><span class="sxs-lookup"><span data-stu-id="24ced-117">A description of the tile.</span></span> |
   | <span data-ttu-id="24ced-118">Веб-адрес</span><span class="sxs-lookup"><span data-stu-id="24ced-118">Internet address</span></span> | <span data-ttu-id="24ced-119">Введите URL-адрес страницы дистанционного обслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="24ced-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="24ced-120">Размер плитки</span><span class="sxs-lookup"><span data-stu-id="24ced-120">Tile size</span></span> | <span data-ttu-id="24ced-121">Размер плитки: маленький, средний или большой.</span><span class="sxs-lookup"><span data-stu-id="24ced-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="24ced-122">Цель</span><span class="sxs-lookup"><span data-stu-id="24ced-122">Target</span></span> | <span data-ttu-id="24ced-123">Указывает, следует ли открывать страницу в новом окне или в текущем окне.</span><span class="sxs-lookup"><span data-stu-id="24ced-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="24ced-124">Фоновое изображение плитки</span><span class="sxs-lookup"><span data-stu-id="24ced-124">Tile background image</span></span> | <span data-ttu-id="24ced-125">URL-адрес изображения, используемого для плитки (необязательно).</span><span class="sxs-lookup"><span data-stu-id="24ced-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="24ced-126">Запустить</span><span class="sxs-lookup"><span data-stu-id="24ced-126">Start</span></span> | <span data-ttu-id="24ced-127">Дата и время начала, когда плитка должна быть доступна.</span><span class="sxs-lookup"><span data-stu-id="24ced-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="24ced-128">Окончание</span><span class="sxs-lookup"><span data-stu-id="24ced-128">End</span></span> | <span data-ttu-id="24ced-129">Дата и время окончания доступности плитки.</span><span class="sxs-lookup"><span data-stu-id="24ced-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="24ced-130">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="24ced-130">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="24ced-131">Настройка плитки планов льгот</span><span class="sxs-lookup"><span data-stu-id="24ced-131">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="24ced-132">В рабочей области **Управление льготами** в **Настройка** выберите **Параметры дистанционного обслуживания сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="24ced-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="24ced-133">Выберите вкладку **Настройка плитки планов льгот**, а затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="24ced-133">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="24ced-134">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="24ced-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="24ced-135">Поле</span><span class="sxs-lookup"><span data-stu-id="24ced-135">Field</span></span> | <span data-ttu-id="24ced-136">Описание</span><span class="sxs-lookup"><span data-stu-id="24ced-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="24ced-137">Идентификатор плитки</span><span class="sxs-lookup"><span data-stu-id="24ced-137">Tile ID</span></span> | <span data-ttu-id="24ced-138">Уникальный идентификатор для плитки.</span><span class="sxs-lookup"><span data-stu-id="24ced-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="24ced-139">Текст метки плитки</span><span class="sxs-lookup"><span data-stu-id="24ced-139">Tile label text</span></span> | <span data-ttu-id="24ced-140">Текст, который будет отображаться для плитки при дистанционном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="24ced-140">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="24ced-141">Описание</span><span class="sxs-lookup"><span data-stu-id="24ced-141">Description</span></span> | <span data-ttu-id="24ced-142">Описание плитки.</span><span class="sxs-lookup"><span data-stu-id="24ced-142">A description of the tile.</span></span> |
   | <span data-ttu-id="24ced-143">Веб-адрес</span><span class="sxs-lookup"><span data-stu-id="24ced-143">Internet address</span></span> | <span data-ttu-id="24ced-144">Введите URL-адрес страницы дистанционного обслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="24ced-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="24ced-145">Размер плитки</span><span class="sxs-lookup"><span data-stu-id="24ced-145">Tile size</span></span> | <span data-ttu-id="24ced-146">Размер плитки: маленький, средний или большой.</span><span class="sxs-lookup"><span data-stu-id="24ced-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="24ced-147">Цель</span><span class="sxs-lookup"><span data-stu-id="24ced-147">Target</span></span> | <span data-ttu-id="24ced-148">Указывает, следует ли открывать страницу в новом окне или в текущем окне.</span><span class="sxs-lookup"><span data-stu-id="24ced-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="24ced-149">Фоновое изображение плитки</span><span class="sxs-lookup"><span data-stu-id="24ced-149">Tile background image</span></span> | <span data-ttu-id="24ced-150">URL-адрес изображения, используемого для плитки (необязательно).</span><span class="sxs-lookup"><span data-stu-id="24ced-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="24ced-151">Запустить</span><span class="sxs-lookup"><span data-stu-id="24ced-151">Start</span></span> | <span data-ttu-id="24ced-152">Дата и время начала, когда плитка должна быть доступна.</span><span class="sxs-lookup"><span data-stu-id="24ced-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="24ced-153">Окончание</span><span class="sxs-lookup"><span data-stu-id="24ced-153">End</span></span> | <span data-ttu-id="24ced-154">Дата и время окончания доступности плитки.</span><span class="sxs-lookup"><span data-stu-id="24ced-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="24ced-155">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="24ced-155">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="24ced-156">Настройка плитки плана гибкого кредита</span><span class="sxs-lookup"><span data-stu-id="24ced-156">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="24ced-157">В рабочей области **Управление льготами** в **Настройка** выберите **Параметры дистанционного обслуживания сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="24ced-157">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="24ced-158">Выберите вкладку **Настройка плитки плана гибкого кредита**, а затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="24ced-158">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="24ced-159">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="24ced-159">Specify values for the following fields:</span></span>

   | <span data-ttu-id="24ced-160">Поле</span><span class="sxs-lookup"><span data-stu-id="24ced-160">Field</span></span> | <span data-ttu-id="24ced-161">Описание</span><span class="sxs-lookup"><span data-stu-id="24ced-161">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="24ced-162">Идентификатор плитки</span><span class="sxs-lookup"><span data-stu-id="24ced-162">Tile ID</span></span> | <span data-ttu-id="24ced-163">Уникальный идентификатор для плитки.</span><span class="sxs-lookup"><span data-stu-id="24ced-163">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="24ced-164">Текст метки плитки</span><span class="sxs-lookup"><span data-stu-id="24ced-164">Tile label text</span></span> | <span data-ttu-id="24ced-165">Текст, который будет отображаться для плитки при дистанционном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="24ced-165">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="24ced-166">Описание</span><span class="sxs-lookup"><span data-stu-id="24ced-166">Description</span></span> | <span data-ttu-id="24ced-167">Описание плитки.</span><span class="sxs-lookup"><span data-stu-id="24ced-167">A description of the tile.</span></span> |
   | <span data-ttu-id="24ced-168">Веб-адрес</span><span class="sxs-lookup"><span data-stu-id="24ced-168">Internet address</span></span> | <span data-ttu-id="24ced-169">Введите URL-адрес страницы дистанционного обслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="24ced-169">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="24ced-170">Размер плитки</span><span class="sxs-lookup"><span data-stu-id="24ced-170">Tile size</span></span> | <span data-ttu-id="24ced-171">Размер плитки: маленький, средний или большой.</span><span class="sxs-lookup"><span data-stu-id="24ced-171">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="24ced-172">Цель</span><span class="sxs-lookup"><span data-stu-id="24ced-172">Target</span></span> | <span data-ttu-id="24ced-173">Указывает, следует ли открывать страницу в новом окне или в текущем окне.</span><span class="sxs-lookup"><span data-stu-id="24ced-173">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="24ced-174">Фоновое изображение плитки</span><span class="sxs-lookup"><span data-stu-id="24ced-174">Tile background image</span></span> | <span data-ttu-id="24ced-175">URL-адрес изображения, используемого для плитки (необязательно).</span><span class="sxs-lookup"><span data-stu-id="24ced-175">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="24ced-176">Запустить</span><span class="sxs-lookup"><span data-stu-id="24ced-176">Start</span></span> | <span data-ttu-id="24ced-177">Дата и время начала, когда плитка должна быть доступна.</span><span class="sxs-lookup"><span data-stu-id="24ced-177">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="24ced-178">Окончание</span><span class="sxs-lookup"><span data-stu-id="24ced-178">End</span></span> | <span data-ttu-id="24ced-179">Дата и время окончания доступности плитки.</span><span class="sxs-lookup"><span data-stu-id="24ced-179">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="24ced-180">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="24ced-180">Select **Save**.</span></span>
