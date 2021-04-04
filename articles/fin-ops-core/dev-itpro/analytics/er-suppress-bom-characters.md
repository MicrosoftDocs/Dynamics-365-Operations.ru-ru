---
title: Разработка конфигураций электронной отчетности для подавления символов метки порядка байтов в созданных файлах
description: В этой теме объясняется, как настроить формат электронной отчетности (ER) для создания отчетов, в которых подавляются символы метки порядка байтов (BOM).
author: NickSelin
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9260db2edab75c9876ddf5af99bee4ff174c64e1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568981"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a><span data-ttu-id="f44c7-103">Разработка конфигураций электронной отчетности для подавления символов метки порядка байтов в созданных файлах</span><span class="sxs-lookup"><span data-stu-id="f44c7-103">Design ER configurations to suppress BOM characters in generated files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f44c7-104">Можно разработать [решение](er-quick-start1-new-solution.md) [электронной отчетности (ER)](general-electronic-reporting.md) для создания исходящих документов.</span><span class="sxs-lookup"><span data-stu-id="f44c7-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md) to generate outgoing documents.</span></span> <span data-ttu-id="f44c7-105">Для создания документов в виде текстовых файлов или XML-файлов решение должно содержать [конфигурацию](general-electronic-reporting.md#Configuration) электронной отчетности, которая содержит компонент [формата](general-electronic-reporting.md#FormatComponentOutbound) электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="f44c7-105">To generate the documents as text or XML files, the solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="f44c7-106">Чтобы задать [кодировку символов](https://docs.microsoft.com/windows/win32/intl/character-sets), представляющую набор символов в создаваемых файлах, формат электронной отчетности должен содержать элемент формата **Common\\File**.</span><span class="sxs-lookup"><span data-stu-id="f44c7-106">To specify the [character encoding](https://docs.microsoft.com/windows/win32/intl/character-sets) that represents the set of characters in generated files, the ER format must contain the **Common\\File** format element.</span></span> <span data-ttu-id="f44c7-107">Чтобы настроить компонент формата электронной отчетности, откройте [черновую](general-electronic-reporting.md#component-versioning) версию конфигурации электронной отчетности в конструкторе форматов электронной отчетности и добавьте элемент **Common\\File**.</span><span class="sxs-lookup"><span data-stu-id="f44c7-107">To configure the ER format component, open the [draft](general-electronic-reporting.md#component-versioning) version of the ER configuration in the ER format designer, and add the **Common\\File** element.</span></span> <span data-ttu-id="f44c7-108">В поле **Кодировка** укажите кодировку исходящих файлов, которая генерируется во время выполнения с помощью данного компонента.</span><span class="sxs-lookup"><span data-stu-id="f44c7-108">In the **Encoding** field, specify the encoding of outbound files that are generated at runtime by using this component.</span></span>

> [!NOTE]
> <span data-ttu-id="f44c7-109">Если формат содержит недопустимое имя кодировки, при сохранении изменений в настройках формата создается ошибка.</span><span class="sxs-lookup"><span data-stu-id="f44c7-109">If the format contains an incorrect encoding name, an error is thrown when you save your changes to the format's settings.</span></span>

![Добавление корневого элемента на странице конструктора форматов](./media/er-suppress-bom-characters-image1.gif)

