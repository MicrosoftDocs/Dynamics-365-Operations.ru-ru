---
title: Изменение прогноза спроса вручную
description: В этой процедуре показано, как внести изменения в прогноз для номенклатуры.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 063554c98b8a6261ebe69073f214a8e45850c623
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560744"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="0a5c2-103">Изменение прогноза спроса вручную</span><span class="sxs-lookup"><span data-stu-id="0a5c2-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0a5c2-104">В этой процедуре показано, как внести изменения в прогноз для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="0a5c2-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="0a5c2-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="0a5c2-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0a5c2-106">Эта запись предназначена для планировщика производства.</span><span class="sxs-lookup"><span data-stu-id="0a5c2-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="0a5c2-107">Изменение прогноза для номенклатуры</span><span class="sxs-lookup"><span data-stu-id="0a5c2-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="0a5c2-108">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="0a5c2-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="0a5c2-109">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="0a5c2-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0a5c2-110">Выберите номенклатуру, прогноз для которой требуется изменить.</span><span class="sxs-lookup"><span data-stu-id="0a5c2-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="0a5c2-111">Например, можно выбрать номенклатуру D0001.</span><span class="sxs-lookup"><span data-stu-id="0a5c2-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="0a5c2-112">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="0a5c2-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="0a5c2-113">Щелкните "Прогноз спроса".</span><span class="sxs-lookup"><span data-stu-id="0a5c2-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="0a5c2-114">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="0a5c2-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0a5c2-115">Если строк прогноза нет, создайте новую строку,</span><span class="sxs-lookup"><span data-stu-id="0a5c2-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="0a5c2-116">щелкнув "Создать" на панели приложения.</span><span class="sxs-lookup"><span data-stu-id="0a5c2-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="0a5c2-117">В поле "Продаваемое количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="0a5c2-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="0a5c2-118">Это число представляет собой прогнозное количество для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="0a5c2-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="0a5c2-119">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="0a5c2-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="0a5c2-120">Изменение прогноза в Excel</span><span class="sxs-lookup"><span data-stu-id="0a5c2-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="0a5c2-121">Щелкните "Открыть" в Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="0a5c2-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="0a5c2-122">Щелкните "Редактировать прогноза спроса в Excel".</span><span class="sxs-lookup"><span data-stu-id="0a5c2-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="0a5c2-123">В Excel можно добавлять, удалять и изменять строки прогноза спроса.</span><span class="sxs-lookup"><span data-stu-id="0a5c2-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="0a5c2-124">Если вы не видите данные в Excel, необходимо войти в Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, установив флажок "Оставаться в системе"; кроме того, необходимо доверять приложению для подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="0a5c2-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

