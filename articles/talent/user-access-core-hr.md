---
title: Пользователь может получить доступ к Core HR, но не к приложению Onboard или Attract
description: В этом разделе объясняется, как решить проблему, когда пользователь имеет доступ к Microsoft Dynamics 365 for Talent Core HR, но не имеет доступа к приложению Attract или Onboard.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "305984"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="83eb4-103">Пользователю доступно Core HR, но недоступно приложение Onboard или Attract</span><span class="sxs-lookup"><span data-stu-id="83eb4-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="83eb4-104">**Сведения среды**</span><span class="sxs-lookup"><span data-stu-id="83eb4-104">**Environment details**</span></span>

- <span data-ttu-id="83eb4-105">Развертывание Microsoft Dynamics Lifecycle Services (LCS) было выполнено пользователем A.</span><span class="sxs-lookup"><span data-stu-id="83eb4-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="83eb4-106">Пользователь А добавил пользователя B в качестве пользователя Microsoft Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="83eb4-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="83eb4-107">**Расход**</span><span class="sxs-lookup"><span data-stu-id="83eb4-107">**Issue**</span></span>

<span data-ttu-id="83eb4-108">Пользователь B имеет доступ к Core HR, но не может получить доступ к приложению Talent: Attract или Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="83eb4-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="83eb4-109">При попытке перейти к разделу **Приложения взаимодействия** вместо этого пользователь попадает в тестовую среду.</span><span class="sxs-lookup"><span data-stu-id="83eb4-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="83eb4-110">**Решение**</span><span class="sxs-lookup"><span data-stu-id="83eb4-110">**Solution**</span></span>

<span data-ttu-id="83eb4-111">Пользователю B необходимо назначить права на просмотр среды Microsoft PowerApps, которую пользователь A создал в процессе подготовки.</span><span class="sxs-lookup"><span data-stu-id="83eb4-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="83eb4-112">Сведения см. в разделе "Предоставление доступа к среде" в статье [Подготовка Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="83eb4-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="83eb4-113">**Долгосрочное решение**</span><span class="sxs-lookup"><span data-stu-id="83eb4-113">**Long-term solution**</span></span>

<span data-ttu-id="83eb4-114">Майкрософт планирует автоматическое назначение соответствующих прав на приложения Onboard и Attract при добавлении пользователя в Core HR.</span><span class="sxs-lookup"><span data-stu-id="83eb4-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
