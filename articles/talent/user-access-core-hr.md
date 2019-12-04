---
title: Пользователю доступно Core HR, но недоступны Onboard или Attract
description: В этом разделе объясняется, как решить проблему, когда пользователь имеет доступ к Microsoft Dynamics 365 Talent - Core HR, но не имеет доступа к Attract или Onboard.
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
ms.openlocfilehash: 1a86936d756d8375761ce50c9d9bf33dc638dfad
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772927"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a><span data-ttu-id="639d8-103">Пользователю доступно Core HR, но недоступны Onboard или Attract</span><span class="sxs-lookup"><span data-stu-id="639d8-103">User can access Core HR but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="639d8-104">**Сведения среды**</span><span class="sxs-lookup"><span data-stu-id="639d8-104">**Environment details**</span></span>

- <span data-ttu-id="639d8-105">Развертывание Microsoft Dynamics Lifecycle Services (LCS) было выполнено пользователем A.</span><span class="sxs-lookup"><span data-stu-id="639d8-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="639d8-106">Пользователь А добавил пользователя B в качестве пользователя Microsoft Dynamics 365 Talent: Core HR.</span><span class="sxs-lookup"><span data-stu-id="639d8-106">User A added user B as a user to Microsoft Dynamics 365 Talent: Core HR.</span></span>

<span data-ttu-id="639d8-107">**Выдать**</span><span class="sxs-lookup"><span data-stu-id="639d8-107">**Issue**</span></span>

<span data-ttu-id="639d8-108">Пользователь B имеет доступ к Core HR, но не может получить доступ к приложению Talent: Attract или Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="639d8-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="639d8-109">При попытке перейти к разделу **Приложения взаимодействия** вместо этого пользователь попадает в тестовую среду.</span><span class="sxs-lookup"><span data-stu-id="639d8-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="639d8-110">**Решение**</span><span class="sxs-lookup"><span data-stu-id="639d8-110">**Solution**</span></span>

<span data-ttu-id="639d8-111">Пользователю B необходимо назначить права на просмотр среды Microsoft Power Apps, которую пользователь A создал в процессе подготовки.</span><span class="sxs-lookup"><span data-stu-id="639d8-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="639d8-112">Сведения см. в разделе "Предоставление доступа к среде" в статье [Подготовка Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="639d8-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="639d8-113">**Долгосрочное решение**</span><span class="sxs-lookup"><span data-stu-id="639d8-113">**Long-term solution**</span></span>

<span data-ttu-id="639d8-114">Майкрософт планирует автоматическое назначение соответствующих прав на приложения Onboard и Attract при добавлении пользователя в Core HR.</span><span class="sxs-lookup"><span data-stu-id="639d8-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
