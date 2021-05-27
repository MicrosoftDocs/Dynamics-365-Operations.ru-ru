---
title: Переменные управления качеством
description: В этой теме описывается, как создавать переменные проверки, чтобы можно было использовать для качественных проверок с заказами контроля качества в Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5102d09f5762a390d6fd3aadafcb2ed23820982
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021716"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="63502-103">Переменные управления качеством</span><span class="sxs-lookup"><span data-stu-id="63502-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63502-104">В этой теме описывается, как создавать переменные проверки, чтобы можно было использовать для качественных проверок с заказами контроля качества в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="63502-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="63502-105">Для каждой качественной проверки, заданной на странице **Проверка**, следует определить переменную проверки и ее возможные результаты.</span><span class="sxs-lookup"><span data-stu-id="63502-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="63502-106">(Для качественных проверок поле **Тип** на странице **Проверки** задается как *Параметр*.)</span><span class="sxs-lookup"><span data-stu-id="63502-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="63502-107">Используйте страницу **Переменные проверки** для настройки, изменения и просмотра возможных результатов переменной проверки, связанной с качественной проверкой.</span><span class="sxs-lookup"><span data-stu-id="63502-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="63502-108">Для каждого результата назначается статус результата *Пройдено* или *Ошибка*, чтобы указать, пройдена ли проверка или нет, при выборе этого результата в качестве результата проверки.</span><span class="sxs-lookup"><span data-stu-id="63502-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="63502-109">Используйте страницу **Группы проверки** для назначения переменной проверки и ее результата по умолчанию для отдельной качественной проверки.</span><span class="sxs-lookup"><span data-stu-id="63502-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="63502-110">Для каждой переменной проверки рекомендуется определить по крайней мере два результата: один со статусом *Пройдено*, а второй *Ошибка*.</span><span class="sxs-lookup"><span data-stu-id="63502-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="63502-111">Нет ограничения на общее число переменных или результатов, которые могут быть определены.</span><span class="sxs-lookup"><span data-stu-id="63502-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="63502-112">Кроме того, несколько проверок могут использовать одни и те же переменные проверки для записи результатов.</span><span class="sxs-lookup"><span data-stu-id="63502-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="63502-113">Примеры переменных проверки</span><span class="sxs-lookup"><span data-stu-id="63502-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="63502-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63502-114">Example 1</span></span>

<span data-ttu-id="63502-115">Производственная компания выполняет две проверки произведенных материалов.</span><span class="sxs-lookup"><span data-stu-id="63502-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="63502-116">В одной проверке уровень pH связан с цветной полоской.</span><span class="sxs-lookup"><span data-stu-id="63502-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="63502-117">Приемлемые уровни pH — более светлые цвета, а неприемлемые уровни pH — более темные цвета.</span><span class="sxs-lookup"><span data-stu-id="63502-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="63502-118">В ходе другой проверки выполняется несколько визуальных проверок, и работники контроля качества используют свое мнение для определения того, проходит ли номенклатура визуальную проверку или нет.</span><span class="sxs-lookup"><span data-stu-id="63502-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="63502-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="63502-119">Example 2</span></span>

<span data-ttu-id="63502-120">Производственная компания, выпускающая печенье, использует инспекционный тест для готовой продукции.</span><span class="sxs-lookup"><span data-stu-id="63502-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="63502-121">Этот инспекционный тест имеет несколько переменных.</span><span class="sxs-lookup"><span data-stu-id="63502-121">This inspection test has several variables.</span></span> <span data-ttu-id="63502-122">Одна из переменных — вкус, при этом возможные результаты — хороший или плохой.</span><span class="sxs-lookup"><span data-stu-id="63502-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="63502-123">Вторая переменная — цвет, возможные результаты — "слишком темное", "слишком светлое" и "правильный".</span><span class="sxs-lookup"><span data-stu-id="63502-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="63502-124">Создание переменной проверки</span><span class="sxs-lookup"><span data-stu-id="63502-124">Create a test variable</span></span>

<span data-ttu-id="63502-125">Чтобы создать переменную проверки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="63502-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="63502-126">Перейдите **Управление запасами \> Настройка \> Контроль качества \> Переменные проверки**.</span><span class="sxs-lookup"><span data-stu-id="63502-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="63502-127">На панели операций выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="63502-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="63502-128">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="63502-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="63502-129">**Переменная** — введите уникальный код или имя переменной.</span><span class="sxs-lookup"><span data-stu-id="63502-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="63502-130">**Описание** — введите подробное описание переменной.</span><span class="sxs-lookup"><span data-stu-id="63502-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="63502-131">Когда новая строка все еще выбрана, выберите **Результаты** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="63502-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="63502-132">На странице **Результаты переменной проверки** в области действий выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="63502-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="63502-133">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="63502-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="63502-134">**Результат** — введите уникальный код или имя результата.</span><span class="sxs-lookup"><span data-stu-id="63502-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="63502-135">**Описание** — введите подробное описание результата.</span><span class="sxs-lookup"><span data-stu-id="63502-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="63502-136">**Статус результата** — выберите *Пройдено* или *Ошибка*, чтобы указать, пройдена ли проверка или нет, при выборе результата в качестве результата проверки.</span><span class="sxs-lookup"><span data-stu-id="63502-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="63502-137">Повторите предыдущий шаг для каждого дополнительного результата.</span><span class="sxs-lookup"><span data-stu-id="63502-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="63502-138">Убедитесь, что по крайней мере один результат имеет статус *Пройдено*, а по крайней мере один имеет статус *Ошибка*.</span><span class="sxs-lookup"><span data-stu-id="63502-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="63502-139">Закройте страницы.</span><span class="sxs-lookup"><span data-stu-id="63502-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="63502-140">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="63502-140">Additional resources</span></span>

- [<span data-ttu-id="63502-141">Инструменты проверки управления качеством</span><span class="sxs-lookup"><span data-stu-id="63502-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="63502-142">Проверки управления качеством</span><span class="sxs-lookup"><span data-stu-id="63502-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="63502-143">Группы проверки контроля качества</span><span class="sxs-lookup"><span data-stu-id="63502-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
