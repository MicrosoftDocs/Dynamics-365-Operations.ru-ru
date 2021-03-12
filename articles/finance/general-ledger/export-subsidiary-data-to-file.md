---
title: Экспорт данных дочерних компаний в файлы
description: В этой теме объясняется, как подготовиться к экспорту данных из Microsoft Dynamics 365 Finance, затем импортируйте их в консолидированное юридическое лицо.
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
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 179a401178935b8a76d6718a7fb1f63e08344f50
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968687"
---
# <a name="export-subsidiary-data-to-files"></a><span data-ttu-id="7ea9e-103">Экспорт данных дочерних компаний в файлы</span><span class="sxs-lookup"><span data-stu-id="7ea9e-103">Export subsidiary data to files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ea9e-104">Страница **Экспорт** (**Администрирование системы \> Рабочие области \> Импорт/экспорт**) используется для подготовки к экспорту данных дочерних компаний в файлы, которые затем могут быть импортированы в консолидированное юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-104">You use the **Export** page (**System administration \> Workspaces \> Import/Export**) to prepare to export subsidiary data to files that can then be imported into a consolidated legal entity.</span></span> <span data-ttu-id="7ea9e-105">Дополнительные сведения о процессах импорта и экспорта см. в разделе [Обзор заданий импорта и экспорта данных](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="7ea9e-105">For more information about the import and export processes, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

