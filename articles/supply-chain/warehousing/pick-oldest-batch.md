---
title: "Выбор самой старой партии на мобильном устройстве"
description: "В этом разделе описывается, как настроить и применить параметры для комплектации самой старой партии на мобильном устройстве."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 25056886b1a18dbaef12c8732a1fd0bd92a6d04b
ms.contentlocale: ru-ru
ms.lasthandoff: 07/18/2017

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a><span data-ttu-id="2b001-103">Выбор самой старой партии на мобильном устройстве</span><span class="sxs-lookup"><span data-stu-id="2b001-103">Pick oldest batch on a mobile device</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2b001-104">К конфигурации **Выбрать самую старую партию** можно перейти через меню мобильного устройства, она позволяет инициировать или предупредить работников склада скомплектовать саму старую партию в их текущем местонахождении.</span><span class="sxs-lookup"><span data-stu-id="2b001-104">You can access the configuration **Pick oldest batch** via a mobile device menu and it allows you to force or warn warehouse workers to pick the oldest batch in their current location.</span></span>  

## <a name="where-it-applies"></a><span data-ttu-id="2b001-105">Где это применяется</span><span class="sxs-lookup"><span data-stu-id="2b001-105">Where it applies</span></span>
<span data-ttu-id="2b001-106">Комплектация самой старой партии настраивается в меню мобильного устройства и влияет на комплектацию следующих партий номенклатур.</span><span class="sxs-lookup"><span data-stu-id="2b001-106">Pick oldest batch is configured on mobile device menu items and effects the pick for batch below items.</span></span>

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a><span data-ttu-id="2b001-107">Порядок настройки комплектации самой старой партии</span><span class="sxs-lookup"><span data-stu-id="2b001-107">How to set up the configuration for Pick oldest batch</span></span> 
<span data-ttu-id="2b001-108">Для номенклатур, которые настроены для использования существующей работы, для **Выбрать самую старую партию** можно задать **Нет**, **Предупредить** или **Инициировать** в меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="2b001-108">For items that are set to use existing work, **Pick oldest batch** can be set to **None**, **Warn**, or **Force** from a mobile device menu.</span></span>

<span data-ttu-id="2b001-109">**Нет**: работники не получат сообщения и смогут скомплектовать любую партию в своем местонахождении.</span><span class="sxs-lookup"><span data-stu-id="2b001-109">**None**: Workers will not receive any messages and they will be allowed to pick any batch in their location.</span></span>

<span data-ttu-id="2b001-110">**Предупредить** и **Инициировать**: список партии (партий) с самыми старыми сроками окончания действия будут отображаться над элементом управления партии, если работник выбирает партию.</span><span class="sxs-lookup"><span data-stu-id="2b001-110">**Warn** and **Force**:  A list of the batch(es) with the oldest expiration date will be displayed above the batch control when the worker selects a batch.</span></span> <span data-ttu-id="2b001-111">Если в местонахождении находятся грузоместа, над элементом управления грузоместом отобразится список грузомест с самой старой партией.</span><span class="sxs-lookup"><span data-stu-id="2b001-111">If the location is license plate controlled, a list of license plates that have the oldest batch will be displayed above the license plate control.</span></span> 
-   <span data-ttu-id="2b001-112">**Предупреждение**: если работник выбирает грузоместо или партию, которая отсутствует в списке, элемент управления начнет мигать и будет показано предупреждение, что для выбора доступна более старая партия.</span><span class="sxs-lookup"><span data-stu-id="2b001-112">**Warn**: If a worker chooses a license plate or batch that is not on the shown list, the control will be blanked and a warning will be shown that there is an older batch to select.</span></span> <span data-ttu-id="2b001-113">Чтобы продолжать работу, работник снова может выбрать то же грузоместо или партию.</span><span class="sxs-lookup"><span data-stu-id="2b001-113">To be allowed to continue the work, the worker can select the same license plate or batch again.</span></span>  
-   <span data-ttu-id="2b001-114">**Инициировать**: работник продолжит получать сообщение, что для комплектации доступна более старая партия.</span><span class="sxs-lookup"><span data-stu-id="2b001-114">**Force**: Workers will continue to receive the message that there is an older batch to pick.</span></span>

