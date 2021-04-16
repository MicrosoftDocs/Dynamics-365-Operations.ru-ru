---
title: Соответствие cookie
description: В этой теме описаны соображения соответствия требованиям файлов cookie и политики по умолчанию, включенные в Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2cc2089bc3052c0c59cb0414f8301123a9a30df2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796035"
---
# <a name="cookie-compliance"></a><span data-ttu-id="3b53c-103">Соответствие файлов cookie</span><span class="sxs-lookup"><span data-stu-id="3b53c-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3b53c-104">В этой теме описаны соображения соответствия требованиям файлов cookie и политики по умолчанию, включенные в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3b53c-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3b53c-105">Конфиденциальность является важным фактором, когда используются технологии отслеживания, влияющие на клиентов электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="3b53c-105">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="3b53c-106">Из-за стандартов конфиденциальности, таких как Общий регламент по защите данных (GDPR) в Европейском союзе (ЕС), электронные руководящие принципы конфиденциальности должны быть учтены для любого сайта, который активен сегодня.</span><span class="sxs-lookup"><span data-stu-id="3b53c-106">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="3b53c-107">Поскольку многие сайты электронной коммерции доступны глобально по умолчанию, важно пересмотреть стандарты соответствия для вашего сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="3b53c-107">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="3b53c-108">Чтобы узнать больше об основных принципах, которые использует Майкрософт для соответствия файлов cookie, посетите [Центр управления безопасностью Майкрософт](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="3b53c-108">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="3b53c-109">На этом сайте вы также можете получить более подробную информацию о областях соответствия и конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="3b53c-109">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="3b53c-110">В следующей таблице показан текущий справочный список файлов cookie, размещаемых сайтами Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3b53c-110">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="3b53c-111">Имя файла cookie</span><span class="sxs-lookup"><span data-stu-id="3b53c-111">Cookie name</span></span>                               | <span data-ttu-id="3b53c-112">Использование</span><span class="sxs-lookup"><span data-stu-id="3b53c-112">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="3b53c-113">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="3b53c-113">.AspNet.Cookies</span></span>                             | <span data-ttu-id="3b53c-114">Сохранение файлов cookie проверки подлинности Microsoft Azure Active Directory (Azure AD) для единого входа (SSO).</span><span class="sxs-lookup"><span data-stu-id="3b53c-114">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="3b53c-115">Хранит зашифрованные данные участника-пользователя (имя, фамилия, адрес электронной почты).</span><span class="sxs-lookup"><span data-stu-id="3b53c-115">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="3b53c-116">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="3b53c-116">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="3b53c-117">Хранит идентификатор корзины магазина, используемый для получения списка продуктов, добавленных в экземпляр корзины.</span><span class="sxs-lookup"><span data-stu-id="3b53c-117">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="3b53c-118">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="3b53c-118">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="3b53c-119">Отслеживание согласия на соответствие cookie.</span><span class="sxs-lookup"><span data-stu-id="3b53c-119">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="3b53c-120">ai_session</span><span class="sxs-lookup"><span data-stu-id="3b53c-120">ai_session</span></span>                                  | <span data-ttu-id="3b53c-121">Определяет, сколько сеансов активности пользователей включало определенные страницы и функции приложения.</span><span class="sxs-lookup"><span data-stu-id="3b53c-121">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="3b53c-122">ai_user</span><span class="sxs-lookup"><span data-stu-id="3b53c-122">ai_user</span></span>                                     | <span data-ttu-id="3b53c-123">Определяет, сколько человек использовало приложение и его функции.</span><span class="sxs-lookup"><span data-stu-id="3b53c-123">Detects how many people used the app and its features.</span></span> <span data-ttu-id="3b53c-124">Пользователи подсчитываются с помощью анонимных идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="3b53c-124">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="3b53c-125">b2cru</span><span class="sxs-lookup"><span data-stu-id="3b53c-125">b2cru</span></span>                                       | <span data-ttu-id="3b53c-126">Хранит URL-адрес перенаправления динамически.</span><span class="sxs-lookup"><span data-stu-id="3b53c-126">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="3b53c-127">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="3b53c-127">JSESSIONID</span></span>                                  | <span data-ttu-id="3b53c-128">Используется соединителем платежей Adyen для хранения сеанса пользователя.</span><span class="sxs-lookup"><span data-stu-id="3b53c-128">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="3b53c-129">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="3b53c-129">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="3b53c-130">Аутентификация</span><span class="sxs-lookup"><span data-stu-id="3b53c-130">Authentication</span></span>                                               |
| <span data-ttu-id="3b53c-131">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="3b53c-131">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="3b53c-132">Используется для поддержки состояния запроса.</span><span class="sxs-lookup"><span data-stu-id="3b53c-132">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="3b53c-133">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="3b53c-133">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="3b53c-134">Маркер подделки межсайтовых запросов (CRSF), используемый для защиты от CRSF.</span><span class="sxs-lookup"><span data-stu-id="3b53c-134">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="3b53c-135">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="3b53c-135">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="3b53c-136">Используется для маршрутизации запросов к соответствующему производственному экземпляру сервера аутентификации.</span><span class="sxs-lookup"><span data-stu-id="3b53c-136">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="3b53c-137">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="3b53c-137">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="3b53c-138">Используется для маршрутизации запросов к соответствующему производственному экземпляру сервера аутентификации.</span><span class="sxs-lookup"><span data-stu-id="3b53c-138">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="3b53c-139">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="3b53c-139">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="3b53c-140">Используется для маршрутизации запросов к соответствующему производственному экземпляру сервера аутентификации.</span><span class="sxs-lookup"><span data-stu-id="3b53c-140">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="3b53c-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="3b53c-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="3b53c-142">Используется для ведения сеанса SSO.</span><span class="sxs-lookup"><span data-stu-id="3b53c-142">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="3b53c-143">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="3b53c-143">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="3b53c-144">Используется для отслеживания проводок (число открытых вкладок проверка подлинности для сайта "бизнес-клиент" (B2C)), включая текущую проводку.</span><span class="sxs-lookup"><span data-stu-id="3b53c-144">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="3b53c-145">Согласие пользователя сайта на использование файлов cookie на сайте электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="3b53c-145">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="3b53c-146">Если функция или модуль сайта электронной коммерции использует необязательные файлы cookie, перед отслеживанием этого файла cookie необходимо получить согласие пользователя сайта.</span><span class="sxs-lookup"><span data-stu-id="3b53c-146">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="3b53c-147">Чтобы разрешить пользователям сайтов предоставлять согласие на файлы cookie на сайте электронной коммерции, автор сайта должен добавить и настроить модуль разрешения файлов cookie в модуле заголовка страницы, чтобы обеспечить, что разрешение было запрошено и получено.</span><span class="sxs-lookup"><span data-stu-id="3b53c-147">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="3b53c-148">Согласие пользователя сайта должно быть предоставлено, прежде чем функция или модуль, использующие необязательный файл cookie, смогут отображаться на странице сайта.</span><span class="sxs-lookup"><span data-stu-id="3b53c-148">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b53c-149">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3b53c-149">Additional resources</span></span>

[<span data-ttu-id="3b53c-150">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="3b53c-150">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="3b53c-151">Обзор соответствия</span><span class="sxs-lookup"><span data-stu-id="3b53c-151">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="3b53c-152">Добавление страницы политики конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="3b53c-152">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="3b53c-153">Замена идентификаторов пользователей, связанных с отслеживаемыми изменениями содержимого</span><span class="sxs-lookup"><span data-stu-id="3b53c-153">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="3b53c-154">Модуль согласия на файлы cookie</span><span class="sxs-lookup"><span data-stu-id="3b53c-154">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="3b53c-155">Модуль верхнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="3b53c-155">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
