---
title: Отправка конфигурации в Lifecycle Services
description: В этой теме поясняется, как пользователь с ролью системного администратора или разработчика электронной отчетности может создать новую конфигурацию электронной отчетности (ER) и отправить ее в Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c43bad3ee2530a454de718a0a7da4d1e468a4af4
ms.sourcegitcommit: 9857d5cbdc0ab2fc9db049ac5ad118fc2b29bedc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/14/2020
ms.locfileid: "3810699"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="8997f-103">Отправка конфигурации в Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="8997f-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8997f-104">В этой теме поясняется, как пользователь с ролью системного администратора или разработчика электронной отчетности может создать новую [конфигурацию электронной отчетности (ER)](../general-electronic-reporting.md#Configuration) и отправить ее в [библиотеку ресурсов уровня проекта](../../lifecycle-services/asset-library.md) в Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="8997f-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="8997f-105">В этом примере вам предстоит создать конфигурацию и отправить ее в LCS для демонстрационной компании под названием Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку конфигурации электронной отчетности являются общими для всех компаний.</span><span class="sxs-lookup"><span data-stu-id="8997f-105">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="8997f-106">Для выполнения этих шагов необходимо сначала выполнить шаги в теме [Создание поставщиков конфигурации и установка их в качестве активных](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="8997f-106">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="8997f-107">Также требуется доступ к LCS.</span><span class="sxs-lookup"><span data-stu-id="8997f-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="8997f-108">Войдите в приложение с помощью одной из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="8997f-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="8997f-109">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="8997f-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="8997f-110">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="8997f-110">System administrator</span></span>

2. <span data-ttu-id="8997f-111">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="8997f-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="8997f-112">Выберите компанию **Litware, Inc.** и пометьте ее как **Активная**.</span><span class="sxs-lookup"><span data-stu-id="8997f-112">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="8997f-113">Выберите **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="8997f-113">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="8997f-114">Убедитесь, что текущий пользователь Dynamics 365 Finance является членом проекта LCS, который содержит [библиотеку активов](../../lifecycle-services/asset-library.md#asset-library-support), которая используется, чтобы импортировать конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="8997f-114">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="8997f-115">Невозможно получить доступ к проекту LCS из репозитория электронной отчетности, который представляет другой домен, отличный от домена, используемого в Finance.</span><span class="sxs-lookup"><span data-stu-id="8997f-115">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="8997f-116">При попытке будет отображен пустой список проектов LCS, и вы не сможете импортировать конфигурации электронной отчетности из библиотеки активов уровня проекта в LCS.</span><span class="sxs-lookup"><span data-stu-id="8997f-116">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="8997f-117">Чтобы получить доступ к библиотекам активов уровня проекта из репозитория электронной отчетности, который используется для импорта конфигураций электронной отчетности, выполните вход в Finance, используя учетные данные пользователя, принадлежащего к клиенту (домену), для которого была выполнена подготовка текущего экземпляра Finance.</span><span class="sxs-lookup"><span data-stu-id="8997f-117">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="8997f-118">Создать новой конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="8997f-118">Create a new data model configuration</span></span>

1. <span data-ttu-id="8997f-119">Перейдите в раздел **Управление организацией \> Электронная отчетность \> Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="8997f-119">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="8997f-120">На странице **Конфигурации** выберите **Создать конфигурацию**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8997f-120">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="8997f-121">В этом примере вам предстоит создать конфигурацию, которая содержит пример модели данных для электронных документов.</span><span class="sxs-lookup"><span data-stu-id="8997f-121">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="8997f-122">Эта конфигурация модели данных будет отправлена в LCS позже.</span><span class="sxs-lookup"><span data-stu-id="8997f-122">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="8997f-123">В поле **Имя** введите **Пример конфигурации модели**.</span><span class="sxs-lookup"><span data-stu-id="8997f-123">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="8997f-124">В поле **Описание** введите **Пример конфигурации модели**.</span><span class="sxs-lookup"><span data-stu-id="8997f-124">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="8997f-125">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="8997f-125">Select **Create configuration**.</span></span>
6. <span data-ttu-id="8997f-126">Выберите **Конструктор моделей**.</span><span class="sxs-lookup"><span data-stu-id="8997f-126">Select **Model designer**.</span></span>
7. <span data-ttu-id="8997f-127">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="8997f-127">Select **New**.</span></span>
8. <span data-ttu-id="8997f-128">В поле **Имя** введите **Точка входа**.</span><span class="sxs-lookup"><span data-stu-id="8997f-128">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="8997f-129">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="8997f-129">Select **Add**.</span></span>
10. <span data-ttu-id="8997f-130">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8997f-130">Select **Save**.</span></span>
11. <span data-ttu-id="8997f-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8997f-131">Close the page.</span></span>
12. <span data-ttu-id="8997f-132">Выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="8997f-132">Select **Change status**.</span></span>
13. <span data-ttu-id="8997f-133">Выберите **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="8997f-133">Select **Complete**.</span></span>
14. <span data-ttu-id="8997f-134">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8997f-134">Select **OK**.</span></span>
15. <span data-ttu-id="8997f-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8997f-135">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="8997f-136">Регистрация нового репозитория</span><span class="sxs-lookup"><span data-stu-id="8997f-136">Register a new repository</span></span>

1. <span data-ttu-id="8997f-137">Перейдите в раздел **Управление организацией \> Рабочие области \> Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="8997f-137">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="8997f-138">В разделе **Поставщики конфигурации** выберите плитку **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="8997f-138">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="8997f-139">На плитке **Litware, Inc.** выберите **Репозитории**.</span><span class="sxs-lookup"><span data-stu-id="8997f-139">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="8997f-140">Теперь можно открыть список репозиториев для поставщика конфигурации Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="8997f-140">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="8997f-141">Выберите **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8997f-141">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="8997f-142">Теперь можно добавить новый репозиторий.</span><span class="sxs-lookup"><span data-stu-id="8997f-142">You can now add a new repository.</span></span>

5. <span data-ttu-id="8997f-143">В поле **Тип репозитория конфигурации** выберите **LCS**.</span><span class="sxs-lookup"><span data-stu-id="8997f-143">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="8997f-144">Выберите **Создать репозиторий**.</span><span class="sxs-lookup"><span data-stu-id="8997f-144">Select **Create repository**.</span></span>
7. <span data-ttu-id="8997f-145">В поле **Проект** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8997f-145">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="8997f-146">В данном примере выберите требуемый вариант LCS.</span><span class="sxs-lookup"><span data-stu-id="8997f-146">For this example, select the desired LCS project.</span></span> <span data-ttu-id="8997f-147">Вы должны иметь [доступ](#accessconditions) к проекту.</span><span class="sxs-lookup"><span data-stu-id="8997f-147">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="8997f-148">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8997f-148">Select **OK**.</span></span>

    <span data-ttu-id="8997f-149">Заполните новую запись репозитория.</span><span class="sxs-lookup"><span data-stu-id="8997f-149">Complete a new repository entry.</span></span>

9. <span data-ttu-id="8997f-150">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="8997f-150">In the list, mark the selected row.</span></span>

    <span data-ttu-id="8997f-151">В данном примере выберите запись репозитория **LCS**.</span><span class="sxs-lookup"><span data-stu-id="8997f-151">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="8997f-152">Обратите внимание, что зарегистрированный репозиторий помечается текущим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="8997f-152">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="8997f-153">Другими словами, в этот репозиторий можно поместить только конфигурации, принадлежащие данному поставщику, и, следовательно, отправить их в выбранный проект LCS.</span><span class="sxs-lookup"><span data-stu-id="8997f-153">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="8997f-154">Выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="8997f-154">Select **Open**.</span></span>

    <span data-ttu-id="8997f-155">Вы открываете репозиторий для просмотра списка конфигураций электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="8997f-155">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="8997f-156">Если выбранный проект еще не использовался для совместного использования конфигураций электронной отчетности, список будет пустым.</span><span class="sxs-lookup"><span data-stu-id="8997f-156">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="8997f-157">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8997f-157">Close the page.</span></span>
12. <span data-ttu-id="8997f-158">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8997f-158">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="8997f-159">Отправка конфигурации в LCS</span><span class="sxs-lookup"><span data-stu-id="8997f-159">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="8997f-160">Перейдите в раздел **Управление организацией \> Электронная отчетность \> Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="8997f-160">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="8997f-161">На странице **Конфигурации** в дереве конфигураций выберите пункт **Пример конфигурации модели**.</span><span class="sxs-lookup"><span data-stu-id="8997f-161">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="8997f-162">Вы должны выбрать созданную конфигурацию, которая уже завершена.</span><span class="sxs-lookup"><span data-stu-id="8997f-162">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="8997f-163">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8997f-163">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="8997f-164">Для этого примера выберите версию выбранной конфигурации со статусом **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="8997f-164">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="8997f-165">Выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="8997f-165">Select **Change status**.</span></span>
5. <span data-ttu-id="8997f-166">Выберите **Поделиться**.</span><span class="sxs-lookup"><span data-stu-id="8997f-166">Select **Share**.</span></span>

    <span data-ttu-id="8997f-167">Статус конфигурации изменяется с **Завершено** на **Общие**, когда конфигурация публикуется в LCS.</span><span class="sxs-lookup"><span data-stu-id="8997f-167">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="8997f-168">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8997f-168">Select **OK**.</span></span>
7. <span data-ttu-id="8997f-169">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8997f-169">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="8997f-170">Для этого примера выберите версию конфигурации со статусом **Общие**.</span><span class="sxs-lookup"><span data-stu-id="8997f-170">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="8997f-171">Обратите внимание, что статус выбранной версии изменился с **Завершено** на **Общие**.</span><span class="sxs-lookup"><span data-stu-id="8997f-171">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="8997f-172">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8997f-172">Close the page.</span></span>
9. <span data-ttu-id="8997f-173">Выберите **Репозитории**.</span><span class="sxs-lookup"><span data-stu-id="8997f-173">Select **Repositories**.</span></span>

    <span data-ttu-id="8997f-174">Теперь можно открыть список репозиториев для поставщика конфигурации Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="8997f-174">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="8997f-175">Выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="8997f-175">Select **Open**.</span></span>

    <span data-ttu-id="8997f-176">В данном примере выберите репозиторий **LCS** и откройте его.</span><span class="sxs-lookup"><span data-stu-id="8997f-176">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="8997f-177">Обратите внимание, что выбранная конфигурация отображается как актив выбранного проекта LCS.</span><span class="sxs-lookup"><span data-stu-id="8997f-177">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="8997f-178">Откройте LCS, перейдя на <https://lcs.dynamics.com>.</span><span class="sxs-lookup"><span data-stu-id="8997f-178">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="8997f-179">Откройте проект, который использовался ранее для регистрации репозитория.</span><span class="sxs-lookup"><span data-stu-id="8997f-179">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="8997f-180">Откройте библиотеку активов проекта.</span><span class="sxs-lookup"><span data-stu-id="8997f-180">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="8997f-181">Выберите тип актива **Конфигурация GER**.</span><span class="sxs-lookup"><span data-stu-id="8997f-181">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="8997f-182">В списке должна быть указана отправленная вами конфигурация электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="8997f-182">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="8997f-183">Обратите внимание, что отправленную конфигурацию LCS можно импортировать в другой экземпляр, если поставщики имеют доступ к этому проекту LCS.</span><span class="sxs-lookup"><span data-stu-id="8997f-183">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>
