---
title: "Разбиение созданных файлов XML по их размеру и количеству содержимого"
description: "В этой теме представлена информация о разбиении созданных файлов на основе размера файла и количества этого товара."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 8c3899d5c6602b3afe13b447b40f0b4dcc701448
ms.contentlocale: ru-ru
ms.lasthandoff: 08/13/2018

---

# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a><span data-ttu-id="07b1e-103">Разбиение созданных файлов XML по их размеру и количеству содержимого</span><span class="sxs-lookup"><span data-stu-id="07b1e-103">Split generated XML files based on file size and content quantity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="07b1e-104">Можно разработать форматы электронной отчетности (ER) для создания исходящих документов в формате XML.</span><span class="sxs-lookup"><span data-stu-id="07b1e-104">You can design Electronic reporting (ER) formats to generate outgoing documents in XML format.</span></span> <span data-ttu-id="07b1e-105">В некоторых случаях эти документы могут быть приняты только в том случае, если они соответствуют определенным критериям, например максимальный размер файла или максимальное число некоторых узлов XML.</span><span class="sxs-lookup"><span data-stu-id="07b1e-105">Sometimes, those documents can be accepted only when they meet specific criteria, such a maximum file size or a maximum number of some XML nodes.</span></span> <span data-ttu-id="07b1e-106">Можно разработать форматы ER для создания электронных документов, которые удовлетворяют требованиям, которые указывают получатели этих документов.</span><span class="sxs-lookup"><span data-stu-id="07b1e-106">You can design ER formats to generate electronic documents that satisfy the requirements that the recipients of those documents specify.</span></span>

- <span data-ttu-id="07b1e-107">Для элемента формата файла можно определить ограничение на размер файла как выражение ER.</span><span class="sxs-lookup"><span data-stu-id="07b1e-107">For the FILE format element, you can define a limit on the file size as an ER expression.</span></span> <span data-ttu-id="07b1e-108">При превышении определенного предела и создании отчета ER, ER завершает создание текущего файла и затем переходит к созданию следующего файла.</span><span class="sxs-lookup"><span data-stu-id="07b1e-108">If the defined limit is exceeded when an ER report is generated, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="07b1e-109">Для любого формата элемента XML можно определить ограничение количество элементов как выражение ER.</span><span class="sxs-lookup"><span data-stu-id="07b1e-109">For any XML ELEMENT format, you can define a limit on the number of elements as an ER expression.</span></span> <span data-ttu-id="07b1e-110">Если количество узлов XML в генерируемом файле превышает заданный предел при выполнении отчета ER, ER завершает создание текущего файла и затем переходит к созданию следующего файла.</span><span class="sxs-lookup"><span data-stu-id="07b1e-110">If the number of XML nodes in the file that is generated exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="07b1e-111">Для любого последовательного элемента формата XML можно определить ограничение по количеству формата элементов как выражение ER.</span><span class="sxs-lookup"><span data-stu-id="07b1e-111">For any XML SEQUENCE format element, you can define a limit on the number of child elements as an ER expression.</span></span> <span data-ttu-id="07b1e-112">Если количество формата узлов XML элемента формата в генерируемом файле превышает заданный предел при выполнении отчета ER, ER завершает создание текущего файла и затем переходит к созданию следующего файла.</span><span class="sxs-lookup"><span data-stu-id="07b1e-112">If the number of nested XML nodes of the format element in the generated file exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="07b1e-113">Можно пометить любой элемент формата XML как не прерываемый.</span><span class="sxs-lookup"><span data-stu-id="07b1e-113">You can mark any XML ELEMENT format element as non-breakable.</span></span> <span data-ttu-id="07b1e-114">Таким образом можно хранить вложенные элементы узлов XML, которые создаются под одним элементом формата в созданном файле.</span><span class="sxs-lookup"><span data-stu-id="07b1e-114">In this way, you can keep the nested items of XML nodes that are generated under the format element in a single generated file.</span></span>

