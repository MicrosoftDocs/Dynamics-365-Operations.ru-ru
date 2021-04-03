---
title: Обновление статуса канбана
description: Если канбан освобождается по ошибке или полученный канбан требуется освободить, необходимо обновить статус канбана.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 055765452579b1de74f1c2158de9c6cb4ee80f16
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252830"
---
# <a name="update-kanban-status"></a><span data-ttu-id="a36f3-103">Обновление статуса канбана</span><span class="sxs-lookup"><span data-stu-id="a36f3-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a36f3-104">Если канбан освобождается по ошибке или полученный канбан требуется освободить, необходимо обновить статус канбана.</span><span class="sxs-lookup"><span data-stu-id="a36f3-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="a36f3-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="a36f3-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a36f3-106">Эта процедура предназначена для начальника цеха.</span><span class="sxs-lookup"><span data-stu-id="a36f3-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="a36f3-107">Найдите канбан.</span><span class="sxs-lookup"><span data-stu-id="a36f3-107">Find the kanban.</span></span>
1. <span data-ttu-id="a36f3-108">Перейдите в раздел "Управление производством" > "Канбан" > "Канбаны".</span><span class="sxs-lookup"><span data-stu-id="a36f3-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="a36f3-109">Откройте фильтр столбца статуса единицы обработки.</span><span class="sxs-lookup"><span data-stu-id="a36f3-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="a36f3-110">Щелкните "Очистить".</span><span class="sxs-lookup"><span data-stu-id="a36f3-110">Click Clear.</span></span>
    * <span data-ttu-id="a36f3-111">Это приведет к сбросу фильтров.</span><span class="sxs-lookup"><span data-stu-id="a36f3-111">This resets the filters.</span></span>  
4. <span data-ttu-id="a36f3-112">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="a36f3-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a36f3-113">Например, отфильтруйте поле "Номер карты" по значению "000149".</span><span class="sxs-lookup"><span data-stu-id="a36f3-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="a36f3-114">Изменение статуса "Освобождено" на "Получено"</span><span class="sxs-lookup"><span data-stu-id="a36f3-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="a36f3-115">Щелкните "Обращение пустой единицы обработки".</span><span class="sxs-lookup"><span data-stu-id="a36f3-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="a36f3-116">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a36f3-116">Click OK.</span></span>
    * <span data-ttu-id="a36f3-117">Обратите внимание, что единица обработки имеет статус "Получено".</span><span class="sxs-lookup"><span data-stu-id="a36f3-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="a36f3-118">Изменение статуса "Получено" на "Освобождено"</span><span class="sxs-lookup"><span data-stu-id="a36f3-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="a36f3-119">Щелкните "Пустой канбан".</span><span class="sxs-lookup"><span data-stu-id="a36f3-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="a36f3-120">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="a36f3-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a36f3-121">Обратите внимание, что единица обработки имеет статус "Освобождено".</span><span class="sxs-lookup"><span data-stu-id="a36f3-121">Notice that the Handling unit status is Emptied.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]