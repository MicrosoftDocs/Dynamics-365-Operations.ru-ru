---
title: Оценка рентабельности по клиентам и продуктам
description: В этой статье описывается, как можно использовать размещенные в памяти аналитики и аналитики реального времени для получения доступа, изучения и анализа рентабельности клиентов и продуктов на основе данных Microsoft Dynamics 365 for Retail.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 28d4eeaa3fcae33f817690ad496b4b123a5838ce
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561372"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="670df-103">Оценка рентабельности по клиентам и продуктам</span><span class="sxs-lookup"><span data-stu-id="670df-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="670df-104">В этой статье описывается, как можно использовать размещенные в памяти аналитики и аналитики реального времени для получения доступа, изучения и анализа рентабельности клиентов и продуктов на основе данных Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="670df-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span>

<span data-ttu-id="670df-105">В рамках использования Dynamics 365 for Retail пользователи могут анализировать прибыльность ключевых клиентов (от 10 до 100) на разных уровнях иерархии организации с учетом одного из следующих критериев.</span><span class="sxs-lookup"><span data-stu-id="670df-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="670df-106">Сумма продаж</span><span class="sxs-lookup"><span data-stu-id="670df-106">Sales amount</span></span>
- <span data-ttu-id="670df-107">Количество</span><span class="sxs-lookup"><span data-stu-id="670df-107">Quantity</span></span>
- <span data-ttu-id="670df-108">Маржа для валовой прибыли</span><span class="sxs-lookup"><span data-stu-id="670df-108">Gross profit margin</span></span>
- <span data-ttu-id="670df-109">Процент маржи</span><span class="sxs-lookup"><span data-stu-id="670df-109">Margin percentage</span></span>

<span data-ttu-id="670df-110">Для этой оценки можно использовать готовый отчет **Ведущие клиенты**, который можно открыть в любом из следующих расположений.</span><span class="sxs-lookup"><span data-stu-id="670df-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="670df-111">Рабочая область **Руководство розничного магазина** &gt; **Розничная торговля** &gt; **Каналы** &gt; **Управление розничными магазинами** &gt; **Отчеты** &gt; **Отчет о лучших клиентах**</span><span class="sxs-lookup"><span data-stu-id="670df-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="670df-112">Раздел **Запросы и отчеты** &gt; **Розничная торговля** &gt; **Запросы и отчеты** &gt; **Отчеты о продажах** &gt; **Отчет о лучших клиентах**</span><span class="sxs-lookup"><span data-stu-id="670df-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="670df-113">Аналогично пользователи могут анализировать прибыльность ключевых продуктов (от 10 до 100) на разных уровнях иерархии организации с учетом одного из следующих критериев.</span><span class="sxs-lookup"><span data-stu-id="670df-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="670df-114">Сумма продаж</span><span class="sxs-lookup"><span data-stu-id="670df-114">Sales amount</span></span>
- <span data-ttu-id="670df-115">Количество</span><span class="sxs-lookup"><span data-stu-id="670df-115">Quantity</span></span>
- <span data-ttu-id="670df-116">Маржа для валовой прибыли</span><span class="sxs-lookup"><span data-stu-id="670df-116">Gross profit margin</span></span>
- <span data-ttu-id="670df-117">Процент маржи</span><span class="sxs-lookup"><span data-stu-id="670df-117">Margin percentage</span></span>

<span data-ttu-id="670df-118">Для этой оценки можно использовать готовый отчет **Ведущие продукты**, который можно открыть в любом из следующих расположений.</span><span class="sxs-lookup"><span data-stu-id="670df-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="670df-119">Рабочая область **Руководство розничного магазина** &gt; **Розничная торговля** &gt; **Каналы** &gt; **Управление розничными магазинами** &gt; **Отчеты** &gt; **Отчет "Самые популярные продукты"**</span><span class="sxs-lookup"><span data-stu-id="670df-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="670df-120">Рабочая область **Управление категориями и продуктами** &gt; **Розничная торговля** &gt; **Продукты и категории** &gt; **Управление розничными магазинами** &gt; **Отчеты** &gt; **Отчет "Ведущие продукты"**</span><span class="sxs-lookup"><span data-stu-id="670df-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="670df-121">Раздел **Запросы и отчеты** &gt; **Розничная торговля** &gt; **Запросы и отчеты** &gt; **Отчеты о продажах** &gt; **Отчет "Самые популярные продукты"**</span><span class="sxs-lookup"><span data-stu-id="670df-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
