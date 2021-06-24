---
title: Включение прогнозов платежей клиентов (предварительная версия)
description: В этой теме объясняется, как включить и настроить функцию прогнозирования платежей клиентов в финансовом анализе.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ae957f592ad9a1237817fec5d4172295f9a53020
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222594"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="d80e2-103">Включение прогнозов платежей клиентов (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="d80e2-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d80e2-104">В этой теме объясняется, как включить и настроить функцию прогнозирования платежей клиентов в финансовом анализе.</span><span class="sxs-lookup"><span data-stu-id="d80e2-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="d80e2-105">Функция включается в рабочей области **Управление функциями** и вводятся параметры конфигурации на странице **Параметры финансового анализа**.</span><span class="sxs-lookup"><span data-stu-id="d80e2-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="d80e2-106">Кроме того, в этой теме содержатся сведения, которые могут помочь эффективно использовать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="d80e2-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="d80e2-107">Перед выполнением следующих шагов обязательно выполните предварительные шаги из раздела [Настройка для финансового анализа](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="d80e2-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="d80e2-108">Используйте информацию со страницы среды в Microsoft Dynamics Lifecycle Services (LCS) для подключения к основному экземпляру Azure SQL для этой среды.</span><span class="sxs-lookup"><span data-stu-id="d80e2-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="d80e2-109">Выполните следующую команду Transact-SQL (T-SQL), чтобы включить фокус-тестирования для среды песочницы.</span><span class="sxs-lookup"><span data-stu-id="d80e2-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="d80e2-110">(Возможно, придется включить доступ для своего IP-адреса в LCS, прежде чем можно будет дистанционно подключиться к серверу Application Object Server \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="d80e2-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('PayPredEnableFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="d80e2-111">Пропустите этот шаг, если используется версия 10.0.20 или более поздняя либо используется развертывание с помощью Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d80e2-111">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="d80e2-112">Рабочая группа финансового анализа уже должна была включить доступ для вас.</span><span class="sxs-lookup"><span data-stu-id="d80e2-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="d80e2-113">Если вы не видите эту функцию в рабочей области **Управления функциями** или у вас возникают проблемы при попытке ее включения, обратитесь по адресу <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="d80e2-113">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span> 

2. <span data-ttu-id="d80e2-114">Включите функцию анализа платежей клиентов:</span><span class="sxs-lookup"><span data-stu-id="d80e2-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="d80e2-115">Перейдите в раздел **Администрирование системы \> Рабочие области \> Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="d80e2-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="d80e2-116">Найдите функцию, которая называется **Анализ платежей клиентов (предварительная версия)**.</span><span class="sxs-lookup"><span data-stu-id="d80e2-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="d80e2-117">Выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="d80e2-117">Select **Enable now**.</span></span>

    <span data-ttu-id="d80e2-118">Функция анализа платежей клиентов теперь включена и готова к настройке.</span><span class="sxs-lookup"><span data-stu-id="d80e2-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="d80e2-119">Настройте функцию анализа платежей клиентов:</span><span class="sxs-lookup"><span data-stu-id="d80e2-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="d80e2-120">Перейти в раздел **Кредит и сбор задолженностей \> Настройка \> Финансовый анализ \> Параметры финансового анализа**.</span><span class="sxs-lookup"><span data-stu-id="d80e2-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="d80e2-121">[![Страница параметров финансового анализа перед настройкой функции](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="d80e2-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="d80e2-122">На странице **Параметры финансового анализа** на вкладке **Анализ платежей клиентов** выберите ссылку **Просмотр полей данных, используемых в модели прогнозирования**, чтобы открыть страницу **Поля данных для модели прогнозирования**.</span><span class="sxs-lookup"><span data-stu-id="d80e2-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="d80e2-123">На ней можно просмотреть список полей по умолчанию, используемых для создания модели прогнозирования искусственного интеллекта (ИИ) для прогнозов платежей клиентов.</span><span class="sxs-lookup"><span data-stu-id="d80e2-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="d80e2-124">Чтобы использовать список полей по умолчанию для создания модели прогноза, закройте страницу **Поля данных для модели прогноза**, затем на странице **Параметры финансового анализа** задайте для параметра **Включить функцию** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="d80e2-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="d80e2-125">Укажите период проводки "С большой задержкой", чтобы определить, что сегмент прогноза **С большой задержкой** означает для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="d80e2-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="d80e2-126">Для каждой открытой накладной система прогнозирует вероятность платежа в трех сегментах: **Вовремя**, **С задержкой** и **С большой задержкой**.</span><span class="sxs-lookup"><span data-stu-id="d80e2-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="d80e2-127">**Вовремя** — этот сегмент включает платежи, которые прогнозируются для оплаты на дату крайнего срока проводки или до нее.</span><span class="sxs-lookup"><span data-stu-id="d80e2-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="d80e2-128">**С задержкой** — этот сегмент включает платежи, которые прогнозируются для оплаты после даты крайнего срока проводки, но до начала периода проводки "С большой задержкой".</span><span class="sxs-lookup"><span data-stu-id="d80e2-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="d80e2-129">**С большой задержкой** — этот сегмент включает платежи, которые прогнозируются для оплаты после начала периода проводки "С большой задержкой".</span><span class="sxs-lookup"><span data-stu-id="d80e2-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="d80e2-130">Если изменить период проводки "С большой задержкой" и выбрать **Изменить позднее пороговое значение** после создания прогнозной модели ИИ для платежей клиентов, существующая прогнозная модель удаляется и создается новая модель.</span><span class="sxs-lookup"><span data-stu-id="d80e2-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="d80e2-131">Новая модель прогнозирования переместит проводки в период "С большой задержкой" на основе введенных настроек, чтобы определить их.</span><span class="sxs-lookup"><span data-stu-id="d80e2-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="d80e2-132">После завершения определения периода проводки "С большой задержкой" выберите **Создать модель прогнозирования**, чтобы создать модель прогнозирования.</span><span class="sxs-lookup"><span data-stu-id="d80e2-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="d80e2-133">В разделе **Модель прогнозирования** страницы **Параметры финансового анализа** отображается статус модели прогнозирования.</span><span class="sxs-lookup"><span data-stu-id="d80e2-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="d80e2-134">В любое время, пока модель прогнозирования создается, можно выбрать **Сброс создания модели** для перезапуска процесса.</span><span class="sxs-lookup"><span data-stu-id="d80e2-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="d80e2-135">Теперь функция настроена и готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="d80e2-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="d80e2-136">После того как функция включена и настроена, а модель прогнозирования создана и работает, в разделе **Модель прогнозирования** страницы **Параметры финансового анализа** отображается точность модели, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="d80e2-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="d80e2-137">[![Точность модели прогнозирования на странице параметров финансового анализа](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="d80e2-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="d80e2-138">Сведения о выпуске</span><span class="sxs-lookup"><span data-stu-id="d80e2-138">Release details</span></span>

<span data-ttu-id="d80e2-139">Общедоступная предварительная версия финансового анализа доступна для пробных развертываний в США, Европе и Соединенном Королевстве.</span><span class="sxs-lookup"><span data-stu-id="d80e2-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="d80e2-140">Корпорация Майкрософт последовательно добавляет поддержку дополнительных регионов.</span><span class="sxs-lookup"><span data-stu-id="d80e2-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="d80e2-141">Общедоступные предварительные версии функций могут и должны быть включены только в средах песочницы уровня 2.</span><span class="sxs-lookup"><span data-stu-id="d80e2-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="d80e2-142">Настройки и модели ИИ, созданные в среде песочницы, не могут быть перенесены в производственную среду.</span><span class="sxs-lookup"><span data-stu-id="d80e2-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="d80e2-143">Дополнительные сведения см. в разделе [Дополнительные условия использования предварительных версий Microsoft Dynamics 365](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span><span class="sxs-lookup"><span data-stu-id="d80e2-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
