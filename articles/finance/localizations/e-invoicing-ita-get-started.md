---
title: Начало работы с электронным выставлением накладных для Италии
description: В этой теме приводятся сведения, которые помогут приступить к работе с электронным выставлением накладных для Италии.
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 23cb0523b6d6d065ad19f6c3bddf881b0dc82a7d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840108"
---
# <a name="get-started-with-electronic-invoicing-for-italy"></a><span data-ttu-id="dbb6c-103">Начало работы с электронным выставлением накладных для Италии</span><span class="sxs-lookup"><span data-stu-id="dbb6c-103">Get started with Electronic invoicing for Italy</span></span>

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="dbb6c-104">В настоящее время модуль электронного выставления накладных для Италии может не поддерживать все функции, доступные для электронных накладных в Microsoft Dynamics 365 Finance и Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-104">Electronic invoicing for Italy might not currently support all the functions that are available for electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="dbb6c-105">В этой теме приводятся сведения, которые помогут приступить к работе с электронным выставлением накладных для Италии.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-105">This topic provides information that will help you get started with Electronic invoicing for Italy.</span></span> <span data-ttu-id="dbb6c-106">Она поможет выполнить этапы настройки, зависящие от страны или региона, в службах Regulatory Configuration Services (RCS) и в Finance.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="dbb6c-107">Она также проводит пользователя через процесс отправки электронных накладных, которые создаются в специальном формате **FatturaPA** для Италии, через службу и объясняет, как просмотреть результаты обработки.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-107">It also guides you through the process for submitting electronic invoices that are generated in the Italy-specific **FatturaPA** format through the service, and it explains how to review the results of processing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dbb6c-108">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="dbb6c-108">Prerequisites</span></span>

