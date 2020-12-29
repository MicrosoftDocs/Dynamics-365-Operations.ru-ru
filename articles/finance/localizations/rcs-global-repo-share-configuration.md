---
title: Совместное использование конфигураций ER в RCS/глобальном репозитории с внешними организациями
description: В этом разделе объясняется, как совместно использовать конфигурацию электронной отчетности (ER) в Microsoft Regulatory Configuration Service (RCS)/глобальном репозитории непосредственно с внешними организациями.
author: JaneA07
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 04c46824123906eccbfff18a03974c8043729e0a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447262"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="b985a-103">Совместно использовать конфигурацию электронной отчетности (ER) в глобальном репозитории Regulatory Configuration Service (RCS) с внешними организациями.</span><span class="sxs-lookup"><span data-stu-id="b985a-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b985a-104">Можно использовать службы Microsoft Payment Configuration Services (RCS) для совместного использования конфигураций электронной отчетности (ER), а затем опубликовать их в внешних организациях.</span><span class="sxs-lookup"><span data-stu-id="b985a-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="b985a-105">Следующие процедуры показывают, как пользователь RCS может совместно использовать версию конфигурации ER, которая была настроена в экземпляре RCS с внешней организацией.</span><span class="sxs-lookup"><span data-stu-id="b985a-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="b985a-106">Перед окончанием выполнения этих процедур необходимо выполнить следующие необходимые условия:</span><span class="sxs-lookup"><span data-stu-id="b985a-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="b985a-107">Доступ к экземпляру RCS.</span><span class="sxs-lookup"><span data-stu-id="b985a-107">Access an RCS instance.</span></span>
- <span data-ttu-id="b985a-108">Создание активного поставщика конфигураций.</span><span class="sxs-lookup"><span data-stu-id="b985a-108">Create an active configuration provider.</span></span> <span data-ttu-id="b985a-109">Дополнительные сведения см. в [Создание поставщиков конфигураций и пометка их как активных](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="b985a-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="b985a-110">Создайте и загрузите новую версию конфигурации ER.</span><span class="sxs-lookup"><span data-stu-id="b985a-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="b985a-111">Дополнительные сведения см. в разделе [Создание и загрузка новой версии электронной отчетности (ER)](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="b985a-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="b985a-112">Кроме того, необходимо убедиться, что среда RCS подготовлена для вашей компании.</span><span class="sxs-lookup"><span data-stu-id="b985a-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="b985a-113">В приложении Finance and Operations перейдите к **Администрирование организации** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="b985a-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="b985a-114">Если у вашей компании нет среды RCS, щелкните **Regulatory Services — внешняя конфигурация** и следуйте инструкциям по подготовке среды.</span><span class="sxs-lookup"><span data-stu-id="b985a-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="b985a-115">Если среда RCS уже подготовлена для вашей компании, воспользуйтесь URL-адресом страницы для доступа к ней, выбрав параметр входа.</span><span class="sxs-lookup"><span data-stu-id="b985a-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="b985a-116">Проверьте конфигурацию, к которой необходимо предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="b985a-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="b985a-117">Выполните следующие действия, чтобы убедиться, что конфигурация, которую вы хотите использовать, уже была загружена в глобальном репозитории.</span><span class="sxs-lookup"><span data-stu-id="b985a-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="b985a-118">В рабочей области **электронной отчетности** выберите **репозитории** для поставщика конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b985a-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![Поставщики конфигурации](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="b985a-120">Выберите **Глобальный репозиторий** \> **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="b985a-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="b985a-121">Выполните поиск конфигурацию, к которой необходимо предоставить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="b985a-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="b985a-122">Чтобы уточнить поиск, можно использовать поля фильтра.</span><span class="sxs-lookup"><span data-stu-id="b985a-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="b985a-123">Если не удается найти конфигурацию в глобальном репозитории, выполните шаги в [Создание и загрузка новой версии электронной отчетности (ER)](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="b985a-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="b985a-124">Совместное использование конфигураций ER с внешними организациями</span><span class="sxs-lookup"><span data-stu-id="b985a-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="b985a-125">После создания конфигурации под поставщиком конфигураций ее можно использовать непосредственно с внешними организациями, используя экспресс-вкладку **совместно с** на странице **глобального репозитория конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="b985a-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="b985a-126">В рабочей области **электронной отчетности** выберите **репозитории** для поставщика конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b985a-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="b985a-127">Выберите **Глобальный репозиторий** \> **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="b985a-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="b985a-128">Выберите конфигурацию, к которой необходимо предоставить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="b985a-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="b985a-129">На экспресс-вкладке **совместно с** выберите **организация**.</span><span class="sxs-lookup"><span data-stu-id="b985a-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![Экспресс-вкладка "совместно с"](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="b985a-131">В диалоговом окне введите имя домена для внешней организации, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b985a-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![Диалоговое окно Поделиться версией конфигурации с внешней организацией](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="b985a-133">Конфигурация используется совместно с внешней организацией и доступна для данной организации в глобальном репозитории.</span><span class="sxs-lookup"><span data-stu-id="b985a-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="b985a-134">Здесь можно импортировать ее в экземпляр RCS организации или в экземпляры приложений Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b985a-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

![Конфигурация используется совместно с внешней организацией](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_test.com)

6. <span data-ttu-id="b985a-136">Чтобы отменить общий доступ к конфигурации, который ранее был предоставлен для внешней организации, выберите конфигурацию и щелкните **Отмена общего доступа**, а затем нажмите кнопку **OK**</span><span class="sxs-lookup"><span data-stu-id="b985a-136">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>
