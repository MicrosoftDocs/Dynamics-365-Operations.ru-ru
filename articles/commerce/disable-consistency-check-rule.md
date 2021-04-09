---
title: Отключение правил в программе проверки согласованности розничных проводок
description: В этом разделе описываются функции отключения правил программы проверки согласованности проводок в Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: ce2abe7e15773edc3122a1bfdf40f3b830e8790e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792903"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="4cfc8-103">Отключение правил в программе проверки согласованности розничных проводок</span><span class="sxs-lookup"><span data-stu-id="4cfc8-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4cfc8-104">Многие розничные компании используют уникальные бизнес-сценарии и процессы.</span><span class="sxs-lookup"><span data-stu-id="4cfc8-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="4cfc8-105">Поэтому не все правила, по умолчанию включенные в программу проверки согласованности проводок Commerce, применимы для всех продавцов.</span><span class="sxs-lookup"><span data-stu-id="4cfc8-105">Therefore, not all the rules that are included by default in the commerce transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="4cfc8-106">Для учета этих различий в Microsoft Dynamics 365 Commerce предусмотрена возможность отключения неприменимых правил.</span><span class="sxs-lookup"><span data-stu-id="4cfc8-106">To accommodate differences, Microsoft Dynamics 365 Commerce provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="4cfc8-107">Чтобы посмотреть список доступных правил программы проверки согласованности проводок и статус каждого правила, перейдите в раздел **Retail и Commerce \> Настройка центрального офиса \> Параметры \> Параметры Commerce** и откройте вкладку **Проверка проводок**.</span><span class="sxs-lookup"><span data-stu-id="4cfc8-107">To view the list of rules that are available in the transaction consistency checker in your environment, and to see the status of each rule, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="4cfc8-108">По умолчанию каждое правило имеет статус **Включено**.</span><span class="sxs-lookup"><span data-stu-id="4cfc8-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="4cfc8-109">Поэтому для проверки проводок перед их передачей в журналы операций коммерции используются все правила.</span><span class="sxs-lookup"><span data-stu-id="4cfc8-109">Therefore, all the rules are used to validate transactions before they are pulled into the commerce statements.</span></span> <span data-ttu-id="4cfc8-110">Чтобы отключить правило, измените его статус на **Отключено**.</span><span class="sxs-lookup"><span data-stu-id="4cfc8-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="4cfc8-111">Отключенные правила не учитываются при проверке проводок в процессе формирования журнала операций.</span><span class="sxs-lookup"><span data-stu-id="4cfc8-111">Disabled rules aren't considered when transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="4cfc8-112">Чтобы обойти весь процесс проверки независимо от состояния правил, выберите **Retail и Commerce \> Настройка центрального офиса \> Параметры \> Параметры Commerce** и на вкладке **Проверка проводок** выберите для параметра **Отключение программы проверки согласованности для проводок Commerce** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="4cfc8-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Commerce transactions** option to **Yes**.</span></span> <span data-ttu-id="4cfc8-113">Если для этого параметра установлено значение **Нет**, его невозможно изменить на **Да** в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="4cfc8-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]