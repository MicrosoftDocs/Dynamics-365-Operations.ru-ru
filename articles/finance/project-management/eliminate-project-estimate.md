---
title: Удаление оценки проекта
description: В этой теме содержатся сведения об удалении оценки проекта после его завершения.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410258"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="cbec0-103">Удаление оценки проекта</span><span class="sxs-lookup"><span data-stu-id="cbec0-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cbec0-104">Оценки проекта обеспечивают финансовое представление для работы, которая оценивается и планируется для проекта.</span><span class="sxs-lookup"><span data-stu-id="cbec0-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="cbec0-105">Для обработки оценок для проекта, следует присоединить проект к проекту НЗП.</span><span class="sxs-lookup"><span data-stu-id="cbec0-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="cbec0-106">Проекты НЗП всегда основаны на существующем проекте, однако несколько проектов могут ссылаться на один проект НЗП.</span><span class="sxs-lookup"><span data-stu-id="cbec0-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="cbec0-107">К проектам НЗП могут быть привязаны только проекты с фиксированной ценой и инвестиционные проекты, которые должны принадлежать той же группе проектов, что и проект НЗП.</span><span class="sxs-lookup"><span data-stu-id="cbec0-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="cbec0-108">Чтобы удалить оценку проекта, он должен быть завершен.</span><span class="sxs-lookup"><span data-stu-id="cbec0-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="cbec0-109">Следующие шаги описывают, как удалить оценку.</span><span class="sxs-lookup"><span data-stu-id="cbec0-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="cbec0-110">Перейдите в раздел **Управление и учет по проектам** > **Все проекты** и откройте проект.</span><span class="sxs-lookup"><span data-stu-id="cbec0-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="cbec0-111">На вкладке **Управление** выберите **Оценки**, а на странице **Оценка** выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="cbec0-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="cbec0-112">На странице **Удалить оценку** на вкладке **Общие** задайте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="cbec0-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="cbec0-113">**Код периода**: выберите код периода для выбора соответствующих проектов НЗП.</span><span class="sxs-lookup"><span data-stu-id="cbec0-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="cbec0-114">**Дата оценки**: выберите соответствующую дату оценки для удаления.</span><span class="sxs-lookup"><span data-stu-id="cbec0-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="cbec0-115">**Удалить с предупреждениями о НЗП**: включите этот параметр, чтобы выдать уведомление, если оценка, связанная с незавершенным производством (НЗП), будет удалена.</span><span class="sxs-lookup"><span data-stu-id="cbec0-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="cbec0-116">Если этот параметр не задан, удаление невозможно продолжить, если существуют не оцененные проводки.</span><span class="sxs-lookup"><span data-stu-id="cbec0-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="cbec0-117">Этот параметр доступен только в том случае, когда закрытие должно применяться к проекту НЗП.</span><span class="sxs-lookup"><span data-stu-id="cbec0-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="cbec0-118">Он недоступен при использовании периодических разносок.</span><span class="sxs-lookup"><span data-stu-id="cbec0-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="cbec0-119">Этот параметр используется с настройками на вкладке **Оценка** на странице **Параметры проекта** в группе полей **Разрешить удаление, когда существуют неоцененные проводки**.</span><span class="sxs-lookup"><span data-stu-id="cbec0-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="cbec0-120">**Задать этап как "Завершено"**: включите этот параметр, чтобы после выполнения удаления этап проекта НЗП был **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="cbec0-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="cbec0-121">**Печать списка оценок**: выберите информацию, которую надо будет включить, когда будет напечатан список оценок.</span><span class="sxs-lookup"><span data-stu-id="cbec0-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="cbec0-122">**Показать Infolog**: включите этот параметр, чтобы отобразить Infolog.</span><span class="sxs-lookup"><span data-stu-id="cbec0-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="cbec0-123">**Дата разноски**: выберите дату разноски ГК для оценки.</span><span class="sxs-lookup"><span data-stu-id="cbec0-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="cbec0-124">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cbec0-124">Select **OK**.</span></span>
5. <span data-ttu-id="cbec0-125">После завершения процесса удаления отображается отрицательное значение для удаленного проекта НЗП.</span><span class="sxs-lookup"><span data-stu-id="cbec0-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="cbec0-126">Если не требуется удалять оценку, можно выбрать удаленную оценку и выбрать **Отменить удаление**.</span><span class="sxs-lookup"><span data-stu-id="cbec0-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
