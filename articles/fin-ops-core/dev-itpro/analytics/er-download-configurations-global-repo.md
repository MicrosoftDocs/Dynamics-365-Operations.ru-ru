---
title: Загрузка конфигураций электронной отчетности (ER) из глобального репозитория Configuration Service
description: В этом разделе описан порядок загрузки конфигураций электронной отчетности (ER) из глобального репозитория Configuration Service.
author: NickSelin
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a96e78a64fe0559ae5f3bfddabf3fe1cad8a3dcb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679566"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a><span data-ttu-id="2b4e0-103">Загрузка конфигураций электронной отчетности (ER) из глобального репозитория Configuration Service</span><span class="sxs-lookup"><span data-stu-id="2b4e0-103">Download ER configurations from the Global repository of Configuration service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b4e0-104">В этом разделе описан порядок загрузки [конфигураций электронной отчетности (ER)](general-electronic-reporting.md#Configuration) из глобального репозитория Configuration Service.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-104">This topic explains how to download [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the Global repository of configuration service.</span></span> <span data-ttu-id="2b4e0-105">Дополнительные сведения см. в разделе [Microsoft Dynamics 365 for Finance and Operations — Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="2b4e0-105">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="open-configurations-repository"></a><span data-ttu-id="2b4e0-106">Откройте репозиторий конфигураций</span><span class="sxs-lookup"><span data-stu-id="2b4e0-106">Open configurations repository</span></span>

1. <span data-ttu-id="2b4e0-107">Войдите в приложение Dynamics 365 Finance с помощью одной из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="2b4e0-107">Sign in to the Dynamics 365 Finance application using one of the following roles:</span></span>

    - <span data-ttu-id="2b4e0-108">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b4e0-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="2b4e0-109">Консультант по функциональным возможностям электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b4e0-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="2b4e0-110">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="2b4e0-110">System administrator</span></span>

2. <span data-ttu-id="2b4e0-111">Перейдите в раздел **Управление организацией > Рабочие области > Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-111">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="2b4e0-112">В разделе **Поставщики конфигурации** выберите плитку **Майкрософт**.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
3. <span data-ttu-id="2b4e0-113">На плитке **Майкрософт** выберите **Репозитории**.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    ![Рабочая область электронной отчетности](./media/er-download-configurations-global-repo-er-workspace.png)

4. <span data-ttu-id="2b4e0-115">На странице **Репозиторий конфигураций** в сетке выберите существующий репозиторий типа **Глобальный**.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **Global** type.</span></span> <span data-ttu-id="2b4e0-116">Если этот репозиторий не отображается в сетке, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="2b4e0-117">Выберите **Добавить**, чтобы добавить новый репозиторий.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-117">Select **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="2b4e0-118">Выберите **Глобальный** в качестве типа репозитория, а затем выберите **Создать репозиторий**.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-118">Select **Global** as the repository type, and then select **Create repository**.</span></span>
    3. <span data-ttu-id="2b4e0-119">Если будет предложено, следуйте инструкциям по авторизации.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-119">If prompted, follow the authorization instructions.</span></span>
    4. <span data-ttu-id="2b4e0-120">Введите имя и описание репозитория, а затем нажмите **ОК**, чтобы подтвердить новую запись репозитория.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-120">Enter a name and description for the repository and then select **OK** to confirm the new repository entry.</span></span>
    5. <span data-ttu-id="2b4e0-121">В сетке выберите новый репозиторий типа **Глобальный**.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-121">In the grid, select the new repository of the **Global** type.</span></span>

5. <span data-ttu-id="2b4e0-122">Выберите **Открыть** для просмотра списка конфигураций электронной отчетности для выбранного репозитория.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    ![Страница репозиториев конфигураций](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a><span data-ttu-id="2b4e0-124">Импорт одной конфигурации</span><span class="sxs-lookup"><span data-stu-id="2b4e0-124">Import a single configuration</span></span>

1. <span data-ttu-id="2b4e0-125">На странице **Репозитории конфигураций** в дереве конфигураций выберите нужную конфигурацию электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-125">On the **Configuration repositories** page, in the configurations tree, select the ER configuration that you want.</span></span>
2. <span data-ttu-id="2b4e0-126">На экспресс-вкладке **Версии** выберите требуемую версию выбранной конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
3. <span data-ttu-id="2b4e0-127">Выберите **Импорт** для загрузки выбранной версии из глобального репозитория в текущий экземпляр Finance.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-127">Select **Import** to download the selected version from Global repository to the current Finance instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2b4e0-128">Кнопка **Импорт** недоступна для версий конфигурации электронной отчетности, которые уже установлены в текущем экземпляре Finance.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance instance.</span></span>

    ![Страница репозитория конфигурации](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a><span data-ttu-id="2b4e0-130">Импорт отфильтрованных конфигураций</span><span class="sxs-lookup"><span data-stu-id="2b4e0-130">Import filtered configurations</span></span>

1. <span data-ttu-id="2b4e0-131">На странице **Репозитории конфигураций** в дереве конфигураций разверните экспресс-вкладку **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-131">On the **Configuration repositories** page, in the configurations tree, expand the **Filter** FastTab.</span></span>
2. <span data-ttu-id="2b4e0-132">В сетке **Теги** добавьте необходимые теги.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-132">In the **Tags** grid, add any tags that are needed.</span></span>
3. <span data-ttu-id="2b4e0-133">В поле **Применимость страны/региона** выберите соответствующие коды страны/региона, а затем выберите **Применить фильтр**.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-133">In the **Country/region applicability** field, select the appropriate country/region codes, and then select  **Apply filter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2b4e0-134">На экспресс-вкладке **Конфигурации** показаны все конфигурации, удовлетворяющие указанным условиям выбора.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-134">The **Configurations** FastTab shows all the configurations that satisfy the specified selection conditions.</span></span>

4. <span data-ttu-id="2b4e0-135">На экспресс-вкладке **Конфигурации** выберите **Импорт**, чтобы загрузить отфильтрованные конфигурации из глобального репозитория в текущий экземпляр.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-135">On the **Configurations** FastTab, select **Import** to download the filtered configurations from the Global repository to the current instance.</span></span>
5. <span data-ttu-id="2b4e0-136">На экспресс-вкладке **Конфигурации** выберите **Сброс фильтра** для очистки указанных условий выбора.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-136">On the **Configurations** FastTab, select **Reset filter** to clean up the specified selection conditions.</span></span>

    ![Страница репозитория конфигурации](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> <span data-ttu-id="2b4e0-138">В зависимости от параметров электронной отчетности конфигурации проверяются после импорта.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-138">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="2b4e0-139">Возможно, вы получите уведомление об обнаруженных проблемах несоответствия.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-139">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="2b4e0-140">Необходимо устранить эти проблемы перед использованием импортированной версии конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-140">Before you can use the imported configuration version, you must resolve the issues.</span></span> <span data-ttu-id="2b4e0-141">Дополнительные сведения см. в списке связанных ресурсов для этой темы.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-141">For more information, see the list of related resources for this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="2b4e0-142">Конфигурации электронной отчетности могут быть настроены как зависимые от других конфигураций.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-142">ER configurations can be configured as being dependent on other configurations.</span></span> <span data-ttu-id="2b4e0-143">Таким образом, наряду с выбранной конфигурацией другие конфигурации могут быть импортированы автоматически.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-143">Therefore, along with a selected configuration, other configurations might be automatically imported.</span></span> <span data-ttu-id="2b4e0-144">Дополнительные сведения о зависимостях конфигураций см. в разделе [Определение зависимости конфигураций электронной отчетности от других компонентов](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span><span class="sxs-lookup"><span data-stu-id="2b4e0-144">For more about configuration dependencies, see [Define the dependency of ER configurations on other components](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2b4e0-145">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2b4e0-145">Additional resources</span></span>

[<span data-ttu-id="2b4e0-146">Обзор электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="2b4e0-146">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
