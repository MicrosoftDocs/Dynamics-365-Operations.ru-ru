---
title: Ответственные специалисты по обслуживанию
description: В этом разделе описан порядок настройки ответственных специалистов по обслуживанию в «Управлении активами».
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63f436ffd01ac56bb4bc0021e226dad46d7c3377
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569923"
---
# <a name="responsible-maintenance-workers"></a><span data-ttu-id="40e91-103">Ответственные специалисты по обслуживанию</span><span class="sxs-lookup"><span data-stu-id="40e91-103">Responsible maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="40e91-104">Ответственные специалисты по обслуживанию могут быть связаны с типами активов, активами, функциональными местоположениями, категориями типов заданий обслуживания, типами заданий обслуживания, вариантами типов заданий обслуживания и сделками.</span><span class="sxs-lookup"><span data-stu-id="40e91-104">Responsible maintenance workers can be related to asset types, assets, functional locations, maintenance job type categories, maintenance job types, maintenance job type variants, and trades.</span></span> <span data-ttu-id="40e91-105">Они могут быть использованы в заказах на работу и запросах на обслуживание, чтобы указать предпочтение в отношении специалиста по обслуживанию, который должен нести ответственность за заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="40e91-105">They can be used on work orders and maintenance requests to indicate a preference about the maintenance workers who should be responsible for a work order.</span></span> <span data-ttu-id="40e91-106">(Однако эти специалисты по обслуживанию не обязательно являются теми же работниками, которые должны выполнять заказ на работу). Использование этой функциональности является необязательным.</span><span class="sxs-lookup"><span data-stu-id="40e91-106">(However, those maintenance workers aren't necessarily the same workers who are scheduled to carry out the work order.) Use of this functionality is optional.</span></span> <span data-ttu-id="40e91-107">Например, она может использоваться для выбора ответственных работников или групп работников для конкретных типов работ или рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="40e91-107">For example, it can be used to select responsible workers or worker groups for specific work types or work areas.</span></span>

<span data-ttu-id="40e91-108">Во время жизненного цикла заказа на работу или жизненного цикла запроса на обслуживание ответственные специалисты по обслуживанию могут быть изменены или обновлены.</span><span class="sxs-lookup"><span data-stu-id="40e91-108">During a work order lifecycle or a maintenance request lifecycle, responsible maintenance workers can be changed or updated.</span></span> <span data-ttu-id="40e91-109">Это изменение или обновление может быть связано, например, с изменением состояния жизненного цикла запроса на обслуживание или состоянием жизненного цикла заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="40e91-109">This change or update might be related to, for example, a change in the maintenance request lifecycle state or the work order lifecycle state.</span></span>

<span data-ttu-id="40e91-110">Настройка на странице **Ответственные специалисты по обслуживанию** *не* используется при планировании заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="40e91-110">The setup on the **Responsible maintenance workers** page is *not* used during work order scheduling.</span></span>

> [!NOTE]
> <span data-ttu-id="40e91-111">В «Управлении активами» можно также настроить *предпочтительных* специалистов по обслуживанию, которые могут быть выделены для заказов на работу во время планирования заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="40e91-111">In Asset Management, you can also set up *preferred* maintenance workers who might be allocated to work orders during work order scheduling.</span></span>

