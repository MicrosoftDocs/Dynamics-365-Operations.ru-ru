---
title: Функция ER QRCODE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности QRCODE.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bac0910d213ee05a2a7a7b218a6714d4f935be16
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916760"
---
# <span data-ttu-id="96d44-103"><a name="QRCODE">Функция ER QRCODE</a></span><span class="sxs-lookup"><span data-stu-id="96d44-103"><a name="QRCODE">QRCODE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96d44-104">Функция `QRCODE` возвращает значение *Контейнер*, которое представляет изображение Quick Response (QR) для указанной строки в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="96d44-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="96d44-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96d44-105">Syntax</span></span>

```
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="96d44-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="96d44-106">Arguments</span></span>

<span data-ttu-id="96d44-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="96d44-107">`text`: *String*</span></span>

<span data-ttu-id="96d44-108">*Строковое* значение, представляющее исходный текст.</span><span class="sxs-lookup"><span data-stu-id="96d44-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="96d44-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="96d44-109">Return values</span></span>

<span data-ttu-id="96d44-110">*Тара*</span><span class="sxs-lookup"><span data-stu-id="96d44-110">*Container*</span></span>

<span data-ttu-id="96d44-111">Полученный двоичный поток.</span><span class="sxs-lookup"><span data-stu-id="96d44-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="96d44-112">Пример</span><span class="sxs-lookup"><span data-stu-id="96d44-112">Example</span></span>

<span data-ttu-id="96d44-113">Вы можете настроить формат электронной отчетности (ER) для создания исходящего документа в формате Microsoft Office (рабочие книги Excel или документы Word) с помощью предварительно заданного шаблона.</span><span class="sxs-lookup"><span data-stu-id="96d44-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="96d44-114">Этот шаблон может содержать объект **Изображение** (книга Excel) или **Элемент управления изображения** (документ Word) в качестве заполнителя для изображения кода QR.</span><span class="sxs-lookup"><span data-stu-id="96d44-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="96d44-115">Необходимо добавить в настроенный формат ER элемент **Ячейка**, который будет использоваться для заполнения этого заполнителя.</span><span class="sxs-lookup"><span data-stu-id="96d44-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="96d44-116">Чтобы указать, какая информация будет храниться в коде QR, необходимо определить привязку для этого элемента **Ячейка**.</span><span class="sxs-lookup"><span data-stu-id="96d44-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="96d44-117">Например, можно настроить такую привязку как содержащую следующие выражения:</span><span class="sxs-lookup"><span data-stu-id="96d44-117">For example, you can configure such binding as containing the following expression:</span></span>

```
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="96d44-118">При запуске настроенного формата ER текстовое значение поля **LabelText** источника данных **model.ListOfShelfLabels** будет использовано для создания изображения кода QR.</span><span class="sxs-lookup"><span data-stu-id="96d44-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="96d44-119">Это изображение заменит заполнитель изображения кода QR в шаблоне документа, используемого для создания исходящего документа.</span><span class="sxs-lookup"><span data-stu-id="96d44-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="96d44-120">Когда это изображение созданного документа сканируется, оно возвращает текст, взятый из поля **LabelText** источника данных **model.ListOfShelfLabels**.</span><span class="sxs-lookup"><span data-stu-id="96d44-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="96d44-121">Дополнительные сведения см. в разделе [Внедрение изображений и фигур в документы, создаваемые с помощью электронной отчетности](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="96d44-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96d44-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="96d44-122">Additional resources</span></span>

[<span data-ttu-id="96d44-123">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="96d44-123">Text functions</span></span>](er-functions-category-text.md)
