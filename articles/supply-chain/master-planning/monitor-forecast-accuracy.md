---
title: Отслеживание точности прогноза
description: Эта тема описывает типы точности прогнозов, вычисляемые Dynamics 365 Supply Chain Management, и поясняет, как просмотреть значения точности.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a21e9d6199229438b73bfdf8307030eed60c21bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977946"
---
# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="d49e0-103">Отслеживание точности прогноза</span><span class="sxs-lookup"><span data-stu-id="d49e0-103">Monitor forecast accuracy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d49e0-104">Эта тема описывает типы точности прогнозов, вычисляемые Microsoft Dynamics 365 Supply Chain Management, и поясняет, как просмотреть значения точности.</span><span class="sxs-lookup"><span data-stu-id="d49e0-104">This topic describes the types of forecast accuracy that Microsoft Dynamics 365 Supply Chain Management calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="d49e0-105">Supply Chain Management вычисляет следующие типы точности прогноза.</span><span class="sxs-lookup"><span data-stu-id="d49e0-105">Supply Chain Management calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="d49e0-106">Историческая точность прогноза: путем сравнения исторического прогноза, используемого в сводном планировании, с историческим спросом.</span><span class="sxs-lookup"><span data-stu-id="d49e0-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="d49e0-107">Для просмотра значений (абсолютных и процентных) исторической точности прогноза щелкните **Показать точность** на странице **Сведения о прогнозе спроса**.</span><span class="sxs-lookup"><span data-stu-id="d49e0-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="d49e0-108">Предполагаемая точность модели прогнозирования, которая используется для создания прогнозов.</span><span class="sxs-lookup"><span data-stu-id="d49e0-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="d49e0-109">Процент точности можно посмотреть в разделе **Сведения о модели — MAPE** на странице **Сведения о прогнозе спроса**.</span><span class="sxs-lookup"><span data-stu-id="d49e0-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

> [!NOTE]
> <span data-ttu-id="d49e0-110">Если используется служба прогнозирования спроса Microsoft Azure Machine Learning, вычисления точности внутренней модели основываются на тестовом наборе данных.</span><span class="sxs-lookup"><span data-stu-id="d49e0-110">If you use the Demand forecasting Microsoft Azure Machine Learning, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="d49e0-111">Чтобы задать размер тестового набора данных, задайте параметр **TEST\_SET\_SIZE\_PERCENT** на странице **Параметры прогнозирования спроса**.</span><span class="sxs-lookup"><span data-stu-id="d49e0-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="d49e0-112">Например, если задать значение равным **20**, последние 20 % исторических данных будут использоваться для вычисления точности внутренней модели.</span><span class="sxs-lookup"><span data-stu-id="d49e0-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="additional-resources"></a><span data-ttu-id="d49e0-113">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d49e0-113">Additional resources</span></span>
--------

[<span data-ttu-id="d49e0-114">Авторизация скорректированного прогноза</span><span class="sxs-lookup"><span data-stu-id="d49e0-114">Authorize an adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="d49e0-115">Удаление выбросов из исторических транзакционных данных при расчете прогноза спроса</span><span class="sxs-lookup"><span data-stu-id="d49e0-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)



