---
title: Настройка номерных серий с использованием мастера
description: В этой теме поясняется, как настроить все требуемые номерные серии одновременно с помощью мастера.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f97c4cd6cdb117ebdd67a155478bb6f8d1703541
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867399"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="6100f-103">Настройка номерных серий с использованием мастера</span><span class="sxs-lookup"><span data-stu-id="6100f-103">Set up number sequences using a wizard</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6100f-104">Номерные серии используются для создания читаемых уникальных кодов для записей справочников и записей проводок, для которых требуются идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="6100f-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="6100f-105">Основные данные или запись проводки, для которой требуется идентификатор, называется образцом.</span><span class="sxs-lookup"><span data-stu-id="6100f-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="6100f-106">Перед созданием новых записей для ссылки необходимо настроить номерную серию и связать ее со ссылкой.</span><span class="sxs-lookup"><span data-stu-id="6100f-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="6100f-107">В этой теме поясняется, как настроить все требуемые номерные серии одновременно с помощью мастера.</span><span class="sxs-lookup"><span data-stu-id="6100f-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="6100f-108">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="6100f-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="6100f-109">Перейдите к **Область перехода > Модули > Управление организацией > Номерные серии" > Номерные серии**.</span><span class="sxs-lookup"><span data-stu-id="6100f-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="6100f-110">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="6100f-110">Select **Generate**.</span></span>
3. <span data-ttu-id="6100f-111">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="6100f-111">Select **Next**.</span></span>

   - <span data-ttu-id="6100f-112">На этой странице можно изменить идентификационный код, наименьшее значение и самое высокое значение.</span><span class="sxs-lookup"><span data-stu-id="6100f-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="6100f-113">Кроме того, можно указать, должна ли номерная серия быть непрерывной.</span><span class="sxs-lookup"><span data-stu-id="6100f-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="6100f-114">Не выбирайте вариант **Непрерывная**, если необходимо предварительно распределить числа для номерной серии.</span><span class="sxs-lookup"><span data-stu-id="6100f-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="6100f-115">Для добавления сегмента масштаба в формат номерной серии выберите формат в списке, затем выберите **Включение области в формат**.</span><span class="sxs-lookup"><span data-stu-id="6100f-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="6100f-116">Для удаления сегмента масштаба из формата номерной серии выберите формат в списке, затем выберите **Удаление области из формата**.</span><span class="sxs-lookup"><span data-stu-id="6100f-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="6100f-117">Чтобы исключить номерную серию из автоматического создания, выберите номерную серию в списке, затем выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="6100f-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="6100f-118">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="6100f-118">Select **Next**.</span></span>
5. <span data-ttu-id="6100f-119">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="6100f-119">Select **Finish**.</span></span>

