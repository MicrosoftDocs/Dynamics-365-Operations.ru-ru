---
title: Отключение правил в программе проверки согласованности проводок
description: В этом разделе описываются функции отключения правил программы проверки согласованности проводок в Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586305"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="01e75-103">Отключение правил в программе проверки согласованности проводок</span><span class="sxs-lookup"><span data-stu-id="01e75-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="01e75-104">Многие розничные компании используют уникальные бизнес-сценарии и процессы.</span><span class="sxs-lookup"><span data-stu-id="01e75-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="01e75-105">Поэтому не все правила, по умолчанию включенные в программу проверки согласованности проводок розничной торговли, применимы для всех продавцов.</span><span class="sxs-lookup"><span data-stu-id="01e75-105">Therefore, not all the rules that are included by default in the retail transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="01e75-106">Для учета этих различий в Microsoft Dynamics 365 Retail предусмотрена возможность отключения неприменимых правил.</span><span class="sxs-lookup"><span data-stu-id="01e75-106">To accommodate differences, Microsoft Dynamics 365 Retail provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="01e75-107">Чтобы посмотреть список доступных правил программы проверки согласованности проводок и статус каждого правила, перейдите в раздел **Розничная торговля \> Настройка центрального офиса \> Параметры \> Параметры розничной торговли** и откройте вкладку **Проверка проводок**.</span><span class="sxs-lookup"><span data-stu-id="01e75-107">To view the list of rules that are available in the retail transaction consistency checker in your environment, and to see the status of each rule, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="01e75-108">По умолчанию каждое правило имеет статус **Включено**.</span><span class="sxs-lookup"><span data-stu-id="01e75-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="01e75-109">Поэтому для проверки проводок перед их передачей в журналы операций розницы используются все правила.</span><span class="sxs-lookup"><span data-stu-id="01e75-109">Therefore, all the rules are used to validate retail transactions before they are pulled into the retail statements.</span></span> <span data-ttu-id="01e75-110">Чтобы отключить правило, измените его статус на **Отключено**.</span><span class="sxs-lookup"><span data-stu-id="01e75-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="01e75-111">Отключенные правила не учитываются при проверке проводок в процессе формирования журнала операций.</span><span class="sxs-lookup"><span data-stu-id="01e75-111">Disabled rules aren't considered when retail transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="01e75-112">Чтобы обойти весь процесс проверки независимо от состояния правил, выберите **Розничная торговля \> Настройка центрального офиса \> Параметры \> Параметры розничной торговли** и на вкладке **Проверка проводок** выберите для параметра **Отключение программы проверки согласованности для проводок розничной торговли** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="01e75-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Retail transactions** option to **Yes**.</span></span> <span data-ttu-id="01e75-113">Если для этого параметра установлено значение **Нет**, его невозможно изменить на **Да** в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="01e75-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>