1. <span data-ttu-id="7ea9e-106">Создайте юридическое лицо для процесса консолидации.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-106">Create a legal entity for the consolidation process.</span></span> <span data-ttu-id="7ea9e-107">Сведения о порядке создания юридических лиц см. в разделе [Создание юридических лиц](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span><span class="sxs-lookup"><span data-stu-id="7ea9e-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="7ea9e-108">Дополнительные сведения см. в разделах [Подготовка юридического лица для использования в процессе консолидации](prepare-company-for-consolidation.md) и [Настройка дочернего юридического лица для консолидации](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="7ea9e-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span> 

2. <span data-ttu-id="7ea9e-109">Перейдите в раздел **Консолидации \> Экспорт сальдо компаний**.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-109">Go to **Consolidations \> Export company balances**.</span></span> <span data-ttu-id="7ea9e-110">На странице **Экспорт сальдо компаний** на вкладке **Критерии** укажите подробные сведения о консолидации, задав следующие поля.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-110">On the **Export company balances** page, on the **Criteria** tab, specify the details of the consolidation by setting the following fields.</span></span>

    | <span data-ttu-id="7ea9e-111">Поле</span><span class="sxs-lookup"><span data-stu-id="7ea9e-111">Field</span></span>                             | <span data-ttu-id="7ea9e-112">описание</span><span class="sxs-lookup"><span data-stu-id="7ea9e-112">Description</span></span> |
    |-----------------------------------|-------|
    | <span data-ttu-id="7ea9e-113">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="7ea9e-113">Main account</span></span>                      | <span data-ttu-id="7ea9e-114">Укажите счета для консолидации.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-114">Specify the accounts to consolidate.</span></span> <span data-ttu-id="7ea9e-115">Чтобы включить все счета, оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-115">To include all accounts, leave this field blank.</span></span> |
    | <span data-ttu-id="7ea9e-116">Использовать счет консолидации</span><span class="sxs-lookup"><span data-stu-id="7ea9e-116">Use consolidation account</span></span>         | <span data-ttu-id="7ea9e-117">Если вы указали счета консолидации, установите для этого параметра значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-117">If you've specified consolidation accounts, set this option to **Yes**.</span></span> |
    | <span data-ttu-id="7ea9e-118">Выбрать счет консолидации из</span><span class="sxs-lookup"><span data-stu-id="7ea9e-118">Select consolidation account from</span></span> | <span data-ttu-id="7ea9e-119">Выберите **Счет ГК** или **Группа счетов консолидации**.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-119">Select either **Main account** or **Consolidation account group**.</span></span> |
    | <span data-ttu-id="7ea9e-120">Группы счетов консолидации</span><span class="sxs-lookup"><span data-stu-id="7ea9e-120">Consolidation account group</span></span>       | <span data-ttu-id="7ea9e-121">Выберите группу счетов консолидации для выбранного вами счета консолидации.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-121">Select a consolidation account group for the consolidation account that you selected.</span></span> |
    | <span data-ttu-id="7ea9e-122">Период консолидации</span><span class="sxs-lookup"><span data-stu-id="7ea9e-122">Consolidation period</span></span>              | <span data-ttu-id="7ea9e-123">Укажите даты "С" и "По" для консолидации.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-123">Specify "from" and "to" dates for the consolidation.</span></span> |
    | <span data-ttu-id="7ea9e-124">Включить фактические суммы</span><span class="sxs-lookup"><span data-stu-id="7ea9e-124">Include actual amounts</span></span>            | <span data-ttu-id="7ea9e-125">Установите для этого параметра значение **Да**, чтобы включить фактические значения.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-125">Set this option to **Yes** to include actual amounts.</span></span> |
    | <span data-ttu-id="7ea9e-126">Включить бюджетные суммы</span><span class="sxs-lookup"><span data-stu-id="7ea9e-126">Include budget amounts</span></span>            | <span data-ttu-id="7ea9e-127">Установите для этого параметра значение **Да**, чтобы включить бюджетные значения в консолидации.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-127">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="7ea9e-128">Модели бюджета</span><span class="sxs-lookup"><span data-stu-id="7ea9e-128">Budget models</span></span>                     | <span data-ttu-id="7ea9e-129">Укажите модель бюджета для включения.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-129">Specify the budget model to include.</span></span> |

3. <span data-ttu-id="7ea9e-130">На вкладке **Финансовые аналитики** укажите подробные сведения по консолидации:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-130">On the **Financial dimensions** tab, specify the details of the consolidation:</span></span>

    - <span data-ttu-id="7ea9e-131">Укажите сведения о финансовых аналитиках, которые должны переноситься из проводок по счетам дочерних компаний в проводки консолидированного юридического лица.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-131">Specify the financial dimension information that should be transferred from the transactions in the subsidiary accounts to the transactions in the consolidated legal entity.</span></span>
    - <span data-ttu-id="7ea9e-132">Выберите финансовые аналитики в списке.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-132">Select financial dimensions in the list.</span></span>
    - <span data-ttu-id="7ea9e-133">Определите правильную спецификацию для каждой консолидированной финансовой аналитики.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-133">Identify the correct specification for each financial dimension that is consolidated.</span></span> <span data-ttu-id="7ea9e-134">Доступны следующие параметры: **Аналитика**, **Групповая аналитика**, **Счета компании** и **Счет**.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-134">The available options include **Dimension**, **Group dimension**, **Company accounts**, and **Account**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="7ea9e-135">Параметр **Групповая аналитика** позволяет определить значение аналитики, используемое группой консолидируемых компаний.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-135">The **Group dimension** option lets you define the dimension value that is used by the group of companies that is being consolidated.</span></span>

    - <span data-ttu-id="7ea9e-136">Укажите порядок консолидации сегментов.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-136">Specify the segment order to consolidate in.</span></span>

4. <span data-ttu-id="7ea9e-137">На вкладке **Юридические лица** выполните следующие действия, чтобы указать юридическое лицо, для которого выполняется экспорт:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-137">On the **Legal entities** tab, follow these steps to specify the legal entity that you're exporting:</span></span>

    1. <span data-ttu-id="7ea9e-138">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-138">Select **New**.</span></span>
    2. <span data-ttu-id="7ea9e-139">В поле **Исходное юридическое лицо** введите юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-139">In the **Source legal entity** field, enter the legal entity.</span></span>

        <span data-ttu-id="7ea9e-140">Если по отношению к нескольким дочерним компаниям из одной базы данных применяются одинаковые критерии, данные из этих компаний можно перенести в отдельные файлы экспорта в рамках одной операции:</span><span class="sxs-lookup"><span data-stu-id="7ea9e-140">If the same criteria apply to several subsidiaries that are in the same database, you can transfer data from those subsidiaries to separate export files in a single operation:</span></span>

        1. <span data-ttu-id="7ea9e-141">Создайте строку для каждого дочернего юридического лица, чьи счета следует экспортировать в файлы.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-141">Create a line for each subsidiary legal entity for which accounts should be exported to files.</span></span> <span data-ttu-id="7ea9e-142">Эти файлы в дальнейшем будут импортированы в консолидированное юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-142">These files will be imported into the consolidated legal entity later.</span></span>
        2. <span data-ttu-id="7ea9e-143">Для каждой дочерней компании введите наименование дочерней компании и имя файла экспорта, который будет создан во время выполнения задания экспорта.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-143">For each subsidiary, enter the subsidiary name and the name of the export file that will be created during the export job.</span></span>

    3. <span data-ttu-id="7ea9e-144">В поле **Тип счета разницы преобразования** выберите **Прибыли и убытки** или **Балансовый отчет**.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-144">In **Account type of conversion differences** field, Select **Profit and loss** or **Balance sheet**.</span></span>
    4. <span data-ttu-id="7ea9e-145">Введите имя файла для файла экспорта, который будет создан.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-145">Enter a file name for the export file that will be created.</span></span>

5. <span data-ttu-id="7ea9e-146">Выберите **OK**, чтобы выполнить экспорт.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-146">Select **OK** to run the export.</span></span>

<span data-ttu-id="7ea9e-147">После завершения экспорта вы получите сообщение, которое показывает количество записей, которые были сохранены в каждом файле.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-147">When the export is completed, you receive a message that shows the number of records that were saved in each file.</span></span> <span data-ttu-id="7ea9e-148">Теперь можно импортировать файлы в консолидированное юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="7ea9e-148">You can then import the files into the consolidated legal entity.</span></span>
