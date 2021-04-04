---
title: Обновление структуры шаблона бизнес-документа
description: В этой теме объясняется, как обновить структуру шаблона бизнес-документа с помощью функции управления бизнес-документами.
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 09813115544701ea3fffb6be06114bcdd63c0ba0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570456"
---
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="45a42-103">Обновление структуры шаблона бизнес-документа</span><span class="sxs-lookup"><span data-stu-id="45a42-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="45a42-104">В области **Структура шаблона** редактора шаблонов [Управление бизнес-документами](er-business-document-management.md) можно изменить шаблон бизнес-документа, [добавляя новые поля](er-bdm-add-field-to-excel-template.md) в шаблон в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="45a42-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="45a42-105">Структура шаблона затем автоматически обновляется в Dynamics 365 Finance, так что она отражает изменения, внесенные в области **Структура шаблона**.</span><span class="sxs-lookup"><span data-stu-id="45a42-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="45a42-106">Имеется также возможность изменить шаблон с помощью функций Office 365 Online.</span><span class="sxs-lookup"><span data-stu-id="45a42-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="45a42-107">Например, можно добавить на редактируемый лист новый именованный элемент, например рисунок или фигуру.</span><span class="sxs-lookup"><span data-stu-id="45a42-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="45a42-108">В этом случае структура шаблона не обновляется автоматически в Finance, и добавленный элемент не отображается в области **Структура шаблона**.</span><span class="sxs-lookup"><span data-stu-id="45a42-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="45a42-109">Обновите структуру шаблона вручную в Finance, выбрав **Обновить структуру** на странице редактора шаблонов.</span><span class="sxs-lookup"><span data-stu-id="45a42-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="45a42-110">Чтобы получить дополнительные сведения об этой функции, выполните следующий пример.</span><span class="sxs-lookup"><span data-stu-id="45a42-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="45a42-111">Пример. Обновление структуры шаблона бизнес-документа</span><span class="sxs-lookup"><span data-stu-id="45a42-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="45a42-112">В этом примере показано, как системный администратор может обновить структуру шаблона бизнес-документа в модуле Finance после изменения шаблона в Office Online.</span><span class="sxs-lookup"><span data-stu-id="45a42-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="45a42-113">В следующих разделах описаны выполняемые шаги.</span><span class="sxs-lookup"><span data-stu-id="45a42-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="45a42-114">Подготовка шаблона бизнес-документа для редактирования</span><span class="sxs-lookup"><span data-stu-id="45a42-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="45a42-115">Выполните следующие процедуры в разделе [Обзор управления бизнес-документами](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="45a42-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="45a42-116">Настройка параметров ER</span><span class="sxs-lookup"><span data-stu-id="45a42-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="45a42-117">Импорт решений электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="45a42-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="45a42-118">Включение управления бизнес-документами</span><span class="sxs-lookup"><span data-stu-id="45a42-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="45a42-119">Настроить параметры</span><span class="sxs-lookup"><span data-stu-id="45a42-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="45a42-120">Редактирование шаблона бизнес-документа</span><span class="sxs-lookup"><span data-stu-id="45a42-120">Edit a business document template</span></span>

1. <span data-ttu-id="45a42-121">В рабочей области **Управление бизнес-документами** выберите **Создать документ**.</span><span class="sxs-lookup"><span data-stu-id="45a42-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="45a42-122">На странице **Создание нового шаблона** выберите шаблон **Накладная с произвольным текстом (пример электронной отчетности) (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="45a42-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="45a42-123">Выберите **Создать документ**.</span><span class="sxs-lookup"><span data-stu-id="45a42-123">Select **Create document**.</span></span>
4. <span data-ttu-id="45a42-124">В поле **Заголовок** введите **Образец FTI Litware**</span><span class="sxs-lookup"><span data-stu-id="45a42-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="45a42-125">Выберите **ОК** для создания нового шаблона.</span><span class="sxs-lookup"><span data-stu-id="45a42-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="45a42-126">Если вы еще не выполнили вход в Office Online, вы [переходите на страницу входа Office 365](er-business-document-management.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="45a42-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#frequently-asked-questions).</span></span> <span data-ttu-id="45a42-127">Чтобы вернуться в среду Finance, нажмите кнопку **Назад** в браузере.</span><span class="sxs-lookup"><span data-stu-id="45a42-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="45a42-128">Новый шаблон открывается для редактирования во встроенном элементе управления Excel Online на странице редактора шаблонов.</span><span class="sxs-lookup"><span data-stu-id="45a42-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="45a42-129">[![Использование рабочей области управления бизнес-документами для запуска редактирования шаблона бизнес-документа](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="45a42-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="45a42-130">Просмотр текущей структуры редактируемого шаблона</span><span class="sxs-lookup"><span data-stu-id="45a42-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="45a42-131">В Excel Online на ленте на вкладке **Вид** в группе **Показать** выберите пункт **Линии сетки**.</span><span class="sxs-lookup"><span data-stu-id="45a42-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="45a42-132">В редактируемом шаблоне выберите прямоугольник над заголовком шаблона.</span><span class="sxs-lookup"><span data-stu-id="45a42-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="45a42-133">Этот прямоугольник представляет собой рисунок с именем **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="45a42-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="45a42-134">Если панель **Структура шаблона** скрыта, выберите **Показать структуру**.</span><span class="sxs-lookup"><span data-stu-id="45a42-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="45a42-135">В области **Структура шаблона** разверните **Отчет \> Накладная \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="45a42-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="45a42-136">Обратите внимание, что в структуре шаблонов в Finance элемент **rptHeaderCompLogo** представляется в качестве дочернего элемента **Отчет \> Накладная \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="45a42-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="45a42-137">[![Использование рабочей области управления бизнес-документами для просмотра текущей структуры редактируемого шаблона](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="45a42-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="45a42-138">Обновление структуры шаблона бизнес-документа путем удаления рисунка</span><span class="sxs-lookup"><span data-stu-id="45a42-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="45a42-139">В Excel Online в редактируемом шаблоне выберите изображение **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="45a42-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="45a42-140">Выполните одно из следующих действий, чтобы удалить выбранный рисунок из редактируемого шаблона:</span><span class="sxs-lookup"><span data-stu-id="45a42-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="45a42-141">Выберите клавишу **DELETE** на клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="45a42-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="45a42-142">Выберите и удерживайте (или щелкните правой кнопкой мыши) рисунок, затем выберите **Вырезать**.</span><span class="sxs-lookup"><span data-stu-id="45a42-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="45a42-143">Элемент **rptHeaderCompLogo** в настоящее время все еще присутствует в структуре шаблона в Finance, хотя рисунок больше не включен в шаблон Excel.</span><span class="sxs-lookup"><span data-stu-id="45a42-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="45a42-144">Выберите **Обновить структуру** для синхронизации структуры редактируемого шаблона в Excel и Finance.</span><span class="sxs-lookup"><span data-stu-id="45a42-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="45a42-145">В области **Структура шаблона** разверните **Отчет \> Накладная \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="45a42-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="45a42-146">Обратите внимание, что элемент **rptHeaderCompLogo** больше не включен в структуру шаблонов в модуле Finance.</span><span class="sxs-lookup"><span data-stu-id="45a42-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="45a42-147">[![Использование рабочей области управления бизнес-документами для удаления рисунка из шаблона бизнес-документа](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="45a42-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="45a42-148">Обновление структуры шаблона бизнес-документа путем добавления рисунка</span><span class="sxs-lookup"><span data-stu-id="45a42-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="45a42-149">В Excel Online на ленте на вкладке **Вставить** в группе **Иллюстрации** выберите пункт **Рисунок**.</span><span class="sxs-lookup"><span data-stu-id="45a42-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="45a42-150">Выберите **Выбрать файл**, перейдите к изображению, которое необходимо добавить, выберите его и затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="45a42-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="45a42-151">Выберите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="45a42-151">Select **Insert**.</span></span>
4. <span data-ttu-id="45a42-152">Переместите новый рисунок, пока он не будет в нужном месте.</span><span class="sxs-lookup"><span data-stu-id="45a42-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="45a42-153">По умолчанию Excel задаем имя рисунка.</span><span class="sxs-lookup"><span data-stu-id="45a42-153">By default, Excel names the picture.</span></span> <span data-ttu-id="45a42-154">Например, это может быть имя рисунка **Рисунок 2**.</span><span class="sxs-lookup"><span data-stu-id="45a42-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="45a42-155">Выберите **Обновить структуру** для синхронизации структуры редактируемого шаблона в Excel и Finance.</span><span class="sxs-lookup"><span data-stu-id="45a42-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="45a42-156">В области **Структура шаблона** разверните **Отчет \> Накладная \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="45a42-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="45a42-157">Обратите внимание, что новый рисунок теперь включен как элемент в структуру шаблона в модуле Finance.</span><span class="sxs-lookup"><span data-stu-id="45a42-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="45a42-158">[![Использование рабочей области управления бизнес-документами для добавления рисунка в шаблон бизнес-документа](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="45a42-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="45a42-159">Связанные ссылки</span><span class="sxs-lookup"><span data-stu-id="45a42-159">Related links</span></span>

[<span data-ttu-id="45a42-160">Обзор электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="45a42-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="45a42-161">Обзор управления бизнес-документами</span><span class="sxs-lookup"><span data-stu-id="45a42-161">Business document management overview</span></span>](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]