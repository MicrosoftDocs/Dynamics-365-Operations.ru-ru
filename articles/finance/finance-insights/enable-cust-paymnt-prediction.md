---
title: Включение прогнозов платежей клиентов (предварительная версия)
description: В этой теме объясняется, как включить и настроить функцию прогнозирования платежей клиентов в финансовом анализе.
author: ShivamPandey-msft
ms.date: 05/27/2020
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
ms.openlocfilehash: ecc3851cc91c8fe17a7582f2be06e84cf9bc2d83
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818664"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="d7830-103">Включение прогнозов платежей клиентов (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="d7830-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d7830-104">В этой теме объясняется, как включить и настроить функцию прогнозирования платежей клиентов в финансовом анализе.</span><span class="sxs-lookup"><span data-stu-id="d7830-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="d7830-105">Функция включается в рабочей области **Управление функциями** и вводятся параметры конфигурации на странице **Параметры финансового анализа**.</span><span class="sxs-lookup"><span data-stu-id="d7830-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="d7830-106">Кроме того, в этой теме содержатся сведения, которые могут помочь эффективно использовать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="d7830-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="d7830-107">Перед выполнением следующих шагов обязательно выполните предварительные шаги из раздела [Настройка для финансового анализа](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="d7830-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="d7830-108">Используйте информацию со страницы среды в Microsoft Dynamics Lifecycle Services (LCS) для подключения к основному экземпляру Azure SQL для этой среды.</span><span class="sxs-lookup"><span data-stu-id="d7830-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="d7830-109">Выполните следующую команду Transact-SQL (T-SQL), чтобы включить фокус-тестирования для среды песочницы.</span><span class="sxs-lookup"><span data-stu-id="d7830-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="d7830-110">(Возможно, придется включить доступ для своего IP-адреса в LCS, прежде чем можно будет дистанционно подключиться к серверу Application Object Server \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="d7830-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > <span data-ttu-id="d7830-111">Если развертывание Microsoft Dynamics 365 Finance является развертыванием Service Fabric, этот шаг можно пропустить</span><span class="sxs-lookup"><span data-stu-id="d7830-111">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="d7830-112">Рабочая группа финансового анализа уже должна была включить доступ для вас.</span><span class="sxs-lookup"><span data-stu-id="d7830-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="d7830-113">Если вы не видите эту функцию в рабочей области **Управления функциями** или возникают проблемы при попытке ее включения, обратитесь по адресу <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="d7830-113">If you don't see the feature in the **Feature management** workspace, or if experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="d7830-114">Включите функцию анализа платежей клиентов:</span><span class="sxs-lookup"><span data-stu-id="d7830-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="d7830-115">Перейдите в раздел **Администрирование системы \> Рабочие области \> Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="d7830-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="d7830-116">Найдите функцию, которая называется **Анализ платежей клиентов (предварительная версия)**.</span><span class="sxs-lookup"><span data-stu-id="d7830-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="d7830-117">Выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="d7830-117">Select **Enable now**.</span></span>

    <span data-ttu-id="d7830-118">Функция анализа платежей клиентов теперь включена и готова к настройке.</span><span class="sxs-lookup"><span data-stu-id="d7830-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="d7830-119">Настройте функцию анализа платежей клиентов:</span><span class="sxs-lookup"><span data-stu-id="d7830-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="d7830-120">Перейти в раздел **Кредит и сбор задолженностей \> Настройка \> Финансовый анализ \> Параметры финансового анализа**.</span><span class="sxs-lookup"><span data-stu-id="d7830-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="d7830-121">[![Страница параметров финансового анализа перед настройкой функции](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="d7830-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="d7830-122">На странице **Параметры финансового анализа** на вкладке **Анализ платежей клиентов** выберите ссылку **Просмотр полей данных, используемых в модели прогнозирования**, чтобы открыть страницу **Поля данных для модели прогнозирования**.</span><span class="sxs-lookup"><span data-stu-id="d7830-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="d7830-123">На ней можно просмотреть список полей по умолчанию, используемых для создания модели прогнозирования искусственного интеллекта (ИИ) для прогнозов платежей клиентов.</span><span class="sxs-lookup"><span data-stu-id="d7830-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="d7830-124">Чтобы использовать список полей по умолчанию для создания модели прогноза, закройте страницу **Поля данных для модели прогноза**, затем на странице **Параметры финансового анализа** задайте для параметра **Включить функцию** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="d7830-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="d7830-125">Укажите период проводки "С большой задержкой", чтобы определить, что сегмент прогноза **С большой задержкой** означает для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="d7830-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="d7830-126">Для каждой открытой накладной система прогнозирует вероятность платежа в трех сегментах: **Вовремя**, **С задержкой** и **С большой задержкой**.</span><span class="sxs-lookup"><span data-stu-id="d7830-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="d7830-127">**Вовремя** — этот сегмент включает платежи, которые прогнозируются для оплаты на дату крайнего срока проводки или до нее.</span><span class="sxs-lookup"><span data-stu-id="d7830-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="d7830-128">**С задержкой** — этот сегмент включает платежи, которые прогнозируются для оплаты после даты крайнего срока проводки, но до начала периода проводки "С большой задержкой".</span><span class="sxs-lookup"><span data-stu-id="d7830-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="d7830-129">**С большой задержкой** — этот сегмент включает платежи, которые прогнозируются для оплаты после начала периода проводки "С большой задержкой".</span><span class="sxs-lookup"><span data-stu-id="d7830-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="d7830-130">Если изменить период проводки "С большой задержкой" и выбрать **Изменить позднее пороговое значение** после создания прогнозной модели ИИ для платежей клиентов, существующая прогнозная модель удаляется и создается новая модель.</span><span class="sxs-lookup"><span data-stu-id="d7830-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="d7830-131">Новая модель прогнозирования переместит проводки в период "С большой задержкой" на основе введенных настроек, чтобы определить их.</span><span class="sxs-lookup"><span data-stu-id="d7830-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="d7830-132">После завершения определения периода проводки "С большой задержкой" выберите **Создать модель прогнозирования**, чтобы создать модель прогнозирования.</span><span class="sxs-lookup"><span data-stu-id="d7830-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="d7830-133">В разделе **Модель прогнозирования** страницы **Параметры финансового анализа** отображается статус модели прогнозирования.</span><span class="sxs-lookup"><span data-stu-id="d7830-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="d7830-134">В любое время, пока модель прогнозирования создается, можно выбрать **Сброс создания модели** для перезапуска процесса.</span><span class="sxs-lookup"><span data-stu-id="d7830-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="d7830-135">Теперь функция настроена и готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="d7830-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="d7830-136">После того как функция включена и настроена, а модель прогнозирования создана и работает, в разделе **Модель прогнозирования** страницы **Параметры финансового анализа** отображается точность модели, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="d7830-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="d7830-137">[![Точность модели прогнозирования на странице параметров финансового анализа](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="d7830-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="d7830-138">Сведения о выпуске</span><span class="sxs-lookup"><span data-stu-id="d7830-138">Release details</span></span>

<span data-ttu-id="d7830-139">Общедоступная предварительная версия финансового анализа доступна для пробных развертываний в США, Европе и Соединенном Королевстве.</span><span class="sxs-lookup"><span data-stu-id="d7830-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="d7830-140">Корпорация Майкрософт последовательно добавляет поддержку дополнительных регионов.</span><span class="sxs-lookup"><span data-stu-id="d7830-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="d7830-141">Общедоступные предварительные версии функций могут и должны быть включены только в средах песочницы уровня 2.</span><span class="sxs-lookup"><span data-stu-id="d7830-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="d7830-142">Настройки и модели ИИ, созданные в среде песочницы, не могут быть перенесены в производственную среду.</span><span class="sxs-lookup"><span data-stu-id="d7830-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="d7830-143">Дополнительные сведения см. в разделе [Дополнительные условия использования предварительных версий Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span><span class="sxs-lookup"><span data-stu-id="d7830-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="d7830-144">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="d7830-144">Privacy notice</span></span>

<span data-ttu-id="d7830-145">Предварительные версии (1) могут использовать меньшую степень конфиденциальности и безопасности, чем сервис Dynamics 365 Finance and Operations, (2) не включаются в соглашение об уровне обслуживания (SLA) для этого сервиса, (3), не должны использоваться для обработки личных данных или других данных, являющихся объектом соответствия юридическим или нормативным требованиям и (4) имеет ограниченную поддержку.</span><span class="sxs-lookup"><span data-stu-id="d7830-145">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]