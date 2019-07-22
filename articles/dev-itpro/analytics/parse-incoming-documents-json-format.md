---
title: Разбор входящих документов в формате JSON
description: В этом разделе описан порядок настройки формата электронной отчетности (ER) для разбора входящих документов в формате JavaScript Object Notation (JSON).
author: kfend
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 92ef83bc1783b00a4d7d9739ca1c17e863c7ff44
ms.sourcegitcommit: f6581bab16225a027f4fbfad25fdef45bd286489
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703929"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="85d51-103">Разбор входящих документов в формате JSON</span><span class="sxs-lookup"><span data-stu-id="85d51-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="85d51-104">Форматы электронной отчетности можно разрабатывать для разбора входящих электронных документов, представляющих данные в текстовом формате, основанном на JavaScript (иными словами, файлы в формате JavaScript Object Notation \[JSON\]).</span><span class="sxs-lookup"><span data-stu-id="85d51-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="85d51-105">Чтобы получить дополнительные сведения об этой функции, загрузите файлы в приведенной ниже таблице, а затем запустите руководство по задаче "Электронная отчетность — Создание конфигурации формата для импорта данных из внешнего файла JSON".</span><span class="sxs-lookup"><span data-stu-id="85d51-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="85d51-106">В этом руководстве по задаче показано, как можно использовать формат ER для разбора входящего файла JSON с целью обновления данных приложения.</span><span class="sxs-lookup"><span data-stu-id="85d51-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="85d51-107">Название должности</span><span class="sxs-lookup"><span data-stu-id="85d51-107">Title</span></span>                                  | <span data-ttu-id="85d51-108">Имя файла</span><span class="sxs-lookup"><span data-stu-id="85d51-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="85d51-109">Конфигурация формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="85d51-109">ER format configuration</span></span>                | [<span data-ttu-id="85d51-110">Формат для импорта trans_JSON.xml поставщиков</span><span class="sxs-lookup"><span data-stu-id="85d51-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="85d51-111">Пример входящего файла в формате .CSV</span><span class="sxs-lookup"><span data-stu-id="85d51-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="85d51-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="85d51-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="85d51-113">Требования</span><span class="sxs-lookup"><span data-stu-id="85d51-113">Requirements</span></span>

<span data-ttu-id="85d51-114">Перед завершением руководства по задаче "Электронная отчетность — Создание конфигурации формата для импорта данных из внешнего файла JSON" необходимо выполнить следующие требования:</span><span class="sxs-lookup"><span data-stu-id="85d51-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="85d51-115">Родительскими элементами в JSON-файле могут быть только элементы объектов.</span><span class="sxs-lookup"><span data-stu-id="85d51-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="85d51-116">Вложенные элементы для объекта должны быть элементами свойств, чтобы была создана допустимая структура JSON.</span><span class="sxs-lookup"><span data-stu-id="85d51-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="85d51-117">Массивы JSON могут быть только вложенными элементами элементов свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="85d51-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="85d51-118">Массивы JSON могут содержать только объекты JSON.</span><span class="sxs-lookup"><span data-stu-id="85d51-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="85d51-119">Они не могут содержать прямые строковые/числовые значения и вложенные массивы.</span><span class="sxs-lookup"><span data-stu-id="85d51-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="85d51-120">Элементы в этих массивах будут анализироваться в порядке, в котором они указаны в формате.</span><span class="sxs-lookup"><span data-stu-id="85d51-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="85d51-121">Будут учитываться настройки кратности для каждого объекта JSON.</span><span class="sxs-lookup"><span data-stu-id="85d51-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="85d51-122">Кроме того, необходимо выполнить руководство по задаче [ER Создание необходимых конфигураций для импорта данных из внешнего файла для электронной отчетности](tasks/er-required-configurations-import-data.md), если оно еще не было выполнено.</span><span class="sxs-lookup"><span data-stu-id="85d51-122">Additionally, you must complete the [ER Create required configurations to import data from an external file for electronic reporting](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="85d51-123">Загрузите следующий файл для завершения проводника по задаче.</span><span class="sxs-lookup"><span data-stu-id="85d51-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="85d51-124">Название должности</span><span class="sxs-lookup"><span data-stu-id="85d51-124">Title</span></span>                  | <span data-ttu-id="85d51-125">Имя файла</span><span class="sxs-lookup"><span data-stu-id="85d51-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="85d51-126">Конфигурация модели ER</span><span class="sxs-lookup"><span data-stu-id="85d51-126">ER model configuration</span></span> | [<span data-ttu-id="85d51-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="85d51-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
