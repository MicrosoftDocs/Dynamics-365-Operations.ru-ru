---
title: Загрузка конфигураций электронной отчетности из Lifecycle Services
description: В этом разделе описывается, как загрузить конфигурации электронной отчетности из Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 418586113c038c3227f0704495a561eac319bdc9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745095"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="e607a-103">Загрузка конфигураций электронной отчетности из Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="e607a-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e607a-104">В этой теме объясняется, как загрузить новейшую версию [конфигураций электронной отчетности (ER)](general-electronic-reporting.md#Configuration) из [библиотеки общих ресурсов](../lifecycle-services/asset-library.md) в Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e607a-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="e607a-105">Войдите в приложение с помощью одной из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="e607a-105">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="e607a-106">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="e607a-106">Electronic reporting developer</span></span>
    - <span data-ttu-id="e607a-107">Консультант по функциональным возможностям электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="e607a-107">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="e607a-108">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="e607a-108">System administrator</span></span>

2. <span data-ttu-id="e607a-109">Перейдите в раздел **Управление организацией** &gt; **Рабочие области** &gt; **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="e607a-109">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="e607a-110">В разделе **Поставщики конфигурации** выберите плитку **Майкрософт**.</span><span class="sxs-lookup"><span data-stu-id="e607a-110">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="e607a-111">На плитке **Майкрософт** выберите **Репозитории**.</span><span class="sxs-lookup"><span data-stu-id="e607a-111">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="e607a-112">[![Плитка Майкрософт на странице конфигураций локализации](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="e607a-112">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="e607a-113">На странице **Репозиторий конфигураций** в сетке выберите существующий репозиторий типа **LCS**.</span><span class="sxs-lookup"><span data-stu-id="e607a-113">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="e607a-114">Если этот репозиторий не отображается в сетке, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e607a-114">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="e607a-115">Выберите **Добавить**, чтобы добавить репозиторий.</span><span class="sxs-lookup"><span data-stu-id="e607a-115">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="e607a-116">Выберите **LCS** как тип репозитория.</span><span class="sxs-lookup"><span data-stu-id="e607a-116">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="e607a-117">Выберите **Создать репозиторий**.</span><span class="sxs-lookup"><span data-stu-id="e607a-117">Select **Create repository**.</span></span>
    4. <span data-ttu-id="e607a-118">При появлении запроса об авторизации выполните инструкции на экране.</span><span class="sxs-lookup"><span data-stu-id="e607a-118">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="e607a-119">Введите имя и описание репозитория.</span><span class="sxs-lookup"><span data-stu-id="e607a-119">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="e607a-120">Выберите **ОК**, чтобы подтвердить новую запись репозитория.</span><span class="sxs-lookup"><span data-stu-id="e607a-120">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="e607a-121">В сетке выберите новый репозиторий типа **LCS**.</span><span class="sxs-lookup"><span data-stu-id="e607a-121">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="e607a-122">Выберите **Открыть** для просмотра списка конфигураций электронной отчетности для выбранного репозитория.</span><span class="sxs-lookup"><span data-stu-id="e607a-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="e607a-123">[![Страница репозиториев конфигураций](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="e607a-123">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="e607a-124">При возникновении проблем с доступом к репозиторию LCS для загрузки конфигураций из библиотеки общих активов в LCS можно загрузить конфигурации из [глобального репозитория](er-download-configurations-global-repo.md).</span><span class="sxs-lookup"><span data-stu-id="e607a-124">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="e607a-125">В дереве конфигураций в левой области выберите требуемую конфигурацию электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="e607a-125">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="e607a-126">На экспресс-вкладке **Версии** выберите требуемую версию выбранной конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="e607a-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="e607a-127">Выберите **Импорт** для загрузки выбранной версии из LCS в текущий экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e607a-127">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e607a-128">Кнопка **Импорт** недоступна для версий конфигурации электронной отчетности, которые уже установлены в текущем экземпляре.</span><span class="sxs-lookup"><span data-stu-id="e607a-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="e607a-129">[![Страница репозитория конфигурации](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="e607a-129">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="e607a-130">В зависимости от параметров электронной отчетности конфигурации проверяются после импорта.</span><span class="sxs-lookup"><span data-stu-id="e607a-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="e607a-131">Возможно, вы получите уведомление об обнаруженных проблемах несоответствия.</span><span class="sxs-lookup"><span data-stu-id="e607a-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="e607a-132">Необходимо устранить эти проблемы перед использованием импортированной версии конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e607a-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="e607a-133">Дополнительные сведения см. в списке связанных тем для этой темы.</span><span class="sxs-lookup"><span data-stu-id="e607a-133">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e607a-134">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e607a-134">Additional resources</span></span>

[<span data-ttu-id="e607a-135">Обзор электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="e607a-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="e607a-136">Загрузка конфигураций электронной отчетности (ER) из глобального репозитория Configuration Service</span><span class="sxs-lookup"><span data-stu-id="e607a-136">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]