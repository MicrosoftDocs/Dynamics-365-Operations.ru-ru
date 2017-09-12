---
title: "Настройка оповещений о мошенничестве"
description: "В этом разделе описывается, как настроить правила для предупреждения представителей отдела обслуживания клиентов о потенциально мошеннической информации при обработке заказов. Можно определить специальные коды, чтобы блокировать подозрительные заказы автоматически или вручную."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: ru-ru
ms.lasthandoff: 06/29/2017



---

# <a name="set-up-fraud-alerts"></a><span data-ttu-id="303f1-104">Настройка оповещений о мошенничестве</span><span class="sxs-lookup"><span data-stu-id="303f1-104">Set up fraud alerts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="303f1-105">В этом разделе описывается, как настроить правила для предупреждения представителей отдела обслуживания клиентов о потенциально мошеннической информации при обработке заказов.</span><span class="sxs-lookup"><span data-stu-id="303f1-105">This topic explains how to set up rules to alert customer service representatives of potentially fraudulent information when orders are processed.</span></span> <span data-ttu-id="303f1-106">Можно определить специальные коды, чтобы блокировать подозрительные заказы автоматически или вручную.</span><span class="sxs-lookup"><span data-stu-id="303f1-106">You can define specific codes to use to automatically or manually put suspicious orders on hold.</span></span> 

<span data-ttu-id="303f1-107">Перед настройкой правил проверки на мошенничество необходимо включить проверку на мошенничество и определить базовые значения проверки на мошенничество в параметрах центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="303f1-107">Before you set up and use fraud checking rules, you must enable fraud checking and define the basic fraud checking values in the call center parameters.</span></span> <span data-ttu-id="303f1-108">Существует два типа правил проверки на мошенничество:</span><span class="sxs-lookup"><span data-stu-id="303f1-108">There are two types of fraud rules:</span></span>

-   <span data-ttu-id="303f1-109">**Статические правила** предполагают использование конкретного значения, такого как номер телефона, занесенный в черный список.</span><span class="sxs-lookup"><span data-stu-id="303f1-109">**Static rules** use a specific value, such as a phone number that has been blacklisted.</span></span>
-   <span data-ttu-id="303f1-110">**Динамические правила** могут состоять из переменных и условий.</span><span class="sxs-lookup"><span data-stu-id="303f1-110">**Dynamic rules** can be composed from variables and conditions.</span></span>

<span data-ttu-id="303f1-111">Прежде чем создавать динамическое правило, необходимо создать переменные и условия, определяющие, к кому и когда будет применяться правило.</span><span class="sxs-lookup"><span data-stu-id="303f1-111">Before you create a dynamic rule, you must create the variables and conditions that define who the rule applies to and when the rule should be applied.</span></span> <span data-ttu-id="303f1-112">К примеру, необходимо создать правило, согласно которому, когда клиент 1202 размещает заказ на продажу стоимостью 1000,00 или более, заказ на продажу необходимо блокировать до проверки платежа клиента.</span><span class="sxs-lookup"><span data-stu-id="303f1-112">For example, you want to create a rule to require that any sales order that customer 1202 places that is worth 1,000.00 or more be put on hold until the customer payment can be verified.</span></span> <span data-ttu-id="303f1-113">В этом случае переменными являются клиент 1202 и общая сумма заказа 1000,00.</span><span class="sxs-lookup"><span data-stu-id="303f1-113">In this case, the variables are customer 1202 and an order total of 1,000.00.</span></span> <span data-ttu-id="303f1-114">Условие означает, что, если клиент 1202 размещает заказ и общая сумма заказа равна или больше 1000,00, заказ на продажу должен быть блокирован до тех пор, пока не будет проверен платеж клиента.</span><span class="sxs-lookup"><span data-stu-id="303f1-114">The condition specifies that if customer 1202 places an order, and the total amount of the order is equal to or more than 1,000.00, the sales order must be put on hold until the customer payment can be verified.</span></span>




