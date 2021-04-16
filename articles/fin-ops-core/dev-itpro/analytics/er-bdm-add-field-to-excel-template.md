---
title: Добавление новых полей в шаблон бизнес-документа в Microsoft Excel
description: В этой теме приводятся сведения о добавлении новых полей в шаблон бизнес-документа в Microsoft Excel с помощью функции управления бизнес-документами.
author: NickSelin
ms.date: 11/15/2019
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
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 991fe4ea56a2726c5df835cfc90a390cef2d5df5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751138"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a><span data-ttu-id="904df-103">Добавление новых полей в шаблон бизнес-документа в Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="904df-103">Add new fields to a business document template in Microsoft Excel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="904df-104">В шаблон можно добавлять новые поля, используемые для создания бизнес-документов в формате Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="904df-104">You can add new fields to a template that is used to generate business documents in Microsoft Excel format.</span></span> <span data-ttu-id="904df-105">Эти поля могут быть добавлены в качестве заполнителей, используемых для заполнения созданных документов необходимыми сведениями из приложения.</span><span class="sxs-lookup"><span data-stu-id="904df-105">These fields can be added as placeholders that are used to fill generated documents with required information from the application.</span></span> <span data-ttu-id="904df-106">Для каждого добавляемого поля можно также задать привязку к источникам данных, чтобы указать, какие данные приложения будут вводиться в поле при использовании шаблона для создания бизнес-документов.</span><span class="sxs-lookup"><span data-stu-id="904df-106">For every field that you add, you can also specify a binding to the data sources, to specify what application data will be entered in the field when the template is used to generate business documents.</span></span>

<span data-ttu-id="904df-107">Чтобы получить дополнительные сведения об этой функции, выполните пример в этой теме.</span><span class="sxs-lookup"><span data-stu-id="904df-107">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="904df-108">В этом примере показано, как обновить шаблон, чтобы заполнить поля в создаваемых формах накладных с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="904df-108">This example shows how to update a template to fill in the fields in free text invoice forms that are generated.</span></span>

## <a name="configure-business-document-management-to-edit-templates"></a><span data-ttu-id="904df-109">Настройка управления бизнес-документами для редактирования шаблонов</span><span class="sxs-lookup"><span data-stu-id="904df-109">Configure Business document management to edit templates</span></span>

<span data-ttu-id="904df-110">Так как управление бизнес-документами (BDM) основано на верхней части [Обзор электронной отчетности (ER)](general-electronic-reporting.md), необходимо настроить необходимые параметры ER и BDM, прежде чем можно будет начать работать с BDM.</span><span class="sxs-lookup"><span data-stu-id="904df-110">Because Business document management (BDM) is built on top of the [Electronic reporting (ER) overview](general-electronic-reporting.md) framework, you must configure the required ER and BDM parameters before you can start to work with BDM.</span></span>

1.  <span data-ttu-id="904df-111">Выполните вход в экземпляр Microsoft Dynamics 365 Finance в качестве системного администратора.</span><span class="sxs-lookup"><span data-stu-id="904df-111">Sign in to the instance of Microsoft Dynamics 365 Finance as the system administrator.</span></span>
2.  <span data-ttu-id="904df-112">Выполните следующие шаги примера в разделе [Обзор управления бизнес-документами](er-business-document-management.md):</span><span class="sxs-lookup"><span data-stu-id="904df-112">Complete the following steps of the example in the [Business document management overview](er-business-document-management.md) topic:</span></span>

    1.  <span data-ttu-id="904df-113">Настройте параметры ER.</span><span class="sxs-lookup"><span data-stu-id="904df-113">Configure ER parameters.</span></span>
    2.  <span data-ttu-id="904df-114">Включите BDM.</span><span class="sxs-lookup"><span data-stu-id="904df-114">Turn on BDM.</span></span>

<span data-ttu-id="904df-115">Теперь можно приступить к использованию БДМ для редактирования шаблонов бизнес-документов.</span><span class="sxs-lookup"><span data-stu-id="904df-115">You can now start to use BDM to edit business document templates.</span></span>

## <a name="import-er-solutions-that-contain-a-template"></a><span data-ttu-id="904df-116">Импорт решений ER, содержащих шаблон</span><span class="sxs-lookup"><span data-stu-id="904df-116">Import ER solutions that contain a template</span></span>

