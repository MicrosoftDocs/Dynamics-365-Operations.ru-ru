---
title: Пользователь может получить доступ к Core HR, но не к приложению Onboard или Attract
description: В этом разделе объясняется, как решить проблему, когда пользователь имеет доступ к Microsoft Dynamics 365 for Talent Core HR, но не имеет доступа к приложению Attract или Onboard.
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
ms.openlocfilehash: ece6a81c54ef1421284fc79ab82ed3e31a972255
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "855664"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="d0dff-103">Пользователю доступно Core HR, но недоступно приложение Onboard или Attract</span><span class="sxs-lookup"><span data-stu-id="d0dff-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d0dff-104">**Сведения среды**</span><span class="sxs-lookup"><span data-stu-id="d0dff-104">**Environment details**</span></span>

- <span data-ttu-id="d0dff-105">Развертывание Microsoft Dynamics Lifecycle Services (LCS) было выполнено пользователем A.</span><span class="sxs-lookup"><span data-stu-id="d0dff-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="d0dff-106">Пользователь А добавил пользователя B в качестве пользователя Microsoft Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="d0dff-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="d0dff-107">**Расход**</span><span class="sxs-lookup"><span data-stu-id="d0dff-107">**Issue**</span></span>

<span data-ttu-id="d0dff-108">Пользователь B имеет доступ к Core HR, но не может получить доступ к приложению Talent: Attract или Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="d0dff-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="d0dff-109">При попытке перейти к разделу **Приложения взаимодействия** вместо этого пользователь попадает в тестовую среду.</span><span class="sxs-lookup"><span data-stu-id="d0dff-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="d0dff-110">**Решение**</span><span class="sxs-lookup"><span data-stu-id="d0dff-110">**Solution**</span></span>

<span data-ttu-id="d0dff-111">Пользователю B необходимо назначить права на просмотр среды Microsoft PowerApps, которую пользователь A создал в процессе подготовки.</span><span class="sxs-lookup"><span data-stu-id="d0dff-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="d0dff-112">Сведения см. в разделе "Предоставление доступа к среде" в статье [Подготовка Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="d0dff-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="d0dff-113">**Долгосрочное решение**</span><span class="sxs-lookup"><span data-stu-id="d0dff-113">**Long-term solution**</span></span>

<span data-ttu-id="d0dff-114">Майкрософт планирует автоматическое назначение соответствующих прав на приложения Onboard и Attract при добавлении пользователя в Core HR.</span><span class="sxs-lookup"><span data-stu-id="d0dff-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
