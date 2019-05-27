---
title: Конфигурации параметров для журналов операций розничной торговли
description: Эта процедура демонстрирует конфигурации параметров розничной торговли, которые влияют на то, как создаются и разносятся журналы операций розницы.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6dacd2b80ca0d51d81d2bdf5bc2636b47da621ee
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564301"
---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="60b9f-103">Конфигурации параметров для журналов операций розничной торговли</span><span class="sxs-lookup"><span data-stu-id="60b9f-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="60b9f-104">Эта процедура демонстрирует конфигурации параметров розничной торговли, которые влияют на то, как создаются и разносятся журналы операций розницы.</span><span class="sxs-lookup"><span data-stu-id="60b9f-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="60b9f-105">В данной процедуре используется демонстрационная компания USRT.</span><span class="sxs-lookup"><span data-stu-id="60b9f-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="60b9f-106">Перейдите в раздел "Розничная торговля и коммерция" > "Настройка центрального офиса" > "Параметры" > "Параметры розничной торговли".</span><span class="sxs-lookup"><span data-stu-id="60b9f-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="60b9f-107">Перейдите на вкладку Разноска.</span><span class="sxs-lookup"><span data-stu-id="60b9f-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="60b9f-108">Выберите "Да", если необходимо отдельно разносить периодические суммы скидки.</span><span class="sxs-lookup"><span data-stu-id="60b9f-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="60b9f-109">Выберите "Стандартный" для использования счетов по умолчанию или "Периодический", если вы хотите определить, какой счет будет использоваться для каждой периодической скидки.</span><span class="sxs-lookup"><span data-stu-id="60b9f-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="60b9f-110">Выберите "Сводка", если строки запасов должны по возможности агрегироваться.</span><span class="sxs-lookup"><span data-stu-id="60b9f-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="60b9f-111">Выберите "Да", если накладные и платежи должны автоматически сопоставляться в процессе разноски журнала операций.</span><span class="sxs-lookup"><span data-stu-id="60b9f-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="60b9f-112">Выберите "Да", если должны агрегироваться проводки сдачи наличных средств в сейф.</span><span class="sxs-lookup"><span data-stu-id="60b9f-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="60b9f-113">Выберите "Да", если должны агрегироваться проводки инкассации.</span><span class="sxs-lookup"><span data-stu-id="60b9f-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="60b9f-114">Выберите "Да", чтобы включить агрегирование для разноски журнала операций.</span><span class="sxs-lookup"><span data-stu-id="60b9f-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="60b9f-115">Выберите "Да" для создания и обработки заказов параллельно при разноске журнала операций.</span><span class="sxs-lookup"><span data-stu-id="60b9f-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="60b9f-116">Введите максимальное число заказов для обработки в каждом пакетном задании.</span><span class="sxs-lookup"><span data-stu-id="60b9f-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="60b9f-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="60b9f-117">Click Save.</span></span>

