---
title: Рассчитать прогноз номенклатуры
description: В этом разделе описывается, как рассчитать прогноз по номенклатуре в модуле "Управление активами".
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9392245abe5858b03b8324dcb471f5652aed7cd6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813901"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="b3c44-103">Рассчитать прогноз номенклатуры</span><span class="sxs-lookup"><span data-stu-id="b3c44-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b3c44-104">Точно так же, как можно выполнить расчеты загрузки мощностей, которые описаны в предыдущем разделе, можно также выполнять расчеты прогноза по номенклатурам:</span><span class="sxs-lookup"><span data-stu-id="b3c44-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on:</span></span>

- <span data-ttu-id="b3c44-105">строки графика обслуживания</span><span class="sxs-lookup"><span data-stu-id="b3c44-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="b3c44-106">заказы на работу, которые еще не были запланированы</span><span class="sxs-lookup"><span data-stu-id="b3c44-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="b3c44-107">запланированные заказы на работу</span><span class="sxs-lookup"><span data-stu-id="b3c44-107">scheduled work orders</span></span>

<span data-ttu-id="b3c44-108">Это полезно, если требуется получить обзор ожидаемого потребления номенклатур (запасные части, а также другие номенклатуры, необходимые для выполнения заказов на работу) за конкретный период.</span><span class="sxs-lookup"><span data-stu-id="b3c44-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="b3c44-109">Расчет прогноза по номенклатурам может выполняться по всем активам или по выбранным активам.</span><span class="sxs-lookup"><span data-stu-id="b3c44-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="b3c44-110">Кроме того, можно выполнить расчет по мероприятию простоя из-за обслуживания (**Все мероприятия по простою из-за обслуживания** или **Активные мероприятия по простою из-за обслуживания**) или по пулу заказов на работу (**Все пулы заказов на работу** или **Активные пулы заказов на работу**).</span><span class="sxs-lookup"><span data-stu-id="b3c44-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="b3c44-111">Щелкните **Управление активами** > **Запросы** > **Прогноз по номенклатурам** или **Управление активами** > **Общее** > **Пулы заказов на работу** > **Все пулы заказов на работу** / **Активные пулы заказов на работу** > выберите пул заказов на работу в списке > кнопка **Прогноз по номенклатурам** или **Управление активами** > **Общее** > **Мероприятия по простою из-за обслуживания** > **Все мероприятия по простою из-за обслуживания** / **Активные мероприятия по простою из-за обслуживания** > выберите мероприятие по простою из-за обслуживания в списке > кнопка **Прогноз по номенклатурам**.</span><span class="sxs-lookup"><span data-stu-id="b3c44-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="b3c44-112">В диалоговом окне **Рассчитать прогноз номенклатуры** выберите период для расчета в полях **Дата и время начала** и **Дата и время окончания**.</span><span class="sxs-lookup"><span data-stu-id="b3c44-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="b3c44-113">Выберите "Да" на кнопке-переключателе **Включить график обслуживания**, если требуется включить строки графика обслуживания в расчет прогноза.</span><span class="sxs-lookup"><span data-stu-id="b3c44-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="b3c44-114">Выберите "Да" на кнопке-переключателе **Включить заказ на работу**, если требуется включить задания заказа на работу в расчет прогноза.</span><span class="sxs-lookup"><span data-stu-id="b3c44-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="b3c44-115">Можно использовать поле **Уровень**, чтобы указать, насколько подробными должны быть строки прогноза по номенклатурам относительно функциональных местоположений.</span><span class="sxs-lookup"><span data-stu-id="b3c44-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> 

      <span data-ttu-id="b3c44-116">Например, если вставить число "1" в это поле, и имеется структура функциональных местоположений с несколькими уровнями, все строки графика обслуживания и заказы на работу для функционального местоположения будут показаны на верхнем уровне, и поэтому часы по строке могут быть добавлены из функциональных местоположений, расположенных на более низком уровне.</span><span class="sxs-lookup"><span data-stu-id="b3c44-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
  
      <span data-ttu-id="b3c44-117">Если вставить число "0" в поле **Уровень**, будет выведен подробный результат, отображающий все строки графика обслуживания и все заказы на работу на всех уровнях функциональных местоположений, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="b3c44-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="b3c44-118">Нажмите **ОК**, чтобы начать расчет.</span><span class="sxs-lookup"><span data-stu-id="b3c44-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="b3c44-119">В группах **Группировать по...** щелкните соответствующие кнопки, чтобы отобразить необходимый уровень детализации для расчета.</span><span class="sxs-lookup"><span data-stu-id="b3c44-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="b3c44-120">На снимке экрана ниже выбранные кнопки **Группировать по** выделяются синим цветом.</span><span class="sxs-lookup"><span data-stu-id="b3c44-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="b3c44-121">Нажимайте кнопку, чтобы активировать или деактивировать ее.</span><span class="sxs-lookup"><span data-stu-id="b3c44-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="b3c44-122">Нажмите кнопку **Отобразить аналитики**, если требуется просмотреть аналитики продукта, хранения или отслеживания, имеющие отношение к номенклатурам.</span><span class="sxs-lookup"><span data-stu-id="b3c44-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="b3c44-123">Выберите соответствующие флажки и щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3c44-123">Select the relevant check boxes, and click **OK**.</span></span>

![Рисунок 1](media/02-capacity-planning.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]