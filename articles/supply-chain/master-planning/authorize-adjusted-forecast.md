---
title: Авторизация скорректированного прогноза
description: Не все данные прогноза необходимо авторизовать немедленно. Эта статья объясняет, как задать период, для которого авторизован прогноз. Она также объясняет, как авторизовать прогноз для определенных компаний и моделей прогноза.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de7384e94a4b97cf515bb437ad546a8a5f96aa77
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815234"
---
# <a name="authorize-an-adjusted-forecast"></a><span data-ttu-id="7b360-105">Авторизация скорректированного прогноза</span><span class="sxs-lookup"><span data-stu-id="7b360-105">Authorize an adjusted forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b360-106">Не все данные прогноза необходимо авторизовать немедленно.</span><span class="sxs-lookup"><span data-stu-id="7b360-106">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="7b360-107">Эта статья объясняет, как задать период, для которого авторизован прогноз.</span><span class="sxs-lookup"><span data-stu-id="7b360-107">This article explains how you can specify the period that a forecast is authorized for.</span></span> <span data-ttu-id="7b360-108">Она также объясняет, как авторизовать прогноз для определенных компаний и моделей прогноза.</span><span class="sxs-lookup"><span data-stu-id="7b360-108">It also explains how you can authorize the forecast for specific companies and forecast models.</span></span>

<span data-ttu-id="7b360-109">Не все данные прогноза необходимо авторизовать немедленно.</span><span class="sxs-lookup"><span data-stu-id="7b360-109">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="7b360-110">Можно задать начальные и конечные даты периода, для которого авторизован прогноз.</span><span class="sxs-lookup"><span data-stu-id="7b360-110">You can specify the start and end dates of the period that the forecast is authorized for.</span></span> <span data-ttu-id="7b360-111">Эта функциональность позволяет блокировать конкретные периоды.</span><span class="sxs-lookup"><span data-stu-id="7b360-111">This functionality lets you freeze specific buckets.</span></span> 

<span data-ttu-id="7b360-112">Указанные даты начала и окончания должны соответствовать датам начала и окончания периода, в котором создается прогноз.</span><span class="sxs-lookup"><span data-stu-id="7b360-112">The start and end dates that you specify must correspond to the start and end dates of the bucket that the forecast is generated in.</span></span> <span data-ttu-id="7b360-113">Система принудительно применяет это ограничение и автоматически изменяет даты, если требуется корректировка.</span><span class="sxs-lookup"><span data-stu-id="7b360-113">The system enforces this restriction and automatically adjusts the dates, if adjustment is required.</span></span> 

<span data-ttu-id="7b360-114">На вкладке **Сведения** страницы **Авторизация** можно просмотреть сведения о недавно созданном прогнозе.</span><span class="sxs-lookup"><span data-stu-id="7b360-114">On the **Details** tab of the **Authorization** page, you can view details about the forecast that was most recently generated.</span></span> 

<span data-ttu-id="7b360-115">Можно выбрать компании и модели прогноза, чтобы авторизовать прогноз, который требуется использовать.</span><span class="sxs-lookup"><span data-stu-id="7b360-115">You can select the companies and the forecast models to authorize the forecast for use.</span></span> <span data-ttu-id="7b360-116">По умолчанию сетка включает все компании, для которых был создан прогнозируемый спрос.</span><span class="sxs-lookup"><span data-stu-id="7b360-116">By default, the grid includes all the companies that forecast demand has been created for.</span></span> <span data-ttu-id="7b360-117">Для каждой компании модель прогноза, которая соответствует текущему плану прогноза, который настроен в параметрах сводного планирования, заполняется предварительно.</span><span class="sxs-lookup"><span data-stu-id="7b360-117">For each company, the forecast model that corresponds to the current forecast plan that is set up in the master planning parameters is prefilled.</span></span> <span data-ttu-id="7b360-118">Однако можно изменить эту модель прогноза на любую модель прогноза, которая относится к этой компании.</span><span class="sxs-lookup"><span data-stu-id="7b360-118">However, you can change this forecast model to any forecast model that belongs to that company.</span></span> <span data-ttu-id="7b360-119">Если никакие данные прогнозируемого спроса не созданы для выбранной компании, во время импорта отображается предупреждение.</span><span class="sxs-lookup"><span data-stu-id="7b360-119">If no forecast demand data has been generated for a selected company, you receive a warning message at import time.</span></span> 

<span data-ttu-id="7b360-120">Важно понимать принцип работы флажка **Сохранить ручные корректировки базового прогноза спроса**.</span><span class="sxs-lookup"><span data-stu-id="7b360-120">It's very important that you understand how the **Save the manual adjustments made to the baseline demand forecast** check box works.</span></span> <span data-ttu-id="7b360-121">Если внесены ручные коррективы в статистический базовый прогноз, скорректированные значения авторизованы для использования, даже если флажок снят.</span><span class="sxs-lookup"><span data-stu-id="7b360-121">If you've made manual adjustments to the statistical baseline forecast, the adjusted values are authorized for use, even if this check box is cleared.</span></span> <span data-ttu-id="7b360-122">Однако изменения после авторизации сбрасываются.</span><span class="sxs-lookup"><span data-stu-id="7b360-122">However, the changes are discarded after the authorization.</span></span> <span data-ttu-id="7b360-123">Следовательно, в следующий раз при создании прогноза этот прогноз является только статистическим и не имеет никаких переопределений вручную, даже если выбрано значение **Перенести ручные корректировки в прогноз спроса**.</span><span class="sxs-lookup"><span data-stu-id="7b360-123">Therefore, the next time that a forecast is generated, that forecast is only a statistical forecast and doesn't have any manual overrides, even if **Transfer manual adjustments to the demand forecast** is selected.</span></span> <span data-ttu-id="7b360-124">Поэтому можно рассматривать флажок **Сохранить ручные корректировки базового прогноза спроса** как механизм, который позволяет сохранить все внесенные вручную изменения или отказаться от них.</span><span class="sxs-lookup"><span data-stu-id="7b360-124">Therefore, you can consider the **Save the manual adjustments made to the baseline demand forecast** check box a mechanism that lets you keep or discard all manual changes.</span></span>

<a name="additional-resources"></a><span data-ttu-id="7b360-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7b360-125">Additional resources</span></span>
--------

[<span data-ttu-id="7b360-126">Внесение ручных корректировок в базовый прогноз</span><span class="sxs-lookup"><span data-stu-id="7b360-126">Make manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="7b360-127">Отслеживание точности прогноза</span><span class="sxs-lookup"><span data-stu-id="7b360-127">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)



