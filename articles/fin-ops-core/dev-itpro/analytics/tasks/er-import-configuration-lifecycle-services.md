---
title: Импорт конфигурации из Lifecycle Services
description: В этой теме описывается, как импортировать новую версию электронной отчетности (ER) из Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b58ecb8a7d6f52631dbca7642a4acbcf6ff895a3
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270845"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="ba32a-103">Импорт конфигурации из Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="ba32a-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ba32a-104">В этой теме поясняется, как пользователь с ролью системного администратора или разработчика электронной отчетности может импортировать новую версию [конфигурации электронной отчетности (ER)](../general-electronic-reporting.md#Configuration) из [библиотеки ресурсов уровня проекта](../../lifecycle-services/asset-library.md) в Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ba32a-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ba32a-105">Использование LCS в качестве репозитория для конфигураций ER [устаревает](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="ba32a-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="ba32a-106">Дополнительные сведения см. в [Regulatory Configuration Service (RCS) — устаревание хранилища Lifecycle Services (LCS)](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="ba32a-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="ba32a-107">В этом примере вам предстоит выбрать желаемую версию конфигурации электронной отчетности и импортировать ее для демонстрационной компании с названием Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку конфигурации электронной отчетности являются общими для всех компаний.</span><span class="sxs-lookup"><span data-stu-id="ba32a-107">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="ba32a-108">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре [Отправка конфигурации в Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="ba32a-108">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="ba32a-109">Также требуется доступ к LCS.</span><span class="sxs-lookup"><span data-stu-id="ba32a-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="ba32a-110">Войдите в приложение с помощью одной из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="ba32a-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="ba32a-111">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="ba32a-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="ba32a-112">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="ba32a-112">System administrator</span></span>

2. <span data-ttu-id="ba32a-113">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="ba32a-114">Выберите **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-114">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="ba32a-115">Убедитесь, что текущий пользователь Dynamics 365 Finance является членом проекта LCS, который содержит библиотеку активов, к которой пользователь хочет получить [доступ](../../lifecycle-services/asset-library.md#asset-library-support), чтобы импортировать конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="ba32a-115">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="ba32a-116">Невозможно получить доступ к проекту LCS из репозитория электронной отчетности, который представляет другой домен, отличный от домена, используемого в Finance.</span><span class="sxs-lookup"><span data-stu-id="ba32a-116">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="ba32a-117">При попытке будет отображен пустой список проектов LCS, и вы не сможете импортировать конфигурации электронной отчетности из библиотеки активов уровня проекта в LCS.</span><span class="sxs-lookup"><span data-stu-id="ba32a-117">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="ba32a-118">Чтобы получить доступ к библиотекам активов уровня проекта из репозитория электронной отчетности, который используется для импорта конфигураций электронной отчетности, выполните вход в Finance, используя учетные данные пользователя, принадлежащего к клиенту (домену), для которого была выполнена подготовка текущего экземпляра Finance.</span><span class="sxs-lookup"><span data-stu-id="ba32a-118">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="ba32a-119">Удаление общей версии конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="ba32a-119">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="ba32a-120">На странице **Конфигурации** в дереве конфигураций выберите пункт **Пример конфигурации модели**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-120">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="ba32a-121">Вы создали первую версию конфигурации примера модели данных и опубликовали ее в LCS, когда завершили шаги в разделе [Отправка конфигурации в Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="ba32a-121">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="ba32a-122">В этой процедуре мы удалим эту версию конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="ba32a-122">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="ba32a-123">Затем эту версию можно будет импортировать из LCS позже в этой теме.</span><span class="sxs-lookup"><span data-stu-id="ba32a-123">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="ba32a-124">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ba32a-124">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="ba32a-125">Для этого примера выберите версию этой конфигурации со статусом **Общие**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-125">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="ba32a-126">Этот статус указывает, что конфигурация была опубликована в LCS.</span><span class="sxs-lookup"><span data-stu-id="ba32a-126">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="ba32a-127">Выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-127">Select **Change status**.</span></span>
4. <span data-ttu-id="ba32a-128">Выберите **Отменить**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-128">Select **Discontinue**.</span></span>

    <span data-ttu-id="ba32a-129">Изменив статус выбранной версии с **Общее** на **Отменено**, можно сделать эту версию доступной для удаления.</span><span class="sxs-lookup"><span data-stu-id="ba32a-129">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="ba32a-130">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-130">Select **OK**.</span></span>
6. <span data-ttu-id="ba32a-131">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ba32a-131">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="ba32a-132">Для этого примера выберите версию этой конфигурации со статусом **Отменено**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-132">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="ba32a-133">Выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-133">Select **Delete**.</span></span>
8. <span data-ttu-id="ba32a-134">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-134">Select **Yes**.</span></span>

    <span data-ttu-id="ba32a-135">Обратите внимание, что теперь доступна только черновая версия 2 выбранной конфигурации модели данных.</span><span class="sxs-lookup"><span data-stu-id="ba32a-135">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="ba32a-136">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ba32a-136">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="ba32a-137">Импорт общей версии конфигурации модели данных из LCS</span><span class="sxs-lookup"><span data-stu-id="ba32a-137">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="ba32a-138">Перейдите в раздел **Управление организацией \> Рабочие области \> Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-138">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="ba32a-139">В разделе **Поставщики конфигурации** выберите плитку **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="ba32a-139">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="ba32a-140">На плитке **Litware, Inc.** выберите **Репозитории**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-140">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="ba32a-141">Теперь можно открыть список репозиториев для поставщика конфигурации Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="ba32a-141">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="ba32a-142">Выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-142">Select **Open**.</span></span>

    <span data-ttu-id="ba32a-143">В данном примере выберите репозиторий **LCS** и откройте его.</span><span class="sxs-lookup"><span data-stu-id="ba32a-143">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="ba32a-144">Необходимо иметь [доступ](#accessconditions) к проекту LCS и к библиотеке активов, доступ к которой осуществляется выбранным репозиторием электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="ba32a-144">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="ba32a-145">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="ba32a-145">In the list, mark the selected row.</span></span>

    <span data-ttu-id="ba32a-146">Для этого примера выберите первую версию **примера конфигурации модели** в списке версий.</span><span class="sxs-lookup"><span data-stu-id="ba32a-146">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="ba32a-147">Выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-147">Select **Import**.</span></span>
7. <span data-ttu-id="ba32a-148">Выберите **Да**, чтобы подтвердить импорт выбранной версии из LCS.</span><span class="sxs-lookup"><span data-stu-id="ba32a-148">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="ba32a-149">Информационное сообщение подтверждает, что выбранная версия была успешно импортирована.</span><span class="sxs-lookup"><span data-stu-id="ba32a-149">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="ba32a-150">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ba32a-150">Close the page.</span></span>
9. <span data-ttu-id="ba32a-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ba32a-151">Close the page.</span></span>
10. <span data-ttu-id="ba32a-152">Выберите **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-152">Select **Configurations**.</span></span>
11. <span data-ttu-id="ba32a-153">В дереве выберите **Пример конфигурации модели**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-153">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="ba32a-154">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ba32a-154">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="ba32a-155">Для этого примера выберите версию этой конфигурации со статусом **Общие**.</span><span class="sxs-lookup"><span data-stu-id="ba32a-155">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="ba32a-156">Обратите внимание, что общая версия 1 выбранной конфигурации модели данных теперь также доступна.</span><span class="sxs-lookup"><span data-stu-id="ba32a-156">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
