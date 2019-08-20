---
title: Обновление статуса канбана
description: Если канбан освобождается по ошибке или полученный канбан требуется освободить, необходимо обновить статус канбана.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97b6eea4e93967dbe1eea5eac9fe3fbf6b336a49
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838471"
---
# <a name="update-kanban-status"></a><span data-ttu-id="afbee-103">Обновление статуса канбана</span><span class="sxs-lookup"><span data-stu-id="afbee-103">Update kanban status</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="afbee-104">Если канбан освобождается по ошибке или полученный канбан требуется освободить, необходимо обновить статус канбана.</span><span class="sxs-lookup"><span data-stu-id="afbee-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="afbee-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="afbee-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="afbee-106">Эта процедура предназначена для начальника цеха.</span><span class="sxs-lookup"><span data-stu-id="afbee-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="afbee-107">Найдите канбан.</span><span class="sxs-lookup"><span data-stu-id="afbee-107">Find the kanban.</span></span>
1. <span data-ttu-id="afbee-108">Перейдите в раздел "Управление производством" > "Канбан" > "Канбаны".</span><span class="sxs-lookup"><span data-stu-id="afbee-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="afbee-109">Откройте фильтр столбца статуса единицы обработки.</span><span class="sxs-lookup"><span data-stu-id="afbee-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="afbee-110">Щелкните "Очистить".</span><span class="sxs-lookup"><span data-stu-id="afbee-110">Click Clear.</span></span>
    * <span data-ttu-id="afbee-111">Это приведет к сбросу фильтров.</span><span class="sxs-lookup"><span data-stu-id="afbee-111">This resets the filters.</span></span>  
4. <span data-ttu-id="afbee-112">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="afbee-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="afbee-113">Например, отфильтруйте поле "Номер карты" по значению "000149".</span><span class="sxs-lookup"><span data-stu-id="afbee-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="afbee-114">Изменение статуса "Освобождено" на "Получено"</span><span class="sxs-lookup"><span data-stu-id="afbee-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="afbee-115">Щелкните "Обращение пустой единицы обработки".</span><span class="sxs-lookup"><span data-stu-id="afbee-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="afbee-116">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="afbee-116">Click OK.</span></span>
    * <span data-ttu-id="afbee-117">Обратите внимание, что единица обработки имеет статус "Получено".</span><span class="sxs-lookup"><span data-stu-id="afbee-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="afbee-118">Изменение статуса "Получено" на "Освобождено"</span><span class="sxs-lookup"><span data-stu-id="afbee-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="afbee-119">Щелкните "Пустой канбан".</span><span class="sxs-lookup"><span data-stu-id="afbee-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="afbee-120">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="afbee-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="afbee-121">Обратите внимание, что единица обработки имеет статус "Освобождено".</span><span class="sxs-lookup"><span data-stu-id="afbee-121">Notice that the Handling unit status is Emptied.</span></span>  

