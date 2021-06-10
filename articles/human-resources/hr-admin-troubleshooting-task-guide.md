---
title: Сохранение проводников по задачам в LCS и их воспроизведение
description: В этой статье объясняется, как сохранять руководства по задачам в Microsoft Dynamics Lifecycle Services (LCS) и затем воспроизводить их.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a18bb14ba8c3c926065c97b0ee26c38ee86ded2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053283"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="0741c-103">Сохранение проводников по задачам в LCS и их воспроизведение</span><span class="sxs-lookup"><span data-stu-id="0741c-103">Save task guides to LCS and replay them</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0741c-104">**Сведения среды**</span><span class="sxs-lookup"><span data-stu-id="0741c-104">**Environment details**</span></span> 

<span data-ttu-id="0741c-105">Microsoft Dynamics 365 Human Resources, который был развернут с помощью Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="0741c-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="0741c-106">**Расход**</span><span class="sxs-lookup"><span data-stu-id="0741c-106">**Issue**</span></span>

<span data-ttu-id="0741c-107">Клиент хочет сохранить новые записи задач в своем проекте LCS и затем воспроизводить сохраненные руководства по задачам.</span><span class="sxs-lookup"><span data-stu-id="0741c-107">The customer wants to save new task recordings to the LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="0741c-108">**Приказ**</span><span class="sxs-lookup"><span data-stu-id="0741c-108">**Resolution**</span></span>

<span data-ttu-id="0741c-109">Выполните эти действия для сохранения записей задач в LCS.</span><span class="sxs-lookup"><span data-stu-id="0741c-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="0741c-110">Выполните вход в LCS, затем выберите проект.</span><span class="sxs-lookup"><span data-stu-id="0741c-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="0741c-111">Выберите плитку **Средство моделирования бизнес-процессов**.</span><span class="sxs-lookup"><span data-stu-id="0741c-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="0741c-112">Просмотрите эту страницу в обновленном средстве моделирования бизнес-процессов.</span><span class="sxs-lookup"><span data-stu-id="0741c-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="0741c-113">Выберите библиотеку, затем выберите **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="0741c-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="0741c-114">Введите имя для модели средства моделирования бизнес-процессов (BPM).</span><span class="sxs-lookup"><span data-stu-id="0741c-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="0741c-115">Выполните вход в Human Resources из LCS.</span><span class="sxs-lookup"><span data-stu-id="0741c-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="0741c-116">В поле **Поиск** введите **справка**.</span><span class="sxs-lookup"><span data-stu-id="0741c-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="0741c-117">Открывается справка Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="0741c-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="0741c-118">Выберите кнопку **Обновить** для конфигурации справки Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="0741c-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="0741c-119">Должна появиться ваша новая библиотека BPM, и она должна быть активной.</span><span class="sxs-lookup"><span data-stu-id="0741c-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="0741c-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="0741c-120">Close the page.</span></span>
10. <span data-ttu-id="0741c-121">Создайте запись задачи.</span><span class="sxs-lookup"><span data-stu-id="0741c-121">Create a task recording.</span></span>
11. <span data-ttu-id="0741c-122">После завершения выберите **Сохранить файл в Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="0741c-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Сохраните файл в Lifecycle Services.](media/task-guides.png)

12. <span data-ttu-id="0741c-124">Выберите библиотеку BMP и узел, в который требуется сохранить запись задачи.</span><span class="sxs-lookup"><span data-stu-id="0741c-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="0741c-125">Выполните следующие действия, чтобы воспроизвести руководство по задаче из LCS.</span><span class="sxs-lookup"><span data-stu-id="0741c-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="0741c-126">Запустите регистратор задач.</span><span class="sxs-lookup"><span data-stu-id="0741c-126">Start Task recorder.</span></span>
2. <span data-ttu-id="0741c-127">Выберите **Открыть из LCS**.</span><span class="sxs-lookup"><span data-stu-id="0741c-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="0741c-128">Выберите библиотеку и узел BPM, в которых сохранено руководство по задаче.</span><span class="sxs-lookup"><span data-stu-id="0741c-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="0741c-129">Откройте руководство по задаче.</span><span class="sxs-lookup"><span data-stu-id="0741c-129">Open the task guide.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]