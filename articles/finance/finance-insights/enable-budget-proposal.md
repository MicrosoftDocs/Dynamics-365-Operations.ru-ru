---
title: Включение предложений по бюджету (предварительная версия)
description: В этой теме объясняется, как включить функцию предложений по бюджету в финансовом анализе.
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
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222542"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="91b28-103">Включение предложений по бюджету (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="91b28-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="91b28-104">В этой теме объясняется, как включить функцию предложений по бюджету в финансовом анализе.</span><span class="sxs-lookup"><span data-stu-id="91b28-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="91b28-105">Используйте информацию со страницы среды в Microsoft Dynamics Lifecycle Services (LCS) для подключения к основному экземпляру Azure SQL для этой среды.</span><span class="sxs-lookup"><span data-stu-id="91b28-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="91b28-106">Выполните следующую команду Transact-SQL (T-SQL), чтобы включить фокус-тестирования для среды песочницы.</span><span class="sxs-lookup"><span data-stu-id="91b28-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="91b28-107">(Возможно, придется включить доступ для своего IP-адреса в LCS, прежде чем можно будет дистанционно подключиться к серверу Application Object Server \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="91b28-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="91b28-108">Пропустите этот шаг, если используется версия 10.0.20 или более поздняя либо используется развертывание с помощью Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="91b28-108">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="91b28-109">Рабочая группа финансового анализа уже должна была включить доступ для вас.</span><span class="sxs-lookup"><span data-stu-id="91b28-109">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="91b28-110">Если вы не видите эту функцию в рабочей области **Управления функциями** или у вас возникают проблемы при попытке ее включения, обратитесь по адресу <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="91b28-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="91b28-111">Откройте рабочую область **Управление функциями** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="91b28-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="91b28-112">Выберите **Проверить наличие обновлений**.</span><span class="sxs-lookup"><span data-stu-id="91b28-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="91b28-113">Выполните поиск **Предложение бюджета** и включите эту функцию.</span><span class="sxs-lookup"><span data-stu-id="91b28-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="91b28-114">Перейдите в раздел **Бюджетирование \> Настройка \> Базовое бюджетирование \> Предложение бюджета (предварительная версия)** и выберите **Включить функцию**.</span><span class="sxs-lookup"><span data-stu-id="91b28-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
