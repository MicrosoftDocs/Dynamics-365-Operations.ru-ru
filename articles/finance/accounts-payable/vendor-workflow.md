---
title: Workflow-процесс поставщика
description: Изменение информации о поставщике и использование workflow-процесса для ее утверждения.
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: afda0ead11ec1adac2d436511eef8165a7f0aed2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189277"
---
# <a name="vendor-workflow"></a><span data-ttu-id="d9df5-103">Workflow-процесс поставщика</span><span class="sxs-lookup"><span data-stu-id="d9df5-103">Vendor workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9df5-104">При использовании workflow-процесса поставщика изменения, вносимые в конкретные поля, отправляются в workflow-процесс на утверждение, прежде чем они будут добавлены в запись поставщика.</span><span class="sxs-lookup"><span data-stu-id="d9df5-104">When the vendor workflow is used, changes that are made to specific fields are sent to the workflow for approval before they are added to the vendor.</span></span>

## <a name="set-up-the-vendor-workflow"></a><span data-ttu-id="d9df5-105">Настройка workflow-процесса поставщика</span><span class="sxs-lookup"><span data-stu-id="d9df5-105">Set up the vendor workflow</span></span>

<span data-ttu-id="d9df5-106">Перед использованием функции workflow-процесса необходимо ее активировать.</span><span class="sxs-lookup"><span data-stu-id="d9df5-106">Before you can use the workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="d9df5-107">Перейдите в раздел **Расчеты с поставщиками \> Настройка \> Параметры расчетов с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="d9df5-107">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="d9df5-108">На вкладке **Общее** на экспресс-вкладке **Утверждение поставщика** установите параметр **Включить утверждения поставщика** в значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="d9df5-108">On the **General** tab, on the **Vendor approval** FastTab, set the **Enable vendor approvals** option to **Yes**.</span></span>
3. <span data-ttu-id="d9df5-109">В поле **Поведение информационного объекта** выберите поведение, которое должно использоваться при импорте данных:</span><span class="sxs-lookup"><span data-stu-id="d9df5-109">In the **Data entity behavior** field, select the behavior that should be used when data is imported:</span></span>

    - <span data-ttu-id="d9df5-110">**Разрешить изменения без утверждения** — информационный объект может обновить запись поставщика без ее обработки workflow-процессом.</span><span class="sxs-lookup"><span data-stu-id="d9df5-110">**Allow changes without approval** – The data entity can update the vendor record without processing it through the workflow.</span></span>
    - <span data-ttu-id="d9df5-111">**Отклонить изменения** — вносить изменения в запись поставщика невозможно.</span><span class="sxs-lookup"><span data-stu-id="d9df5-111">**Reject changes** – Changes can't be made to the vendor record.</span></span> <span data-ttu-id="d9df5-112">Для полей, для которых включен workflow-процесс, импорт завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d9df5-112">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="d9df5-113">**Создать предложения изменений** — все поля будут изменены, кроме полей, для которых включен workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="d9df5-113">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="d9df5-114">Новые значения для этих полей будут добавлены в запись поставщика в качестве предлагаемых изменений, и workflow-процесс запустится автоматически.</span><span class="sxs-lookup"><span data-stu-id="d9df5-114">The new values for those fields will be added to the vendor as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="d9df5-115">В списке полей поставщика установите флажок **Включить** для каждого поля, которое должно быть утверждено, прежде чем изменения смогут быть внесены.</span><span class="sxs-lookup"><span data-stu-id="d9df5-115">In the list of vendor fields, select the **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="d9df5-116">Перейдите в раздел **Расчеты с поставщиками \> Настройка \> Workflow-процессы для расчетов с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="d9df5-116">Go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