<span data-ttu-id="f44c7-111">Если в качестве кодировки указать **UTF-8**, **UTF-16** или **UTF-32**, параметр **Подавления символов метки порядка байтов** становится доступным.</span><span class="sxs-lookup"><span data-stu-id="f44c7-111">If you specify **UTF-8**, **UTF-16**, or **UTF-32** as the encoding, the **Suppress BOM characters** option becomes available.</span></span> <span data-ttu-id="f44c7-112">Установите для этого параметра значение **Да**, чтобы подавить [символы меток порядка байтов (BOM)](https://docs.microsoft.com/globalization/encoding/byte-order-mark) в исходящих файлах, которые генерируются во время выполнения, когда выполняется редактируемый формат электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="f44c7-112">Set this option to **Yes** to suppress [byte order mark (BOM) characters](https://docs.microsoft.com/globalization/encoding/byte-order-mark) in outbound files that are generated at runtime when the editable ER format is run.</span></span>

> [!NOTE]
> <span data-ttu-id="f44c7-113">Если поле **Кодировка** остается пустым, по умолчанию используется кодировка **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="f44c7-113">If you leave the **Encoding** field blank, the default **UTF-8** encoding is used.</span></span>

![Установка параметра подавления символов метки порядка байтов на странице конструктора форматов](./media/er-suppress-bom-characters-image2.gif)

<span data-ttu-id="f44c7-115">Чтобы просмотреть функциональность во время выполнения, выполните соответствующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="f44c7-115">To review the functionality at runtime, complete the appropriate procedure.</span></span> <span data-ttu-id="f44c7-116">Например, выполните шаги из темы [Отложенное выполнение элементов XML в форматах электронной отчетности](er-defer-xml-element.md).</span><span class="sxs-lookup"><span data-stu-id="f44c7-116">For example, complete the steps in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic.</span></span> <span data-ttu-id="f44c7-117">После выполнения шагов, описанных из раздела [Измените формат так, чтобы расчет основывался на созданных выходных данных](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) этой темы, выполните следующие дополнительные действия.</span><span class="sxs-lookup"><span data-stu-id="f44c7-117">After you've completed the steps in the [Modify the format so that the calculation is based on generated output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) section of that topic, follow these additional steps.</span></span>

1. <span data-ttu-id="f44c7-118">Укажите кодировку UTF:</span><span class="sxs-lookup"><span data-stu-id="f44c7-118">Specify the UTF encoding:</span></span>

    1. <span data-ttu-id="f44c7-119">Выберите элемент **Отчет** типа **Common\\File**.</span><span class="sxs-lookup"><span data-stu-id="f44c7-119">Select the **Report** element of the **Common\\File** type.</span></span>
    2. <span data-ttu-id="f44c7-120">В поле **Кодировка** укажите кодировку **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="f44c7-120">In the **Encoding** field, specify the **UTF-8** encoding.</span></span>

2. <span data-ttu-id="f44c7-121">Создайте файл XML, содержащий символ метки порядка байтов:</span><span class="sxs-lookup"><span data-stu-id="f44c7-121">Generate an XML file that includes a BOM character:</span></span>

    1. <span data-ttu-id="f44c7-122">Установите для параметра **Подавления символов метки порядка байтов** значение **Нет**, чтобы включать символы меток порядка байтов (BOM) в создаваемые файлы XML.</span><span class="sxs-lookup"><span data-stu-id="f44c7-122">Set the **Suppress BOM characters** option to **No** to include BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="f44c7-123">Выполните шаги в разделе [Отсрочка выполнения элемента XML сводки для использования рассчитанного итогового значения](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) темы [Отложенное выполнение элементов XML в форматах электронной отчетности](er-defer-xml-element.md) и сохраните созданный файл XML под именем **SampleXmlReport.xml**.</span><span class="sxs-lookup"><span data-stu-id="f44c7-123">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport.xml**.</span></span>

3. <span data-ttu-id="f44c7-124">Создайте файл XML, не содержащий символ метки порядка байтов:</span><span class="sxs-lookup"><span data-stu-id="f44c7-124">Generate an XML file that doesn't include a BOM character:</span></span>

    1. <span data-ttu-id="f44c7-125">Установите для параметра **Подавления символов метки порядка байтов** значение **Да**, чтобы подавить символы меток порядка байтов (BOM) в создаваемых файлах XML.</span><span class="sxs-lookup"><span data-stu-id="f44c7-125">Set the **Suppress BOM characters** option to **Yes** to suppress BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="f44c7-126">Выполните шаги в разделе [Отсрочка выполнения элемента XML сводки для использования рассчитанного итогового значения](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) темы [Отложенное выполнение элементов XML в форматах электронной отчетности](er-defer-xml-element.md) и сохраните созданный файл XML под именем **SampleXmlReport (1).xml**.</span><span class="sxs-lookup"><span data-stu-id="f44c7-126">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport (1).xml**.</span></span>

4. <span data-ttu-id="f44c7-127">В средстве сравнения файлов сравните созданные файлы.</span><span class="sxs-lookup"><span data-stu-id="f44c7-127">In a file comparison utility, compare the generated files.</span></span>

    <span data-ttu-id="f44c7-128">Первое различие, которое вы увидите, находится в заголовке файла.</span><span class="sxs-lookup"><span data-stu-id="f44c7-128">The first difference that you will notice is in the file header.</span></span> <span data-ttu-id="f44c7-129">Файл Самплексмлрепорт. XML содержит символ метки порядка байтов (BOM), а файл SampleXmlReport (1).xml — не содержит.</span><span class="sxs-lookup"><span data-stu-id="f44c7-129">The SampleXmlReport.xml file contains a BOM character, where the SampleXmlReport (1).xml file doesn't.</span></span>

    ![Сравнение созданных файлов с помощью средства сравнения файлов](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a><span data-ttu-id="f44c7-131">См. также</span><span class="sxs-lookup"><span data-stu-id="f44c7-131">See also</span></span>

- [<span data-ttu-id="f44c7-132">Отложенное выполнение элементов XML в форматах электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="f44c7-132">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]