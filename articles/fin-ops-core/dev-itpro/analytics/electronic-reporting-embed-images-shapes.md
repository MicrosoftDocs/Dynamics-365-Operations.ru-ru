---
title: Внедрение изображений и фигур в документы, создаваемые с помощью электронной отчетности
description: В этой статье объясняется, как использовать средство "Электронная отчетность" для создания бизнес-документов, содержащих внедренные изображения и фигуры.
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.custom: 27621
ms.assetid: ''
ms.search.form: EROperationDesigner, ERParameters
ms.openlocfilehash: 0bb652f245db93424aeadcaadf2ad393945e616b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280999"
---
# <a name="embed-images-and-shapes-in-documents-that-you-generate-by-using-er"></a>Внедрение изображений и фигур в документы, создаваемые с помощью электронной отчетности

[!include [banner](../includes/banner.md)]

Можно использовать средство электронной отчетности (ER) для создания отчетов, которые можно выполнить, чтобы создать необходимые электронные документы. Можно использовать документы Microsoft Excel или Microsoft Word, чтобы указать макет отчета. С помощью конструктора операций ER можно привязать документ Excel или Word в качестве шаблона для отчета. Именованные элементы в связанном шаблоне связаны с элементами формата отчета ER. Элементы формата отчета связаны с источниками данных. Эти элементы данных определяют данные, которые будут введены в генерируемые документы во время выполнения.

Эта новая функция выходит за пределы существующих возможностей ER при создании документов в форматах Microsoft Office. Для получения дополнительных сведений воспроизведите следующие руководства по задачам. Эти руководства по задачам можно найти в 7.5.4.3 Приобретение/разработка компонентов ИТ-услуг и решений (10677).

- Электронная отчетность — Разработка конфигурации для создания отчетов в формате OPENXML
- Разработка конфигурации ER для создания отчетов в формате Microsoft Word

## <a name="embed-an-image-in-an-excel-document"></a>Внедрение изображения в документ Excel

### <a name="embed-an-image-in-an-excel-worksheet"></a>Внедрение изображения в таблица Excel

Сначала необходимо добавить заполнитель для изображения в документ Excel. Откройте книгу Excel и добавьте рисунок в качестве заполнителя для изображения, которое будет добавлено позже. Затем воспользуйтесь средством ER, чтобы добавить новую конфигурацию формата ER, чтобы включить создаваемый отчет. Приложите книгу Excel в качестве шаблона к формату отчета, а затем импортируйте содержимое книги в формат ER. Определение формата будет создано автоматически. Добавленный заполнитель изображения будет включен в определение формата ER как элемент **ЯЧЕЙКА**.

> [!NOTE]
> Можно указать определение формата вручную, а не импортировать его. При сохранении изменений формат будет проверен.