6. <span data-ttu-id="d9df5-117">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d9df5-117">Select **New**.</span></span>
7. <span data-ttu-id="d9df5-118">Выберите **Workflow-процесс предлагаемых изменений поставщика**.</span><span class="sxs-lookup"><span data-stu-id="d9df5-118">Select **Proposed vendor changes workflow**.</span></span> 
8. <span data-ttu-id="d9df5-119">Настройте workflow-процесс, чтобы он соответствовал вашему процессу утверждения.</span><span class="sxs-lookup"><span data-stu-id="d9df5-119">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="d9df5-120">Элемент утверждения workflow-процесса **Утверждение workflow-процесса для предлагаемого изменения поставщика** будет применять изменения к записи поставщика.</span><span class="sxs-lookup"><span data-stu-id="d9df5-120">The **Workflow approval for proposed vendor change** workflow approval element will apply the changes to the vendor.</span></span>

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="d9df5-121">Изменение информации о поставщике и отправка изменений в workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="d9df5-121">Change vendor information and submit the changes to the workflow</span></span>

<span data-ttu-id="d9df5-122">При изменении поля, для которого включен workflow-процесс, появляется страница **Предлагаемые изменения**.</span><span class="sxs-lookup"><span data-stu-id="d9df5-122">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="d9df5-123">На этой странице отображается исходное значение поля и новое введенное значение.</span><span class="sxs-lookup"><span data-stu-id="d9df5-123">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="d9df5-124">Поле, которое вы изменили, возвращается к своему исходному значению.</span><span class="sxs-lookup"><span data-stu-id="d9df5-124">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="d9df5-125">Кроме того, появляется сообщение о состоянии о том, что ваши изменения не отправлены.</span><span class="sxs-lookup"><span data-stu-id="d9df5-125">A status message also informs you that your changes haven't been submitted.</span></span> 

<span data-ttu-id="d9df5-126">Каждый раз, когда вы изменяете поле, для которого включен workflow-процесс, это поле добавляется в список на странице **Предлагаемые изменения**.</span><span class="sxs-lookup"><span data-stu-id="d9df5-126">Every time that you change a field that is enabled for the workflow, that field is added to the list on the **Proposed changes** page.</span></span> <span data-ttu-id="d9df5-127">Чтобы отказаться от предлагаемого значения для поля, нажмите кнопку **Отменить** рядом с полем в списке.</span><span class="sxs-lookup"><span data-stu-id="d9df5-127">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="d9df5-128">Чтобы отменить все изменения, нажмите кнопку **Отменить все изменения** внизу страницы.</span><span class="sxs-lookup"><span data-stu-id="d9df5-128">To discard all changes, use the **Discard all changes** button at the bottom of the page.</span></span> <span data-ttu-id="d9df5-129">Нажмите кнопку **OK**, чтобы закрыть страницу.</span><span class="sxs-lookup"><span data-stu-id="d9df5-129">Select **OK** to close the page.</span></span>

<span data-ttu-id="d9df5-130">Когда у вас будет хотя бы одно предложенное изменение, в области действий появятся две дополнительные вкладки: **Предлагаемые изменения** и **Workflow-процесс**.</span><span class="sxs-lookup"><span data-stu-id="d9df5-130">After you have at least one proposed change, two additional tabs appear on the action pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="d9df5-131">Выберите **Предлагаемые изменения**, чтобы открыть страницу **Предлагаемые изменения** и просмотреть изменения.</span><span class="sxs-lookup"><span data-stu-id="d9df5-131">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="d9df5-132">Выберите **Workflow-процесс \> Отправить**, чтобы отправить изменения в workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="d9df5-132">Select **Workflow \> Submit to submit the changes to workflow**.</span></span>

    <span data-ttu-id="d9df5-133">Статус на странице изменится на **Изменения, ожидающие утверждения**.</span><span class="sxs-lookup"><span data-stu-id="d9df5-133">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="d9df5-134">Бизнес-правило следует стандартному процессу бизнес-правила.</span><span class="sxs-lookup"><span data-stu-id="d9df5-134">The workflow follows the standard workflow process.</span></span> <span data-ttu-id="d9df5-135">Утверждающее лицо направляется на страницу **Поставщик**, где может просмотреть изменения на странице **Предлагаемые изменения** странице, а затем выбрать **Workflow-процесс \> Утвердить**, чтобы утвердить workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="d9df5-135">The approver is directed to the **Vendor** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="d9df5-136">По завершении всех утверждений поля будут обновлены для отображения предложенных значений.</span><span class="sxs-lookup"><span data-stu-id="d9df5-136">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
