---
title: Функциональность продаж в центре обработки вызовов
description: Этот раздел содержит обзор возможностей продаж в центре обработки вызовов в Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d188138654ba20d8393ed4bca8124a65402daff2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991448"
---
# <a name="call-center-sales-functionality"></a><span data-ttu-id="2d5b9-103">Функциональность продажи центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="2d5b9-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="2d5b9-104">В Dynamics 365 Commerce центр обработки вызовов — это тип канала, который можно определить в приложении.</span><span class="sxs-lookup"><span data-stu-id="2d5b9-104">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="2d5b9-105">Определение конкретного канала для центра обработки вызовов позволяет системе связать значения по умолчанию конкретных данных и значения по умолчанию обработки заказов с заказами на продажу, созданными пользователем канала центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="2d5b9-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="2d5b9-106">К функциям центра обработки вызовов относятся дополнительные и рекламные акции, каталоги, подарочные сертификаты, программы лояльности и купоны.</span><span class="sxs-lookup"><span data-stu-id="2d5b9-106">Call center features include advanced price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="2d5b9-107">Заказы центра обработки вызовов также используются приложением POS для поддержки сценариев выполнения заказов между каналами.</span><span class="sxs-lookup"><span data-stu-id="2d5b9-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="2d5b9-108">Важно отметить, что хотя модуль центра обработки вызовов можно использовать в других отраслях помимо Commerce, текущий выпуск приложения центра обработки вызовов не оптимизирован для использования в сценариях обработки заказов по схеме "предприятие-предприятие" (B2B) или в сценариях, когда в заказах имеется большое количество строк продаж.</span><span class="sxs-lookup"><span data-stu-id="2d5b9-108">It's important to note that while the call center module can be utilized by other industries outside of Commerce, the current release of the call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large number of sales lines.</span></span> <span data-ttu-id="2d5b9-109">Рекомендуется, чтобы пользователи, желающие использовать функции центра обработки вызовов для обработки заказов, не связанных со стандартным процессом обработки проводок напрямую клиенту, провели тщательное тестирование и проверку функциональных возможностей центра обработки для обеспечения соответствия функциональным потребностям и требованиям к производительности.</span><span class="sxs-lookup"><span data-stu-id="2d5b9-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="2d5b9-110">В дополнение к поддержке создания заказов модуль центра обработки вызовов также предоставляет удобное приложение по обслуживанию клиентов, которое упрощает пользователям поиск счетов клиентов и просмотр всех связанных данных заказов клиента и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2d5b9-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="2d5b9-111">Экран обслуживания клиентов предоставляет возможность быстро получить доступ к связанным данным заказа, которые позволят пользователю ответить на самые распространенные связанные с заказом вопросы, полученные от клиентов.</span><span class="sxs-lookup"><span data-stu-id="2d5b9-111">The customer service screen is designed to enable a user to quickly access order-related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="2d5b9-112">Эта страница содержит ссылки на соответствующую документацию, относящуюся к настройке, конфигурации и функциональному использованию функций центра обработки вызов.</span><span class="sxs-lookup"><span data-stu-id="2d5b9-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features.</span></span>


## <a name="configure-the-call-center"></a><span data-ttu-id="2d5b9-113">Настройка центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="2d5b9-113">Configure the call center</span></span>

[<span data-ttu-id="2d5b9-114">Настройка каналов центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="2d5b9-114">Set up call center channels</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="2d5b9-115">Настройка обработки заказов</span><span class="sxs-lookup"><span data-stu-id="2d5b9-115">Configure order processing</span></span>

[<span data-ttu-id="2d5b9-116">Настройка и работа с оповещениями мошенничества центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="2d5b9-116">Set up and work with call center fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="2d5b9-117">Настройка удержаний заказов центра обработки вызовов и работа с ними</span><span class="sxs-lookup"><span data-stu-id="2d5b9-117">Configure and work with call center order holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="2d5b9-118">Настройка обработки платежей</span><span class="sxs-lookup"><span data-stu-id="2d5b9-118">Configure payment processing</span></span>

[<span data-ttu-id="2d5b9-119">Способы оплаты в центрах обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="2d5b9-119">Payment methods in call centers</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="2d5b9-120">Настройка режимов доставки</span><span class="sxs-lookup"><span data-stu-id="2d5b9-120">Configure delivery modes</span></span>

[<span data-ttu-id="2d5b9-121">Настройка режимов доставки и расходов центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="2d5b9-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="2d5b9-122">Настройка прямого маркетинга</span><span class="sxs-lookup"><span data-stu-id="2d5b9-122">Configure direct marketing</span></span>

[<span data-ttu-id="2d5b9-123">Каталоги центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="2d5b9-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="2d5b9-124">Настройка анализа актуальности, периодичности и денежных значений (RFM)</span><span class="sxs-lookup"><span data-stu-id="2d5b9-124">Set up Recency, Frequency, and Monetary (RFM) analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="2d5b9-125">Настройка программ непрерывности</span><span class="sxs-lookup"><span data-stu-id="2d5b9-125">Configure continuity programs</span></span>

[<span data-ttu-id="2d5b9-126">Настройка программ непрерывности для центров обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="2d5b9-126">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
