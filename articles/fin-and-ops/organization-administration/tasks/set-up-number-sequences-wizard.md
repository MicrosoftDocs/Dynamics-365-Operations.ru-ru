--- 
title: "Настройка номерных серий с использованием мастера"
description: "Номерные серии используются для создания читаемых уникальных кодов для записей справочников и записей проводок, для которых требуются идентификаторы."
author: sericks007
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e8f3227f231ffc287bd6ea6204ed50f8b684e5fb
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-number-sequences-by-using-a-wizard"></a><span data-ttu-id="e94d7-103">Настройка номерных серий с использованием мастера</span><span class="sxs-lookup"><span data-stu-id="e94d7-103">Set up number sequences by using a wizard</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e94d7-104">Номерные серии используются для создания читаемых уникальных кодов для записей справочников и записей проводок, для которых требуются идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="e94d7-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="e94d7-105">Основные данные или запись проводки, для которой требуется идентификатор, называется образцом.</span><span class="sxs-lookup"><span data-stu-id="e94d7-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="e94d7-106">Перед созданием новых записей для ссылки необходимо настроить номерную серию и связать ее со ссылкой.</span><span class="sxs-lookup"><span data-stu-id="e94d7-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="e94d7-107">В этой процедуре поясняется, как настроить все требуемые номерные серии одновременно с помощью мастера.</span><span class="sxs-lookup"><span data-stu-id="e94d7-107">This procedure explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="e94d7-108">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="e94d7-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="e94d7-109">Перейдите в раздел "Управление организацией" > "Номерные серии" > "Номерные серии".</span><span class="sxs-lookup"><span data-stu-id="e94d7-109">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="e94d7-110">Щелкните "Сформировать".</span><span class="sxs-lookup"><span data-stu-id="e94d7-110">Click Generate.</span></span>
3. <span data-ttu-id="e94d7-111">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="e94d7-111">Click Next.</span></span>
    * <span data-ttu-id="e94d7-112">На этой странице можно изменить идентификационный код, наименьшее значение и самое высокое значение.</span><span class="sxs-lookup"><span data-stu-id="e94d7-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="e94d7-113">Кроме того, можно указать, должна ли номерная серия быть непрерывной.</span><span class="sxs-lookup"><span data-stu-id="e94d7-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
    * <span data-ttu-id="e94d7-114">Не выбирайте вариант "Непрерывная", если необходимо предварительно распределить числа для номерной серии.</span><span class="sxs-lookup"><span data-stu-id="e94d7-114">Do not select the Continuous option if you must preallocate numbers for the number sequence.</span></span>     <span data-ttu-id="e94d7-115">Для добавления сегмента масштаба в формат номерной серии выберите формат в списке, а затем щелкните "Включение области в формат".</span><span class="sxs-lookup"><span data-stu-id="e94d7-115">To add a scope segment to the format of a number sequence, select the format in the list, and then click Include scope in format.</span></span>     <span data-ttu-id="e94d7-116">Для удаления сегмента масштаба из формата номерной серии выберите формат в списке, а затем щелкните "Удаление области из формата".</span><span class="sxs-lookup"><span data-stu-id="e94d7-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then click Remove scope from format.</span></span>     <span data-ttu-id="e94d7-117">Чтобы исключить номерную серию из автоматического создания, выберите номерную серию в списке, а затем щелкните "Удалить".</span><span class="sxs-lookup"><span data-stu-id="e94d7-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then click Delete.</span></span>  
4. <span data-ttu-id="e94d7-118">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="e94d7-118">Click Next.</span></span>
5. <span data-ttu-id="e94d7-119">Нажмите кнопку Готово.</span><span class="sxs-lookup"><span data-stu-id="e94d7-119">Click Finish.</span></span>


