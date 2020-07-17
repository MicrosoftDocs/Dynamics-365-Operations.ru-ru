---
title: Импорт обновленных версий конфигураций электронной отчетности
description: В этом разделе описан порядок импорта обновленных версий конфигураций электронной отчетности (ER) из глобального репозитория Configuration Service.
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4f167a0209713b5bca0cefe0135abd46a149a515
ms.sourcegitcommit: 1e6a7b50596eaf9d965e0155f3f2c50f7f50747e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/22/2020
ms.locfileid: "3498112"
---
# <a name="import-updated-versions-of-er-configurations"></a><span data-ttu-id="815d2-103">Импорт обновленных версий конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="815d2-103">Import updated versions of ER configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="815d2-104">[Репозитории](general-electronic-reporting.md#Repository) электронной отчетности (ER) служат для совместного использования [конфигураций ER](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="815d2-104">Electronic reporting (ER) [repositories](general-electronic-reporting.md#Repository) are used to share [ER configurations](general-electronic-reporting.md#Configuration).</span></span> <span data-ttu-id="815d2-105">Можно [импортировать](download-electronic-reporting-configuration-lcs.md) конфигурации ER из других репозиториев в экземпляр Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="815d2-105">You can [import](download-electronic-reporting-configuration-lcs.md) ER configurations from different repositories into your instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="815d2-106">При импорте конфигураций ER [поставщики конфигурации](general-electronic-reporting.md#Provider) могут публиковать новые [версии](general-electronic-reporting.md#component-versioning) репозиториев, чтобы их можно было использовать совместно.</span><span class="sxs-lookup"><span data-stu-id="815d2-106">When you import ER configurations, [configuration providers](general-electronic-reporting.md#Provider) can publish new [versions](general-electronic-reporting.md#component-versioning) repositories so that they can be shared.</span></span>

