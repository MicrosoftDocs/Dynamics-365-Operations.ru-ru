---
title: Макет маршрутизации документов для наклеек грузомест
description: В этом разделе описывается, как использовать методы форматирования для печати значений на этикетках.
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: faf54fec2885f868c66987a7b481559d0c5615d0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838282"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="95bf8-103">Макет маршрутизации документов для наклеек грузомест</span><span class="sxs-lookup"><span data-stu-id="95bf8-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="95bf8-104">Макет маршрутизации документов определяет компоновку наклеек грузомест и печатаемые на них данные.</span><span class="sxs-lookup"><span data-stu-id="95bf8-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="95bf8-105">Точки запуска печати настраиваются при настройке элементов меню и шаблонов работы мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="95bf8-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="95bf8-106">В типичном сценарии работники приемки на складе печатают этикетки для грузомест сразу после записи содержимого палет, прибывающих в область приемки.</span><span class="sxs-lookup"><span data-stu-id="95bf8-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="95bf8-107">Физические этикетки закрепляются на палетах.</span><span class="sxs-lookup"><span data-stu-id="95bf8-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="95bf8-108">Затем они могут использоваться для проверки в рамках процесса размещения, который следует, и для будущих исходящих операций комплектации.</span><span class="sxs-lookup"><span data-stu-id="95bf8-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="95bf8-109">Можно печатать очень сложные наклейки при условии, что устройство печати может интерпретировать отправляемый на него текст.</span><span class="sxs-lookup"><span data-stu-id="95bf8-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="95bf8-110">Например, макет Zebra Programming Language (ZPL), содержащий штрих-код, может выглядеть так, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="95bf8-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

<span data-ttu-id="95bf8-111">В процессе печати этикеток текст `$LicensePlateId$` в этом примере будет заменен значением данных.</span><span class="sxs-lookup"><span data-stu-id="95bf8-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="95bf8-112">Чтобы просмотреть значения, которые будут распечатаны, перейдите к пункту **Управление складом \> Запросы и отчеты \> Метки грузомест**.</span><span class="sxs-lookup"><span data-stu-id="95bf8-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="95bf8-113">Несколько широко доступных инструментов создания меток могут помочь отформатировать текст для макета метки.</span><span class="sxs-lookup"><span data-stu-id="95bf8-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="95bf8-114">Многие из этих средств поддерживают формат `$FieldName$`.</span><span class="sxs-lookup"><span data-stu-id="95bf8-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="95bf8-115">Кроме того, Microsoft Dynamics 365 Supply Chain Management использует специальную логику форматирования в качестве части сопоставления полей для макета маршрутизации документов.</span><span class="sxs-lookup"><span data-stu-id="95bf8-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="95bf8-116">Включите эту функцию для своей системы</span><span class="sxs-lookup"><span data-stu-id="95bf8-116">Turn on this feature for your system</span></span>

<span data-ttu-id="95bf8-117">Если ваша система еще не содержит функций, описанных в этом разделе, перейдите в [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) и включите функцию *Усовершенствованные макеты меток грузомест*.</span><span class="sxs-lookup"><span data-stu-id="95bf8-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Enhanced license plate label layouts* feature.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="95bf8-118">Пользовательские числовые форматы</span><span class="sxs-lookup"><span data-stu-id="95bf8-118">Custom number formats</span></span>

<span data-ttu-id="95bf8-119">Можно настроить форматирование числовых значений полей, которые печатаются с помощью кодов, имеющих следующий формат.</span><span class="sxs-lookup"><span data-stu-id="95bf8-119">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="95bf8-120">Вот объяснение этого формата:</span><span class="sxs-lookup"><span data-stu-id="95bf8-120">Here is an explanation of this format:</span></span>

- <span data-ttu-id="95bf8-121">`FieldName` — это имя поля данных (например, **Кол-во**).</span><span class="sxs-lookup"><span data-stu-id="95bf8-121">`FieldName` is the name of the data field (such as **Qty**).</span></span>
- <span data-ttu-id="95bf8-122">`FormatString` определяет, как должны печататься данные.</span><span class="sxs-lookup"><span data-stu-id="95bf8-122">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="95bf8-123">В следующих примерах показано, как можно настроить поле количества работы (**Кол-во**):</span><span class="sxs-lookup"><span data-stu-id="95bf8-123">The following examples show how you can customize the work quantity (**Qty**) field:</span></span>

