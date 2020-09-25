---
title: Соответствие cookie
description: В этой теме описаны соображения соответствия требованиям файлов cookie и политики по умолчанию, включенные в Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f54b9b8130a167dbecdb13fccd7039f827f6ed0
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761329"
---
# <a name="cookie-compliance"></a><span data-ttu-id="cf7d3-103">Соответствие cookie</span><span class="sxs-lookup"><span data-stu-id="cf7d3-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cf7d3-104">В этой теме описаны соображения соответствия требованиям файлов cookie и политики по умолчанию, включенные в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cf7d3-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="cf7d3-105">Overview</span></span>

<span data-ttu-id="cf7d3-106">Конфиденциальность является важным фактором, когда используются технологии отслеживания, влияющие на клиентов электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="cf7d3-107">Из-за стандартов конфиденциальности, таких как Общий регламент по защите данных (GDPR) в Европейском союзе (ЕС), электронные руководящие принципы конфиденциальности должны быть учтены для любого сайта, который активен сегодня.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="cf7d3-108">Поскольку многие сайты электронной коммерции доступны глобально по умолчанию, важно пересмотреть стандарты соответствия для вашего сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="cf7d3-109">Чтобы узнать больше об основных принципах, которые использует Майкрософт для соответствия файлов cookie, посетите [Центр управления безопасностью Майкрософт](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="cf7d3-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="cf7d3-110">На этом сайте вы также можете получить более подробную информацию о областях соответствия и конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="cf7d3-111">В следующей таблице показан текущий справочный список файлов cookie, размещаемых сайтами Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="cf7d3-112">Имя файла cookie</span><span class="sxs-lookup"><span data-stu-id="cf7d3-112">Cookie name</span></span>                               | <span data-ttu-id="cf7d3-113">Использование</span><span class="sxs-lookup"><span data-stu-id="cf7d3-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="cf7d3-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="cf7d3-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="cf7d3-115">Сохранение файлов cookie проверки подлинности Microsoft Azure Active Directory (Azure AD) для единого входа (SSO).</span><span class="sxs-lookup"><span data-stu-id="cf7d3-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="cf7d3-116">Хранит зашифрованные данные участника-пользователя (имя, фамилия, адрес электронной почты).</span><span class="sxs-lookup"><span data-stu-id="cf7d3-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="cf7d3-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="cf7d3-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="cf7d3-118">Хранит идентификатор корзины магазина, используемый для получения списка продуктов, добавленных в экземпляр корзины.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="cf7d3-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="cf7d3-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="cf7d3-120">Отслеживание согласия на соответствие cookie.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="cf7d3-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="cf7d3-121">ai_session</span></span>                                  | <span data-ttu-id="cf7d3-122">Определяет, сколько сеансов активности пользователей включало определенные страницы и функции приложения.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="cf7d3-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="cf7d3-123">ai_user</span></span>                                     | <span data-ttu-id="cf7d3-124">Определяет, сколько человек использовало приложение и его функции.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="cf7d3-125">Пользователи подсчитываются с помощью анонимных идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="cf7d3-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="cf7d3-126">b2cru</span></span>                                       | <span data-ttu-id="cf7d3-127">Хранит URL-адрес перенаправления динамически.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="cf7d3-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="cf7d3-128">JSESSIONID</span></span>                                  | <span data-ttu-id="cf7d3-129">Используется соединителем платежей Adyen для хранения сеанса пользователя.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="cf7d3-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="cf7d3-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="cf7d3-131">Аутентификация</span><span class="sxs-lookup"><span data-stu-id="cf7d3-131">Authentication</span></span>                                               |
| <span data-ttu-id="cf7d3-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="cf7d3-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="cf7d3-133">Используется для поддержки состояния запроса.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="cf7d3-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="cf7d3-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="cf7d3-135">Маркер подделки межсайтовых запросов (CRSF), используемый для защиты от CRSF.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="cf7d3-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="cf7d3-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="cf7d3-137">Используется для маршрутизации запросов к соответствующему производственному экземпляру сервера аутентификации.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="cf7d3-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="cf7d3-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="cf7d3-139">Используется для маршрутизации запросов к соответствующему производственному экземпляру сервера аутентификации.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="cf7d3-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="cf7d3-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="cf7d3-141">Используется для маршрутизации запросов к соответствующему производственному экземпляру сервера аутентификации.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="cf7d3-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="cf7d3-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="cf7d3-143">Используется для ведения сеанса SSO.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="cf7d3-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="cf7d3-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="cf7d3-145">Используется для отслеживания проводок (число открытых вкладок проверка подлинности для сайта "бизнес-клиент" (B2C)), включая текущую проводку.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="cf7d3-146">Согласие пользователя сайта на использование файлов cookie на сайте электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="cf7d3-146">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="cf7d3-147">Если функция или модуль сайта электронной коммерции использует необязательные файлы cookie, перед отслеживанием этого файла cookie необходимо получить согласие пользователя сайта.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-147">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="cf7d3-148">Чтобы разрешить пользователям сайтов предоставлять согласие на файлы cookie на сайте электронной коммерции, автор сайта должен добавить и настроить модуль разрешения файлов cookie в модуле заголовка страницы, чтобы обеспечить, что разрешение было запрошено и получено.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-148">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="cf7d3-149">Согласие пользователя сайта должно быть предоставлено, прежде чем функция или модуль, использующие необязательный файл cookie, смогут отображаться на странице сайта.</span><span class="sxs-lookup"><span data-stu-id="cf7d3-149">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf7d3-150">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cf7d3-150">Additional resources</span></span>

[<span data-ttu-id="cf7d3-151">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="cf7d3-151">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="cf7d3-152">Обзор соответствия</span><span class="sxs-lookup"><span data-stu-id="cf7d3-152">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="cf7d3-153">Добавление страницы политики конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="cf7d3-153">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="cf7d3-154">Замена идентификаторов пользователей, связанных с отслеживаемыми изменениями содержимого</span><span class="sxs-lookup"><span data-stu-id="cf7d3-154">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="cf7d3-155">Модуль согласия на файлы cookie</span><span class="sxs-lookup"><span data-stu-id="cf7d3-155">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="cf7d3-156">Модуль верхнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="cf7d3-156">Header module</span></span>](author-header-module.md)