<span data-ttu-id="815d2-107">В этом разделе описан порядок импорта обновленных версий конфигураций электронной отчетности из глобального репозитория Configuration Service.</span><span class="sxs-lookup"><span data-stu-id="815d2-107">This topic explains how to import updated versions of ER configurations from the Global repository of the Configuration service.</span></span> <span data-ttu-id="815d2-108">Дополнительные сведения см. в разделе [Microsoft Dynamics 365 for Finance and Operations — Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="815d2-108">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="review-the-available-updated-versions"></a><span data-ttu-id="815d2-109">Просмотр доступных обновленных версий</span><span class="sxs-lookup"><span data-stu-id="815d2-109">Review the available updated versions</span></span>

1. <span data-ttu-id="815d2-110">Войдите в Finance с помощью одной из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="815d2-110">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="815d2-111">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="815d2-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="815d2-112">Консультант по функциональным возможностям электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="815d2-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="815d2-113">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="815d2-113">System administrator</span></span>

2. <span data-ttu-id="815d2-114">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="815d2-114">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="815d2-115">На странице **Конфигурации локализации** в разделе **Связанные ссылки** выберите плитку **Импорт обновлений версий конфигураций**.</span><span class="sxs-lookup"><span data-stu-id="815d2-115">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>

    ![Страница локализации конфигураций](./media/er-download-updated-versions-global-repo1.png)

4. <span data-ttu-id="815d2-117">В диалоговом окне **Импорт обновлений версий конфигураций электронной отчетности** в поле **режим работы** выберите **Отображать только доступные обновления**.</span><span class="sxs-lookup"><span data-stu-id="815d2-117">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Only show available updates**.</span></span> <span data-ttu-id="815d2-118">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="815d2-118">Then select **OK**.</span></span> 

    ![В поле режим прогона задано отображение только доступных обновлений](./media/er-download-updated-versions-global-repo2.png)

5. <span data-ttu-id="815d2-120">Проверьте полученное сообщение.</span><span class="sxs-lookup"><span data-stu-id="815d2-120">Review the messages that you receive.</span></span> <span data-ttu-id="815d2-121">Эти сообщения предоставляют следующие сведения о конфигурациях ER в текущем экземпляре Finance и о том, как они сравниваются с содержимым глобального репозитория:</span><span class="sxs-lookup"><span data-stu-id="815d2-121">These messages provide the following information about the ER configurations in the current Finance instance and how they compare to the content of the Global repository:</span></span>

    - <span data-ttu-id="815d2-122">Общее число конфигураций ER</span><span class="sxs-lookup"><span data-stu-id="815d2-122">The total number of ER configurations</span></span>
    - <span data-ttu-id="815d2-123">Конфигурации ER, отсутствующие в глобальном репозитории</span><span class="sxs-lookup"><span data-stu-id="815d2-123">ER configurations that aren't present in the Global repository</span></span>
    - <span data-ttu-id="815d2-124">Конфигурации ER, для которых последняя версия уже доступна в текущем экземпляре Finance (Для просмотра полного списка этих конфигураций ER выберите ссылку **Сведения о сообщении**.)</span><span class="sxs-lookup"><span data-stu-id="815d2-124">ER configurations for which the latest version is already available in the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![Сообщение "Последние версии следующих конфигураций уже импортированы" и сведения о сообщении](./media/er-download-updated-versions-global-repo3.png)

    - <span data-ttu-id="815d2-126">Конфигурации ER, для которых последняя версия доступна в глобальном репозитории и которые можно импортировать в текущей экземпляр Finance (Для просмотра полного списка этих конфигураций ER выберите ссылку **Сведения о сообщении**.)</span><span class="sxs-lookup"><span data-stu-id="815d2-126">ER configurations for which the latest version is available in the Global repository and can be imported into the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![Сообщение "Доступные обновления" и сведения о сообщении](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a><span data-ttu-id="815d2-128">Импорт доступных обновленных версий</span><span class="sxs-lookup"><span data-stu-id="815d2-128">Import available updated versions</span></span>

1. <span data-ttu-id="815d2-129">Войдите в Finance с помощью одной из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="815d2-129">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="815d2-130">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="815d2-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="815d2-131">Консультант по функциональным возможностям электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="815d2-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="815d2-132">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="815d2-132">System administrator</span></span>

2. <span data-ttu-id="815d2-133">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="815d2-133">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="815d2-134">На странице **Конфигурации локализации** в разделе **Связанные ссылки** выберите плитку **Импорт обновлений версий конфигураций**.</span><span class="sxs-lookup"><span data-stu-id="815d2-134">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>
4. <span data-ttu-id="815d2-135">В диалоговом окне **Импорт обновлений версий конфигураций электронной отчетности** в поле **Режим прогона** выберите **Импорт последних обновлений** для импорта последних версий конфигураций ER из глобального репозитория в текущий экземпляр Finance.</span><span class="sxs-lookup"><span data-stu-id="815d2-135">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Import latest updates** to import the latest versions of ER configurations from the Global repository into the current Finance instance.</span></span>
5. <span data-ttu-id="815d2-136">Чтобы запланировать пакетное задание для импорта, на экспресс-вкладке **Выполнять в фоновом режиме** установите для параметра **Пакетная обработка** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="815d2-136">To schedule a batch job for the import, on the **Run in the background** FastTab, set the **Batch processing** option to **Yes**.</span></span> <span data-ttu-id="815d2-137">Если необходимо периодически повторять импорт, настройте необходимые повторения.</span><span class="sxs-lookup"><span data-stu-id="815d2-137">If you want to repeat the import periodically, configure the required recurrence.</span></span>

    ![В поле режима прогона задан импорт последних обновлений](./media/er-download-updated-versions-global-repo5.png)

6. <span data-ttu-id="815d2-139">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="815d2-139">Select **OK**.</span></span>
7. <span data-ttu-id="815d2-140">Чтобы узнать, какие версии конфигурации были импортированы, выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="815d2-140">To learn what configuration versions have been imported, follow one of these steps:</span></span>

    - <span data-ttu-id="815d2-141">Если вы запускаете импорт в интерактивном режиме вместо использования пакетного задания, проверьте полученное сообщение.</span><span class="sxs-lookup"><span data-stu-id="815d2-141">If you run the import interactively instead of using a batch job, review the messages that you receive.</span></span>

        ![Сообщения, полученные в ходе интерактивного выполнения импорта](./media/er-download-updated-versions-global-repo6.png)

    - <span data-ttu-id="815d2-143">Если выполняется импорт в пакетном режиме, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="815d2-143">If you run the import in batch mode, follow these steps:</span></span>

        1. <span data-ttu-id="815d2-144">Перейдите в раздел **Общие** \> **Запросы** \> **Пакетные задания** \> **Мои пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="815d2-144">Go to **Common** \> **Inquiries** \> **Batch jobs** \> **My batch jobs**.</span></span>
        2. <span data-ttu-id="815d2-145">Найдите и выберите задание **Импорт обновлений версий конфигураций электронной отчетности**, затем на панели операций на вкладке **Пакетное задание** выберите **Журнал пакетных заданий** для просмотра журнала заданий.</span><span class="sxs-lookup"><span data-stu-id="815d2-145">Find and select the **Import electronic reporting configurations versions updates** job, and then, on the Action Pane, on the **Batch job** tab, select **Batch job history** to view the job history.</span></span>
        3. <span data-ttu-id="815d2-146">На странице **Журнал пакетных заданий** выберите **Журнал**.</span><span class="sxs-lookup"><span data-stu-id="815d2-146">On the **Batch job history** page, select **Log**.</span></span> <span data-ttu-id="815d2-147">Затем в полученном сообщении выберите ссылку **Сведения о сообщении** для просмотра журнала заданий.</span><span class="sxs-lookup"><span data-stu-id="815d2-147">Then, in the message that you receive, select the **Message details** link to view the job log.</span></span>

        ![Журнал заданий](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> <span data-ttu-id="815d2-149">Не рекомендуется планировать повторяющееся пакетное задание, чтобы импортировать обновленные версии конфигураций ER непосредственно из глобального репозитория в производственную среду, так как импортированные версии сразу будут доступны для использования.</span><span class="sxs-lookup"><span data-stu-id="815d2-149">We don't recommend that you schedule a recurring batch job to import updated versions of ER configurations directly from the Global repository into a production environment, because the imported versions will immediately be available for use.</span></span> <span data-ttu-id="815d2-150">Вместо этого такой подход следует использовать для развертывания версий конфигураций ER в среде "песочницы".</span><span class="sxs-lookup"><span data-stu-id="815d2-150">Instead, use this approach to deploy versions of ER configurations to a sandbox environment.</span></span> <span data-ttu-id="815d2-151">Затем их можно оценить в среде "песочницы" перед их развертыванием в производственной среде.</span><span class="sxs-lookup"><span data-stu-id="815d2-151">They can then be evaluated in the sandbox environment before they are deployed to a production environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="815d2-152">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="815d2-152">Additional resources</span></span>

- [<span data-ttu-id="815d2-153">Обзор электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="815d2-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="815d2-154">Загрузка конфигураций электронной отчетности (ER) из глобального репозитория Configuration Service</span><span class="sxs-lookup"><span data-stu-id="815d2-154">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
