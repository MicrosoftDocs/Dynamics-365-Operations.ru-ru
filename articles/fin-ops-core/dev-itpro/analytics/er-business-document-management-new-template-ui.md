---
title: Microsoft Office-стильный пользовательский интерфейс в управлении бизнес-документами
description: В этом разделе объясняется, как использовать новый пользовательский интерфейс в управлении бизнес-документами на платформе электронной отчетности (ER).
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881044"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a><span data-ttu-id="f8fd0-103">Microsoft Office-стильный пользовательский интерфейс в управлении бизнес-документами</span><span class="sxs-lookup"><span data-stu-id="f8fd0-103">Microsoft Office-style user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8fd0-104">Управление бизнес-документами позволяет бизнес-пользователям редактировать шаблоны деловых документов с помощью службы Microsoft 365 или соответствующего классического приложения Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="f8fd0-105">Правки могут включать изменения структуры или новые развертывания, или пользователи могут добавлять заполнители для включения дополнительных данных без изменения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="f8fd0-106">Дополнительные сведения о работе с системой управления бизнес-документами см. в разделе [Обзор управления бизнес-документами](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="f8fd0-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="f8fd0-107">Новый пользовательский интерфейс является более четким и более удобным для использования.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-107">The new user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="f8fd0-108">В области **Бизнес-документ** отображаются только шаблоны, доступные для текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-108">The **Business document** area shows only the templates that are available for the current provider.</span></span> <span data-ttu-id="f8fd0-109">В предыдущем пользовательском интерфейсе на вкладке **шаблон** перечислены все шаблоны, доступные для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-109">In the previous UI, the **Template** tab listed all the templates that were available for any providers.</span></span> <span data-ttu-id="f8fd0-110">Также были показаны все шаблоны, которые были созданы и отредактированы любым пользователем, который обладает одной и той же ролью.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-110">It also showed all the templates that were created and edited by any user who had the same role.</span></span>

<span data-ttu-id="f8fd0-111">Можно использовать кнопку **Создать документ**, чтобы создавать и изменять шаблоны в конфигурации формата электронной отчетности, предоставляемой другим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-111">You can use the **New document** button to create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="f8fd0-112">В примере данного раздела поставщиком является Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-112">In the example in this topic, the provider is Microsoft.</span></span> <span data-ttu-id="f8fd0-113">Кроме того, можно создать шаблон, загружая свой собственный шаблон в формате Excel.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-113">Alternatively, you can create a template by uploading your own template in Excel format.</span></span>


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

<span data-ttu-id="f8fd0-114">Видео [Создание нового бизнес-документа с помощью управления бизнес-документами](https://youtu.be/gAIYl-mM_pw) (показано выше) включено в [Finance and Operations список воспроизведения](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), доступный на YouTube.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-114">The [Create a new business document using Business document management](https://youtu.be/gAIYl-mM_pw) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="f8fd0-115">Предоставление доступа для нового пользовательского интерфейса документа в управлении бизнес-документами</span><span class="sxs-lookup"><span data-stu-id="f8fd0-115">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="f8fd0-116">Чтобы начать пользоваться новым пользовательским интерфейсом документа в управлении бизнес-документами, необходимо включить функцию **Взаимодействие с пользовательским интерфейсом по типу Office для управления бизнес-документами** в рабочей области **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-116">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="f8fd0-117">Чтобы включить эту функцию для всех юридических лиц, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-117">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="f8fd0-118">В рабочей области **Управление функциями** на вкладке **Все** в списке выберите функцию **Взаимодействие с пользовательским интерфейсов по типу Office для управления бизнес-документами**.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-118">In the **Feature management** workspace, on the **All** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="f8fd0-119">Чтобы включить выбранный компонент, установите флажок **Включить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-119">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="f8fd0-120">Обновите страницу, чтобы получить доступ к новому компоненту.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-120">Refresh the page to access the new feature.</span></span>

## <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="f8fd0-121">Редактирование шаблонов, принадлежащих другим поставщикам</span><span class="sxs-lookup"><span data-stu-id="f8fd0-121">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="f8fd0-122">В рабочей области **Управление бизнес-документами** выберите **Создать документ**.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-122">In the **Business document management** workspace, select **New document**.</span></span>

    ![Рабочая область управления бизнес-документами](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="f8fd0-124">На вкладке **Выбор** выберите документ для используемого шаблона и выберите **Создать документ**.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-124">On the **Select** tab, select the document to use as a template, and then select **Create document**.</span></span>

    ![Диалоговое окно бизнес-документов](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="f8fd0-126">В новом диалоговом окне в поле **Заголовок** измените заголовок нужным образом.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-126">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="f8fd0-127">Этот текст заголовка будет использоваться для имени новой конфигурации формата ER, которая создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-127">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="f8fd0-128">Черновая версия этой конфигурации (**Копия отчета FTI клиента (GER)**), которая будет содержать отредактированный шаблон, будет автоматически помечена для запуска этого формата ER для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-128">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="f8fd0-129">Для запуска этого формата ER для любого другого пользователя будет использоваться исходный шаблон из базовой конфигурации формата ER.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-129">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="f8fd0-130">В поле **Имя** измените имя первой редакции редактируемого шаблона, которая будет создана автоматически.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-130">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="f8fd0-131">В поле **Комментарий** обновите примечания для редакции редактируемого шаблона, которая будет создана автоматически.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-131">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="f8fd0-132">Выберите **ОК**, чтобы подтвердить начало процесса редактирования.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-132">Select **OK** to confirm the start of the editing process.</span></span>

    ![Диалоговое окно создания документа](./media/BDM_overview_new_template3.png)

<span data-ttu-id="f8fd0-134">Кнопка **Создать документ** позволяет создавать и изменять шаблоны в конфигурации формата электронной отчетности, предоставляемой другим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-134">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="f8fd0-135">В этом примере поставщиком является Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-135">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="f8fd0-136">При выборе **Создать документ** отображаются все шаблоны, принадлежащие текущим и другим поставщикам.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-136">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="f8fd0-137">После выбора шаблона он будет открыт для редактирования.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-137">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="f8fd0-138">Измененный шаблон будет затем сохранен в новой конфигурации формата ER, которая создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-138">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a><span data-ttu-id="f8fd0-139">Загрузка шаблона, использующего существующий формат Excel</span><span class="sxs-lookup"><span data-stu-id="f8fd0-139">Upload a template that uses an existing Excel format</span></span>
<span data-ttu-id="f8fd0-140">Выполните следующие действия, чтобы ввести необходимые сведения перед отправкой шаблона.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-140">Follow these steps to provide required information before you upload a template.</span></span>

1. <span data-ttu-id="f8fd0-141">В рабочей области **Управление бизнес-документами** выберите **Создать документ**.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-141">In the **Business document management** workspace, select **New document**.</span></span>

    ![Рабочая область управления бизнес-документами](./media/BDM_overview_new_template1.png)
    
2. <span data-ttu-id="f8fd0-143">На странице **Создание нового шаблона** на вкладке **Загрузка** на вкладке **шаблон** выберите **Обзор**, чтобы найти и выбрать файл Excel, который будет использоваться в качестве шаблона.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-143">On the **Create a new template** page, on the **Upload** tab, on the **Template** tab, select **Browse** to find and select the Excel file that you want to use as a template.</span></span> <span data-ttu-id="f8fd0-144">В разделе **шаблона** поля **заголовка** и **описания** заполняются автоматически.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-144">In the **Template** section, the **Title** and **Description** fields are automatically filled in.</span></span> <span data-ttu-id="f8fd0-145">Они указывают имя и описание новой конфигурации формата электронной отчетности, которая создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-145">They specify the name and description of the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="f8fd0-146">Если необходимо, эти поля можно изменить.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-146">You can edit these fields as you require.</span></span>
3. <span data-ttu-id="f8fd0-147">В разделе **Тип документа** в поле **Имя** укажите тип бизнес-документа.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-147">In the **Document Type** section, in the **Name** field, specify the type of business document.</span></span> <span data-ttu-id="f8fd0-148">Это значение будет использоваться для поиска правильного источника данных (то есть, конфигурации модели электронной отчетности).</span><span class="sxs-lookup"><span data-stu-id="f8fd0-148">This value will be used to search the correct data source (that is, the ER model configuration).</span></span>

    ![Вкладка "Шаблон"](./media/BDM_overview_new_UI_import_21.jpg)

4. <span data-ttu-id="f8fd0-150">На вкладке **Источник данных** на экспресс-вкладке **Фильтр** выберите **Применить фильтр**.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-150">On the **Data source** tab, on the **Filter** FastTab, select **Apply filter**.</span></span> <span data-ttu-id="f8fd0-151">В разделе **Источник данных** поле **имя** заполняется автоматически, или можно выбрать значение вручную.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-151">In the **Data source** section, the **Name** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="f8fd0-152">Фильтр можно использовать для поиска соответствующего имени источника данных по имени, описанию, коду страны/региона и типу бизнес-документа.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-152">You can use the filter to search for the appropriate data source name by name, description, country/region code, and business document type.</span></span>

    ![Вкладка "Источник данных"](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > <span data-ttu-id="f8fd0-154">Экспресс-вкладка **Фильтр** используется для поиска правильного источника данных (то есть, конфигурации модели электронной отчетности).</span><span class="sxs-lookup"><span data-stu-id="f8fd0-154">The **Filter** FastTab is used to search the correct data source (that is, the ER model configuration).</span></span> <span data-ttu-id="f8fd0-155">Можно изменить все поля фильтра, чтобы найти наиболее подходящий источник данных для отправляемого документа.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-155">You can edit all filter fields to find the most appropriate data source for the document that you're uploading.</span></span>
    > 
    > <span data-ttu-id="f8fd0-156">Условия на экспресс-вкладке **фильтр** используются как условия **ИЛИ**.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-156">The conditions on the **Filter** FastTab are used as **OR** conditions.</span></span>
    
5. <span data-ttu-id="f8fd0-157">На вкладке **Сопоставление** выберите **Автоопределение**.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-157">On the **Mapping** tab, select **Auto detect**.</span></span> <span data-ttu-id="f8fd0-158">Поле **корневое определение** заполняется автоматически, или можно выбрать значение вручную.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-158">The **Root definition** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="f8fd0-159">На этой вкладке отображается конечное сопоставление для элементов шаблона и модели.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-159">This tab shows the end mapping for the elements from the template and the model.</span></span>

    ![Вкладка "Сопоставление"](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > <span data-ttu-id="f8fd0-161">Сопоставление в разделе **Структура шаблона** использует полное соответствие меток или описаний в источнике данных в языке пользователя и имя ячейки в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-161">The mapping in the **Template structure** section uses the full match of the labels or descriptions in the data source in the user's language, and in the cell name in the template.</span></span>

6. <span data-ttu-id="f8fd0-162">Выберите **создать документ**, чтобы подтвердить необходимость создания шаблона и начать процесс редактирования.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-162">Select **Create document** to confirm that you want to create a template and start the editing process.</span></span>

<span data-ttu-id="f8fd0-163">Дополнительные сведения см. в разделе [Обзор управления бизнес-документами](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="f8fd0-163">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="f8fd0-164">Если в электронной отчетности нет ни одного поставщика, его можно создать.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-164">If there isn't a provider in Electronic reporting, you can create one.</span></span> <span data-ttu-id="f8fd0-165">Если активного поставщика нет, вы можете активировать его.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-165">If there's no active provider, you can select to activate one.</span></span>

- <span data-ttu-id="f8fd0-166">Чтобы создать поставщика, измените имя поставщика в поле **имя**, обновите веб-адрес нового поставщика в поле **Веб-адрес** и нажмите кнопку **ОК** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-166">To create a provider, change the name of the provider in the **Name** field, update the internet address of the new provider in the **Internet address** field, and select **OK** to confirm.</span></span>

    ![Создать нового поставщика в BDM](./media/bdm_create_provider.png)
    
- <span data-ttu-id="f8fd0-168">Чтобы активировать существующего поставщика, выберите имя поставщика в поле **Поставщик конфигурации** и нажмите кнопку **OK**, чтобы указать поставщика в качестве активного.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-168">To activate existing provider, choose the name of the provider in the **Configuration provider** field, and select **OK** to set provider as active.</span></span>

    ![Активация поставщика в BDM](./media/bdm_choose_provider.png)

> [!NOTE]
> <span data-ttu-id="f8fd0-170">Каждый шаблон BDM ссылается на поставщика как автора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-170">Each BDM template refers to the provider as the author of the configuration.</span></span> <span data-ttu-id="f8fd0-171">Это объясняется тем, что для шаблона необходим активный поставщик.</span><span class="sxs-lookup"><span data-stu-id="f8fd0-171">This is why an active provider is required for the template.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
