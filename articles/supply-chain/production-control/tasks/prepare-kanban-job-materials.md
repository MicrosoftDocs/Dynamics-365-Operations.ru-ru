---
title: Подготовка обработки заданий канбана при наличии материалов для производственной ячейки
description: В этой задаче особое внимание обращается на подготовку задания канбана обработки, когда для производственной ячейки имеются все материалы.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 460d55a8c4b8a8401db7abc43721cf0d114c27c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807832"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="d7be4-103">Подготовка обработки заданий канбана при наличии материалов для производственной ячейки</span><span class="sxs-lookup"><span data-stu-id="d7be4-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7be4-104">В этой задаче особое внимание обращается на подготовку задания канбана обработки, когда для производственной ячейки имеются все материалы.</span><span class="sxs-lookup"><span data-stu-id="d7be4-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="d7be4-105">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="d7be4-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="d7be4-106">Эта задача предназначена для оператора.</span><span class="sxs-lookup"><span data-stu-id="d7be4-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="d7be4-107">Перейдите на доску канбана для заданий обработки.</span><span class="sxs-lookup"><span data-stu-id="d7be4-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="d7be4-108">В поле "Производственная ячейка" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="d7be4-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d7be4-109">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d7be4-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d7be4-110">Выберите производственную ячейку 1250 и нажмите "ОК".</span><span class="sxs-lookup"><span data-stu-id="d7be4-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="d7be4-111">В списке выберите строку 4.</span><span class="sxs-lookup"><span data-stu-id="d7be4-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="d7be4-112">В чистой демонстрационной компании канбан 000329 в строке 4 — это первое задание, которое еще не завершено.</span><span class="sxs-lookup"><span data-stu-id="d7be4-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="d7be4-113">Переключите развертывание раздела "Отгрузочная накладная".</span><span class="sxs-lookup"><span data-stu-id="d7be4-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="d7be4-114">Убедитесь, что статус поставки для всех номенклатур в листе комплектации — "доступно".</span><span class="sxs-lookup"><span data-stu-id="d7be4-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="d7be4-115">Если выбрано несколько заданий, в листе комплектации отображается сумма всех номенклатур, необходимых для выбранных заданий.</span><span class="sxs-lookup"><span data-stu-id="d7be4-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="d7be4-116">Щелкните "Подготовить".</span><span class="sxs-lookup"><span data-stu-id="d7be4-116">Click Prepare.</span></span>
    * <span data-ttu-id="d7be4-117">Процесс подготовки завершен.</span><span class="sxs-lookup"><span data-stu-id="d7be4-117">The preparation process is now completed.</span></span> <span data-ttu-id="d7be4-118">Установленный флажок для всех строк в листе комплектации указывает, что статус поставки — "скомплектовано".</span><span class="sxs-lookup"><span data-stu-id="d7be4-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]