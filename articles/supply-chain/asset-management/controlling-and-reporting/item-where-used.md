---
title: Используемая номенклатура
description: В этой теме объясняется, как получить обзор использования номенклатуры в модуле "Управление активами".
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemWhereUsed, EntAssetItemWhereUsedCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 262a5a9d83767599f6e15183d6afcacf4b5901fe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808648"
---
# <a name="item-where-used"></a><span data-ttu-id="116a4-103">Используемая номенклатура</span><span class="sxs-lookup"><span data-stu-id="116a4-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="116a4-104">Можно выполнить расчет для определенной номенклатуры, чтобы получить обзор того, где в управлении активами была использована номенклатура.</span><span class="sxs-lookup"><span data-stu-id="116a4-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="116a4-105">Результаты показывают контекст, в котором номенклатура использовалась во время ее существования.</span><span class="sxs-lookup"><span data-stu-id="116a4-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="116a4-106">Страницу **Используемая номенклатура** можно открыть страницу из главного меню управления активами, а также со следующих страниц:</span><span class="sxs-lookup"><span data-stu-id="116a4-106">The **Item where used** page can be opened from the main Asset Management menu, and it can also be accessed from the following pages:</span></span>

- [<span data-ttu-id="116a4-107">Спецификации актива</span><span class="sxs-lookup"><span data-stu-id="116a4-107">Asset BOMs</span></span>](../objects/object-BOM.md)

- [<span data-ttu-id="116a4-108">Запасные части в настройках по умолчанию типа актива</span><span class="sxs-lookup"><span data-stu-id="116a4-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [<span data-ttu-id="116a4-109">Категории типов заданий обслуживания и типы заданий обслуживания, варианты типов заданий обслуживания, торговля заданий обслуживания, контрольные списки обслуживания</span><span class="sxs-lookup"><span data-stu-id="116a4-109">Maintenance job type categories and maintenance job types, maintenance job type variants, maintenance job trades, and maintenance checklists</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [<span data-ttu-id="116a4-110">Прогноз обслуживания</span><span class="sxs-lookup"><span data-stu-id="116a4-110">Maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

- [<span data-ttu-id="116a4-111">Закупки</span><span class="sxs-lookup"><span data-stu-id="116a4-111">Procurement</span></span>](../work-orders/procurement.md)

- [<span data-ttu-id="116a4-112">Заказ на покупку заказа на работу</span><span class="sxs-lookup"><span data-stu-id="116a4-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="116a4-113">Выполнение расчета используемой номенклатуры</span><span class="sxs-lookup"><span data-stu-id="116a4-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="116a4-114">Выберите **Управление активами** > **Запросы** > **Используемая номенклатура** или выберите кнопку **Используемая номенклатура** на одной из упомянутых выше страниц.</span><span class="sxs-lookup"><span data-stu-id="116a4-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="116a4-115">В диалоговом окне **Используемая номенклатура** выберите номенклатуру, для которой необходимо выполнить расчет, в поле **Код номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="116a4-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="116a4-116">Можно использовать поле **Уровень**, чтобы указать, насколько подробными должны быть строки номенклатуры относительно функциональных местоположений.</span><span class="sxs-lookup"><span data-stu-id="116a4-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="116a4-117">Например, если вставить число "1" в поле, и имеется структура функциональных местоположений с несколькими уровнями, все строки номенклатур для функционального местоположения будут показаны на верхнем уровне.</span><span class="sxs-lookup"><span data-stu-id="116a4-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="116a4-118">Таким образом, отношение/количество в строке могут быть добавлены из функциональных местоположений, расположенных на более низком уровне.</span><span class="sxs-lookup"><span data-stu-id="116a4-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="116a4-119">Если вставить число "0" в поле **Уровень**, будет выведен подробный результат, отображающий все строки номенклатур на всех уровнях функциональных местоположений, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="116a4-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="116a4-120">В разделе **Включить** выберите "Да" на переключателях, которые требуется включить в расчет.</span><span class="sxs-lookup"><span data-stu-id="116a4-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="116a4-121">Нажмите **ОК**, чтобы начать расчет.</span><span class="sxs-lookup"><span data-stu-id="116a4-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="116a4-122">На вкладке **Используемая номенклатура** выберите кнопки **Группировать по**, чтобы отобразить необходимый уровень детализации для расчета.</span><span class="sxs-lookup"><span data-stu-id="116a4-122">On the **Item where used** tab, select the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="116a4-123">Выбранные кнопки **Группировать по...** выделяются.</span><span class="sxs-lookup"><span data-stu-id="116a4-123">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="116a4-124">Нажимайте кнопку, чтобы активировать или деактивировать ее.</span><span class="sxs-lookup"><span data-stu-id="116a4-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="116a4-125">Если требуется отобразить аналитики, имеющие отношение к номенклатуре, щелкните **Отобразить аналитики** и выберите аналитики для отображения.</span><span class="sxs-lookup"><span data-stu-id="116a4-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

## <a name="example"></a><span data-ttu-id="116a4-126">Пример</span><span class="sxs-lookup"><span data-stu-id="116a4-126">Example</span></span>

<span data-ttu-id="116a4-127">На снимке экрана, приведенном ниже, вы видите пример расчета использования номенклатуры для кода номенклатуры "1000".</span><span class="sxs-lookup"><span data-stu-id="116a4-127">In the screenshot below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![Пример расчета используемой номенклатуры](media/12-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]