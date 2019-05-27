---
title: Клиент Talent отключается
description: В этом разделе объясняется, что делать, если клиент отключен от свой среды и не знает, почему.
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
ms.openlocfilehash: 885e2d743cd2b01588546327840508f6f7e95958
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518893"
---
# <a name="talent-client-disconnects"></a><span data-ttu-id="bb17c-103">Клиент Talent отключается</span><span class="sxs-lookup"><span data-stu-id="bb17c-103">Talent client disconnects</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bb17c-104">**Сведения среды**</span><span class="sxs-lookup"><span data-stu-id="bb17c-104">**Environment details**</span></span> 

<span data-ttu-id="bb17c-105">Эта проблема может возникнуть во всех средах.</span><span class="sxs-lookup"><span data-stu-id="bb17c-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="bb17c-106">**Симптом**</span><span class="sxs-lookup"><span data-stu-id="bb17c-106">**Symptom**</span></span> 

<span data-ttu-id="bb17c-107">Клиент отключен от свой среды и не знает, почему.</span><span class="sxs-lookup"><span data-stu-id="bb17c-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="bb17c-108">Клиент получает одно из следующих сообщений об ошибке:</span><span class="sxs-lookup"><span data-stu-id="bb17c-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="bb17c-109">Потеряно подключение.</span><span class="sxs-lookup"><span data-stu-id="bb17c-109">We've lost your connection.</span></span> <span data-ttu-id="bb17c-110">Нажмите кнопку "Закрыть" для продолжения работы.</span><span class="sxs-lookup"><span data-stu-id="bb17c-110">Click Close to continue working.</span></span>
- <span data-ttu-id="bb17c-111">Похоже, что потеряно подключение к сети; нажмите кнопку "Повторить", чтобы повторить попытку.</span><span class="sxs-lookup"><span data-stu-id="bb17c-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="bb17c-112">**Красный флаг**</span><span class="sxs-lookup"><span data-stu-id="bb17c-112">**Red flag**</span></span>

<span data-ttu-id="bb17c-113">Эта проблема часто возникает, когда пользователи находятся на этапе реализации, выполняют сравнение сведений по производственным и тестовым средам и забывают, что они перемещаются между сеансами.</span><span class="sxs-lookup"><span data-stu-id="bb17c-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="bb17c-114">Если пользователи находятся на этом этапе, они скорее всего столкнутся с этой проблемой.</span><span class="sxs-lookup"><span data-stu-id="bb17c-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="bb17c-115">**Расход**</span><span class="sxs-lookup"><span data-stu-id="bb17c-115">**Issue**</span></span> 

<span data-ttu-id="bb17c-116">**Типы браузеров:** Google Chrome, Internet Explorer и Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bb17c-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="bb17c-117">Платформа Microsoft Dynamics 365 for Talent отключает пользователей, когда одновременно открыто два разных сеанса для одного пользователя и одного типа браузера.</span><span class="sxs-lookup"><span data-stu-id="bb17c-117">The Microsoft Dynamics 365 for Talent platform disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="bb17c-118">(Например, пользователь А просматривает как среду 1, так и среду 2 в Chrome.) Не имеет значения, открыли ли пользователи разные окна браузера или разные вкладки.</span><span class="sxs-lookup"><span data-stu-id="bb17c-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="bb17c-119">Если одинаковые учетные данные пользователя используются для входа в обе среды 1 и 2 одновременно в одном типа браузера, Talent отключает один из сеансов.</span><span class="sxs-lookup"><span data-stu-id="bb17c-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Talent disconnects one of the sessions.</span></span>

<span data-ttu-id="bb17c-120">**Решение**</span><span class="sxs-lookup"><span data-stu-id="bb17c-120">**Solution**</span></span>

<span data-ttu-id="bb17c-121">Убедитесь в том, что одновременно открыта только одна среда для определенного типа браузера.</span><span class="sxs-lookup"><span data-stu-id="bb17c-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="bb17c-122">Пользователи могут открывать несколько сеансов в одной среде (то есть, несколько вкладок в одном браузере).</span><span class="sxs-lookup"><span data-stu-id="bb17c-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="bb17c-123">Пользователи, которые хотят переходить двумя средами одновременно, должны открыть каждую среду в другом типе браузера.</span><span class="sxs-lookup"><span data-stu-id="bb17c-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="bb17c-124">(Например, пользователь А может просматривать среду 1 в Chrome и среду 2 в Microsoft Edge.)</span><span class="sxs-lookup"><span data-stu-id="bb17c-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>
