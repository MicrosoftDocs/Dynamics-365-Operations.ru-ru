---
title: Добавление полей данных в налоговую интеграцию с помощью расширений
description: В этой теме объясняется, как использовать расширения X++ для добавления полей данных в налоговую интеграцию.
author: qire
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a3da8e1b8176eb25fe4e0a320aa3e907c06e09c5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021400"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>Добавление полей данных в налоговую интеграцию с помощью расширения

[!include [banner](../includes/banner.md)]


В этой теме объясняется, как использовать расширения X++ для добавления полей данных в налоговую интеграцию. Эти поля могут быть расширены до модели налоговых данных налоговой службы и использоваться для определения налоговых кодов. Дополнительные сведения см. в разделе [Добавление полей данных в налоговые конфигурации](tax-service-add-data-fields-tax-configurations.md).

## <a name="data-model"></a>Модель данных

Данные в модели данных переносятся объектами и реализуются классами.

Ниже представлен список основных объектов:

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

На следующем рисунке показано, как эти объекты связаны друг с другом.

[![Связь объектов модели данных](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

Объект **Документ** может содержать много объектов **Строка**. Каждый объект содержит метаданные для налоговой службы.

- `TaxIntegrationDocumentObject` имеет метаданные `originAddress`, которые содержат сведения об исходном адресе и метаданные `includingTax`, которые указывают, включает ли сумма по строке налог с продаж.
- `TaxIntegrationLineObject` содержит метаданные `itemId`, `quantity` и `categoryId`.

> [!NOTE]
> `TaxIntegrationLineObject` также реализует объекты **Накладные расходы**.

## <a name="integration-flow"></a>Поток интеграции

Данные в потоке управляются действиями.

### <a name="key-activities"></a>Основные действия

* AxClass/TaxIntegration **Calculation** ActivityOnDocument
* AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument
* AxClass/TaxIntegration **DataPersistence** ActivityOnDocument
* AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument
* AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument

Действия выполняются в следующем порядке:

1. Извлечение параметра
2. Извлечение данных
3. Служба вычислений
4. Валютный курс
5. Сохранение данных

Например, расширьте **Получение данных** перед **Службы вычислений**.

#### <a name="data-retrieval-activities"></a>Действия по извлечению данных

Действия **Извлечение данных** извлекают данные из базы данных. Адаптеры для разных проводок доступны для получения данных из других таблиц проводок:

- AxClass/TaxIntegration **PurchTable** DataRetrieval
- AxClass/TaxIntegration **PurchParmTable** DataRetrieval
- AxClass/TaxIntegration **PurchREQTable** DataRetrieval
- AxClass/TaxIntegration **PurchRFQTable** DataRetrieval
- AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval
- AxClass/TaxIntegration **SalesTable** DataRetrieval
- AxClass/TaxIntegration **SalesParm** DataRetrieval

В этих действиях **Извлечение данных** данные копируются из базы данных в объекты `TaxIntegrationDocumentObject` и `TaxIntegrationLineObject`. Так как все эти действия расширяют один и тот же абстрактный класс шаблона, они имеют общие методы.

#### <a name="calculation-service-activities"></a>Действия службы вычисления

Действие **Службы вычисления** — это связь между налоговой службой и налоговой интеграцией. Это действие отвечает за следующие функции:

1. Создание запроса.
2. Отправка запроса в налоговую службу.
3. Получение ответа от налоговой службы.
4. Синтаксический анализ ответа.

Поле данных, добавленное к запросу, будет разноситься вместе с другими метаданными. 

## <a name="extension-implementation"></a>Реализация расширения

В этом разделе представлено подробное описание действий, которые описывают, как реализовать расширение. В качестве примеров используются финансовые аналитики **Центр затрат** и **Проект**.

### <a name="step-1-add-the-data-variable-in-the-object-class"></a>Шаг 1. Добавьте переменную данных в класс объекта

Класс объекта содержит переменную данных и методы получения/задания для данных. Добавьте поле данных в объект `TaxIntegrationDocumentObject` или `TaxIntegrationLineObject` в зависимости от уровня поля. В следующем примере используется уровень строки, и имя файла — `TaxIntegrationLineObject_Extension.xpp`.

> [!NOTE]
> Если добавляемое поле данных находится на уровне документа, измените имя файла на `TaxIntegrationDocumentObject_Extension.xpp`.

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

**Центр затрат** и **Проект** добавляются как частные переменные. Создайте методы получения и задания для этих полей данных, чтобы управлять данными.

### <a name="step-2-retrieve-data-from-the-database"></a>Шаг 2. Извлечение данных из базы данных

Укажите проводку и расширьте соответствующие классы адаптеров, чтобы извлечь данные. Например, если используется проводка **Заказ на покупку**, необходимо расширить `TaxIntegrationPurchTableDataRetrieval` и `TaxIntegrationVendInvoiceInfoTableDataRetrieval`. 

> [!NOTE]
> `TaxIntegrationPurchParmTableDataRetrieval` наследуется от `TaxIntegrationPurchTableDataRetrieval`. Он не должно изменяться, если только логика таблиц `purchTable` и `purchParmTable` не различается.

Если поле данных должно быть добавлено для всех проводок, необходимо расширить все классы `DataRetrieval`.

Так как все действия **Извлечение данных** расширяют один и тот же класс шаблона, структуры классов, переменные и методы схожи.

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

В следующем примере показана основная структура при использовании таблицы `PurchTable`.

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

При вызове метода `CopyToDocument` буфер `this.purchTable` уже существует. Этот метод предназначен для копирования всех требуемых данных из `this.purchTable` в объект `document` с помощью метода задания, созданного в классе `DocumentObject`.

Аналогичным образом буфер `this.purchLine` уже существует в методе `CopyToLine`. Этот метод предназначен для копирования всех требуемых данных из `this.purchLine` в объект `_line` с помощью метода задания, созданного в классе `LineObject`.

Самый простой подход — расширить методы `CopyToDocument` и `CopyToLine`. Однако рекомендуется сначала попробовать использовать методы `copyToDocumentFromHeaderTable` и `copyToLineFromLineTable`. Если они не работают должным образом, реализуйте свой метод и вызовите его в `CopyToDocument` и `CopyToLine`. Существует три типичных ситуации, когда вы можете использовать такой подход:

- Требуемое поле находится в `PurchTable` или `PurchLine`. В этой ситуации можно расширять `copyToDocumentFromHeaderTable` и `copyToLineFromLineTable`. Вот пример кода.

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

- Требуемые данные отсутствуют в таблице по умолчанию проводки. Однако имеются некоторые связи соединения с таблицей по умолчанию, и поле в большинстве строк является обязательным. В этом случае необходимо заменить `getDocumentQueryObject` или `getLineObject`, чтобы запросить таблицу с помощью связи соединения. В следующем примере поле **Немедленная поставка** интегрировано со заказом на продажу на уровне строки.

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

    В этом примере объявляется буфер `mcrSalesLineDropShipment`, а запрос определяется в `getLineQueryObject`. Запрос использует отношение `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`. При расширении в этой ситуации можно заменить `getLineQueryObject` собственным созданным объектом запроса. Однако обратите внимание на следующие моменты:

    * Так как возвращаемое значение метода `getLineQueryObject` является `SysDaQueryObject`, необходимо сконструировать этот объект, используя подход SysDa.
    * Не удается удалить существовавшую таблицу.

- Требуемые данные связаны с таблицей проводок с помощью сложного отношения соединения, либо отношение является не отношением "один к одному" (1:1), а отношением "один к нескольким" (1:N). В этом случае все становится немного сложнее. Эта ситуация применима к примеру финансовых аналитик. 

    В этом случае можно реализовать собственный метод для извлечения данных. Вот пример кода в файле `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`.

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

### <a name="step-3-add-data-to-the-request"></a>Шаг 3. Добавление данных в запрос

Расширьте метод `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` или `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine`, чтобы добавить данные в запрос. Вот пример кода в файле `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`.

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

В этом коде `_destination` — это объект-оболочка, который используется для создания запроса POST, и `_source` является объектом `TaxIntegrationLineObject`. 

> [!NOTE]
> * Определите ключ, который используется в форме запроса как `private const str`.
> * Задайте поле в методе `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` с помощью метода `SetField`. Второй параметр должен иметь тип данных `string`. Если тип данных отличается от `string`, преобразуйте его в `string`.

## <a name="appendix"></a>Приложение

В этом приложении представлен полный пример кода для интеграции финансовых аналитик (**Центр затрат** и **Проект**) на уровне строки.

### <a name="taxintegrationlineobject_extensionxpp"></a>TaxIntegrationLineObject_Extension.xpp

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

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a>TaxIntegrationPurchTableDataRetrieval_Extension.xpp

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

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a>TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp

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
