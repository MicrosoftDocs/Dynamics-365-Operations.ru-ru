---
title: Настройка самообслуживания сотрудников
description: ''
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
ms.openlocfilehash: e44a35071b8d0987e6c949fb11312204317b44a1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010345"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="4088b-102">Настройка самообслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="4088b-102">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="4088b-103">В Microsoft Dynamics 365 Human Resources можно настроить плитки для переходов верхнего уровня в модуле дистанционного обслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="4088b-103">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="4088b-104">Плитки плана льгот направляют пользователей в планы льгот, для которых они могут быть зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="4088b-104">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="4088b-105">Настройка плитки ролевого центра</span><span class="sxs-lookup"><span data-stu-id="4088b-105">Set up a role center tile</span></span>

1. <span data-ttu-id="4088b-106">В рабочей области **Управление льготами** в **Настройка** выберите **Параметры дистанционного обслуживания сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="4088b-106">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="4088b-107">Выберите вкладку **Настройка плитки ролевого центра**, а затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4088b-107">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="4088b-108">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="4088b-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="4088b-109">Поле</span><span class="sxs-lookup"><span data-stu-id="4088b-109">Field</span></span> | <span data-ttu-id="4088b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4088b-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4088b-111">Идентификатор плитки</span><span class="sxs-lookup"><span data-stu-id="4088b-111">Tile ID</span></span> | <span data-ttu-id="4088b-112">Уникальный идентификатор для плитки.</span><span class="sxs-lookup"><span data-stu-id="4088b-112">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="4088b-113">Текст метки плитки</span><span class="sxs-lookup"><span data-stu-id="4088b-113">Tile label text</span></span> | <span data-ttu-id="4088b-114">Текст, который будет отображаться для плитки при дистанционном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="4088b-114">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="4088b-115">Описание</span><span class="sxs-lookup"><span data-stu-id="4088b-115">Description</span></span> | <span data-ttu-id="4088b-116">Описание плитки.</span><span class="sxs-lookup"><span data-stu-id="4088b-116">A description of the tile.</span></span> |
   | <span data-ttu-id="4088b-117">Веб-адрес</span><span class="sxs-lookup"><span data-stu-id="4088b-117">Internet address</span></span> | <span data-ttu-id="4088b-118">Введите URL-адрес страницы дистанционного обслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="4088b-118">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="4088b-119">Размер плитки</span><span class="sxs-lookup"><span data-stu-id="4088b-119">Tile size</span></span> | <span data-ttu-id="4088b-120">Размер плитки: маленький, средний или большой.</span><span class="sxs-lookup"><span data-stu-id="4088b-120">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="4088b-121">Цель</span><span class="sxs-lookup"><span data-stu-id="4088b-121">Target</span></span> | <span data-ttu-id="4088b-122">Указывает, следует ли открывать страницу в новом окне или в текущем окне.</span><span class="sxs-lookup"><span data-stu-id="4088b-122">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="4088b-123">Фоновое изображение плитки</span><span class="sxs-lookup"><span data-stu-id="4088b-123">Tile background image</span></span> | <span data-ttu-id="4088b-124">URL-адрес изображения, используемого для плитки (необязательно).</span><span class="sxs-lookup"><span data-stu-id="4088b-124">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="4088b-125">Запустить</span><span class="sxs-lookup"><span data-stu-id="4088b-125">Start</span></span> | <span data-ttu-id="4088b-126">Дата и время начала, когда плитка должна быть доступна.</span><span class="sxs-lookup"><span data-stu-id="4088b-126">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="4088b-127">Окончание</span><span class="sxs-lookup"><span data-stu-id="4088b-127">End</span></span> | <span data-ttu-id="4088b-128">Дата и время окончания доступности плитки.</span><span class="sxs-lookup"><span data-stu-id="4088b-128">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="4088b-129">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4088b-129">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="4088b-130">Настройка плитки планов льгот</span><span class="sxs-lookup"><span data-stu-id="4088b-130">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="4088b-131">В рабочей области **Управление льготами** в **Настройка** выберите **Параметры дистанционного обслуживания сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="4088b-131">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="4088b-132">Выберите вкладку **Настройка плитки планов льгот**, а затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4088b-132">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="4088b-133">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="4088b-133">Specify values for the following fields:</span></span>

   | <span data-ttu-id="4088b-134">Поле</span><span class="sxs-lookup"><span data-stu-id="4088b-134">Field</span></span> | <span data-ttu-id="4088b-135">Описание</span><span class="sxs-lookup"><span data-stu-id="4088b-135">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4088b-136">Идентификатор плитки</span><span class="sxs-lookup"><span data-stu-id="4088b-136">Tile ID</span></span> | <span data-ttu-id="4088b-137">Уникальный идентификатор для плитки.</span><span class="sxs-lookup"><span data-stu-id="4088b-137">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="4088b-138">Текст метки плитки</span><span class="sxs-lookup"><span data-stu-id="4088b-138">Tile label text</span></span> | <span data-ttu-id="4088b-139">Текст, который будет отображаться для плитки при дистанционном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="4088b-139">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="4088b-140">Описание</span><span class="sxs-lookup"><span data-stu-id="4088b-140">Description</span></span> | <span data-ttu-id="4088b-141">Описание плитки.</span><span class="sxs-lookup"><span data-stu-id="4088b-141">A description of the tile.</span></span> |
   | <span data-ttu-id="4088b-142">Веб-адрес</span><span class="sxs-lookup"><span data-stu-id="4088b-142">Internet address</span></span> | <span data-ttu-id="4088b-143">Введите URL-адрес страницы дистанционного обслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="4088b-143">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="4088b-144">Размер плитки</span><span class="sxs-lookup"><span data-stu-id="4088b-144">Tile size</span></span> | <span data-ttu-id="4088b-145">Размер плитки: маленький, средний или большой.</span><span class="sxs-lookup"><span data-stu-id="4088b-145">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="4088b-146">Цель</span><span class="sxs-lookup"><span data-stu-id="4088b-146">Target</span></span> | <span data-ttu-id="4088b-147">Указывает, следует ли открывать страницу в новом окне или в текущем окне.</span><span class="sxs-lookup"><span data-stu-id="4088b-147">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="4088b-148">Фоновое изображение плитки</span><span class="sxs-lookup"><span data-stu-id="4088b-148">Tile background image</span></span> | <span data-ttu-id="4088b-149">URL-адрес изображения, используемого для плитки (необязательно).</span><span class="sxs-lookup"><span data-stu-id="4088b-149">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="4088b-150">Запустить</span><span class="sxs-lookup"><span data-stu-id="4088b-150">Start</span></span> | <span data-ttu-id="4088b-151">Дата и время начала, когда плитка должна быть доступна.</span><span class="sxs-lookup"><span data-stu-id="4088b-151">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="4088b-152">Окончание</span><span class="sxs-lookup"><span data-stu-id="4088b-152">End</span></span> | <span data-ttu-id="4088b-153">Дата и время окончания доступности плитки.</span><span class="sxs-lookup"><span data-stu-id="4088b-153">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="4088b-154">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4088b-154">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="4088b-155">Настройка плитки плана гибкого кредита</span><span class="sxs-lookup"><span data-stu-id="4088b-155">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="4088b-156">В рабочей области **Управление льготами** в **Настройка** выберите **Параметры дистанционного обслуживания сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="4088b-156">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="4088b-157">Выберите вкладку **Настройка плитки плана гибкого кредита**, а затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4088b-157">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="4088b-158">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="4088b-158">Specify values for the following fields:</span></span>

   | <span data-ttu-id="4088b-159">Поле</span><span class="sxs-lookup"><span data-stu-id="4088b-159">Field</span></span> | <span data-ttu-id="4088b-160">Описание</span><span class="sxs-lookup"><span data-stu-id="4088b-160">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4088b-161">Идентификатор плитки</span><span class="sxs-lookup"><span data-stu-id="4088b-161">Tile ID</span></span> | <span data-ttu-id="4088b-162">Уникальный идентификатор для плитки.</span><span class="sxs-lookup"><span data-stu-id="4088b-162">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="4088b-163">Текст метки плитки</span><span class="sxs-lookup"><span data-stu-id="4088b-163">Tile label text</span></span> | <span data-ttu-id="4088b-164">Текст, который будет отображаться для плитки при дистанционном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="4088b-164">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="4088b-165">Описание</span><span class="sxs-lookup"><span data-stu-id="4088b-165">Description</span></span> | <span data-ttu-id="4088b-166">Описание плитки.</span><span class="sxs-lookup"><span data-stu-id="4088b-166">A description of the tile.</span></span> |
   | <span data-ttu-id="4088b-167">Веб-адрес</span><span class="sxs-lookup"><span data-stu-id="4088b-167">Internet address</span></span> | <span data-ttu-id="4088b-168">Введите URL-адрес страницы дистанционного обслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="4088b-168">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="4088b-169">Размер плитки</span><span class="sxs-lookup"><span data-stu-id="4088b-169">Tile size</span></span> | <span data-ttu-id="4088b-170">Размер плитки: маленький, средний или большой.</span><span class="sxs-lookup"><span data-stu-id="4088b-170">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="4088b-171">Цель</span><span class="sxs-lookup"><span data-stu-id="4088b-171">Target</span></span> | <span data-ttu-id="4088b-172">Указывает, следует ли открывать страницу в новом окне или в текущем окне.</span><span class="sxs-lookup"><span data-stu-id="4088b-172">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="4088b-173">Фоновое изображение плитки</span><span class="sxs-lookup"><span data-stu-id="4088b-173">Tile background image</span></span> | <span data-ttu-id="4088b-174">URL-адрес изображения, используемого для плитки (необязательно).</span><span class="sxs-lookup"><span data-stu-id="4088b-174">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="4088b-175">Запустить</span><span class="sxs-lookup"><span data-stu-id="4088b-175">Start</span></span> | <span data-ttu-id="4088b-176">Дата и время начала, когда плитка должна быть доступна.</span><span class="sxs-lookup"><span data-stu-id="4088b-176">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="4088b-177">Окончание</span><span class="sxs-lookup"><span data-stu-id="4088b-177">End</span></span> | <span data-ttu-id="4088b-178">Дата и время окончания доступности плитки.</span><span class="sxs-lookup"><span data-stu-id="4088b-178">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="4088b-179">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4088b-179">Select **Save**.</span></span>
