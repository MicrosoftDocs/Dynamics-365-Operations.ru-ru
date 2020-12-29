---
title: Настройка формата электронной отчетности для создания пользовательского электронного документа
description: В этой теме объясняется, как настроить поставляемый корпорацией Майкрософт формат электронной отчетности (ER), чтобы он создавал специальный электронный документ.
author: NickSelin
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20e7a32ac5f6ab21f89ed3c11c64458286864c9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680178"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a><span data-ttu-id="2b90e-103">Настройка формата электронной отчетности для создания пользовательского электронного документа</span><span class="sxs-lookup"><span data-stu-id="2b90e-103">Adjust an ER format to generate a custom electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2b90e-104">Процедуры данного раздела объясняют, как пользователь с ролью системного администратора или функционального консультанта по электронной отчетности может выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="2b90e-104">The procedures in this topic explain how a user in the System Administrator or Electronic Reporting Functional Consultant role can perform these tasks:</span></span>

- <span data-ttu-id="2b90e-105">Настройка параметров для [платформы электронной отчетности (ER)](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="2b90e-105">Configure parameters for the [Electronic reporting (ER) framework](general-electronic-reporting.md).</span></span>
- <span data-ttu-id="2b90e-106">Импорт конфигураций ER, которые предоставляются корпорацией Майкрософт и используются для создания файла платежа при обработке [платежа поставщику](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2b90e-106">Import ER configurations that are provided by Microsoft and used to generate a payment file while a [vendor payment](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) is being processed.</span></span>
- <span data-ttu-id="2b90e-107">Создание настраиваемой версии стандартной конфигурации формата ER, предоставляемой корпорацией Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2b90e-107">Create a custom version of a standard ER format configuration that is provided by Microsoft.</span></span>
- <span data-ttu-id="2b90e-108">Изменение пользовательской конфигурации формата ER таким образом, чтобы она создавала файлы платежей, соответствующие требованиям конкретного банка.</span><span class="sxs-lookup"><span data-stu-id="2b90e-108">Modify the custom ER format configuration so that it generates payment files that meets the requirements of a specific bank.</span></span>
- <span data-ttu-id="2b90e-109">Адаптация изменений, внесенных в стандартную конфигурацию формата ER, в пользовательской конфигурации формата ER.</span><span class="sxs-lookup"><span data-stu-id="2b90e-109">Adopt changes that are made to the standard ER format configuration in the custom ER format configuration.</span></span>

<span data-ttu-id="2b90e-110">Все следующие процедуры могут выполняться в компании **GBSI**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-110">All the following procedures can be done in the **GBSI** company.</span></span> <span data-ttu-id="2b90e-111">Написание кода не требуется.</span><span class="sxs-lookup"><span data-stu-id="2b90e-111">No coding is required.</span></span>

- [<span data-ttu-id="2b90e-112">Настройка платформы электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-112">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="2b90e-113">Настройка параметров ER</span><span class="sxs-lookup"><span data-stu-id="2b90e-113">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="2b90e-114">Активация поставщика конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-114">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="2b90e-115">Просмотр списка поставщиков конфигурации электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-115">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="2b90e-116">Добавление нового поставщика конфигурации электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-116">Add a new ER configuration provider</span></span>](#ActivateProvider)
        - [<span data-ttu-id="2b90e-117">Активация поставщика конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-117">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="2b90e-118">Импорт стандартных конфигураций формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-118">Import the standard ER format configurations</span></span>](#ImportERSolution1)

    - [<span data-ttu-id="2b90e-119">Импорт стандартных конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-119">Import the standard ER configurations</span></span>](#ImportERFormat1)
    - [<span data-ttu-id="2b90e-120">Проверка импортированных конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-120">Review the imported ER configurations</span></span>](#ReviewImportedERSolution)

- [<span data-ttu-id="2b90e-121">Подготовка обработки платежа поставщику</span><span class="sxs-lookup"><span data-stu-id="2b90e-121">Prepare a vendor payment for processing</span></span>](#PrepareVendorPayment)

    - [<span data-ttu-id="2b90e-122">Добавление банковской информации для счета поставщика</span><span class="sxs-lookup"><span data-stu-id="2b90e-122">Add bank information for a vendor account</span></span>](#AddBankAccount)
    - [<span data-ttu-id="2b90e-123">Ввод платежа поставщику</span><span class="sxs-lookup"><span data-stu-id="2b90e-123">Enter a vendor payment</span></span>](#EnterVendorPayment)

- [<span data-ttu-id="2b90e-124">Обработка платежа поставщику с помощью стандартного формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-124">Process a vendor payment by using the standard ER format</span></span>](#ProcessVendorPayment1)

    - [<span data-ttu-id="2b90e-125">Настройка способа оплаты с помощью электронного платежа</span><span class="sxs-lookup"><span data-stu-id="2b90e-125">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment1)
    - [<span data-ttu-id="2b90e-126">Обработка платежа поставщику</span><span class="sxs-lookup"><span data-stu-id="2b90e-126">Process a vendor payment</span></span>](#ProcessPayment1)

- [<span data-ttu-id="2b90e-127">Настройка стандартного формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-127">Customize the standard ER format</span></span>](#CustomizeProvidedFormat)

    - [<span data-ttu-id="2b90e-128">Создание пользовательского формата</span><span class="sxs-lookup"><span data-stu-id="2b90e-128">Create a custom format</span></span>](#DeriveProvidedFormat)
    - [<span data-ttu-id="2b90e-129">Изменение пользовательского формата</span><span class="sxs-lookup"><span data-stu-id="2b90e-129">Edit a custom format</span></span>](#ConfigureDerivedFormat)
    - [<span data-ttu-id="2b90e-130">Пометка пользовательского формата как готового к запуску</span><span class="sxs-lookup"><span data-stu-id="2b90e-130">Mark a custom format as runnable</span></span>](#MarkFormatRunnable)

- [<span data-ttu-id="2b90e-131">Обработка платежа поставщику с помощью пользовательского формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-131">Process a vendor payment by using the custom ER format</span></span>](#ProcessVendorPayment2)

    - [<span data-ttu-id="2b90e-132">Настройка способа оплаты с помощью электронного платежа</span><span class="sxs-lookup"><span data-stu-id="2b90e-132">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment2)
    - [<span data-ttu-id="2b90e-133">Обработка платежа поставщику</span><span class="sxs-lookup"><span data-stu-id="2b90e-133">Process a vendor payment</span></span>](#ProcessPayment2)

- [<span data-ttu-id="2b90e-134">Импорт новых версий стандартных конфигураций формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-134">Import new versions of the standard ER format configurations</span></span>](#ImportERSolution2)

    - [<span data-ttu-id="2b90e-135">Импорт новых версий стандартных конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-135">Import new versions of the standard ER configurations</span></span>](#ImportERFormat2)
    - [<span data-ttu-id="2b90e-136">Проверка импортированных конфигураций формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-136">Review the imported ER format configurations</span></span>](#ReviewImportedERFormat)

- [<span data-ttu-id="2b90e-137">Адаптация изменений в новой версии импортированного формата в пользовательском формате</span><span class="sxs-lookup"><span data-stu-id="2b90e-137">Adopt the changes in the new version of an imported format in a custom format</span></span>](#AdoptNewBaseVersion)

    - [<span data-ttu-id="2b90e-138">Завершение текущей черновой версии пользовательского формата</span><span class="sxs-lookup"><span data-stu-id="2b90e-138">Complete the current draft version of a custom format</span></span>](#CompleteDerivedFormat)
    - [<span data-ttu-id="2b90e-139">Перемещение пользовательского формата на новую базовую версию</span><span class="sxs-lookup"><span data-stu-id="2b90e-139">Rebase a custom format to a new base version</span></span>](#RebaseDerivedFormat)
    - [<span data-ttu-id="2b90e-140">Обработка платежа поставщику с помощью перемещенного формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-140">Process a vendor payment by using a rebased ER format</span></span>](#ProcessPayment3)

- [<span data-ttu-id="2b90e-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2b90e-141">Additional resources</span></span>](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a><span data-ttu-id="2b90e-142">Настройка платформы электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-142">Configure the ER framework</span></span>

<span data-ttu-id="2b90e-143">В качестве пользователя в роли функционального консультанта по электронной отчетности вам необходимо настроить минимальный набор параметров ER, прежде чем можно будет начать использовать платформу электронной отчетности для создания пользовательской версии стандартного формата электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="2b90e-143">As a user in the Electronic Reporting Functional Consultant role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design a custom version of a standard ER format.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="2b90e-144">Настройка параметров ER</span><span class="sxs-lookup"><span data-stu-id="2b90e-144">Configure ER parameters</span></span>

1. <span data-ttu-id="2b90e-145">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-145">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2b90e-146">На странице **Конфигурации локализации** в разделе **Связанные ссылки** выберите **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-146">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="2b90e-147">На странице **Параметры электронной отчетности** на вкладке **Общие сведения** задайте для параметра **Включить режим конструктора** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-147">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="2b90e-148">На вкладке **Вложения** установите следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="2b90e-148">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="2b90e-149">В поле **Конфигурации** выберите тип **Файл** для компании **USMF**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-149">In the **Configurations** field, select the **File** type for the **USMF** company.</span></span>
    - <span data-ttu-id="2b90e-150">В полях **Архив заданий**, **Временная**, **Базовый** и **Другие** выберите тип **Файл**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-150">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="2b90e-151">Дополнительные сведения о настройке параметров электронной отчетности см. в разделе [Настройка платформы электронной отчетности](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2b90e-151">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="2b90e-152">Активация поставщика конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-152">Activate an ER configuration provider</span></span>

<span data-ttu-id="2b90e-153">Каждая добавленная конфигурация электронной отчетности помечается как принадлежащая поставщику конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="2b90e-153">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="2b90e-154">Для этой цели используется поставщик конфигурации электронной отчетности, который активирован в рабочей области **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-154">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="2b90e-155">Поэтому перед началом добавления или изменения конфигураций электронной отчетности необходимо активировать поставщика конфигурации электронной отчетности в рабочей области **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-155">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="2b90e-156">Только владелец конфигурации электронной отчетности может редактировать ее.</span><span class="sxs-lookup"><span data-stu-id="2b90e-156">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="2b90e-157">Поэтому перед редактированием конфигурации электронной отчетности необходимо активировать соответствующего поставщика конфигурации электронной отчетности в рабочей области **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-157">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="2b90e-158">Просмотр списка поставщиков конфигурации электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-158">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="2b90e-159">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-159">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2b90e-160">На странице **Конфигурации локализации** в разделе **Связанные ссылки** выберите **Поставщики конфигураций**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-160">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="2b90e-161">На странице **Таблица поставщиков конфигураций** каждая запись поставщика имеет уникальное имя и URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="2b90e-161">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="2b90e-162">Проверьте содержимое данной страницы.</span><span class="sxs-lookup"><span data-stu-id="2b90e-162">Review the contents of this page.</span></span> <span data-ttu-id="2b90e-163">Если запись для **Litware, Inc.** (`https://www.litware.com`) уже существует, пропустите следующую процедуру, [Добавление нового поставщика конфигурации электронной отчетности](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="2b90e-163">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="2b90e-164">Добавление нового поставщика конфигурации электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-164">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="2b90e-165">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-165">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2b90e-166">На странице **Конфигурации локализации** в разделе **Связанные ссылки** выберите **Поставщики конфигураций**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-166">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="2b90e-167">На странице **Поставщики конфигураций** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-167">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="2b90e-168">В поле **Имя** введите **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="2b90e-168">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="2b90e-169">В поле **Интернет-адрес** введите `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="2b90e-169">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="2b90e-170">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-170">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="2b90e-171">Активация поставщика конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-171">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="2b90e-172">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2b90e-173">На странице **Конфигурации локализации** в разделе **Поставщики конфигураций** выберите плитку **Litware, Inc.**, затем выберите **Установить активные**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-173">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="2b90e-174">Дополнительные сведения о поставщиках конфигурации электронной отчетности см. в разделе [Создание поставщиков конфигураций и пометка их как активных](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="2b90e-174">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a><span data-ttu-id="2b90e-175">Импорт стандартных конфигураций формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-175">Import the standard ER format configurations</span></span>

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a><span data-ttu-id="2b90e-176">Импорт стандартных конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-176">Import the standard ER configurations</span></span>

<span data-ttu-id="2b90e-177">Чтобы добавить стандартные конфигурации электронной отчетности в текущий экземпляр Microsoft Dynamics 365 Finance, необходимо импортировать их из [репозитория](general-electronic-reporting.md#Repository) электронной отчетности, который был настроен для этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2b90e-177">To add the standard ER configurations to your current instance of Microsoft Dynamics 365 Finance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="2b90e-178">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-178">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2b90e-179">На странице **Конфигурации локализации** в разделе **Поставщики конфигураций** выберите плитку **Майкрософт**, затем выберите **Репозитории**, чтобы просмотреть список репозиториев для поставщика Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2b90e-179">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="2b90e-180">На странице **Репозитории конфигураций** выберите репозиторий типа **Глобальный**, затем выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-180">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="2b90e-181">Если будет предложено выполнить проверку подлинности для подключения к службе Regulatory Configuration Service, следуйте инструкциям по проверке подлинности.</span><span class="sxs-lookup"><span data-stu-id="2b90e-181">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="2b90e-182">На странице **Репозиторий конфигураций** в дереве конфигураций на левой панели выберите конфигурацию формата **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-182">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="2b90e-183">На экспресс-вкладке **Версии** выберите версию **1.1** выбранной конфигурации формата электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="2b90e-183">On the **Versions** FastTab, select version **1.1** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="2b90e-184">Выберите **Импорт** для загрузки выбранной версии из глобального репозитория в текущий экземпляр Finance.</span><span class="sxs-lookup"><span data-stu-id="2b90e-184">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Страница репозитория конфигурации](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> <span data-ttu-id="2b90e-186">При возникновении проблем с доступом к [глобальному репозиторию](er-download-configurations-global-repo.md) можно вместо этого [загрузить конфигурации](download-electronic-reporting-configuration-lcs.md) из служб Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="2b90e-186">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a><span data-ttu-id="2b90e-187">Проверка импортированных конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-187">Review the imported ER configurations</span></span>

1. <span data-ttu-id="2b90e-188">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-188">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2b90e-189">На странице **Конфигурации локализации** в разделе **Конфигурации** выберите плитку **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-189">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="2b90e-190">На странице **Конфигурации** в дереве конфигураций на левой панели разверните **Модель платежа**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-190">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**.</span></span>
4. <span data-ttu-id="2b90e-191">Обратите внимание, что в дополнение к выбранному формату **BACS (UK)** были импортированы другие необходимые конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="2b90e-191">Notice that, in addition to the selected **BACS (UK)** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="2b90e-192">Убедитесь, что в дереве конфигураций доступны следующие конфигурации электронной отчетности:</span><span class="sxs-lookup"><span data-stu-id="2b90e-192">Make sure that the following ER configurations are available in the configuration tree:</span></span>

    - <span data-ttu-id="2b90e-193">**Модель платежа** — эта конфигурация содержит компонент [модели данных](general-electronic-reporting.md#data-model-and-model-mapping-components) электронной отчетности, который представляет структуру данных бизнес-домена платежа.</span><span class="sxs-lookup"><span data-stu-id="2b90e-193">**Payment model** – This configuration contains the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the payment business domain.</span></span>
    - <span data-ttu-id="2b90e-194">**Сопоставление модели платежа 1611** — эта конфигурация содержит компонент [сопоставления моделей](general-electronic-reporting.md#data-model-and-model-mapping-components) электронной отчетности, описывающий заполнение модели данных данными приложения во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="2b90e-194">**Payment model mapping 1611** – This configuration contains the [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that describes how the data model is filled in with application data at runtime.</span></span>
    - <span data-ttu-id="2b90e-195">**BACS (UK)** — данная конфигурация содержит [формат](general-electronic-reporting.md#FormatComponentOutbound) и компоненты сопоставления форматов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="2b90e-195">**BACS (UK)** – This configuration contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="2b90e-196">Компонент формата определяет макет отчета.</span><span class="sxs-lookup"><span data-stu-id="2b90e-196">The format component specifies the report layout.</span></span> <span data-ttu-id="2b90e-197">Компонент сопоставления формата содержит источник данных модели и определяет, как заполняется макет отчета при помощи этого источника данных во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="2b90e-197">The format mapping component contains the model data source and specifies how the report layout is filled in by using this data source at runtime.</span></span>

![Страница конфигураций](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a><span data-ttu-id="2b90e-199">Подготовка обработки платежа поставщику</span><span class="sxs-lookup"><span data-stu-id="2b90e-199">Prepare a vendor payment for processing</span></span>

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a><span data-ttu-id="2b90e-200">Добавление банковской информации для счета поставщика</span><span class="sxs-lookup"><span data-stu-id="2b90e-200">Add bank information for a vendor account</span></span>

<span data-ttu-id="2b90e-201">Необходимо добавить банковскую информацию для счета поставщика, на который позднее будете ссылаться в зарегистрированном платеже.</span><span class="sxs-lookup"><span data-stu-id="2b90e-201">You must add bank information for a vendor account that will be referred to later in a registered payment.</span></span>

1. <span data-ttu-id="2b90e-202">Перейдите в раздел **Расчеты с поставщиками** \> **Поставщики** \> **Все поставщики**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-202">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="2b90e-203">На странице **Все поставщики** выберите счет поставщика **GB_SI_000001**, затем в области действий на вкладке **Поставщик** в группе **Настройка** выберите **Банковские счета**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-203">On the **All vendors** page, select the **GB_SI_000001** vendor account, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="2b90e-204">На странице **Банковские счета поставщика** выберите **Создать**, затем введите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="2b90e-204">On the **Vendor bank accounts** page, select **New**, and then enter the following information:</span></span>

    1. <span data-ttu-id="2b90e-205">В поле **Банковский счет** введите **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-205">In the **Bank account** field, enter **GBP OPER**.</span></span>
    2. <span data-ttu-id="2b90e-206">В поле **Банковские группы** выберите **BankGBP**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-206">In the **Bank groups** field, select **BankGBP**.</span></span>
    3. <span data-ttu-id="2b90e-207">В поле **Номер банковского счета** введите **202015**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-207">In the **Bank account number** field, enter **202015**.</span></span>
    4. <span data-ttu-id="2b90e-208">В поле **Код SWIFT** введите <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-208">In the **SWIFT code** field, enter <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span></span>
    5. <span data-ttu-id="2b90e-209">В поле **IBAN** введите **GB33BUKB20201555555555**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-209">In the **IBAN** field, enter **GB33BUKB20201555555555**.</span></span>
    6. <span data-ttu-id="2b90e-210">В поле **Номер маршрутизации** сохраните значение по умолчанию <a id="DefineRoutingNumber"></a>**123456**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-210">In the **Routing number** field, keep the default value, <a id="DefineRoutingNumber"></a>**123456**.</span></span>

    ![Страница банковских счетов поставщика](./media/er-quick-start2-bank-account.png)

4. <span data-ttu-id="2b90e-212">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-212">Select **Save**.</span></span>
5. <span data-ttu-id="2b90e-213">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2b90e-213">Close the page.</span></span>
6. <span data-ttu-id="2b90e-214">На странице **Все поставщики** откройте счет поставщика **GB_SI_000001**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-214">On the **All vendors** page, open the **GB_SI_000001** vendor account.</span></span>
7. <span data-ttu-id="2b90e-215">На странице сведения о поставщике выберите **Правка**, чтобы сделать страницу редактируемой, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="2b90e-215">On the vendor details page, select **Edit** to make the page editable, if required.</span></span>
8. <span data-ttu-id="2b90e-216">На экспресс-вкладке **Платеж** в поле **Банковский счет** выберите **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-216">On the **Payment** FastTab, in the **Bank account** field, select **GBP OPER**.</span></span>

    ![Страница сведений о поставщике](./media/er-quick-start2-bank-account-reference.png)

9. <span data-ttu-id="2b90e-218">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-218">Select **Save**.</span></span>
10. <span data-ttu-id="2b90e-219">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2b90e-219">Close the page.</span></span>

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a><span data-ttu-id="2b90e-220">Ввод платежа поставщику</span><span class="sxs-lookup"><span data-stu-id="2b90e-220">Enter a vendor payment</span></span>

<span data-ttu-id="2b90e-221">Необходимо ввести новый платеж поставщику с помощью [предложения по оплате](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span><span class="sxs-lookup"><span data-stu-id="2b90e-221">You must enter a new vendor payment by using a [payment proposal](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span></span>

1. <span data-ttu-id="2b90e-222">Перейдите в раздел **Расчеты с поставщиками** \> **Платежи** \> **Журнал платежей поставщикам**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-222">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="2b90e-223">На странице **Журнал платежей поставщикам** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-223">On the **Vendor payment journal** page, select **New**.</span></span>
3. <span data-ttu-id="2b90e-224">В поле **Имя** выберите **VendPay**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-224">In the **Name** field, select **VendPay**.</span></span>
4. <span data-ttu-id="2b90e-225">Выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-225">Select **Lines**.</span></span>
5. <span data-ttu-id="2b90e-226">Выберите **Предложение по оплате** \> **Создать предложение по оплате**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-226">Select **Payment proposal** \> **Create payment proposal**.</span></span>
6. <span data-ttu-id="2b90e-227">В диалоговом окне **Предложение по оплате поставщику** настройте условия для фильтрации записей только для счета поставщика **GB_SI_000001**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-227">In the **Vendor payment proposal** dialog box, configure conditions to filter for records for the **GB_SI_000001** vendor account only, and then select **OK**.</span></span>
7. <span data-ttu-id="2b90e-228">Выберите строку для счета **00000007_Inv**, затем выберите **Создать платеж**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-228">Select the line for the **00000007_Inv** invoice, and then select **Create payment**.</span></span>

    ![Диалоговое окно предложения по оплате поставщику](./media/er-quick-start2-payment-proposal.png)

8. <span data-ttu-id="2b90e-230">Убедитесь, что введенный платеж настроен на использование **электронного** метода оплаты.</span><span class="sxs-lookup"><span data-stu-id="2b90e-230">Verify that the payment that is entered is configured to use the **Electronic** method of payment.</span></span>

    ![Страница платежей поставщикам](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a><span data-ttu-id="2b90e-232">Обработка платежа поставщику с помощью стандартного формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-232">Process a vendor payment by using the standard ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a><span data-ttu-id="2b90e-233">Настройка способа оплаты с помощью электронного платежа</span><span class="sxs-lookup"><span data-stu-id="2b90e-233">Set up the electronic payment method</span></span>

<span data-ttu-id="2b90e-234">Необходимо настроить электронный способ оплаты, чтобы он использовал импортированную конфигурацию формата электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="2b90e-234">You must configure the electronic method of payment so that it uses the imported ER format configuration.</span></span>

1. <span data-ttu-id="2b90e-235">Перейдите в раздел **Расчеты с поставщиками** \> **Настройка платежей** \> **Способы оплаты**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-235">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="2b90e-236">На странице **Методы оплаты — поставщики** выберите **электронный** способ оплаты на левой панели.</span><span class="sxs-lookup"><span data-stu-id="2b90e-236">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="2b90e-237">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-237">Select **Edit**.</span></span>
4. <span data-ttu-id="2b90e-238">На экспресс-вкладке **Форматы файлов** установите для параметра **Универсальный электронный формат экспорта** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-238">On the **File formats** FastTab, set the **General electronic Export format** option to **Yes**.</span></span>
5. <span data-ttu-id="2b90e-239">В поле **Экспорт конфигурации формата** выберите конфигурацию формата **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-239">In the **Export format configuration** field, select the **BACS (UK)** format configuration.</span></span>

    ![Страница "Способы оплаты - поставщики"](./media/er-quick-start2-method-of-payment1.png)

6. <span data-ttu-id="2b90e-241">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-241">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a><span data-ttu-id="2b90e-242">Обработка платежа поставщику</span><span class="sxs-lookup"><span data-stu-id="2b90e-242">Process a vendor payment</span></span>

1. <span data-ttu-id="2b90e-243">Перейдите в раздел **Расчеты с поставщиками** \> **Платежи** \> **Журнал платежей поставщикам**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-243">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="2b90e-244">На странице **Журнал платежей поставщику** выберите добавленный ранее журнал платежей, затем выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-244">On the **Vendor payment journal** page, select the payment journal that you added earlier, and then select **Lines**.</span></span>
3. <span data-ttu-id="2b90e-245">На странице **Платежи поставщикам** выберите **Создать платежи**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-245">On the **Vendor payments** page, select **Generate payments**.</span></span>
4. <span data-ttu-id="2b90e-246">В диалоговом окне **Создать платежи** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="2b90e-246">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="2b90e-247">В поле **Способ оплаты** выберите **Электронный**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-247">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="2b90e-248">В поле **Банковский счет** выберите **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-248">In the **Bank account** field, select **GBSI OPER**.</span></span>

5. <span data-ttu-id="2b90e-249">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-249">Select **OK**.</span></span>
6. <span data-ttu-id="2b90e-250">В диалоговом окне **Параметры электронного отчета** установите для параметра **Печать контрольного отчета** значение **Да**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-250">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    ![Страница диалогового окна параметров электронной отчетности](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > <span data-ttu-id="2b90e-252">В дополнение к файлу платежа теперь можно создать контрольный отчет.</span><span class="sxs-lookup"><span data-stu-id="2b90e-252">In addition to the payment file, you can now generate the control report.</span></span>

7. <span data-ttu-id="2b90e-253">Загрузите ZIP-файл, затем извлеките из него следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="2b90e-253">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="2b90e-254">Контрольный отчет в формате Excel</span><span class="sxs-lookup"><span data-stu-id="2b90e-254">The control report in Excel format</span></span>
    - <span data-ttu-id="2b90e-255">Файл платежей в формате TXT</span><span class="sxs-lookup"><span data-stu-id="2b90e-255">The payment file in TXT format</span></span>

        <span data-ttu-id="2b90e-256">Обратите внимание, что в соответствии со [структурой](#PositionRoutingNumber) указанного формата электронной отчетности строка платежа в созданном файле начинается с кода банка, который был [определен](#DefineRoutingNumber) для настроенного банковского счета.</span><span class="sxs-lookup"><span data-stu-id="2b90e-256">Notice that, in accordance with the [structure](#PositionRoutingNumber) of the provided ER format, the payment line in the generated file starts with the routing number that was [defined](#DefineRoutingNumber) for the configured bank account.</span></span>

        ![Файл платежей в формате TXT](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a><span data-ttu-id="2b90e-258">Настройка стандартного формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-258">Customize the standard ER format</span></span>

<span data-ttu-id="2b90e-259">Для примера, показанного в этом разделе, вы хотите использовать конфигурации электронной отчетности, предоставляемые корпорацией Майкрософт, для создания файлов платежей поставщиков в формате BACS, но необходимо добавить настройки для поддержки требований конкретного банка.</span><span class="sxs-lookup"><span data-stu-id="2b90e-259">For the example that is shown in this section, you want to use the ER configurations that are provided by Microsoft to generate vendor payment files in BACS format, but you must add a customization to support the requirements of a specific bank.</span></span> <span data-ttu-id="2b90e-260">Кроме того, необходимо иметь возможность обновить пользовательский формат, когда станут доступны новые версии конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="2b90e-260">You also want to be able to upgrade your custom format when new versions of ER configurations become available.</span></span> <span data-ttu-id="2b90e-261">Однако необходимо иметь возможность выполнять обновление с самыми низкими затратами.</span><span class="sxs-lookup"><span data-stu-id="2b90e-261">However, you want to be able to do the upgrade at the lowest cost.</span></span>

<span data-ttu-id="2b90e-262">В этом случае, как представитель Litware, Inc., необходимо создать (наследовать) новую конфигурацию формата электронной отчетности, используя конфигурацию **BACS (UK)**, предоставляемую корпорацией Майкрософт в качестве базы.</span><span class="sxs-lookup"><span data-stu-id="2b90e-262">In this case, as the representative of Litware, Inc., you must create (derive) a new ER format configuration by using the **BACS (UK)** Microsoft-provided configuration as a base.</span></span>

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a><span data-ttu-id="2b90e-263">Создание пользовательского формата</span><span class="sxs-lookup"><span data-stu-id="2b90e-263">Create a custom format</span></span>

1. <span data-ttu-id="2b90e-264">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-264">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2b90e-265">На странице **Конфигурации** в дереве конфигураций на левой панели разверните **Модель платежа**, затем выберите **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-265">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span> <span data-ttu-id="2b90e-266">Litware, Inc. будет использовать конфигурацию формата электронной отчетности версии 1.1 в качестве основы для пользовательской версии.</span><span class="sxs-lookup"><span data-stu-id="2b90e-266">Litware, Inc. will use version 1.1 of this ER format configuration as the base for the custom version.</span></span>
3. <span data-ttu-id="2b90e-267">Выберите **Создать конфигурацию**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="2b90e-267">Select **Create configuration** to open the drop-down dialog box.</span></span> <span data-ttu-id="2b90e-268">Вы можете использовать диалоговое окно, чтобы создать новую конфигурацию для пользовательского формата платежей.</span><span class="sxs-lookup"><span data-stu-id="2b90e-268">You can use this dialog box to create a new configuration for a custom payment format.</span></span>
4. <span data-ttu-id="2b90e-269">В группе полей **Создать** выберите параметр **Производное от имени: BACS (UK), Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-269">In the **New** field group, select the **Derive from Name: BACS (UK), Microsoft** option.</span></span>
5. <span data-ttu-id="2b90e-270">В поле **Имя** введите **BACS (Соединенное Королевство, пользовательский)**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-270">In the **Name** field, enter **BACS (UK custom)**.</span></span>

    ![Раскрывающееся диалоговое окно создания конфигурации](./media/er-quick-start2-add-derived-format.png)

6. <span data-ttu-id="2b90e-272">Выберите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-272">Select **Create configuration**.</span></span>

<span data-ttu-id="2b90e-273">Создана версии 1.1.1 конфигурация формата электронной отчетности **BACS (Соединенное Королевство, пользовательский)**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-273">Version 1.1.1 of the **BACS (UK custom)** ER format configuration is created.</span></span> <span data-ttu-id="2b90e-274">Эта версия имеет [статус](general-electronic-reporting.md#component-versioning) **Черновик** и может редактироваться.</span><span class="sxs-lookup"><span data-stu-id="2b90e-274">This version has a [status](general-electronic-reporting.md#component-versioning) of **Draft** and can be edited.</span></span> <span data-ttu-id="2b90e-275">Текущее содержимое пользовательского формата электронной отчетности соответствует содержимому формата, предоставленного корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2b90e-275">The current content of your custom ER format matches the content of the format that is provided by Microsoft.</span></span>

![Страница конфигураций](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a><span data-ttu-id="2b90e-277">Изменение пользовательского формата</span><span class="sxs-lookup"><span data-stu-id="2b90e-277">Edit a custom format</span></span>

<span data-ttu-id="2b90e-278">Необходимо настроить пользовательский формат, чтобы он соответствовал требованиям конкретного банка.</span><span class="sxs-lookup"><span data-stu-id="2b90e-278">You must configure your custom format so that it meets bank-specific requirements.</span></span> <span data-ttu-id="2b90e-279">Например, банк может требовать, чтобы создаваемые файлы платежа содержали код SWIFT банка, которому назначена роль агента в обработанном платеже поставщика.</span><span class="sxs-lookup"><span data-stu-id="2b90e-279">For example, a bank might require that payment files that are generated include the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of a bank that is assigned the agent role in the processed vendor payment.</span></span> <span data-ttu-id="2b90e-280">Коды SWIFT являются международными кодами банка, которые определяют конкретные банки во всем мире.</span><span class="sxs-lookup"><span data-stu-id="2b90e-280">SWIFT codes are international bank codes that identify specific banks worldwide.</span></span> <span data-ttu-id="2b90e-281">Они также называются идентификационными кодами банка (БИК).</span><span class="sxs-lookup"><span data-stu-id="2b90e-281">They are also known as Bank Identifier Codes (BICs).</span></span> <span data-ttu-id="2b90e-282">Код SWIFT должен иметь длину 11 символов и должен быть введен в начале каждой строки платежа в созданном файле платежа.</span><span class="sxs-lookup"><span data-stu-id="2b90e-282">The SWIFT code must be 11 characters long, and it must be entered at the beginning of every payment line in a generated payment file.</span></span>

1. <span data-ttu-id="2b90e-283">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-283">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2b90e-284">На странице **Конфигурации** в дереве конфигураций на левой панели разверните **Модель платежа**, затем выберите **BACS (Соединенное Королевство, пользовательский)**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-284">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="2b90e-285">На экспресс-вкладке **Версии** выберите версию **1.1.1** выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2b90e-285">On the **Versions** FastTab, select version **1.1.1** of the selected configuration.</span></span>
4. <span data-ttu-id="2b90e-286">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-286">Select **Designer**.</span></span>
5. <span data-ttu-id="2b90e-287">На странице **Конструктор форматов** выберите **Показать сведения** для просмотра дополнительных сведений об элементах формата.</span><span class="sxs-lookup"><span data-stu-id="2b90e-287">On the **Format designer** page, select **Show details** to view more information about the format elements.</span></span>
6. <span data-ttu-id="2b90e-288">Разверните и изучите следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="2b90e-288">Expand and review the following elements:</span></span>

    - <span data-ttu-id="2b90e-289">Элемент **BACSReportsFolder** типа **Папка**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-289">The **BACSReportsFolder** element of the **Folder** type.</span></span> <span data-ttu-id="2b90e-290">Этот элемент используется для создания выходных данных в формате ZIP.</span><span class="sxs-lookup"><span data-stu-id="2b90e-290">This element is used to generate output in ZIP format.</span></span>
    - <span data-ttu-id="2b90e-291">Элемент **файл** типа **Файл**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-291">The **file** element of the **File** type.</span></span> <span data-ttu-id="2b90e-292">Этот элемент используется для создания файла платежей в формате TXT.</span><span class="sxs-lookup"><span data-stu-id="2b90e-292">This element is used to generate a payment file in TXT format.</span></span>
    - <span data-ttu-id="2b90e-293">Элемент **транзакции** типа **Последовательность**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-293">The **transactions** element of the **Sequence** type.</span></span> <span data-ttu-id="2b90e-294">Этот элемент используется для создания одной строки платежа в файле платежей.</span><span class="sxs-lookup"><span data-stu-id="2b90e-294">This element is used to generate a single payment line in a payment file.</span></span>
    - <span data-ttu-id="2b90e-295">Элемент **транзакция** типа **Последовательность**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-295">The **transaction** element of the **Sequence** type.</span></span> <span data-ttu-id="2b90e-296">Этот элемент используется для создания отдельных полей одной строки платежа.</span><span class="sxs-lookup"><span data-stu-id="2b90e-296">This element is used to generate individual fields of a single payment line.</span></span>

7. <span data-ttu-id="2b90e-297">Выберите элемент **транзакция**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-297">Select the **transaction** element.</span></span>

    ![Элемент "транзакция" в конструкторе операций электронной отчетности](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <span data-ttu-id="2b90e-299">Представленный отчет настроен таким образом, что <a id="PositionRoutingNumber"></a>каждая строка платежа начинается с кода банка.</span><span class="sxs-lookup"><span data-stu-id="2b90e-299">The provided report is configured so that <a id="PositionRoutingNumber"></a>every payment line starts with the bank routing number.</span></span> <span data-ttu-id="2b90e-300">Для этой цели используется элемент формата **vendBankRouteNum**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-300">The **vendBankRouteNum** format element is used for this purpose.</span></span> 

8. <span data-ttu-id="2b90e-301">Выберите **Добавить**, затем выберите тип **Текст\\Строка** для добавляемого элемента формата:</span><span class="sxs-lookup"><span data-stu-id="2b90e-301">Select **Add**, and then select the **Text\\String** type of the format element that you're adding:</span></span>

    1. <span data-ttu-id="2b90e-302">В поле **Имя** введите **vendBankSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-302">In the **Name** field, enter **vendBankSWIFT**.</span></span>
    2. <span data-ttu-id="2b90e-303">В поле **Минимальная длина** введите **11**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-303">In the **Minimum length** field, enter **11**.</span></span>
    3. <span data-ttu-id="2b90e-304">В поле **Максимальная длина** введите **11**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-304">In the **Maximum length** field, enter **11**.</span></span>
    4. <span data-ttu-id="2b90e-305">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-305">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2b90e-306">Элемент **vendBankSWIFT** будет использоваться для ввода SWIFT-кода банка поставщика в созданных файлах.</span><span class="sxs-lookup"><span data-stu-id="2b90e-306">The **vendBankSWIFT** element will be used to enter the SWIFT code of a vendor bank in generated files.</span></span>

9. <span data-ttu-id="2b90e-307">В дереве структуры формата выберите **vendBankSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-307">In the format structure tree, select **vendBankSWIFT**.</span></span>
10. <span data-ttu-id="2b90e-308">Выберите **Вверх**, чтобы переместить выбранный элемент форматирования на один уровень вверх.</span><span class="sxs-lookup"><span data-stu-id="2b90e-308">Select **Move up** to move the selected format element up one level.</span></span> <span data-ttu-id="2b90e-309">Повторяйте этот шаг до тех пор, пока элемент **vendBankSWIFT** не станет <a id="PositionSWIFTCode"></a>первым элементом родительского элемента **транзакция**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-309">Repeat this step until the **vendBankSWIFT** element is the <a id="PositionSWIFTCode"></a>first element under the parent **transaction** element.</span></span>

    ![VendBankSWIFT в качестве первого элемента в проводке в конструкторе операций электронной отчетности](./media/er-quick-start2-derived-format1.png)

11. <span data-ttu-id="2b90e-311">Когда **vendBankSWIFT** все еще выбран в дереве структуры формата, выберите вкладку **Сопоставление**, затем — источник данных **модели**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-311">While the **vendBankSWIFT** is still selected in the format structure tree, select the **Mapping** tab, and then expand the **model** data source.</span></span>
12. <span data-ttu-id="2b90e-312">Разверните узел **model.Payment** \> **model.Payment.CreditorAgent** и выберите поле источника данных **model.Payment.CreditorAgent.BICFI**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-312">Expand **model.Payment** \> **model.Payment.CreditorAgent**, and select the **model.Payment.CreditorAgent.BICFI** data source field.</span></span> <span data-ttu-id="2b90e-313">Это поле источника данных представляет SWIFT-код банка поставщика, которому назначена роль агента в обработанном платеже поставщику.</span><span class="sxs-lookup"><span data-stu-id="2b90e-313">This data source field exposes the SWIFT code of a vendor bank that is assigned the agent role in the processed vendor payment.</span></span>
13. <span data-ttu-id="2b90e-314">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-314">Select **Bind**.</span></span> <span data-ttu-id="2b90e-315">Элемент формата **vendBankSWIFT** теперь привязан к полю источника данных **model.Payment.CreditorAgent.BICFI**, так что коды SWIFT будут вводиться в создаваемые файлы платежей.</span><span class="sxs-lookup"><span data-stu-id="2b90e-315">The **vendBankSWIFT** format element is now bound with the **model.Payment.CreditorAgent.BICFI** data source field, so that SWIFT codes will be entered in generated payment files.</span></span>

    ![Элемент форматирования vendBankSWIFT, связанный с полем источника model.Payment.CreditorAgent.BICFI в конструкторе операций электронной отчетности](./media/er-quick-start2-derived-format2.png)

14. <span data-ttu-id="2b90e-317">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-317">Select **Save**.</span></span>
15. <span data-ttu-id="2b90e-318">Закройте страницу конструктора.</span><span class="sxs-lookup"><span data-stu-id="2b90e-318">Close the designer page.</span></span>

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a><span data-ttu-id="2b90e-319">Пометка пользовательского формата как готового к запуску</span><span class="sxs-lookup"><span data-stu-id="2b90e-319">Mark a custom format as runnable</span></span>

<span data-ttu-id="2b90e-320">Теперь, когда была создана первая версия пользовательского формата и она имеет статус **Черновик**, ее можно запустить для целей тестирования.</span><span class="sxs-lookup"><span data-stu-id="2b90e-320">Now that the first version of your custom format has been created and has a status of **Draft**, you can run it for testing purposes.</span></span> <span data-ttu-id="2b90e-321">Для выполнения отчета необходимо обработать платеж поставщику с помощью метода платежа, который ссылается на пользовательский формат электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="2b90e-321">To run the report, you must process a vendor payment by using the payment method that refers to your custom ER format.</span></span> <span data-ttu-id="2b90e-322">По умолчанию при вызове формата электронной отчетности из приложения [учитываются](general-electronic-reporting.md#component-versioning) только те версии, которые имеют статус **Завершено** и **Общие**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-322">By default, when you call an ER format from the application, only versions that have a status of **Completed** or **Shared** are [considered](general-electronic-reporting.md#component-versioning).</span></span> <span data-ttu-id="2b90e-323">Это позволяет предотвратить использование в форматах электронной отчетности незаконченных макетов.</span><span class="sxs-lookup"><span data-stu-id="2b90e-323">This behavior helps prevent ER formats that have unfinished designs from being used.</span></span> <span data-ttu-id="2b90e-324">Однако для выполнения тестов можно заставить приложение использовать версию формата электронной отчетности, имеющую статус **Черновик**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-324">However, for your test runs, you can force the application to use the version of your ER format that has a status of **Draft**.</span></span> <span data-ttu-id="2b90e-325">Таким образом, можно откорректировать текущую версию формата, если требуется внести изменения.</span><span class="sxs-lookup"><span data-stu-id="2b90e-325">In this way, you can adjust the current format version if any modifications are required.</span></span> <span data-ttu-id="2b90e-326">Дополнительные сведения см. в разделе [Применимость](electronic-reporting-destinations.md#applicability).</span><span class="sxs-lookup"><span data-stu-id="2b90e-326">For more information, see [Applicability](electronic-reporting-destinations.md#applicability).</span></span>

<span data-ttu-id="2b90e-327">Чтобы использовать черновую версию формата электронной отчетности, необходимо явно пометить формат электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="2b90e-327">To use the draft version of an ER format, you must explicitly mark the ER format.</span></span>

1. <span data-ttu-id="2b90e-328">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-328">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2b90e-329">На странице **Конфигурации** в области действий на вкладке **Конфигурации** в группе **Дополнительные параметры** выберите **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-329">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="2b90e-330">В диалоговом окне **Параметры пользователя** установите для параметра **Параметры выполнения** значение **Да**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-330">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
4. <span data-ttu-id="2b90e-331">При необходимости выберите **Правка**, чтобы сделать текущую страницу редактируемой.</span><span class="sxs-lookup"><span data-stu-id="2b90e-331">Select **Edit** to make the current page editable, as required.</span></span>
5. <span data-ttu-id="2b90e-332">В дереве конфигурации в левой области выберите **BACS (UK, пользовательский)**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-332">In the configuration tree in the left pane, select **BACS (UK custom)**.</span></span>
6. <span data-ttu-id="2b90e-333">Для параметра **Выполнить черновик** выберите значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-333">Set the **Run Draft** option to **Yes**.</span></span>

    ![Параметр "Выполнить черновик" на странице конфигурации](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a><span data-ttu-id="2b90e-335">Обработка платежа поставщику с помощью пользовательского формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-335">Process a vendor payment by using the custom ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a><span data-ttu-id="2b90e-336">Настройка способа оплаты с помощью электронного платежа</span><span class="sxs-lookup"><span data-stu-id="2b90e-336">Set up the electronic payment method</span></span>

<span data-ttu-id="2b90e-337">Необходимо настроить электронный способ оплаты, чтобы пользовательский формат электронной отчетности использовался для обработки платежей поставщикам.</span><span class="sxs-lookup"><span data-stu-id="2b90e-337">You must configure the electronic method of payment so that your custom ER format is used to process vendor payments.</span></span>

1. <span data-ttu-id="2b90e-338">Перейдите в раздел **Расчеты с поставщиками** \> **Настройка платежей** \> **Способы оплаты**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-338">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="2b90e-339">На странице **Методы оплаты — поставщики** выберите **электронный** способ оплаты на левой панели.</span><span class="sxs-lookup"><span data-stu-id="2b90e-339">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="2b90e-340">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-340">Select **Edit**.</span></span>
4. <span data-ttu-id="2b90e-341">На экспресс-вкладке **Формат файла** установите для параметра **Универсальный электронный формат экспорта** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-341">On the **File format** FastTab, set the **General electronic export format** option to **Yes**.</span></span>
5. <span data-ttu-id="2b90e-342">В поле **Экспорт конфигурации формата** выберите конфигурацию формата **BACS (UK, пользовательский)**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-342">In the **Export format configuration** field, select the **BACS (UK custom)** format configuration.</span></span>

    ![Страница "Способы оплаты - поставщики"](./media/er-quick-start2-method-of-payment2.png)

6. <span data-ttu-id="2b90e-344">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-344">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a><span data-ttu-id="2b90e-345">Обработка платежа поставщику</span><span class="sxs-lookup"><span data-stu-id="2b90e-345">Process a vendor payment</span></span>

1. <span data-ttu-id="2b90e-346">Перейдите в раздел **Расчеты с поставщиками** \> **Платежи** \> **Журнал платежей поставщикам**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-346">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="2b90e-347">На странице **Журнал платежей поставщику** выберите созданный ранее журнал платежей.</span><span class="sxs-lookup"><span data-stu-id="2b90e-347">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="2b90e-348">Выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-348">Select **Lines**.</span></span>
4. <span data-ttu-id="2b90e-349">На странице **Платежи поставщикам** над сеткой выберите **Статус платежа** \> **Нет**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-349">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="2b90e-350">Выберите **Создать платеж**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-350">Select **Generate payment**.</span></span>
6. <span data-ttu-id="2b90e-351">В диалоговом окне **Создать платежи** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="2b90e-351">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="2b90e-352">В поле **Способ оплаты** выберите **Электронный**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-352">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="2b90e-353">В поле **Банковский счет** выберите **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-353">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="2b90e-354">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-354">Select **OK**.</span></span>
8. <span data-ttu-id="2b90e-355">В диалоговом окне **Параметры электронного отчета** установите для параметра **Печать контрольного отчета** значение **Да**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-355">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2b90e-356">В дополнение к файлу платежа можно создать только контрольный отчет.</span><span class="sxs-lookup"><span data-stu-id="2b90e-356">In addition to the payment file, you can generate only the control report.</span></span>

9. <span data-ttu-id="2b90e-357">Загрузите ZIP-файл, затем извлеките из него следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="2b90e-357">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="2b90e-358">Контрольный отчет в формате Excel</span><span class="sxs-lookup"><span data-stu-id="2b90e-358">The control report in Excel format</span></span>
    - <span data-ttu-id="2b90e-359">Файл платежей в формате TXT</span><span class="sxs-lookup"><span data-stu-id="2b90e-359">The payment file in TXT format</span></span>

        <span data-ttu-id="2b90e-360">Обратите внимание, что в соответствии со структурой пользовательского формата электронной отчетности строка платежа в созданном файле теперь [начинается](#PositionSWIFTCode) с кода SWIFT, который был [введен](#DefineSWIFTCode) для банковского счета поставщика, платеж которого был обработан.</span><span class="sxs-lookup"><span data-stu-id="2b90e-360">Notice that, in accordance with the structure of your custom ER format, the payment line in the generated file now [starts](#PositionSWIFTCode) with the SWIFT code that was [entered](#DefineSWIFTCode) for the bank account of the vendor whose payment has been processed.</span></span>

        ![Файл платежей в формате TXT](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a><span data-ttu-id="2b90e-362">Импорт новых версий стандартных конфигураций формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-362">Import new versions of the standard ER format configurations</span></span>

<span data-ttu-id="2b90e-363">В примере, показанном в этом разделе, выводится уведомление о статье базы знаний [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span><span class="sxs-lookup"><span data-stu-id="2b90e-363">For the example that is shown in this section, you receive a notification about Knowledge Base article [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span></span> <span data-ttu-id="2b90e-364">Это уведомление информирует вас о новой версии формата электронной отчетности **BACS (UK)**, которая была опубликована корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2b90e-364">This notification informs you about the new version of the **BACS (UK)** ER format that has been published by Microsoft.</span></span> <span data-ttu-id="2b90e-365">В дополнение к контрольному отчету, эта новая версия позволяет пользователям создавать отчет уведомления о платеже и отчет докладной о посещении во время обработки платежа поставщику.</span><span class="sxs-lookup"><span data-stu-id="2b90e-365">In addition to the control report, this new version lets users generate the payment advice report and the attending note report while a vendor payment is being processed.</span></span> <span data-ttu-id="2b90e-366">Вы хотите начать использовать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="2b90e-366">You want to start to use that functionality.</span></span>

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a><span data-ttu-id="2b90e-367">Импорт новых версий стандартных конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-367">Import new versions of the standard ER configurations</span></span>

<span data-ttu-id="2b90e-368">Чтобы добавить новые версии конфигураций электронной отчетности в текущий экземпляр Finance, необходимо импортировать их из [репозитория](general-electronic-reporting.md#Repository) электронной отчетности, который был настроен вами.</span><span class="sxs-lookup"><span data-stu-id="2b90e-368">To add new versions of the ER configurations to the current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that you've configured.</span></span>

1. <span data-ttu-id="2b90e-369">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-369">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2b90e-370">На странице **Конфигурации локализации** в разделе **Поставщики конфигураций** выберите плитку **Майкрософт**, затем выберите **Репозитории**, чтобы просмотреть список репозиториев для поставщика Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2b90e-370">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="2b90e-371">На странице **Репозитории конфигураций** выберите репозиторий типа **Глобальный**, затем выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-371">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="2b90e-372">Если будет предложено выполнить проверку подлинности для подключения к службе Regulatory Configuration Service, следуйте инструкциям по проверке подлинности.</span><span class="sxs-lookup"><span data-stu-id="2b90e-372">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="2b90e-373">На странице **Репозиторий конфигураций** в дереве конфигураций на левой панели выберите конфигурацию формата **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-373">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="2b90e-374">На экспресс-вкладке **Версии** выберите версию **3.3** выбранной конфигурации формата электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="2b90e-374">On the **Versions** FastTab, select version **3.3** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="2b90e-375">Выберите **Импорт** для загрузки выбранной версии из глобального репозитория в текущий экземпляр Finance.</span><span class="sxs-lookup"><span data-stu-id="2b90e-375">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Страница репозитория конфигурации](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> <span data-ttu-id="2b90e-377">При возникновении проблем с доступом к [глобальному репозиторию](er-download-configurations-global-repo.md) можно вместо этого [загрузить конфигурации](download-electronic-reporting-configuration-lcs.md) из служб LCS.</span><span class="sxs-lookup"><span data-stu-id="2b90e-377">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from LCS instead.</span></span>

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a><span data-ttu-id="2b90e-378">Проверка импортированных конфигураций формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-378">Review the imported ER format configurations</span></span>

1. <span data-ttu-id="2b90e-379">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-379">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2b90e-380">На странице **Конфигурации локализации** в разделе **Конфигурации** выберите плитку **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-380">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="2b90e-381">На странице **Конфигурации** в дереве конфигураций на левой панели разверните **Модель платежа**, затем выберите **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-381">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span>
4. <span data-ttu-id="2b90e-382">На экспресс-вкладке **Версии** выберите версию **3.3**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-382">On the **Versions** FastTab, select version **3.3**.</span></span>
5. <span data-ttu-id="2b90e-383">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-383">Select **Designer**.</span></span>
6. <span data-ttu-id="2b90e-384">На странице **Конструктор формата** разверните элемент формата **BACSReportsFolder**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-384">On the **Format designer** page, expand the **BACSReportsFolder** format element.</span></span>
7.  <span data-ttu-id="2b90e-385">Обратите внимание, что версия 3.3 содержит элемент формата **PaymentAdviceReport**, который используется для создания отчета уведомления о платеже при обработке платежа поставщику.</span><span class="sxs-lookup"><span data-stu-id="2b90e-385">Notice that version 3.3 contains the **PaymentAdviceReport** format element that is used to generate a payment advice report when a vendor payment is processed.</span></span>

    ![Элемент формата PaymentAdviceReport в конструкторе операций электронной отчетности](./media/er-quick-start2-imported-solution2.png)

8. <span data-ttu-id="2b90e-387">Закройте страницу конструктора.</span><span class="sxs-lookup"><span data-stu-id="2b90e-387">Close the designer page.</span></span>

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a><span data-ttu-id="2b90e-388">Адаптация изменений в новой версии импортированного формата в пользовательском формате</span><span class="sxs-lookup"><span data-stu-id="2b90e-388">Adopt the changes in the new version of an imported format in a custom format</span></span>

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a><span data-ttu-id="2b90e-389">Завершение текущей черновой версии пользовательского формата</span><span class="sxs-lookup"><span data-stu-id="2b90e-389">Complete the current draft version of a custom format</span></span>

<span data-ttu-id="2b90e-390">Если требуется сохранить текущее состояние пользовательского формата, завершите черновую версию 1.1.1, изменив ее статус с **Черновик** на **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-390">If you want to keep the current state of your custom format, complete the draft version 1.1.1 by changing its status from **Draft** to **Completed**.</span></span>

1. <span data-ttu-id="2b90e-391">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-391">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2b90e-392">На странице **Конфигурации локализации** в разделе **Конфигурации** выберите плитку **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-392">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="2b90e-393">На странице **Конфигурации** в дереве конфигураций на левой панели разверните **Модель платежа**, разверните **BACS (UK)**, затем выберите **BACS (UK, пользовательский)**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-393">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, expand **BACS (UK)**, and then select **BACS (UK custom)**.</span></span>
4. <span data-ttu-id="2b90e-394">На экспресс-вкладке **Версии** выберите **Изменить статус** \> **Завершено**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-394">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="2b90e-395">Состояние версии 1.1.1 изменится с **Черновик** на **Завершено**, и версия становится доступной только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2b90e-395">The status of version 1.1.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="2b90e-396">Добавлена новая редактируемая версия, 1.1.2, имеющая статус **Черновик**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-396">A new editable version, 1.1.2, has been added and has a status of **Draft**.</span></span> <span data-ttu-id="2b90e-397">Эту версию можно использовать для внесения дальнейших изменений в настраиваемый формат электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="2b90e-397">You can use this version to make further changes in your custom ER format.</span></span>

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a><span data-ttu-id="2b90e-398">Перемещение пользовательского формата на новую базовую версию</span><span class="sxs-lookup"><span data-stu-id="2b90e-398">Rebase a custom format to a new base version</span></span>

<span data-ttu-id="2b90e-399">Чтобы начать использовать новые функции версии 3.3 в формате **BACS (UK)** в вашей настройке, необходимо изменить основную версию конфигурации для пользовательской конфигурации **BACS (UK пользовательская)**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-399">To start to use the new functionality of version 3.3 of the **BACS (UK)** format in your customization, you must change the base configuration version for the custom configuration, **BACS (UK custom)**.</span></span> <span data-ttu-id="2b90e-400">Этот процесс называется [повторным размещением](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span><span class="sxs-lookup"><span data-stu-id="2b90e-400">This process is known as [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span></span> <span data-ttu-id="2b90e-401">Вместо версии 1.1 **BACS (UK)** используйте версию 3.3.</span><span class="sxs-lookup"><span data-stu-id="2b90e-401">Instead of version 1.1 of **BACS (UK)**, use version 3.3.</span></span>

1. <span data-ttu-id="2b90e-402">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-402">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2b90e-403">На странице **Конфигурации** в дереве конфигураций на левой панели разверните **Модель платежа**, затем выберите **BACS (Соединенное Королевство, пользовательский)**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-403">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="2b90e-404">На экспресс-вкладке **Версии** выберите версию **1.1.2**, а затем выберите **Повторно разместить**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-404">On the **Versions** FastTab, select version **1.1.2**, and then select **Rebase**.</span></span>
4. <span data-ttu-id="2b90e-405">В диалоговом окне **Повторно разместить** в поле **Целевая версия** выберите версию **3.3** базовой конфигурации, чтобы применить ее в качестве новой базы, и используйте ее для обновления конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2b90e-405">In the **Rebase** dialog box, in the **Target version** field, select version **3.3** of the base configuration to apply it as the new base and use it to update the configuration.</span></span>

    ![Диалоговое окно повторного размещения](./media/er-quick-start2-rebase1.png)

5. <span data-ttu-id="2b90e-407">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-407">Select **OK**.</span></span>
6. <span data-ttu-id="2b90e-408">Обратите внимание, что номер черновой версии был изменен с **1.1.2** на **3.3.2**, чтобы отразить изменение в базовой версии.</span><span class="sxs-lookup"><span data-stu-id="2b90e-408">Notice that the number of the draft version has been changed from **1.1.2** to **3.3.2** to reflect the change in the base version.</span></span>

    <span data-ttu-id="2b90e-409">При объединении пользовательской версии и новой базовой версии могут быть обнаружены некоторые конфликты из-за изменений формата, которые невозможно объединить автоматически.</span><span class="sxs-lookup"><span data-stu-id="2b90e-409">When the custom version and a new base version are merged, some conflicts might be discovered because of format changes that can't be merged automatically.</span></span>

    ![Перемещенная конфигурация с конфликтами на странице конфигураций](./media/er-quick-start2-rebase2.png)

    <span data-ttu-id="2b90e-411">При обнаружении конфликтов их необходимо разрешить вручную в конструкторе форматов.</span><span class="sxs-lookup"><span data-stu-id="2b90e-411">If conflicts are discovered, they must be manually resolved in the format designer.</span></span>

7. <span data-ttu-id="2b90e-412">На экспресс-вкладке **Версии** выберите версию **3.3.2**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-412">On the **Versions** FastTab, select version **3.3.2**.</span></span>
8. <span data-ttu-id="2b90e-413">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-413">Select **Designer**.</span></span>
9. <span data-ttu-id="2b90e-414">На странице **Конструктор формата** на экспресс-вкладке **Сведения** выберите запись о конфликте для изменения базы, затем выберите **Применить базовое значение**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-414">On the **Format designer** page, on the **Details** FastTab, select a rebase conflict record, and then select **Apply base value**.</span></span>

    ![Запись конфликта изменения базы в конструкторе операций электронной отчетности](./media/er-quick-start2-rebase3.png)

10. <span data-ttu-id="2b90e-416">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-416">Select **Save**.</span></span>

    <span data-ttu-id="2b90e-417">Запись о конфликте изменения базы не должна больше отображаться на экспресс-вкладке **Сведения**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-417">The rebase conflict record should no longer appear on the **Details** FastTab.</span></span>

    ![Конфликт, разрешенный в конструкторе операций электронной отчетности](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > <span data-ttu-id="2b90e-419">Этот конфликт был устранен путем подтверждения того, что в этом формате электронной отчетности должна использоваться версия 3 базовой модели.</span><span class="sxs-lookup"><span data-stu-id="2b90e-419">You resolved the conflict by confirming that version 3 of the base model must be used in this ER format.</span></span>

11. <span data-ttu-id="2b90e-420">Разверните **BACSReportsFolder** \> **файл** \> **транзакции** \> **транзакция**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-420">Expand **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span></span>
12. <span data-ttu-id="2b90e-421">На вкладке **Сопоставление** обратите внимание на то, что версия 3.3.2 настраиваемого формата электронной отчетности содержит настройку (элемент формата **vendBankSWIFT** и его привязку) и новые функции версии 3.3 базового формата электронной отчетности, которые были предоставлены корпорацией Майкрософт (элемент форматирования **PaymentAdviceReport** вместе с вложенными элементами и настроенными привязками).</span><span class="sxs-lookup"><span data-stu-id="2b90e-421">On the **Mapping** tab, notice that version 3.3.2 of your custom ER format contains both your customization (the **vendBankSWIFT** format element and its binding) and the new functionality of version 3.3 of the base ER format that was provided by Microsoft (the **PaymentAdviceReport** format element together with its nested elements and configured bindings).</span></span> <span data-ttu-id="2b90e-422">С помощью нескольких щелчков мышью можно адаптировать изменения новой базовой версии, объединив их с настройкой.</span><span class="sxs-lookup"><span data-stu-id="2b90e-422">In just a few mouse clicks, you adopted the modifications of a new base version by merging them with your customization.</span></span>

    ![Объединенный формат в конструкторе операций электронной отчетности](./media/er-quick-start2-rebase5.png)

13. <span data-ttu-id="2b90e-424">Закройте страницу конструктора.</span><span class="sxs-lookup"><span data-stu-id="2b90e-424">Close the designer page.</span></span>

> [!NOTE]
> <span data-ttu-id="2b90e-425">Операция изменения базы обратима.</span><span class="sxs-lookup"><span data-stu-id="2b90e-425">The rebase action is reversible.</span></span> <span data-ttu-id="2b90e-426">Чтобы отменить это изменение базы, выберите версию **1.1.1** для формата **BACS (UK, пользовательский)** на экспресс-вкладке **Версии**, затем выберите **Получить эту версию**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-426">To cancel this rebase, select version **1.1.1** of the **BACS (UK custom)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="2b90e-427">Версия 3.3.2 будет перенумерована в 1.1.2, а содержимое черновой версии 1.1.2 будет соответствовать содержимому версии 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="2b90e-427">Version 3.3.2 will then be renumbered 1.1.2, and the content of draft version 1.1.2 will match the content of version 1.1.1.</span></span>

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a><span data-ttu-id="2b90e-428">Обработка платежа поставщику с помощью перемещенного формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-428">Process a vendor payment by using a rebased ER format</span></span>

1. <span data-ttu-id="2b90e-429">Перейдите в раздел **Расчеты с поставщиками** \> **Платежи** \> **Журнал платежей поставщикам**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-429">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="2b90e-430">На странице **Журнал платежей поставщику** выберите созданный ранее журнал платежей.</span><span class="sxs-lookup"><span data-stu-id="2b90e-430">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="2b90e-431">Выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-431">Select **Lines**.</span></span>
4. <span data-ttu-id="2b90e-432">На странице **Платежи поставщикам** над сеткой выберите **Статус платежа** \> **Нет**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-432">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="2b90e-433">Выберите **Создать платеж**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-433">Select **Generate payment**.</span></span>
6. <span data-ttu-id="2b90e-434">В диалоговом окне **Создать платежи** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="2b90e-434">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="2b90e-435">В поле **Способ оплаты** выберите **Электронный**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-435">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="2b90e-436">В поле **Банковский счет** выберите **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-436">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="2b90e-437">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-437">Select **OK**.</span></span>
8. <span data-ttu-id="2b90e-438">В диалоговом окне **Параметры электронной отчетности** введите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="2b90e-438">In the **Electronic report parameters** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="2b90e-439">Задайте для параметра **Печать контрольного отчета** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-439">Set the **Print control report** option to **Yes**.</span></span>
    - <span data-ttu-id="2b90e-440">Задайте для параметра **Печать уведомления об оплате** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-440">Set the **Print payment advice** option to **Yes**.</span></span>

    ![Диалоговое окно параметров электронной отчетности](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > <span data-ttu-id="2b90e-442">В дополнение к файлу платежа теперь можно создать как контрольный отчет, так и отчет уведомления об оплате.</span><span class="sxs-lookup"><span data-stu-id="2b90e-442">In addition to the payment file, you can now generate both the control report and the payment advice report.</span></span>

9. <span data-ttu-id="2b90e-443">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2b90e-443">Select **OK**.</span></span>
10. <span data-ttu-id="2b90e-444">Загрузите ZIP-файл, затем извлеките из него следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="2b90e-444">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="2b90e-445">Контрольный отчет в формате Excel</span><span class="sxs-lookup"><span data-stu-id="2b90e-445">The control report in Excel format</span></span>
    - <span data-ttu-id="2b90e-446">Отчет уведомления об оплате в формате Excel</span><span class="sxs-lookup"><span data-stu-id="2b90e-446">The payment advice report in Excel format</span></span>

        ![Отчет уведомления об оплате в формате Excel](./media/er-quick-start2-payment-advice-report.png)

    - <span data-ttu-id="2b90e-448">Файл платежей в формате TXT</span><span class="sxs-lookup"><span data-stu-id="2b90e-448">The payment file in TXT format</span></span>

        <span data-ttu-id="2b90e-449">Обратите внимание, что строка платежа в созданном файле начинается с кода SWIFT, который был введен для банковского счета поставщика, платеж которого был обработан.</span><span class="sxs-lookup"><span data-stu-id="2b90e-449">Notice that the payment line in the generated file starts  with the SWIFT code that was entered for the bank account of a vendor whose payment has been processed.</span></span>

        ![Файл платежей в формате TXT](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a><span data-ttu-id="2b90e-451">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2b90e-451">Additional resources</span></span>

- [<span data-ttu-id="2b90e-452">Обзор электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="2b90e-452">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="2b90e-453">Загрузка конфигураций электронной отчетности из Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="2b90e-453">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="2b90e-454">Загрузка конфигураций электронной отчетности из глобального репозитория Configuration Service</span><span class="sxs-lookup"><span data-stu-id="2b90e-454">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
