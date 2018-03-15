---
title: "Решение \"Перспективный клиент в наличные деньги\""
description: "В этой теме представлен обзор решения \"Перспективный клиент в наличные деньги\" между Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition и Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 02/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 95d5bf26c22238753586cf4a7aaf5c26f061a705
ms.openlocfilehash: 62f328c5a6bf5343c97de0b7d907bbcfe2fcde4d
ms.contentlocale: ru-ru
ms.lasthandoff: 02/23/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="8b1d6-103">Решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="8b1d6-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8b1d6-104">Решение "Перспективный клиент в наличные деньги" обеспечивает прямую синхронизацию между Dynamics 365 for Finance and Operations, Enterprise Edition и Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, Enterprise edition, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="8b1d6-105">Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных для организаций, контактов, продуктов, предложений по продажам, заказов на продажу и накладных по продажам между Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="8b1d6-106">Во время выполнения обмена данными между Finance and Operations и Sales вы можете выполнять мероприятия по продажам и маркетингу в Sales и обрабатывать выполнение заказов с помощью управления запасами в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="8b1d6-107">Дополнительные сведения об интеграции решения "Перспективный клиент в наличные деньги" см. в коротком видео на YouTube:</span><span class="sxs-lookup"><span data-stu-id="8b1d6-107">For more information about the Prospect to cash integration, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

