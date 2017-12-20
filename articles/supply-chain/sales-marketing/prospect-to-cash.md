---
title: "Решение \"Перспективный клиент в наличные деньги\""
description: "В этой теме представлен обзор решения \"Перспективный клиент в наличные деньги\" между Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition и Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 11/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 788e64476094e84eb4d438890776306c05b20582
ms.openlocfilehash: 762699cf68ec8a9df5db20d7dd33bc9248f0a36e
ms.contentlocale: ru-ru
ms.lasthandoff: 12/11/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="cf1c2-103">Решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="cf1c2-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cf1c2-104">Решение "Перспективный клиент в наличные деньги" обеспечивает прямую синхронизацию между Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition и Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-104">The Prospect to cash solution provides direct synchronization across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, and Microsoft Dynamics 365 for Sales.</span></span> <span data-ttu-id="cf1c2-105">Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных для организаций, контактов, продуктов, предложений по продажам, заказов на продажу и накладных по продажам между Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="cf1c2-106">Во время выполнения обмена данными между Finance and Operations и Sales вы можете выполнять мероприятия по продажам и маркетингу в Sales и обрабатывать выполнение заказов с помощью управления запасами в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span>

<span data-ttu-id="cf1c2-107">В текущей версии решение "Перспективный клиент в наличные деньги" предоставляет следующие типы прямой синхронизации:</span><span class="sxs-lookup"><span data-stu-id="cf1c2-107">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="cf1c2-108">Ведение организаций в Sales и их прямая синхронизация из Sales в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cf1c2-108">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="cf1c2-109">Ведение продуктов в Finance and Operations и их прямая синхронизация с Sales</span><span class="sxs-lookup"><span data-stu-id="cf1c2-109">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="cf1c2-110">Ведение контактов в Sales и их прямая синхронизация с контактами или клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cf1c2-110">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="cf1c2-111">Синхронизация предложений по продажам напрямую из Sales с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cf1c2-111">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="cf1c2-112">Синхронизация заказов на продажу напрямую из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="cf1c2-112">Synchronize sales orders directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)
- [<span data-ttu-id="cf1c2-113">Синхронизация заказов на продажу непосредственно между Sales и Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cf1c2-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="cf1c2-114">Синхронизация накладных по продаже напрямую из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="cf1c2-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

<span data-ttu-id="cf1c2-115">В предыдущих версиях решение "Перспективный клиент в наличные деньги" предоставляет следующие типы непрямой синхронизации:</span><span class="sxs-lookup"><span data-stu-id="cf1c2-115">In earlier versions, the Prospect to cash solution provides the following types of non-direct synchronization:</span></span>

- [<span data-ttu-id="cf1c2-116">Ведение счетов в Sales и их синхронизация с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cf1c2-116">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
- [<span data-ttu-id="cf1c2-117">Ведение контактов в Sales и их синхронизация с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cf1c2-117">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
- [<span data-ttu-id="cf1c2-118">Ведение продуктов в Finance and Operations и их синхронизация с Sales</span><span class="sxs-lookup"><span data-stu-id="cf1c2-118">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
- [<span data-ttu-id="cf1c2-119">Создание предложений по продажам в Sales и их синхронизация с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cf1c2-119">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
- [<span data-ttu-id="cf1c2-120">Создание заказов на продажу в Finance and Operations и их синхронизация с Sales</span><span class="sxs-lookup"><span data-stu-id="cf1c2-120">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
- [<span data-ttu-id="cf1c2-121">Создание накладных по продажам в Finance and Operations и их синхронизация с Sales</span><span class="sxs-lookup"><span data-stu-id="cf1c2-121">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="cf1c2-122">Системные требования для Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cf1c2-122">System requirements for Finance and Operations</span></span>

<span data-ttu-id="cf1c2-123">Чтобы использовать решение "Перспективный клиент в наличные деньги", вы должны установить следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="cf1c2-123">To use the Prospect to cash solution, you must install the following components:</span></span>

### <a name="july-2017"></a><span data-ttu-id="cf1c2-124">Июль 2017</span><span class="sxs-lookup"><span data-stu-id="cf1c2-124">July 2017</span></span> 

- <span data-ttu-id="cf1c2-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (июль 2017 г.) с обновлением платформы 8 (сборка приложения 7.2.11792.56024 со сборкой платформы 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="cf1c2-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212)</span></span>
- <span data-ttu-id="cf1c2-126">Следующие исправления для Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="cf1c2-126">The following hotfixes for Finance and Operations:</span></span>

    - <span data-ttu-id="cf1c2-127">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** — это исправление делает возможным синхронизацию заказов на продажу из Sales в Finance and Operations с помощью компонента интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-127">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="cf1c2-128">Оно также предоставляет несколько других улучшений.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-128">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="cf1c2-129">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** — это исправление делает возможным синхронизацию строк заказов на продажу из Finance and Operations в Sales с помощью компонента интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-129">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="cf1c2-130">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** — это исправление делает возможным синхронизацию заказов на продажу из Finance and Operations в Sales с помощью компонента интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-130">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cf1c2-131">Достаточно установить только KB4045570, потому что в пакет установки входят изменения из других статей базы знаний (KB) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-131">You only have to install KB4045570, because the installation includes the changes from the other Microsoft Knowledge Base (KB) articles.</span></span>

### <a name="november-2016-version-1611"></a><span data-ttu-id="cf1c2-132">Ноябрь 2016 (версия 1611)</span><span class="sxs-lookup"><span data-stu-id="cf1c2-132">November 2016 (Version 1611)</span></span>

- <span data-ttu-id="cf1c2-133">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (ноябрь 2016 г.) с обновлением платформы 8 или выше</span><span class="sxs-lookup"><span data-stu-id="cf1c2-133">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (November 2016) with platform update 8 or higher</span></span>

- <span data-ttu-id="cf1c2-134">Следующие исправления для Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="cf1c2-134">The following hotfixes for Finance and Operations:</span></span>

    - <span data-ttu-id="cf1c2-135">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** — делает возможной синхронизацию заказов на продажу с помощью компонента интеграции данных из Microsoft Dynamics 365 for Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="cf1c2-135">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Microsoft Dynamics 365 for Finance and Operations to Sales</span></span> 
    - <span data-ttu-id="cf1c2-136">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** — делает возможной синхронизацию заголовков и строк заказов на продажу с помощью компонента интеграции данных из Microsoft Dynamics 365 for Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="cf1c2-136">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Microsoft Dynamics 365 for Finance and Operations to Sales</span></span>
    - <span data-ttu-id="cf1c2-137">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** — требуется поддержка интеграции решения "Перспективный клиент в наличные деньги" с помощью информационных объектов</span><span class="sxs-lookup"><span data-stu-id="cf1c2-137">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="cf1c2-138">После установки исправлений необходимо запустить следующее пакетное задание из формы SalesPopulateProspectToCash.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-138">After installing the hotfixes you have to trigger the following batch job from the form SalesPopulateProspectToCash.</span></span> <span data-ttu-id="cf1c2-139">Эта форма скрыта, так как она требуется только один раз.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-139">This form is hidden as you only need it once.</span></span> <span data-ttu-id="cf1c2-140">Для доступа к ней добавьте следующее в адрес в веб-браузере, когда выполнен вход в среду: &mi=action:SalesPopulateProspectToCash Например,</span><span class="sxs-lookup"><span data-stu-id="cf1c2-140">To access it add the following to your browser address, when logged in to the environment: &mi=action:SalesPopulateProspectToCash E.g.</span></span> <span data-ttu-id="cf1c2-141">https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash В открывшейся форме нажмите кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-141">https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash In the form that opens click OK.</span></span>
    <span data-ttu-id="cf1c2-142">При этом новое поле “LineCreationSequnceNumber” в таблицах “SalesLine”, “SalesQuotationLine” и “CustInvoiceTrans” будет заполнено уникальными значениями, и будет обновлен список продуктов.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-142">This will populate a new “LineCreationSequnceNumber” field in “SalesLine”, “SalesQuotationLine” and “CustInvoiceTrans” tables with unique values and refresh the product list.</span></span> <span data-ttu-id="cf1c2-143">Это необходимо, чтобы интеграции P2C работала в версии 7.1</span><span class="sxs-lookup"><span data-stu-id="cf1c2-143">This is needed for the P2C integration to work on 7.1</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="cf1c2-144">Системные требования для Sales</span><span class="sxs-lookup"><span data-stu-id="cf1c2-144">System requirements for Sales</span></span>

<span data-ttu-id="cf1c2-145">Чтобы использовать решение "Перспективный клиент в наличные деньги", вы должны установить следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="cf1c2-145">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="cf1c2-146">Microsoft Dynamics 365 for Sales версии 1612 (8.2.1.207) (БД 8.2.1.207) (сетевая версия)</span><span class="sxs-lookup"><span data-stu-id="cf1c2-146">Microsoft Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online</span></span>
- <span data-ttu-id="cf1c2-147">Решение "Перспективный клиент в наличные деньги" Microsoft Dynamics 365 for Sales, версия 1.15.0.0 (v15)</span><span class="sxs-lookup"><span data-stu-id="cf1c2-147">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

   > [!NOTE]
   >
   > <span data-ttu-id="cf1c2-148">Шаблоны с версией 1.0.0.0 и 1.0.0.1 поддерживаются в решении "Перспективный клиент в наличные деньги" для Microsoft Dynamics 365 for Sales, версия 1.14.1.0</span><span class="sxs-lookup"><span data-stu-id="cf1c2-148">Templates with version 1.0.0.0 and 1.0.0.1 are supported on Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.1.0</span></span>
   >
   > <span data-ttu-id="cf1c2-149">Шаблоны с версией 2.0.0.0 и 2.1.0.0 поддерживаются в решении "Перспективный клиент в наличные деньги" для Microsoft Dynamics 365 for Sales, версия 1.15.0.0</span><span class="sxs-lookup"><span data-stu-id="cf1c2-149">Templates with version 2.0.0.0 and 2.1.0.0 are upported on Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.15.0.0</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="cf1c2-150">Установка решения "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="cf1c2-150">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="cf1c2-151">Загрузите [ZIP-файл с пакетом решения "Перспективный клиент в наличные деньги" для Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) из CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-151">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="cf1c2-152">Убедитесь, что ZIP-файл разблокирован.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-152">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="cf1c2-153">В противном случае при попытке установить пакет решения появляется следующее сообщение об ошибке: "Пакеты для импорта не найдены".</span><span class="sxs-lookup"><span data-stu-id="cf1c2-153">Otherwise, when you try to install the solution package, you receive the following error message: "No import packages were found."</span></span> <span data-ttu-id="cf1c2-154">Чтобы разблокировать ZIP-файл щелкните на нем правой кнопкой мыши и выберите **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-154">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="cf1c2-155">Затем выберите **Разблокировать**.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-155">Then select **Unblock**.</span></span>
3. <span data-ttu-id="cf1c2-156">Распакуйте и запустите **PackageDeployer.exe**.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-156">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="cf1c2-157">Установите решение "Перспективный клиент в наличные деньги" в своем экземпляре Sales:</span><span class="sxs-lookup"><span data-stu-id="cf1c2-157">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="cf1c2-158">Выберите тип развертывания **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-158">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="cf1c2-159">Выберите **Показать дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-159">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="cf1c2-160">Для быстрой установки выберите регион.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-160">For a quick installation, select a region.</span></span> <span data-ttu-id="cf1c2-161">При выборе варианта **Не знаю** система выполняет поиск всех регионов, и установка займет больше времени.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-161">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="cf1c2-162">Введите имя пользователя и пароль для пользователя admin, у которого есть права на установку.</span><span class="sxs-lookup"><span data-stu-id="cf1c2-162">Enter the user name and password of an admin user who has installation rights.</span></span>

