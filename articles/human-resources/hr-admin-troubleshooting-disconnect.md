---
title: Отключение клиента
description: В этой статье объясняется, что делать, если клиент отключен от свой среды и не знает, почему.
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
ms.openlocfilehash: db0e8efec1a5a6f01c9b7c4d9334a959fc42886b
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027995"
---
# <a name="client-disconnects"></a><span data-ttu-id="1fd72-103">Отключение клиента</span><span class="sxs-lookup"><span data-stu-id="1fd72-103">Client disconnects</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1fd72-104">**Сведения среды**</span><span class="sxs-lookup"><span data-stu-id="1fd72-104">**Environment details**</span></span> 

<span data-ttu-id="1fd72-105">Эта проблема может возникнуть во всех средах.</span><span class="sxs-lookup"><span data-stu-id="1fd72-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="1fd72-106">**Симптом**</span><span class="sxs-lookup"><span data-stu-id="1fd72-106">**Symptom**</span></span> 

<span data-ttu-id="1fd72-107">Клиент отключен от свой среды и не знает, почему.</span><span class="sxs-lookup"><span data-stu-id="1fd72-107">The customer is disconnected from the environment and doesn't know why.</span></span> <span data-ttu-id="1fd72-108">Клиент получает одно из следующих сообщений об ошибке:</span><span class="sxs-lookup"><span data-stu-id="1fd72-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="1fd72-109">Потеряно подключение.</span><span class="sxs-lookup"><span data-stu-id="1fd72-109">We've lost your connection.</span></span> <span data-ttu-id="1fd72-110">Нажмите кнопку "Закрыть" для продолжения работы.</span><span class="sxs-lookup"><span data-stu-id="1fd72-110">Click Close to continue working.</span></span>
- <span data-ttu-id="1fd72-111">Похоже, что потеряно подключение к сети; нажмите кнопку "Повторить", чтобы повторить попытку.</span><span class="sxs-lookup"><span data-stu-id="1fd72-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="1fd72-112">**Красный флаг**</span><span class="sxs-lookup"><span data-stu-id="1fd72-112">**Red flag**</span></span>

<span data-ttu-id="1fd72-113">Эта проблема часто возникает, когда пользователи находятся на этапе реализации, выполняют сравнение сведений по производственным и тестовым средам и забывают, что они перемещаются между сеансами.</span><span class="sxs-lookup"><span data-stu-id="1fd72-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="1fd72-114">Если пользователи находятся на этом этапе, они скорее всего столкнутся с этой проблемой.</span><span class="sxs-lookup"><span data-stu-id="1fd72-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="1fd72-115">**Выдать**</span><span class="sxs-lookup"><span data-stu-id="1fd72-115">**Issue**</span></span> 

<span data-ttu-id="1fd72-116">**Типы браузеров:** Google Chrome, Internet Explorer и Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1fd72-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="1fd72-117">Microsoft Dynamics 365 Human Resources отключает пользователей, когда одновременно открыто два разных сеанса для одного пользователя и одного типа браузера.</span><span class="sxs-lookup"><span data-stu-id="1fd72-117">Microsoft Dynamics 365 Human Resources disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="1fd72-118">(Например, пользователь А просматривает как среду 1, так и среду 2 в Chrome.) Не имеет значения, открыли ли пользователи разные окна браузера или разные вкладки.</span><span class="sxs-lookup"><span data-stu-id="1fd72-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="1fd72-119">Если одинаковые учетные данные пользователя используются для входа в обе среды 1 и 2 одновременно в одном типа браузера, Human Resources отключает один из сеансов.</span><span class="sxs-lookup"><span data-stu-id="1fd72-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Human Resources disconnects one of the sessions.</span></span>

<span data-ttu-id="1fd72-120">**Решение**</span><span class="sxs-lookup"><span data-stu-id="1fd72-120">**Solution**</span></span>

<span data-ttu-id="1fd72-121">Убедитесь в том, что одновременно открыта только одна среда для определенного типа браузера.</span><span class="sxs-lookup"><span data-stu-id="1fd72-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="1fd72-122">Пользователи могут открывать несколько сеансов в одной среде (то есть, несколько вкладок в одном браузере).</span><span class="sxs-lookup"><span data-stu-id="1fd72-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="1fd72-123">Пользователи, которые хотят переходить двумя средами одновременно, должны открыть каждую среду в другом типе браузера.</span><span class="sxs-lookup"><span data-stu-id="1fd72-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="1fd72-124">(Например, пользователь А может просматривать среду 1 в Chrome и среду 2 в Microsoft Edge.)</span><span class="sxs-lookup"><span data-stu-id="1fd72-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]