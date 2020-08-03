---
title: Разработка конфигурации для создания документов в формате Excel
description: В этом разделе приводятся сведения о создании формата электронной отчетности (ER) для заполнения шаблона Excel, а затем создание исходящих документов в формате Excel.
author: NickSelin
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e889b08f10c5d0c95fed7c9e422340706bdd154a
ms.sourcegitcommit: 67ce81c57194afb26a04ae4c0b7509e0efa32afc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "3375821"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a><span data-ttu-id="dd37a-103">Разработка конфигурации для создания документов в формате Excel</span><span class="sxs-lookup"><span data-stu-id="dd37a-103">Design a configuration for generating documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dd37a-104">Можно разработать конфигурацию формата [электронной отчетности (ER)](general-electronic-reporting.md), имеющую [компонент формата](general-electronic-reporting.md#FormatComponentOutbound) ER, который можно настроить для создания исходящего документа в формате книги Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="dd37a-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) format configuration that has an ER [format component](general-electronic-reporting.md#FormatComponentOutbound) that you can configure to generate an outbound document in a Microsoft Excel workbook format.</span></span> <span data-ttu-id="dd37a-105">Для этой цели необходимо использовать специальный компонент формата ER.</span><span class="sxs-lookup"><span data-stu-id="dd37a-105">Specific ER format components must be used for this purpose.</span></span>

<span data-ttu-id="dd37a-106">Для получения дополнительных сведений об этой возможности следуйте указаниям в разделе [Создание конфигурации для создания отчетов в формате OPENXML](tasks/er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="dd37a-106">To learn more about this feature, follow the steps in the topic, [Design a configuration for generating reports in OPENXML format](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="add-a-new-er-format"></a><span data-ttu-id="dd37a-107">Добавление нового формата ER</span><span class="sxs-lookup"><span data-stu-id="dd37a-107">Add a new ER format</span></span>

<span data-ttu-id="dd37a-108">При добавлении новой конфигурации формата ER для создания исходящего документа в формате книги Excel необходимо либо выбрать значение **Excel** для атрибута **типа формата** для формата, либо оставить атрибут **тип формата** пустым.</span><span class="sxs-lookup"><span data-stu-id="dd37a-108">When you add a new ER format configuration to generate an outbound document in an Excel workbook format, you must either select the **Excel** value for the **Format type** attribute of the format or leave the **Format type** attribute blank.</span></span>

- <span data-ttu-id="dd37a-109">При выборе **Excel** можно настроить формат для создания исходящего документа только в формате Excel.</span><span class="sxs-lookup"><span data-stu-id="dd37a-109">If you select **Excel**, you can configure the format to generate an outbound document only in Excel format.</span></span>
- <span data-ttu-id="dd37a-110">Если оставить этот атрибут пустым, можно настроить формат для создания исходящего документа в любом формате, поддерживаемом структурой ER.</span><span class="sxs-lookup"><span data-stu-id="dd37a-110">If you leave the attribute blank, you can configure the format to generate an outbound document in any format that is supported by the ER framework.</span></span>

<span data-ttu-id="dd37a-111">Чтобы настроить компонент "формат ER" конфигурации, выберите **конструктор** на панели операций и откройте компонент формата ER для редактирования в конструкторе операций ER.</span><span class="sxs-lookup"><span data-stu-id="dd37a-111">To configure the ER format component of the configuration, select **Designer** on the Action Pane, and open the ER format component for editing in the ER Operation designer.</span></span>

![Страница конфигураций](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a><span data-ttu-id="dd37a-113">Компонент файла Excel</span><span class="sxs-lookup"><span data-stu-id="dd37a-113">Excel file component</span></span>

### <a name="manual-entry"></a><span data-ttu-id="dd37a-114">Ручной ввод</span><span class="sxs-lookup"><span data-stu-id="dd37a-114">Manual entry</span></span>

<span data-ttu-id="dd37a-115">Для создания исходящего документа в формате Excel необходимо добавить компонент **файла\\Excel** в настроенный формат ER.</span><span class="sxs-lookup"><span data-stu-id="dd37a-115">You must add an **Excel\\File** component to the configured ER format to generate an outbound document in Excel format.</span></span>

![Компонент Excel\файл](./media/er-excel-format-add-file-component.png)

<span data-ttu-id="dd37a-117">Чтобы указать макет для исходящего документа, вложите в компонент **файл\\Excel** книгу Excel с расширением .xlsx в качестве шаблона для исходящих документов.</span><span class="sxs-lookup"><span data-stu-id="dd37a-117">To specify the layout of the outbound document, attach an Excel workbook that has the .xlsx extension to the **Excel\\File** component as the template for outbound documents.</span></span>

> [!NOTE]
> <span data-ttu-id="dd37a-118">При присоединении шаблона вручную необходимо использовать [тип документа](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types), который был настроен для этой цели в [параметрах ER](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span><span class="sxs-lookup"><span data-stu-id="dd37a-118">When you manually attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has been configured for that purpose in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span></span>

![Добавление вложения в компонент Excel\файл](./media/er-excel-format-add-file-component2.png)

<span data-ttu-id="dd37a-120">Чтобы указать, как будет заполняться заданный шаблон при выполнении настроенного формата ER, необходимо добавить вложенные компоненты **Лист**, **Диапазон**, и **Ячейка** к компоненту **Excel\\файл**.</span><span class="sxs-lookup"><span data-stu-id="dd37a-120">To specify how the attached template will be filled in when you run the configured ER format, you must add nested **Sheet**, **Range**, and **Cell** components to the **Excel\\File** component.</span></span> <span data-ttu-id="dd37a-121">Каждый вложенный компонент должен быть связан с именованной номенклатурой Excel.</span><span class="sxs-lookup"><span data-stu-id="dd37a-121">Each nested component must be associated with an Excel named item.</span></span>

### <a name="template-import"></a><span data-ttu-id="dd37a-122">Импорт шаблона</span><span class="sxs-lookup"><span data-stu-id="dd37a-122">Template import</span></span>

<span data-ttu-id="dd37a-123">Можно выбрать **Импорт из Excel** на вкладке **Импорт** панели операций для импорта нового шаблона в пустой формат ER.</span><span class="sxs-lookup"><span data-stu-id="dd37a-123">You can select **Import from Excel** on the **Import** tab of the Action Pane to import a new template into a blank ER format.</span></span> <span data-ttu-id="dd37a-124">В этом примере компонент **Excel\\файл** будет создан автоматически, и к нему будет присоединяться импортированный шаблон.</span><span class="sxs-lookup"><span data-stu-id="dd37a-124">In this example, an **Excel\\File** component will be created automatically, and the imported template will be attached to it.</span></span> <span data-ttu-id="dd37a-125">Все необходимые компоненты ER также будут созданы автоматически на основе списка обнаруженных именованных номенклатур Excel.</span><span class="sxs-lookup"><span data-stu-id="dd37a-125">All required ER components will also be created automatically, based on the list of Excel named items that are discovered.</span></span>

![Выберите Импорт из Excel](./media/er-excel-format-import-template.png)

> [!NOTE]
> <span data-ttu-id="dd37a-127">Если требуется создать необязательный элемент **Лист** в редактируемом формате ER, установите для параметра **Создать элемент формата листа Excel** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="dd37a-127">If you want to create the optional **Sheet** element in the editable ER format, set the **Create Excel Sheet format element** option to **Yes**.</span></span>

## <a name="sheet-component"></a><span data-ttu-id="dd37a-128">Компонент листа</span><span class="sxs-lookup"><span data-stu-id="dd37a-128">Sheet component</span></span>

<span data-ttu-id="dd37a-129">Компонент **Лист** указывает лист прилагаемой книги Excel, который должен быть заполнен.</span><span class="sxs-lookup"><span data-stu-id="dd37a-129">The **Sheet** component indicates a worksheet of the attached Excel workbook that must be filled in.</span></span> <span data-ttu-id="dd37a-130">Имя листа в шаблоне Excel определяется в свойстве **Лист** этого компонента.</span><span class="sxs-lookup"><span data-stu-id="dd37a-130">The name of the worksheet in an Excel template is defined in the **Sheet** property of this component.</span></span>

> [!NOTE]
> <span data-ttu-id="dd37a-131">Этот компонент не является обязательным для книг Excel, содержащих один лист.</span><span class="sxs-lookup"><span data-stu-id="dd37a-131">This component is optional for Excel workbooks that contain a single worksheet.</span></span>

<span data-ttu-id="dd37a-132">На вкладке **Сопоставление** в конструкторе операций ER можно настроить свойство **Включено** для компонента **листа**, чтобы указать, должен ли компонент быть помещен в созданный документ:</span><span class="sxs-lookup"><span data-stu-id="dd37a-132">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Sheet** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="dd37a-133">Если выражение свойства **Включено** настроено так, что оно возвращает значение **истина** во время выполнения, или если какое-либо выражение не настроено, в созданный документ будет помещен соответствующий лист.</span><span class="sxs-lookup"><span data-stu-id="dd37a-133">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate worksheet will be put in the generated document.</span></span>
- <span data-ttu-id="dd37a-134">Если выражение свойства **Включено** настроено на возврат значения **Ложь** во время выполнения, созданный документ не будет содержать лист.</span><span class="sxs-lookup"><span data-stu-id="dd37a-134">If an expression of the **Enabled** property is configured to return **False** at runtime, the generated document won't contain a worksheet.</span></span>

![Пример компонента листа](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a><span data-ttu-id="dd37a-136">Компонент Диапазон</span><span class="sxs-lookup"><span data-stu-id="dd37a-136">Range component</span></span>

<span data-ttu-id="dd37a-137">Компонент **диапазон** указывает диапазон Excel, который должен управляться этим компонентом ER.</span><span class="sxs-lookup"><span data-stu-id="dd37a-137">The **Range** component indicates an Excel range that must be controlled by this ER component.</span></span> <span data-ttu-id="dd37a-138">Имя диапазона определяется в свойстве **Диапазон Excel** этого компонента.</span><span class="sxs-lookup"><span data-stu-id="dd37a-138">The name of the range is defined in the **Excel range** property of this component.</span></span>

<span data-ttu-id="dd37a-139">Свойство **Направление репликации** определяет, будет ли и каким образом повторяться диапазон в созданном документе:</span><span class="sxs-lookup"><span data-stu-id="dd37a-139">The **Replication direction** property specifies whether and how the range will be repeated in a generated document:</span></span>

- <span data-ttu-id="dd37a-140">Если для свойства **Направление репликации** установлено значение **Без репликации** , соответствующий диапазон Excel не будет повторяться в созданном документе.</span><span class="sxs-lookup"><span data-stu-id="dd37a-140">If the **Replication direction** property is set to **No replication**, the appropriate Excel range won't be repeated in the generated document.</span></span>
- <span data-ttu-id="dd37a-141">Если для свойства **Направление репликации** установлено значение **Вертикально** , соответствующий диапазон Excel будет повторяться в созданном документе.</span><span class="sxs-lookup"><span data-stu-id="dd37a-141">If the **Replication direction** property is set to **Vertical**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="dd37a-142">Каждый реплицируемый диапазон помещается под исходным диапазоном шаблона Excel.</span><span class="sxs-lookup"><span data-stu-id="dd37a-142">Every replicated range is put below the original range in an Excel template.</span></span> <span data-ttu-id="dd37a-143">Число повторов определяется числом записей в источнике данных типа **списка записей**, привязанного к этому компоненту ER.</span><span class="sxs-lookup"><span data-stu-id="dd37a-143">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>
- <span data-ttu-id="dd37a-144">Если для свойства **Направление репликации** установлено значение **Горизонтально** , соответствующий диапазон Excel будет повторяться в созданном документе.</span><span class="sxs-lookup"><span data-stu-id="dd37a-144">If the **Replication direction** property is set to **Horizontal**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="dd37a-145">Каждый реплицируемый диапазон помещается справа от исходным диапазоном шаблона Excel.</span><span class="sxs-lookup"><span data-stu-id="dd37a-145">Every replicated range is put to the right of the original range in an Excel template.</span></span> <span data-ttu-id="dd37a-146">Число повторов определяется числом записей в источнике данных типа **списка записей**, привязанного к этому компоненту ER.</span><span class="sxs-lookup"><span data-stu-id="dd37a-146">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>

<span data-ttu-id="dd37a-147">Для получения дополнительных сведений о горизонтальной репликации выполните шаги разделе [Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel](tasks/er-horizontal-1.md).</span><span class="sxs-lookup"><span data-stu-id="dd37a-147">To learn more about horizontal replication, follow the steps in [Use horizontally expandable ranges to dynamically add columns in Excel reports](tasks/er-horizontal-1.md).</span></span>

<span data-ttu-id="dd37a-148">Компонент **диапазон** может иметь другие вложенные компоненты ER, которые используются для ввода значений в соответствующие именованные диапазоны Excel.</span><span class="sxs-lookup"><span data-stu-id="dd37a-148">The **Range** component can have other nested ER components that are used to enter values in the appropriate Excel named ranges.</span></span>

- <span data-ttu-id="dd37a-149">Если какой-либо компонент группы **Текст** используется для ввода значений, значение вводится в диапазон Excel в виде текстового значения.</span><span class="sxs-lookup"><span data-stu-id="dd37a-149">If any component of the **Text** group is used to enter values, the value is entered in an Excel range as a text value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dd37a-150">Этот шаблон используется для форматирования введенных значений на основе языкового стандарта, определенного в приложении.</span><span class="sxs-lookup"><span data-stu-id="dd37a-150">Use this pattern to format entered values based on the locale that is defined in the application.</span></span>

- <span data-ttu-id="dd37a-151">Если для ввода значений используется компонент **ячейка** группы **Excel**, значение вводится в диапазон Excel как значение типа данных, которое определяется привязкой этого компонента **ячейка** (например, **Строка**, **Вещественный** или **Целочисленный**).</span><span class="sxs-lookup"><span data-stu-id="dd37a-151">If the **Cell** component of the **Excel** group is used to enter values, the value is entered in an Excel range as a value of the data type that is defined by the binding of that **Cell** component (for example, **String**, **Real**, or **Integer**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="dd37a-152">Этот шаблон используется для того, чтобы приложение Excel могло форматировать введенные значения на основе языкового стандарта локального компьютера, открывающего исходящий документ.</span><span class="sxs-lookup"><span data-stu-id="dd37a-152">Use this pattern to enable the Excel application to format entered values based on the locale of the local computer that opens the outbound document.</span></span>

<span data-ttu-id="dd37a-153">На вкладке **Сопоставление** в конструкторе операций ER можно настроить свойство **Включено** для компонента **Диапазон**, чтобы указать, должен ли компонент быть помещен в созданный документ:</span><span class="sxs-lookup"><span data-stu-id="dd37a-153">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Range** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="dd37a-154">Если выражение свойства **Включено** настроено так, что оно возвращает значение **истина** во время выполнения, или если какое-либо выражение не настроено, в созданный документ будет помещен соответствующий диапазон.</span><span class="sxs-lookup"><span data-stu-id="dd37a-154">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate range will be filled in in the generated document.</span></span>
- <span data-ttu-id="dd37a-155">Если выражение свойства **Включено** настроено так, что оно возвращает значение **Ложь** во время выполнения, и если этот диапазон не представляет все строки или столбцы, в созданный документ не будет помещен соответствующий диапазон.</span><span class="sxs-lookup"><span data-stu-id="dd37a-155">If an expression of the **Enabled** property is configured to return **False** at runtime, and if this range doesn't represent the entire rows or columns, the appropriate range won't be filled in in the generated document.</span></span>
- <span data-ttu-id="dd37a-156">Если выражение свойства **Включено** настроено так, что оно возвращает значение **Ложь** во время выполнения, и этот диапазон представляет все строки или столбцы, созданный документ будет содержать эти строки и столбцы в виде скрытых строк и столбцов.</span><span class="sxs-lookup"><span data-stu-id="dd37a-156">If an expression of the **Enabled** property is configured to return **False** at runtime, and this range represents the entire rows or columns, the generated document will contain those rows and columns as hidden rows and columns.</span></span>

## <a name="cell-component"></a><span data-ttu-id="dd37a-157">Компонент ячейка</span><span class="sxs-lookup"><span data-stu-id="dd37a-157">Cell component</span></span>

<span data-ttu-id="dd37a-158">Компонент **ячейка** используется для заполнения именованных ячеек, фигур и изображений Excel.</span><span class="sxs-lookup"><span data-stu-id="dd37a-158">The **Cell** component is used to fill in Excel named cells, shapes, and pictures.</span></span> <span data-ttu-id="dd37a-159">Чтобы указать имя объекта Excel, которое должно быть заполнено компонентом ER **ячейка**, необходимо указать название этого объекта в свойстве **диапазон Excel** для компонента **ячейка**.</span><span class="sxs-lookup"><span data-stu-id="dd37a-159">To indicate an Excel named object that must be filled in by a **Cell** ER component, you must specify the name of that object in the **Excel range** property of the **Cell** component.</span></span>

<span data-ttu-id="dd37a-160">На вкладке **Сопоставление** в конструкторе операций ER можно настроить свойство **Включено** для компонента **Ячейка**, чтобы указать, должен ли объект быть помещен в созданный документ:</span><span class="sxs-lookup"><span data-stu-id="dd37a-160">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Cell** component to specify whether the object must be filled in in a generated document:</span></span>

- <span data-ttu-id="dd37a-161">Если выражение свойства **Включено** настроено так, что оно возвращает значение **истина** во время выполнения, или если какое-либо выражение не настроено, в созданный документ будет помещен соответствующий объект.</span><span class="sxs-lookup"><span data-stu-id="dd37a-161">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate object will be filled in in the generated document.</span></span> <span data-ttu-id="dd37a-162">Привязка этого компонента **ячейка** указывает значение, помещаемое в соответствующий объект.</span><span class="sxs-lookup"><span data-stu-id="dd37a-162">The binding of this **Cell** component specifies a value that is put in the appropriate object.</span></span>
- <span data-ttu-id="dd37a-163">Если выражение свойства **Включено** настроено на возврат значения **Ложь** во время выполнения, соответствующий объект не будет помещен в созданном документе.</span><span class="sxs-lookup"><span data-stu-id="dd37a-163">If an expression of the **Enabled** property is configured to return **False** at runtime, the appropriate object won't be filled in in the generated document.</span></span>

<span data-ttu-id="dd37a-164">Когда компонент **ячейка** настраивается на ввод значения в ячейку, она может быть привязана к источнику данных, который возвращает значение примитивного типа данных (например, **Строка**, **Вещественный** или **Целочисленный**).</span><span class="sxs-lookup"><span data-stu-id="dd37a-164">When a **Cell** component is configured to enter a value in a cell, it can be bound with a data source that returns the value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="dd37a-165">В этом случае значение вводится в ячейку как значение того же типа данных.</span><span class="sxs-lookup"><span data-stu-id="dd37a-165">In this case, the value is entered in the cell as a value of the same data type.</span></span>

<span data-ttu-id="dd37a-166">Когда компонент **ячейка** настраивается на ввод значения в форму Excel, она может быть привязана к источнику данных, который возвращает значение примитивного типа данных (например, **Строка**, **Вещественный** или **Целочисленный**).</span><span class="sxs-lookup"><span data-stu-id="dd37a-166">When a **Cell** component is configured to enter a value in an Excel shape, it can be bound with a data source that returns a value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="dd37a-167">В этом случае значение вводится в форму Excel как текст этой формы.</span><span class="sxs-lookup"><span data-stu-id="dd37a-167">In this case, the value is entered in the Excel shape as the text of that shape.</span></span> <span data-ttu-id="dd37a-168">Для значений типов данных, не являющихся **строками**, преобразование в текст выполняется автоматически.</span><span class="sxs-lookup"><span data-stu-id="dd37a-168">For values of data types that aren't **String**, the conversion to text is done automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="dd37a-169">Можно настроить компонент **ячейка** для заполнения формы только в тех случаях, когда поддерживается свойство текста формы.</span><span class="sxs-lookup"><span data-stu-id="dd37a-169">You can configure a **Cell** component to fill in a shape only in cases where a shape text property is supported.</span></span>

<span data-ttu-id="dd37a-170">Когда компонент **ячейка** настраивается на ввод значения в изображение Excel, она может быть привязана к источнику данных, который возвращает значение типа данных **Контейнер**, который представляет изображение в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="dd37a-170">When a **Cell** component is configured to enter a value in an Excel picture, it can be bound with a data source that returns a value of the **Container** data type that represents an image in binary format.</span></span> <span data-ttu-id="dd37a-171">В этом случае значение вводится в изображение Excel в виде изображения.</span><span class="sxs-lookup"><span data-stu-id="dd37a-171">In this case, the value is entered in the Excel picture as an image.</span></span>

> [!NOTE]
> <span data-ttu-id="dd37a-172">Все изображения и формы Excel перекрепляются по верхнему левому углу в конкретную ячейку или диапазон Excel.</span><span class="sxs-lookup"><span data-stu-id="dd37a-172">Every Excel picture and shape is considered to be anchored by its upper-left corner to a specific Excel cell or range.</span></span> <span data-ttu-id="dd37a-173">Если требуется копировать изображение или форму Excel, необходимо настроить ячейку или диапазон, для которых она была привязана, в качестве копируемой ячейки или диапазона.</span><span class="sxs-lookup"><span data-stu-id="dd37a-173">If you want to replicate an Excel picture or shape, you must configure the cell or range that it's anchored to as a replicated cell or range.</span></span>

<span data-ttu-id="dd37a-174">Дополнительные сведения о внедрении изображений и форм см. в разделе [Внедрение изображений и фигур в документы, создаваемые с помощью электронной отчетности](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="dd37a-174">To learn more about how to embed images and shapes, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="page-break-component"></a><span data-ttu-id="dd37a-175">Компонент Разрыв страницы</span><span class="sxs-lookup"><span data-stu-id="dd37a-175">Page break component</span></span>

<span data-ttu-id="dd37a-176">Компонент **Разрыв страниц** заставляет Excel начать новую страницу.</span><span class="sxs-lookup"><span data-stu-id="dd37a-176">The **PageBreak** component forces Excel to start a new page.</span></span> <span data-ttu-id="dd37a-177">Этот компонент не требуется, если необходимо использовать разбиение по страницам Excel по умолчанию, но его следует использовать, если требуется, чтобы Excel использовал формат ER для структурирования разбиения.</span><span class="sxs-lookup"><span data-stu-id="dd37a-177">This component isn't required when you want to use Excel's default paging, but you should use it when you want Excel to follow your ER format to structure paging.</span></span>

## <a name="edit-an-added-er-format"></a><span data-ttu-id="dd37a-178">Редактирование добавленного формата ER</span><span class="sxs-lookup"><span data-stu-id="dd37a-178">Edit an added ER format</span></span>

### <a name="update-a-template"></a><span data-ttu-id="dd37a-179">Обновление шаблона</span><span class="sxs-lookup"><span data-stu-id="dd37a-179">Update a template</span></span>

<span data-ttu-id="dd37a-180">Можно выбрать **Обновление из Excel** на вкладке **Импорт** панели операций для импорта обновленного шаблона в редактируемый формат ER.</span><span class="sxs-lookup"><span data-stu-id="dd37a-180">You can select **Update from Excel** on the **Import** tab of the Action Pane to import an updated template into an editable ER format.</span></span> <span data-ttu-id="dd37a-181">В ходе этого процесса шаблон выбранного компонента **Excel\\Файл** будет заменен новым шаблоном.</span><span class="sxs-lookup"><span data-stu-id="dd37a-181">During this process, a template of the selected **Excel\\File** component will be replaced by a new template.</span></span> <span data-ttu-id="dd37a-182">Содержимое редактируемого формата ER будет синхронизировано с содержимым обновленного шаблона ER.</span><span class="sxs-lookup"><span data-stu-id="dd37a-182">The content of the editable ER format will be synced with the content of the updated ER template.</span></span>

- <span data-ttu-id="dd37a-183">Новый компонент формата ER будет создан автоматически для каждого имени Excel, если компонент формата ER не найден в редактируемом формате.</span><span class="sxs-lookup"><span data-stu-id="dd37a-183">A new ER format component will automatically be created for every Excel name if the ER format component isn't found in the editable format.</span></span>
- <span data-ttu-id="dd37a-184">Если соответствующее имя Excel не найдено, все компоненты формата ER будут удалены из редактируемого формата ER.</span><span class="sxs-lookup"><span data-stu-id="dd37a-184">Every ER format component will be deleted from the editable ER format if the appropriate Excel name isn't found for it.</span></span>

> [!NOTE]
> <span data-ttu-id="dd37a-185">Задайте для параметра **Создать элемент формата листа Excel** значение **Да**, если требуется создать необязательный элемент **Лист** в редактируемом формате ER.</span><span class="sxs-lookup"><span data-stu-id="dd37a-185">Set the **Create Excel Sheet format element** option to **Yes** if you want to create the optional **Sheet** element in the editable ER format.</span></span>
>
> <span data-ttu-id="dd37a-186">Если редактируемый формат ER первоначально содержал элементы **лист**, рекомендуется настроить для параметра **Создать элемент формата листа Excel** значение **Да**, если импортируется обновленный шаблон.</span><span class="sxs-lookup"><span data-stu-id="dd37a-186">If the editable ER format originally contained **Sheet** elements, we recommend that you set the **Create Excel Sheet format element** option to **Yes** when you import an updated template.</span></span> <span data-ttu-id="dd37a-187">В противном случае все вложенные элементы исходного элемента **лист** будут создаваться "с нуля".</span><span class="sxs-lookup"><span data-stu-id="dd37a-187">Otherwise, all nested elements of the original **Sheet** element will be created from scratch.</span></span> <span data-ttu-id="dd37a-188">Таким образом, все привязки повторно созданных элементов формата будут потеряны в обновленном формате ER.</span><span class="sxs-lookup"><span data-stu-id="dd37a-188">Therefore, all bindings of the re-created format elements will be lost in the updated ER format.</span></span>

![Параметр "Создать элемент формата листа Excel" в диалоговом окне Обновление из Excel](./media/er-excel-format-update-template.png)

<span data-ttu-id="dd37a-190">Чтобы получить дополнительные сведения об этой функции, выполните действия, описанные в разделе [Изменение форматов электронной отчетности путем повторного применения шаблонов Excel](modify-electronic-reporting-format-reapply-excel-template.md).</span><span class="sxs-lookup"><span data-stu-id="dd37a-190">To learn more about this feature, follow the steps in [Modify Electronic reporting formats by reapplying Excel templates](modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

## <a name="validate-an-er-format"></a><span data-ttu-id="dd37a-191">Проверяет формат ER</span><span class="sxs-lookup"><span data-stu-id="dd37a-191">Validate an ER format</span></span>

<span data-ttu-id="dd37a-192">При проверке формата ER, который может быть изменен, выполняется проверка согласованности, чтобы убедиться в том, что в используемом в данный момент шаблоне Excel присутствует имя Excel.</span><span class="sxs-lookup"><span data-stu-id="dd37a-192">When you validate an ER format that can be edited, a consistency check is done to make sure that the Excel name is present in the Excel template that is currently used.</span></span> <span data-ttu-id="dd37a-193">Будет выведено уведомление о любых несоответствиях.</span><span class="sxs-lookup"><span data-stu-id="dd37a-193">You will be notified about any inconsistencies.</span></span> <span data-ttu-id="dd37a-194">Для некоторых несоответствий будет предложено автоматическое исправление вопросов.</span><span class="sxs-lookup"><span data-stu-id="dd37a-194">For some inconsistencies, the option to automatically fix issues will be offered.</span></span>

![Сообщения об ошибка проверки](./media/er-excel-format-validate.png)


## <a name="additional-resources"></a><span data-ttu-id="dd37a-196">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dd37a-196">Additional resources</span></span>

[<span data-ttu-id="dd37a-197">Обзор электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="dd37a-197">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="dd37a-198">Разработка конфигурации для создания отчетов в формате OPENXML</span><span class="sxs-lookup"><span data-stu-id="dd37a-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks\er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="dd37a-199">Изменение форматов электронной отчетности путем повторного применения шаблонов Excel</span><span class="sxs-lookup"><span data-stu-id="dd37a-199">Modify Electronic reporting formats by reapplying Excel templates</span></span>](modify-electronic-reporting-format-reapply-excel-template.md)

[<span data-ttu-id="dd37a-200">Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel</span><span class="sxs-lookup"><span data-stu-id="dd37a-200">Use horizontally expandable ranges to dynamically add columns in Excel reports</span></span>](tasks/er-horizontal-1.md)

[<span data-ttu-id="dd37a-201">Внедрение изображений и фигур в документы, создаваемые с помощью электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="dd37a-201">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="dd37a-202">Настройка электронной отчетности (ER) для загрузки данных в Power BI</span><span class="sxs-lookup"><span data-stu-id="dd37a-202">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)