Затем свяжите элемент **ЯЧЕЙКА** формата ER с полем источника данных формата, который предоставляет данные изображения в двоичном формате во время выполнения. Когда модель данных ER используется в качестве источника данных в формате, тип данных поля должен быть [контейнер](er-formula-supported-data-types-composite.md#container). В настоящее время поле модели данных ER с типом данных [Контейнер](er-formula-supported-data-types-composite.md#container) может быть привязано к нескольким типам источников данных, которые возвращают изображения в двоичном формате. Для доступа к полю в таблице данных и файле, присоединенного к записи таблицы данных, используется структура управления документами.

> [!IMPORTANT]
> - Если необходимо заполнить заполнитель изображения в документе, создаваемом с помощью шаблона Excel, формат ER должен содержать элемент **ЯЧЕЙКА**, который ссылается на именованный элемент рисунка в шаблоне Excel. В противном случае в выходных данных отчета не появится заполнитель изображения. Если привязка элемента **ЯЧЕЙКА** не возвращает данные во время выполнения, создаваемый документ будет показывать заполнитель изображения из шаблона. Чтобы скрыть изображение в создаваемом документе, определите элемент **ЯЧЕЙКА** и укажите, что выражение **Включение** должно возвращать значение **FALSE**.
> - В шаблоне Excel используйте уникальное имя для каждого элемента. Эти элементы включают рисунки и ячейки. Если дублируется имя элемента, создаваемое вами содержание отчета будет неоднозначным и запутанным.

### <a name="embed-images-in-the-header-and-footer-of-an-excel-worksheet"></a>Внедрение изображений в верхние и нижние колонтитулы листа Excel

Используйте документ книги Excel в качестве шаблона, чтобы указать выходную форму отчета. Книга может содержать несколько листов, каждая из которых может быть спроектирована так, чтобы иметь заголовок и нижний колонтитул. Excel поддерживает до трех изображений в верхнем и нижнем колонтитулах каждого листа. Изображения могут быть выровнены по левому краю, по правому или по центру.

В выпуске Finance 10.0.21 можно управлять изображениями верхних и нижних колонтитулов, которые создаются решением ER с шаблоном Excel.

Если требуется, чтобы изображение по умолчанию отображалось в верхнем или нижнем колонтитуле созданного документа, можно добавить изображение в верхний или нижний колонтитул листа шаблона ER. Чтобы получить доступ к этому изображению в формате ER, необходимо добавить компонент **Рисунок** в компонент [верхнего](er-fillable-excel.md#header-component) или [нижнего](er-fillable-excel.md#footer-component) колонтитула формата. Настройте выравнивание для компонента **Рисунок**, если это необходимо. 

Можно также использовать компонент **Рисунок** для помещения изображения в верхний или нижний колонтитул созданного документа во время выполнения, даже если шаблон не содержит изображения по умолчанию. Чтобы указать мультимедийное содержимое, которое должно быть помещено в верхний или нижний колонтитул созданного документа в качестве нового изображения или замены изображения по умолчанию, необходимо связать компонент **Рисунок** с источником данных типа [Контейнер](er-formula-supported-data-types-composite.md#container), представляющего изображение в двоичном формате.

Каждый компонент **верхнего** или **нижнего** колонтитула может содержать один компонент **Рисунок** для каждого поддерживаемого выравнивания: **По левому краю**, **По центру** и **По правому краю**.

Свойство **Масштабировать** компонента **Рисунок** позволяет использовать сконфигурированную привязку для управления размером изображения:

- Выберите **Оригинал**, чтобы сохранить исходный размер изображения.
- Выберите **Относительный** для масштабирования высоты изображения пропорционально высоте верхнего или нижнего колонтитула, содержащего это изображение.

    - В этом случае высота изображения должна быть определена как процент от исходного верхнего или нижнего колонтитула.
    - Если значение масштабирования превышает 100 процентов, изображение может перекрывать область данных соответствующего листа.
    - Если высота изображения изменяется при применении масштабирования, ширина также изменяется, чтобы сохранить исходные пропорции изображения.

- Выберите **Абсолютный**, чтобы изменить размер изображения в соответствии со значениями высоты и ширины (в пикселях), предоставляемыми во время разработки.

    - Если указанная высота превышает высоту родительского верхнего или нижнего колонтитула, изображение может перекрывать область данных соответствующего листа.

Можно также использовать свойство **Включено** компонента **Рисунок** для управления видимостью изображения, помещаемого в созданный документ с помощью данного компонента.

> [!NOTE]
> Чтобы добавить компонент **Рисунок** в редактируемый формат ER, необходимо использовать конструктор формата ER. Невозможно добавить компонент, если вы используете рабочую область [Управление бизнес-документами](er-business-document-management.md) для редактирования шаблона бизнес-документа.

Для получения дополнительных сведений об этих функциях выполните действия, описанные в разделе [Создание формата ER для создания отчета в формате Excel с внедренными изображениями в нижних или верхних колонтитулах](er-embed-images-header-footer-excel-reports.md).

## <a name="embed-a-shape-in-an-excel-document"></a>Внедрение фигуры в документ Excel

Сначала необходимо добавить заполнитель для фигуры в документ Excel. Откройте книгу Excel и выберите **Фигура**, **Текстовое поле** или **WordArt** в качестве заполнителя для фигуры. Затем воспользуйтесь средством ER, чтобы добавить новую конфигурацию формата ER, чтобы включить создаваемый отчет. Приложите книгу Excel в качестве шаблона к формату отчета, а затем импортируйте содержимое книги в формат ER. Определение формата будет создано автоматически. Добавленный заполнитель фигуры будет включен в определение формата ER как элемент **ЯЧЕЙКА**, относящийся к именованному элементу фигуры Excel.

> [!NOTE]
> Можно указать определение формата вручную, а не импортировать его. При сохранении изменений формат будет проверен.

Затем свяжите элемент **ЯЧЕЙКА** формата ER с полем источника данных формата, который предоставляет данные во время выполнения. Эти данные могут быть преобразованы в текстовую строку. Если элемент **ЯЧЕЙКА** в формате ER ссылается на элемент фигуры в шаблоне Excel, поддерживающем текст, то текст, предоставляемый в этой привязке во время выполнения, будет показан в фигуре создаваемого документа.

> [!IMPORTANT]
> - Если требуется использовать шаблон Excel, который содержит заполнитель фигуры для создания нового документа, формат ER должен содержать элемент **ЯЧЕЙКА**, относящийся к элементу фигуры Excel. В противном случае в выходных данных отчета не появится заполнитель фигуры. Если привязка элемента **ЯЧЕЙКА**, относящегося к именованному элементу фигуры Excel, не возвращает данные во время выполнения, создаваемый документ будет показывать текст заполнителя фигуры из шаблона Excel. Чтобы скрыть фигуру в создаваемом документе, определите элемент **ЯЧЕЙКА**, который ссылается на именованный элемент фигуры Excel, и укажите, что выражение **Включение** должно возвращать значение **FALSE**.
> - В шаблоне Excel используйте уникальное имя для каждого элемента. Эти элементы включают фигуры и ячейки. Если дублируется имя элемента, создаваемое вами содержание отчета будет неоднозначным и запутанным.

## <a name="embed-an-image-in-a-word-document"></a>Внедрение изображения в документ Word
> [!IMPORTANT]
> Можно повторно использовать формат ER, который использует шаблон Excel для создания документов, содержащих внедренные изображения. В формате ER убедитесь, что для элемента **ЯЧЕЙКА**, относящегося к именованному элементу рисунка в Excel, задано имя, которое связано с источником данных, который возвращает изображение во время выполнения.

Сначала необходимо настроить макет документа Word. Используйте элемент управления **Содержимое рисунка**, чтобы создать заполнитель для внедренного изображения. Чтобы получить доступ к этому элементу управления, необходимо сначала открыть вкладку **Разработчик** на ленте Word.

Затем удалите шаблон Excel из формата ER и вложите документ шаблона Word. Обновите ссылку на шаблон и сохраните изменения. Структура текущего формата ER сохраняется в шаблоне Word в качестве новой пользовательской XML-части с именем **Отчет**.

Затем сохраните шаблон Word для текущего формата ER на локальном компьютере. Откройте шаблон и откройте область **Сопоставление XML**. Найдите пользовательскую XML-часть с именем **Отчет**, а затем наведите указатель на элемент **ЯЧЕЙКА** в отчете ER, который связан с источником данных, который возвращает изображение в двоичном формате. Сопоставьте элемент XML-части с выбранным элементом управления **Содержимое рисунка** и сохраните изменения.

[![Внедрите изображения.](./media/embed-images-shapes-01.png)](./media/embed-images-shapes-01.png)

Наконец, удалите шаблон Word из формата ER и вложите документ Word, содержащий сопоставленные пользовательские XML-части. Обновите ссылку формата на шаблон и сохраните изменения, внесенные в данный формат ER.

## <a name="more-information"></a>Дополнительные сведения
Чтобы ознакомиться с подробными сведениями о данной функции, воспроизведите набор руководств по задачам, **Создание отчетов ER в форматах MS Office с внедренными изображениями**. Эти руководства показывают, как можно внедрить изображения логотипа компании и подпись уполномоченного лица в платежные документы, созданные с помощью средства ER в документах Excel и Word.

В следующей таблице перечислены файлы, необходимые для выполнения руководств по задачам **Электронная отчетность — Создание отчетов в форматах MS Office с внедренными изображениями**. Загрузите и сохраните файлы на локальном компьютере.

| описание                                          | Имя файла                   |
|------------------------------------------------------|-----------------------------|
| Конфигурации модели данных электронной отчетности                          | [Model for cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| Конфигурация формата электронной отчетности                              | [Cheques printing format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Изображение логотипа компании                                   | [Company logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Изображение подписи                                      | [Signature image.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Альтернативное изображение подписи                          | [Signature image 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Шаблон Microsoft Word для печати чеков платежей  | [Cheque template Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |
| Шаблон Microsoft Excel для печати чеков платежей | [Cheque template.xlsx](https://download.microsoft.com/download/1/f/6/1f671963-73aa-48d5-ae69-45f21fe7dfb4/Cheque%20template.xlsx)        |

На следующем рисунке представлен пример распечатки чека для проверки платежа, созданной из шаблона Excel.

[![Тестовая распечатка чека по оплате](./media/embed-images-shapes-02.png)](./media/embed-images-shapes-02.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
