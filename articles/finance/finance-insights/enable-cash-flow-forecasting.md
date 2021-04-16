---
title: Включение прогнозирования движения денежных средств (предварительная версия)
description: В этой теме объясняется, как включить функцию прогнозов движения денежных средств в финансовом анализе.
author: ShivamPandey-msft
ms.date: 07/24/2020
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
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: f7c06eaeb79c1a2aa319cfa3d2ad8255bf716cd0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818736"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="90d81-103">Включение прогнозирования движения денежных средств (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="90d81-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="90d81-104">В этой теме объясняется, как включить функцию прогнозов движения денежных средств в финансовом анализе.</span><span class="sxs-lookup"><span data-stu-id="90d81-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="90d81-105">Чтобы использовать прогнозы платежей в движении денежных средств, необходимо настроить функцию прогнозирования платежей клиентов, как описано в разделе [Включение прогнозов платежей клиентов](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="90d81-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="90d81-106">Используйте информацию со страницы среды в Microsoft Dynamics Lifecycle Services (LCS) для подключения к основному экземпляру Azure SQL для этой среды.</span><span class="sxs-lookup"><span data-stu-id="90d81-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="90d81-107">Выполните следующую команду Transact-SQL (T-SQL), чтобы включить фокус-тестирования для среды песочницы.</span><span class="sxs-lookup"><span data-stu-id="90d81-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="90d81-108">(Возможно, придется включить доступ для своего IP-адреса в LCS, прежде чем можно будет дистанционно подключиться к серверу Application Object Server \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="90d81-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="90d81-109">Если развертывание Microsoft Dynamics 365 Finance является развертыванием Service Fabric, этот шаг можно пропустить</span><span class="sxs-lookup"><span data-stu-id="90d81-109">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="90d81-110">Рабочая группа финансового анализа уже должна была включить фокус-тестирование для вас.</span><span class="sxs-lookup"><span data-stu-id="90d81-110">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="90d81-111">Если вы не видите эти функции в рабочей области **Управления функциями** или возникают проблемы при попытке их включения, обратитесь по адресу <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="90d81-111">If you don't see the features in the **Feature management** workspace, or if experience issues when you try to turn them on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="90d81-112">Откройте рабочую область **Управление функциями** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="90d81-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="90d81-113">Выберите **Проверить наличие обновлений**.</span><span class="sxs-lookup"><span data-stu-id="90d81-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="90d81-114">Включите следующие функции:</span><span class="sxs-lookup"><span data-stu-id="90d81-114">Turn on the following features:</span></span>

        - <span data-ttu-id="90d81-115">Новый элемент управления сетки</span><span class="sxs-lookup"><span data-stu-id="90d81-115">New grid control</span></span>
        - <span data-ttu-id="90d81-116">Группирование в сетках (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="90d81-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="90d81-117">Прогнозирование платежей клиентов (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="90d81-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="90d81-118">Прогнозы движения денежных средств (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="90d81-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="90d81-119">Перейдите в раздел **Управление банком и кассовыми операциями \> Настройка прогноза движения денежных средств** и добавьте счета денежных средств, которые должны быть включены в прогнозы.</span><span class="sxs-lookup"><span data-stu-id="90d81-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="90d81-120">Если не настроены счета денежных средств, движение денежных средств не может быть создано.</span><span class="sxs-lookup"><span data-stu-id="90d81-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="90d81-121">Перейдите в раздел **Управление банком и кассовыми операциями \> Настройка \> Финансовый анализ (предварительная версия) \> Прогнозы движения денежных средств (предварительная версия)** и выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="90d81-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="90d81-122">На вкладке **Прогноз движения денежных средств** выберите **Включить функцию**.</span><span class="sxs-lookup"><span data-stu-id="90d81-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="90d81-123">Выберите **Создать модель прогнозирования**.</span><span class="sxs-lookup"><span data-stu-id="90d81-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="90d81-124">Дополнительные сведения о возможности прогнозирования движения денежных средств см. в разделе [Прогнозирование движения денежных средств](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="90d81-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="90d81-125">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="90d81-125">Privacy notice</span></span>

<span data-ttu-id="90d81-126">Предварительные версии (1) могут использовать меньшую степень конфиденциальности и безопасности, чем сервис Dynamics 365 Finance and Operations, (2) не включаются в соглашение об уровне обслуживания (SLA) для этого сервиса, (3), не должны использоваться для обработки личных данных или других данных, являющихся объектом соответствия юридическим или нормативным требованиям и (4) имеет ограниченную поддержку.</span><span class="sxs-lookup"><span data-stu-id="90d81-126">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]