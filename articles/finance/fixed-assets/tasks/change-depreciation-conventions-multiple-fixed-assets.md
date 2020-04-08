---
title: Изменение соглашений по амортизации для нескольких основных средств
description: В результате этой задачи будет обновлено соглашение по амортизации для указанной группы основных средств.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39930134782b40de05a92a6ad51c4f628f304a78
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142900"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="c53f9-103">Изменение соглашений по амортизации для нескольких основных средств</span><span class="sxs-lookup"><span data-stu-id="c53f9-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c53f9-104">В результате этой задачи будет обновлено соглашение по амортизации для указанной группы основных средств.</span><span class="sxs-lookup"><span data-stu-id="c53f9-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="c53f9-105">В данном руководстве по задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="c53f9-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="c53f9-106">Перейдите в раздел "Основные средства" > "Периодические задачи" > "Массовое обновление"</span><span class="sxs-lookup"><span data-stu-id="c53f9-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="c53f9-107">В поле "Журнал амортизации" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c53f9-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c53f9-108">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c53f9-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c53f9-109">В поле "Начало размещения на обслуживание" введите дату.</span><span class="sxs-lookup"><span data-stu-id="c53f9-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="c53f9-110">В поле "Завершение размещения на обслуживание" введите дату.</span><span class="sxs-lookup"><span data-stu-id="c53f9-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="c53f9-111">Будут обновлены только основные средства, являющиеся частью выбранного журнала амортизации и помещенные на сервис между этими датами.</span><span class="sxs-lookup"><span data-stu-id="c53f9-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="c53f9-112">В поле "Текущее соглашение по амортизации" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="c53f9-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="c53f9-113">Будут обновлены только основные средства, которые имеют текущее соглашение по амортизации.</span><span class="sxs-lookup"><span data-stu-id="c53f9-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="c53f9-114">В поле "Новое соглашение по амортизации" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="c53f9-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="c53f9-115">Убедитесь, что отчет будет распечатан в нужном месте.</span><span class="sxs-lookup"><span data-stu-id="c53f9-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="c53f9-116">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="c53f9-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="c53f9-117">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="c53f9-117">Click Filter.</span></span>
10. <span data-ttu-id="c53f9-118">В списке выберите группу ОС.</span><span class="sxs-lookup"><span data-stu-id="c53f9-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="c53f9-119">В поле "Критерии" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c53f9-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="c53f9-120">Выберите требуемую группу ОС.</span><span class="sxs-lookup"><span data-stu-id="c53f9-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="c53f9-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c53f9-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="c53f9-122">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c53f9-122">Click OK.</span></span>
15. <span data-ttu-id="c53f9-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c53f9-123">Click OK.</span></span>
    *  <span data-ttu-id="c53f9-124">Результаты процесса отображаются в отчете "Массовое обновление".</span><span class="sxs-lookup"><span data-stu-id="c53f9-124">Results of the process are shown on the Mass update report.</span></span>     

