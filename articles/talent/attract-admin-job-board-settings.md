---
title: Включение интеграции Broadbean в Microsoft Dynamics 365 for Talent - Attract
description: В этой теме объясняется, как настроить Microsoft Dynamics 365 for Talent - Attract для публикации вакансий на внешних досках вакансий, таких как Broadbean.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 2334c2bd0edccf3000f8d91651afafd4619ad0b8
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739687"
---
# <a name="enable-broadbean-integration"></a><span data-ttu-id="5e5a3-103">Включение интеграции с Broadbean</span><span class="sxs-lookup"><span data-stu-id="5e5a3-103">Enable Broadbean integration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5e5a3-104">Вы хотите получить свои открытые вакансии перед как можно большим количеством квалифицированных кандидатов.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="5e5a3-105">Сайты трудоустройства, такие как Broadbean, помогают достичь этой цели.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="5e5a3-106">Microsoft Dynamics 365 for Talent: Attract теперь позволяет вам публиковать объявления о вакансиях на сайте Broadbean, и Microsoft постоянно предоставляет новые предложения в этой области.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-106">Microsoft Dynamics 365 for Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

> [!NOTE]
> - <span data-ttu-id="5e5a3-107">Чтобы размещать объявления о вакансиях на внешних сайтах, необходима [надстройка Comprehensive Hiring](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="5e5a3-107">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="5e5a3-108">Для публикации вакансий в Broadbean через Attract необходимо иметь подписку на Broadbean.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-108">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="5e5a3-109">Эта функция в данный момент находится в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-109">This feature is currently in preview.</span></span> <span data-ttu-id="5e5a3-110">Если вы хотите попробовать его, необходимо [включить его в настройках администратора Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="5e5a3-110">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

## <a name="configure-broadbean-integration"></a><span data-ttu-id="5e5a3-111">Настройка интеграции Broadbean</span><span class="sxs-lookup"><span data-stu-id="5e5a3-111">Configure Broadbean integration</span></span>

1. <span data-ttu-id="5e5a3-112">Выполните вход в Attract в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-112">Sign in to Attract as an admin.</span></span>

2. <span data-ttu-id="5e5a3-113">Выберите кнопку **Параметры** (символ шестеренки) в верхнем правом углу страницы, затем выберите **Центр администрирования**.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-113">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>

3. <span data-ttu-id="5e5a3-114">Обратитесь в Broadbean и введите сведения в поля **Имя пользователя**, **Идентификатор клиента**, **Токен шифрования**.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-114">Contact Broadbean, and enter your information in the **Username**, **Client ID**, and **Encryption Token** fields.</span></span>

4. <span data-ttu-id="5e5a3-115">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-115">Select **Save**.</span></span>

> [!WARNING]
> <span data-ttu-id="5e5a3-116">Ваши учетные данные Broadbean являются важными и конфиденциальными.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-116">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="5e5a3-117">Поэтому храните и совместно используйте их ответственно.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-117">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="5e5a3-118">Любой пользователь с ролью администратора в Attract можно просмотреть эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-118">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="5e5a3-119">Корпорация Майкрософт и Attract не участвуют в создании и ведении этих значений.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-119">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="5e5a3-120">Вашей обязанностью является их обновление в Attract и работа с Broadbean для устранения любых проблем с вашими учетными данными.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-120">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>
