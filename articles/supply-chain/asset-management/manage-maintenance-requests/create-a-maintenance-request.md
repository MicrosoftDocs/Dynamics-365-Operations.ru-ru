---
title: Создание запросов на обслуживание
description: В этом разделе объясняется, как создавать запросы на обслуживание в управлении активами.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 147388d5052bd14851bbddfbb7fe25297a43f104
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102982"
---
# <a name="create-maintenance-requests"></a><span data-ttu-id="b3db8-103">Создание запросов на обслуживание</span><span class="sxs-lookup"><span data-stu-id="b3db8-103">Create maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b3db8-104">Запросы на техническое обслуживание могут быть использованы, если обслуживающий персонал или производственные работники обнаружили, что оборудование требует ремонта, но ремонтные работы не могут быть выполнены сразу.</span><span class="sxs-lookup"><span data-stu-id="b3db8-104">Maintenance requests can be used if maintenance workers or production workers discover that equipment requires repair, but the repair job can't be done right away.</span></span>

<span data-ttu-id="b3db8-105">**Пример.** Когда специалист по обслуживанию производит ремонт, он обнаруживает, что другой актив в том же месте требует обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b3db8-105">**Example:** While a maintenance worker is making a repair, they discover that another asset at the same location must be serviced.</span></span> <span data-ttu-id="b3db8-106">Тем не менее, специалист по обслуживанию не имеет времени или необходимых запасных частей, чтобы сделать ремонт.</span><span class="sxs-lookup"><span data-stu-id="b3db8-106">However, the maintenance worker doesn't have the time or the required spare parts to do the repair job.</span></span> <span data-ttu-id="b3db8-107">Поэтому он создает запрос на обслуживание актива и вводит краткое описание проблемы.</span><span class="sxs-lookup"><span data-stu-id="b3db8-107">Therefore, they create a maintenance request on the asset and enters a short description of the issue.</span></span>

<span data-ttu-id="b3db8-108">Раздел **Активные запросы на обслуживание** на панели **Связанные сведения** с правой стороны страницы **Все активы** или **Активные активы** (**Управление активами** \> **Общее** \> **Активы** \> **Все активы** или **Активные активы**) показывает активные запросы на техническое обслуживание, которые прилагаются к выбранному активу.</span><span class="sxs-lookup"><span data-stu-id="b3db8-108">The **Active maintenance requests** section of the **Related information** pane on the right side of the **All assets** or **Active assets** page (**Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**) shows the active maintenance requests that are attached to the selected asset.</span></span>

1. <span data-ttu-id="b3db8-109">Выберите **Управление активами** \> **Общее** \> **Запросы на обслуживание** \> **Все запросы на обслуживание** или **Активные запросы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="b3db8-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="b3db8-110">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b3db8-110">Select **New**.</span></span>
3. <span data-ttu-id="b3db8-111">В диалоговом окне **Создать запрос** в поле **Типа запроса на обслуживание** выберите тип запроса на техническое обслуживание.</span><span class="sxs-lookup"><span data-stu-id="b3db8-111">In the **Create request** dialog box, in the **Maintenance request type** field, select the type of maintenance request.</span></span> <span data-ttu-id="b3db8-112">Предлагается тип по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b3db8-112">A default type is suggested.</span></span>
4. <span data-ttu-id="b3db8-113">В поле **Описание** введите имя или название, кратко описывающее запрос на техническое обслуживание.</span><span class="sxs-lookup"><span data-stu-id="b3db8-113">In the **Description** field, enter a name or title that briefly describes the maintenance request.</span></span>
5. <span data-ttu-id="b3db8-114">В полях **Функциональное местоположение** и **Актив** выберите функциональное местоположение или актив либо комбинацию функционального местоположения и актива, как вам требуется.</span><span class="sxs-lookup"><span data-stu-id="b3db8-114">In the **Functional location** and **Asset** fields, select a functional location or an asset, or a combination of a functional location and an asset, as you require.</span></span> <span data-ttu-id="b3db8-115">Вы можете создать запрос на техническое обслуживание без выбора актива, и актив может быть добавлен в запрос на обслуживание позже.</span><span class="sxs-lookup"><span data-stu-id="b3db8-115">You can create a maintenance request without selecting an asset, and the asset can be added to the maintenance request later.</span></span> <span data-ttu-id="b3db8-116">Если специалист по обслуживанию, выполнивший вход, связан с ресурсом, связанным с активом, поле **Актив** автоматически устанавливается.</span><span class="sxs-lookup"><span data-stu-id="b3db8-116">If the maintenance worker who is signed in is related to a resource that is related to an asset, the **Asset** field is automatically set.</span></span>

    <span data-ttu-id="b3db8-117">Если запрос на техническое обслуживание уже присоединен к выбранному активу, в верхней части диалогового окна **Создать запрос** появляется панель сообщений, чтобы уведомить вас об идентификаторе существующего запроса на техническое обслуживание.</span><span class="sxs-lookup"><span data-stu-id="b3db8-117">If a maintenance request is already attached to the selected asset, a message bar appears at the top of the **Create request** dialog box to notify you about the ID of the existing maintenance request.</span></span> <span data-ttu-id="b3db8-118">Панель сообщений также уведомляет, если актив покрывается гарантийным соглашением.</span><span class="sxs-lookup"><span data-stu-id="b3db8-118">A message bar also notifies you if the asset is covered by a warranty agreement.</span></span>

