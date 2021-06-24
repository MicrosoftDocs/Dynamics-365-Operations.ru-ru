---
title: Включение прогнозирования движения денежных средств (предварительная версия)
description: В этой теме объясняется, как включить функцию прогнозов движения денежных средств в финансовом анализе.
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
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ba8acb2191291e2abed5cabf234c19fe09e6c8ff
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222566"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="76c8d-103">Включение прогнозирования движения денежных средств (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="76c8d-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="76c8d-104">В этой теме объясняется, как включить функцию прогнозов движения денежных средств в финансовом анализе.</span><span class="sxs-lookup"><span data-stu-id="76c8d-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="76c8d-105">Чтобы использовать прогнозы платежей в движении денежных средств, необходимо настроить функцию прогнозирования платежей клиентов, как описано в разделе [Включение прогнозов платежей клиентов](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="76c8d-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="76c8d-106">Используйте информацию со страницы среды в Microsoft Dynamics Lifecycle Services (LCS) для подключения к основному экземпляру Azure SQL для этой среды.</span><span class="sxs-lookup"><span data-stu-id="76c8d-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="76c8d-107">Выполните следующую команду Transact-SQL (T-SQL), чтобы включить фокус-тестирования для среды песочницы.</span><span class="sxs-lookup"><span data-stu-id="76c8d-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="76c8d-108">(Возможно, придется включить доступ для своего IP-адреса в LCS, прежде чем можно будет дистанционно подключиться к серверу Application Object Server \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="76c8d-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="76c8d-109">Пропустите этот шаг, если используется версия 10.0.20 или более поздняя либо используется развертывание с помощью Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="76c8d-109">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="76c8d-110">Рабочая группа финансового анализа уже должна была включить доступ для вас.</span><span class="sxs-lookup"><span data-stu-id="76c8d-110">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="76c8d-111">Если вы не видите эту функцию в рабочей области **Управления функциями** или у вас возникают проблемы при попытке ее включения, обратитесь по адресу <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="76c8d-111">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="76c8d-112">Откройте рабочую область **Управление функциями** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="76c8d-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="76c8d-113">Выберите **Проверить наличие обновлений**.</span><span class="sxs-lookup"><span data-stu-id="76c8d-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="76c8d-114">Включите следующие функции:</span><span class="sxs-lookup"><span data-stu-id="76c8d-114">Turn on the following features:</span></span>

        - <span data-ttu-id="76c8d-115">Новый элемент управления сетки</span><span class="sxs-lookup"><span data-stu-id="76c8d-115">New grid control</span></span>
        - <span data-ttu-id="76c8d-116">Группирование в сетках (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="76c8d-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="76c8d-117">Прогнозирование платежей клиентов (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="76c8d-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="76c8d-118">Прогнозы движения денежных средств (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="76c8d-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="76c8d-119">Перейдите в раздел **Управление банком и кассовыми операциями \> Настройка прогноза движения денежных средств** и добавьте счета денежных средств, которые должны быть включены в прогнозы.</span><span class="sxs-lookup"><span data-stu-id="76c8d-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="76c8d-120">Если не настроены счета денежных средств, движение денежных средств не может быть создано.</span><span class="sxs-lookup"><span data-stu-id="76c8d-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="76c8d-121">Перейдите в раздел **Управление банком и кассовыми операциями \> Настройка \> Финансовый анализ (предварительная версия) \> Прогнозы движения денежных средств (предварительная версия)** и выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="76c8d-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="76c8d-122">На вкладке **Прогноз движения денежных средств** выберите **Включить функцию**.</span><span class="sxs-lookup"><span data-stu-id="76c8d-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="76c8d-123">Выберите **Создать модель прогнозирования**.</span><span class="sxs-lookup"><span data-stu-id="76c8d-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="76c8d-124">Дополнительные сведения о возможности прогнозирования движения денежных средств см. в разделе [Прогнозирование движения денежных средств](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="76c8d-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
