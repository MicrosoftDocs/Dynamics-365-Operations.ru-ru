---
title: Настройка workflow-процессов по номенклатуре строки
description: В этом разделе описывается, как настроить элемент workflow-процесса номенклатуры по строке.
author: ChrisGarty
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84da7080542b4cc2ecc487b0a1331482fb69b998
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747913"
---
# <a name="configure-line-item-workflows"></a><span data-ttu-id="598a1-103">Настройка workflow-процессов по номенклатуре строки</span><span class="sxs-lookup"><span data-stu-id="598a1-103">Configure line-item workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="598a1-104">В этом разделе описывается, как настроить элемент workflow-процесса номенклатуры по строке.</span><span class="sxs-lookup"><span data-stu-id="598a1-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="598a1-105">Чтобы настроить элемент workflow-процесса по строке, в редакторе workflow-процессов, щелкните правой кнопкой мыши элемент а затем щелкните **Свойства**, чтобы открыть страницу **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="598a1-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="598a1-106">Затем используйте следующие процедуры для настройки свойств элемента workflow-процесса по строке.</span><span class="sxs-lookup"><span data-stu-id="598a1-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-line-item-workflow-element"></a><span data-ttu-id="598a1-107">Дайте имя элемента workflow-процесса по строке.</span><span class="sxs-lookup"><span data-stu-id="598a1-107">Name the line-item workflow element</span></span>

<span data-ttu-id="598a1-108">Выполните следующие действия, чтобы ввести название элемента workflow-процесса по строке.</span><span class="sxs-lookup"><span data-stu-id="598a1-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1. <span data-ttu-id="598a1-109">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="598a1-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="598a1-110">В поле **Имя** введите уникальное название для workflow-процесса по строке.</span><span class="sxs-lookup"><span data-stu-id="598a1-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="598a1-111">Укажите, используется ли тот же workflow-процесс для обработки всех элементов строк</span><span class="sxs-lookup"><span data-stu-id="598a1-111">Specify whether the same workflow is used to process all line items</span></span>

<span data-ttu-id="598a1-112">Выполните следующие действия, чтобы определить, используется ли тот же workflow-процесс для обработки всех элементов строк в документе.</span><span class="sxs-lookup"><span data-stu-id="598a1-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1. <span data-ttu-id="598a1-113">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="598a1-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="598a1-114">Если один и тот же workflow-процесс должен обрабатывать все номенклатуры строк в документе, нажмите **Вызывать один workflow-процесс для всех строк номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="598a1-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="598a1-115">Выберите workflow-процесс, который будет использоваться для обработки элемента строки.</span><span class="sxs-lookup"><span data-stu-id="598a1-115">Then select the workflow to use to process the line items.</span></span>
3. <span data-ttu-id="598a1-116">Если конкретный workflow-процесс должен обрабатывать номенклатуры строк, которые соответствуют определенному набору условий, нажмите **Вызывать workflow-процесс для каждой строки номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="598a1-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="598a1-117">Затем выполните следующие действия для определения набора условий:</span><span class="sxs-lookup"><span data-stu-id="598a1-117">Then follow these steps to define the set of conditions:</span></span>

    1. <span data-ttu-id="598a1-118">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="598a1-118">Click **Add**.</span></span>
    2. <span data-ttu-id="598a1-119">Выберите условие в таблице.</span><span class="sxs-lookup"><span data-stu-id="598a1-119">Select the condition in the table.</span></span>
    3. <span data-ttu-id="598a1-120">На вкладке **Наименование условия** введите имя набора условий, который вы определяете.</span><span class="sxs-lookup"><span data-stu-id="598a1-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4. <span data-ttu-id="598a1-121">Щелкните **Добавить условие**, чтобы ввести условие.</span><span class="sxs-lookup"><span data-stu-id="598a1-121">Click **Add condition** to enter a condition.</span></span>
    5. <span data-ttu-id="598a1-122">Введите все необходимые дополнительные условия.</span><span class="sxs-lookup"><span data-stu-id="598a1-122">Enter any additional conditions that are required.</span></span>
    6. <span data-ttu-id="598a1-123">Чтобы проверить, что введенный набор условий настроен верно, нажмите **Проверка**.</span><span class="sxs-lookup"><span data-stu-id="598a1-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="598a1-124">На странице **Проверить условие workflow-процесса** в области **Проверить условие** выберите запись и щелкните **Проверка**.</span><span class="sxs-lookup"><span data-stu-id="598a1-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="598a1-125">Система оценит запись и определит, соответствует ли она определенным вами условиям.</span><span class="sxs-lookup"><span data-stu-id="598a1-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="598a1-126">Нажмите кнопку **OK** или **Отмена** для возврата на страницу **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="598a1-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="598a1-127">На вкладке **Workflow-процесс** выберите workflow-процесс, который будет использоваться для обработки номенклатур строк, которые соответствуют определенным вами условиям.</span><span class="sxs-lookup"><span data-stu-id="598a1-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]