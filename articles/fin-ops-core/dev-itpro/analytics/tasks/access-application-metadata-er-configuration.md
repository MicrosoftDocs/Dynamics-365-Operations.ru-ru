---
title: Доступ к метаданным приложения с помощью конфигурации электронной отчетности
description: В этой теме описывается, как пользователь службы Regulatory Configuration Service может создать новое сопоставление модели электронной отчетности с помощью метаданных.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91c50047781fdc21c9157ceb634822c6cfb5a075
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559659"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="725fd-103">Доступ к метаданным приложения с помощью конфигурации электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="725fd-103">Access application metadata by using ER configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="725fd-104">В следующих шагах поясняется, как пользователь службы Regulatory Configuration Service (RCS) с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать новое сопоставление модели электронной отчетности с помощью метаданных.</span><span class="sxs-lookup"><span data-stu-id="725fd-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the application metadata.</span></span> <span data-ttu-id="725fd-105">Доступ к метаданным приложения будет осуществляться с помощью конфигурации метаданных ER, которая содержит образец набора метаданных для доступа к проводкам внешней торговли.</span><span class="sxs-lookup"><span data-stu-id="725fd-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="725fd-106">Для выполнения этих шагов в RCS необходимо сначала выполнить шаги в процедуре [Создание поставщиков конфигурации и установка их в качестве активных](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="725fd-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="725fd-107">Затем выполните шаги раздела [Подготовки метаданных приложения для использования в RCS](prepare-application-metadata-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="725fd-107">Then complete the steps in the topic, [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="725fd-108">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="725fd-108">Prerequisites</span></span>
1. <span data-ttu-id="725fd-109">Перейдите в раздел **Все рабочие области** > **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="725fd-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="725fd-110">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как **Активный**.</span><span class="sxs-lookup"><span data-stu-id="725fd-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="725fd-111">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре [Создание поставщиков конфигурации и пометка их как активных](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="725fd-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="725fd-112">Импорт конфигурации метаданных</span><span class="sxs-lookup"><span data-stu-id="725fd-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="725fd-113">Щелкните **Конфигурации метаданных**.</span><span class="sxs-lookup"><span data-stu-id="725fd-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="725fd-114">Импортируйте конфигурацию метаданных ER, которая содержит метаданные и настроена для создания электронных документов для бизнес-домена внешней торговли.</span><span class="sxs-lookup"><span data-stu-id="725fd-114">Import the ER metadata configuration that contains metadata that has been configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="725fd-115">Эта конфигурация метаданных ER была экспортирована в XML-файл в ходе выполнения шагов в процедуре [Подготовка метаданных приложения для использования в RCS](prepare-application-metadata-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="725fd-115">This ER metadata configuration has been exported as XML file while the steps in the [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="725fd-116">Щелкните **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="725fd-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="725fd-117">Щелкните **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="725fd-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="725fd-118">Щелкните **Обзор** и выберите файл "Метаданные внешней торговли.xml".</span><span class="sxs-lookup"><span data-stu-id="725fd-118">Click **Browse** and select the 'Foreign trade metadata.xml' file.</span></span> 
6. <span data-ttu-id="725fd-119">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="725fd-119">Click **OK**.</span></span> 
7. <span data-ttu-id="725fd-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="725fd-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="725fd-121">Создание конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="725fd-121">Create data model configuration</span></span>
1. <span data-ttu-id="725fd-122">Щелкните **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="725fd-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="725fd-123">Щелкните **Создать конфигурацию**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="725fd-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="725fd-124">В поле **Имя** введите "Модель внешней торговли".</span><span class="sxs-lookup"><span data-stu-id="725fd-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="725fd-125">Нажмите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="725fd-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="725fd-126">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="725fd-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="725fd-127">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="725fd-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="725fd-128">В поле **Имя** введите "Root".</span><span class="sxs-lookup"><span data-stu-id="725fd-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="725fd-129">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="725fd-129">Click **Add**.</span></span> 
9. <span data-ttu-id="725fd-130">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="725fd-130">Click **New** to open the drop dialog.</span></span> 
10.    <span data-ttu-id="725fd-131">В поле **Имя** введите "Проводка".</span><span class="sxs-lookup"><span data-stu-id="725fd-131">In the **Name** field, type 'Transaction'.</span></span> 
11.    <span data-ttu-id="725fd-132">В поле **Тип элемента** выберите **Список записей**.</span><span class="sxs-lookup"><span data-stu-id="725fd-132">In the **Item type** field, select **Record list**.</span></span> 
12.    <span data-ttu-id="725fd-133">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="725fd-133">Click **Add**.</span></span> 
13.    <span data-ttu-id="725fd-134">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="725fd-134">Click **New** to open the drop dialog.</span></span> 
14.    <span data-ttu-id="725fd-135">В поле **Имя** введите "Код товара".</span><span class="sxs-lookup"><span data-stu-id="725fd-135">In the **Name** field, type 'Commodity code'.</span></span> 
15.    <span data-ttu-id="725fd-136">В поле **Тип элемента** выберите **Строка**.</span><span class="sxs-lookup"><span data-stu-id="725fd-136">In the **Item type** field, select **String**.</span></span> 
16.    <span data-ttu-id="725fd-137">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="725fd-137">Click **Add**.</span></span> 
17.    <span data-ttu-id="725fd-138">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="725fd-138">Click **New** to open the drop dialog.</span></span> 
18.    <span data-ttu-id="725fd-139">В поле **Имя** введите "Сумма, выставленная по накладным".</span><span class="sxs-lookup"><span data-stu-id="725fd-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19.    <span data-ttu-id="725fd-140">В поле **Тип элемента** выберите **Вещественный**.</span><span class="sxs-lookup"><span data-stu-id="725fd-140">In the **Item type** field, select **Real**.</span></span> 
20.    <span data-ttu-id="725fd-141">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="725fd-141">Click **Add**.</span></span> 
21.    <span data-ttu-id="725fd-142">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="725fd-142">Click **New** to open the drop dialog.</span></span> 
22.    <span data-ttu-id="725fd-143">В поле **Имя** введите "Дата".</span><span class="sxs-lookup"><span data-stu-id="725fd-143">In the **Name** field, type 'Date'.</span></span> 
23.    <span data-ttu-id="725fd-144">В поле **Тип элемента** выберите **Дата**.</span><span class="sxs-lookup"><span data-stu-id="725fd-144">In the **Item type** field, select **Date**.</span></span> 
24.    <span data-ttu-id="725fd-145">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="725fd-145">Click **Add**.</span></span> 
25.    <span data-ttu-id="725fd-146">Щелкните **Корневая ссылка**.</span><span class="sxs-lookup"><span data-stu-id="725fd-146">Click **Root reference**.</span></span> 
26.    <span data-ttu-id="725fd-147">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="725fd-147">Click **OK**.</span></span> 
27.    <span data-ttu-id="725fd-148">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="725fd-148">Click **Save**.</span></span> 
28.    <span data-ttu-id="725fd-149">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="725fd-149">Close the page.</span></span> 
29.    <span data-ttu-id="725fd-150">Щелкните **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="725fd-150">Click **Change status**.</span></span> 
30.    <span data-ttu-id="725fd-151">Щелкните **Завершить**.</span><span class="sxs-lookup"><span data-stu-id="725fd-151">Click **Complete**.</span></span> 
31.    <span data-ttu-id="725fd-152">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="725fd-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="725fd-153">Создание конфигурации сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="725fd-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="725fd-154">Щелкните **Создать конфигурацию**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="725fd-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="725fd-155">В поле **Создать** введите "Сопоставление модели, основанное на модели данных «Модель внешней торговли»".</span><span class="sxs-lookup"><span data-stu-id="725fd-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="725fd-156">В поле **Имя** введите "Сопоставление внешней торговли".</span><span class="sxs-lookup"><span data-stu-id="725fd-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="725fd-157">Нажмите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="725fd-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="725fd-158">Разверните раздел **Необходимые условия**.</span><span class="sxs-lookup"><span data-stu-id="725fd-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="725fd-159">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="725fd-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="725fd-160">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="725fd-160">Click **New**.</span></span> 
8. <span data-ttu-id="725fd-161">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="725fd-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="725fd-162">В поле **Тип необходимого компонента** выберите **Конфигурация**.</span><span class="sxs-lookup"><span data-stu-id="725fd-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10.    <span data-ttu-id="725fd-163">Выберите конфигурацию **Метаданные внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="725fd-163">Select **Foreign trade metadata** configuration.</span></span> 
11.    <span data-ttu-id="725fd-164">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="725fd-164">Click **Save**.</span></span> 
12.    <span data-ttu-id="725fd-165">Мы добавили ссылку на версию 1 конфигурации "Метаданные внешней торговли".</span><span class="sxs-lookup"><span data-stu-id="725fd-165">We added the reference to the version 1 of the 'Foreign trade metadata' configuration.</span></span> <span data-ttu-id="725fd-166">Метаданные приложения из этой конфигурации будут предлагаться при разработке этого сопоставления моделей.</span><span class="sxs-lookup"><span data-stu-id="725fd-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13.    <span data-ttu-id="725fd-167">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="725fd-167">Close the page.</span></span> 
14.    <span data-ttu-id="725fd-168">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="725fd-168">Click **Designer**.</span></span> 
15.    <span data-ttu-id="725fd-169">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="725fd-169">Click **Designer**.</span></span> 
16.    <span data-ttu-id="725fd-170">В дереве выберите узел **Dynamics 365 for Operations\Записи таблиц**.</span><span class="sxs-lookup"><span data-stu-id="725fd-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17.    <span data-ttu-id="725fd-171">Щелкните **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="725fd-171">Click **Add root**.</span></span> 
18.    <span data-ttu-id="725fd-172">В поле **Имя** введите "Интрастат".</span><span class="sxs-lookup"><span data-stu-id="725fd-172">In the **Name** field, type 'Intrastat'.</span></span> 
19.    <span data-ttu-id="725fd-173">Выберите записи таблицы **Интрастат**.</span><span class="sxs-lookup"><span data-stu-id="725fd-173">Select **Intrastat** table records.</span></span> 
20.    <span data-ttu-id="725fd-174">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="725fd-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="725fd-175">Предлагались только 2 таблицы, поскольку только 2 таблицы были добавлены в набор метаданных, который в настоящее время используется.</span><span class="sxs-lookup"><span data-stu-id="725fd-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21.    <span data-ttu-id="725fd-176">Щелкните **Связать**.</span><span class="sxs-lookup"><span data-stu-id="725fd-176">Click **Bind**.</span></span> 
22.    <span data-ttu-id="725fd-177">В дереве разверните узел **Интрастат**.</span><span class="sxs-lookup"><span data-stu-id="725fd-177">In the tree, expand **Intrastat**.</span></span> 
23.    <span data-ttu-id="725fd-178">В дереве выберите **Интрастат\AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="725fd-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24.    <span data-ttu-id="725fd-179">В дереве разверните узел **Проводка = Интрастат**.</span><span class="sxs-lookup"><span data-stu-id="725fd-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25.    <span data-ttu-id="725fd-180">В дереве выберите **Проводка = Интрастат\Сумма, выставленная по накладным**.</span><span class="sxs-lookup"><span data-stu-id="725fd-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26.    <span data-ttu-id="725fd-181">Щелкните **Связать**.</span><span class="sxs-lookup"><span data-stu-id="725fd-181">Click **Bind**.</span></span> 
27.    <span data-ttu-id="725fd-182">В дереве выберите **Интрастат\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="725fd-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28.    <span data-ttu-id="725fd-183">В дереве выберите **Проводка = Интрастат\Дата**.</span><span class="sxs-lookup"><span data-stu-id="725fd-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29.    <span data-ttu-id="725fd-184">Щелкните **Связать**.</span><span class="sxs-lookup"><span data-stu-id="725fd-184">Click **Bind**.</span></span> 
30.    <span data-ttu-id="725fd-185">В дереве разверните **Интрастат\>Отношения**.</span><span class="sxs-lookup"><span data-stu-id="725fd-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31.    <span data-ttu-id="725fd-186">В дереве разверните **Интрастат\>Отношения\IntrastatCommodity**.</span><span class="sxs-lookup"><span data-stu-id="725fd-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32.    <span data-ttu-id="725fd-187">В дереве выберите **Интрастат\>Отношения\IntrastatCommodity\Код**.</span><span class="sxs-lookup"><span data-stu-id="725fd-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33.    <span data-ttu-id="725fd-188">В дереве выберите **Проводка = Интрастат\Товарный код**.</span><span class="sxs-lookup"><span data-stu-id="725fd-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34.    <span data-ttu-id="725fd-189">Щелкните **Связать**.</span><span class="sxs-lookup"><span data-stu-id="725fd-189">Click **Bind**.</span></span> 
35.    <span data-ttu-id="725fd-190">Щелкните **Проверить**.</span><span class="sxs-lookup"><span data-stu-id="725fd-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="725fd-191">Мы успешно привязали элементы модели данных к элементам источников данных, которые описаны с помощью подробных сведений метаданных приложения из указанной конфигурации метаданных ER.</span><span class="sxs-lookup"><span data-stu-id="725fd-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36.    <span data-ttu-id="725fd-192">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="725fd-192">Click **Save**.</span></span> 
37.    <span data-ttu-id="725fd-193">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="725fd-193">Close the page.</span></span> 
38.    <span data-ttu-id="725fd-194">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="725fd-194">Close the page.</span></span> 
39.    <span data-ttu-id="725fd-195">При необходимости можно расширить существующий набор метаданных и затем экспортировать новую завершенную версию конфигурации метаданных ER.</span><span class="sxs-lookup"><span data-stu-id="725fd-195">When needed, you can extend the existing set of metadata and then export the new completed version of ER metadata configuration.</span></span> <span data-ttu-id="725fd-196">Затем ее можно импортировать в RCS и обновить необходимые компоненты настроенной конфигурации сопоставления модели, ссылаясь на новую версию импортированной конфигурации метаданных.</span><span class="sxs-lookup"><span data-stu-id="725fd-196">You can then import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="725fd-197">Этот способ получения сведений о метаданных приложения является единственным доступным методом для локально развернутых приложений (то есть, когда используются локальные бизнес-данные (LBD) или локальная модель развертывания).</span><span class="sxs-lookup"><span data-stu-id="725fd-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used).</span></span>
        


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]