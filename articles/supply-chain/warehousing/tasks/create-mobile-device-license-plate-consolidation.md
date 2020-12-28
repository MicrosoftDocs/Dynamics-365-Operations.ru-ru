---
title: Создание пункта меню мобильного устройства для консолидации грузомест
description: Эта процедура показывает, как создать пункт меню мобильного устройства для работы по консолидации номерных знаков.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7dc52284473f3e3275675b608386641c8570218b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435901"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="76be1-103">Создание пункта меню мобильного устройства для консолидации грузомест</span><span class="sxs-lookup"><span data-stu-id="76be1-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="76be1-104">Эта процедура показывает, как создать пункт меню мобильного устройства для работы по консолидации номерных знаков.</span><span class="sxs-lookup"><span data-stu-id="76be1-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="76be1-105">Это позволяет работникам склада консолидировать номенклатуры на одном номерном знаке с номенклатурами в другом грузоместе в пределах одного местоположения.</span><span class="sxs-lookup"><span data-stu-id="76be1-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="76be1-106">Например, они могут использовать это, если последующие шаги переноса были одинаковыми в обоих заказах на выполнение работ, поэтому работу необходимо выполнить только один раз для объединенных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="76be1-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="76be1-107">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="76be1-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="76be1-108">Эта задача обычно выполняется менеджером склада.</span><span class="sxs-lookup"><span data-stu-id="76be1-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="76be1-109">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="76be1-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="76be1-110">Перейдите в раздел "Управление складом" > "Настройка" > "Мобильное устройство" > "Пункты меню мобильного устройства".</span><span class="sxs-lookup"><span data-stu-id="76be1-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="76be1-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="76be1-111">Click New.</span></span>
3. <span data-ttu-id="76be1-112">В поле "Имя пункта меню" введите значение.</span><span class="sxs-lookup"><span data-stu-id="76be1-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="76be1-113">В поле "Заголовок" введите значение.</span><span class="sxs-lookup"><span data-stu-id="76be1-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="76be1-114">В поле "Режим" выберите "Косвенный".</span><span class="sxs-lookup"><span data-stu-id="76be1-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="76be1-115">В поле "Код мероприятия" выберите "Объединенные грузоместа".</span><span class="sxs-lookup"><span data-stu-id="76be1-115">In the Activity code field, select 'Consolidate license plates'.</span></span>

