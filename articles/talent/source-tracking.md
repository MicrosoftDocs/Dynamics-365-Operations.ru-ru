---
title: Отслеживание источников для профилей и заявлений кандидатов
description: В этом разделе приводятся сведения об отслеживании источника для профилей и заявлений кандидатов.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 2cfa180f992a4f7a9b2e21e0fb3e0845c7546c94
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742731"
---
# <a name="track-candidate-sources"></a><span data-ttu-id="b53c0-103">Отслеживание источников кандидатов</span><span class="sxs-lookup"><span data-stu-id="b53c0-103">Track candidate sources</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> <span data-ttu-id="b53c0-104">Функциональность, описанная в этой теме, доступна в рамках предварительного выпуска.</span><span class="sxs-lookup"><span data-stu-id="b53c0-104">Functionality noted in this topic is available as part of a preview review release.</span></span> <span data-ttu-id="b53c0-105">Содержимое и функциональность могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="b53c0-105">The content and the functionality are subject to change.</span></span> <span data-ttu-id="b53c0-106">Для использования этой функции попросите администратора включить ее с помощью пункта **Параметры администрирования** в Attract.</span><span class="sxs-lookup"><span data-stu-id="b53c0-106">To use this feature, ask an administrator to enable it using the **Admin settings** in Attract.</span></span> <span data-ttu-id="b53c0-107">В будущих выпусках будут представлены отчеты отслеживания источника.</span><span class="sxs-lookup"><span data-stu-id="b53c0-107">A future release will provide source tracking reports.</span></span> <span data-ttu-id="b53c0-108">Дополнительные сведения см. в разделе [Доступ к предварительным версиям функций в Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="b53c0-108">For more information, see [Access preview features in Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

<span data-ttu-id="b53c0-109">Когда кандидаты подают заявление о приеме на работу, Attract автоматически отслеживает источник их заявлений, предоставляя ценные сведения, чтобы помочь правильно направить ваши усилия по найму.</span><span class="sxs-lookup"><span data-stu-id="b53c0-109">When candidates apply for a job, Attract automatically tracks the source of their applications, providing you with valuable information to help you target your recruiting efforts.</span></span> <span data-ttu-id="b53c0-110">Агенты и менеджеры по найму могут также выбрать источник заявления, вручную добавляя кандидата в должность или кадровый пул.</span><span class="sxs-lookup"><span data-stu-id="b53c0-110">Recruiters and hiring managers can also select an application source while manually adding a candidate to a job or talent pool.</span></span>

<span data-ttu-id="b53c0-111">Источник заявления можно просмотреть в сведениях действий заявлений на вкладке **Действие**, а также в истории заявлений, доступной в разделе **Профиль** в кадровом пуле.</span><span class="sxs-lookup"><span data-stu-id="b53c0-111">You can view the application source in the application activity details under the **Activity** tab, as well as in the application history available under **Profile** in talent pools.</span></span> <span data-ttu-id="b53c0-112">Можно найти источник профиля кандидата в сведениях кандидата на вкладке **Профиль** как в заявлениях, так и в кадровых пулах.</span><span class="sxs-lookup"><span data-stu-id="b53c0-112">You can find a candidate's profile source in the candidate details under the **Profile** tab in both applications and talent pools.</span></span>

