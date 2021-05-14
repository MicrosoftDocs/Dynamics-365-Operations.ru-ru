---
title: Работа не заблокирована
description: Работа не заблокирована
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924212"
---
# <a name="work-isnt-blocked"></a><span data-ttu-id="ca7f5-103">Работа не заблокирована</span><span class="sxs-lookup"><span data-stu-id="ca7f5-103">Work isn't blocked</span></span>

<span data-ttu-id="ca7f5-104">Код ошибки: WHSUnblockNotBlockedWorkErrorMessage</span><span class="sxs-lookup"><span data-stu-id="ca7f5-104">Error code: WHSUnblockNotBlockedWorkErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="ca7f5-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="ca7f5-105">Symptoms</span></span>

<span data-ttu-id="ca7f5-106">Система отобразит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="ca7f5-106">The system shows the following error message:</span></span>

> <span data-ttu-id="ca7f5-107">Работа с кодом %1 не заблокирована.</span><span class="sxs-lookup"><span data-stu-id="ca7f5-107">Work with Id %1 is not blocked.</span></span>

## <a name="cause"></a><span data-ttu-id="ca7f5-108">Причина</span><span class="sxs-lookup"><span data-stu-id="ca7f5-108">Cause</span></span>

<span data-ttu-id="ca7f5-109">Параметр **Заблокированная волна** в волне задан как *Нет*.</span><span class="sxs-lookup"><span data-stu-id="ca7f5-109">The **Blocked wave** option on the wave is set to *No*.</span></span> <span data-ttu-id="ca7f5-110">Работа не может быть разблокирована, поскольку в данный момент она не заблокирована.</span><span class="sxs-lookup"><span data-stu-id="ca7f5-110">The work can't be unblocked because it isn't currently blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="ca7f5-111">Приказ</span><span class="sxs-lookup"><span data-stu-id="ca7f5-111">Resolution</span></span>

 <span data-ttu-id="ca7f5-112">Может быть разблокирована только та работа, параметр которой **Заблокированная волна** задан как *Да*.</span><span class="sxs-lookup"><span data-stu-id="ca7f5-112">Only work where the **Blocked wave** option is set to *Yes* can be unblocked.</span></span>