6. <span data-ttu-id="b3db8-119">В поле **Уровень обслуживания** выберите уровень обслуживания, указывающий на срочность запроса.</span><span class="sxs-lookup"><span data-stu-id="b3db8-119">In the **Service level** field, select a service level that indicates the urgency of the request.</span></span>
7. <span data-ttu-id="b3db8-120">Если выбран актив в шаге 5, можно использовать поля **Симптом неисправности**, **Область неисправности** и **Тип неисправности** для создания регистрации неисправности.</span><span class="sxs-lookup"><span data-stu-id="b3db8-120">If you selected an asset in step 5, you can use the **Fault symptom**, **Fault area**, and **Fault type** fields to create a fault registration.</span></span>
8. <span data-ttu-id="b3db8-121">Если запрос на техническое обслуживание вызвал простой из-за обслуживания, введите дату начала и время простоя.</span><span class="sxs-lookup"><span data-stu-id="b3db8-121">If the maintenance request has caused maintenance downtime, enter the start date and time of the downtime.</span></span>

    <span data-ttu-id="b3db8-122">В поле **Кем начато** автоматически устанавливается ваше имя.</span><span class="sxs-lookup"><span data-stu-id="b3db8-122">The **Started by** field is automatically set to your name.</span></span>

10. <span data-ttu-id="b3db8-123">В поле **Фактическое начало** автоматически задаются текущая дата и время.</span><span class="sxs-lookup"><span data-stu-id="b3db8-123">The **Actual start** field is automatically set to the current date and time.</span></span> <span data-ttu-id="b3db8-124">Однако если требуется, это значение можно изменить.</span><span class="sxs-lookup"><span data-stu-id="b3db8-124">However, you can change the value as you require.</span></span>
11. <span data-ttu-id="b3db8-125">В поле **Примечания** введите все необходимые дополнительные заметки.</span><span class="sxs-lookup"><span data-stu-id="b3db8-125">In the **Notes** field, enter any additional notes that are required.</span></span>
12. <span data-ttu-id="b3db8-126">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b3db8-126">Select **OK**.</span></span>

![Создание запроса на обслуживание](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a><span data-ttu-id="b3db8-128">Последующая обработка запросов на техническое обслуживание</span><span class="sxs-lookup"><span data-stu-id="b3db8-128">Subsequent processing of maintenance requests</span></span>

<span data-ttu-id="b3db8-129">После создания запроса на техническое обслуживание, но прежде чем он будет преобразован в рабочий заказ, в нем должна быть обновлена различная информация.</span><span class="sxs-lookup"><span data-stu-id="b3db8-129">After a maintenance request is created, but before it's converted to a work order, various information should be updated on it.</span></span> <span data-ttu-id="b3db8-130">Как правило, планировщик или другой административный сотрудник выполняет эту задачу.</span><span class="sxs-lookup"><span data-stu-id="b3db8-130">Typically, a planner or another administrative employee completes this task.</span></span>

- <span data-ttu-id="b3db8-131">На странице **Все запросы на обслуживание** или **Активные запросы на обслуживание** выберите запрос, с которым требуется работать, затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="b3db8-131">On the **All maintenance requests** or **Active maintenance requests** page, select the request to work with, and then select **Edit**.</span></span>

<span data-ttu-id="b3db8-132">В подробном представлении можно обновить различную информацию.</span><span class="sxs-lookup"><span data-stu-id="b3db8-132">In the details view, you can update various information.</span></span> <span data-ttu-id="b3db8-133">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="b3db8-133">Here are some examples:</span></span>

- <span data-ttu-id="b3db8-134">Выберите и проверьте актив.</span><span class="sxs-lookup"><span data-stu-id="b3db8-134">Select and verify the asset.</span></span> <span data-ttu-id="b3db8-135">Если вы должны выбрать другой актив позже, можно установить для параметра **Актив проверен** значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="b3db8-135">If you must select a different asset later, you can set the **Asset verified** option to **No**.</span></span>
- <span data-ttu-id="b3db8-136">Выберите группу ответственных специалистов по обслуживанию и/или ответственного специалиста по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="b3db8-136">Select a responsible maintenance worker group and/or a responsible maintenance worker.</span></span> <span data-ttu-id="b3db8-137">Дополнительные сведения о необходимой настройке см. в разделе [Ответственные специалисты по обслуживанию](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="b3db8-137">For more information about the required setup, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>
- <span data-ttu-id="b3db8-138">Выберите тип задания на обслуживание и, если эта информация актуальна, связанный вариант работы по техническому обслуживанию и предложение работы.</span><span class="sxs-lookup"><span data-stu-id="b3db8-138">Select a maintenance job type and, if this information is relevant, a related maintenance job variant and a job trade.</span></span>
- <span data-ttu-id="b3db8-139">В полях **Широта** и **Долгота** введите географические координаты.</span><span class="sxs-lookup"><span data-stu-id="b3db8-139">In the **Latitude** and **Longitude** fields, enter geographic coordinates.</span></span> <span data-ttu-id="b3db8-140">Любые координаты, добавленные в запрос на техническое обслуживание, автоматически переносятся в соответствующий заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="b3db8-140">Any coordinates that are added to a maintenance request are automatically transferred to a related work order.</span></span> 

![Обновление запроса на обслуживание](media/04-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="b3db8-142">Если выбран актив при создании запроса на техническое обслуживание, можно добавить одну неисправность в активе.</span><span class="sxs-lookup"><span data-stu-id="b3db8-142">If you select an asset when you create a maintenance request, you can add one fault to the asset.</span></span> <span data-ttu-id="b3db8-143">После того, как запрос на техническое обслуживание был создан, при необходимости можно добавить больше неисправностей.</span><span class="sxs-lookup"><span data-stu-id="b3db8-143">After the maintenance request has been created, you can add more faults, as you require.</span></span> <span data-ttu-id="b3db8-144">Чтобы добавить неисправности, выберите **Неисправность актива** на странице **Все запросы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="b3db8-144">To add faults, select **Asset fault** on the **All maintenance requests** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]