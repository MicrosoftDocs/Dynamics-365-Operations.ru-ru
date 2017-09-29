--- 
title: "Изменение прогноза спроса вручную"
description: "В этой процедуре показано, как внести изменения в прогноз для номенклатуры."
author: YuyuScheller
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2e269ef7b33b4d7e171d284d68d28c825c2fe86c
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="1e2db-103">Изменение прогноза спроса вручную</span><span class="sxs-lookup"><span data-stu-id="1e2db-103">Modify a demand forecast manually</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e2db-104">В этой процедуре показано, как внести изменения в прогноз для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="1e2db-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="1e2db-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="1e2db-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="1e2db-106">Эта запись предназначена для планировщика производства.</span><span class="sxs-lookup"><span data-stu-id="1e2db-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="1e2db-107">Изменение прогноза для номенклатуры</span><span class="sxs-lookup"><span data-stu-id="1e2db-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="1e2db-108">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="1e2db-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="1e2db-109">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="1e2db-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1e2db-110">Выберите номенклатуру, прогноз для которой требуется изменить.</span><span class="sxs-lookup"><span data-stu-id="1e2db-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="1e2db-111">Например, можно выбрать номенклатуру D0001.</span><span class="sxs-lookup"><span data-stu-id="1e2db-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="1e2db-112">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="1e2db-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="1e2db-113">Щелкните "Прогноз спроса".</span><span class="sxs-lookup"><span data-stu-id="1e2db-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="1e2db-114">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="1e2db-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1e2db-115">Если строк прогноза нет, создайте новую строку,</span><span class="sxs-lookup"><span data-stu-id="1e2db-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="1e2db-116">щелкнув "Создать" на панели приложения.</span><span class="sxs-lookup"><span data-stu-id="1e2db-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="1e2db-117">В поле "Продаваемое количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="1e2db-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="1e2db-118">Это число представляет собой прогнозное количество для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="1e2db-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="1e2db-119">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="1e2db-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="1e2db-120">Изменение прогноза в Excel</span><span class="sxs-lookup"><span data-stu-id="1e2db-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="1e2db-121">Щелкните "Открыть в Microsoft Office".</span><span class="sxs-lookup"><span data-stu-id="1e2db-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="1e2db-122">Щелкните "Редактировать прогноза спроса в Excel".</span><span class="sxs-lookup"><span data-stu-id="1e2db-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="1e2db-123">В Excel можно добавлять, удалять и изменять строки прогноза спроса.</span><span class="sxs-lookup"><span data-stu-id="1e2db-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="1e2db-124">Если вы не видите данные в Excel, необходимо войти в Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, установив флажок "Оставаться в системе"; кроме того, необходимо доверять приложению для подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="1e2db-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  


