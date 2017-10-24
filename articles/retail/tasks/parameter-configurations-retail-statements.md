--- 
title: "Конфигурации параметров для журналов операций розничной торговли"
description: "Эта процедура демонстрирует конфигурации параметров розничной торговли, которые влияют на то, как создаются и разносятся журналы операций розницы."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 731a3ec06efa103ba663df83240c77dfe78bb7cd
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="fd14c-103">Конфигурации параметров для журналов операций розничной торговли</span><span class="sxs-lookup"><span data-stu-id="fd14c-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="fd14c-104">Эта процедура демонстрирует конфигурации параметров розничной торговли, которые влияют на то, как создаются и разносятся журналы операций розницы.</span><span class="sxs-lookup"><span data-stu-id="fd14c-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="fd14c-105">В данной процедуре используется демонстрационная компания USRT.</span><span class="sxs-lookup"><span data-stu-id="fd14c-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="fd14c-106">Перейдите в раздел "Розничная торговля и коммерция" > "Настройка центрального офиса" > "Параметры" > "Параметры розничной торговли".</span><span class="sxs-lookup"><span data-stu-id="fd14c-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="fd14c-107">Перейдите на вкладку Разноска.</span><span class="sxs-lookup"><span data-stu-id="fd14c-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="fd14c-108">Выберите "Да", если необходимо отдельно разносить периодические суммы скидки.</span><span class="sxs-lookup"><span data-stu-id="fd14c-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="fd14c-109">Выберите "Стандартный" для использования счетов по умолчанию или "Периодический", если вы хотите определить, какой счет будет использоваться для каждой периодической скидки.</span><span class="sxs-lookup"><span data-stu-id="fd14c-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="fd14c-110">Выберите "Сводка", если строки запасов должны по возможности агрегироваться.</span><span class="sxs-lookup"><span data-stu-id="fd14c-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="fd14c-111">Выберите "Да", если накладные и платежи должны автоматически сопоставляться в процессе разноски журнала операций.</span><span class="sxs-lookup"><span data-stu-id="fd14c-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="fd14c-112">Выберите "Да", если должны агрегироваться проводки сдачи наличных средств в сейф.</span><span class="sxs-lookup"><span data-stu-id="fd14c-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="fd14c-113">Выберите "Да", если должны агрегироваться проводки инкассации.</span><span class="sxs-lookup"><span data-stu-id="fd14c-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="fd14c-114">Выберите "Да", чтобы включить агрегирование для разноски журнала операций.</span><span class="sxs-lookup"><span data-stu-id="fd14c-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="fd14c-115">Выберите "Да" для создания и обработки заказов параллельно при разноске журнала операций.</span><span class="sxs-lookup"><span data-stu-id="fd14c-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="fd14c-116">Введите максимальное число заказов для обработки в каждом пакетном задании.</span><span class="sxs-lookup"><span data-stu-id="fd14c-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="fd14c-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fd14c-117">Click Save.</span></span>


