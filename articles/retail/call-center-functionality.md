---
title: "Функциональность центра обработки вызовов"
description: "Этот раздел содержит обзор возможностей продаж в центре обработки вызовов в Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e85b65e116b32adca09e46252d7d3bbe5101e1cf
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="call-center"></a><span data-ttu-id="25a94-103">Центр обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="25a94-103">Call center</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="25a94-104">В Dynamics 365 for Retail центр обработки вызовов — это тип канала розничной торговли, который можно определить в приложении.</span><span class="sxs-lookup"><span data-stu-id="25a94-104">In Dynamics 365 for Retail, a call center is a type of Retail channel that can be defined in the application.</span></span> <span data-ttu-id="25a94-105">Определение конкретного канала для центра обработки вызовов позволяет системе связать значения по умолчанию конкретных данных и значения по умолчанию обработки заказов с заказами на продажу, созданными пользователем канала центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="25a94-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="25a94-106">К функциям центра обработки вызовов относятся дополнительные розничные цены и рекламные акции, каталоги, подарочные сертификаты, программы лояльности и купоны.</span><span class="sxs-lookup"><span data-stu-id="25a94-106">Call center features include advanced retail price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="25a94-107">Заказы центра обработки вызовов также используются приложением POS для поддержки сценариев выполнения заказов между каналами.</span><span class="sxs-lookup"><span data-stu-id="25a94-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="25a94-108">Важно отметить, что хотя модуль центра обработки вызовов можно использовать в других отраслях помимо розничной торговли, текущий выпуск приложения центра обработки вызовов Dynamics 365 for Retail не оптимизирован для использования в сценариях обработки заказов по схеме "предприятие-предприятие" (B2B) или в сценариях, когда в заказах имеется большое число строк продаж.</span><span class="sxs-lookup"><span data-stu-id="25a94-108">It's important to note that while the call center module can be utilized by other industries outside of Retail, the current release of the Dynamics 365 for Retail call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="25a94-109">Рекомендуется, чтобы пользователи, желающие использовать функции центра обработки вызовов для обработки заказов, не связанных со стандартным процессом обработки проводок напрямую клиенту, провели тщательное тестирование и проверку функциональных возможностей центра обработки для обеспечения соответствия функциональным потребностям и требованиям к производительности.</span><span class="sxs-lookup"><span data-stu-id="25a94-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="25a94-110">В дополнение к поддержке создания заказов модуль центра обработки вызовов также предоставляет удобное приложение по обслуживанию клиентов, которое упрощает пользователям поиск счетов клиентов и просмотр всех связанных данных заказов клиента и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="25a94-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="25a94-111">Экран обслуживания клиентов предоставляет возможность быстро получить доступ к связанным данным заказа, которые позволят пользователю ответить на самые распространенные связанные с заказом вопросы, полученные от клиентов.</span><span class="sxs-lookup"><span data-stu-id="25a94-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="25a94-112">Эта страница содержит ссылки на соответствующую документацию, относящуюся к настройке, конфигурации и функциональному использованию функций центра обработки вызов в Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="25a94-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features in Dynamics 365 for Retail.</span></span>

## <a name="configure-the-call-center"></a><span data-ttu-id="25a94-113">Настройка центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="25a94-113">Configure the call center</span></span>
[<span data-ttu-id="25a94-114">Настройка параметров обработки заказов</span><span class="sxs-lookup"><span data-stu-id="25a94-114">Set up order processing options</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="25a94-115">Настройка обработки заказов</span><span class="sxs-lookup"><span data-stu-id="25a94-115">Configure order processing</span></span>
<span data-ttu-id="25a94-116">[Настройка оповещений о мошенничестве](set-up-fraud-alerts.md)
[Удержания заказов вручную](work-with-order-holds.md)</span><span class="sxs-lookup"><span data-stu-id="25a94-116">[Set up fraud alerts](set-up-fraud-alerts.md)
[Manual Order Holds](work-with-order-holds.md)</span></span>

## <a name="configure-payment-processing"></a><span data-ttu-id="25a94-117">Настройка обработки платежей</span><span class="sxs-lookup"><span data-stu-id="25a94-117">Configure payment processing</span></span>
[<span data-ttu-id="25a94-118">Методы оплаты в центре обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="25a94-118">Payment methods in a call center</span></span>](work-with-payments.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="25a94-119">Настройка прямого маркетинга</span><span class="sxs-lookup"><span data-stu-id="25a94-119">Configure direct marketing</span></span>
[<span data-ttu-id="25a94-120">Каталоги центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="25a94-120">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="25a94-121">Настройка анализа RFM</span><span class="sxs-lookup"><span data-stu-id="25a94-121">Set up RFM analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="25a94-122">Настройка программ непрерывности</span><span class="sxs-lookup"><span data-stu-id="25a94-122">Configure continuity programs</span></span>
[<span data-ttu-id="25a94-123">Настройка программы непрерывности для центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="25a94-123">Set up a continuity program for a call center</span></span>](set-up-continuity-program.md)


