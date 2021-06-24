---
title: 'Руководство: изменение прогноза спроса вручную'
description: В этом разделе описывается, как внести изменения в прогноз для номенклатуры
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224018"
---
# <a name="guide-modify-a-demand-forecast-manually"></a><span data-ttu-id="774ed-103">Руководство: изменение прогноза спроса вручную</span><span class="sxs-lookup"><span data-stu-id="774ed-103">Guide: Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="774ed-104">В этой процедуре показано, как внести изменения в прогноз для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="774ed-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="774ed-105">Эта процедура предназначена для планировщика производства.</span><span class="sxs-lookup"><span data-stu-id="774ed-105">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="774ed-106">Изменение прогноза для выбранной номенклатуры</span><span class="sxs-lookup"><span data-stu-id="774ed-106">Modify the forecast for a selected item</span></span>

<span data-ttu-id="774ed-107">Для изменения прогноза для выбранной номенклатуры:</span><span class="sxs-lookup"><span data-stu-id="774ed-107">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="774ed-108">Перейдите к **Модули \> Управление сведениями о производстве \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="774ed-108">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="774ed-109">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="774ed-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="774ed-110">Выберите номенклатуру, прогноз для которой требуется изменить.</span><span class="sxs-lookup"><span data-stu-id="774ed-110">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="774ed-111">На панели операций откройте вкладку **план** и выберите **прогноз спроса**.</span><span class="sxs-lookup"><span data-stu-id="774ed-111">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="774ed-112">В списке выберите строку.</span><span class="sxs-lookup"><span data-stu-id="774ed-112">In the list, select a row.</span></span> <span data-ttu-id="774ed-113">Если строк прогноза нет, создайте новую строку, выбрав **Создать** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="774ed-113">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="774ed-114">В поле **Продаваемое количество** введите положительное число.</span><span class="sxs-lookup"><span data-stu-id="774ed-114">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="774ed-115">Это число представляет собой прогнозное количество для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="774ed-115">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="774ed-116">При вводе отрицательного числа отображается сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="774ed-116">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="774ed-117">Заполните соответствующим образом остальные поля.</span><span class="sxs-lookup"><span data-stu-id="774ed-117">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="774ed-118">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="774ed-118">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a><span data-ttu-id="774ed-119">Изменение прогноза для одной или нескольких номенклатур с помощью Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="774ed-119">Modify the forecast for one or more items with Microsoft Excel</span></span>

<span data-ttu-id="774ed-120">Чтобы изменить прогноз для одной или нескольких номенклатур с помощью Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="774ed-120">To modify the forecast for one or more items with Microsoft Excel:</span></span>

1. <span data-ttu-id="774ed-121">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="774ed-121">Do one of the following:</span></span>
    - <span data-ttu-id="774ed-122">Откройте страницу **прогноз спроса** для любой номенклатуры (но не имеет значения, какой из них), как описано в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="774ed-122">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="774ed-123">Перейдите в раздел **Сводное планирование \> Прогнозирование \> Ручной ввод прогноза \> Строки прогноза спроса**.</span><span class="sxs-lookup"><span data-stu-id="774ed-123">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="774ed-124">На панели операций выберите **Открыть в Microsoft Office \> записи прогноза спроса**.</span><span class="sxs-lookup"><span data-stu-id="774ed-124">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="774ed-125">Выберите место загрузки, сохраните, а затем откройте загруженный файл в Excel.</span><span class="sxs-lookup"><span data-stu-id="774ed-125">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="774ed-126">Если отображается предупреждение, выберите **Разрешить изменение**.</span><span class="sxs-lookup"><span data-stu-id="774ed-126">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="774ed-127">В Microsoft Excel выполните вход в Supply Chain Management с помощью панели задач Microsoft Dynamics.</span><span class="sxs-lookup"><span data-stu-id="774ed-127">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="774ed-128">Необходимо войти в систему с включенным параметром **Оставаться в системе**, и вы должны доверять приложению для подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="774ed-128">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="774ed-129">В таблице Excel отображаются все строки текущего прогноза спроса для вашей компании.</span><span class="sxs-lookup"><span data-stu-id="774ed-129">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="774ed-130">Добавлять, удалять и изменять строки прогноза спроса, при необходимости.</span><span class="sxs-lookup"><span data-stu-id="774ed-130">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="774ed-131">Выберите **Опубликовать** в панели задач Microsoft Dynamics, чтобы отправить изменения обратно в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="774ed-131">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