<span data-ttu-id="904df-117">В примере в этой процедуре используется официально опубликованное решение ER.</span><span class="sxs-lookup"><span data-stu-id="904df-117">The example in this procedure uses the officially published ER solution.</span></span> <span data-ttu-id="904df-118">Необходимо импортировать конфигурации ER данного решения в текущий экземпляр Finance.</span><span class="sxs-lookup"><span data-stu-id="904df-118">You must import the ER configurations of this solution into your current instance of Finance.</span></span>

<span data-ttu-id="904df-119">Конфигурация формата ER **Накладная с произвольным текстом (Excel)** для этого решения содержит шаблон бизнес-документа в формате Excel, который можно редактировать с помощью BDM.</span><span class="sxs-lookup"><span data-stu-id="904df-119">The **Free text invoice (Excel)** ER format configuration of this solution contains the business document template in Excel format that can be edited by using BDM.</span></span> <span data-ttu-id="904df-120">Импортируйте последнюю версию конфигурации формата ER Microsoft Dynamics Lifecycle Service (LCS).</span><span class="sxs-lookup"><span data-stu-id="904df-120">Import the latest version of this ER format configuration from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="904df-121">Соответствующая модель данных ER и конфигурации сопоставления модели ER будут импортированы автоматически.</span><span class="sxs-lookup"><span data-stu-id="904df-121">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

