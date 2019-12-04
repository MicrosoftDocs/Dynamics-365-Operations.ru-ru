---
title: Невозможно создать среду в центре администрирования Power Apps
description: В этом разделе объясняется, что делать, если администратор не может создать среду в центре администрирования Microsoft Power Apps.
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
ms.openlocfilehash: 5923c59ab5dde13fed0483972e76634031404fd8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773227"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="7649a-103">Невозможно создать среду в центре администрирования Power Apps</span><span class="sxs-lookup"><span data-stu-id="7649a-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7649a-104">**Выдать**</span><span class="sxs-lookup"><span data-stu-id="7649a-104">**Issue**</span></span>

- <span data-ttu-id="7649a-105">Администратор владельца/среды не может создать среду в центре администрирования Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="7649a-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="7649a-106">Лицензия, дающая пользователям право на выполнение этапа создания среды, еще не была назначена непосредственно пользователю, который выполняет этот этап.</span><span class="sxs-lookup"><span data-stu-id="7649a-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="7649a-107">**Решение**</span><span class="sxs-lookup"><span data-stu-id="7649a-107">**Solution**</span></span>

<span data-ttu-id="7649a-108">Убедитесь в том, что администратор владельца назначил действительную лицензию Power Apps P2 непосредственно пользователю, который будет выполнять этап создания среды.</span><span class="sxs-lookup"><span data-stu-id="7649a-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="7649a-109">Вот планы обслуживания Microsoft Dynamics, которые предоставляют это право.</span><span class="sxs-lookup"><span data-stu-id="7649a-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="7649a-110">Общая единица складского хранения (SKU) продукта</span><span class="sxs-lookup"><span data-stu-id="7649a-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="7649a-111">План услуг Power Apps P2</span><span class="sxs-lookup"><span data-stu-id="7649a-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="7649a-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="7649a-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="7649a-113">Power Apps для Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7649a-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="7649a-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="7649a-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="7649a-115">Power Apps для Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7649a-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="7649a-116">Обратите внимание, что различные единицы складского хранения Microsoft Office также предоставляют это право, вместе с автономными единицами складского хранения Power Apps Plan 2.</span><span class="sxs-lookup"><span data-stu-id="7649a-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="7649a-117">Важно, что необходимо наличие одной из этих единиц складского хранения.</span><span class="sxs-lookup"><span data-stu-id="7649a-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="7649a-118">Перейдите на страницу [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="7649a-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="7649a-119">Создайте среды, следуйте инструкциям в разделе [Подготовка Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="7649a-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
