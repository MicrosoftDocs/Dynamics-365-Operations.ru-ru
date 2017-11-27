---
title: "Решение \"Перспективный клиент в наличные деньги\""
description: "В этой теме представлен обзор решения \"Перспективный клиент в наличные деньги\" между Dynamics 365 for Finance and Operations, Enterprise Edition и Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 2accf77c5241adff7ad1648737dde451153fde46
ms.contentlocale: ru-ru
ms.lasthandoff: 11/14/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="e4792-103">Решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="e4792-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e4792-104">Решение "Перспективный клиент в наличные деньги" использует [интеграцию данных](/common-data-service/entity-reference/dynamics-365-integration) для синхронизации данных между экземплярами Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition и Dynamics 365 for Sales с помощью службы Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="e4792-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="e4792-105">Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных о счетах, контактах, продуктах, предложениях по продажам, заказах на продажу и накладных по продажам между Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="e4792-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="e4792-106">Во время выполнения обмена данными между Finance and Operations и Sales вы можете продолжать выполнять мероприятия по продажам и маркетингу в Sales и обрабатывать выполнение заказов с помощью управления запасами в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e4792-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="e4792-107">Это решение обеспечивает интеграцию в следующих областях:</span><span class="sxs-lookup"><span data-stu-id="e4792-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="e4792-108">Ведение счетов в Sales и их синхронизация с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e4792-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="e4792-109">Ведение контактов в Sales и их синхронизация с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e4792-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="e4792-110">Ведение продуктов в Finance and Operations и их синхронизация с Sales</span><span class="sxs-lookup"><span data-stu-id="e4792-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="e4792-111">Создание предложений по продажам в Sales и их синхронизация с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e4792-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="e4792-112">Создание заказов на продажу в Finance and Operations и их синхронизация с Sales</span><span class="sxs-lookup"><span data-stu-id="e4792-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="e4792-113">Создание накладных по продажам в Finance and Operations и их синхронизация с Sales</span><span class="sxs-lookup"><span data-stu-id="e4792-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

<span data-ttu-id="e4792-114">Это решение обеспечивает прямую синхронизацию в следующих областях:</span><span class="sxs-lookup"><span data-stu-id="e4792-114">This solution provides direct synchronization in the following areas:</span></span>

