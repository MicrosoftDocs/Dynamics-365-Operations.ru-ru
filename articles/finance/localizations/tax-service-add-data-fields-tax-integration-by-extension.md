---
title: Добавление полей данных в налоговую интеграцию с помощью расширений
description: В этой теме объясняется, как использовать расширения X++ для добавления полей данных в налоговую интеграцию.
author: qire
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8e3573f9c9971d4a5af33ece08b7e0b43f2e813a
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921173"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a><span data-ttu-id="364dc-103">Добавление полей данных в налоговую интеграцию с помощью расширения</span><span class="sxs-lookup"><span data-stu-id="364dc-103">Add data fields in the tax integration by using extension</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="364dc-104">В этой теме объясняется, как использовать расширения X++ для добавления полей данных в налоговую интеграцию.</span><span class="sxs-lookup"><span data-stu-id="364dc-104">This topic explains how to use X++ extensions to add data fields in the tax integration.</span></span> <span data-ttu-id="364dc-105">Эти поля могут быть расширены до модели налоговых данных налоговой службы и использоваться для определения налоговых кодов.</span><span class="sxs-lookup"><span data-stu-id="364dc-105">These fields can be extended to the tax data model of the tax service and used to determine tax codes.</span></span> <span data-ttu-id="364dc-106">Дополнительные сведения см. в разделе [Добавление полей данных в налоговые конфигурации](tax-service-add-data-fields-tax-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="364dc-106">For more information, see [Add data fields in tax configurations](tax-service-add-data-fields-tax-configurations.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="364dc-107">Модель данных</span><span class="sxs-lookup"><span data-stu-id="364dc-107">Data model</span></span>

<span data-ttu-id="364dc-108">Данные в модели данных переносятся объектами и реализуются классами.</span><span class="sxs-lookup"><span data-stu-id="364dc-108">The data in the data model is carried by objects and implemented by classes.</span></span>

<span data-ttu-id="364dc-109">Ниже представлен список основных объектов:</span><span class="sxs-lookup"><span data-stu-id="364dc-109">Here is a list of the major objects:</span></span>

* <span data-ttu-id="364dc-110">AxClass/TaxIntegration **Document** Object</span><span class="sxs-lookup"><span data-stu-id="364dc-110">AxClass/TaxIntegration **Document** Object</span></span>
* <span data-ttu-id="364dc-111">AxClass/TaxIntegration **Line** Object</span><span class="sxs-lookup"><span data-stu-id="364dc-111">AxClass/TaxIntegration **Line** Object</span></span>
* <span data-ttu-id="364dc-112">AxClass/TaxIntegration **TaxLine** Object</span><span class="sxs-lookup"><span data-stu-id="364dc-112">AxClass/TaxIntegration **TaxLine** Object</span></span>

<span data-ttu-id="364dc-113">На следующем рисунке показано, как эти объекты связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="364dc-113">The following illustration shows how these objects are related.</span></span>

