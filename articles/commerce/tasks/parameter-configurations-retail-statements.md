---
title: Настройка параметров влияющих на журналы розничных операций
description: Эта тема демонстрирует конфигурации параметров Commerce, которые влияют на то, как создаются и разносятся журналы операций.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023794"
---
# <a name="configure-parameters-that-affect-retail-statements"></a><span data-ttu-id="4dc31-103">Настройка параметров влияющих на журналы розничных операций</span><span class="sxs-lookup"><span data-stu-id="4dc31-103">Configure parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4dc31-104">Эта тема демонстрирует конфигурации параметров Commerce, которые влияют на то, как создаются и разносятся журналы операций.</span><span class="sxs-lookup"><span data-stu-id="4dc31-104">This topic demonstrates configurations for Commerce parameters that affect how statements get created and posted.</span></span> <span data-ttu-id="4dc31-105">В данной процедуре используется демонстрационная компания USRT.</span><span class="sxs-lookup"><span data-stu-id="4dc31-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="4dc31-106">В области переходов выберите **Модули > Retail и Commerce > Настройка центрального офиса > Параметры > Параметры Commerce**.</span><span class="sxs-lookup"><span data-stu-id="4dc31-106">In the navigation pane, go to **Modules > Retail and Commerce > Headquarters setup  > Parameters > Commerce parameters**.</span></span>
2. <span data-ttu-id="4dc31-107">Выберите вкладку **Разноска**.</span><span class="sxs-lookup"><span data-stu-id="4dc31-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="4dc31-108">Выберите **Да**, если необходимо отдельно разносить периодические суммы скидки.</span><span class="sxs-lookup"><span data-stu-id="4dc31-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="4dc31-109">Выберите **Стандартный** для использования счетов по умолчанию или **Периодический**, если вы хотите определить, какой счет будет использоваться для каждой периодической скидки.</span><span class="sxs-lookup"><span data-stu-id="4dc31-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="4dc31-110">Выберите **Сводка**, если строки запасов должны по возможности агрегироваться.</span><span class="sxs-lookup"><span data-stu-id="4dc31-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="4dc31-111">Выберите **Да**, если накладные и платежи должны автоматически сопоставляться в процессе разноски журнала операций.</span><span class="sxs-lookup"><span data-stu-id="4dc31-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="4dc31-112">Выберите **Да**, если должны агрегироваться проводки сдачи наличных средств в сейф.</span><span class="sxs-lookup"><span data-stu-id="4dc31-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="4dc31-113">Выберите **Да**, если должны агрегироваться проводки инкассации.</span><span class="sxs-lookup"><span data-stu-id="4dc31-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="4dc31-114">Выберите **Да**, чтобы включить агрегирование для разноски журнала операций.</span><span class="sxs-lookup"><span data-stu-id="4dc31-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="4dc31-115">Выберите **Да** для создания и обработки заказов параллельно при разноске журнала операций.</span><span class="sxs-lookup"><span data-stu-id="4dc31-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="4dc31-116">Введите максимальное число заказов для обработки в каждом пакетном задании.</span><span class="sxs-lookup"><span data-stu-id="4dc31-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="4dc31-117">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4dc31-117">Select **Save**.</span></span>

