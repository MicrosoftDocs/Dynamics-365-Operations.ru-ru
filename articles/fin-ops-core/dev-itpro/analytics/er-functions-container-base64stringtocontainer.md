---
title: Функция электронной отчетности Base64StringToContainer
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности Base64StringToContainer.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0e92ae41a3e0f03cb14d4791ab768f096f2a0523
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739107"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="8c4c4-103">Функция электронной отчетности Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="8c4c4-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c4c4-104">[Функция](er-formula-language.md#functions) `BASE64STRINGTOCONTAINER` преобразует заданный ввод типа *Строка* в элемент данных типа *[Контейнер](er-functions-category-container.md)*.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c4c4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c4c4-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="8c4c4-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="8c4c4-106">Arguments</span></span>

<span data-ttu-id="8c4c4-107">`input`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="8c4c4-107">`input`: *String*</span></span>

<span data-ttu-id="8c4c4-108">Действительный путь источника данных типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="8c4c4-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8c4c4-109">Return values</span></span>

<span data-ttu-id="8c4c4-110">*Тара*</span><span class="sxs-lookup"><span data-stu-id="8c4c4-110">*Container*</span></span>

<span data-ttu-id="8c4c4-111">Результирующее двоичное значение в формате больших двоичных объектов (BLOB).</span><span class="sxs-lookup"><span data-stu-id="8c4c4-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8c4c4-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="8c4c4-112">Usage notes</span></span>

<span data-ttu-id="8c4c4-113">Исключение "Недопустимый параметр" генерируется, если входная строка не предоставляет правильную группу Base64 для схем кодирования двоичного кода в текст.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="8c4c4-114">Пример</span><span class="sxs-lookup"><span data-stu-id="8c4c4-114">Example</span></span>

<span data-ttu-id="8c4c4-115">Определите следующие источники данных в соответствии вашей модели:</span><span class="sxs-lookup"><span data-stu-id="8c4c4-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="8c4c4-116">Корневой источник данных **DocuTypeGroupEnum** типа *Dynamics 365 for Operations/перечисление*, относящийся к перечислению приложения **DocuTypeGroup**.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="8c4c4-117">Корневой источник данных **Customer** типа *Dynamics 365 for Operations / Записи таблицы*, который ссылается на таблицу приложения **CustTable**.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="8c4c4-118">Источник данных **\#Media** типа *Вычисляемое поле*, сконфигурированного следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8c4c4-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="8c4c4-119">Он добавляется как дочерний источник данных для источника данных **Customer**.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="8c4c4-120">Он содержит выражение `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="8c4c4-121">Источник данных **\#MediaAsBase64String** типа *Вычисляемое поле*, сконфигурированного следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8c4c4-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="8c4c4-122">Он добавляется как дочерний источник данных для источника данных **Customer.'\#Media'**.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="8c4c4-123">Он содержит выражение `Customer.'#Media'.'getFileContentAsBase64String()'`.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="8c4c4-124">Источник данных **\#BlobFomBase64** типа *Вычисляемое поле*, сконфигурированного следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8c4c4-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="8c4c4-125">Он добавляется как дочерний источник данных для источника данных **Customer.'\#Media'**.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="8c4c4-126">Он содержит выражение `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="8c4c4-127">В этом примере источник данных **\#MediaAsBase64String** кодирует двоичное содержимое текущего вложения мультимедиа в виде текста, представляющего группу Base64 схем кодирования двоичных значений в текст.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="8c4c4-128">Источник данных **\#BlobFomBase64** декодирует строку Base64 и возвращает двоичное значение в формате BLOB.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![Пример источников данных на странице конструктора сопоставления модели электронной отчетности](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="8c4c4-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8c4c4-130">Additional resources</span></span>

[<span data-ttu-id="8c4c4-131">Контейнерные функции</span><span class="sxs-lookup"><span data-stu-id="8c4c4-131">Container functions</span></span>](er-functions-category-container.md)
