---
title: Настройка среды для поиска справочника
description: В этом разделе объясняется, как настроить среду для использования функции поиска основных данных для Расчет налогов.
author: kai-cloud
ms.date: 03/31/2021
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
ms.openlocfilehash: eda093a75898bace2f3c7968933b83ccafa7fabb
ms.sourcegitcommit: 66095f1b7e0fd2756aa29fd7deb9ce5392b7e0b2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/08/2021
ms.locfileid: "5869094"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="4ff18-103">Настройка среды для поиска справочника</span><span class="sxs-lookup"><span data-stu-id="4ff18-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="4ff18-104">В этом разделе объясняется, как настроить среду для использования функции поиска основных данных для Расчет налогов.</span><span class="sxs-lookup"><span data-stu-id="4ff18-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="4ff18-105">Настройте интеграцию Power Platform в Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="4ff18-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="4ff18-106">Дополнительные сведения см. в [Microsoft Power Platform интеграция — Обзор надстроек](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4ff18-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="4ff18-107">Настройка Dynamics 365 Finance и Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="4ff18-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="4ff18-108">Дополнительные сведения см. в [Получение решения](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) и [Проверка подлинности и авторизация](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="4ff18-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="4ff18-109">Импорт *решения виртуальной сущности необходимого условия для налоговой службы* из [виртуальной сущности налоговой службы](https://go.microsoft.com/fwlink/?linkid=2158160).</span><span class="sxs-lookup"><span data-stu-id="4ff18-109">Import the *Prerequisite tax service virtual entity solution* from the [Tax service virtual entity](https://go.microsoft.com/fwlink/?linkid=2158160).</span></span>
4. <span data-ttu-id="4ff18-110">Настройте Dynamics 365 Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="4ff18-110">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="4ff18-111">Создайте запрос на обслуживание для Microsoft, чтобы включить в фокус-тестирование следующих функций:</span><span class="sxs-lookup"><span data-stu-id="4ff18-111">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="4ff18-112">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="4ff18-112">ERCdsFeature</span></span>
      - <span data-ttu-id="4ff18-113">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="4ff18-113">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="4ff18-114">В Финансы, перейдите к рабочей области **Управление функциями** и включите следующие функции:</span><span class="sxs-lookup"><span data-stu-id="4ff18-114">In Finance, go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="4ff18-115">(Предварительная версия) Поддержка источников данных Dataverse электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="4ff18-115">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="4ff18-116">(Предварительная версия) Поддержка источников данных Dataverse налоговой службы</span><span class="sxs-lookup"><span data-stu-id="4ff18-116">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="4ff18-117">(Предварительная версия) Функции глобализации</span><span class="sxs-lookup"><span data-stu-id="4ff18-117">(Preview) Globalization features</span></span>

5. <span data-ttu-id="4ff18-118">Войдите в RCS с помощью учетной записи администратора клиента.</span><span class="sxs-lookup"><span data-stu-id="4ff18-118">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="4ff18-119">Перейдите к **Электронная отчетность** > **Подключенные приложения**.</span><span class="sxs-lookup"><span data-stu-id="4ff18-119">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="4ff18-120">Выберите **Создать**, чтобы добавить запись, и введите следующие сведения в поле.</span><span class="sxs-lookup"><span data-stu-id="4ff18-120">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="4ff18-121">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="4ff18-121">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="4ff18-122">В поле **Тип** выберите **Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="4ff18-122">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="4ff18-123">В поле **Приложение** выберите ваш URL-адрес Dataverse.</span><span class="sxs-lookup"><span data-stu-id="4ff18-123">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="4ff18-124">В поле **Клиент** введите ваш клиент.</span><span class="sxs-lookup"><span data-stu-id="4ff18-124">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="4ff18-125">В поле **пользовательский URL-адрес** введите ваш URL-адрес Dataverse и добавьте к нему "/api/data/v9.1".</span><span class="sxs-lookup"><span data-stu-id="4ff18-125">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="4ff18-126">Выберите **Проверить подключение** и завершите процесс подключения.</span><span class="sxs-lookup"><span data-stu-id="4ff18-126">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="4ff18-127">[![Кнопка проверить подключение](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="4ff18-127">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="4ff18-128">Перейдите к **Электронная отчетность** > **Конфигурации налогов** и выполните импорт конфигурации налогов из [Конфигурации налогов](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="4ff18-128">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="4ff18-129">[![Страница конфигурации налогов, дерево модели налоговых данных](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="4ff18-129">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="4ff18-130">Перейдите к **Сопоставление модели налогооблагаемого документа** или **Dataverse Сопоставление модели** при использовании конфигурации Microsoft, а в поле **Подключенное приложение** выберите запись, созданную на шаге 7.</span><span class="sxs-lookup"><span data-stu-id="4ff18-130">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="4ff18-131">Установите **По умолчанию для сопоставления модели** на **Да**.</span><span class="sxs-lookup"><span data-stu-id="4ff18-131">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="4ff18-132">[![Страница сопоставления модели](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="4ff18-132">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
