---
title: Улучшение модели прогнозирования (предварительная версия)
description: В этой теме описываются функции, которые можно использовать для повышения эффективности моделей прогноза.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 2bcdea4a2a8f4386b274077cd1e95398fb6fac37
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009378"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="68819-103">Улучшение модели прогнозирования (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="68819-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="68819-104">В этой теме описываются функции, которые можно использовать для повышения эффективности моделей прогноза.</span><span class="sxs-lookup"><span data-stu-id="68819-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="68819-105">Вы начинаете совершенствовать свою модель в рабочей области **Прогнозы платежей клиентов** в Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="68819-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="68819-106">Этапы улучшения затем выполняются в AI Builder.</span><span class="sxs-lookup"><span data-stu-id="68819-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="68819-107">Выбор исторических результатов</span><span class="sxs-lookup"><span data-stu-id="68819-107">Select historical outcomes</span></span>

<span data-ttu-id="68819-108">Сначала необходимо выбрать один или несколько из трех возможных результатов для накладных: **Вовремя**, **С задержкой** и **С большой задержкой**.</span><span class="sxs-lookup"><span data-stu-id="68819-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="68819-109">Должны быть выбраны все три результата.</span><span class="sxs-lookup"><span data-stu-id="68819-109">All three outcomes should be selected.</span></span> <span data-ttu-id="68819-110">Если снять выделение каких-либо результатов, накладные будут отфильтрованы из процесса обучения, и точность прогноза будет уменьшена.</span><span class="sxs-lookup"><span data-stu-id="68819-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="68819-111">[![Подтверждение результатов](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="68819-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="68819-112">Если вашей организации требуется только два результата, измените пороговые значения **С задержкой** и **С большой задержкой** на 0 (ноль) дней.</span><span class="sxs-lookup"><span data-stu-id="68819-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="68819-113">Таким образом, можно эффективно свернуть прогноз до двоичного состояния **Вовремя** и **С задержкой**.</span><span class="sxs-lookup"><span data-stu-id="68819-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="68819-114">Выбрать поля</span><span class="sxs-lookup"><span data-stu-id="68819-114">Select fields</span></span>

<span data-ttu-id="68819-115">При выборе полей, включаемых в модель, имейте в виду, что список включает все доступные поля в таблице Microsoft Dataverse, сопоставленной с данными в Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="68819-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="68819-116">Некоторые из этих полей **не должны** быть выбраны.</span><span class="sxs-lookup"><span data-stu-id="68819-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="68819-117">Поля, которые не должны быть выбраны, попадают в одну из трех категорий:</span><span class="sxs-lookup"><span data-stu-id="68819-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="68819-118">Поле является обязательным для таблицы Dataverse, но в Data Lake нет поддерживающих его данных.</span><span class="sxs-lookup"><span data-stu-id="68819-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="68819-119">Это поле является идентификатором и поэтому не имеет смысла для функции машинного обучения.</span><span class="sxs-lookup"><span data-stu-id="68819-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="68819-120">Поле представляет информацию, которая не будет доступна при прогнозировании.</span><span class="sxs-lookup"><span data-stu-id="68819-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="68819-121">В следующих разделах показаны поля, доступные для сущностей накладной и клиента, и перечислены поля, которые **не следует** выбирать для обучения.</span><span class="sxs-lookup"><span data-stu-id="68819-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="68819-122">Категория, которая указана для каждого из этих полей, ссылается на категории в предыдущем списке.</span><span class="sxs-lookup"><span data-stu-id="68819-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="68819-123">Таблица накладной Dataverse</span><span class="sxs-lookup"><span data-stu-id="68819-123">Invoice Dataverse table</span></span>

<span data-ttu-id="68819-124">На следующем рисунке показаны поля, которые доступны для таблицы накладной.</span><span class="sxs-lookup"><span data-stu-id="68819-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="68819-125">[![Доступные поля для таблицы накладной](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="68819-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="68819-126">Следующие поля не должны выбираться для обучения:</span><span class="sxs-lookup"><span data-stu-id="68819-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="68819-127">**Счет накладной** (категория 2)</span><span class="sxs-lookup"><span data-stu-id="68819-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="68819-128">**Закрыто** (категория 3) — это поле используется для фильтрации накладных для обучения (закрыто) и прогнозирования (не закрыто).</span><span class="sxs-lookup"><span data-stu-id="68819-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="68819-129">**Имя** (категория 1)</span><span class="sxs-lookup"><span data-stu-id="68819-129">**Name** (category 1)</span></span>
- <span data-ttu-id="68819-130">**Код источника** (категория 2)</span><span class="sxs-lookup"><span data-stu-id="68819-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="68819-131">**Запись источника** (категория 2)</span><span class="sxs-lookup"><span data-stu-id="68819-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="68819-132">**Таблица источника** (категория 2)</span><span class="sxs-lookup"><span data-stu-id="68819-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="68819-133">Таблица клиента Dataverse</span><span class="sxs-lookup"><span data-stu-id="68819-133">Customer Dataverse table</span></span>

<span data-ttu-id="68819-134">На следующем рисунке показаны поля, которые доступны для таблицы клиента.</span><span class="sxs-lookup"><span data-stu-id="68819-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="68819-135">[![Доступные поля для таблицы клиента](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="68819-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="68819-136">Следующее поле не должно выбираться для обучения:</span><span class="sxs-lookup"><span data-stu-id="68819-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="68819-137">**Уникальный ключ строки** (категория 2)</span><span class="sxs-lookup"><span data-stu-id="68819-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="68819-138">Фильтры</span><span class="sxs-lookup"><span data-stu-id="68819-138">Filters</span></span>

<span data-ttu-id="68819-139">В настоящее время фильтры не поддерживают сценарий прогноза платежей клиентов.</span><span class="sxs-lookup"><span data-stu-id="68819-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="68819-140">Поэтому выберите **Пропустить этот шаг** и перейдите на сводную страницу.</span><span class="sxs-lookup"><span data-stu-id="68819-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="68819-141">[![Модель фокусировки с фильтрами](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="68819-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="68819-142">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="68819-142">Privacy notice</span></span>
<span data-ttu-id="68819-143">Предварительные версии (1) могут использовать меньшую степень конфиденциальности и безопасности, чем сервис Dynamics 365 Finance and Operations, (2) не включаются в соглашение об уровне обслуживания (SLA) для этого сервиса, (3), не должны использоваться для обработки личных данных или других данных, являющихся объектом соответствия юридическим или нормативным требованиям и (4) имеет ограниченную поддержку.</span><span class="sxs-lookup"><span data-stu-id="68819-143">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
