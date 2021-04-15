---
title: Функция ER LISTOFFIELDS
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LISTOFFIELDS.
author: NickSelin
ms.date: 12/12/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f394a557beaeb558f5c7065eefe16f4aadce6ac
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743783"
---
# <a name="listoffields-er-function"></a><span data-ttu-id="9dcf9-103">Функция ER LISTOFFIELDS</span><span class="sxs-lookup"><span data-stu-id="9dcf9-103">LISTOFFIELDS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9dcf9-104">Функция `LISTOFFIELDS` возвращает значение *Список записей*, созданное на основе структуры указанного аргумента типа *Перечисление* или *Контейнер (запись)*.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="9dcf9-105">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="9dcf9-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="9dcf9-106">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="9dcf9-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="9dcf9-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="9dcf9-107">Arguments</span></span>

<span data-ttu-id="9dcf9-108">`path`: Ссылка на источник данных</span><span class="sxs-lookup"><span data-stu-id="9dcf9-108">`path`: Data source reference</span></span>

<span data-ttu-id="9dcf9-109">Действительный путь ссылки источника данных одного из следующих типов данных:</span><span class="sxs-lookup"><span data-stu-id="9dcf9-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="9dcf9-110">Перечисление модели</span><span class="sxs-lookup"><span data-stu-id="9dcf9-110">Model enumeration</span></span>
- <span data-ttu-id="9dcf9-111">Перечисление форматов</span><span class="sxs-lookup"><span data-stu-id="9dcf9-111">Format enumeration</span></span>
- <span data-ttu-id="9dcf9-112">Перечисление приложений</span><span class="sxs-lookup"><span data-stu-id="9dcf9-112">Application enumeration</span></span>
- <span data-ttu-id="9dcf9-113">Контейнер (запись)</span><span class="sxs-lookup"><span data-stu-id="9dcf9-113">Container (record)</span></span>

<span data-ttu-id="9dcf9-114">`language`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="9dcf9-114">`language`: *String*</span></span>

<span data-ttu-id="9dcf9-115">Текст, представляющий код языка.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="9dcf9-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9dcf9-116">Return values</span></span>

<span data-ttu-id="9dcf9-117">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="9dcf9-117">*Record list*</span></span>

<span data-ttu-id="9dcf9-118">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9dcf9-119">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="9dcf9-119">Usage notes</span></span>

<span data-ttu-id="9dcf9-120">Созданный список состоит из записей, которые имеют следующие поля:</span><span class="sxs-lookup"><span data-stu-id="9dcf9-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="9dcf9-121">**Имя** (тип данных *Строка*)</span><span class="sxs-lookup"><span data-stu-id="9dcf9-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="9dcf9-122">**Метка** (тип данных *Строка*)</span><span class="sxs-lookup"><span data-stu-id="9dcf9-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="9dcf9-123">**Описание** (тип данных *Строка*)</span><span class="sxs-lookup"><span data-stu-id="9dcf9-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="9dcf9-124">**IsTranslated** (тип данных *Логический*)</span><span class="sxs-lookup"><span data-stu-id="9dcf9-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="9dcf9-125">Если аргумент `path` относится к источнику данных типа *Контейнер (запись)*, для каждого поля записи контейнера, на которую есть ссылка , новая запись добавляется в созданный список.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="9dcf9-126">Для каждой созданной записи поле **Имя** возвращает имя поля записи контейнера, на которую ест ссылка, для которого была создана текущая запись.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="9dcf9-127">Если аргумент `path` относится к источнику данных одного из типов *Перечисление*, для каждого значения перечисления, для которого есть ссылка , новая запись добавляется в созданный список.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="9dcf9-128">Для каждой созданной записи поле **Имя** возвращает значение перечисления, на которое есть ссылка, для которого была создана текущая запись, поле **Описание** возвращает описание этого перечисления, а поле **Метка** возвращает метку этого перечисления.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="9dcf9-129">Во время выполнения, когда используется синтаксис 1, поля **Метка** и **Описание** должны возвращать значения, основанные на настройках языка формата электронной отчетности (ER), который используется:</span><span class="sxs-lookup"><span data-stu-id="9dcf9-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="9dcf9-130">Если доступны метки и описания для запрашиваемого языка, поля **Метка** и **Описание** возвращают значения, основанные на этом языке, и поле **IsTranslated** возвращает **True**.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="9dcf9-131">Если метки и описания для запрашиваемого языка недоступны, поля **Метка** и **Описание** возвращают значения, основанные на языке по умолчанию **EN-US**, и поле **IsTranslated** возвращает **False**.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="9dcf9-132">Во время выполнения, когда используется синтаксис 2, поля **Метка** и **Описание** должны возвращать значения, основанные на языке, который задан как второй аргумент вызываемой функции:</span><span class="sxs-lookup"><span data-stu-id="9dcf9-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="9dcf9-133">Если доступны метки и описания для запрашиваемого языка, поля **Метка** и **Описание** возвращают значения, основанные на этом языке, и поле **IsTranslated** возвращает **True**.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="9dcf9-134">Если метки и описания для запрашиваемого языка недоступны, поля **Метка** и **Описание** возвращают значения, основанные на языке **EN-US**, и поле **IsTranslated** возвращает **False**.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="9dcf9-135">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9dcf9-135">Example 1</span></span>

<span data-ttu-id="9dcf9-136">На следующем рисунке показано перечисление, введенное в модели данных ER.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="9dcf9-137">Следующая иллюстрация показывает эти детали:</span><span class="sxs-lookup"><span data-stu-id="9dcf9-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="9dcf9-138">Перечисление модели, вставленное в отчет в качестве источника данных.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="9dcf9-139">Выражение ER использует перечисление модели как параметр функции `LISTOFFIELDS`.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="9dcf9-140">Источник данных типа *Список записей* вставляется в отчет с помощью созданного выражения ER.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="9dcf9-141">В следующем примере показано элементы формата электронной отчетности, которые привязаны к источнику данных типа *Список записей*, который был создан с помощью функции `LISTOFFIELDS`.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="9dcf9-142">На следующем рисунке показан результат выполнения созданного формата.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="9dcf9-143">На основе параметров языка родительских элементов формата **FILE** и **FOLDER** переведенный текст для меток и описаний вводится в выходные данные формата электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="9dcf9-144">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9dcf9-144">Example 2</span></span>

<span data-ttu-id="9dcf9-145">Можно использовать тип источника данных *Вычисляемое поле* для настройки источников данных **enumType\_de** и **enumType\_deCH** для перечисления модели данных **enumType**.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="9dcf9-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="9dcf9-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="9dcf9-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="9dcf9-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="9dcf9-148">В этом случае можно использовать следующее выражение для получения метки значения перечисления на немецком языке (Швейцария), если этот перевод доступен.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="9dcf9-149">Если перевод со швейцарского на немецкий не поддерживается, подпись появляется на немецком языке.</span><span class="sxs-lookup"><span data-stu-id="9dcf9-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="9dcf9-150">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9dcf9-150">Additional resources</span></span>

[<span data-ttu-id="9dcf9-151">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="9dcf9-151">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]