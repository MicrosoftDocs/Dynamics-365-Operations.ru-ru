---
title: Сохранение проводников по задачам в LCS и их воспроизведение
description: В этом разделе объясняется, как сохранять руководства по задачам в Microsoft Dynamics Lifecycle Services (LCS) и затем воспроизводить их.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 40b4c3154a04a557b8a670e1f1ae3722c71122fe
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "305966"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="46248-103">Сохранение проводников по задачам в LCS и их воспроизведение</span><span class="sxs-lookup"><span data-stu-id="46248-103">Save task guides to LCS and replay them</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="46248-104">**Сведения среды**</span><span class="sxs-lookup"><span data-stu-id="46248-104">**Environment details**</span></span> 

<span data-ttu-id="46248-105">Microsoft Dynamics 365 for Talent, который был развернут с помощью Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="46248-105">Microsoft Dynamics 365 for Talent, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="46248-106">**Расход**</span><span class="sxs-lookup"><span data-stu-id="46248-106">**Issue**</span></span>

<span data-ttu-id="46248-107">Клиент хочет сохранить новые записи задач в своем проекте LCS и затем воспроизводить сохраненные руководства по задачам.</span><span class="sxs-lookup"><span data-stu-id="46248-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="46248-108">**Разрешение**</span><span class="sxs-lookup"><span data-stu-id="46248-108">**Resolution**</span></span>

<span data-ttu-id="46248-109">Выполните эти действия для сохранения записей задач в LCS.</span><span class="sxs-lookup"><span data-stu-id="46248-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="46248-110">Выполните вход в LCS, затем выберите проект.</span><span class="sxs-lookup"><span data-stu-id="46248-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="46248-111">Выберите плитку **Средство моделирования бизнес-процессов**.</span><span class="sxs-lookup"><span data-stu-id="46248-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="46248-112">Просмотрите эту страницу в обновленном средстве моделирования бизнес-процессов.</span><span class="sxs-lookup"><span data-stu-id="46248-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="46248-113">Выберите библиотеку, затем выберите **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="46248-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="46248-114">Введите имя для модели средства моделирования бизнес-процессов (BPM).</span><span class="sxs-lookup"><span data-stu-id="46248-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="46248-115">Войдите в Talent из LCS.</span><span class="sxs-lookup"><span data-stu-id="46248-115">Sign in to Talent from LCS.</span></span>
7. <span data-ttu-id="46248-116">В поле **Поиск** введите **справка**.</span><span class="sxs-lookup"><span data-stu-id="46248-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="46248-117">Открывается справка Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="46248-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="46248-118">Выберите кнопку **Обновить** для конфигурации справки Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="46248-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="46248-119">Должна появиться ваша новая библиотека BPM, и она должна быть активной.</span><span class="sxs-lookup"><span data-stu-id="46248-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="46248-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="46248-120">Close the page.</span></span>
10. <span data-ttu-id="46248-121">Создайте запись задачи.</span><span class="sxs-lookup"><span data-stu-id="46248-121">Create a task recording.</span></span>
11. <span data-ttu-id="46248-122">После завершения выберите **Сохранить файл в Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="46248-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Сохраните файл в Lifecycle Services.](media/task-guides.png)

12. <span data-ttu-id="46248-124">Выберите библиотеку BMP и узел, в который требуется сохранить запись задачи.</span><span class="sxs-lookup"><span data-stu-id="46248-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="46248-125">Выполните следующие действия, чтобы воспроизвести руководство по задаче из LCS.</span><span class="sxs-lookup"><span data-stu-id="46248-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="46248-126">Запустите регистратор задач.</span><span class="sxs-lookup"><span data-stu-id="46248-126">Start Task recorder.</span></span>
2. <span data-ttu-id="46248-127">Выберите **Открыть из LCS**.</span><span class="sxs-lookup"><span data-stu-id="46248-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="46248-128">Выберите библиотеку и узел BPM, в которых сохранено руководство по задаче.</span><span class="sxs-lookup"><span data-stu-id="46248-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="46248-129">Откройте руководство по задаче.</span><span class="sxs-lookup"><span data-stu-id="46248-129">Open the task guide.</span></span>
