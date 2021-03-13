---
title: Импорт данных дочерних компаний из файлов
description: В этой теме объясняется, как подготовить данные из внешних систем, чтобы их можно было импортировать в Microsoft Dynamics 365 Finance.
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 7ced1b970aefa20a27ab16e005dff8fabace78d1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988833"
---
# <a name="import-subsidiary-data-from-files"></a><span data-ttu-id="61af1-103">Импорт данных дочерних компаний из файлов</span><span class="sxs-lookup"><span data-stu-id="61af1-103">Import subsidiary data from files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61af1-104">В этой теме объясняется, как подготовить данные из внешних систем, чтобы их можно было импортировать в Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="61af1-104">This topic explains how to prepare data from external systems so that it can be imported into Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="61af1-105">Используйте страницу **Консолидировать с импортом** (**Консолидации \> Консолидировать с импортом**) для подготовки переноса данных дочерней компании из внешних систем.</span><span class="sxs-lookup"><span data-stu-id="61af1-105">You use the **Consolidate with import** page (**Consolidations \> Consolidate with import**) to prepare the transfer of subsidiary data from external systems.</span></span>

1. <span data-ttu-id="61af1-106">Создайте дочернее юридическое лицо для консолидации.</span><span class="sxs-lookup"><span data-stu-id="61af1-106">Create a subsidiary legal entity for the consolidation.</span></span> <span data-ttu-id="61af1-107">Сведения о порядке создания юридических лиц см. в разделе [Создание юридических лиц](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span><span class="sxs-lookup"><span data-stu-id="61af1-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="61af1-108">Дополнительные сведения см. в разделах [Подготовка юридического лица для использования в процессе консолидации](prepare-company-for-consolidation.md) и [Настройка дочернего юридического лица для консолидации](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="61af1-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span>

2. <span data-ttu-id="61af1-109">Подготовьте файл, который будет содержать импортируемые данные.</span><span class="sxs-lookup"><span data-stu-id="61af1-109">Prepare a file that will contain the data that is imported.</span></span> <span data-ttu-id="61af1-110">Дополнительные сведения о процессе импорта см. в разделе [Обзор заданий импорта и экспорта данных](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="61af1-110">For more information about the import process, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
3. <span data-ttu-id="61af1-111">Экспортируйте данные в файл, следуя шагам в процедуре "Процесс импорта/экспорта данных" в разделе [Обзор заданий импорта и экспорта данных](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="61af1-111">Export the data to a file by following the steps in the "Data import/export process" procedure in [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span> <span data-ttu-id="61af1-112">Эту процедуру можно использовать для консолидации данных либо из другого экземпляра Dynamics 365 Finance, либо из Dynamics 365 Business Central.</span><span class="sxs-lookup"><span data-stu-id="61af1-112">You can use that procedure to consolidate data either from another instance of Dynamics 365 Finance or from Dynamics 365 Business Central.</span></span> <span data-ttu-id="61af1-113">При импорте данных из внешних систем данные должны иметь формат, описанный в разделе [Экспорт данных дочерних компаний в файлы](export-subsidiary-data-to-file.md).</span><span class="sxs-lookup"><span data-stu-id="61af1-113">If you're importing data from external systems, data must be in the format that's described in [Export subsidiary data to files](export-subsidiary-data-to-file.md).</span></span>
4. <span data-ttu-id="61af1-114">Перейдите в раздел **Консолидации \> Консолидировать с импортом**.</span><span class="sxs-lookup"><span data-stu-id="61af1-114">Go to **Consolidations \> Consolidate with import**.</span></span> <span data-ttu-id="61af1-115">На странице **Консолидировать с импортом** на вкладке **Критерии** укажите подробные сведения отчета и/или импорта, задав следующие поля.</span><span class="sxs-lookup"><span data-stu-id="61af1-115">On the **Consolidate with import** page, on the **Criteria** tab, specify the details of the report and/or the import by setting the following fields.</span></span>

    | <span data-ttu-id="61af1-116">Поле</span><span class="sxs-lookup"><span data-stu-id="61af1-116">Field</span></span>                                 | <span data-ttu-id="61af1-117">Значение для отчета</span><span class="sxs-lookup"><span data-stu-id="61af1-117">Value for the report</span></span> | <span data-ttu-id="61af1-118">Значение для импорта</span><span class="sxs-lookup"><span data-stu-id="61af1-118">Value for the import</span></span> |
    |---------------------------------------|----------------------|----------------------|
    | <span data-ttu-id="61af1-119">описание</span><span class="sxs-lookup"><span data-stu-id="61af1-119">Description</span></span>                           | <span data-ttu-id="61af1-120">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="61af1-120">Not applicable</span></span> | <span data-ttu-id="61af1-121">Введите описание для определения импорта.</span><span class="sxs-lookup"><span data-stu-id="61af1-121">Enter a description to identify the import.</span></span> |
    | <span data-ttu-id="61af1-122">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="61af1-122">Main account</span></span>                          | <span data-ttu-id="61af1-123">Определите диапазон счетов, которые должны быть включены в отчет.</span><span class="sxs-lookup"><span data-stu-id="61af1-123">Define the range of accounts that the report should include.</span></span> <span data-ttu-id="61af1-124">Если диапазон не определен, будут включены все счета.</span><span class="sxs-lookup"><span data-stu-id="61af1-124">If you don't define a range, all accounts will be included.</span></span> | <span data-ttu-id="61af1-125">Определите диапазон счетов, которые должны быть включены в импорт.</span><span class="sxs-lookup"><span data-stu-id="61af1-125">Define the range of accounts that the import should include.</span></span> <span data-ttu-id="61af1-126">Если диапазон не определен, будут включены все счета.</span><span class="sxs-lookup"><span data-stu-id="61af1-126">If you don't define a range, all accounts will be included.</span></span> |
    | <span data-ttu-id="61af1-127">Период консолидации</span><span class="sxs-lookup"><span data-stu-id="61af1-127">Consolidation period</span></span>                  | <span data-ttu-id="61af1-128">Определите диапазон дат для консолидации.</span><span class="sxs-lookup"><span data-stu-id="61af1-128">Define the range of dates to consolidate.</span></span> | <span data-ttu-id="61af1-129">Определите диапазон дат для консолидации.</span><span class="sxs-lookup"><span data-stu-id="61af1-129">Define the range of dates to consolidate.</span></span> |
    | <span data-ttu-id="61af1-130">Включить фактические суммы</span><span class="sxs-lookup"><span data-stu-id="61af1-130">Include actual amounts</span></span>                | <span data-ttu-id="61af1-131">Установите для этого параметра значение **Да**, чтобы включить фактические значения.</span><span class="sxs-lookup"><span data-stu-id="61af1-131">Set this option to **Yes** to include actuals.</span></span> | <span data-ttu-id="61af1-132">Установите для этого параметра значение **Да**, чтобы включить фактические значения.</span><span class="sxs-lookup"><span data-stu-id="61af1-132">Set this option to **Yes** to include actuals.</span></span> |
    | <span data-ttu-id="61af1-133">Включить бюджетные суммы</span><span class="sxs-lookup"><span data-stu-id="61af1-133">Include budget amounts</span></span>                | <span data-ttu-id="61af1-134">Установите для этого параметра значение **Да**, чтобы включить бюджетные значения в консолидации.</span><span class="sxs-lookup"><span data-stu-id="61af1-134">Set this option to **Yes** to include budget amounts in consolidations.</span></span> | <span data-ttu-id="61af1-135">Установите для этого параметра значение **Да**, чтобы включить бюджетные значения в консолидации.</span><span class="sxs-lookup"><span data-stu-id="61af1-135">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="61af1-136">Перестройка сальдо во время консолидации</span><span class="sxs-lookup"><span data-stu-id="61af1-136">Rebuild balances during consolidation</span></span> | <span data-ttu-id="61af1-137">Установите для этого параметра значение **Да**, если процесс перестроения должен полностью очистить баланс и новые записи, а затем повторно создать сальдо с начала времени.</span><span class="sxs-lookup"><span data-stu-id="61af1-137">Set this option to **Yes** if the rebuild process should completely clear the balance and new records, and re-create the balance from the beginning of time.</span></span> | <span data-ttu-id="61af1-138">Установите для этого параметра значение **Да**, если процесс перестроения должен полностью очистить баланс и новые записи, а затем повторно создать сальдо с начала времени.</span><span class="sxs-lookup"><span data-stu-id="61af1-138">Set this option to **Yes** if the rebuild process should completely clear the balance and new records, and re-create the balance from the beginning of time.</span></span> |
    | <span data-ttu-id="61af1-139">Модели бюджета</span><span class="sxs-lookup"><span data-stu-id="61af1-139">Budget models</span></span>                         | <span data-ttu-id="61af1-140">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="61af1-140">Not applicable</span></span> | <span data-ttu-id="61af1-141">Если вы выбрали импорт бюджетных сумм, введите модели бюджета для консолидации.</span><span class="sxs-lookup"><span data-stu-id="61af1-141">If you selected to import budget amounts, enter the budget models to consolidate.</span></span> |
    | <span data-ttu-id="61af1-142">Тип бюджетного курса</span><span class="sxs-lookup"><span data-stu-id="61af1-142">Budget rate type</span></span>                      | <span data-ttu-id="61af1-143">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="61af1-143">Not applicable</span></span> | <span data-ttu-id="61af1-144">Введите тип валютного курса для бюджета.</span><span class="sxs-lookup"><span data-stu-id="61af1-144">Enter the type of budget exchange rate.</span></span> |

6. <span data-ttu-id="61af1-145">Если имеются различные валюты учета, используйте поля на вкладке **Преобразование валют** для настройки преобразования, выполняемого в ходе консолидации.</span><span class="sxs-lookup"><span data-stu-id="61af1-145">If you have different accounting currencies, use the fields on the **Currency translation** tab to configure the translation that is done during consolidation.</span></span>

    | <span data-ttu-id="61af1-146">Поле</span><span class="sxs-lookup"><span data-stu-id="61af1-146">Field</span></span>                      | <span data-ttu-id="61af1-147">описание</span><span class="sxs-lookup"><span data-stu-id="61af1-147">Description</span></span> |
    |----------------------------|-------------|
    | <span data-ttu-id="61af1-148">Исходное юридическое лицо</span><span class="sxs-lookup"><span data-stu-id="61af1-148">Source legal entity</span></span>        | <span data-ttu-id="61af1-149">Выберите юридическое лицо, из которого выполняется импорт.</span><span class="sxs-lookup"><span data-stu-id="61af1-149">Select the legal entity that you're importing from.</span></span> |
    | <span data-ttu-id="61af1-150">Исходная валюта учета</span><span class="sxs-lookup"><span data-stu-id="61af1-150">Source accounting currency</span></span> | <span data-ttu-id="61af1-151">Эта валюта по умолчанию является валютой, связанной с исходным юридическим лицом, выбранным в поле **Исходное юридическое лицо**.</span><span class="sxs-lookup"><span data-stu-id="61af1-151">This default currency is the currency that is associated with the source legal entity that you selected in the **Source legal entity** field.</span></span> |
    | <span data-ttu-id="61af1-152">Исходный и конечный счета</span><span class="sxs-lookup"><span data-stu-id="61af1-152">From and To accounts</span></span>       | <span data-ttu-id="61af1-153">Определите диапазон счетов для импорта из исходного юридического лица.</span><span class="sxs-lookup"><span data-stu-id="61af1-153">Define the range of accounts to import from the source legal entity.</span></span> |
    | <span data-ttu-id="61af1-154">Тип валютного курса</span><span class="sxs-lookup"><span data-stu-id="61af1-154">Exchange rate type</span></span>         | <span data-ttu-id="61af1-155">Выберите тип валютного курса.</span><span class="sxs-lookup"><span data-stu-id="61af1-155">Select the type of exchange rate.</span></span> <span data-ttu-id="61af1-156">Типы валютных курсов назначаются при создании счета ГК.</span><span class="sxs-lookup"><span data-stu-id="61af1-156">Exchange rate types are assigned when you create a main account.</span></span> <span data-ttu-id="61af1-157">Дополнительные сведения см. в разделе [Создание счета ГК](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="61af1-157">For more information, see [Create a main account](tasks/create-main-account.md).</span></span> |
    | <span data-ttu-id="61af1-158">Применить валютный курс из</span><span class="sxs-lookup"><span data-stu-id="61af1-158">Apply exchange rate from</span></span>   | <span data-ttu-id="61af1-159">Введите дату, чтобы применить валютный курс, действовавший на эту дату.</span><span class="sxs-lookup"><span data-stu-id="61af1-159">Enter a date to apply the exchange rate that was effective on that date.</span></span> <span data-ttu-id="61af1-160">Или введите значение, которое должно использоваться в качестве валютного курса.</span><span class="sxs-lookup"><span data-stu-id="61af1-160">Alternatively, enter the value that should be used as the exchange rate.</span></span> |
    | <span data-ttu-id="61af1-161">Курс обмена</span><span class="sxs-lookup"><span data-stu-id="61af1-161">Exchange rate</span></span>              | <span data-ttu-id="61af1-162">Значение по умолчанию зависит от типа валютного курса, выбранного в поле **Тип валютного курса**.</span><span class="sxs-lookup"><span data-stu-id="61af1-162">The default value depends on the type of exchange rate that you selected in the **Exchange rate type** field.</span></span> <span data-ttu-id="61af1-163">Если вы ввели определяемый пользователем валютный курс, можно определить курс.</span><span class="sxs-lookup"><span data-stu-id="61af1-163">If you entered a user-defined exchange rate, you can define a rate.</span></span> |

7. <span data-ttu-id="61af1-164">Установите для параметра **Выполнять в фоновом режиме** значение **Да**, чтобы разрешить выполнение процесса импорта в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="61af1-164">Set the **Run in background** option to **Yes** to enable the import process to run in the background.</span></span>
8. <span data-ttu-id="61af1-165">Установите для параметра **Пакетная обработка** значение **Да**, чтобы выполнить консолидацию как пакетное задание в заданное время.</span><span class="sxs-lookup"><span data-stu-id="61af1-165">Set the **Batch Processing** option to **Yes** to run the consolidation as a batch job at a specific time.</span></span> <span data-ttu-id="61af1-166">Чтобы немедленно выполнить консолидацию, выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="61af1-166">To run the consolidation immediately, select **OK**.</span></span> 

<span data-ttu-id="61af1-167">Проводки и сальдо, которые были выбраны для консолидации в дочерних компаниях, добавляются к соответствующим счетам консолидированного юридического лица.</span><span class="sxs-lookup"><span data-stu-id="61af1-167">The transactions and balances that were specified for consolidation in the subsidiaries are added to the appropriate accounts in the consolidated legal entity.</span></span>