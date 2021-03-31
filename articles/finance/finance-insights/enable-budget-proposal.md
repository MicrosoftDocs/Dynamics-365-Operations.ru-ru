---
title: Включение предложений по бюджету (предварительная версия)
description: В этой теме объясняется, как включить функцию предложений по бюджету в финансовом анализе.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 3a2060d082ed55e3b6fac506898916942ccc9db7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208493"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="4a57d-103">Включение предложений по бюджету (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="4a57d-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="4a57d-104">В этой теме объясняется, как включить функцию предложений по бюджету в финансовом анализе.</span><span class="sxs-lookup"><span data-stu-id="4a57d-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="4a57d-105">Используйте информацию со страницы среды в Microsoft Dynamics Lifecycle Services (LCS) для подключения к основному экземпляру Azure SQL для этой среды.</span><span class="sxs-lookup"><span data-stu-id="4a57d-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="4a57d-106">Выполните следующую команду Transact-SQL (T-SQL), чтобы включить фокус-тестирования для среды песочницы.</span><span class="sxs-lookup"><span data-stu-id="4a57d-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="4a57d-107">(Возможно, придется включить доступ для своего IP-адреса в LCS, прежде чем можно будет дистанционно подключиться к серверу Application Object Server \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="4a57d-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="4a57d-108">Если развертывание Microsoft Dynamics 365 Finance является развертыванием Service Fabric, этот шаг можно пропустить</span><span class="sxs-lookup"><span data-stu-id="4a57d-108">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="4a57d-109">Рабочая группа финансового анализа уже должна была включить фокус-тестирование для вас.</span><span class="sxs-lookup"><span data-stu-id="4a57d-109">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="4a57d-110">Если эта функция не отображается в рабочей области **Управление функциями** или при попытке ее включения возникают проблемы, отправьте сообщение электронной почты [рабочей группе предварительной версии приложения финансового анализа](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="4a57d-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, send email to the [Finance Insights App Preview team](mailto:fiap@microsoft.com).</span></span>

2. <span data-ttu-id="4a57d-111">Откройте рабочую область **Управление функциями** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="4a57d-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="4a57d-112">Выберите **Проверить наличие обновлений**.</span><span class="sxs-lookup"><span data-stu-id="4a57d-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="4a57d-113">Выполните поиск **Предложение бюджета** и включите эту функцию.</span><span class="sxs-lookup"><span data-stu-id="4a57d-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="4a57d-114">Перейдите в раздел **Бюджетирование \> Настройка \> Базовое бюджетирование \> Предложение бюджета (предварительная версия)** и выберите **Включить функцию**.</span><span class="sxs-lookup"><span data-stu-id="4a57d-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="4a57d-115">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="4a57d-115">Privacy notice</span></span>
<span data-ttu-id="4a57d-116">Предварительные версии (1) могут использовать меньшую степень конфиденциальности и безопасности, чем сервис Dynamics 365 Finance and Operations, (2) не включаются в соглашение об уровне обслуживания (SLA) для этого сервиса, (3), не должны использоваться для обработки личных данных или других данных, являющихся объектом соответствия юридическим или нормативным требованиям и (4) имеет ограниченную поддержку.</span><span class="sxs-lookup"><span data-stu-id="4a57d-116">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]