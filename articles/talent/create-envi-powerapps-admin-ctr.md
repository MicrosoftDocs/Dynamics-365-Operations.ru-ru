---
title: Не удается создать среду в центре администрирования PowerApps
description: В этом разделе объясняется, что делать, если администратор не может создать среду в центре администрирования Microsoft PowerApps.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 97d44dc034cb8097fc0ecf9ac4e485425f097102
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "857254"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="07fc9-103">Невозможно создать среду в центре администрирования PowerApps</span><span class="sxs-lookup"><span data-stu-id="07fc9-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="07fc9-104">**Расход**</span><span class="sxs-lookup"><span data-stu-id="07fc9-104">**Issue**</span></span>

- <span data-ttu-id="07fc9-105">Администратор владельца/среды не может создать среду в центре администрирования Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="07fc9-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="07fc9-106">Лицензия, дающая пользователям право на выполнение этапа создания среды, еще не была назначена непосредственно пользователю, который выполняет этот этап.</span><span class="sxs-lookup"><span data-stu-id="07fc9-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="07fc9-107">**Решение**</span><span class="sxs-lookup"><span data-stu-id="07fc9-107">**Solution**</span></span>

<span data-ttu-id="07fc9-108">Убедитесь в том, что администратор владельца назначил действительную лицензию PowerApps P2 непосредственно пользователю, который будет выполнять этап создания среды.</span><span class="sxs-lookup"><span data-stu-id="07fc9-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="07fc9-109">Вот планы обслуживания Microsoft Dynamics, которые предоставляют это право.</span><span class="sxs-lookup"><span data-stu-id="07fc9-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="07fc9-110">Общая единица складского хранения (SKU) продукта</span><span class="sxs-lookup"><span data-stu-id="07fc9-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="07fc9-111">План обслуживания PowerApps P2</span><span class="sxs-lookup"><span data-stu-id="07fc9-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="07fc9-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="07fc9-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="07fc9-113">PowerApps для Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="07fc9-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="07fc9-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="07fc9-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="07fc9-115">PowerApps для Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="07fc9-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="07fc9-116">Обратите внимание, что различные единицы складского хранения Microsoft Office также предоставляют это право, вместе с автономными единицами складского хранения PowerApps Plan 2.</span><span class="sxs-lookup"><span data-stu-id="07fc9-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="07fc9-117">Важно, что необходимо наличие одной из этих единиц складского хранения.</span><span class="sxs-lookup"><span data-stu-id="07fc9-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="07fc9-118">Перейдите на страницу [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="07fc9-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="07fc9-119">Создайте среды, следуйте инструкциям в разделе [Подготовка Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="07fc9-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
