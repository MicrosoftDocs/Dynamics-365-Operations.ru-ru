---
title: Ссылка для входа перенаправляет обратно на сайт электронной коммерции
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь при переадресации ссылки входа на сайт электронной коммерции вместо перехода на страницу входа.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: a1d0ae4e487c391020947c607d5d7cb5d1ba6af4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020611"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="7b68e-103">Ссылка для входа перенаправляет обратно на сайт электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="7b68e-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7b68e-104">В этом разделе содержатся указания по устранению неполадок, которые могут помочь при переадресации ссылки входа на сайт электронной коммерции вместо перехода на страницу входа.</span><span class="sxs-lookup"><span data-stu-id="7b68e-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="7b68e-105">описание</span><span class="sxs-lookup"><span data-stu-id="7b68e-105">Description</span></span>

<span data-ttu-id="7b68e-106">После того, как вы настроили новый клиент B2C Microsoft Azure Active Directory (Azure AD B2C) в конструкторе сайтов Commerce, пользователи, выбравшие ссылку **Войти**, перенаправляются назад на основную целевую страницу электронной коммерции без перехода на страницу входа.</span><span class="sxs-lookup"><span data-stu-id="7b68e-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="7b68e-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="7b68e-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="7b68e-108">Убедитесь, что URL-адрес ответа правильно настроен в приложении Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="7b68e-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="7b68e-109">Чтобы убедиться, что URL-адрес ответа правильно настроен в приложении Azure AD B2C, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b68e-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="7b68e-110">Перейдите в раздел [порталу Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="7b68e-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="7b68e-111">Выберите приложение Azure AD B2C, созданное для доступа к сайту.</span><span class="sxs-lookup"><span data-stu-id="7b68e-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="7b68e-112">Выберите приложение, которое было создано во время настройки Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="7b68e-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="7b68e-113">В разделе **URL-адрес ответа** убедитесь, что в списке имеются записи как для URL-адреса домена сайта, так и для URL-адреса, созданного в электронной коммерции, как показано в примере на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="7b68e-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![Записи URL-адресов ответа Azure AD B2C](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="7b68e-115">URL-адрес домена сайта и созданный в электронной коммерции URL-адрес должны иметь допустимый формат URL-адреса, не включающий начальную и заключительную косую черту.</span><span class="sxs-lookup"><span data-stu-id="7b68e-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b68e-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7b68e-116">Additional resources</span></span>

[<span data-ttu-id="7b68e-117">Регистрация веб-приложения в Azure Active Directory B2C</span><span class="sxs-lookup"><span data-stu-id="7b68e-117">Register a web application in Azure Active Directory B2C</span></span>](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="7b68e-118">Настройка клиента B2C в модуле Commerce</span><span class="sxs-lookup"><span data-stu-id="7b68e-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)