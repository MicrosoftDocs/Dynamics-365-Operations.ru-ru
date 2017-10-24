---
title: "Оценка рентабельности по клиентам и продуктам"
description: "В этой статье описывается, как можно использовать размещенные в памяти аналитики и аналитики реального времени для получения доступа, изучения и анализа рентабельности клиентов и продуктов на основе данных Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 84a9e0b3936adcf2ed99fddca77dd57dfedeb050
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="ef0e3-103">Оценка рентабельности по клиентам и продуктам</span><span class="sxs-lookup"><span data-stu-id="ef0e3-103">Assess customer and product profitability</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="ef0e3-104">В этой статье описывается, как можно использовать размещенные в памяти аналитики и аналитики реального времени для получения доступа, изучения и анализа рентабельности клиентов и продуктов на основе данных Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="ef0e3-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span> 

<span data-ttu-id="ef0e3-105">В рамках использования Dynamics 365 for Retail пользователи могут анализировать прибыльность ключевых клиентов (от 10 до 100) на разных уровнях иерархии организации с учетом одного из следующих критериев.</span><span class="sxs-lookup"><span data-stu-id="ef0e3-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="ef0e3-106">Сумма продаж</span><span class="sxs-lookup"><span data-stu-id="ef0e3-106">Sales amount</span></span>
-   <span data-ttu-id="ef0e3-107">Количество</span><span class="sxs-lookup"><span data-stu-id="ef0e3-107">Quantity</span></span>
-   <span data-ttu-id="ef0e3-108">Маржа для валовой прибыли</span><span class="sxs-lookup"><span data-stu-id="ef0e3-108">Gross profit margin</span></span>
-   <span data-ttu-id="ef0e3-109">Процент маржи</span><span class="sxs-lookup"><span data-stu-id="ef0e3-109">Margin percentage</span></span>

<span data-ttu-id="ef0e3-110">Для этой оценки можно использовать готовый отчет **Ведущие клиенты**, который можно открыть в любом из следующих расположений.</span><span class="sxs-lookup"><span data-stu-id="ef0e3-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="ef0e3-111">Рабочая область **Руководство розничного магазина** &gt; **Розничная торговля** &gt; **Каналы** &gt; **Управление розничными магазинами** &gt; **Отчеты** &gt; **Отчет о лучших клиентах**</span><span class="sxs-lookup"><span data-stu-id="ef0e3-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
-   <span data-ttu-id="ef0e3-112">Раздел **Запросы и отчеты** &gt; **Розничная торговля** &gt; **Запросы и отчеты** &gt; **Отчеты о продажах** &gt; **Отчет о лучших клиентах**</span><span class="sxs-lookup"><span data-stu-id="ef0e3-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="ef0e3-113">Аналогично пользователи могут анализировать прибыльность ключевых продуктов (от 10 до 100) на разных уровнях иерархии организации с учетом одного из следующих критериев.</span><span class="sxs-lookup"><span data-stu-id="ef0e3-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="ef0e3-114">Сумма продаж</span><span class="sxs-lookup"><span data-stu-id="ef0e3-114">Sales amount</span></span>
-   <span data-ttu-id="ef0e3-115">Количество</span><span class="sxs-lookup"><span data-stu-id="ef0e3-115">Quantity</span></span>
-   <span data-ttu-id="ef0e3-116">Маржа для валовой прибыли</span><span class="sxs-lookup"><span data-stu-id="ef0e3-116">Gross profit margin</span></span>
-   <span data-ttu-id="ef0e3-117">Процент маржи</span><span class="sxs-lookup"><span data-stu-id="ef0e3-117">Margin percentage</span></span>

<span data-ttu-id="ef0e3-118">Для этой оценки можно использовать готовый отчет **Ведущие продукты**, который можно открыть в любом из следующих расположений.</span><span class="sxs-lookup"><span data-stu-id="ef0e3-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="ef0e3-119">Рабочая область **Руководство розничного магазина** &gt; **Розничная торговля** &gt; **Каналы** &gt; **Управление розничными магазинами** &gt; **Отчеты** &gt; **Отчет "Самые популярные продукты"**</span><span class="sxs-lookup"><span data-stu-id="ef0e3-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="ef0e3-120">Рабочая область **Управление категориями и продуктами** &gt; **Розничная торговля** &gt; **Продукты и категории** &gt; **Управление розничными магазинами** &gt; **Отчеты** &gt; **Отчет "Ведущие продукты"**</span><span class="sxs-lookup"><span data-stu-id="ef0e3-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="ef0e3-121">Раздел **Запросы и отчеты** &gt; **Розничная торговля** &gt; **Запросы и отчеты** &gt; **Отчеты о продажах** &gt; **Отчет "Самые популярные продукты"**</span><span class="sxs-lookup"><span data-stu-id="ef0e3-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>




