---
title: Функция электронной отчетности Base64StringToContainer
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности Base64StringToContainer.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 612590dacc1887b87677c12eddaef42660a7a154
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561550"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="7e9d5-103">Функция электронной отчетности Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="7e9d5-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e9d5-104">[Функция](er-formula-language.md#functions) `BASE64STRINGTOCONTAINER` преобразует заданный ввод типа *Строка* в элемент данных типа *[Контейнер](er-functions-category-container.md)*.</span><span class="sxs-lookup"><span data-stu-id="7e9d5-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e9d5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e9d5-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="7e9d5-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="7e9d5-106">Arguments</span></span>

<span data-ttu-id="7e9d5-107">`input`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="7e9d5-107">`input`: *String*</span></span>

<span data-ttu-id="7e9d5-108">Действительный путь источника данных типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="7e9d5-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="7e9d5-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7e9d5-109">Return values</span></span>

<span data-ttu-id="7e9d5-110">*Тара*</span><span class="sxs-lookup"><span data-stu-id="7e9d5-110">*Container*</span></span>

<span data-ttu-id="7e9d5-111">Результирующее двоичное значение в формате больших двоичных объектов (BLOB).</span><span class="sxs-lookup"><span data-stu-id="7e9d5-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7e9d5-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="7e9d5-112">Usage notes</span></span>

<span data-ttu-id="7e9d5-113">Исключение "Недопустимый параметр" генерируется, если входная строка не предоставляет правильную группу Base64 для схем кодирования двоичного кода в текст.</span><span class="sxs-lookup"><span data-stu-id="7e9d5-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="7e9d5-114">Пример</span><span class="sxs-lookup"><span data-stu-id="7e9d5-114">Example</span></span>

<span data-ttu-id="7e9d5-115">Определите следующие источники данных в соответствии вашей модели:</span><span class="sxs-lookup"><span data-stu-id="7e9d5-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="7e9d5-116">Корневой источник данных **DocuTypeGroupEnum** типа *Dynamics 365 for Operations/перечисление*, относящийся к перечислению приложения **DocuTypeGroup**.</span><span class="sxs-lookup"><span data-stu-id="7e9d5-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="7e9d5-117">Корневой источник данных **Customer** типа *Dynamics 365 for Operations / Записи таблицы*, который ссылается на таблицу приложения **CustTable**.</span><span class="sxs-lookup"><span data-stu-id="7e9d5-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="7e9d5-118">Источник данных **\#Media** типа *Вычисляемое поле*, сконфигурированного следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7e9d5-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="7e9d5-119">Он добавляется как дочерний источник данных для источника данных **Customer**.</span><span class="sxs-lookup"><span data-stu-id="7e9d5-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="7e9d5-120">Он содержит выражение `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span><span class="sxs-lookup"><span data-stu-id="7e9d5-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="7e9d5-121">Источник данных **\#MediaAsBase64String** типа *Вычисляемое поле*, сконфигурированного следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7e9d5-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="7e9d5-122">Он добавляется как дочерний источник данных для источника данных **Customer.'\#Media'**.</span><span class="sxs-lookup"><span data-stu-id="7e9d5-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="7e9d5-123">Он содержит выражение `Customer.'#Media'.'getFileContentAsBase64String()'`.</span><span class="sxs-lookup"><span data-stu-id="7e9d5-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="7e9d5-124">Источник данных **\#BlobFomBase64** типа *Вычисляемое поле*, сконфигурированного следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7e9d5-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="7e9d5-125">Он добавляется как дочерний источник данных для источника данных **Customer.'\#Media'**.</span><span class="sxs-lookup"><span data-stu-id="7e9d5-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="7e9d5-126">Он содержит выражение `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span><span class="sxs-lookup"><span data-stu-id="7e9d5-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="7e9d5-127">В этом примере источник данных **\#MediaAsBase64String** кодирует двоичное содержимое текущего вложения мультимедиа в виде текста, представляющего группу Base64 схем кодирования двоичных значений в текст.</span><span class="sxs-lookup"><span data-stu-id="7e9d5-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="7e9d5-128">Источник данных **\#BlobFomBase64** декодирует строку Base64 и возвращает двоичное значение в формате BLOB.</span><span class="sxs-lookup"><span data-stu-id="7e9d5-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![Пример источников данных на странице конструктора сопоставления модели электронной отчетности](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="7e9d5-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7e9d5-130">Additional resources</span></span>

[<span data-ttu-id="7e9d5-131">Контейнерные функции</span><span class="sxs-lookup"><span data-stu-id="7e9d5-131">Container functions</span></span>](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]