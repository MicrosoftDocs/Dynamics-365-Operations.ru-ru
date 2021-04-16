---
title: Шаблоны загрузок
description: В этом разделе описывается, как настроить шаблоны загрузки, и как связать шаблон загрузки с новой загрузкой.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 175c8017b14cc298cdaa00031f8450015a747786
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831514"
---
# <a name="load-templates"></a><span data-ttu-id="bf7d8-103">Шаблоны загрузок</span><span class="sxs-lookup"><span data-stu-id="bf7d8-103">Load templates</span></span>

<span data-ttu-id="bf7d8-104">При создании новой загрузки можно назначить шаблон загрузки.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="bf7d8-105">Шаблон загрузок содержит информацию об оборудовании и о показателях, таких как высота, ширина, глубина и объем загрузки.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="bf7d8-106">В этом разделе описывается, как настроить шаблоны загрузки, и как связать шаблон загрузки с новой загрузкой.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="bf7d8-107">Настройка шаблона загрузки</span><span class="sxs-lookup"><span data-stu-id="bf7d8-107">Set up a load template</span></span>

1. <span data-ttu-id="bf7d8-108">Перейдите в раздел **Управление транспортировкой \> Настройка \> Формирование загрузки \> Шаблон загрузки**.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="bf7d8-109">В области действий выберите **Создать**, чтобы добавить новый шаблон, или выберите **Правка**, чтобы изменить существующий шаблон.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="bf7d8-110">В строке для нового или существующего шаблона задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="bf7d8-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="bf7d8-111">**Код шаблона загрузки** — введите уникальный код шаблона загрузки.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="bf7d8-112">**Оборудование** — выберите оборудование, которое должно использоваться для отгрузки загрузки.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="bf7d8-113">**Высота загрузки**, **Ширина загрузки** и **Глубина загрузки** — введите аналитики для загрузки.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="bf7d8-114">**Максимально допустимый объем загрузки** и **Максимально допустимый вес загрузки** — введите максимально допустимый объем и вес загрузки.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="bf7d8-115">**Максимально допустимый вес брутто** — введите максимально допустимый вес брутто загрузки.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="bf7d8-116">Вес брутто загрузки включает вес тары и вес загрузки.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="bf7d8-117">**Максимальное разрешенное число фрагментов фрахта** — введите максимальное количество единиц поставки, которое может содержаться в загрузке.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="bf7d8-118">**Складывать загрузку на этаже** — установите этот флажок, чтобы использовать загрузку на пол.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="bf7d8-119">В сценарии, учитывающем нагрузку на пол, коробки штабелируются от пола до потолка и от стены к стене внутри контейнера, чтобы максимально эффективно использовать емкость.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="bf7d8-120">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="bf7d8-121">Связывание шаблона загрузки с новой загрузкой</span><span class="sxs-lookup"><span data-stu-id="bf7d8-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="bf7d8-122">Перейдите в раздел **Управление транспортировкой \> Планирование \> Рабочее место планирования загрузки**.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="bf7d8-123">В верхней части страницы выберите одну из следующих вкладок, в зависимости от типа документа источника, для которого создается загрузка: **Отгрузки**, **Строки продажи**, **Строки перемещения** или **Строки заказа на покупку**.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="bf7d8-124">Выберите конкретный документ, для которого планируется загрузка.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="bf7d8-125">В области действий на вкладке **Поставки и спрос** в группе **Добавить** выберите **В новую загрузку**.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="bf7d8-126">В диалоговом окне **Шаблон загрузки** в поле **Код шаблона загрузки** выберите шаблон для применения.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="bf7d8-127">Выберите **ОК**, чтобы применить шаблон.</span><span class="sxs-lookup"><span data-stu-id="bf7d8-127">Select **OK** to apply the template.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]