- <span data-ttu-id="95bf8-124">Чтобы всегда показывать четыре цифры (с использованием нулей в качестве заполнителей), используйте `$Qty:0000$`.</span><span class="sxs-lookup"><span data-stu-id="95bf8-124">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="95bf8-125">Например, если количество равно 10, метка отобразит "0010".</span><span class="sxs-lookup"><span data-stu-id="95bf8-125">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="95bf8-126">Чтобы всегда отображалось два знака после запятой, используйте `$Qty:0.00$`.</span><span class="sxs-lookup"><span data-stu-id="95bf8-126">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="95bf8-127">Например, если количество равно 10, метка отобразит "10,00".</span><span class="sxs-lookup"><span data-stu-id="95bf8-127">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="95bf8-128">Полный список доступных строк числовых форматов см. в разделе [Настраиваемые строки числовых форматов](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="95bf8-128">For a complete list of the available number format strings, see [Custom numeric format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="95bf8-129">Пользовательские форматы строк</span><span class="sxs-lookup"><span data-stu-id="95bf8-129">Custom string formats</span></span>

<span data-ttu-id="95bf8-130">Можно удалить первые символы строки, используя следующий код поля и формата.</span><span class="sxs-lookup"><span data-stu-id="95bf8-130">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="95bf8-131">Здесь `#` указывается число пропускаемых символов.</span><span class="sxs-lookup"><span data-stu-id="95bf8-131">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="95bf8-132">Например, чтобы для номера грузоместа напечатать серийный номер контейнера отгрузки (SSCC), который не содержит первых двух знаков, используйте `$LicensePlateId:2..$`.</span><span class="sxs-lookup"><span data-stu-id="95bf8-132">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="95bf8-133">В этом случае номер грузоместа 0011111111111222221 будет напечатан как "11111111111222221".</span><span class="sxs-lookup"><span data-stu-id="95bf8-133">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="95bf8-134">Настраиваемые форматы даты и времени</span><span class="sxs-lookup"><span data-stu-id="95bf8-134">Custom date/time formats</span></span>

<span data-ttu-id="95bf8-135">В следующем примере показано, как можно управлять форматом, используемым для печати дат.</span><span class="sxs-lookup"><span data-stu-id="95bf8-135">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="95bf8-136">В этом примере дата "30 апреля 2020 года" будет распечатана как "30-04-2020".</span><span class="sxs-lookup"><span data-stu-id="95bf8-136">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="95bf8-137">Полный список доступных форматов даты и времени см. в разделе [Настраиваемые строки форматов даты и времени](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="95bf8-137">For a complete list of the available date/time formats, see [Custom date and time format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="95bf8-138">Печать отдельных строк из многострочных данных</span><span class="sxs-lookup"><span data-stu-id="95bf8-138">Print individual lines from multiline data</span></span>

<span data-ttu-id="95bf8-139">Если поле данных содержит несколько строк (то есть строк, разделенных разрывами строки), можно напечатать отдельную строку, используя следующий формат:</span><span class="sxs-lookup"><span data-stu-id="95bf8-139">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="95bf8-140">Здесь `#` представляет собой номер строки, которую необходимо напечатать.</span><span class="sxs-lookup"><span data-stu-id="95bf8-140">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="95bf8-141">(Используйте 1 для первой строки.)</span><span class="sxs-lookup"><span data-stu-id="95bf8-141">(Use 1 for the first line.)</span></span>

<span data-ttu-id="95bf8-142">Например, в системе имеется поле `AdditionalAddress`, в котором хранится следующий многострочный адрес:</span><span class="sxs-lookup"><span data-stu-id="95bf8-142">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="95bf8-143">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="95bf8-143">Contoso Inc.</span></span>  
<span data-ttu-id="95bf8-144">123 Название улицы</span><span class="sxs-lookup"><span data-stu-id="95bf8-144">123 Street Name</span></span>  
<span data-ttu-id="95bf8-145">Некоторый город, некоторый регион</span><span class="sxs-lookup"><span data-stu-id="95bf8-145">Some City, Some State</span></span>

<span data-ttu-id="95bf8-146">Можно напечатать этот адрес по одной строке за раз, используя следующие коды:</span><span class="sxs-lookup"><span data-stu-id="95bf8-146">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="95bf8-147">Код</span><span class="sxs-lookup"><span data-stu-id="95bf8-147">Code</span></span> | <span data-ttu-id="95bf8-148">Печатаемый текст</span><span class="sxs-lookup"><span data-stu-id="95bf8-148">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="95bf8-149">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="95bf8-149">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="95bf8-150">123 Название улицы</span><span class="sxs-lookup"><span data-stu-id="95bf8-150">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="95bf8-151">Некоторый город, некоторый регион</span><span class="sxs-lookup"><span data-stu-id="95bf8-151">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="95bf8-152">Печать и форматирование из метода отображения</span><span class="sxs-lookup"><span data-stu-id="95bf8-152">Print and format from a display method</span></span>

<span data-ttu-id="95bf8-153">Можно выполнить печать из метода отображения, используя следующий формат.</span><span class="sxs-lookup"><span data-stu-id="95bf8-153">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="95bf8-154">Этот формат можно комбинировать с другими типами, которые были описаны ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="95bf8-154">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="95bf8-155">Например, имеется метод отображения с именем `DisplayListOfItemsNumbers()`, и необходимо напечатать первый код номенклатуры этого метода.</span><span class="sxs-lookup"><span data-stu-id="95bf8-155">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="95bf8-156">В этом случае можно использовать следующий код.</span><span class="sxs-lookup"><span data-stu-id="95bf8-156">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="95bf8-157">Дополнительные сведения о печати меток</span><span class="sxs-lookup"><span data-stu-id="95bf8-157">More information about how to print labels</span></span>

<span data-ttu-id="95bf8-158">Дополнительные сведения о настройке и печати меток см. в разделе [Включение печати меток грузомест](tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="95bf8-158">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]