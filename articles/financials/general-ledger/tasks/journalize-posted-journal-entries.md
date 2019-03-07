---
title: Учет учтенных записей журнала в субкниге
description: Эта процедура описывает, как выполнить журнализацию разнесенных записей в журнале.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b50809cf9eb59475856f91d9f1ddfe28ecfd8de6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "318542"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="6017a-103">Учет учтенных записей журнала в субкниге</span><span class="sxs-lookup"><span data-stu-id="6017a-103">Journalize posted journal entries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6017a-104">Эта процедура описывает, как выполнить журнализацию разнесенных записей в журнале.</span><span class="sxs-lookup"><span data-stu-id="6017a-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="6017a-105">В этой процедуре используется компания с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="6017a-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="6017a-106">Проверьте настройки для журнализации в пункте "Главная книга" > "Настройка главной книги" > "Параметры главной книги".</span><span class="sxs-lookup"><span data-stu-id="6017a-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="6017a-107">В поле "Расширенный журнал ГК" можно задать значение "Да" или "Нет".</span><span class="sxs-lookup"><span data-stu-id="6017a-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="6017a-108">Если "Да", выходные данные отчета будут другими.</span><span class="sxs-lookup"><span data-stu-id="6017a-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="6017a-109">Выберите, можно ли закрыть период, если процесс журнализации не был запущен.</span><span class="sxs-lookup"><span data-stu-id="6017a-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="6017a-110">Если для этого параметра задано значение "Да", период нельзя закрыть до тех пор, пока не будет завершен процесс журнализации за этот период.</span><span class="sxs-lookup"><span data-stu-id="6017a-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="6017a-111">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6017a-111">Close the page.</span></span>
5. <span data-ttu-id="6017a-112">Перейдите в раздел "Главная книга" > "Периодические задачи" > "Журнализация".</span><span class="sxs-lookup"><span data-stu-id="6017a-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="6017a-113">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="6017a-113">Click Filter.</span></span>
7. <span data-ttu-id="6017a-114">Выделите строку с критериями фильтра, которые вы хотите указать.</span><span class="sxs-lookup"><span data-stu-id="6017a-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="6017a-115">В поле "Критерии" введите или выберите критерий фильтра.</span><span class="sxs-lookup"><span data-stu-id="6017a-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="6017a-116">Чтобы закрыть страницу фильтра, нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="6017a-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="6017a-117">Щелкните ОК, чтобы начать процесс журнализации.</span><span class="sxs-lookup"><span data-stu-id="6017a-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="6017a-118">Отчет будет создан после завершения процесса.</span><span class="sxs-lookup"><span data-stu-id="6017a-118">A report will be generated after the process is complete.</span></span>  

