---
title: Используемая номенклатура
description: В этой теме объясняется, как получить обзор использования номенклатуры в модуле "Управление активами".
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 84ab803aedf5b803b6c5f39ff1907726335cb45d
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918334"
---
# <a name="item-where-used"></a><span data-ttu-id="2f8fa-103">Используемая номенклатура</span><span class="sxs-lookup"><span data-stu-id="2f8fa-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="2f8fa-104">Можно выполнить расчет для определенной номенклатуры, чтобы получить обзор того, где в управлении активами была использована номенклатура.</span><span class="sxs-lookup"><span data-stu-id="2f8fa-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="2f8fa-105">Результаты показывают контекст, в котором номенклатура использовалась во время ее существования.</span><span class="sxs-lookup"><span data-stu-id="2f8fa-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="2f8fa-106">Страницу **Используемая номенклатура** можно открыть страницу из главного меню управления активами, а также со следующих страниц:</span><span class="sxs-lookup"><span data-stu-id="2f8fa-106">The **Item where used** page can be opened from the main Asset management menu, and it can also be accessed from the following pages:</span></span>

[<span data-ttu-id="2f8fa-107">Спецификация актива</span><span class="sxs-lookup"><span data-stu-id="2f8fa-107">Asset BOM</span></span>](../objects/object-BOM.md)

[<span data-ttu-id="2f8fa-108">Запасные части в настройках по умолчанию типа актива</span><span class="sxs-lookup"><span data-stu-id="2f8fa-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md)

[<span data-ttu-id="2f8fa-109">Прогноз по номенклатурам в прогнозе значений по умолчанию для типа заданий обслуживания</span><span class="sxs-lookup"><span data-stu-id="2f8fa-109">Item forecast on Maintenance job type defaults forecast</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

[<span data-ttu-id="2f8fa-110">Прогноз обслуживания заказа на работу</span><span class="sxs-lookup"><span data-stu-id="2f8fa-110">Work order maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

[<span data-ttu-id="2f8fa-111">Заявка на покупку заказа на работу</span><span class="sxs-lookup"><span data-stu-id="2f8fa-111">Work order purchase requisition</span></span>](../work-orders/procurement.md)

[<span data-ttu-id="2f8fa-112">Заказ на покупку заказа на работу</span><span class="sxs-lookup"><span data-stu-id="2f8fa-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="2f8fa-113">Выполнение расчета используемой номенклатуры</span><span class="sxs-lookup"><span data-stu-id="2f8fa-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="2f8fa-114">Выберите **Управление активами** > **Запросы** > **Используемая номенклатура** или выберите кнопку **Используемая номенклатура** на одной из упомянутых выше страниц.</span><span class="sxs-lookup"><span data-stu-id="2f8fa-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="2f8fa-115">В диалоговом окне **Используемая номенклатура** выберите номенклатуру, для которой необходимо выполнить расчет, в поле **Код номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="2f8fa-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="2f8fa-116">Можно использовать поле **Уровень**, чтобы указать, насколько подробными должны быть строки номенклатуры относительно функциональных местоположений.</span><span class="sxs-lookup"><span data-stu-id="2f8fa-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> <span data-ttu-id="2f8fa-117">Например, если вставить число "1" в поле, и имеется структура функциональных местоположений с несколькими уровнями, все строки номенклатур для функционального местоположения будут показаны на верхнем уровне.</span><span class="sxs-lookup"><span data-stu-id="2f8fa-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="2f8fa-118">Таким образом, отношение/количество в строке могут быть добавлены из функциональных местоположений, расположенных на более низком уровне.</span><span class="sxs-lookup"><span data-stu-id="2f8fa-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="2f8fa-119">Если вставить число "0" в поле **Уровень**, будет выведен подробный результат, отображающий все строки номенклатур на всех уровнях функциональных местоположений, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="2f8fa-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="2f8fa-120">В разделе **Включить** выберите "Да" на переключателях, которые требуется включить в расчет.</span><span class="sxs-lookup"><span data-stu-id="2f8fa-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="2f8fa-121">Нажмите **ОК**, чтобы начать расчет.</span><span class="sxs-lookup"><span data-stu-id="2f8fa-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="2f8fa-122">На вкладке **Используемая номенклатура** > в группах панели операций **Группировать по...** выберите соответствующие кнопки, чтобы отобразить необходимый уровень детализации для расчета.</span><span class="sxs-lookup"><span data-stu-id="2f8fa-122">On the **Item where used** tab > **Group by...** action pane groups, select the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="2f8fa-123">Выбранные кнопки панели операций выделяются.</span><span class="sxs-lookup"><span data-stu-id="2f8fa-123">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="2f8fa-124">Нажимайте кнопку, чтобы активировать или деактивировать ее.</span><span class="sxs-lookup"><span data-stu-id="2f8fa-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="2f8fa-125">Если требуется отобразить аналитики, имеющие отношение к номенклатуре, щелкните **Отобразить аналитики** и выберите аналитики для отображения.</span><span class="sxs-lookup"><span data-stu-id="2f8fa-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

<span data-ttu-id="2f8fa-126">На рисунке, приведенном ниже, вы видите пример расчета использования номенклатуры для кода номенклатуры "1000".</span><span class="sxs-lookup"><span data-stu-id="2f8fa-126">In the figure below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![Рисунок 1](media/12-controlling-and-reporting.png)

