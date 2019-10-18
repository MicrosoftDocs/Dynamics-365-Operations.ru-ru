---
title: Бизнес-правило клиента
description: В этом разделе приводятся сведения о бизнес-правиле клиента. Измените отдельные поля для клиента и отправьте эти изменения на утверждение с помощью бизнес-правила, чтобы они были добавлены к клиенту.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 8ff91a1df82d6195da266b97c347ef27afec662d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176071"
---
# <a name="customer-workflow"></a><span data-ttu-id="8bc46-104">Бизнес-правило клиента</span><span class="sxs-lookup"><span data-stu-id="8bc46-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8bc46-105">В версии 8.0.4 появилось бизнес-правило клиента.</span><span class="sxs-lookup"><span data-stu-id="8bc46-105">The customer workflow has been added to version 8.0.4.</span></span> <span data-ttu-id="8bc46-106">Можно изменить отдельные поля для клиента и отправить эти изменения на утверждение с помощью бизнес-правила, чтобы они были добавлены к клиенту.</span><span class="sxs-lookup"><span data-stu-id="8bc46-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="8bc46-107">Настройка бизнес-правила клиента</span><span class="sxs-lookup"><span data-stu-id="8bc46-107">Set up the customer workflow</span></span>

<span data-ttu-id="8bc46-108">Прежде чем использовать функцию бизнес-правила клиента, необходимо включить ее.</span><span class="sxs-lookup"><span data-stu-id="8bc46-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="8bc46-109">Перейдите в раздел **Расчеты с клиентами \> Настройка \> Параметры модуля расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="8bc46-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="8bc46-110">На вкладке **Общие** на экспресс-вкладке **Утверждение клиентом** задайте для параметра **Включить утверждения клиентом** значение **Да**, чтобы включить функцию.</span><span class="sxs-lookup"><span data-stu-id="8bc46-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="8bc46-111">В поле **Поведение информационного объекта** выберите поведение для информационного объекта при импорте данных:</span><span class="sxs-lookup"><span data-stu-id="8bc46-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="8bc46-112">**Разрешить изменения без утверждения** — объект может обновить запись клиента без обработки в бизнес-правиле.</span><span class="sxs-lookup"><span data-stu-id="8bc46-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="8bc46-113">**Отклонить изменения** — невозможно вносить изменения в запись клиента.</span><span class="sxs-lookup"><span data-stu-id="8bc46-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="8bc46-114">Импорт завершится с ошибкой для полей, которые включены для этого бизнес-правила.</span><span class="sxs-lookup"><span data-stu-id="8bc46-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="8bc46-115">**Создать предложения изменений** — будут изменены все поля за исключением полей, которые включены для бизнес-правила.</span><span class="sxs-lookup"><span data-stu-id="8bc46-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="8bc46-116">Новые значения этих полей будут добавлены к клиенту как предложенные изменения, и бизнес-правило запустится автоматически.</span><span class="sxs-lookup"><span data-stu-id="8bc46-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="8bc46-117">В списке полей клиента установите флажок **Включить** для каждого поля, которое должно быть утверждено, прежде чем можно будет внести изменения.</span><span class="sxs-lookup"><span data-stu-id="8bc46-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="8bc46-118">Перейдите в раздел **Расчеты с клиентами \> Настройка \> Бизнес-правила расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="8bc46-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="8bc46-119">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="8bc46-119">Select **New**.</span></span>
7. <span data-ttu-id="8bc46-120">Выберите **Бизнес-правило предлагаемых изменений клиента**.</span><span class="sxs-lookup"><span data-stu-id="8bc46-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="8bc46-121">Настройте бизнес-правило, чтобы оно соответствовало процессу утверждения.</span><span class="sxs-lookup"><span data-stu-id="8bc46-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="8bc46-122">Элемент утверждения бизнес-правила **Утверждение бизнес-правила для предлагаемого изменения клиента** применит изменения к клиенту.</span><span class="sxs-lookup"><span data-stu-id="8bc46-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="8bc46-123">Изменение информации по клиенту и отправка изменений в бизнес-правило</span><span class="sxs-lookup"><span data-stu-id="8bc46-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="8bc46-124">При изменении поля, включенного для бизнес-правила, отобразится страница **Предлагаемые изменения**.</span><span class="sxs-lookup"><span data-stu-id="8bc46-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="8bc46-125">На этой странице отображается исходное значение поля и новое введенное значение.</span><span class="sxs-lookup"><span data-stu-id="8bc46-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="8bc46-126">Поле, которое вы изменили, вернется к исходному значению.</span><span class="sxs-lookup"><span data-stu-id="8bc46-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="8bc46-127">Сообщение о статусе на странице информирует о том, что изменения не были отправлены.</span><span class="sxs-lookup"><span data-stu-id="8bc46-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="8bc46-128">При каждом изменении поля, включенного для бизнес-правила, это поле добавляется в список предлагаемых изменений.</span><span class="sxs-lookup"><span data-stu-id="8bc46-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="8bc46-129">Чтобы отменить предлагаемое значение для поля, нажмите кнопку **Отменить** рядом с полем в списке.</span><span class="sxs-lookup"><span data-stu-id="8bc46-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="8bc46-130">Чтобы отменить все изменения, нажмите кнопку **Отменить все изменения** в нижней части страницы.</span><span class="sxs-lookup"><span data-stu-id="8bc46-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="8bc46-131">Нажмите кнопку **ОК**, чтобы закрыть страницу.</span><span class="sxs-lookup"><span data-stu-id="8bc46-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="8bc46-132">Если у вас есть хотя бы одно предлагаемое изменение, откроется два дополнительных меню в области действий: **Предлагаемые изменения** и **Бизнес-правило**.</span><span class="sxs-lookup"><span data-stu-id="8bc46-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="8bc46-133">Выберите **Предлагаемые изменения**, чтобы открыть страницу **Предлагаемые изменения** и просмотреть изменения.</span><span class="sxs-lookup"><span data-stu-id="8bc46-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="8bc46-134">Выберите **Бизнес-правило \> Отправить**, чтобы отправить изменения в бизнес-правило.</span><span class="sxs-lookup"><span data-stu-id="8bc46-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="8bc46-135">Статус на странице изменится на **Изменения, ожидающие утверждения**.</span><span class="sxs-lookup"><span data-stu-id="8bc46-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="8bc46-136">Бизнес-правило следует стандартному процессу бизнес-правила в приложении.</span><span class="sxs-lookup"><span data-stu-id="8bc46-136">The workflow follows the standard workflow process in the application.</span></span> <span data-ttu-id="8bc46-137">Утверждающее лицо будет направлено на страницу **Клиент**, на которой оно может просмотреть изменения на странице **Предлагаемые изменения** и выбрать **Бизнес-правило \> Утвердить** для утверждения бизнес-правила.</span><span class="sxs-lookup"><span data-stu-id="8bc46-137">The approver is directed to the **Customer** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="8bc46-138">По завершении всех утверждений поля будут обновлены для отображения предложенных значений.</span><span class="sxs-lookup"><span data-stu-id="8bc46-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>