<span data-ttu-id="40e91-112">Прежде чем вы сможете настроить ответственных специалистов по обслуживанию, необходимо настроить специалистов и группы специалистов по обслуживанию, которые должны быть доступны для выбора.</span><span class="sxs-lookup"><span data-stu-id="40e91-112">Before you can set up responsible maintenance workers, you must set up the workers and maintenance worker groups that should be available for selection.</span></span> <span data-ttu-id="40e91-113">Для получения информации о том, как настроить специалистов и группы специалистов по обслуживанию, см. в разделе [Специалисты и группы специалистов по обслуживанию](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="40e91-113">For information about how to set up workers and maintenance worker groups, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-responsible-maintenance-workers"></a><span data-ttu-id="40e91-114">Настройка ответственных специалистов по обслуживанию</span><span class="sxs-lookup"><span data-stu-id="40e91-114">Set up responsible maintenance workers</span></span>

1. <span data-ttu-id="40e91-115">Выберите **Управление активами** \> **Настройка** \> **Работники** \> **Ответственные специалисты по обслуживанию**.</span><span class="sxs-lookup"><span data-stu-id="40e91-115">Select **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span></span>
2. <span data-ttu-id="40e91-116">Выберите **Создать**, чтобы создать запись.</span><span class="sxs-lookup"><span data-stu-id="40e91-116">Select **New** to create a record.</span></span>
3. <span data-ttu-id="40e91-117">Сначала создайте ответственного специалиста по обслуживанию по умолчанию или настройку группы ответственных специалистов по обслуживанию, где вы задаете только поле **Группа ответственных специалистов по обслуживанию** и/или поле **Ответственный специалист по обслуживанию**.</span><span class="sxs-lookup"><span data-stu-id="40e91-117">First create a default responsible maintenance worker or responsible maintenance worker group setup, where you set only the **Responsible maintenance worker group** field and/or the **Responsible worker** field.</span></span> <span data-ttu-id="40e91-118">Оставьте оставшиеся поля пустыми.</span><span class="sxs-lookup"><span data-stu-id="40e91-118">Leave the remaining fields blank.</span></span> <span data-ttu-id="40e91-119">Эта настройка по умолчанию будет использоваться при планировании заказа на работу, если никакая другая, более конкретная комбинация не соответствует содержимому заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="40e91-119">This default setup will be used during work order scheduling if no other, more specific combination matches the contents of the work order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="40e91-120">При создании запроса на обслуживание, когда ответственный специалист по обслуживанию или группа ответственных специалистов по обслуживанию доступны для выбора на странице **Все запросы на обслуживание**, «Управление активами» проходит через все записи ответственных специалистов по обслуживанию для проверки на возможное совпадение.</span><span class="sxs-lookup"><span data-stu-id="40e91-120">During creation of a maintenance request, when a responsible maintenance worker or responsible maintenance worker group is made available for selection on the **All maintenance requests** page, Asset Management goes through all responsible maintenance worker records to check for a possible match.</span></span> <span data-ttu-id="40e91-121">Она всегда проверяет наиболее конкретные комбинации в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="40e91-121">It always checks the most specific combination first.</span></span> <span data-ttu-id="40e91-122">Другими словами, «Управление активами» сначала проверяет соответствие для поля **Торговля**.</span><span class="sxs-lookup"><span data-stu-id="40e91-122">In other words, Asset Management first checks for a match for the **Trade** field.</span></span> <span data-ttu-id="40e91-123">Если совпадение не найдено, оно проверяет соответствие для поля **Вариант типа задания обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="40e91-123">If no match is found, it checks for a match for the **Maintenance job type variant** field.</span></span> <span data-ttu-id="40e91-124">Если совпадение не найдено, оно проверяет соответствие для поля **Тип задания обслуживания** и т.д.</span><span class="sxs-lookup"><span data-stu-id="40e91-124">If no match is found, it checks for a match for the **Maintenance job type** field, and so on.</span></span> <span data-ttu-id="40e91-125">Как вы можете видеть в макете страницы, это поведение означает, что, чтобы найти наиболее конкретную комбинацию, «Управление активами» проверяет каждую запись справа налево на совпадение (сначала **Торговля**, затем **Вариант типа задания обслуживания**, затем **Тип задания обслуживания**, затем **Категория типа задания обслуживания**, затем **Функциональное местоположение**, затем **Актив**, и наконец **Тип актива**).</span><span class="sxs-lookup"><span data-stu-id="40e91-125">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match (first **Trade**, then **Maintenance job type variant**, then **Maintenance job type**, then **Maintenance job type category**, then **Functional location**, then **Asset**, and finally **Asset type**).</span></span> <span data-ttu-id="40e91-126">Если совпадение не найдено, используется запись по умолчанию, которая не имеет выбора в этих семи полях.</span><span class="sxs-lookup"><span data-stu-id="40e91-126">If no match is found, the default record that has no selections in those seven fields is used.</span></span>

<span data-ttu-id="40e91-127">На следующем рисунке показан пример страницы **Ответственные специалисты по обслуживанию**.</span><span class="sxs-lookup"><span data-stu-id="40e91-127">The following illustration shows an example of the **Responsible maintenance workers** page.</span></span>

![Страница ответственных специалистов по обслуживанию](media/08-setup-for-requests.png)
