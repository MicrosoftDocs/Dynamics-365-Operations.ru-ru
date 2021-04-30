---
title: Regulatory Configuration Service
description: В этом разделе представлен обзор возможностей службы Regulatory Configuration Service (RCS) и объясняется, как получить доступ к службе.
author: JaneA07
manager: AnnBe
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ec7e0fe07d979b85109605949b6ba33ab6d99b51
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890808"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="bd42b-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="bd42b-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd42b-104">Служба Regulatory Configuration Service (RCS) — это изолированный конструктор и служба управления жизненным циклом для функций глобализации без кода/мало кода.</span><span class="sxs-lookup"><span data-stu-id="bd42b-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="bd42b-105">RCS позволяет заинтересованным сторонам глобализации расширять и настраивать ключевые области глобализации, такие как налогообложение, электронное выставление накладных, нормативная отчетность, банковские операции и бизнес-документы, без необходимости привлечения разработчиков.</span><span class="sxs-lookup"><span data-stu-id="bd42b-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="bd42b-106">Такой подход к глобализации без кода/мало кода упрощает работу с глобализацией и повышает эффективность создания и расширения.</span><span class="sxs-lookup"><span data-stu-id="bd42b-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="bd42b-107">RCS обеспечивает следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="bd42b-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="bd42b-108">Поддержка всех функций, предоставляемых электронной отчетностью (ER).</span><span class="sxs-lookup"><span data-stu-id="bd42b-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="bd42b-109">Необходимое условие для настройки новых микрослужб глобализации.</span><span class="sxs-lookup"><span data-stu-id="bd42b-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="bd42b-110">Поддержка электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="bd42b-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="bd42b-111">Дополнительные сведения см. в [Электронное выставление накладных](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="bd42b-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="bd42b-112">Поддержка расчета налогов.</span><span class="sxs-lookup"><span data-stu-id="bd42b-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="bd42b-113">Дополнительные сведения см. в [Служба налогообложения](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="bd42b-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="bd42b-114">Поддержка новых функциональных возможностей глобализации, которая упрощает управление многокомпонентными возможностями и предоставляет дополнительные возможности для настройки действий и настройки параметров функций.</span><span class="sxs-lookup"><span data-stu-id="bd42b-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="bd42b-115">Дополнительные сведения см. в [Служба Regulatory Configuration Service — упрощенное управление функциями глобализации для служб глобализации](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="bd42b-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="bd42b-116">Поддержка централизованной публикации, хранения и совместного использования пользовательских конфигураций в глобальном репозитории для упрощения управления конфигурацией без необходимости использования Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="bd42b-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="bd42b-117">Доступ к RCS</span><span class="sxs-lookup"><span data-stu-id="bd42b-117">Access RCS</span></span>

<span data-ttu-id="bd42b-118">Вы можете зарегистрироваться или войти в RCS на [странице Служба Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="bd42b-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![Регистрация/вход в RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="bd42b-120">На странице **Служба Regulatory Configuration Service** проверьте и примите дополнительные условия использования службы, а затем выберите одну из следующих кнопок:</span><span class="sxs-lookup"><span data-stu-id="bd42b-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="bd42b-121">**Регистрация**, если вы впервые пользуетесь службой и используете рабочий адрес электронной почты для предоставления вашей организации среды службы</span><span class="sxs-lookup"><span data-stu-id="bd42b-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="bd42b-122">**Вход**, если вы ранее зарегистрировались в службе, и вам необходимо получить доступ к корпоративной среде</span><span class="sxs-lookup"><span data-stu-id="bd42b-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="bd42b-123">Региональная доступность</span><span class="sxs-lookup"><span data-stu-id="bd42b-123">Regional availability</span></span>

<span data-ttu-id="bd42b-124">RCS обычно доступен в следующих регионах:</span><span class="sxs-lookup"><span data-stu-id="bd42b-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="bd42b-125">США</span><span class="sxs-lookup"><span data-stu-id="bd42b-125">United States</span></span>
- <span data-ttu-id="bd42b-126">Индия</span><span class="sxs-lookup"><span data-stu-id="bd42b-126">India</span></span>
- <span data-ttu-id="bd42b-127">Франция</span><span class="sxs-lookup"><span data-stu-id="bd42b-127">France</span></span>
- <span data-ttu-id="bd42b-128">Европа</span><span class="sxs-lookup"><span data-stu-id="bd42b-128">Europe</span></span>

<span data-ttu-id="bd42b-129">Полный список регионов см. в [Dynamics 365 и Power Platform: доступность, расположение данных, язык и локализация](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="bd42b-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="bd42b-130">Документация, связанная с RCS</span><span class="sxs-lookup"><span data-stu-id="bd42b-130">Related RCS documentation</span></span>

<span data-ttu-id="bd42b-131">Дополнительные сведения о связанных компонентах см. в следующей документации:</span><span class="sxs-lookup"><span data-stu-id="bd42b-131">For more information about related components, see the following documentation:</span></span>

- <span data-ttu-id="bd42b-132">**Глобальный репозиторий:**</span><span class="sxs-lookup"><span data-stu-id="bd42b-132">**Global repository:**</span></span>

    - [<span data-ttu-id="bd42b-133">Создание конфигурации электронной отчетности и загрузка в глобальный репозиторий</span><span class="sxs-lookup"><span data-stu-id="bd42b-133">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="bd42b-134">Общая конфигурация в глобальном репозитории</span><span class="sxs-lookup"><span data-stu-id="bd42b-134">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="bd42b-135">Улучшенная фильтрация в глобальном репозитории</span><span class="sxs-lookup"><span data-stu-id="bd42b-135">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="bd42b-136">Загрузка конфигураций электронной отчетности из глобального репозитория</span><span class="sxs-lookup"><span data-stu-id="bd42b-136">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="bd42b-137">Прекращение использования конфигураций в глобальном репозитории</span><span class="sxs-lookup"><span data-stu-id="bd42b-137">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)

- <span data-ttu-id="bd42b-138">**Функция глобализации:**</span><span class="sxs-lookup"><span data-stu-id="bd42b-138">**Globalization feature:**</span></span>

    - [<span data-ttu-id="bd42b-139">Regulatory Configuration Service (RCS) — функции глобализации</span><span class="sxs-lookup"><span data-stu-id="bd42b-139">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)