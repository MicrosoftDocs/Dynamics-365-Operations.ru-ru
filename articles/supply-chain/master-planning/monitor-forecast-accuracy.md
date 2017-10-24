---
title: "Мониторинг точности прогноза"
description: "Эта статья описывает типы точности прогнозов, вычисляемые Microsoft Dynamics 365 for Finance and Operations, и поясняет, как просмотреть значения точности."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c2f9482a9906ad6c607d275769ac06b29b22c25d
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="3d1c2-103">Мониторинг точности прогноза</span><span class="sxs-lookup"><span data-stu-id="3d1c2-103">Monitor forecast accuracy</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3d1c2-104">Эта статья описывает типы точности прогнозов, вычисляемые Microsoft Dynamics 365 for Finance and Operations, и поясняет, как просмотреть значения точности.</span><span class="sxs-lookup"><span data-stu-id="3d1c2-104">This article describes the types of forecast accuracy that Microsoft Dynamics 365 for Finance and Operations calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="3d1c2-105">Finance and Operations вычисляет следующие типы точности прогноза.</span><span class="sxs-lookup"><span data-stu-id="3d1c2-105">Finance and Operations calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="3d1c2-106">Историческая точность прогноза: путем сравнения исторического прогноза, используемого в сводном планировании, с историческим спросом.</span><span class="sxs-lookup"><span data-stu-id="3d1c2-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="3d1c2-107">Для просмотра значений (абсолютных и процентных) исторической точности прогноза щелкните **Показать точность** на странице **Сведения о прогнозе спроса**.</span><span class="sxs-lookup"><span data-stu-id="3d1c2-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="3d1c2-108">Предполагаемая точность модели прогнозирования, которая используется для создания прогнозов.</span><span class="sxs-lookup"><span data-stu-id="3d1c2-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="3d1c2-109">Процент точности можно посмотреть в разделе **Сведения о модели — MAPE** на странице **Сведения о прогнозе спроса**.</span><span class="sxs-lookup"><span data-stu-id="3d1c2-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

<span data-ttu-id="3d1c2-110">**Примечание.** Если используется служба Microsoft Azure Machine Learning прогнозирования спроса Dynamics 365 for Finance and Operations, вычисления точности внутренней модели основываются на тестовом наборе данных.</span><span class="sxs-lookup"><span data-stu-id="3d1c2-110">**Note:** If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="3d1c2-111">Чтобы задать размер тестового набора данных, задайте параметр **TEST\_SET\_SIZE\_PERCENT** на странице **Параметры прогнозирования спроса**.</span><span class="sxs-lookup"><span data-stu-id="3d1c2-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="3d1c2-112">Например, если задать значение равным **20**, последние 20 % исторических данных будут использоваться для вычисления точности внутренней модели.</span><span class="sxs-lookup"><span data-stu-id="3d1c2-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="see-also"></a><span data-ttu-id="3d1c2-113">См. также</span><span class="sxs-lookup"><span data-stu-id="3d1c2-113">See also</span></span>
--------

[<span data-ttu-id="3d1c2-114">Авторизация скорректированного прогноза</span><span class="sxs-lookup"><span data-stu-id="3d1c2-114">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="3d1c2-115">Удаление выбросов из исторических транзакционных данных при расчете прогноза спроса</span><span class="sxs-lookup"><span data-stu-id="3d1c2-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)




