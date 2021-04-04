---
title: Ограничение доступа к витрине в ходе тестирования или разработки
description: В этой теме объясняется, как ограничить доступ к витрине в Microsoft Dynamics 365 Commerce во время внутреннего испытания или разработки.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2cdf131048e0fac940475322294ed99e76c0a53b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585505"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="9cab4-103">Ограничение доступа к витрине в ходе тестирования или разработки</span><span class="sxs-lookup"><span data-stu-id="9cab4-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9cab4-104">В этой теме объясняется, как ограничить доступ к витрине в Microsoft Dynamics 365 Commerce во время внутреннего испытания или разработки.</span><span class="sxs-lookup"><span data-stu-id="9cab4-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="9cab4-105">описание</span><span class="sxs-lookup"><span data-stu-id="9cab4-105">Description</span></span>

<span data-ttu-id="9cab4-106">Во время внутреннего тестирования или активной разработки может возникнуть необходимость ограничить доступ к вашему сайту, чтобы запретить внешним пользователям доступ к опубликованным страницам витрин.</span><span class="sxs-lookup"><span data-stu-id="9cab4-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="9cab4-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="9cab4-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="9cab4-108">Настройте Azure AD B2C с помощью стандартных потоков пользователей</span><span class="sxs-lookup"><span data-stu-id="9cab4-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="9cab4-109">Сведения о настройке Azure Active Directory B2C (Azure AD B2C) для вашего сайта электронной коммерции см. [Настройка клиента в коммерческих организациях B2C](../set-up-b2c-tenant.md).</span><span class="sxs-lookup"><span data-stu-id="9cab4-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="9cab4-110">Ограничьте доступ пользователя к страницам витрин и запретите создание новых пользователей</span><span class="sxs-lookup"><span data-stu-id="9cab4-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="9cab4-111">Чтобы ограничить доступ пользователей к страницам витрин в Commerce Site Builder, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9cab4-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9cab4-112">Перейдите на ваш сайт.</span><span class="sxs-lookup"><span data-stu-id="9cab4-112">Go to your site.</span></span>
1. <span data-ttu-id="9cab4-113">Выберите **страницы**, а затем выберите страницу, для которой требуется ограничить доступ пользователя.</span><span class="sxs-lookup"><span data-stu-id="9cab4-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="9cab4-114">Выберите модуль или ячейку фрагмента, а затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="9cab4-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="9cab4-115">В области свойств выберите **требуется вход в систему?**, а затем нажмите кнопку **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="9cab4-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="9cab4-116">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="9cab4-116">Select **Publish**.</span></span>

<span data-ttu-id="9cab4-117">Чтобы заблокировать создание новых пользователей в Azure AD, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9cab4-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="9cab4-118">Перейдите в раздел [порталу Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="9cab4-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="9cab4-119">Выберите приложение Azure AD B2C, созданное для доступа к сайту.</span><span class="sxs-lookup"><span data-stu-id="9cab4-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="9cab4-120">В левой области переходов выберите **Потоки пользователей**.</span><span class="sxs-lookup"><span data-stu-id="9cab4-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="9cab4-121">В верхней части страницы **Потоки пользователей** выберите **Создать поток пользователей**.</span><span class="sxs-lookup"><span data-stu-id="9cab4-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="9cab4-122">На странице **Выбор типа потока пользователя** выберите **Предварительный просмотр**.</span><span class="sxs-lookup"><span data-stu-id="9cab4-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="9cab4-123">В середине страницы выберите **Выполните вход v2**.</span><span class="sxs-lookup"><span data-stu-id="9cab4-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="9cab4-124">Затем выполните шаги, описанные в разделе [Настройка клиента B2C в Commerce](../set-up-b2c-tenant.md), чтобы настроить поток в качестве стандартного потока пользователей узла для Azure AD B2C во время тестирования или разработки.</span><span class="sxs-lookup"><span data-stu-id="9cab4-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9cab4-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9cab4-125">Additional resources</span></span>

[<span data-ttu-id="9cab4-126">Настройка клиента B2C в модуле Commerce</span><span class="sxs-lookup"><span data-stu-id="9cab4-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="9cab4-127">Настройка пользовательских страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="9cab4-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)