<span data-ttu-id="dbb6c-109">Перед выполнением шагов, описанных в этой теме, необходимо выполнить шаги из раздела [Приступая к работе с модулем электронного выставления накладных](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="dbb6c-109">Before you complete the steps in this topic, you must complete the steps in [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="dbb6c-110">Настройка RCS</span><span class="sxs-lookup"><span data-stu-id="dbb6c-110">RCS setup</span></span>

<span data-ttu-id="dbb6c-111">Во время настройки RCS будут выполнены следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="dbb6c-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="dbb6c-112">Импортируйте функцию электронных накладных для экспорта электронных накладных клиента в формате **FatturaPA**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-112">Import the e-Invoicing feature for the export of customer electronic invoices in the **FatturaPA** format.</span></span>
2. <span data-ttu-id="dbb6c-113">Проверьте конфигураций форматов, необходимых для создания, отправки и получения ответов об электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-113">Review the format configurations that are required to generate, submit, and receive responses about electronic invoices.</span></span>
3. <span data-ttu-id="dbb6c-114">Настройте события, которые поддерживают сценарии отправки электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-114">Configure the events that support the electronic invoice submission scenarios.</span></span>
4. <span data-ttu-id="dbb6c-115">Опубликуйте функцию выставления накладных в электронной форме.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-115">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="dbb6c-116">"Функция электронных накладных" — это универсальное имя для ресурса, который настраивается и публикуется для использования сервера модуля электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing server.</span></span> <span data-ttu-id="dbb6c-117">В данном случае экспорт электронных накладных клиента является функцией электронных накладных, которую мы будем настраивать.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-117">In this case, the export of customer electronic invoices is the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="dbb6c-118">Импорт функции выставления накладных в электронной форме</span><span class="sxs-lookup"><span data-stu-id="dbb6c-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="dbb6c-119">Войдите в учетную запись RCS.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="dbb6c-120">В рабочей области **Функции глобализации** в разделе **Функции** выберите плитку **Электронные накладные**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="dbb6c-121">На странице **Функции электронного выставления накладных** выберите **Импорт**, чтобы импортировать функцию электронных накладных из глобального репозитория.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-121">On the **e-Invoicing Features** page, select **Import** to import the e-Invoicing feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dbb6c-122">Если список доступных функций не отображается, выберите **Синхронизировать**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-122">If you don't see the list of available features, select **Synchronize**.</span></span> 

4. <span data-ttu-id="dbb6c-123">Выберите функцию **Экспорт электронных накладных (IT)**, затем выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-123">Select the **e-Invoices Export (IT)** feature, and then select **Import**.</span></span>

![Импорт функции экспорта электронных накладных (IT)](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

<span data-ttu-id="dbb6c-125">При импорте функции **Экспорт электронных накладных (IT)** из глобального репозитория все параметры, описанные в следующих разделах, также импортируются.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-125">When you import the **e-Invoices Export (IT)** feature from the Global repository, all the settings that are described in the next sections are also imported.</span></span>

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a><span data-ttu-id="dbb6c-126">Создание новой версии функции экспорта электронных накладных (IT)</span><span class="sxs-lookup"><span data-stu-id="dbb6c-126">Create a new version of the e-Invoices Export (IT) feature</span></span>

1. <span data-ttu-id="dbb6c-127">На странице **Функции электронных накладных** на вкладке **Версии** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-127">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span> 

    ![Добавление новой версии функции электронных накладных](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    <span data-ttu-id="dbb6c-129">Далее нужно настроить форматы электронной отчетности (ER), которые связаны с функцией электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-129">Next, you will configure the Electronic reporting (ER) formats that are associated with the e-Invoicing feature.</span></span>

2. <span data-ttu-id="dbb6c-130">На вкладке **Конфигурации** выберите **Добавить** для управления версиями конфигурации.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-130">On the **Configurations** tab, select **Add** to manage the configuration versions.</span></span>

    ![Управление версиями конфигурации функции электронных накладных](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    <span data-ttu-id="dbb6c-132">На этом шаге вы добавляете и настраиваете форматы электронной отчетности для различных файлов, используемых для экспорта итальянских электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-132">In this step, you're adding and configuring the ER formats of different files that are used to export Italian e-invoices.</span></span> <span data-ttu-id="dbb6c-133">Для итальянских электронных накладных FatturaPA используйте следующие стандартные конфигурации или фактические настроенные конфигурации, которые вы используете для электронных накладных:</span><span class="sxs-lookup"><span data-stu-id="dbb6c-133">For Italian FatturaPA e-invoices, use either the following standard configurations or the actual customized configurations that you use for e-invoicing:</span></span>

    - <span data-ttu-id="dbb6c-134">Накладная по продаже (IT)</span><span class="sxs-lookup"><span data-stu-id="dbb6c-134">Sales invoice (IT)</span></span>
    - <span data-ttu-id="dbb6c-135">Накладная по проекту (IT)</span><span class="sxs-lookup"><span data-stu-id="dbb6c-135">Project invoice (IT)</span></span>

    <span data-ttu-id="dbb6c-136">При создании функции электронных накладных, которая является производной от другой функции электронных накладных, все форматы электронной отчетности наследуются от исходной функции.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-136">When you create an e-Invoicing feature that is derived from another e-Invoicing feature, all ER formats are inherited from the original feature.</span></span>

3. <span data-ttu-id="dbb6c-137">Выберите конкретную конфигурацию файла формата электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-137">Select a specific ER format file configuration.</span></span>
4. <span data-ttu-id="dbb6c-138">Выберите **Изменить** или **Просмотреть**, чтобы открыть страницу **Конструктор формата**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-138">Select **Edit** or **View** to open the **Format designer** page.</span></span>

    ![Открытие страницы конструктора формата](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. <span data-ttu-id="dbb6c-140">Страница **Конструктор форматов** используется для изменения и просмотра конфигураций форматов файлов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-140">Use the **Format designer** page to edit and view the ER format file configurations.</span></span>

    ![Страница конструктора форматов](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="dbb6c-142">Управление настройками функции электронных накладных</span><span class="sxs-lookup"><span data-stu-id="dbb6c-142">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="dbb6c-143">На странице **Функции электронного выставления накладных** на вкладке **Настройки** выберите **Добавить**, **Удалить** или **Изменить** для управления настройками функций электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-143">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![Управление настройками функций электронных накладных](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="dbb6c-145">На этом шаге настраиваются события, применимые к электронным накладным, в том числе генерация выходных файлов XML в формате **FatturaPA** и цифровой подписи (если необходимо).</span><span class="sxs-lookup"><span data-stu-id="dbb6c-145">In this step, you configure the events that are applicable to electronic invoices, including generation of the XML output files in **FatturaPA** format and digital signing (if required).</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="dbb6c-146">Настройка настройки функций накладных на продажу</span><span class="sxs-lookup"><span data-stu-id="dbb6c-146">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="dbb6c-147">На странице **Функции электронного выставления накладных** на вкладке **Настройки** в столбце **Настройка функции** выберите **Накладная на продажу**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-147">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="dbb6c-148">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-148">Select **Edit**.</span></span>
3. <span data-ttu-id="dbb6c-149">На странице **Настройка версии функции** выберите вкладку **Действия** для управления списком действий.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-149">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="dbb6c-150">Действия определяют список операций, которые должны выполняться в последовательном порядке для обеспечения полного выполнения события.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-150">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Вкладка "Действия"](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | <span data-ttu-id="dbb6c-152">Код действия</span><span class="sxs-lookup"><span data-stu-id="dbb6c-152">Action ID</span></span> | <span data-ttu-id="dbb6c-153">Имя действия</span><span class="sxs-lookup"><span data-stu-id="dbb6c-153">Action name</span></span>        | <span data-ttu-id="dbb6c-154">Описание действия</span><span class="sxs-lookup"><span data-stu-id="dbb6c-154">Action description</span></span>                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | <span data-ttu-id="dbb6c-155">1</span><span class="sxs-lookup"><span data-stu-id="dbb6c-155">1</span></span>         | <span data-ttu-id="dbb6c-156">Преобразование документа</span><span class="sxs-lookup"><span data-stu-id="dbb6c-156">Transform document</span></span> | <span data-ttu-id="dbb6c-157">Создание файла XML для электронной накладной в формате **FatturaPA**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-157">Create the e-invoice XML file in **FatturaPA** format.</span></span> |
    | <span data-ttu-id="dbb6c-158">2</span><span class="sxs-lookup"><span data-stu-id="dbb6c-158">2</span></span>         | <span data-ttu-id="dbb6c-159">Подписать документ</span><span class="sxs-lookup"><span data-stu-id="dbb6c-159">Sign document</span></span>      | <span data-ttu-id="dbb6c-160">Применение цифровой подписи к файлу XML.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-160">Apply a digital signature to the XML file.</span></span>             |

4. <span data-ttu-id="dbb6c-161">Выберите вкладку **Правила применимости** для просмотра и сопровождения правил применимости.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-161">Select the **Applicability rules** tab to view and maintain the applicability rules.</span></span> <span data-ttu-id="dbb6c-162">Правила применимости определяют контекст, в котором будет выполняться действие.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-162">Applicability rules define the context where the action will be run.</span></span>

    ![Вкладка "Правила применимости"](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. <span data-ttu-id="dbb6c-164">Перейдите на вкладку **Переменные**, чтобы просмотреть и настроить переменные.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-164">Select the **Variables** tab to view and maintain the variables.</span></span>

    ![Вкладка "Переменные"](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. <span data-ttu-id="dbb6c-166">Определите открытые переменные, необходимые для выполнения действий.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-166">Define the public variables that are required to run the actions.</span></span>

### <a name="configure-the-project-invoice-feature-setup"></a><span data-ttu-id="dbb6c-167">Настройка настройки функций накладных по проекту</span><span class="sxs-lookup"><span data-stu-id="dbb6c-167">Configure the Project invoice feature setup</span></span> 

<span data-ttu-id="dbb6c-168">Шаги и настройки, необходимые для задания настроек функции **Накладная по проекту**, очень похожи на шаги и параметры для настройки функции **Накладная по продаже**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-168">The steps and settings that are required to configure the **Project invoice** feature setup are very similar to the steps and settings for the **Sales invoice** feature setup.</span></span> <span data-ttu-id="dbb6c-169">При работе с накладными по проекту см. процедуры для накладных по продаже.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-169">When you work with project invoices, see the procedures for sales invoices.</span></span>

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a><span data-ttu-id="dbb6c-170">Назначение функции электронных накладных для среды</span><span class="sxs-lookup"><span data-stu-id="dbb6c-170">Assign the e-Invoicing feature to the environment</span></span>

1. <span data-ttu-id="dbb6c-171">На странице **Функции электронных накладных** на вкладке **Среды** выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-171">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="dbb6c-172">В поле **Среда** выберите среду.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-172">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="dbb6c-173">В поле **Действует с** выберите дату, когда новая среда должна начать действовать.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-173">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="dbb6c-174">Выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-174">Select **Enable**.</span></span> 

![Включение среды выставления накладных в электронной форме](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="dbb6c-176">Публикация функции выставления накладных в электронной форме</span><span class="sxs-lookup"><span data-stu-id="dbb6c-176">Publish the e-invoicing feature</span></span>

<span data-ttu-id="dbb6c-177">Можно опубликовать функцию электронных накладных, изменив статус версии на **Завершено** или **Опубликовано**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-177">You can publish the e-Invoicing feature by changing the version status to **Completed** or **Published**.</span></span>

### <a name="change-the-version-status-to-completed"></a><span data-ttu-id="dbb6c-178">Изменение статуса версии на "Завершено"</span><span class="sxs-lookup"><span data-stu-id="dbb6c-178">Change the version status to Completed</span></span>

1. <span data-ttu-id="dbb6c-179">На странице **Функции электронных накладных** на вкладке **Версии** выберите версию функции электронных накладных, имеющую статус **Черновик**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-179">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="dbb6c-180">Выберите **Изменить статус \> Завершено**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-180">Select **Change status \> Complete**.</span></span> 

### <a name="change-the-version-status-to-published"></a><span data-ttu-id="dbb6c-181">Изменение статуса версии на "Опубликовано"</span><span class="sxs-lookup"><span data-stu-id="dbb6c-181">Change the version status to Published</span></span> 

1. <span data-ttu-id="dbb6c-182">На странице **Функции электронных накладных** на вкладке **Версии** выберите версию функции электронных накладных, имеющую статус **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-182">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="dbb6c-183">Выберите **Изменить статус \> Опубликовано**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-183">Select **Change status \> Publish**.</span></span>

![Изменение статуса функции электронных накладных](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-integration-in-finance"></a><span data-ttu-id="dbb6c-185">Настройка интеграции модуля электронного выставления накладных в Finance</span><span class="sxs-lookup"><span data-stu-id="dbb6c-185">Set up Electronic invoicing integration in Finance</span></span>

<span data-ttu-id="dbb6c-186">Во время настройки Finance будут выполнены следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="dbb6c-186">During the setup of Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="dbb6c-187">Импортируйте модель данных электронной отчетности, сопоставление модели данных электронной отчетности и контекстные конфигурации для электронных накладных FatturaPA.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-187">Import the ER data model, the ER data model mapping, and the context configurations for FatturaPA e-invoices.</span></span>
2. <span data-ttu-id="dbb6c-188">Настройте сертификат, необходимый для цифрового подписывания итальянских электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-188">Configure the certificate that is required to digitally sign Italian e-invoices.</span></span>

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a><span data-ttu-id="dbb6c-189">Импорт модели данных электронной отчетности, сопоставление модели данных и форматы</span><span class="sxs-lookup"><span data-stu-id="dbb6c-189">Import the ER data model, data model mapping, and formats</span></span>

1. <span data-ttu-id="dbb6c-190">В рабочей области **Электронной отчетности** убедитесь, что для поставщика конфигурации **Служба бизнес-документов** установлен статус **Активно**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-190">In the **Electronic reporting** workspace, verify that the **Business Document Service** configuration provider is set to **Active**.</span></span>
2. <span data-ttu-id="dbb6c-191">Выберите **Репозитории**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-191">Select **Repositories**.</span></span>
3. <span data-ttu-id="dbb6c-192">Выберите **Глобальный ресурс \> Открыть**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-192">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="dbb6c-193">Импортируйте **Модель накладных**, **Сопоставление модели накладных** и **Контекстная модель накладной клиента**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-193">Import **Invoice model**, **Invoice model mapping**, and **Customer invoice context model**.</span></span>

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a><span data-ttu-id="dbb6c-194">Включение функции экспорта электронных накладных клиента для Италии</span><span class="sxs-lookup"><span data-stu-id="dbb6c-194">Turn on the feature for exporting customer electronic invoices for Italy</span></span>

1. <span data-ttu-id="dbb6c-195">Перейдите в раздел **Администрирование организации \> Настройка \> Параметры электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-195">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="dbb6c-196">На вкладке **Функции** установите флажок **Включено** в строке для ссылки на функцию **IT00036**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-196">On the **Features** tab, select the **Enabled** check box in the row for feature reference **IT00036**.</span></span>

![Включение функции FatturaPA](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a><span data-ttu-id="dbb6c-198">Настройка электронных документов</span><span class="sxs-lookup"><span data-stu-id="dbb6c-198">Configure electronic documents</span></span>

1. <span data-ttu-id="dbb6c-199">Перейдите в раздел **Администрирование организации \> Настройка \> Параметры электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-199">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="dbb6c-200">На вкладке **Электронный документ** выберите **Добавить** и введите таблицы, которые необходимы для создания итальянских электронных накладных:</span><span class="sxs-lookup"><span data-stu-id="dbb6c-200">On the **Electronic document** tab, select **Add**, and enter the tables that are required to generate Italian e-invoices:</span></span>

    - <span data-ttu-id="dbb6c-201">**Имя таблицы:** Журнал накладных клиента</span><span class="sxs-lookup"><span data-stu-id="dbb6c-201">**Table name:** Customer invoice journal</span></span>
    - <span data-ttu-id="dbb6c-202">**Имя таблицы:** Накладная по проекту</span><span class="sxs-lookup"><span data-stu-id="dbb6c-202">**Table name:** Project invoice</span></span>

3. <span data-ttu-id="dbb6c-203">Для каждой таблицы определите связанный контекст документа:</span><span class="sxs-lookup"><span data-stu-id="dbb6c-203">For each table, define a related document context:</span></span>

    - <span data-ttu-id="dbb6c-204">Для **журнала накладных клиента** выберите **Контекст накладной клиента**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-204">For **Customer invoice journal**, select **Customer invoice context**.</span></span>
    - <span data-ttu-id="dbb6c-205">Для **накладной по проекту** выберите **Контекст накладной по проекту**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-205">For **Project invoice**, select **Project invoice context**.</span></span>

![Настройка типов ответов](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a><span data-ttu-id="dbb6c-207">Обработка электронных накладных</span><span class="sxs-lookup"><span data-stu-id="dbb6c-207">Electronic invoice processing</span></span>

<span data-ttu-id="dbb6c-208">Во время обработки в Finance будут выполнены следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="dbb6c-208">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="dbb6c-209">Создание итальянских электронных накладных с помощью модуля электронного выставления накладных</span><span class="sxs-lookup"><span data-stu-id="dbb6c-209">Generate Italian e-invoices through Electronic invoicing</span></span>
2. <span data-ttu-id="dbb6c-210">Просмотр журналов выполнения и просмотр результатов обработки</span><span class="sxs-lookup"><span data-stu-id="dbb6c-210">View the execution logs and review the results of processing</span></span>

### <a name="generate-electronic-invoices"></a><span data-ttu-id="dbb6c-211">Создание электронных накладных</span><span class="sxs-lookup"><span data-stu-id="dbb6c-211">Generate electronic invoices</span></span>

<span data-ttu-id="dbb6c-212">После включения функции **Интеграция настраиваемой функции электронного выставления накладных** и активации функции **IT00036** старый процесс Finance для создания итальянских электронных накладных больше использоваться не может.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-212">After you turn on the **Configurable Electronic invoicing integration** feature and activate the **IT00036** feature, the old Finance process for generating Italian e-invoices can no longer be used.</span></span> <span data-ttu-id="dbb6c-213">Он заменяется новым процессом с именем **Отправка электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-213">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

<span data-ttu-id="dbb6c-214">Документы можно отправлять вручную в соответствии с потребностями для электронных документов.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-214">You can submit the documents manually, based on your demand for e-invoice documents.</span></span>

> [!NOTE]
> <span data-ttu-id="dbb6c-215">Перед продолжением убедитесь, что настройка, необходимая для итальянских электронных накладных, была выполнена.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-215">Before you continue, verify that the setup that is required for Italian e-invoices was completed.</span></span> <span data-ttu-id="dbb6c-216">Дополнительные сведения см. в разделе [Электронные накладные клиента](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span><span class="sxs-lookup"><span data-stu-id="dbb6c-216">For more information, see [Customer electronic invoices](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span></span> <span data-ttu-id="dbb6c-217">Имейте в виду, что некоторые из описанных в этой теме шагов настройки могут оказаться недоступными в связи с включением функции электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-217">Be aware that some of the setup steps that are described in that topic might be unavailable because of Electronic invoicing activation.</span></span>

1. <span data-ttu-id="dbb6c-218">Перейдите в раздел **Администрирование организации \> Периодические задачи \> Электронные документы \> Отправка электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-218">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="dbb6c-219">Для первой отправки любого документа установите для параметра **Повторно отправить документы** значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-219">For the first submission of any document, set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="dbb6c-220">Если необходимо повторно отправить документ через службу, установите для этого параметра значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-220">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="dbb6c-221">На экспресс-вкладке **Включаемые записи** выберите **Фильтр**, чтобы открыть диалоговое окно **Запрос**, в котором можно построить запрос для выбора повторно отправляемых документов.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-221">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Диалоговое окно отправки электронных документов](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a><span data-ttu-id="dbb6c-223">Запрос фильтрации</span><span class="sxs-lookup"><span data-stu-id="dbb6c-223">Filter query</span></span>

1. <span data-ttu-id="dbb6c-224">В диалоговом окне **Запрос** настройте условия фильтрации для накладных по продаже и накладных по проекту либо оставьте эти условия пустыми, чтобы включить все неотправленные накладные.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-224">In the **Inquiry** dialog box, configure the filtering conditions for both sales invoices and project invoices, or leave the conditions blank to include all unsubmitted invoices.</span></span>

    ![Настройка критериев фильтрации отправки](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. <span data-ttu-id="dbb6c-226">Выберите **ОК**, чтобы закрыть диалоговое окно **Запрос**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-226">Select **OK** to close the **Inquiry** dialog box.</span></span>
3. <span data-ttu-id="dbb6c-227">Выберите **ОК**, чтобы отправить выбранные документы.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-227">Select **OK** submit the selected documents.</span></span>

> <span data-ttu-id="dbb6c-228">![ПРИМЕЧАНИЕ] При первой попытке отправить документ через службу вам будет предложено подтвердить связь с модулем электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-228">![NOTE] During your first attempt to submit a document through the service, you will be prompted to confirm the connection with Electronic invoicing.</span></span> <span data-ttu-id="dbb6c-229">Выберите **Щелкните здесь для подключения к службе отправки электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-229">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

#### <a name="view-submission-logs"></a><span data-ttu-id="dbb6c-230">Просмотр журналов отправки</span><span class="sxs-lookup"><span data-stu-id="dbb6c-230">View submission logs</span></span>

<span data-ttu-id="dbb6c-231">Можно просмотреть журналы отправки для всех отправленных документов.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-231">You can view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="dbb6c-232">Перейдите в раздел **Администрирование организации \> Периодические задачи \> Электронные документы \> Журнал отправки электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-232">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="dbb6c-233">В поле **Тип документов** выберите **Журнал накладных клиента** или **Накладная по проекту**, чтобы отфильтровать необходимые электронные документы.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-233">In the **Document type** field, select **Customer invoice journal** or **Project invoice** to filter for the required electronic documents.</span></span>

    ![Выбор типа документов для просмотра журналов отправки](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    <span data-ttu-id="dbb6c-235">Значение, отображаемое в столбце **Состояние отправки**, представляет статус процесса отправки.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-235">The value that is shown in the **Submission status** column represents the status of the submission process.</span></span> <span data-ttu-id="dbb6c-236">Он указывает, завершился ли процесс, как было настроено, и требуются ли дополнительные действия.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-236">It indicates whether the process ran as configured and whether additional action is required.</span></span>

3. <span data-ttu-id="dbb6c-237">В области действий выберите **Запросы \> Сведения об отправке** для просмотра сведений о журналах выполнения отправки.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-237">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Просмотр сведений журнала отправки](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. <span data-ttu-id="dbb6c-239">На экспресс-вкладке **Действия по обработке** можно просмотреть журнал выполнения для действий, настроенных в версии функции, которая была настроена в RCS.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-239">On the **Processing actions** FastTab, you can view the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="dbb6c-240">Столбец **Состояние** показывает, было ли действие успешно выполнено.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-240">The **Status** column shows whether the action was successfully run.</span></span>
5. <span data-ttu-id="dbb6c-241">На экспресс-вкладке **Файлы действий** можно просматривать промежуточные файлы, созданные во время выполнения действий.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-241">On the **Action files** FastTab, you can view the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="dbb6c-242">Можно выбрать **Просмотр** для загрузки выходного файла XML в формате **FatturaPA** и просмотра его содержимого.</span><span class="sxs-lookup"><span data-stu-id="dbb6c-242">You can select **View** to download the output XML file in **FatturaPA** format and view its content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbb6c-243">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="dbb6c-243">Related topics</span></span>

- [<span data-ttu-id="dbb6c-244">Обзор электронного выставления накладных</span><span class="sxs-lookup"><span data-stu-id="dbb6c-244">Electronic invoicing overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="dbb6c-245">Начало работы с электронным выставлением накладных</span><span class="sxs-lookup"><span data-stu-id="dbb6c-245">Get started with Electronic invoicing</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="dbb6c-246">Настройка электронного выставления накладных</span><span class="sxs-lookup"><span data-stu-id="dbb6c-246">Set up Electronic invoicing</span></span>](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
