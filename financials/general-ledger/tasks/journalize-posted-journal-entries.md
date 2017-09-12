--- 
title: "Учет учтенных записей журнала в субкниге"
description: "Эта процедура описывает, как выполнить журнализацию разнесенных записей в журнале."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 490e9a4beda43f6e32b87792b11153c3e8e322d6
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="60568-103">Учет учтенных записей журнала в субкниге</span><span class="sxs-lookup"><span data-stu-id="60568-103">Journalize posted journal entries</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60568-104">Эта процедура описывает, как выполнить журнализацию разнесенных записей в журнале.</span><span class="sxs-lookup"><span data-stu-id="60568-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="60568-105">В этой процедуре используется компания с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="60568-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="60568-106">Проверьте настройки для журнализации в пункте "Главная книга" > "Настройка главной книги" > "Параметры главной книги".</span><span class="sxs-lookup"><span data-stu-id="60568-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="60568-107">В поле "Расширенный журнал ГК" можно задать значение "Да" или "Нет".</span><span class="sxs-lookup"><span data-stu-id="60568-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="60568-108">Если "Да", выходные данные отчета будут другими.</span><span class="sxs-lookup"><span data-stu-id="60568-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="60568-109">Выберите, можно ли закрыть период, если процесс журнализации не был запущен.</span><span class="sxs-lookup"><span data-stu-id="60568-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="60568-110">Если для этого параметра задано значение "Да", период нельзя закрыть до тех пор, пока не будет завершен процесс журнализации за этот период.</span><span class="sxs-lookup"><span data-stu-id="60568-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="60568-111">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="60568-111">Close the page.</span></span>
5. <span data-ttu-id="60568-112">Перейдите в раздел "Главная книга" > "Периодические задачи" > "Журнализация".</span><span class="sxs-lookup"><span data-stu-id="60568-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="60568-113">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="60568-113">Click Filter.</span></span>
7. <span data-ttu-id="60568-114">Выделите строку с критериями фильтра, которые вы хотите указать.</span><span class="sxs-lookup"><span data-stu-id="60568-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="60568-115">В поле "Критерии" введите или выберите критерий фильтра.</span><span class="sxs-lookup"><span data-stu-id="60568-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="60568-116">Чтобы закрыть страницу фильтра, нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="60568-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="60568-117">Щелкните ОК, чтобы начать процесс журнализации.</span><span class="sxs-lookup"><span data-stu-id="60568-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="60568-118">Отчет будет создан после завершения процесса.</span><span class="sxs-lookup"><span data-stu-id="60568-118">A report will be generated after the process is complete.</span></span>  