<span data-ttu-id="364dc-114">[![Связь объектов модели данных](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span><span class="sxs-lookup"><span data-stu-id="364dc-114">[![Data model object relationship](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span></span>

<span data-ttu-id="364dc-115">Объект **Документ** может содержать много объектов **Строка**.</span><span class="sxs-lookup"><span data-stu-id="364dc-115">A **Document** object can contain many **Line** objects.</span></span> <span data-ttu-id="364dc-116">Каждый объект содержит метаданные для налоговой службы.</span><span class="sxs-lookup"><span data-stu-id="364dc-116">Each object contains metadata for the tax service.</span></span>

- <span data-ttu-id="364dc-117">`TaxIntegrationDocumentObject` имеет метаданные `originAddress`, которые содержат сведения об исходном адресе и метаданные `includingTax`, которые указывают, включает ли сумма по строке налог с продаж.</span><span class="sxs-lookup"><span data-stu-id="364dc-117">`TaxIntegrationDocumentObject` has `originAddress` metadata, which contains information about the source address, and `includingTax` metadata, which indicates whether the line amount includes sales tax.</span></span>
- <span data-ttu-id="364dc-118">`TaxIntegrationLineObject` содержит метаданные `itemId`, `quantity` и `categoryId`.</span><span class="sxs-lookup"><span data-stu-id="364dc-118">`TaxIntegrationLineObject` has `itemId`, `quantity`, and `categoryId` metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="364dc-119">`TaxIntegrationLineObject` также реализует объекты **Накладные расходы**.</span><span class="sxs-lookup"><span data-stu-id="364dc-119">`TaxIntegrationLineObject` also implements **Charge** objects.</span></span>

## <a name="integration-flow"></a><span data-ttu-id="364dc-120">Поток интеграции</span><span class="sxs-lookup"><span data-stu-id="364dc-120">Integration flow</span></span>

<span data-ttu-id="364dc-121">Данные в потоке управляются действиями.</span><span class="sxs-lookup"><span data-stu-id="364dc-121">The data in the flow is manipulated by activities.</span></span>

### <a name="key-activities"></a><span data-ttu-id="364dc-122">Основные действия</span><span class="sxs-lookup"><span data-stu-id="364dc-122">Key activities</span></span>

* <span data-ttu-id="364dc-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="364dc-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span></span>
* <span data-ttu-id="364dc-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="364dc-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span></span>
* <span data-ttu-id="364dc-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="364dc-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span></span>
* <span data-ttu-id="364dc-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="364dc-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span></span>
* <span data-ttu-id="364dc-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="364dc-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span></span>

<span data-ttu-id="364dc-128">Действия выполняются в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="364dc-128">Activities are run in the following order:</span></span>

1. <span data-ttu-id="364dc-129">Извлечение параметра</span><span class="sxs-lookup"><span data-stu-id="364dc-129">Setting Retrieval</span></span>
2. <span data-ttu-id="364dc-130">Извлечение данных</span><span class="sxs-lookup"><span data-stu-id="364dc-130">Data Retrieval</span></span>
3. <span data-ttu-id="364dc-131">Служба вычислений</span><span class="sxs-lookup"><span data-stu-id="364dc-131">Calculation Service</span></span>
4. <span data-ttu-id="364dc-132">Валютный курс</span><span class="sxs-lookup"><span data-stu-id="364dc-132">Currency Exchange</span></span>
5. <span data-ttu-id="364dc-133">Сохранение данных</span><span class="sxs-lookup"><span data-stu-id="364dc-133">Data Persistence</span></span>

<span data-ttu-id="364dc-134">Например, расширьте **Получение данных** перед **Службы вычислений**.</span><span class="sxs-lookup"><span data-stu-id="364dc-134">For example, extend **Data Retrieval** before **Calculation Service**.</span></span>

#### <a name="data-retrieval-activities"></a><span data-ttu-id="364dc-135">Действия по извлечению данных</span><span class="sxs-lookup"><span data-stu-id="364dc-135">Data Retrieval activities</span></span>

<span data-ttu-id="364dc-136">Действия **Извлечение данных** извлекают данные из базы данных.</span><span class="sxs-lookup"><span data-stu-id="364dc-136">**Data Retrieval** activities retrieve data from the database.</span></span> <span data-ttu-id="364dc-137">Адаптеры для разных проводок доступны для получения данных из других таблиц проводок:</span><span class="sxs-lookup"><span data-stu-id="364dc-137">Adapters for different transactions are available to retrieve data from different transaction tables:</span></span>

- <span data-ttu-id="364dc-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="364dc-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span></span>
- <span data-ttu-id="364dc-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="364dc-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span></span>
- <span data-ttu-id="364dc-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="364dc-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span></span>
- <span data-ttu-id="364dc-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="364dc-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span></span>
- <span data-ttu-id="364dc-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="364dc-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span></span>
- <span data-ttu-id="364dc-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="364dc-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span></span>
- <span data-ttu-id="364dc-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="364dc-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span></span>

<span data-ttu-id="364dc-145">В этих действиях **Извлечение данных** данные копируются из базы данных в объекты `TaxIntegrationDocumentObject` и `TaxIntegrationLineObject`.</span><span class="sxs-lookup"><span data-stu-id="364dc-145">In these **Data Retrieval** activities, data is copied from the database to `TaxIntegrationDocumentObject` and `TaxIntegrationLineObject`.</span></span> <span data-ttu-id="364dc-146">Так как все эти действия расширяют один и тот же абстрактный класс шаблона, они имеют общие методы.</span><span class="sxs-lookup"><span data-stu-id="364dc-146">Because all these activities extend the same abstract template class, they have common methods.</span></span>

#### <a name="calculation-service-activities"></a><span data-ttu-id="364dc-147">Действия службы вычисления</span><span class="sxs-lookup"><span data-stu-id="364dc-147">Calculation Service activities</span></span>

<span data-ttu-id="364dc-148">Действие **Службы вычисления** — это связь между налоговой службой и налоговой интеграцией.</span><span class="sxs-lookup"><span data-stu-id="364dc-148">The **Calculation Service** activity is the link between the tax service and the tax integration.</span></span> <span data-ttu-id="364dc-149">Это действие отвечает за следующие функции:</span><span class="sxs-lookup"><span data-stu-id="364dc-149">This activity is responsible for the following functions:</span></span>

1. <span data-ttu-id="364dc-150">Создание запроса.</span><span class="sxs-lookup"><span data-stu-id="364dc-150">Construct the request.</span></span>
2. <span data-ttu-id="364dc-151">Отправка запроса в налоговую службу.</span><span class="sxs-lookup"><span data-stu-id="364dc-151">Post the request to the tax service.</span></span>
3. <span data-ttu-id="364dc-152">Получение ответа от налоговой службы.</span><span class="sxs-lookup"><span data-stu-id="364dc-152">Get the response from the tax service.</span></span>
4. <span data-ttu-id="364dc-153">Синтаксический анализ ответа.</span><span class="sxs-lookup"><span data-stu-id="364dc-153">Parse the response.</span></span>

<span data-ttu-id="364dc-154">Поле данных, добавленное к запросу, будет разноситься вместе с другими метаданными.</span><span class="sxs-lookup"><span data-stu-id="364dc-154">A data field that you add to the request will be posted together with other metadata.</span></span> 

## <a name="extension-implementation"></a><span data-ttu-id="364dc-155">Реализация расширения</span><span class="sxs-lookup"><span data-stu-id="364dc-155">Extension implementation</span></span>

<span data-ttu-id="364dc-156">В этом разделе представлено подробное описание действий, которые описывают, как реализовать расширение.</span><span class="sxs-lookup"><span data-stu-id="364dc-156">This section provides detailed steps that explain how to implement the extension.</span></span> <span data-ttu-id="364dc-157">В качестве примеров используются финансовые аналитики **Центр затрат** и **Проект**.</span><span class="sxs-lookup"><span data-stu-id="364dc-157">It uses the **Cost center** and **Project** financial dimensions as examples.</span></span>

### <a name="step-1-add-the-data-variable-in-the-object-class"></a><span data-ttu-id="364dc-158">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="364dc-158">Step 1.</span></span> <span data-ttu-id="364dc-159">Добавьте переменную данных в класс объекта</span><span class="sxs-lookup"><span data-stu-id="364dc-159">Add the data variable in the object class</span></span>

<span data-ttu-id="364dc-160">Класс объекта содержит переменную данных и методы получения/задания для данных.</span><span class="sxs-lookup"><span data-stu-id="364dc-160">The object class contains the data variable and getter/setter methods for the data.</span></span> <span data-ttu-id="364dc-161">Добавьте поле данных в объект `TaxIntegrationDocumentObject` или `TaxIntegrationLineObject` в зависимости от уровня поля.</span><span class="sxs-lookup"><span data-stu-id="364dc-161">Add the data field to either `TaxIntegrationDocumentObject` or `TaxIntegrationLineObject`, depending on the level of the field.</span></span> <span data-ttu-id="364dc-162">В следующем примере используется уровень строки, и имя файла — `TaxIntegrationLineObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="364dc-162">The following example uses the line level, and the file name is `TaxIntegrationLineObject_Extension.xpp`.</span></span>

> [!NOTE]
> <span data-ttu-id="364dc-163">Если добавляемое поле данных находится на уровне документа, измените имя файла на `TaxIntegrationDocumentObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="364dc-163">If the data field that you're adding is at the document level, change the file name to `TaxIntegrationDocumentObject_Extension.xpp`.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

<span data-ttu-id="364dc-164">**Центр затрат** и **Проект** добавляются как частные переменные.</span><span class="sxs-lookup"><span data-stu-id="364dc-164">**Cost center** and **Project** are added as private variables.</span></span> <span data-ttu-id="364dc-165">Создайте методы получения и задания для этих полей данных, чтобы управлять данными.</span><span class="sxs-lookup"><span data-stu-id="364dc-165">Create getter and setter methods for these data fields to manipulate the data.</span></span>

### <a name="step-2-retrieve-data-from-the-database"></a><span data-ttu-id="364dc-166">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="364dc-166">Step 2.</span></span> <span data-ttu-id="364dc-167">Извлечение данных из базы данных</span><span class="sxs-lookup"><span data-stu-id="364dc-167">Retrieve data from the database</span></span>

<span data-ttu-id="364dc-168">Укажите проводку и расширьте соответствующие классы адаптеров, чтобы извлечь данные.</span><span class="sxs-lookup"><span data-stu-id="364dc-168">Specify the transaction, and extend the appropriate adapter classes to retrieve the data.</span></span> <span data-ttu-id="364dc-169">Например, если используется проводка **Заказ на покупку**, необходимо расширить `TaxIntegrationPurchTableDataRetrieval` и `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="364dc-169">For example, if you use a **Purchase order** transaction, you must extend `TaxIntegrationPurchTableDataRetrieval` and `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span></span> 

> [!NOTE]
> <span data-ttu-id="364dc-170">`TaxIntegrationPurchParmTableDataRetrieval` наследуется от `TaxIntegrationPurchTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="364dc-170">`TaxIntegrationPurchParmTableDataRetrieval` is inherited from `TaxIntegrationPurchTableDataRetrieval`.</span></span> <span data-ttu-id="364dc-171">Он не должно изменяться, если только логика таблиц `purchTable` и `purchParmTable` не различается.</span><span class="sxs-lookup"><span data-stu-id="364dc-171">It should not be changed unless the logic of the `purchTable` and `purchParmTable` tables differs.</span></span>

<span data-ttu-id="364dc-172">Если поле данных должно быть добавлено для всех проводок, необходимо расширить все классы `DataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="364dc-172">If the data field should be added for all transactions, extend all `DataRetrieval` classes.</span></span>

<span data-ttu-id="364dc-173">Так как все действия **Извлечение данных** расширяют один и тот же класс шаблона, структуры классов, переменные и методы схожи.</span><span class="sxs-lookup"><span data-stu-id="364dc-173">Because all **Data Retrieval** activities extend the same template class, the class structures, variables, and methods are similar.</span></span>

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

<span data-ttu-id="364dc-174">В следующем примере показана основная структура при использовании таблицы `PurchTable`.</span><span class="sxs-lookup"><span data-stu-id="364dc-174">The following example shows the basic structure when the `PurchTable` table is used.</span></span>

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

<span data-ttu-id="364dc-175">При вызове метода `CopyToDocument` буфер `this.purchTable` уже существует.</span><span class="sxs-lookup"><span data-stu-id="364dc-175">When the `CopyToDocument` method is called, the `this.purchTable` buffer already exists.</span></span> <span data-ttu-id="364dc-176">Этот метод предназначен для копирования всех требуемых данных из `this.purchTable` в объект `document` с помощью метода задания, созданного в классе `DocumentObject`.</span><span class="sxs-lookup"><span data-stu-id="364dc-176">The purpose of this method is to copy all the required data from `this.purchTable` to the `document` object by using the setter method that was created in the `DocumentObject` class.</span></span>

<span data-ttu-id="364dc-177">Аналогичным образом буфер `this.purchLine` уже существует в методе `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="364dc-177">Likewise, a `this.purchLine` buffer already exists in the `CopyToLine` method.</span></span> <span data-ttu-id="364dc-178">Этот метод предназначен для копирования всех требуемых данных из `this.purchLine` в объект `_line` с помощью метода задания, созданного в классе `LineObject`.</span><span class="sxs-lookup"><span data-stu-id="364dc-178">The purpose of this method is to copy all the required data from `this.purchLine` to the `_line` object by using the setter method that was created in the `LineObject` class.</span></span>

<span data-ttu-id="364dc-179">Самый простой подход — расширить методы `CopyToDocument` и `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="364dc-179">The most straightforward approach is to extend the `CopyToDocument` and `CopyToLine` methods.</span></span> <span data-ttu-id="364dc-180">Однако рекомендуется сначала попробовать использовать методы `copyToDocumentFromHeaderTable` и `copyToLineFromLineTable`.</span><span class="sxs-lookup"><span data-stu-id="364dc-180">However, we recommend that you try the `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable` methods first.</span></span> <span data-ttu-id="364dc-181">Если они не работают должным образом, реализуйте свой метод и вызовите его в `CopyToDocument` и `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="364dc-181">If they don't work as you require, implement your own method, and call it in `CopyToDocument` and `CopyToLine`.</span></span> <span data-ttu-id="364dc-182">Существует три типичных ситуации, когда вы можете использовать такой подход:</span><span class="sxs-lookup"><span data-stu-id="364dc-182">There are three common situations where you might use this approach:</span></span>

- <span data-ttu-id="364dc-183">Требуемое поле находится в `PurchTable` или `PurchLine`.</span><span class="sxs-lookup"><span data-stu-id="364dc-183">The required field is in `PurchTable` or `PurchLine`.</span></span> <span data-ttu-id="364dc-184">В этой ситуации можно расширять `copyToDocumentFromHeaderTable` и `copyToLineFromLineTable`.</span><span class="sxs-lookup"><span data-stu-id="364dc-184">In this situation, you can extend `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable`.</span></span> <span data-ttu-id="364dc-185">Вот пример кода.</span><span class="sxs-lookup"><span data-stu-id="364dc-185">Here is the sample code.</span></span>

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- <span data-ttu-id="364dc-186">Требуемые данные отсутствуют в таблице по умолчанию проводки.</span><span class="sxs-lookup"><span data-stu-id="364dc-186">The required data isn't in the default table of the transaction.</span></span> <span data-ttu-id="364dc-187">Однако имеются некоторые связи соединения с таблицей по умолчанию, и поле в большинстве строк является обязательным.</span><span class="sxs-lookup"><span data-stu-id="364dc-187">However, there are some join relationships with the default table, and the field is required on most lines.</span></span> <span data-ttu-id="364dc-188">В этом случае необходимо заменить `getDocumentQueryObject` или `getLineObject`, чтобы запросить таблицу с помощью связи соединения.</span><span class="sxs-lookup"><span data-stu-id="364dc-188">In this situation, replace `getDocumentQueryObject` or `getLineObject` to query the table by join relationship.</span></span> <span data-ttu-id="364dc-189">В следующем примере поле **Немедленная поставка** интегрировано со заказом на продажу на уровне строки.</span><span class="sxs-lookup"><span data-stu-id="364dc-189">In the following example, the **Deliver Now** field is integrated with the sales order at the line level.</span></span>

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    <span data-ttu-id="364dc-190">В этом примере объявляется буфер `mcrSalesLineDropShipment`, а запрос определяется в `getLineQueryObject`.</span><span class="sxs-lookup"><span data-stu-id="364dc-190">In this example, a `mcrSalesLineDropShipment` buffer is declared, and the query is defined in `getLineQueryObject`.</span></span> <span data-ttu-id="364dc-191">Запрос использует отношение `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span><span class="sxs-lookup"><span data-stu-id="364dc-191">The query uses the relationship `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span></span> <span data-ttu-id="364dc-192">При расширении в этой ситуации можно заменить `getLineQueryObject` собственным созданным объектом запроса.</span><span class="sxs-lookup"><span data-stu-id="364dc-192">While you're extending in this situation, you can replace `getLineQueryObject` with your own constructed query object.</span></span> <span data-ttu-id="364dc-193">Однако обратите внимание на следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="364dc-193">However, note the following points:</span></span>

    * <span data-ttu-id="364dc-194">Так как возвращаемое значение метода `getLineQueryObject` является `SysDaQueryObject`, необходимо сконструировать этот объект, используя подход SysDa.</span><span class="sxs-lookup"><span data-stu-id="364dc-194">Because the return value of the `getLineQueryObject` method is `SysDaQueryObject`, you must construct this object by using the SysDa approach.</span></span>
    * <span data-ttu-id="364dc-195">Не удается удалить существовавшую таблицу.</span><span class="sxs-lookup"><span data-stu-id="364dc-195">Can't remove existed table.</span></span>

- <span data-ttu-id="364dc-196">Требуемые данные связаны с таблицей проводок с помощью сложного отношения соединения, либо отношение является не отношением "один к одному" (1:1), а отношением "один к нескольким" (1:N).</span><span class="sxs-lookup"><span data-stu-id="364dc-196">The required data is related to the transaction table by a complicated join relationship, or the relation isn't one to one (1:1) but one to many (1:N).</span></span> <span data-ttu-id="364dc-197">В этом случае все становится немного сложнее.</span><span class="sxs-lookup"><span data-stu-id="364dc-197">In this situation, things become a little complicated.</span></span> <span data-ttu-id="364dc-198">Эта ситуация применима к примеру финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="364dc-198">This situation applies to the example of financial dimensions.</span></span> 

    <span data-ttu-id="364dc-199">В этом случае можно реализовать собственный метод для извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="364dc-199">In this situation, you can implement your own method to retrieve the data.</span></span> <span data-ttu-id="364dc-200">Вот пример кода в файле `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="364dc-200">Here is the sample code in the `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` file.</span></span>

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a><span data-ttu-id="364dc-201">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="364dc-201">Step 3.</span></span> <span data-ttu-id="364dc-202">Добавление данных в запрос</span><span class="sxs-lookup"><span data-stu-id="364dc-202">Add data to the request</span></span>

<span data-ttu-id="364dc-203">Расширьте метод `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` или `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine`, чтобы добавить данные в запрос.</span><span class="sxs-lookup"><span data-stu-id="364dc-203">Extend the `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` or `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method to add data to the request.</span></span> <span data-ttu-id="364dc-204">Вот пример кода в файле `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="364dc-204">Here is the sample code in the `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` file.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```

<span data-ttu-id="364dc-205">В этом коде `_destination` — это объект-оболочка, который используется для создания запроса POST, и `_source` является объектом `TaxIntegrationLineObject`.</span><span class="sxs-lookup"><span data-stu-id="364dc-205">In this code, `_destination` is the wrapper object that is used to generate the post request, and `_source` is the `TaxIntegrationLineObject` object.</span></span> 

> [!NOTE]
> * <span data-ttu-id="364dc-206">Определите ключ, который используется в форме запроса как `private const str`.</span><span class="sxs-lookup"><span data-stu-id="364dc-206">Define the key that is used in the request form as `private const str`.</span></span>
> * <span data-ttu-id="364dc-207">Задайте поле в методе `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` с помощью метода `SetField`.</span><span class="sxs-lookup"><span data-stu-id="364dc-207">Set the field in the `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method by using the `SetField` method.</span></span> <span data-ttu-id="364dc-208">Второй параметр должен иметь тип данных `string`.</span><span class="sxs-lookup"><span data-stu-id="364dc-208">The data type of the second parameter should be `string`.</span></span> <span data-ttu-id="364dc-209">Если тип данных отличается от `string`, преобразуйте его в `string`.</span><span class="sxs-lookup"><span data-stu-id="364dc-209">If the data type isn't `string`, convert it to `string`.</span></span>

## <a name="appendix"></a><span data-ttu-id="364dc-210">Приложение</span><span class="sxs-lookup"><span data-stu-id="364dc-210">Appendix</span></span>

<span data-ttu-id="364dc-211">В этом приложении представлен полный пример кода для интеграции финансовых аналитик (**Центр затрат** и **Проект**) на уровне строки.</span><span class="sxs-lookup"><span data-stu-id="364dc-211">This appendix shows the complete sample code for the integration of financial dimensions (**Cost center** and **Project**) at the line level.</span></span>

### <a name="taxintegrationlineobject_extensionxpp"></a><span data-ttu-id="364dc-212">TaxIntegrationLineObject_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="364dc-212">TaxIntegrationLineObject_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a><span data-ttu-id="364dc-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="364dc-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a><span data-ttu-id="364dc-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="364dc-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
