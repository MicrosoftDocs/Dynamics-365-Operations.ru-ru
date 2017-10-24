---
title: "Решение \"Перспективный клиент в наличные деньги\""
description: "В этой теме представлен обзор решения \"Перспективный клиент в наличные деньги\" между Dynamics 365 for Finance and Operations, Enterprise Edition и Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="b983c-103">Решение "Перспективный клиент в наличные деньги"</span><span class="sxs-lookup"><span data-stu-id="b983c-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b983c-104">Решение "Перспективный клиент в наличные деньги" использует [интеграцию данных](/common-data-service/entity-reference/dynamics-365-integration) для синхронизации данных между экземплярами Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition и Dynamics 365 for Sales с помощью службы Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="b983c-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="b983c-105">Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных о счетах, контактах, продуктах, предложениях по продажам, заказах на продажу и накладных по продажам между Finance and Operations и Sales.</span><span class="sxs-lookup"><span data-stu-id="b983c-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="b983c-106">Во время выполнения обмена данными между Finance and Operations и Sales вы можете продолжать выполнять мероприятия по продажам и маркетингу в Sales и обрабатывать выполнение заказов с помощью управления запасами в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b983c-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="b983c-107">Это решение обеспечивает интеграцию в следующих областях:</span><span class="sxs-lookup"><span data-stu-id="b983c-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="b983c-108">Ведение счетов в Sales и их синхронизация с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b983c-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="b983c-109">Ведение контактов в Sales и их синхронизация с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b983c-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="b983c-110">Ведение продуктов в Finance and Operations и их синхронизация с Sales</span><span class="sxs-lookup"><span data-stu-id="b983c-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="b983c-111">Создание предложений по продажам в Sales и их синхронизация с Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b983c-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="b983c-112">Создание заказов на продажу в Finance and Operations и их синхронизация с Sales</span><span class="sxs-lookup"><span data-stu-id="b983c-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="b983c-113">Создание накладных по продажам в Finance and Operations и их синхронизация с Sales</span><span class="sxs-lookup"><span data-stu-id="b983c-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="b983c-114">Требования к системе для Dynamics 365 for Finance and Operations, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="b983c-114">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="b983c-115">Чтобы использовать решение "Перспективный клиент в наличные деньги", вы должны установить следующее:</span><span class="sxs-lookup"><span data-stu-id="b983c-115">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="b983c-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (июль 2017 г.) с обновлением платформы 8 (приложение 7.2.11792.56024 с платформой 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="b983c-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="b983c-117">Два исправления для Dynamics 365 for Finance and Operations, Enterprise Edition (июль 2017 г.).</span><span class="sxs-lookup"><span data-stu-id="b983c-117">Two hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>

    -  <span data-ttu-id="b983c-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) — это исправление делает возможным синхронизацию строк заказов на продажу с помощью компонента интеграции данных из Finance and Operations в Sales.</span><span class="sxs-lookup"><span data-stu-id="b983c-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="b983c-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) — это исправление делает возможным синхронизацию заказов на продажу с помощью компонента интеграции данных из Finance and Operations в Sales.</span><span class="sxs-lookup"><span data-stu-id="b983c-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
    
<span data-ttu-id="b983c-120">**Примечание**. Достаточно установить только KB4036524, потому что в пакет установки входят изменения из KB4036461.</span><span class="sxs-lookup"><span data-stu-id="b983c-120">**Note**: You only need to install KB4036524 because the installation includes the changes from KB4036461.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="b983c-121">Требования к системе для Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="b983c-121">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="b983c-122">Чтобы использовать решение "Перспективный клиент в наличные деньги", вы должны установить следующее:</span><span class="sxs-lookup"><span data-stu-id="b983c-122">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="b983c-123">Dynamics 365 for Sales версии 1612 (8.2.1.207) (БД 8.2.1.207) (сетевая версия) или выше.</span><span class="sxs-lookup"><span data-stu-id="b983c-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or later.</span></span>
- <span data-ttu-id="b983c-124">Решение "Перспективный клиент в наличные деньги" Dynamics 365 for Sales, версия 1.14.0.0 (v14) или выше.</span><span class="sxs-lookup"><span data-stu-id="b983c-124">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b983c-125">Установка решения "Перспективный клиент в наличные деньги" для Sales</span><span class="sxs-lookup"><span data-stu-id="b983c-125">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="b983c-126">Загрузите [ZIP-файл с пакетом решения "Перспективный клиент в наличные деньги" для Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) на CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="b983c-126">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="b983c-127">Убедитесь, что ZIP-файл не заблокирован, чтобы не получить при установке пакета решения сообщение об ошибке "Пакеты для импорта не найдены".</span><span class="sxs-lookup"><span data-stu-id="b983c-127">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="b983c-128">Чтобы разблокировать файл, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b983c-128">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="b983c-129">Щелкните ZIP-файл правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="b983c-129">Right-click the zip file.</span></span>
    -  <span data-ttu-id="b983c-130">Выберите **Свойства**, а затем выберите **Разблокировать**.</span><span class="sxs-lookup"><span data-stu-id="b983c-130">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="b983c-131">Распакуйте и запустите PackageDeployer.exe.</span><span class="sxs-lookup"><span data-stu-id="b983c-131">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="b983c-132">Установите решение "Перспективный клиент в наличные деньги" в своем экземпляре Sales.</span><span class="sxs-lookup"><span data-stu-id="b983c-132">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="b983c-133">Выберите тип развертывания **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="b983c-133">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="b983c-134">Выберите **Показать дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="b983c-134">Select **Show advanced**.</span></span>
    - <span data-ttu-id="b983c-135">Для быстрой установки выберите **Область**.</span><span class="sxs-lookup"><span data-stu-id="b983c-135">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="b983c-136">При выборе варианта **Не знаю** система выполняет поиск всех регионов, и установка займет больше времени.</span><span class="sxs-lookup"><span data-stu-id="b983c-136">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="b983c-137">Введите **Имя пользователя** и **Пароль** для пользователя admin, у которого есть права на установку.</span><span class="sxs-lookup"><span data-stu-id="b983c-137">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

