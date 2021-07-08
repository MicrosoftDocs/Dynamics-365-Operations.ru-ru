---
title: Параметры для сводного плана не существуют
description: При попытке утверждения спланированного заказа выводится сообщение об ошибке, в котором говорится, что для сводного плана не существует параметров.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294166"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a><span data-ttu-id="96e0e-103">Параметры для сводного плана не существуют</span><span class="sxs-lookup"><span data-stu-id="96e0e-103">Parameters for the master plan don't exist</span></span>

<span data-ttu-id="96e0e-104">Код ошибки: SYS25368</span><span class="sxs-lookup"><span data-stu-id="96e0e-104">Error code: SYS25368</span></span>

## <a name="symptoms"></a><span data-ttu-id="96e0e-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="96e0e-105">Symptoms</span></span>

<span data-ttu-id="96e0e-106">При попытке утвердить спланированный заказ выводится следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="96e0e-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="96e0e-107">Параметры для сводного плана %1 не существуют.</span><span class="sxs-lookup"><span data-stu-id="96e0e-107">Parameters for master plan %1 do not exist.</span></span>

## <a name="cause"></a><span data-ttu-id="96e0e-108">Причина</span><span class="sxs-lookup"><span data-stu-id="96e0e-108">Cause</span></span>

<span data-ttu-id="96e0e-109">Из-за ошибок конфигурации система не может найти настройки для указанного плана.</span><span class="sxs-lookup"><span data-stu-id="96e0e-109">Because of configuration issues, the system can't find the settings for the specified plan.</span></span>

## <a name="resolution"></a><span data-ttu-id="96e0e-110">Решение</span><span class="sxs-lookup"><span data-stu-id="96e0e-110">Resolution</span></span>

- <span data-ttu-id="96e0e-111">Перейдите **Сводное планирование \> Настройка \> Планы \> Сводные планы** и убедитесь, что существует план с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="96e0e-111">Go to **Master planning \> Setup \> Plans \> Master plans**, and make sure that a plan that has the specified name exists.</span></span>