> [!NOTE] 
> <span data-ttu-id="b53c0-113">Шаблоны процесса можно найти в разделе [Надстройка Comprehensive Hiring](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="b53c0-113">You can find process templates in the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>

## <a name="pre-configured-sources"></a><span data-ttu-id="b53c0-114">Заранее настроенные источники</span><span class="sxs-lookup"><span data-stu-id="b53c0-114">Pre-configured sources</span></span>

<span data-ttu-id="b53c0-115">Список источников по умолчанию содержит общие источники заявлений.</span><span class="sxs-lookup"><span data-stu-id="b53c0-115">The default source list contains common application sources.</span></span> <span data-ttu-id="b53c0-116">Некоторые типы источников, такие как **Доска объявлений** и **Социальные сети**, имеют дополнительные сведения об источнике.</span><span class="sxs-lookup"><span data-stu-id="b53c0-116">Some source types, like **Job board** and **Social Network**, have additional source details.</span></span> <span data-ttu-id="b53c0-117">Например, **Социальные сети** включают в себя Facebook и Twitter.</span><span class="sxs-lookup"><span data-stu-id="b53c0-117">For example, **Social Network** includes Facebook and Twitter.</span></span> <span data-ttu-id="b53c0-118">Тип источника **Ссылка** позволяет указать внутреннего сотрудника как источник ссылки.</span><span class="sxs-lookup"><span data-stu-id="b53c0-118">The **Referral** source type allows you to specify an internal employee as the referrer.</span></span> <span data-ttu-id="b53c0-119">Список источников по умолчанию включает в себя следующие предварительно настроенные источники:</span><span class="sxs-lookup"><span data-stu-id="b53c0-119">The default source list includes the following pre-configured sources:</span></span>

-   <span data-ttu-id="b53c0-120">Сайт вакансий Attract</span><span class="sxs-lookup"><span data-stu-id="b53c0-120">Attract career site</span></span>

-   <span data-ttu-id="b53c0-121">Агентство</span><span class="sxs-lookup"><span data-stu-id="b53c0-121">Agency</span></span>

-   <span data-ttu-id="b53c0-122">Ярмарка вакансий</span><span class="sxs-lookup"><span data-stu-id="b53c0-122">Career Fair</span></span>

-   <span data-ttu-id="b53c0-123">Маркетинг компаний</span><span class="sxs-lookup"><span data-stu-id="b53c0-123">Company Marketing</span></span>

-   <span data-ttu-id="b53c0-124">Конференции и торговые выставки</span><span class="sxs-lookup"><span data-stu-id="b53c0-124">Conferences & Trade shows</span></span>

-   <span data-ttu-id="b53c0-125">Профессиональные объединения</span><span class="sxs-lookup"><span data-stu-id="b53c0-125">Professional Association</span></span>

-   <span data-ttu-id="b53c0-126">Доска объявлений</span><span class="sxs-lookup"><span data-stu-id="b53c0-126">Job board</span></span>

    -   <span data-ttu-id="b53c0-127">Indeed</span><span class="sxs-lookup"><span data-stu-id="b53c0-127">Indeed</span></span>

    -   <span data-ttu-id="b53c0-128">Seek</span><span class="sxs-lookup"><span data-stu-id="b53c0-128">Seek</span></span>

    -   <span data-ttu-id="b53c0-129">CareerBuilder</span><span class="sxs-lookup"><span data-stu-id="b53c0-129">CareerBuilder</span></span>

    -   <span data-ttu-id="b53c0-130">Google Jobs</span><span class="sxs-lookup"><span data-stu-id="b53c0-130">Google Jobs</span></span>

    -   <span data-ttu-id="b53c0-131">Xing</span><span class="sxs-lookup"><span data-stu-id="b53c0-131">Xing</span></span>

    -   <span data-ttu-id="b53c0-132">Glassdoor</span><span class="sxs-lookup"><span data-stu-id="b53c0-132">Glassdoor</span></span>

    -   <span data-ttu-id="b53c0-133">Monster Jobs</span><span class="sxs-lookup"><span data-stu-id="b53c0-133">Monster Jobs</span></span>

-   <span data-ttu-id="b53c0-134">Журналы и публикации</span><span class="sxs-lookup"><span data-stu-id="b53c0-134">Magazines & Publications</span></span>

-   <span data-ttu-id="b53c0-135">Социальные сети</span><span class="sxs-lookup"><span data-stu-id="b53c0-135">Social Network</span></span>

    -   <span data-ttu-id="b53c0-136">Facebook</span><span class="sxs-lookup"><span data-stu-id="b53c0-136">Facebook</span></span>

    -   <span data-ttu-id="b53c0-137">Twitter</span><span class="sxs-lookup"><span data-stu-id="b53c0-137">Twitter</span></span>

-   <span data-ttu-id="b53c0-138">Набор сотрудников в университеты</span><span class="sxs-lookup"><span data-stu-id="b53c0-138">University Recruiting</span></span>

-   <span data-ttu-id="b53c0-139">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="b53c0-139">LinkedIn</span></span>

-   <span data-ttu-id="b53c0-140">Classifieds</span><span class="sxs-lookup"><span data-stu-id="b53c0-140">Classifieds</span></span>

-   <span data-ttu-id="b53c0-141">Ссылка</span><span class="sxs-lookup"><span data-stu-id="b53c0-141">Referral</span></span>

-   <span data-ttu-id="b53c0-142">Добавлено агентом по найму</span><span class="sxs-lookup"><span data-stu-id="b53c0-142">Added by Recruiter</span></span>

-   <span data-ttu-id="b53c0-143">Прочие</span><span class="sxs-lookup"><span data-stu-id="b53c0-143">Other</span></span>

## <a name="customize-the-source-list"></a><span data-ttu-id="b53c0-144">Настройка списка источников</span><span class="sxs-lookup"><span data-stu-id="b53c0-144">Customize the source list</span></span> 

<span data-ttu-id="b53c0-145">Можно расширить список источников для включения дополнительных источников заявлений.</span><span class="sxs-lookup"><span data-stu-id="b53c0-145">You can extend the source list to include additional application sources.</span></span> <span data-ttu-id="b53c0-146">Чтобы настроить этот список, следуйте указаниям в разделе [Расширение наборов параметров в Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span><span class="sxs-lookup"><span data-stu-id="b53c0-146">To customize this list, follow the instructions in [Extending Option Sets in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span></span> <span data-ttu-id="b53c0-147">Измените объект **TalentSource**, чтобы включить дополнительные источники.</span><span class="sxs-lookup"><span data-stu-id="b53c0-147">Edit the **TalentSource** entity to include additional sources.</span></span> 

<span data-ttu-id="b53c0-148">Чтобы избежать отрицательного влияния на пользовательский интерфейс (UI), не изменяйте и не удаляйте значения перечисления **TalentCategory** (не имена) для следующего:</span><span class="sxs-lookup"><span data-stu-id="b53c0-148">To avoid negatively impacting the user interface (UI), don't edit or delete the **TalentCategory** enum values (not names) for the following:</span></span>

- <span data-ttu-id="b53c0-149">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="b53c0-149">**Referral**</span></span>
- <span data-ttu-id="b53c0-150">**LinkedIn**</span><span class="sxs-lookup"><span data-stu-id="b53c0-150">**LinkedIn**</span></span>
- <span data-ttu-id="b53c0-151">**Прочие**</span><span class="sxs-lookup"><span data-stu-id="b53c0-151">**Other**</span></span>

<span data-ttu-id="b53c0-152">Вместо этого можно расширить перечисление **TalentSource**, чтобы добавить другие типы источников.</span><span class="sxs-lookup"><span data-stu-id="b53c0-152">Instead, you can extend the **TalentSource** enum to add other types of sources.</span></span>