-   [<span data-ttu-id="e4792-115">Ведение организаций в Sales и их прямая синхронизация из Sales в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e4792-115">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
-   [<span data-ttu-id="e4792-116">Ведение продуктов в Finance and Operations и их прямая синхронизация с Sales</span><span class="sxs-lookup"><span data-stu-id="e4792-116">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
-   [<span data-ttu-id="e4792-117">Ведение контактов в Sales и их прямая синхронизация с контактами или клиентами в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e4792-117">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
-   [<span data-ttu-id="e4792-118">Синхронизация заголовков и строк предложений по продажам напрямую из Sales с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e4792-118">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
-   [<span data-ttu-id="e4792-119">Создание заказов на продажу в Finance and Operations и их прямая синхронизация с Sales</span><span class="sxs-lookup"><span data-stu-id="e4792-119">Create sales orders in Finance and Operations and sync them directly to Sales</span></span>](sales-order-template-mapping-direct.md)
-  [<span data-ttu-id="e4792-120">Синхронизация заголовков и строк заказов на продажу непосредственно между Sales и Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e4792-120">Synchronize sales order headers and lines directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-between-sales-fin.md)
-   [<span data-ttu-id="e4792-121">Синхронизация заказов на продажу непосредственно между Sales и Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e4792-121">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
-   [<span data-ttu-id="e4792-122">Создание накладных по продажам в Finance and Operations и их прямая синхронизация с Sales</span><span class="sxs-lookup"><span data-stu-id="e4792-122">Create sales invoices in Finance and Operations and sync them directly to Sales</span></span>](sales-invoice-template-mapping-direct.md)


## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="e4792-123">Требования к системе для Dynamics 365 for Finance and Operations, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="e4792-123">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="e4792-124">Чтобы использовать решение "Перспективный клиент в наличные деньги", вы должны установить следующее:</span><span class="sxs-lookup"><span data-stu-id="e4792-124">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="e4792-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (июль 2017 г.) с обновлением платформы 8 (приложение 7.2.11792.56024 с платформой 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="e4792-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="e4792-126">Исправления для Dynamics 365 for Finance and Operations, Enterprise Edition (июль 2017 г.).</span><span class="sxs-lookup"><span data-stu-id="e4792-126">Hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>
        
    -  <span data-ttu-id="e4792-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) — это исправление обеспечивает поддержку синхронизации заказов на продажу с функцией интеграции данных из Sales в Finance and Operations, а также ряд других улучшений.</span><span class="sxs-lookup"><span data-stu-id="e4792-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) - This hotfix enabels support for sales order synchronization with the Data Integration feature from Sales to Finance and Operations, along with a number of other enhancements.</span></span>

    -  <span data-ttu-id="e4792-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) — это исправление делает возможным синхронизацию строк заказов на продажу с помощью компонента интеграции данных из Finance and Operations в Sales.</span><span class="sxs-lookup"><span data-stu-id="e4792-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="e4792-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) — это исправление делает возможным синхронизацию заказов на продажу с помощью компонента интеграции данных из Finance and Operations в Sales.</span><span class="sxs-lookup"><span data-stu-id="e4792-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>

<span data-ttu-id="e4792-130">**Примечание**. Достаточно установить только KB4045570, потому что в пакет установки входят изменения из других пакетов исправлений.</span><span class="sxs-lookup"><span data-stu-id="e4792-130">**Note**: You only need to install KB4045570 because the installation includes the changes from the other KB's.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="e4792-131">Требования к системе для Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="e4792-131">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="e4792-132">Чтобы использовать решение "Перспективный клиент в наличные деньги", вы должны установить следующее:</span><span class="sxs-lookup"><span data-stu-id="e4792-132">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="e4792-133">Dynamics 365 for Sales версии 1612 (8.2.1.207) (БД 8.2.1.207) (сетевая версия).</span><span class="sxs-lookup"><span data-stu-id="e4792-133">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online.</span></span>
- <span data-ttu-id="e4792-134">Решение "Перспективный клиент в наличные деньги" Dynamics 365 for Sales, версия 1.14.0.0 (v14) или выше.</span><span class="sxs-lookup"><span data-stu-id="e4792-134">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e4792-135">Установка решения "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="e4792-135">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="e4792-136">Загрузите [ZIP-файл с пакетом решения "Перспективный клиент в наличные деньги" для Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) на CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="e4792-136">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="e4792-137">Убедитесь, что ZIP-файл не заблокирован, чтобы не получить при установке пакета решения сообщение об ошибке "Пакеты для импорта не найдены".</span><span class="sxs-lookup"><span data-stu-id="e4792-137">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="e4792-138">Чтобы разблокировать файл, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="e4792-138">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="e4792-139">Щелкните ZIP-файл правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="e4792-139">Right-click the zip file.</span></span>
    -  <span data-ttu-id="e4792-140">Выберите **Свойства**, а затем выберите **Разблокировать**.</span><span class="sxs-lookup"><span data-stu-id="e4792-140">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="e4792-141">Распакуйте и запустите PackageDeployer.exe.</span><span class="sxs-lookup"><span data-stu-id="e4792-141">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="e4792-142">Установите решение "Перспективный клиент в наличные деньги" в своем экземпляре Sales.</span><span class="sxs-lookup"><span data-stu-id="e4792-142">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="e4792-143">Выберите тип развертывания **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="e4792-143">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="e4792-144">Выберите **Показать дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="e4792-144">Select **Show advanced**.</span></span>
    - <span data-ttu-id="e4792-145">Для быстрой установки выберите **Область**.</span><span class="sxs-lookup"><span data-stu-id="e4792-145">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="e4792-146">При выборе варианта **Не знаю** система выполняет поиск всех регионов, и установка займет больше времени.</span><span class="sxs-lookup"><span data-stu-id="e4792-146">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="e4792-147">Введите **Имя пользователя** и **Пароль** для пользователя admin, у которого есть права на установку.</span><span class="sxs-lookup"><span data-stu-id="e4792-147">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

