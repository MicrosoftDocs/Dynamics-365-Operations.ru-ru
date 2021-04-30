---
title: Невозможно создать среду в центре администрирования Power Apps
description: В этой статье объясняется, что делать, если администратор не может создать среду в центре администрирования Microsoft Power Apps.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 26a228229a09e74809a048675a3ff90025f2a26c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892235"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="eba0f-103">Невозможно создать среду в центре администрирования Power Apps</span><span class="sxs-lookup"><span data-stu-id="eba0f-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="eba0f-104">**Выдать**</span><span class="sxs-lookup"><span data-stu-id="eba0f-104">**Issue**</span></span>

- <span data-ttu-id="eba0f-105">Администратор владельца/среды не может создать среду в центре администрирования Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="eba0f-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="eba0f-106">У пользователя нет лицензии, которая содержит право на создание сред.</span><span class="sxs-lookup"><span data-stu-id="eba0f-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="eba0f-107">**Решение**</span><span class="sxs-lookup"><span data-stu-id="eba0f-107">**Solution**</span></span>

<span data-ttu-id="eba0f-108">Убедитесь, что администратор клиента назначил действительную лицензию Power Apps P2 для пользователя, создающего среду.</span><span class="sxs-lookup"><span data-stu-id="eba0f-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="eba0f-109">В следующих планах обслуживания Microsoft Dynamics имеются разрешения на создание сред:</span><span class="sxs-lookup"><span data-stu-id="eba0f-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="eba0f-110">Общая единица складского хранения (SKU) продукта</span><span class="sxs-lookup"><span data-stu-id="eba0f-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="eba0f-111">План услуг Power Apps P2</span><span class="sxs-lookup"><span data-stu-id="eba0f-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="eba0f-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="eba0f-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="eba0f-113">Power Apps для Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="eba0f-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="eba0f-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="eba0f-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="eba0f-115">Power Apps для Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="eba0f-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="eba0f-116">Обратите внимание, что различные единицы складского хранения Microsoft Office также предоставляют это право, вместе с автономными единицами складского хранения Power Apps Plan 2.</span><span class="sxs-lookup"><span data-stu-id="eba0f-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="eba0f-117">Важно, что необходимо наличие одной из этих единиц складского хранения.</span><span class="sxs-lookup"><span data-stu-id="eba0f-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="eba0f-118">Перейдите на страницу [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="eba0f-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="eba0f-119">Создайте среды, следуйте инструкциям в разделе [Подготовка Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="eba0f-119">Create the environments by following the instructions in [Provision Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]