---
title: Создание конфигураций ER в RCS и их загрузка в глобальный репозиторий
description: В этом разделе объясняется, как создать конфигурацию электронной отчетности (ER) в Microsoft Regulatory Configuration Service (RCS) и загрузить ее в глобальный репозиторий.
author: JaneA07
manager: AnnBe
ms.date: 05/05/2020
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
ms.openlocfilehash: 0e194a8b777f984412d81e315f92ab4bb8a3b0c9
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371265"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="7f8b8-103">Создание конфигураций ER в Regulatory Configuration Service (RCS) и их загрузка в глобальный репозиторий</span><span class="sxs-lookup"><span data-stu-id="7f8b8-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f8b8-104">Можно использовать службы Microsoft Payment Configuration Services (RCS) для проектирования конфигураций электронной отчетности (ER), а затем опубликовать их, так что они могут быть использованы в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="7f8b8-105">Следующие процедуры показывают, как пользователь в роли "системный администратор" или "разработчик электронной отчетности" может создать производную версию конфигурации ER, которая была настроена в экземпляре RCS, а затем загрузить производную конфигурацию в глобальный репозиторий.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="7f8b8-106">Перед окончанием выполнения этих процедур необходимо выполнить следующие необходимые условия:</span><span class="sxs-lookup"><span data-stu-id="7f8b8-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="7f8b8-107">Доступ к экземпляру RCS.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-107">Access an RCS instance.</span></span>
- <span data-ttu-id="7f8b8-108">Создание активного поставщика конфигураций.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-108">Create an active configuration provider.</span></span> <span data-ttu-id="7f8b8-109">Дополнительные сведения см. в [Создание поставщиков конфигураций и пометка их как активных](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="7f8b8-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="7f8b8-110">Кроме того, необходимо убедиться, что среда RCS подготовлена для вашей компании.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="7f8b8-111">В приложении Finance and Operations перейдите к **Администрирование организации** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7f8b8-112">Если у вашей компании нет среды RCS, щелкните **Regulatory Services — внешняя конфигурация** и следуйте инструкциям по подготовке среды.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="7f8b8-113">Если среда RCS уже подготовлена для вашей компании, воспользуйтесь URL-адресом страницы для доступа к ней, выбрав параметр входа.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="7f8b8-114">Создание производной версии конфигурации в RCS</span><span class="sxs-lookup"><span data-stu-id="7f8b8-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="7f8b8-115">В рабочей области **электронной отчетности** убедитесь, что у вас есть активный поставщик конфигурации для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="7f8b8-116">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="7f8b8-117">Выбор конфигурации, с которой требуется создать новую версию.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="7f8b8-118">Чтобы уточнить поиск, можно использовать поля фильтра выше представления дерева.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="7f8b8-119">Выберите **создать конфигурацию** \> **Производное от имени**.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="7f8b8-120">Введите имя и описание, а затем выберите **создать конфигурацию**, чтобы создать новую производную версию.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="7f8b8-121">Выберите вновь производную конфигурацию, добавьте описание версии, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="7f8b8-122">Статус конфигурации изменится на **завершено**.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-122">The status of the configuration to is changed to **Completed**.</span></span>

![Новая версия конфигурации в RCS](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="7f8b8-124">При изменении статуса конфигурации может быть получено сообщение об ошибке проверки, относящееся к связанным приложениям.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="7f8b8-125">Чтобы отключить проверку, на панели операций на вкладке **конфигурации** выберите **пользовательские параметры**, а затем установите параметр **Пропустить проверку при изменении и повторном размещении статуса конфигурации** на **Да**.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="7f8b8-126">Отправка конфигурации в глобальный репозиторий</span><span class="sxs-lookup"><span data-stu-id="7f8b8-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="7f8b8-127">Для совместного использования новой или производной конфигурации с организацией можно загрузить ее в глобальный репозиторий.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="7f8b8-128">Выберите завершенную версию конфигурации, а затем выберите команду **загрузить в репозиторий**.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="7f8b8-129">Выберите параметр **Глобальная (Microsoft)**, а затем выберите команду **загрузить**.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Параметры отправки в репозиторий](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="7f8b8-131">В диалоговом окне подтверждения выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="7f8b8-132">Обновите описание версии, если необходимо, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="7f8b8-133">Статус конфигурации обновляется на **Поделиться**, а конфигурация загружается в глобальный репозиторий.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="7f8b8-134">Отсюда можно работать следующими способами:</span><span class="sxs-lookup"><span data-stu-id="7f8b8-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="7f8b8-135">Импортируйте его в экземпляр Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7f8b8-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="7f8b8-136">Дополнительные сведения см. в разделе [(Электронная отчетность) Импорт конфигураций из RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="7f8b8-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="7f8b8-137">Чтобы поделиться ею с третьей стороной или внешней организацией, см. раздел [RCS Совместно использовать конфигурации электронной отчетности (ER) с внешними организациями](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="7f8b8-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span></span>

![Производная версия конфигурации Интрастат Contoso в глобальном репозитории](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Config_upload_GlobalRepo.JPG)
