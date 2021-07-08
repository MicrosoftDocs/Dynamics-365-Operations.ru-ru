---
title: Отправка конфигурации в Lifecycle Services
description: В этом разделе описывается, как создать новую конфигурацию электронной отчетности (ER) и отправить ее в Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41a8fcf2592bde4901aba703e0cd124b1155dac6
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270567"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="f28a9-103">Отправка конфигурации в Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="f28a9-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f28a9-104">В этой теме поясняется, как пользователь с ролью системного администратора или разработчика электронной отчетности может создать новую [конфигурацию электронной отчетности (ER)](../general-electronic-reporting.md#Configuration) и отправить ее в [библиотеку ресурсов уровня проекта](../../lifecycle-services/asset-library.md) в Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f28a9-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f28a9-105">Использование LCS в качестве репозитория для конфигураций ER [устаревает](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="f28a9-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="f28a9-106">Дополнительные сведения см. в [Regulatory Configuration Service (RCS) — устаревание хранилища Lifecycle Services (LCS)](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="f28a9-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="f28a9-107">В этом примере вам предстоит создать конфигурацию и отправить ее в LCS для демонстрационной компании под названием Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку конфигурации электронной отчетности являются общими для всех компаний.</span><span class="sxs-lookup"><span data-stu-id="f28a9-107">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="f28a9-108">Для выполнения этих шагов необходимо сначала выполнить шаги в теме [Создание поставщиков конфигурации и установка их в качестве активных](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f28a9-108">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="f28a9-109">Также требуется доступ к LCS.</span><span class="sxs-lookup"><span data-stu-id="f28a9-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="f28a9-110">Войдите в приложение с помощью одной из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="f28a9-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="f28a9-111">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="f28a9-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="f28a9-112">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="f28a9-112">System administrator</span></span>

2. <span data-ttu-id="f28a9-113">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="f28a9-114">Выберите компанию **Litware, Inc.** и пометьте ее как **Активная**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-114">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="f28a9-115">Выберите **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-115">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="f28a9-116">Убедитесь, что текущий пользователь Dynamics 365 Finance является членом проекта LCS, который содержит [библиотеку активов](../../lifecycle-services/asset-library.md#asset-library-support), которая используется, чтобы импортировать конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="f28a9-116">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="f28a9-117">Невозможно получить доступ к проекту LCS из репозитория электронной отчетности, который представляет другой домен, отличный от домена, используемого в Finance.</span><span class="sxs-lookup"><span data-stu-id="f28a9-117">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="f28a9-118">При попытке будет отображен пустой список проектов LCS, и вы не сможете импортировать конфигурации электронной отчетности из библиотеки активов уровня проекта в LCS.</span><span class="sxs-lookup"><span data-stu-id="f28a9-118">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="f28a9-119">Чтобы получить доступ к библиотекам активов уровня проекта из репозитория электронной отчетности, который используется для импорта конфигураций электронной отчетности, выполните вход в Finance, используя учетные данные пользователя, принадлежащего к клиенту (домену), для которого была выполнена подготовка текущего экземпляра Finance.</span><span class="sxs-lookup"><span data-stu-id="f28a9-119">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="f28a9-120">Создать новой конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="f28a9-120">Create a new data model configuration</span></span>

1. <span data-ttu-id="f28a9-121">Перейдите в раздел **Управление организацией \> Электронная отчетность \> Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-121">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f28a9-122">На странице **Конфигурации** выберите **Создать конфигурацию**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f28a9-122">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="f28a9-123">В этом примере вам предстоит создать конфигурацию, которая содержит пример модели данных для электронных документов.</span><span class="sxs-lookup"><span data-stu-id="f28a9-123">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="f28a9-124">Эта конфигурация модели данных будет отправлена в LCS позже.</span><span class="sxs-lookup"><span data-stu-id="f28a9-124">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="f28a9-125">В поле **Имя** введите **Пример конфигурации модели**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-125">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="f28a9-126">В поле **Описание** введите **Пример конфигурации модели**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-126">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="f28a9-127">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-127">Select **Create configuration**.</span></span>
6. <span data-ttu-id="f28a9-128">Выберите **Конструктор моделей**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-128">Select **Model designer**.</span></span>
7. <span data-ttu-id="f28a9-129">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-129">Select **New**.</span></span>
8. <span data-ttu-id="f28a9-130">В поле **Имя** введите **Точка входа**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-130">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="f28a9-131">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-131">Select **Add**.</span></span>
10. <span data-ttu-id="f28a9-132">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-132">Select **Save**.</span></span>
11. <span data-ttu-id="f28a9-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f28a9-133">Close the page.</span></span>
12. <span data-ttu-id="f28a9-134">Выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-134">Select **Change status**.</span></span>
13. <span data-ttu-id="f28a9-135">Выберите **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-135">Select **Complete**.</span></span>
14. <span data-ttu-id="f28a9-136">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-136">Select **OK**.</span></span>
15. <span data-ttu-id="f28a9-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f28a9-137">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="f28a9-138">Регистрация нового репозитория</span><span class="sxs-lookup"><span data-stu-id="f28a9-138">Register a new repository</span></span>

1. <span data-ttu-id="f28a9-139">Перейдите в раздел **Управление организацией \> Рабочие области \> Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-139">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="f28a9-140">В разделе **Поставщики конфигурации** выберите плитку **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="f28a9-140">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="f28a9-141">На плитке **Litware, Inc.** выберите **Репозитории**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-141">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="f28a9-142">Теперь можно открыть список репозиториев для поставщика конфигурации Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="f28a9-142">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="f28a9-143">Выберите **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f28a9-143">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="f28a9-144">Теперь можно добавить новый репозиторий.</span><span class="sxs-lookup"><span data-stu-id="f28a9-144">You can now add a new repository.</span></span>

5. <span data-ttu-id="f28a9-145">В поле **Тип репозитория конфигурации** выберите **LCS**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-145">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="f28a9-146">Выберите **Создать репозиторий**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-146">Select **Create repository**.</span></span>
7. <span data-ttu-id="f28a9-147">В поле **Проект** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f28a9-147">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="f28a9-148">В данном примере выберите требуемый вариант LCS.</span><span class="sxs-lookup"><span data-stu-id="f28a9-148">For this example, select the desired LCS project.</span></span> <span data-ttu-id="f28a9-149">Вы должны иметь [доступ](#accessconditions) к проекту.</span><span class="sxs-lookup"><span data-stu-id="f28a9-149">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="f28a9-150">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-150">Select **OK**.</span></span>

    <span data-ttu-id="f28a9-151">Заполните новую запись репозитория.</span><span class="sxs-lookup"><span data-stu-id="f28a9-151">Complete a new repository entry.</span></span>

9. <span data-ttu-id="f28a9-152">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="f28a9-152">In the list, mark the selected row.</span></span>

    <span data-ttu-id="f28a9-153">В данном примере выберите запись репозитория **LCS**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-153">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="f28a9-154">Обратите внимание, что зарегистрированный репозиторий помечается текущим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="f28a9-154">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="f28a9-155">Другими словами, в этот репозиторий можно поместить только конфигурации, принадлежащие данному поставщику, и, следовательно, отправить их в выбранный проект LCS.</span><span class="sxs-lookup"><span data-stu-id="f28a9-155">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="f28a9-156">Выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-156">Select **Open**.</span></span>

    <span data-ttu-id="f28a9-157">Вы открываете репозиторий для просмотра списка конфигураций электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="f28a9-157">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="f28a9-158">Если выбранный проект еще не использовался для совместного использования конфигураций электронной отчетности, список будет пустым.</span><span class="sxs-lookup"><span data-stu-id="f28a9-158">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="f28a9-159">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f28a9-159">Close the page.</span></span>
12. <span data-ttu-id="f28a9-160">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f28a9-160">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="f28a9-161">Отправка конфигурации в LCS</span><span class="sxs-lookup"><span data-stu-id="f28a9-161">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="f28a9-162">Перейдите в раздел **Управление организацией \> Электронная отчетность \> Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-162">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f28a9-163">На странице **Конфигурации** в дереве конфигураций выберите пункт **Пример конфигурации модели**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-163">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="f28a9-164">Вы должны выбрать созданную конфигурацию, которая уже завершена.</span><span class="sxs-lookup"><span data-stu-id="f28a9-164">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="f28a9-165">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="f28a9-165">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="f28a9-166">Для этого примера выберите версию выбранной конфигурации со статусом **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-166">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="f28a9-167">Выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-167">Select **Change status**.</span></span>
5. <span data-ttu-id="f28a9-168">Выберите **Поделиться**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-168">Select **Share**.</span></span>

    <span data-ttu-id="f28a9-169">Статус конфигурации изменяется с **Завершено** на **Общие**, когда конфигурация публикуется в LCS.</span><span class="sxs-lookup"><span data-stu-id="f28a9-169">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="f28a9-170">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-170">Select **OK**.</span></span>
7. <span data-ttu-id="f28a9-171">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="f28a9-171">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="f28a9-172">Для этого примера выберите версию конфигурации со статусом **Общие**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-172">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="f28a9-173">Обратите внимание, что статус выбранной версии изменился с **Завершено** на **Общие**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-173">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="f28a9-174">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f28a9-174">Close the page.</span></span>
9. <span data-ttu-id="f28a9-175">Выберите **Репозитории**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-175">Select **Repositories**.</span></span>

    <span data-ttu-id="f28a9-176">Теперь можно открыть список репозиториев для поставщика конфигурации Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="f28a9-176">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="f28a9-177">Выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-177">Select **Open**.</span></span>

    <span data-ttu-id="f28a9-178">В данном примере выберите репозиторий **LCS** и откройте его.</span><span class="sxs-lookup"><span data-stu-id="f28a9-178">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="f28a9-179">Обратите внимание, что выбранная конфигурация отображается как актив выбранного проекта LCS.</span><span class="sxs-lookup"><span data-stu-id="f28a9-179">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="f28a9-180">Откройте LCS, перейдя на <https://lcs.dynamics.com>.</span><span class="sxs-lookup"><span data-stu-id="f28a9-180">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="f28a9-181">Откройте проект, который использовался ранее для регистрации репозитория.</span><span class="sxs-lookup"><span data-stu-id="f28a9-181">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="f28a9-182">Откройте библиотеку активов проекта.</span><span class="sxs-lookup"><span data-stu-id="f28a9-182">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="f28a9-183">Выберите тип актива **Конфигурация GER**.</span><span class="sxs-lookup"><span data-stu-id="f28a9-183">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="f28a9-184">В списке должна быть указана отправленная вами конфигурация электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="f28a9-184">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="f28a9-185">Обратите внимание, что отправленную конфигурацию LCS можно импортировать в другой экземпляр, если поставщики имеют доступ к этому проекту LCS.</span><span class="sxs-lookup"><span data-stu-id="f28a9-185">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