<span data-ttu-id="904df-122">Дополнительные сведения о способе импорта конфигураций ER см. в разделе [Управление жизненным циклом конфигурации ER](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="904df-122">For more information about how to import ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Страница общей библиотеки активов LCS](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a><span data-ttu-id="904df-124">Редактирование шаблона решения ER</span><span class="sxs-lookup"><span data-stu-id="904df-124">Edit the ER solution template</span></span>

1.  <span data-ttu-id="904df-125">Выполните вход как пользователь, имеющий доступ к рабочей области **Управление бизнес-документами**.</span><span class="sxs-lookup"><span data-stu-id="904df-125">Sign in as a user who has access to the **Business document management** workspace.</span></span>
2.  <span data-ttu-id="904df-126">Откройте рабочую область **Управление бизнес-документами**.</span><span class="sxs-lookup"><span data-stu-id="904df-126">Open the **Business document management** workspace.</span></span>

    ![Рабочая область управления бизнес-документами](./media/BDM-AddFldExcel-Workspace.png)

3.  <span data-ttu-id="904df-128">В сетке выберите шаблон накладной с **Накладная с произвольным текстом (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="904df-128">In the grid, select the **Free text invoice (Excel)** template.</span></span>
4.  <span data-ttu-id="904df-129">В правой области выберите **Создать шаблон**, чтобы создать шаблон, основанный на выбранном шаблоне.</span><span class="sxs-lookup"><span data-stu-id="904df-129">In the right pane, select **New template** to create a new template that is based on the selected template.</span></span>
5.  <span data-ttu-id="904df-130">В поле **Название** введите в качестве названия нового шаблона **Накладная с произвольным текстом (Excel) Contoso**.</span><span class="sxs-lookup"><span data-stu-id="904df-130">In the **Title** field, enter **Free text invoice (Excel) Contoso** as the title of the new template.</span></span>
6.  <span data-ttu-id="904df-131">Выберите **ОК**, чтобы подтвердить начало процесса редактирования.</span><span class="sxs-lookup"><span data-stu-id="904df-131">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="904df-132">Появится страница редактора шаблонов BDM.</span><span class="sxs-lookup"><span data-stu-id="904df-132">The BDM template editor page appears.</span></span> <span data-ttu-id="904df-133">Можно использовать Microsoft 365 для редактирования выбранного шаблона в интерактивном режиме во встроенном элементе управления.</span><span class="sxs-lookup"><span data-stu-id="904df-133">You can use Microsoft 365 to edit the selected template online in the embedded control.</span></span>

![Страница редактора шаблонов BDM](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a><span data-ttu-id="904df-135">Добавление метки для нового поля в шаблон</span><span class="sxs-lookup"><span data-stu-id="904df-135">Add the label for a new field to the template</span></span>

1.  <span data-ttu-id="904df-136">На странице редактора шаблонов BDM в ленте Excel на вкладке **Вид** установите флажки **Заголовки и линии сетки** для редактируемого шаблона Excel.</span><span class="sxs-lookup"><span data-stu-id="904df-136">On the BDM template editor page, on the Excel ribbon, on the **View** tab, select the **Headings and Gridlines** check boxes for the editable Excel template.</span></span>

    ![Установлены флажки заголовков и линий сетки](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  <span data-ttu-id="904df-138">Выберите ячейки **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="904df-138">Select cells **E8:F8**.</span></span>
3.  <span data-ttu-id="904df-139">В ленте Excel на вкладке **Главная** выберите **Объединить и выровнять по центру**, чтобы объединить выбранные ячейки в новую объединенную ячейку **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="904df-139">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **E8:F8** cell.</span></span>
4.  <span data-ttu-id="904df-140">В объединенной ячейке **E8:F8** введите **URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="904df-140">In the merged cell **E8:F8**, enter **URL**.</span></span>
5.  <span data-ttu-id="904df-141">Выберите объединенную ячейку **E7:F7**, выберите **Форматирование по образцу**, а затем выберите объединенную ячейку **E8:F8**, чтобы отформатировать ее так же, как и объединенную ячейку **E7: F7**.</span><span class="sxs-lookup"><span data-stu-id="904df-141">Select merged cell **E7:F7**, select **Format painter**, and then select merged cell **E8:F8** to format it in the same way as merged cell **E7:F7**.</span></span>

    ![Добавление метки нового поля в шаблон](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a><span data-ttu-id="904df-143">Форматирование шаблона для резервирования пространства для нового поля</span><span class="sxs-lookup"><span data-stu-id="904df-143">Format the template to reserve space for a new field</span></span>

1.  <span data-ttu-id="904df-144">На странице редактора шаблонов BDM выберите объединенную ячейку **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="904df-144">On the BDM template editor page, select merged cell **G8:H8**.</span></span>
2.  <span data-ttu-id="904df-145">В ленте Excel на вкладке **Главная** выберите **Объединить и выровнять по центру**, чтобы объединить выбранные ячейки в новую объединенную ячейку **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="904df-145">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **G8:H8** cell.</span></span>
3.  <span data-ttu-id="904df-146">Выберите объединенную ячейку **G7:H7**, выберите **Форматирование по образцу**, а затем выберите объединенную ячейку **G8:H8**, чтобы отформатировать ее так же, как и объединенную ячейку **G7: H7**.</span><span class="sxs-lookup"><span data-stu-id="904df-146">Select merged cell **G7:H7**, select **Format painter**, and then select merged cell **G8:H8** to format it in the same way as merged cell **G7:H7**.</span></span>

    ![Пространство, зарезервированное для нового поля](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  <span data-ttu-id="904df-148">В поле **Имя** выберите **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="904df-148">In the **Name** box field, select **CompanyInfo**.</span></span>

    <span data-ttu-id="904df-149">Диапазон **CompanyInfo** текущего шаблона Excel содержит все поля, используемые для заполнения заголовка созданного отчета сведениями о текущей компании в качестве стороны продавца.</span><span class="sxs-lookup"><span data-stu-id="904df-149">The **CompanyInfo** range of the current Excel template holds all the fields that are used to fill the header of a generated report with the details of the current company as a seller party.</span></span>

    ![Выбран диапазон CompanyInfo](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a><span data-ttu-id="904df-151">Добавление нового поля в шаблон</span><span class="sxs-lookup"><span data-stu-id="904df-151">Add a new field to the template</span></span>

1.  <span data-ttu-id="904df-152">На странице **редактора шаблонов BDM** в области действий выберите **Показать формат**.</span><span class="sxs-lookup"><span data-stu-id="904df-152">On the **BDM template editor** page, on the Action Pane, select **Show format**.</span></span>
2.  <span data-ttu-id="904df-153">В области **Структура шаблона** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="904df-153">In the **Template structure** pane, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="904df-154">Необходимо откорректировать раздел шаблона, который будет использоваться в качестве нового поля.</span><span class="sxs-lookup"><span data-stu-id="904df-154">You must adjust the section of the template that you want to use as a new field.</span></span> <span data-ttu-id="904df-155">Эта корректировка уже была выполнена путем форматирования объединенной ячейки **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="904df-155">You already made this adjustment by formatting merged cell **G8:H8**.</span></span>

    ![Добавление нового поля в шаблон](./media/BDM-AddFldExcel-AddCell.png)

3.  <span data-ttu-id="904df-157">Выберите **Excel\Ячейка**, чтобы добавить новое поле в качестве ячейки в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="904df-157">Select **Excel\Cell** to add a new field as a cell in the template.</span></span>

    <span data-ttu-id="904df-158">Можно выбрать **Excel\Диапазон**, если необходимо добавить новый диапазон в шаблон.</span><span class="sxs-lookup"><span data-stu-id="904df-158">You can select **Excel\Range** if you want to add a new range to the template.</span></span> <span data-ttu-id="904df-159">Введенный диапазон может содержать несколько ячеек.</span><span class="sxs-lookup"><span data-stu-id="904df-159">The range that is entered can contain multiple cells.</span></span> <span data-ttu-id="904df-160">Эти ячейки можно будет добавить позже.</span><span class="sxs-lookup"><span data-stu-id="904df-160">You can add these cells later.</span></span>
    
    <span data-ttu-id="904df-161">Обратите внимание, что компонент шаблона **CompanyInfo** автоматически выбирается в области **Структура шаблона**, поскольку он является наиболее подходящим родительским компонентом в текущей структуре шаблона для добавляемого поля.</span><span class="sxs-lookup"><span data-stu-id="904df-161">Notice that the **CompanyInfo** template component, is automatically selected in the **Template structure** pane, because it's the most suitable parent component in the current template structure for the field that you're adding.</span></span>
    
4.  <span data-ttu-id="904df-162">В поле **Диапазон Excel** введите **CompanyURL_Value**.</span><span class="sxs-lookup"><span data-stu-id="904df-162">In the **Excel range** field, enter **CompanyURL_Value**.</span></span>
5.  <span data-ttu-id="904df-163">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="904df-163">Select **OK**.</span></span>

    ![Поле CompanyURL_Value добавляется в структуру шаблона](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  <span data-ttu-id="904df-165">В области **Структура шаблона** выберите кнопку с многоточием (...), а затем выберите **Показать привязки**.</span><span class="sxs-lookup"><span data-stu-id="904df-165">In the **Template structure** pane, select the ellipsis button (...), and then select **Show bindings**.</span></span>

    ![Отображение выбранных привязок](./media/BDM-AddFldExcel-ShowBindings.png)

    <span data-ttu-id="904df-167">В области **Структура шаблона** теперь отображаются источники данных, доступные в основном формате ER.</span><span class="sxs-lookup"><span data-stu-id="904df-167">The **Template structure** pane now shows the data sources that are available in the underlying ER format.</span></span>

7.  <span data-ttu-id="904df-168">Выберите **CompanyInfo_Value** как поле, которое планируется привязать к источнику данных в основном формате ER.</span><span class="sxs-lookup"><span data-stu-id="904df-168">Select **CompanyInfo_Value** as the field that you plan to bind to a data source of the underlying ER format.</span></span>
8.  <span data-ttu-id="904df-169">В разделе **Источники данных** панели **Структура шаблона** раскройте **Модель \> InvoiceBase \> CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="904df-169">In the **Data sources** section of the **Template structure** pane, expand **Model \> InvoiceBase \> CompanyInfo**.</span></span>
9.  <span data-ttu-id="904df-170">В области **CompanyInfo** выберите элемент **WebsiteURI**.</span><span class="sxs-lookup"><span data-stu-id="904df-170">Under **CompanyInfo**, select the **WebsiteURI** item.</span></span>

    ![Выбран элемент WebsiteURI](./media/BDM-AddFldExcel-BindURL.png)

10. <span data-ttu-id="904df-172">Выберите **Связать**.</span><span class="sxs-lookup"><span data-stu-id="904df-172">Select **Bind**.</span></span>
11. <span data-ttu-id="904df-173">В области **Структура шаблона** выберите **Сохранить** и закройте страницу редактора шаблонов BDM.</span><span class="sxs-lookup"><span data-stu-id="904df-173">In the **Template structure** pane, select **Save**, and then close the BDM template editor page.</span></span>

<span data-ttu-id="904df-174">В рабочей области **Управление бизнес-документами** на вкладке **Шаблон** в правой области отображается обновленный шаблон.</span><span class="sxs-lookup"><span data-stu-id="904df-174">In the **Business document management** workspace, the **Template** tab in the right pane shows the updated template.</span></span> <span data-ttu-id="904df-175">Обратите внимание, что в сетке поле **Статус** для измененного шаблона изменено на **Черновик**, а поле **Версия** больше не пустое.</span><span class="sxs-lookup"><span data-stu-id="904df-175">In the grid, notice that the **Status** field for the edited template has been changed to **Draft**, and the **Revision** field is no longer blank.</span></span> <span data-ttu-id="904df-176">Такие изменения означают, что процесс редактирования этого шаблона был запущен.</span><span class="sxs-lookup"><span data-stu-id="904df-176">These changes indicate that the process of editing this template has been started.</span></span>

![Измененный шаблон в рабочей области управления бизнес-документами](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a><span data-ttu-id="904df-178">Просмотр настроек компании</span><span class="sxs-lookup"><span data-stu-id="904df-178">Review company settings</span></span>

1.  <span data-ttu-id="904df-179">Перейдите в раздел **Управление организацией \> Организации \> Юридические лица**.</span><span class="sxs-lookup"><span data-stu-id="904df-179">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="904df-180">Убедитесь, что URL-адрес компании введен на экспресс-вкладке **Контактная информация**.</span><span class="sxs-lookup"><span data-stu-id="904df-180">On the **Contact information** FastTab, verify that the company URL is entered.</span></span>

![URL-адрес компании, введенный на странице юридических лиц](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a><span data-ttu-id="904df-182">Создание бизнес-документов для тестирования обновленного шаблона</span><span class="sxs-lookup"><span data-stu-id="904df-182">Generate business documents to test the updated template</span></span>

1.  <span data-ttu-id="904df-183">В приложении измените компанию на **USMF** и перейдите **Расчеты с клиентами \> Накладные \> Все накладные с произвольным текстом**.</span><span class="sxs-lookup"><span data-stu-id="904df-183">In the application, change the company to **USMF**, and go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2.  <span data-ttu-id="904df-184">Выберите накладную **FTI-00000002**, затем выберите **Управление печатью**.</span><span class="sxs-lookup"><span data-stu-id="904df-184">Select invoice **FTI-00000002**, and then select **Print management**.</span></span>
3.  <span data-ttu-id="904df-185">В левой области раскройте **Модуль — Расчеты с клиентами \> Документы \> Накладная с произвольным текстом**.</span><span class="sxs-lookup"><span data-stu-id="904df-185">In the left pane, expand **Module - accounts receivable \> Documents \> Free text invoice**.</span></span>
4.  <span data-ttu-id="904df-186">В **Накладная с произвольным текстом** выберите уровень **Исходный документ**, чтобы задать область накладных для обработки.</span><span class="sxs-lookup"><span data-stu-id="904df-186">Under **Free text invoice**, select the **Original document** level to specify the scope of invoices for processing.</span></span>
5.  <span data-ttu-id="904df-187">В правой области в поле **Формат отчета** выберите шаблон **Накладная с произвольным текстом (Excel) Contoso** для указанного уровня документа.</span><span class="sxs-lookup"><span data-stu-id="904df-187">In the right pane, in the **Report format** field, select the **Free text invoice (Excel) Contoso** template for the specified document level.</span></span>

    ![Выбранный шаблон "Накладная с произвольным текстом (Excel) Contoso"](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  <span data-ttu-id="904df-189">Нажмите клавишу **Esc**, чтобы закрыть текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="904df-189">Press **Esc** to close the current page.</span></span>
7.  <span data-ttu-id="904df-190">Выберите **Печать \> Выбранное**.</span><span class="sxs-lookup"><span data-stu-id="904df-190">Select **Print \> Selected**.</span></span>
8.  <span data-ttu-id="904df-191">Загрузите созданный документ и откройте его в Excel.</span><span class="sxs-lookup"><span data-stu-id="904df-191">Download the generated document, and open it in Excel.</span></span>

    ![Накладная с произвольным текстом в Excel](./media/BDM-AddFldExcel-PreviewReport.png)

<span data-ttu-id="904df-193">Измененный шаблон используется для создания отчета по накладной с произвольным текстом для выбранной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="904df-193">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="904df-194">Чтобы проанализировать влияние изменений, введенных в шаблон, на этот отчет, можно выполнить этот отчет в одном сеансе приложения сразу после того, как был изменен шаблон в другом сеансе приложения.</span><span class="sxs-lookup"><span data-stu-id="904df-194">To analyze how this report is affected by changes that you make to the template, run the report in one application session immediately after you change the template in another application session.</span></span>

## <a name="related-links"></a><span data-ttu-id="904df-195">Связанные ссылки</span><span class="sxs-lookup"><span data-stu-id="904df-195">Related links</span></span>

[<span data-ttu-id="904df-196">Обзор электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="904df-196">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="904df-197">Обзор управления бизнес-документами</span><span class="sxs-lookup"><span data-stu-id="904df-197">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="904df-198">Разработка конфигурации для создания отчетов в формате OPENXML</span><span class="sxs-lookup"><span data-stu-id="904df-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]