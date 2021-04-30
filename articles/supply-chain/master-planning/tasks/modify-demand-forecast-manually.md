---
title: Изменение прогноза спроса вручную
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
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889032"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="ba4cc-103">Изменение прогноза спроса вручную</span><span class="sxs-lookup"><span data-stu-id="ba4cc-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ba4cc-104">В этой процедуре показано, как внести изменения в прогноз для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="ba4cc-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ba4cc-106">Эта процедура предназначена для планировщика производства.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-106">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="ba4cc-107">Изменение прогноза для выбранной номенклатуры</span><span class="sxs-lookup"><span data-stu-id="ba4cc-107">Modify the forecast for a selected item</span></span>

<span data-ttu-id="ba4cc-108">Для изменения прогноза для выбранной номенклатуры:</span><span class="sxs-lookup"><span data-stu-id="ba4cc-108">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="ba4cc-109">Перейдите к **Модули \> Управление сведениями о производстве \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-109">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="ba4cc-110">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-110">In the list, find and select the desired record.</span></span> <span data-ttu-id="ba4cc-111">Выберите номенклатуру, прогноз для которой требуется изменить.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-111">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="ba4cc-112">На панели операций откройте вкладку **план** и выберите **прогноз спроса**.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-112">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="ba4cc-113">В списке выберите строку.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-113">In the list, select a row.</span></span> <span data-ttu-id="ba4cc-114">Если строк прогноза нет, создайте новую строку, выбрав **Создать** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-114">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="ba4cc-115">В поле **Продаваемое количество** введите положительное число.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-115">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="ba4cc-116">Это число представляет собой прогнозное количество для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-116">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="ba4cc-117">При вводе отрицательного числа отображается сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-117">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="ba4cc-118">Заполните соответствующим образом остальные поля.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-118">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="ba4cc-119">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-119">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a><span data-ttu-id="ba4cc-120">Изменение прогноза для одной или нескольких номенклатур Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="ba4cc-120">Modify the forecast for one or more items Microsoft Excel</span></span>

<span data-ttu-id="ba4cc-121">Чтобы изменить прогноз для одной или нескольких номенклатур Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="ba4cc-121">To modify the forecast for one or more items Microsoft Excel:</span></span>

1. <span data-ttu-id="ba4cc-122">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-122">Do one of the following:</span></span>
    - <span data-ttu-id="ba4cc-123">Откройте страницу **прогноз спроса** для любой номенклатуры (но не имеет значения, какой из них), как описано в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-123">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="ba4cc-124">Перейдите в раздел **Сводное планирование \> Прогнозирование \> Ручной ввод прогноза \> Строки прогноза спроса**.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-124">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="ba4cc-125">На панели операций выберите **Открыть в Microsoft Office \> записи прогноза спроса**.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-125">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="ba4cc-126">Выберите место загрузки, сохраните, а затем откройте загруженный файл в Excel.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-126">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="ba4cc-127">Если отображается предупреждение, выберите **Разрешить изменение**.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-127">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="ba4cc-128">В Microsoft Excel выполните вход в Supply Chain Management с помощью панели задач Microsoft Dynamics.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-128">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="ba4cc-129">Необходимо войти в систему с включенным параметром **Оставаться в системе**, и вы должны доверять приложению для подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-129">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="ba4cc-130">В таблице Excel отображаются все строки текущего прогноза спроса для вашей компании.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-130">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="ba4cc-131">Добавлять, удалять и изменять строки прогноза спроса, при необходимости.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-131">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="ba4cc-132">Выберите **Опубликовать** в панели задач Microsoft Dynamics, чтобы отправить изменения обратно в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ba4cc-132">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
