---
title: Настройка среды для поиска справочника
description: В этом разделе объясняется, как настроить среду для использования функции поиска основных данных для Расчет налогов.
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9f9b385df1db60b27698d90281c43fabb574af49
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924162"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="f53d6-103">Настройка среды для поиска справочника</span><span class="sxs-lookup"><span data-stu-id="f53d6-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f53d6-104">В этом разделе объясняется, как настроить среду для использования функции поиска основных данных для Расчет налогов.</span><span class="sxs-lookup"><span data-stu-id="f53d6-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="f53d6-105">Настройте интеграцию Power Platform в Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f53d6-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="f53d6-106">Дополнительные сведения см. в [Microsoft Power Platform интеграция — Обзор надстроек](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f53d6-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="f53d6-107">Настройка Dynamics 365 Finance и Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f53d6-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="f53d6-108">Дополнительные сведения см. в [Получение решения](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) и [Проверка подлинности и авторизация](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="f53d6-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="f53d6-109">Настройте следующие сущности.</span><span class="sxs-lookup"><span data-stu-id="f53d6-109">Set up the following entities.</span></span> <span data-ttu-id="f53d6-110">Дополнительные сведения см. в разделе [Включение виртуальных сущностей](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="f53d6-110">For more information, see [Enabling virtual entities](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span></span>
      - <span data-ttu-id="f53d6-111">CompanyInfoEntity</span><span class="sxs-lookup"><span data-stu-id="f53d6-111">CompanyInfoEntity</span></span>
      - <span data-ttu-id="f53d6-112">CurrencyEntity</span><span class="sxs-lookup"><span data-stu-id="f53d6-112">CurrencyEntity</span></span>
      - <span data-ttu-id="f53d6-113">CustCustomerV3Entity</span><span class="sxs-lookup"><span data-stu-id="f53d6-113">CustCustomerV3Entity</span></span>
      - <span data-ttu-id="f53d6-114">DeliveryTermsEntity</span><span class="sxs-lookup"><span data-stu-id="f53d6-114">DeliveryTermsEntity</span></span>
      - <span data-ttu-id="f53d6-115">EcoResProductCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="f53d6-115">EcoResProductCategoryEntity</span></span>
      - <span data-ttu-id="f53d6-116">EcoResReleasedProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="f53d6-116">EcoResReleasedProductV2Entity</span></span>
      - <span data-ttu-id="f53d6-117">LogisticsAddressCityEntity</span><span class="sxs-lookup"><span data-stu-id="f53d6-117">LogisticsAddressCityEntity</span></span>
      - <span data-ttu-id="f53d6-118">LogisticsAddressCountryRegionTranslationEntity</span><span class="sxs-lookup"><span data-stu-id="f53d6-118">LogisticsAddressCountryRegionTranslationEntity</span></span>
      - <span data-ttu-id="f53d6-119">LogisticsAddressStateEntity</span><span class="sxs-lookup"><span data-stu-id="f53d6-119">LogisticsAddressStateEntity</span></span>
      - <span data-ttu-id="f53d6-120">PurchProcurementChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="f53d6-120">PurchProcurementChargeCDSEntity</span></span>
      - <span data-ttu-id="f53d6-121">SalesChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="f53d6-121">SalesChargeCDSEntity</span></span>
      - <span data-ttu-id="f53d6-122">TaxGroupEntity</span><span class="sxs-lookup"><span data-stu-id="f53d6-122">TaxGroupEntity</span></span>
      - <span data-ttu-id="f53d6-123">TaxItemGroupHeadingEntity</span><span class="sxs-lookup"><span data-stu-id="f53d6-123">TaxItemGroupHeadingEntity</span></span>
      - <span data-ttu-id="f53d6-124">VendVendorV2Entity</span><span class="sxs-lookup"><span data-stu-id="f53d6-124">VendVendorV2Entity</span></span>
4. <span data-ttu-id="f53d6-125">Настройте Dynamics 365 Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="f53d6-125">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="f53d6-126">Создайте запрос на обслуживание для Microsoft, чтобы включить в фокус-тестирование следующих функций:</span><span class="sxs-lookup"><span data-stu-id="f53d6-126">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="f53d6-127">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="f53d6-127">ERCdsFeature</span></span>
      - <span data-ttu-id="f53d6-128">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="f53d6-128">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="f53d6-129">Перейдите к рабочей области **Управление функциями** и включите следующие функции:</span><span class="sxs-lookup"><span data-stu-id="f53d6-129">Go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="f53d6-130">(Предварительная версия) Поддержка источников данных Dataverse электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="f53d6-130">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="f53d6-131">(Предварительная версия) Поддержка источников данных Dataverse налоговой службы</span><span class="sxs-lookup"><span data-stu-id="f53d6-131">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="f53d6-132">(Предварительная версия) Функции глобализации</span><span class="sxs-lookup"><span data-stu-id="f53d6-132">(Preview) Globalization features</span></span>

5. <span data-ttu-id="f53d6-133">Войдите в RCS с помощью учетной записи администратора клиента.</span><span class="sxs-lookup"><span data-stu-id="f53d6-133">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="f53d6-134">Перейдите к **Электронная отчетность** > **Подключенные приложения**.</span><span class="sxs-lookup"><span data-stu-id="f53d6-134">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="f53d6-135">Выберите **Создать**, чтобы добавить запись, и введите следующие сведения в поле.</span><span class="sxs-lookup"><span data-stu-id="f53d6-135">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="f53d6-136">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="f53d6-136">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="f53d6-137">В поле **Тип** выберите **Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="f53d6-137">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="f53d6-138">В поле **Приложение** выберите ваш URL-адрес Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f53d6-138">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="f53d6-139">В поле **Клиент** введите ваш клиент.</span><span class="sxs-lookup"><span data-stu-id="f53d6-139">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="f53d6-140">В поле **пользовательский URL-адрес** введите ваш URL-адрес Dataverse и добавьте к нему "/api/data/v9.1".</span><span class="sxs-lookup"><span data-stu-id="f53d6-140">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="f53d6-141">Выберите **Проверить подключение** и завершите процесс подключения.</span><span class="sxs-lookup"><span data-stu-id="f53d6-141">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="f53d6-142">[![Кнопка проверить подключение](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="f53d6-142">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="f53d6-143">Перейдите к **Электронная отчетность** > **Конфигурации налогов** и выполните импорт конфигурации налогов из [Конфигурации налогов](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="f53d6-143">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="f53d6-144">[![Страница конфигурации налогов, дерево модели налоговых данных](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="f53d6-144">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="f53d6-145">Перейдите к **Сопоставление модели налогооблагаемого документа** или **Dataverse Сопоставление модели** при использовании конфигурации Microsoft, а в поле **Подключенное приложение** выберите запись, созданную на шаге 7.</span><span class="sxs-lookup"><span data-stu-id="f53d6-145">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="f53d6-146">Установите **По умолчанию для сопоставления модели** на **Да**.</span><span class="sxs-lookup"><span data-stu-id="f53d6-146">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="f53d6-147">[![Страница сопоставления модели](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="f53d6-147">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
