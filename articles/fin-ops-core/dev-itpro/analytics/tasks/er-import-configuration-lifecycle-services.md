---
title: Импорт конфигурации из Lifecycle Services
description: В этой теме описывается, как импортировать новую версию электронной отчетности (ER) из Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 09/14/2020
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
ms.openlocfilehash: 674d0dc02b4a53e455a15a06fdb7f24ca3036ba3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752372"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="e67d9-103">Импорт конфигурации из Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="e67d9-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e67d9-104">В этой теме поясняется, как пользователь с ролью системного администратора или разработчика электронной отчетности может импортировать новую версию [конфигурации электронной отчетности (ER)](../general-electronic-reporting.md#Configuration) из [библиотеки ресурсов уровня проекта](../../lifecycle-services/asset-library.md) в Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e67d9-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="e67d9-105">В этом примере вам предстоит выбрать желаемую версию конфигурации электронной отчетности и импортировать ее для демонстрационной компании с названием Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку конфигурации электронной отчетности являются общими для всех компаний.</span><span class="sxs-lookup"><span data-stu-id="e67d9-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="e67d9-106">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре [Отправка конфигурации в Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="e67d9-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="e67d9-107">Также требуется доступ к LCS.</span><span class="sxs-lookup"><span data-stu-id="e67d9-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="e67d9-108">Войдите в приложение с помощью одной из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="e67d9-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="e67d9-109">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="e67d9-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="e67d9-110">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="e67d9-110">System administrator</span></span>

2. <span data-ttu-id="e67d9-111">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="e67d9-112">Выберите **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="e67d9-113">Убедитесь, что текущий пользователь Dynamics 365 Finance является членом проекта LCS, который содержит библиотеку активов, к которой пользователь хочет получить [доступ](../../lifecycle-services/asset-library.md#asset-library-support), чтобы импортировать конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="e67d9-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="e67d9-114">Невозможно получить доступ к проекту LCS из репозитория электронной отчетности, который представляет другой домен, отличный от домена, используемого в Finance.</span><span class="sxs-lookup"><span data-stu-id="e67d9-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="e67d9-115">При попытке будет отображен пустой список проектов LCS, и вы не сможете импортировать конфигурации электронной отчетности из библиотеки активов уровня проекта в LCS.</span><span class="sxs-lookup"><span data-stu-id="e67d9-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="e67d9-116">Чтобы получить доступ к библиотекам активов уровня проекта из репозитория электронной отчетности, который используется для импорта конфигураций электронной отчетности, выполните вход в Finance, используя учетные данные пользователя, принадлежащего к клиенту (домену), для которого была выполнена подготовка текущего экземпляра Finance.</span><span class="sxs-lookup"><span data-stu-id="e67d9-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="e67d9-117">Удаление общей версии конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="e67d9-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="e67d9-118">На странице **Конфигурации** в дереве конфигураций выберите пункт **Пример конфигурации модели**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="e67d9-119">Вы создали первую версию конфигурации примера модели данных и опубликовали ее в LCS, когда завершили шаги в разделе [Отправка конфигурации в Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="e67d9-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="e67d9-120">В этой процедуре мы удалим эту версию конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="e67d9-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="e67d9-121">Затем эту версию можно будет импортировать из LCS позже в этой теме.</span><span class="sxs-lookup"><span data-stu-id="e67d9-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="e67d9-122">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="e67d9-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="e67d9-123">Для этого примера выберите версию этой конфигурации со статусом **Общие**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="e67d9-124">Этот статус указывает, что конфигурация была опубликована в LCS.</span><span class="sxs-lookup"><span data-stu-id="e67d9-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="e67d9-125">Выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-125">Select **Change status**.</span></span>
4. <span data-ttu-id="e67d9-126">Выберите **Отменить**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="e67d9-127">Изменив статус выбранной версии с **Общее** на **Отменено**, можно сделать эту версию доступной для удаления.</span><span class="sxs-lookup"><span data-stu-id="e67d9-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="e67d9-128">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-128">Select **OK**.</span></span>
6. <span data-ttu-id="e67d9-129">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="e67d9-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="e67d9-130">Для этого примера выберите версию этой конфигурации со статусом **Отменено**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="e67d9-131">Выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-131">Select **Delete**.</span></span>
8. <span data-ttu-id="e67d9-132">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-132">Select **Yes**.</span></span>

    <span data-ttu-id="e67d9-133">Обратите внимание, что теперь доступна только черновая версия 2 выбранной конфигурации модели данных.</span><span class="sxs-lookup"><span data-stu-id="e67d9-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="e67d9-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e67d9-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="e67d9-135">Импорт общей версии конфигурации модели данных из LCS</span><span class="sxs-lookup"><span data-stu-id="e67d9-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="e67d9-136">Перейдите в раздел **Управление организацией \> Рабочие области \> Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="e67d9-137">В разделе **Поставщики конфигурации** выберите плитку **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="e67d9-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="e67d9-138">На плитке **Litware, Inc.** выберите **Репозитории**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="e67d9-139">Теперь можно открыть список репозиториев для поставщика конфигурации Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="e67d9-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="e67d9-140">Выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-140">Select **Open**.</span></span>

    <span data-ttu-id="e67d9-141">В данном примере выберите репозиторий **LCS** и откройте его.</span><span class="sxs-lookup"><span data-stu-id="e67d9-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="e67d9-142">Необходимо иметь [доступ](#accessconditions) к проекту LCS и к библиотеке активов, доступ к которой осуществляется выбранным репозиторием электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="e67d9-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="e67d9-143">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="e67d9-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="e67d9-144">Для этого примера выберите первую версию **примера конфигурации модели** в списке версий.</span><span class="sxs-lookup"><span data-stu-id="e67d9-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="e67d9-145">Выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-145">Select **Import**.</span></span>
7. <span data-ttu-id="e67d9-146">Выберите **Да**, чтобы подтвердить импорт выбранной версии из LCS.</span><span class="sxs-lookup"><span data-stu-id="e67d9-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="e67d9-147">Информационное сообщение подтверждает, что выбранная версия была успешно импортирована.</span><span class="sxs-lookup"><span data-stu-id="e67d9-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="e67d9-148">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e67d9-148">Close the page.</span></span>
9. <span data-ttu-id="e67d9-149">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e67d9-149">Close the page.</span></span>
10. <span data-ttu-id="e67d9-150">Выберите **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="e67d9-151">В дереве выберите **Пример конфигурации модели**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="e67d9-152">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="e67d9-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="e67d9-153">Для этого примера выберите версию этой конфигурации со статусом **Общие**.</span><span class="sxs-lookup"><span data-stu-id="e67d9-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="e67d9-154">Обратите внимание, что общая версия 1 выбранной конфигурации модели данных теперь также доступна.</span><span class="sxs-lookup"><span data-stu-id="e67d9-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]