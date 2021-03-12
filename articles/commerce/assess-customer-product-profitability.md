---
title: Оценка рентабельности по клиентам и продуктам
description: В этой статье описывается, как можно использовать размещенные в памяти аналитики и аналитики реального времени для получения доступа, изучения и анализа рентабельности клиентов и продуктов на основе данных Dynamics 365 Commerce.
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
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 3770832cb8eee96931d8f8e68c726d5e09d3fceb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980062"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="6a463-103">Оценка рентабельности по клиентам и продуктам</span><span class="sxs-lookup"><span data-stu-id="6a463-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6a463-104">В этой статье описывается, как можно использовать размещенные в памяти аналитики и аналитики реального времени для получения доступа, изучения и анализа рентабельности клиентов и продуктов на основе данных Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6a463-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="6a463-105">В рамках использования Commerce пользователи могут анализировать прибыльность ключевых клиентов (от 10 до 100) на разных уровнях иерархии организации с учетом одного из следующих критериев.</span><span class="sxs-lookup"><span data-stu-id="6a463-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="6a463-106">Сумма продаж</span><span class="sxs-lookup"><span data-stu-id="6a463-106">Sales amount</span></span>
- <span data-ttu-id="6a463-107">Количество</span><span class="sxs-lookup"><span data-stu-id="6a463-107">Quantity</span></span>
- <span data-ttu-id="6a463-108">Маржа для валовой прибыли</span><span class="sxs-lookup"><span data-stu-id="6a463-108">Gross profit margin</span></span>
- <span data-ttu-id="6a463-109">Процент маржи</span><span class="sxs-lookup"><span data-stu-id="6a463-109">Margin percentage</span></span>

<span data-ttu-id="6a463-110">Для этой оценки можно использовать готовый отчет **Ведущие клиенты**, который можно открыть в любом из следующих расположений.</span><span class="sxs-lookup"><span data-stu-id="6a463-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="6a463-111">Рабочая область **Управление магазином** &gt; **Retail и Commerce** &gt; **Каналы** &gt; **Управление магазином** &gt; **Отчеты** &gt; **Отчет о лучших клиентах**</span><span class="sxs-lookup"><span data-stu-id="6a463-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="6a463-112">Раздел **Запросы и отчеты** &gt; **Retail и Commerce** &gt; **Запросы и отчеты** &gt; **Отчеты о продажах** &gt; **Отчет о лучших клиентах**</span><span class="sxs-lookup"><span data-stu-id="6a463-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="6a463-113">Аналогично пользователи могут анализировать прибыльность ключевых продуктов (от 10 до 100) на разных уровнях иерархии организации с учетом одного из следующих критериев.</span><span class="sxs-lookup"><span data-stu-id="6a463-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="6a463-114">Сумма продаж</span><span class="sxs-lookup"><span data-stu-id="6a463-114">Sales amount</span></span>
- <span data-ttu-id="6a463-115">Количество</span><span class="sxs-lookup"><span data-stu-id="6a463-115">Quantity</span></span>
- <span data-ttu-id="6a463-116">Маржа для валовой прибыли</span><span class="sxs-lookup"><span data-stu-id="6a463-116">Gross profit margin</span></span>
- <span data-ttu-id="6a463-117">Процент маржи</span><span class="sxs-lookup"><span data-stu-id="6a463-117">Margin percentage</span></span>

<span data-ttu-id="6a463-118">Для этой оценки можно использовать готовый отчет **Ведущие продукты**, который можно открыть в любом из следующих расположений.</span><span class="sxs-lookup"><span data-stu-id="6a463-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="6a463-119">Рабочая область **Управление магазином** &gt; **Retail и Commerce** &gt; **Каналы** &gt; **Управление магазином** &gt; **Отчеты** &gt; **Отчет о лучших продуктах**</span><span class="sxs-lookup"><span data-stu-id="6a463-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="6a463-120">Рабочая область **Управление категориями и продуктами** &gt; **Retail и Commerce** &gt; **Продукты и категории** &gt; **Управление магазином** &gt; **Отчеты** &gt; **Отчет по лучшим продуктам**</span><span class="sxs-lookup"><span data-stu-id="6a463-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="6a463-121">Раздел **Запросы и отчеты** &gt; **Retail и Commerce** &gt; **Запросы и отчеты** &gt; **Отчеты о продажах** &gt; **Отчет о лучших продуктах**</span><span class="sxs-lookup"><span data-stu-id="6a463-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
