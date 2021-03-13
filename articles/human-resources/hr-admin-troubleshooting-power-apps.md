---
title: Невозможно создать среду в центре администрирования Power Apps
description: В этой статье объясняется, что делать, если администратор не может создать среду в центре администрирования Microsoft Power Apps.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 664c644c9b34e3489b4134040e165d26202dbd38
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114001"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="06865-103">Невозможно создать среду в центре администрирования Power Apps</span><span class="sxs-lookup"><span data-stu-id="06865-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="06865-104">**Выдать**</span><span class="sxs-lookup"><span data-stu-id="06865-104">**Issue**</span></span>

- <span data-ttu-id="06865-105">Администратор владельца/среды не может создать среду в центре администрирования Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="06865-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="06865-106">У пользователя нет лицензии, которая содержит право на создание сред.</span><span class="sxs-lookup"><span data-stu-id="06865-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="06865-107">**Решение**</span><span class="sxs-lookup"><span data-stu-id="06865-107">**Solution**</span></span>

<span data-ttu-id="06865-108">Убедитесь, что администратор клиента назначил действительную лицензию Power Apps P2 для пользователя, создающего среду.</span><span class="sxs-lookup"><span data-stu-id="06865-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="06865-109">В следующих планах обслуживания Microsoft Dynamics имеются разрешения на создание сред:</span><span class="sxs-lookup"><span data-stu-id="06865-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="06865-110">Общая единица складского хранения (SKU) продукта</span><span class="sxs-lookup"><span data-stu-id="06865-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="06865-111">План услуг Power Apps P2</span><span class="sxs-lookup"><span data-stu-id="06865-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="06865-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="06865-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="06865-113">Power Apps для Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="06865-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="06865-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="06865-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="06865-115">Power Apps для Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="06865-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="06865-116">Обратите внимание, что различные единицы складского хранения Microsoft Office также предоставляют это право, вместе с автономными единицами складского хранения Power Apps Plan 2.</span><span class="sxs-lookup"><span data-stu-id="06865-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="06865-117">Важно, что необходимо наличие одной из этих единиц складского хранения.</span><span class="sxs-lookup"><span data-stu-id="06865-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="06865-118">Перейдите на страницу [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="06865-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="06865-119">Создайте среды, следуйте инструкциям в разделе [Подготовка Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="06865-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
