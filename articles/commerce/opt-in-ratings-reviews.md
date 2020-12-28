---
title: Соглашение на использование оценок и отзывов
description: В этой теме объясняется, как согласиться на использование оценок и отзывов на веб-сайте Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cbdb69202ebec19f4442041cfb1f99857da36d2e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415246"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="890f1-103">Соглашение на использование оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="890f1-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="890f1-104">В этой теме объясняется, как согласиться на использование оценок и отзывов на веб-сайте Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="890f1-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="890f1-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="890f1-105">Overview</span></span>

<span data-ttu-id="890f1-106">Решение оценок и отзывов — это омниканальное решение, которое можно сделать доступным в Dynamics 365 Commerce с помощью Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="890f1-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="890f1-107">LCS — это портал администрирования, который используется в розничных магазинах для управления средами от подготовки до выведения из эксплуатации.</span><span class="sxs-lookup"><span data-stu-id="890f1-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="890f1-108">Если вы хотите использовать решение с оценками и обзорами на веб-сайте Commerce, вы должны принять оценки и обзоры во время развертывания узла электронной коммерции Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="890f1-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="890f1-109">Соглашение на использование оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="890f1-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="890f1-110">Чтобы согласиться на использование оценок и отзывов на веб-сайте, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="890f1-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="890f1-111">Выполните шаги раздела [Развертывание нового сайта электронной коммерции](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="890f1-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="890f1-112">Пока вы все еще находитесь в LCS, перейдите к пункту **Настройка развертывания Retail \> Другие параметры**.</span><span class="sxs-lookup"><span data-stu-id="890f1-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="890f1-113">Установите для параметра **Включить службу оценок и отзывов** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="890f1-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="890f1-114">В поле **Группа безопасности AAD для модератора оценок и отзывов (код объекта группы безопасности)** введите идентификатор группы безопасности Microsoft Azure Active Directory (Azure AD), включающий модераторов оценок и отзывов.</span><span class="sxs-lookup"><span data-stu-id="890f1-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Соглашение на использование оценок и отзывов](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="890f1-116">Завершите процесс инициализации электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="890f1-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="890f1-117">Если вы являетесь существующим клиентом Dynamics 365 Commerce, который уже развернул сайт электронной коммерции, не прибегая к оценкам и обзорам, а теперь хотите использовать оценки и обзоры из пакета Dynamics 365 Commerce, отправьте запрос на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="890f1-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="890f1-118">Сведения о том, как отправлять запрос на обслуживание, см. в разделе [Процесс отправки запросов на обслуживание](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="890f1-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="890f1-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="890f1-119">Additional resources</span></span>

[<span data-ttu-id="890f1-120">Обзор оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="890f1-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="890f1-121">Управление оценками и отзывами</span><span class="sxs-lookup"><span data-stu-id="890f1-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="890f1-122">Настройка оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="890f1-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="890f1-123">Синхронизация оценок продуктов в Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="890f1-123">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)


