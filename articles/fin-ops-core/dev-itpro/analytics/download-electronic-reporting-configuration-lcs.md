---
title: Загрузка конфигураций электронной отчетности из Lifecycle Services
description: В этом разделе описывается, как загрузить конфигурации электронной отчетности из Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 561187343073a84b152151abe8770e89196eaa56
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174129"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="41f25-103">Загрузка конфигураций электронной отчетности из Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="41f25-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41f25-104">В этом разделе описывается, как загрузить конфигурации электронной отчетности из Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="41f25-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="41f25-105">В этом учебнике описывается процесс загрузки последней версии конфигураций электронной отчетности из Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="41f25-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="41f25-106">Войдите в приложение с помощью одной из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="41f25-106">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="41f25-107">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="41f25-107">Electronic reporting developer</span></span>
    - <span data-ttu-id="41f25-108">Консультант по функциональным возможностям электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="41f25-108">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="41f25-109">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="41f25-109">System administrator</span></span>

2. <span data-ttu-id="41f25-110">Перейдите в раздел **Управление организацией** &gt; **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="41f25-110">Go to **Organization administration** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="41f25-111">В разделе **Поставщики конфигурации** выберите плитку **Майкрософт**.</span><span class="sxs-lookup"><span data-stu-id="41f25-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="41f25-112">На плитке **Майкрософт** щелкните **Репозитории**.</span><span class="sxs-lookup"><span data-stu-id="41f25-112">On the **Microsoft** tile, click **Repositories**.</span></span>

    <span data-ttu-id="41f25-113">[![обновление-er-из-lcs-для-ms-открытие-списка-репозиториев-ms](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="41f25-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="41f25-114">На странице **Репозиторий конфигураций** в сетке выберите существующий репозиторий типа **LCS**.</span><span class="sxs-lookup"><span data-stu-id="41f25-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="41f25-115">Если этот репозиторий не отображается в сетке, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="41f25-115">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="41f25-116">Нажмите кнопку **Добавить**, чтобы добавить новый репозиторий.</span><span class="sxs-lookup"><span data-stu-id="41f25-116">Click **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="41f25-117">Выберите **LCS** как тип репозитория.</span><span class="sxs-lookup"><span data-stu-id="41f25-117">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="41f25-118">Щелкните **Создать репозиторий**.</span><span class="sxs-lookup"><span data-stu-id="41f25-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="41f25-119">Если будет предложено, следуйте инструкциям по авторизации.</span><span class="sxs-lookup"><span data-stu-id="41f25-119">If prompted, follow the authorization instructions.</span></span>
    5. <span data-ttu-id="41f25-120">Введите имя и описание репозитория.</span><span class="sxs-lookup"><span data-stu-id="41f25-120">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="41f25-121">Нажмите кнопку **ОК**, чтобы подтвердить новую запись репозитория.</span><span class="sxs-lookup"><span data-stu-id="41f25-121">Click **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="41f25-122">В сетке выберите новый репозиторий типа **LCS**.</span><span class="sxs-lookup"><span data-stu-id="41f25-122">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="41f25-123">Нажмите кнопку **Открыть** для просмотра списка конфигураций электронной отчетности для выбранного репозитория.</span><span class="sxs-lookup"><span data-stu-id="41f25-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="41f25-124">[![обновление-er-из-lcs-для-ms-создание-репозитория-lcs](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="41f25-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

7. <span data-ttu-id="41f25-125">В дереве конфигураций в левой области выберите требуемую конфигурацию электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="41f25-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8. <span data-ttu-id="41f25-126">На экспресс-вкладке **Версии** выберите требуемую версию выбранной конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="41f25-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="41f25-127">Нажмите кнопку **Импорт** для загрузки выбранной версии из LCS в текущий экземпляр.</span><span class="sxs-lookup"><span data-stu-id="41f25-127">Click **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="41f25-128">Кнопка **Импорт** недоступна для версий конфигурации электронной отчетности, которые уже установлены в текущем экземпляре.</span><span class="sxs-lookup"><span data-stu-id="41f25-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="41f25-129">[![обновление-er-из-lcs-для-ms-загрузка-конфигурации](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="41f25-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="41f25-130">В зависимости от параметров электронной отчетности конфигурации проверяются после импорта.</span><span class="sxs-lookup"><span data-stu-id="41f25-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="41f25-131">Возможно, вы получите уведомление об обнаруженных проблемах несоответствия.</span><span class="sxs-lookup"><span data-stu-id="41f25-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="41f25-132">Необходимо устранить эти проблемы перед использованием импортированной версии конфигурации.</span><span class="sxs-lookup"><span data-stu-id="41f25-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="41f25-133">Дополнительные сведения см. в списке связанных статей для этого раздела.</span><span class="sxs-lookup"><span data-stu-id="41f25-133">For more information, see the list of related articles for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="41f25-134">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="41f25-134">Additional resources</span></span>

[<span data-ttu-id="41f25-135">Обзор электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="41f25-135">Electronic reporting overview</span></span>](general-electronic-reporting.md)