<span data-ttu-id="07b1e-115">В дополнение к использованию XML-элемента и последовательных элементов формата XML для добавления узлов XML к созданному файлу, можно использовать элемент формата исходного XML.</span><span class="sxs-lookup"><span data-stu-id="07b1e-115">In addition to using the XML ELEMENT and XML SEQUENCE format elements to add XML nodes to the generated file, you can use the RAW XML format element.</span></span> <span data-ttu-id="07b1e-116">Тем не менее узлы, которые можно добавить с помощью элемента формата исходного XML, не учитываются при расчете количества узлов для оценки ограничений на число элементов.</span><span class="sxs-lookup"><span data-stu-id="07b1e-116">However, nodes that you add by using the RAW XML format element aren't considered when the number of nodes is calculated to evaluate the limits on the number of elements.</span></span>

<span data-ttu-id="07b1e-117">Если вы сконфигурировали места назначения файла для элемента формата файла, который был конфигурирован для разбиения созданных выходных данных при превышении заданного ограничения, каждая часть созданных выходных данных отправляется в место назначения конфигурированного файла в качестве отдельного файла.</span><span class="sxs-lookup"><span data-stu-id="07b1e-117">If you configured file destinations for a FILE format element that has been configured to split the generated output whenever specific limits are exceeded, each piece of generated output is sent to the configured file destination as an individual file.</span></span> <span data-ttu-id="07b1e-118">Чтобы уникальным образом назвать файлы, которые должны быть созданы путем разбиения выходных данных, необходимо конфигурировать выражение ER для элемента формата файла.</span><span class="sxs-lookup"><span data-stu-id="07b1e-118">To uniquely name the files that are created by splitting the output, you must configure an ER expression for the FILE format element.</span></span> <span data-ttu-id="07b1e-119">При включении источника данных ER типа НОМЕРНАЯ СЕРИЯ, номерная серия будет расти для каждой части разбитых выходных данных.</span><span class="sxs-lookup"><span data-stu-id="07b1e-119">If you include an ER data source of the NUMBER SEQUENCE type, the number sequence will be incremented for each piece of the split output.</span></span>

<span data-ttu-id="07b1e-120">Для получения дополнительных сведений об этой функции воспроизведите проводник по задаче **файлы ER Split XML на основе размера файла или количества элементов содержания**, который является частью бизнес-процесса **7.5.4.3 компонентов ИТ-службы/решения приобретения/разработки (10677)** и может быть загружено из [Центра загрузки Майкрософт](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="07b1e-120">To learn more about this feature, play the **ER Split XML files based on the file size or content item quantity** task guide, which is part of the **7.5.4.3 Acquire/Develop IT service/solution components (10677)** business process and can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="07b1e-121">Этот проводник по задаче описывает процесс настройки формата ER для разбиения созданных файлов в зависимости от ограничений на размер файла и количество элемент содержимого.</span><span class="sxs-lookup"><span data-stu-id="07b1e-121">This task guide walks you through the process of configuring an ER format to split generated files based on limits on the file size and content item quantity.</span></span> <span data-ttu-id="07b1e-122">Загрузите следующие файлы для завершения проводника по задаче:</span><span class="sxs-lookup"><span data-stu-id="07b1e-122">To complete the task guide, you must download the following files:</span></span>

- [<span data-ttu-id="07b1e-123">Конфигурация модели ER — XmlFilesSplittingModel.xml</span><span class="sxs-lookup"><span data-stu-id="07b1e-123">ER model configuration - XmlFilesSplittingModel.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)
- [<span data-ttu-id="07b1e-124">Конфигурация формата ER — XmlFilesSplittingFormat.xml</span><span class="sxs-lookup"><span data-stu-id="07b1e-124">ER format configuration - XmlFilesSplittingFormat.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a><span data-ttu-id="07b1e-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="07b1e-125">Additional resources</span></span>
[<span data-ttu-id="07b1e-126">Места назначения электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="07b1e-126">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)

[<span data-ttu-id="07b1e-127">Конструктор формул в электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="07b1e-127">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

