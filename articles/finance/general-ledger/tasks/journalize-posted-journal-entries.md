---
title: Учет учтенных записей журнала в субкниге
description: Эта процедура описывает, как выполнить журнализацию разнесенных записей в журнале.
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f50ee568df492bcd811d2fefb1784bb55b50384b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145060"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="4d859-103">Учет учтенных записей журнала в субкниге</span><span class="sxs-lookup"><span data-stu-id="4d859-103">Journalize posted journal entries</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d859-104">Эта процедура описывает, как выполнить журнализацию разнесенных записей в журнале.</span><span class="sxs-lookup"><span data-stu-id="4d859-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="4d859-105">В этой процедуре используется компания с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="4d859-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="4d859-106">В области **Область переходов** выберите **Модули > Главная книга > Настройка главной книги > Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="4d859-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="4d859-107">В поле **Расширенный журнал ГК** можно задать значение "Да" или "Нет".</span><span class="sxs-lookup"><span data-stu-id="4d859-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="4d859-108">Если "Да", выходные данные отчета будут другими.</span><span class="sxs-lookup"><span data-stu-id="4d859-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="4d859-109">Выберите, можно ли закрыть период, если процесс журнализации не был запущен.</span><span class="sxs-lookup"><span data-stu-id="4d859-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="4d859-110">Если для этого параметра задано значение "Да", период нельзя закрыть до тех пор, пока не будет завершен процесс журнализации за этот период.</span><span class="sxs-lookup"><span data-stu-id="4d859-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="4d859-111">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4d859-111">Close the page.</span></span>
5. <span data-ttu-id="4d859-112">В **области переходов** выберите **Модули > Главная книга > Периодические задачи > Журнализация**.</span><span class="sxs-lookup"><span data-stu-id="4d859-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="4d859-113">Щелкните **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="4d859-113">Click **Filter**.</span></span>
7. <span data-ttu-id="4d859-114">Выделите строку с критериями фильтра, которые вы хотите указать.</span><span class="sxs-lookup"><span data-stu-id="4d859-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="4d859-115">В поле **Критерии** введите или выберите критерий фильтра.</span><span class="sxs-lookup"><span data-stu-id="4d859-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="4d859-116">Чтобы закрыть страницу фильтра, нажмите кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d859-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="4d859-117">Щелкните **ОК**, чтобы начать процесс журнализации.</span><span class="sxs-lookup"><span data-stu-id="4d859-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="4d859-118">Отчет будет создан после завершения процесса.</span><span class="sxs-lookup"><span data-stu-id="4d859-118">A report will be generated after the process is complete.</span></span>  

