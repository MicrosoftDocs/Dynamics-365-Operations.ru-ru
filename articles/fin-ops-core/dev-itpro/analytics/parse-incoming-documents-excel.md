---
title: Разбор входящих документов в формате Excel
description: В этом теме приводятся сведения о разработке форматов электронной отчетности (ER) для разбора содержимого входящих файлов Microsoft Excel.
author: NickSelin
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 0c41a062d817307adb2889d3678764f1ea4066e2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755188"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="10d71-103">Разбор входящих документов в формате Excel</span><span class="sxs-lookup"><span data-stu-id="10d71-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="10d71-104">Можно разработать форматы электронной отчетности (ER) для разбора входящих файлы Microsoft Excel, представляющих данные в книгах Microsoft Excel (файлы в формате XLSX).</span><span class="sxs-lookup"><span data-stu-id="10d71-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="10d71-105">Затем можно использовать содержимое из этих файлов для обновления данных приложения.</span><span class="sxs-lookup"><span data-stu-id="10d71-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="10d71-106">Это полезно, если вы:</span><span class="sxs-lookup"><span data-stu-id="10d71-106">This is useful if you:</span></span>

- <span data-ttu-id="10d71-107">Создаете новую модель и формат и хотите проверить их во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="10d71-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="10d71-108">В этом случае Excel будет моделировать реальные данные приложения.</span><span class="sxs-lookup"><span data-stu-id="10d71-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="10d71-109">Управляете данными за пределами приложения в Excel и хотите импортировать эти данные для отправки конкретного отчета.</span><span class="sxs-lookup"><span data-stu-id="10d71-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="10d71-110">Для получения дополнительных сведений о данной функции, выполните проводник по задаче **Импортировать данные ER из файла Microsoft Excel (часть 1: формат разработки)** и **Импортировать данные ER из файла Microsoft Excel (часть 2: Импорт данных)** (части бизнес-процесса 7.5.4.3 Приобретение/разработка компонентов ИТ-услуг и решений (10677)).</span><span class="sxs-lookup"><span data-stu-id="10d71-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="10d71-111">Эти проводники по задаче описывают, как входящий файл Excel можно проанализировать с помощью формата ER для импорта информации из входящих документов и обновления данных приложения.</span><span class="sxs-lookup"><span data-stu-id="10d71-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="10d71-112">Файлы проводника по задаче можно загрузить из [центра загрузки Майкрософт](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="10d71-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="10d71-113">Загрузите следующие файлы для завершения проводников по задаче.</span><span class="sxs-lookup"><span data-stu-id="10d71-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="10d71-114">Описание содержания</span><span class="sxs-lookup"><span data-stu-id="10d71-114">Content description</span></span>                         | <span data-ttu-id="10d71-115">Хранилище файлов</span><span class="sxs-lookup"><span data-stu-id="10d71-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="10d71-116">Входящий файл в формате XLSX - шаблон</span><span class="sxs-lookup"><span data-stu-id="10d71-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="10d71-117">1099import template.xlsx</span><span class="sxs-lookup"><span data-stu-id="10d71-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="10d71-118">Входящий файл в формате .XLSX - образец данных</span><span class="sxs-lookup"><span data-stu-id="10d71-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="10d71-119">1099import data.xlsx</span><span class="sxs-lookup"><span data-stu-id="10d71-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="10d71-120">Если вы еще не выполняли следующий проводник по задаче, [ER создать конфигурации, необходимые для импорта данных из внешнего файла](./tasks/er-required-configurations-import-data.md) в текущем приложении Finance and Operations, загрузите следующий файл.</span><span class="sxs-lookup"><span data-stu-id="10d71-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Finance and Operations application, download the following file.</span></span>

| <span data-ttu-id="10d71-121">Описание содержания</span><span class="sxs-lookup"><span data-stu-id="10d71-121">Content description</span></span>    | <span data-ttu-id="10d71-122">Хранилище файлов</span><span class="sxs-lookup"><span data-stu-id="10d71-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="10d71-123">Конфигурация модели ER</span><span class="sxs-lookup"><span data-stu-id="10d71-123">ER model configuration</span></span> | [<span data-ttu-id="10d71-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="10d71-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]