<span data-ttu-id="8b1d6-108">В текущей версии решение "Перспективный клиент в наличные деньги" предоставляет следующие типы прямой синхронизации:</span><span class="sxs-lookup"><span data-stu-id="8b1d6-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="8b1d6-109">Ведение организаций в Sales и их прямая синхронизация из Sales в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8b1d6-109">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="8b1d6-110">Ведение продуктов в Finance and Operations и их синхронизация напрямую с Sales</span><span class="sxs-lookup"><span data-stu-id="8b1d6-110">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="8b1d6-111">Ведение контактов в Sales и их синхронизация с контактами или клиентами напрямую в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8b1d6-111">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="8b1d6-112">Синхронизация предложений по продажам напрямую из Sales с Finance and Operations (шаблон ожидает выпуска)</span><span class="sxs-lookup"><span data-stu-id="8b1d6-112">Synchronize sales quotation directly from Sales to Finance and Operations (template pending release)</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="8b1d6-113">Синхронизация заказов на продажу напрямую из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="8b1d6-113">Synchronize sales orders directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)
- [<span data-ttu-id="8b1d6-114">Синхронизация заказов на продажу напрямую между Sales и Finance and Operations (шаблон ожидает выпуска)</span><span class="sxs-lookup"><span data-stu-id="8b1d6-114">Synchronize sales orders directly between Sales and Finance and Operations (template pending release)</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="8b1d6-115">Синхронизация накладных по продаже напрямую из Finance and Operations в Sales</span><span class="sxs-lookup"><span data-stu-id="8b1d6-115">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="8b1d6-116">Системные требования для Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8b1d6-116">System requirements for Finance and Operations</span></span>

<span data-ttu-id="8b1d6-117">Интеграция решения "Перспективный клиент в наличные деньги" поддерживается в следующих версиях:</span><span class="sxs-lookup"><span data-stu-id="8b1d6-117">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="8b1d6-118">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (декабрь 2017 г.)</span><span class="sxs-lookup"><span data-stu-id="8b1d6-118">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="8b1d6-119">Dynamics 365 for Finance and Operations, Enterprise Edition (декабрь 2017 г.) — сборка приложения 7.3.11971.56116 с обновлением платформы 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="8b1d6-119">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="8b1d6-120">Dynamics 365 for Finance and Operations, Enterprise Edition (июль 2017 г.)</span><span class="sxs-lookup"><span data-stu-id="8b1d6-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="8b1d6-121">Dynamics 365 for Finance and Operations, Enterprise Edition (июль 2017 г.) — с обновлением платформы 8 (сборка приложения 7.2.11792.56024 со сборкой платформы 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="8b1d6-121">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="8b1d6-122">Следующие исправления являются обязательными:</span><span class="sxs-lookup"><span data-stu-id="8b1d6-122">The following hotfixes are required:</span></span>

    - <span data-ttu-id="8b1d6-123">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** — это исправление делает возможным синхронизацию заказов на продажу из Sales в Finance and Operations с помощью компонента интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-123">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="8b1d6-124">Оно также предоставляет несколько других улучшений.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-124">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="8b1d6-125">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** — это исправление делает возможным синхронизацию строк заказов на продажу из Finance and Operations в Sales с помощью компонента интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-125">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="8b1d6-126">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** — это исправление делает возможным синхронизацию заказов на продажу из Finance and Operations в Sales с помощью компонента интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-126">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8b1d6-127">Достаточно установить только KB4045570, потому что в пакет установки входят изменения из других исправлений.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-127">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="8b1d6-128">Dynamics 365 for Finance and Operations, версия 1611 (ноябрь 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="8b1d6-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="8b1d6-129">Dynamics 365 for Finance and Operations, версия 1611 (ноябрь 2016 г.) с обновлением платформы 8 или выше</span><span class="sxs-lookup"><span data-stu-id="8b1d6-129">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="8b1d6-130">Следующие исправления являются обязательными:</span><span class="sxs-lookup"><span data-stu-id="8b1d6-130">The following hotfixes are required:</span></span>

    - <span data-ttu-id="8b1d6-131">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** — делает возможной синхронизацию заказов на продажу с помощью компонента интеграции данных из Finance and Operations в Sales.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-131">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
    - <span data-ttu-id="8b1d6-132">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** — делает возможной синхронизацию заголовков и строк заказов на продажу с помощью компонента интеграции данных из Finance and Operations в Sales.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-132">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
    - <span data-ttu-id="8b1d6-133">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** — требуется поддержка интеграции решения "Перспективный клиент в наличные деньги" с помощью информационных объектов.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-133">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8b1d6-134">После установки исправлений необходимо запустить следующее пакетное задание из формы **SalesPopulateProspectToCash**.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-134">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="8b1d6-135">Эта форма скрыта, так как она требуется только один раз.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-135">This form is hidden because you only need it once.</span></span> <span data-ttu-id="8b1d6-136">Для доступа к форме выполните вход в среду и добавьте следующее в URL-адрес в веб-браузере: &mi=action:SalesPopulateProspectToCash, Например, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-136">To access the form, log in to the environment and add the following to the URL in your browser address: &mi=action:SalesPopulateProspectToCash, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="8b1d6-137">Когда форма откроется, щелкните OK.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-137">When the form opens, click OK.</span></span> <span data-ttu-id="8b1d6-138">При этом новое поле **LineCreationSequnceNumber** в таблицах **SalesLine**, **SalesQuotationLine** и **CustInvoiceTrans** будет заполнено уникальными значениями, и будет обновлен список продуктов.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-138">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="8b1d6-139">Это необходимо для работы интеграции решения "Перспективный клиент в наличные деньги".</span><span class="sxs-lookup"><span data-stu-id="8b1d6-139">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="8b1d6-140">Системные требования для Sales</span><span class="sxs-lookup"><span data-stu-id="8b1d6-140">System requirements for Sales</span></span>

<span data-ttu-id="8b1d6-141">Чтобы использовать решение "Перспективный клиент в наличные деньги", вы должны установить следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="8b1d6-141">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="8b1d6-142">Dynamics 365 for Sales версии 1612 (8.2.1.207) (БД 8.2.1.207) (сетевая версия)</span><span class="sxs-lookup"><span data-stu-id="8b1d6-142">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online</span></span>
- <span data-ttu-id="8b1d6-143">Решение "Перспективный клиент в наличные деньги" для Dynamics 365 for Sales, версия 1.15.0.0 (v15)</span><span class="sxs-lookup"><span data-stu-id="8b1d6-143">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="8b1d6-144">Установка решения "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="8b1d6-144">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="8b1d6-145">Загрузите [ZIP-файл с пакетом решения "Перспективный клиент в наличные деньги" для Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) из CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-145">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="8b1d6-146">Убедитесь, что ZIP-файл разблокирован.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-146">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="8b1d6-147">В противном случае при попытке установить пакет решения может появиться следующее сообщение об ошибке: "Пакеты для импорта не найдены".</span><span class="sxs-lookup"><span data-stu-id="8b1d6-147">Otherwise, when you try to install the solution package, you may receive the following error message, "No import packages were found."</span></span> <span data-ttu-id="8b1d6-148">Чтобы разблокировать ZIP-файл щелкните на нем правой кнопкой мыши и выберите **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-148">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="8b1d6-149">Выберите **Разблокировать**.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-149">Select **Unblock**.</span></span>
3. <span data-ttu-id="8b1d6-150">Распакуйте и запустите **PackageDeployer.exe**.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-150">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="8b1d6-151">Установите решение "Перспективный клиент в наличные деньги" в своем экземпляре Sales:</span><span class="sxs-lookup"><span data-stu-id="8b1d6-151">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="8b1d6-152">Выберите тип развертывания **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-152">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="8b1d6-153">Выберите **Показать дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-153">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="8b1d6-154">Для быстрой установки выберите регион.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-154">For a quick installation, select a region.</span></span> <span data-ttu-id="8b1d6-155">При выборе варианта **Не знаю** система выполняет поиск всех регионов, и установка займет больше времени.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-155">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="8b1d6-156">Введите имя пользователя и пароль для пользователя admin, у которого есть права на установку.</span><span class="sxs-lookup"><span data-stu-id="8b1d6-156">Enter the user name and password of an admin user who has installation rights.</span></span>



