---
title: Проверки управления качеством
description: В этой теме описывается, как создавать проверки, которые можно использовать заказов контроля качества в Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: b88011f486b6582db4727b85d021868899c6abe1
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956803"
---
# <a name="quality-management-tests"></a><span data-ttu-id="266fd-103">Проверки управления качеством</span><span class="sxs-lookup"><span data-stu-id="266fd-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="266fd-104">В этой теме описывается, как создавать проверки, которые можно использовать заказов контроля качества в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="266fd-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="266fd-105">Используйте страницу **Проверки** для назначения и просмотра отдельных проверок, определяющих соответствие вашей продукции требованиям к качеству.</span><span class="sxs-lookup"><span data-stu-id="266fd-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="266fd-106">Вы можете назначить одни или несколько индивидуальных испытаний в группе проверки.</span><span class="sxs-lookup"><span data-stu-id="266fd-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="266fd-107">В этом случае вы также определяете информацию, специфичную для теста, такую как приемлемые значения измерения.</span><span class="sxs-lookup"><span data-stu-id="266fd-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="266fd-108">Значения измерений используются для количественных проверок.</span><span class="sxs-lookup"><span data-stu-id="266fd-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="266fd-109">Для качественных проверок используются переменные проверки.</span><span class="sxs-lookup"><span data-stu-id="266fd-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="266fd-110">Для количественных проверок поле **Тип** задано как *Целое число* или *Дробь*.</span><span class="sxs-lookup"><span data-stu-id="266fd-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="266fd-111">Также поддерживается единица измерения.</span><span class="sxs-lookup"><span data-stu-id="266fd-111">A unit of measure is also specified.</span></span> <span data-ttu-id="266fd-112">Спецификации качества и результаты теста выражаются числами.</span><span class="sxs-lookup"><span data-stu-id="266fd-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="266fd-113">Для качественных проверок поле **Тип** задано как *Параметр*.</span><span class="sxs-lookup"><span data-stu-id="266fd-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="266fd-114">Для качественных испытаний требуется дополнительная информация об измеряемой тестовой переменной и ее возможных перечислимых вариантах.</span><span class="sxs-lookup"><span data-stu-id="266fd-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="266fd-115">Спецификации качества и результаты теста выражаются в соответствии с результатом.</span><span class="sxs-lookup"><span data-stu-id="266fd-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="266fd-116">Кроме того, можно (необязательно) назначить инструмент проверки для проверки.</span><span class="sxs-lookup"><span data-stu-id="266fd-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="266fd-117">Однако для создания и использования проверок с заказами контроля качества не требуется наличие инструментов проверки.</span><span class="sxs-lookup"><span data-stu-id="266fd-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="266fd-118">Дополнительные сведения см. в разделе [Инструменты проверки управления качеством](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="266fd-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="266fd-119">Есть также возможность указать единицу измерения для проверки, чтобы указать единицу измерения, в которой записываются результаты проверок.</span><span class="sxs-lookup"><span data-stu-id="266fd-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="266fd-120">Например, проверка температуры может включать в себя единицу измерения градусы Фаренгейта или градусы Цельсия.</span><span class="sxs-lookup"><span data-stu-id="266fd-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="266fd-121">Пример проверки</span><span class="sxs-lookup"><span data-stu-id="266fd-121">Example of a test</span></span>

<span data-ttu-id="266fd-122">Производственная компания проводит две проверки купленных материалов: количественную проверку качества материала и качественную проверку повреждения упаковки.</span><span class="sxs-lookup"><span data-stu-id="266fd-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="266fd-123">Компания определяет дополнительную информацию о качественной проверке, чтобы задать переменную проверки (например, поврежденная упаковка) и ее результаты.</span><span class="sxs-lookup"><span data-stu-id="266fd-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="266fd-124">Компания использует страницу **Группы проверки** для того, чтобы назначить два испытания в группу проверки и указать информацию, специфичную для испытания.</span><span class="sxs-lookup"><span data-stu-id="266fd-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="266fd-125">Группа проверки назначается заказу контроля качества, таким образом компания может составить отчет по результатам этих двух проверок.</span><span class="sxs-lookup"><span data-stu-id="266fd-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="266fd-126">Создание проверки</span><span class="sxs-lookup"><span data-stu-id="266fd-126">Create a test</span></span>

<span data-ttu-id="266fd-127">Чтобы создать проверку, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="266fd-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="266fd-128">Перейдите **Управление запасами \> Настройка \> Контроль качества \> Проверки**.</span><span class="sxs-lookup"><span data-stu-id="266fd-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="266fd-129">На панели операций выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="266fd-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="266fd-130">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="266fd-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="266fd-131">**Проверка** — введите уникальный код или имя проверки.</span><span class="sxs-lookup"><span data-stu-id="266fd-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="266fd-132">**Описание** — введите подробное описание проверки.</span><span class="sxs-lookup"><span data-stu-id="266fd-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="266fd-133">**Тип** — выберите тип результатов, которые создает данная проверка.</span><span class="sxs-lookup"><span data-stu-id="266fd-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="266fd-134">Для количественных проверок выберите *Дробь* или *Целое число*.</span><span class="sxs-lookup"><span data-stu-id="266fd-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="266fd-135">Для качественных проверок выберите *Параметр*.</span><span class="sxs-lookup"><span data-stu-id="266fd-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="266fd-136">**Инструмент проверки** — выберите [инструмент проверки](quality-test-instruments.md), который должен использоваться для проверки.</span><span class="sxs-lookup"><span data-stu-id="266fd-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="266fd-137">**Единица измерения** — если выбрано значение *Дробь* или *Целое число* в поле **Тип** (то есть, если проверки являются количественными), выберите единицу измерения, в которой должны записываться результаты проверок.</span><span class="sxs-lookup"><span data-stu-id="266fd-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="266fd-138">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="266fd-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="266fd-139">После сохранения проверки поле **Тип** в сетке больше нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="266fd-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="266fd-140">Если необходимо изменить тип результатов проверки, которые будут записаны для проверки, выберите **Изменение типа проверки качества** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="266fd-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="266fd-141">В диалоговом окне **Изменение типа проверки качества** проверьте значение в поле **Создать тип**, а затем выберите **ОК**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="266fd-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="266fd-142">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="266fd-142">Additional resources</span></span>

- [<span data-ttu-id="266fd-143">Инструменты проверки управления качеством</span><span class="sxs-lookup"><span data-stu-id="266fd-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="266fd-144">Группы проверки контроля качества</span><span class="sxs-lookup"><span data-stu-id="266fd-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="266fd-145">Переменные управления качеством</span><span class="sxs-lookup"><span data-stu-id="266fd-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="266fd-146">Сопоставления контроля качества</span><span class="sxs-lookup"><span data-stu-id="266fd-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
