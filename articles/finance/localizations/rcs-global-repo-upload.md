---
title: Создание конфигураций ER в RCS и их загрузка в глобальный репозиторий
description: В этом разделе объясняется, как создать конфигурацию электронной отчетности (ER) в Microsoft Regulatory Configuration Service (RCS) и загрузить ее в глобальный репозиторий.
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ef12c911c8953b181db1c0eff0874a3d8cfcb3da
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005756"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="b6539-103">Создание конфигураций ER в Regulatory Configuration Service (RCS) и их загрузка в глобальный репозиторий</span><span class="sxs-lookup"><span data-stu-id="b6539-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6539-104">Можно использовать службы Microsoft Payment Configuration Services (RCS) для проектирования конфигураций электронной отчетности (ER), а затем опубликовать их, так что они могут быть использованы в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="b6539-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="b6539-105">Следующие процедуры показывают, как пользователь в роли "системный администратор" или "разработчик электронной отчетности" может создать производную версию конфигурации ER, которая была настроена в экземпляре RCS, а затем загрузить производную конфигурацию в глобальный репозиторий.</span><span class="sxs-lookup"><span data-stu-id="b6539-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="b6539-106">Перед окончанием выполнения этих процедур необходимо выполнить следующие необходимые условия:</span><span class="sxs-lookup"><span data-stu-id="b6539-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="b6539-107">Доступ к экземпляру RCS.</span><span class="sxs-lookup"><span data-stu-id="b6539-107">Access an RCS instance.</span></span>
- <span data-ttu-id="b6539-108">Создание активного поставщика конфигураций.</span><span class="sxs-lookup"><span data-stu-id="b6539-108">Create an active configuration provider.</span></span> <span data-ttu-id="b6539-109">Дополнительные сведения см. в [Создание поставщиков конфигураций и пометка их как активных](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="b6539-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="b6539-110">Кроме того, необходимо убедиться, что среда RCS подготовлена для вашей компании.</span><span class="sxs-lookup"><span data-stu-id="b6539-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="b6539-111">В приложении Finance and Operations перейдите к **Администрирование организации** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="b6539-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="b6539-112">Если у вашей компании нет среды RCS, щелкните **Regulatory Services — внешняя конфигурация** и следуйте инструкциям по подготовке среды.</span><span class="sxs-lookup"><span data-stu-id="b6539-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="b6539-113">Если среда RCS уже подготовлена для вашей компании, воспользуйтесь URL-адресом страницы для доступа к ней, выбрав параметр входа.</span><span class="sxs-lookup"><span data-stu-id="b6539-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="b6539-114">Создание производной версии конфигурации в RCS</span><span class="sxs-lookup"><span data-stu-id="b6539-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="b6539-115">В рабочей области **электронной отчетности** убедитесь, что у вас есть активный поставщик конфигурации для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="b6539-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="b6539-116">Выберите **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="b6539-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="b6539-117">Выбор конфигурации, с которой требуется создать новую версию.</span><span class="sxs-lookup"><span data-stu-id="b6539-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="b6539-118">Чтобы уточнить поиск, можно использовать поля фильтра выше представления дерева.</span><span class="sxs-lookup"><span data-stu-id="b6539-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="b6539-119">Выберите **создать конфигурацию** \> **Производное от имени**.</span><span class="sxs-lookup"><span data-stu-id="b6539-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="b6539-120">Введите имя и описание, а затем выберите **создать конфигурацию**, чтобы создать новую производную версию.</span><span class="sxs-lookup"><span data-stu-id="b6539-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="b6539-121">Выберите вновь производную конфигурацию, добавьте описание версии, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b6539-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="b6539-122">Статус конфигурации изменится на **завершено**.</span><span class="sxs-lookup"><span data-stu-id="b6539-122">The status of the configuration to is changed to **Completed**.</span></span>

![Новая версия конфигурации в RCS](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="b6539-124">При изменении статуса конфигурации может быть получено сообщение об ошибке проверки, относящееся к связанным приложениям.</span><span class="sxs-lookup"><span data-stu-id="b6539-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="b6539-125">Чтобы отключить проверку, на панели операций на вкладке **конфигурации** выберите **пользовательские параметры**, а затем установите параметр **Пропустить проверку при изменении и повторном размещении статуса конфигурации** на **Да**.</span><span class="sxs-lookup"><span data-stu-id="b6539-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="b6539-126">Отправка конфигурации в глобальный репозиторий</span><span class="sxs-lookup"><span data-stu-id="b6539-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="b6539-127">Для совместного использования новой или производной конфигурации с организацией можно загрузить ее в глобальный репозиторий.</span><span class="sxs-lookup"><span data-stu-id="b6539-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="b6539-128">Выберите завершенную версию конфигурации, а затем выберите команду **загрузить в репозиторий**.</span><span class="sxs-lookup"><span data-stu-id="b6539-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="b6539-129">Выберите параметр **Глобальная (Microsoft)**, а затем выберите команду **загрузить**.</span><span class="sxs-lookup"><span data-stu-id="b6539-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Параметры отправки в репозиторий](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="b6539-131">В диалоговом окне подтверждения выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="b6539-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="b6539-132">Обновите описание версии, если необходимо, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b6539-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="b6539-133">Статус конфигурации обновляется на **Поделиться**, а конфигурация загружается в глобальный репозиторий.</span><span class="sxs-lookup"><span data-stu-id="b6539-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="b6539-134">Отсюда можно работать следующими способами:</span><span class="sxs-lookup"><span data-stu-id="b6539-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="b6539-135">Импортируйте его в экземпляр Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b6539-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="b6539-136">Дополнительные сведения см. в разделе [(Электронная отчетность) Импорт конфигураций из RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="b6539-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="b6539-137">Чтобы поделиться ею с третьей стороной или внешней организацией, см. раздел [RCS Совместно использовать конфигурации электронной отчетности (ER) с внешними организациями](rcs-global-repo-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="b6539-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](rcs-global-repo-share-configuration.md)</span></span>

    ![Производная версия конфигурации Интрастат Contoso в глобальном репозитории](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a><span data-ttu-id="b6539-139">Удаление конфигурации из глобального репозитория</span><span class="sxs-lookup"><span data-stu-id="b6539-139">Delete a configuration from the Global repository</span></span>
<span data-ttu-id="b6539-140">Выполните следующие шаги, чтобы удалить конфигурацию, созданную вашей организацией.</span><span class="sxs-lookup"><span data-stu-id="b6539-140">Complete the following steps to delete a configuration that your organization has created.</span></span>

1. <span data-ttu-id="b6539-141">В рабочей области **Электронная отчетность** убедитесь, что ваш поставщик конфигурации **Активен**.</span><span class="sxs-lookup"><span data-stu-id="b6539-141">In the **Electronic reporting** workspace, verify that your configuration provider is **Active**.</span></span> <span data-ttu-id="b6539-142">Дополнительные сведения см. в [Создание поставщиков конфигураций и пометка их как активных](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="b6539-142">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
2. <span data-ttu-id="b6539-143">В активном поставщике конфигурации выберите **репозиторий**.</span><span class="sxs-lookup"><span data-stu-id="b6539-143">On your active configuration provider, select **repository**.</span></span>
3. <span data-ttu-id="b6539-144">Выберите тип репозитория **Глобальный** и выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="b6539-144">Select the repository type **Global**, and select **Open**.</span></span>
4. <span data-ttu-id="b6539-145">На экспресс-вкладке **Фильтр** найдите конфигурацию, которую необходимо удалить, используя функцию **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="b6539-145">On the **Filter** FastTab, find the configuration that you want to delete by using the **Filter** functionality.</span></span>
5. <span data-ttu-id="b6539-146">На экспресс-вкладке **Версия** выберите версию конфигурации, которую необходимо удалить, затем выберите **Удалить**:</span><span class="sxs-lookup"><span data-stu-id="b6539-146">On the **Version** FastTab, select the version of the configuration that you want to delete, and then select **Delete**:</span></span>

    ![Удаление конфигурации из глобального репозитория](media/RCS_Delete_from_GlobalRepo.JPG)

6. <span data-ttu-id="b6539-148">В диалоговом окне подтверждения выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="b6539-148">In the confirmation message box, select **Yes**.</span></span>

    ![Сообщение подтверждения удаления версии конфигурации](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
<span data-ttu-id="b6539-150">Версия конфигурации удаляется, и выводится подтверждающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="b6539-150">The configuration version is deleted, and confirmation message is shown.</span></span> 

> [!NOTE]
> <span data-ttu-id="b6539-151">Конфигурации могут быть удалены только тем поставщиком конфигурации, который их создал.</span><span class="sxs-lookup"><span data-stu-id="b6539-151">Configurations can only be deleted by the Configuration provider that created them.</span></span> <span data-ttu-id="b6539-152">Если конфигурация использовалась совместно с другой организацией, перед удалением этой конфигурации ее необходимо будет удалить из общего доступа.</span><span class="sxs-lookup"><span data-stu-id="b6539-152">If the configuration has been shared with another organization, the configuration will need to be unshared before you delete it.</span></span>
 
