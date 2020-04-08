---
title: Изменение прогноза спроса вручную
description: В этой процедуре показано, как внести изменения в прогноз для номенклатуры.
author: ShylaThompson
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58846f896d60610d0e90f8d04fda3101def53511
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148109"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="44fc5-103">Изменение прогноза спроса вручную</span><span class="sxs-lookup"><span data-stu-id="44fc5-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="44fc5-104">В этой процедуре показано, как внести изменения в прогноз для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="44fc5-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="44fc5-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="44fc5-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="44fc5-106">Эта запись предназначена для планировщика производства.</span><span class="sxs-lookup"><span data-stu-id="44fc5-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="44fc5-107">Изменение прогноза для номенклатуры</span><span class="sxs-lookup"><span data-stu-id="44fc5-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="44fc5-108">В **области переходов** выберите **Модули > Управление сведениями о продукте > Продукты > Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="44fc5-108">In the **Navigation pane**, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="44fc5-109">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="44fc5-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="44fc5-110">Выберите номенклатуру, прогноз для которой требуется изменить.</span><span class="sxs-lookup"><span data-stu-id="44fc5-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="44fc5-111">Например, можно выбрать номенклатуру D0001.</span><span class="sxs-lookup"><span data-stu-id="44fc5-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="44fc5-112">В области **Панель операций** щелкните **План**.</span><span class="sxs-lookup"><span data-stu-id="44fc5-112">On the **Action Pane**, click **Plan**.</span></span>
4. <span data-ttu-id="44fc5-113">Щелкните **Прогноз спроса**.</span><span class="sxs-lookup"><span data-stu-id="44fc5-113">Click **Demand forecast**.</span></span>
5. <span data-ttu-id="44fc5-114">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="44fc5-114">In the list, mark the selected row.</span></span> <span data-ttu-id="44fc5-115">Если строк прогноза нет, создайте новую строку, щелкнув "Создать" на панели приложения.</span><span class="sxs-lookup"><span data-stu-id="44fc5-115">If there are no forecast lines, create a new line by clicking New on the app bar.</span></span>  
6. <span data-ttu-id="44fc5-116">В поле **Продаваемое количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="44fc5-116">In the **Sales quantity** field, enter a number.</span></span> <span data-ttu-id="44fc5-117">Это число представляет собой прогнозное количество для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="44fc5-117">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="44fc5-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="44fc5-118">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="44fc5-119">Изменение прогноза в Excel</span><span class="sxs-lookup"><span data-stu-id="44fc5-119">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="44fc5-120">Щелкните **Открыть** в Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="44fc5-120">Click **Open** in Microsoft Office.</span></span>
2. <span data-ttu-id="44fc5-121">Щелкните **Редактировать прогноз спроса** в Excel".</span><span class="sxs-lookup"><span data-stu-id="44fc5-121">Click **Edit Demand forecast** in Excel.</span></span> <span data-ttu-id="44fc5-122">В Excel можно добавлять, удалять и изменять строки прогноза спроса.</span><span class="sxs-lookup"><span data-stu-id="44fc5-122">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="44fc5-123">Если вы не видите данные в Excel, необходимо войти, установив флажок "Оставаться в системе"; кроме того, необходимо доверять приложению для подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="44fc5-123">If you are not able to see the data in Excel, you need to sign in with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

