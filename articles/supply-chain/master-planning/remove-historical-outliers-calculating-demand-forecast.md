---
title: Удаление выбросов из исторических транзакционных данных при расчете прогноза спроса
description: В этой статье описывается, как удалить выбросы из исторических данных, которые использовались для расчета прогноза спроса. Путем исключения выбросов, вы можете повысить точность прогноза.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup, ReqDemPlanOutlierQueryPreview
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dec963ed5abd6f77e82029a3ea5ba1a69d44e36
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981410"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="59c80-104">Удаление выбросов из исторических транзакционных данных при расчете прогноза спроса</span><span class="sxs-lookup"><span data-stu-id="59c80-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59c80-105">В этой статье описывается, как удалить выбросы из исторических данных, которые использовались для расчета прогноза спроса.</span><span class="sxs-lookup"><span data-stu-id="59c80-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="59c80-106">Путем исключения выбросов, вы можете повысить точность прогноза.</span><span class="sxs-lookup"><span data-stu-id="59c80-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="59c80-107">Можно удалить выбросы для повышения точности прогноза.</span><span class="sxs-lookup"><span data-stu-id="59c80-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="59c80-108">Эта задача не является обязательной.</span><span class="sxs-lookup"><span data-stu-id="59c80-108">This is an optional task.</span></span> <span data-ttu-id="59c80-109">Обзор процесса:</span><span class="sxs-lookup"><span data-stu-id="59c80-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="59c80-110">Щелкните **Сводное планирование** &gt; **Настройка** &gt; **Прогнозирование спроса** &gt; **Удаление выбросов**, чтобы открыть страницу **Удаление выбросов**, где вы можете использовать запрос для того, чтобы выбрать исключаемые проводки.</span><span class="sxs-lookup"><span data-stu-id="59c80-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="59c80-111">Выберите компанию, к которой применяется запрос, а затем введите имя и описание.</span><span class="sxs-lookup"><span data-stu-id="59c80-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="59c80-112">В поле **Дата запроса** автоматически задается текущая дата.</span><span class="sxs-lookup"><span data-stu-id="59c80-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="59c80-113">Установите флажок **Активно**, чтобы исключить проводки, найденные в результате запроса, из исторических данных.</span><span class="sxs-lookup"><span data-stu-id="59c80-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="59c80-114">Эта настройка вступит в силу при создании базового прогноза.</span><span class="sxs-lookup"><span data-stu-id="59c80-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="59c80-115">На странице **Запрос удаления выбросов** можно добавить, удалить и выбрать критерии, определяющие проводки, которые будут исключены при расчете базового прогноза.</span><span class="sxs-lookup"><span data-stu-id="59c80-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="59c80-116">Например, выберите определенную номенклатуру или проводку по заказу, которую необходимо исключить.</span><span class="sxs-lookup"><span data-stu-id="59c80-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="59c80-117">Щелкните **Отобразить проводки**.</span><span class="sxs-lookup"><span data-stu-id="59c80-117">Click **Display transactions**.</span></span> <span data-ttu-id="59c80-118">На странице **Проводки-выбросы** содержится список проводок, которые отвечают критериям, указанным в запросе, и которые будут исключены из исторических данных при расчете прогноза спроса.</span><span class="sxs-lookup"><span data-stu-id="59c80-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="59c80-119">**Примечание.** Вы можете также создать запрос, который основан на существующем запросе.</span><span class="sxs-lookup"><span data-stu-id="59c80-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="59c80-120">Выберите запрос для копирования и после этого щелкните **Дублировать**.</span><span class="sxs-lookup"><span data-stu-id="59c80-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="59c80-121">В поле **Дата запроса** указывается версия.</span><span class="sxs-lookup"><span data-stu-id="59c80-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="59c80-122">Вы можете использовать запрос "как есть" или можете щелкнуть **Изменить запрос**, чтобы изменить критерии.</span><span class="sxs-lookup"><span data-stu-id="59c80-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="59c80-123">Вы можете также изменить имя и описание нового запроса.</span><span class="sxs-lookup"><span data-stu-id="59c80-123">You can optionally modify the name and description of the new query.</span></span>

<a name="additional-resources"></a><span data-ttu-id="59c80-124">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="59c80-124">Additional resources</span></span>
--------

[<span data-ttu-id="59c80-125">Обзор прогнозирования спроса</span><span class="sxs-lookup"><span data-stu-id="59c80-125">Demand forecasting overview</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="59c80-126">Отслеживание точности прогноза</span><span class="sxs-lookup"><span data-stu-id="59c80-126">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)



