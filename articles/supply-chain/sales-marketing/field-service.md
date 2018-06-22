---
title: "Интеграция с Microsoft Dynamics 365 for Field Service"
description: "В этом разделе представлен обзор интеграции с Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a57e23691a6b4d48c6b8dd6d1f61fc9730365b39
ms.openlocfilehash: 0c1268d2fddcf7b28ecfc3197f21e9d30a5a5855
ms.contentlocale: ru-ru
ms.lasthandoff: 05/31/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="b1b85-103">Интеграция с Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="b1b85-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b1b85-104">Microsoft Dynamics 365 for Finance and Operations включает синхронизацию бизнес-процессов между Finance and Operations и Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="b1b85-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="b1b85-105">Варианты интеграции настраиваются с помощью расширяемых шаблонов интегратора данных и службы Common Data Service (CDS) для обеспечения синхронизации бизнес-процессов.</span><span class="sxs-lookup"><span data-stu-id="b1b85-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="b1b85-106">[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="b1b85-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="b1b85-107">Первый этап интеграции между Field Service и Finance and Operations направлен на то, чтобы счета за заказы на выполнение работ и соглашения в Field Service можно было выставлять в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b1b85-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="b1b85-108">Поддерживаемый поток начинается в Field Service, где информация из заказов на выполнение работ синхронизируется с Finance and Operations в виде заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="b1b85-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="b1b85-109">В Finance and Operations счета за заказы на продажу выставляются для создания документов накладных.</span><span class="sxs-lookup"><span data-stu-id="b1b85-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="b1b85-110">Кроме того, информация из накладных договора в Field Service синхронизируется с Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b1b85-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="b1b85-111">Интегратор данных Microsoft Dynamics 365 синхронизирует данные с помощью настраиваемых проектов.</span><span class="sxs-lookup"><span data-stu-id="b1b85-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="b1b85-112">Стандартные шаблоны можно использовать для создания настраиваемых проектов интеграции, где дополнительные стандартные и настраиваемые поля, а также объекты, могут быть сопоставлены для настройки интеграции и соответствия определенным требованиям.</span><span class="sxs-lookup"><span data-stu-id="b1b85-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="b1b85-113">Первый этап интеграции между Field Service and Finance and Operations включает синхронизацию следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="b1b85-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="b1b85-114">Продукты в Finance and Operations с продуктами в Field Service, которые включают сведения о типе продукта</span><span class="sxs-lookup"><span data-stu-id="b1b85-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="b1b85-115">Заказы на выполнение работ в Field Service с заказами на продажу в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b1b85-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="b1b85-116">Накладные в Field Service с накладными с произвольным текстом в Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b1b85-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="b1b85-117">Чтобы просмотреть пример того, как можно выполнять синхронизацию заказа на выполнение работ между Field Service и Finance and Operations, просмотрите это короткое видео на YouTube [Синхронизация заказа на выполнение работ между Dynamics 365 for Field Service и Finance and Operations](https://www.youtube.com/watch?v=hAB4TDVMjxU).</span><span class="sxs-lookup"><span data-stu-id="b1b85-117">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video [Synchronize a work order between Dynamics 365 for Field Service and Finance and Operations](https://www.youtube.com/watch?v=hAB4TDVMjxU).</span></span>

[![](https://img.youtube.com/vi/hAB4TDVMjxU/0.jpg)](https://www.youtube.com/watch?v=hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="b1b85-118">Системные требования для Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b1b85-118">System requirements for Finance and Operations</span></span>
<span data-ttu-id="b1b85-119">Интеграция Field Service поддерживает следующие версии:</span><span class="sxs-lookup"><span data-stu-id="b1b85-119">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="b1b85-120">Dynamics 365 for Finance and Operations, версия 8.0 (апрель 2018 г.) и новее</span><span class="sxs-lookup"><span data-stu-id="b1b85-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="b1b85-121">Dynamics 365 for Finance and Operations версии 8.0 (апрель 2018) выпущена в апреле 2018 и имеет номер сборки приложения 8.0.30.8020 с обновлением платформы 15 (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="b1b85-121">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="b1b85-122">Системные требования для Field Service</span><span class="sxs-lookup"><span data-stu-id="b1b85-122">System requirements for Field Service</span></span>
<span data-ttu-id="b1b85-123">Чтобы использовать решение интеграции Field Service, вы должны установить следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="b1b85-123">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="b1b85-124">Microsoft Dynamics 365 for Field Service 9.0 или новее</span><span class="sxs-lookup"><span data-stu-id="b1b85-124">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="b1b85-125">Dynamics 365 for Field Service версии 1612 (9.0.1.733) (БД 9.0.1.733) (сетевая версия) или более новой.</span><span class="sxs-lookup"><span data-stu-id="b1b85-125">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="b1b85-126">Решение "Перспективный клиент в наличные деньги" (P2C) для Dynamics 365, версия 1.15.0.1 или более новая версия.</span><span class="sxs-lookup"><span data-stu-id="b1b85-126">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="b1b85-127">Это решение можно загрузить с сайта [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="b1b85-127">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="b1b85-128">Решение интеграции Field Service для Dynamics 365, версия 1.0.0.0 или более новая.</span><span class="sxs-lookup"><span data-stu-id="b1b85-128">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="b1b85-129">Это решение можно загрузить с сайта [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span><span class="sxs-lookup"><span data-stu-id="b1b85-129">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span></span>

