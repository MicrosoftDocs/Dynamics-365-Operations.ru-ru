---
title: Карточки постоянного клиента и баллы поощрения
description: В этом разделе описывается интеграция сведений о карточках постоянного клиента и баллах вознаграждения между приложениями Finance and Operations и Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e7e67946930404ab7ba0c7fccf468722f723d675
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172977"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="de22d-103">Карточки постоянного клиента и баллы поощрения</span><span class="sxs-lookup"><span data-stu-id="de22d-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="de22d-104">Предприятия классифицируют клиентов и предоставляют развитые услуги на основе шаблонов покупок и расходов клиентов.</span><span class="sxs-lookup"><span data-stu-id="de22d-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="de22d-105">В пакете приложений Microsoft Dynamics 365 приложение Dynamics 365 Commerce имеет инфраструктуру и функции для обеспечения и обработки карточек постоянного клиента, баллов вознаграждения, ценообразования на основе лояльности и покупок на основе вознаграждения.</span><span class="sxs-lookup"><span data-stu-id="de22d-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="de22d-106">Когда данные о карточках постоянных клиентов и баллах вознаграждений в модуле Commerce синхронизируются со службой Common Data Service, приложения на основе модели в Dynamics 365 могут использовать эти данные.</span><span class="sxs-lookup"><span data-stu-id="de22d-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="de22d-107">Например, пользователи Dynamics 365 Customer Service могут использовать эти данные для предоставления тех же развитых услуг в службе поддержки.</span><span class="sxs-lookup"><span data-stu-id="de22d-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="de22d-108">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="de22d-108">Templates</span></span>

| <span data-ttu-id="de22d-109">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="de22d-109">Finance and Operations apps</span></span> | <span data-ttu-id="de22d-110">Приложения на основе модели в Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="de22d-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="de22d-111">описание</span><span class="sxs-lookup"><span data-stu-id="de22d-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="de22d-112">Карта постоянного клиента</span><span class="sxs-lookup"><span data-stu-id="de22d-112">Loyalty card</span></span>                | <span data-ttu-id="de22d-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="de22d-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="de22d-114">Этот шаблон синхронизирует сведения о карточках постоянных клиентов.</span><span class="sxs-lookup"><span data-stu-id="de22d-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="de22d-115">Баллы поощрения по программе лояльности</span><span class="sxs-lookup"><span data-stu-id="de22d-115">Loyalty reward points</span></span>       | <span data-ttu-id="de22d-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="de22d-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="de22d-117">Этот шаблон синхронизирует сведения о баллах вознаграждения клиентов.</span><span class="sxs-lookup"><span data-stu-id="de22d-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]