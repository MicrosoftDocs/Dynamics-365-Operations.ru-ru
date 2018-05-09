---
title: "Изменение формата электронной отчетности путем повторного применения шаблона Microsoft Excel"
description: "В этом разделе приведены сведения о том, как можно изменить формат электронной отчетности (ER), который используется для создания бизнес-документов, путем повторного применения измененного шаблона Excel."
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7df2c6e86975a35cd97fabad4d96fb1319d2b6ce
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="modify-an-electronic-reporting-format-by-reapplying-a-microsoft-excel-template"></a><span data-ttu-id="417fe-103">Изменение формата электронной отчетности путем повторного применения шаблона Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="417fe-103">Modify an Electronic reporting format by reapplying a Microsoft Excel template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="417fe-104">Средство электронной отчетности (ER) используется для создания бизнес-документов в электронной форме.</span><span class="sxs-lookup"><span data-stu-id="417fe-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="417fe-105">Для создания бизнес-документа необходимо создать формат ER, а затем с помощью конструктора ER определить макет бизнес-документа и указать данные, которые должны быть включены в него.</span><span class="sxs-lookup"><span data-stu-id="417fe-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="417fe-106">Затем можно выполнять формат ER для создания бизнес-документа.</span><span class="sxs-lookup"><span data-stu-id="417fe-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="417fe-107">Средство ER может использоваться для создания бизнес-документов в виде файлов Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="417fe-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="417fe-108">Можно использовать документ Excel в качестве шаблона для этих документов.</span><span class="sxs-lookup"><span data-stu-id="417fe-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="417fe-109">Чтобы определить макет документа в конструкторе ER, можно импортировать содержимое документа Excel, который требуется использовать в качестве шаблона, в определенный формат электронной отчетности ER.</span><span class="sxs-lookup"><span data-stu-id="417fe-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="417fe-110">Чтобы получить дополнительные сведения и попробовать этот сценарий на практике, воспроизведите руководство по задаче **Электронная отчетность. Создание конфигурации отчетов в формате OPENXML** (входит в состав бизнес-процесса 7.5.4.3 Приобретение/разработка компонентов ИТ-услуг и решений (10677)).</span><span class="sxs-lookup"><span data-stu-id="417fe-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="417fe-111">Если документ Excel, используемый в качестве шаблона для бизнес-документа, был отредактирован, новая функциональная возможность электронной отчетности позволяет заново применить обновленный шаблон к формату ER.</span><span class="sxs-lookup"><span data-stu-id="417fe-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="417fe-112">Формат ER затем обновляется таким образом, чтобы он соответствовал обновленному шаблону.</span><span class="sxs-lookup"><span data-stu-id="417fe-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="417fe-113">Для получения дополнительных сведений об этой функциональной возможности воспроизведите руководство по задаче **Электронная отчетность. Изменение формата путем повторного применения шаблона Excel** (входит в состав бизнес-процесса 7.5.5.3 Приобретение/разработка компонентов ИТ-услуг и решений (10683)).</span><span class="sxs-lookup"><span data-stu-id="417fe-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="417fe-114">В шаге руководства по задаче, в котором производится импорт обновленного шаблона, используйте измененный шаблон файла Excel "Отчет о платежах" SampleVendPaymWsReport2 в качестве шаблона.</span><span class="sxs-lookup"><span data-stu-id="417fe-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>

