---
title: Отслеживание производительности продаж и маржи
description: Можно отслеживать производительность продаж и маржи в реальном времени с помощью Dynamics 365 Commerce.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a7b2b6ba8115b43ef2e52e934bf8364e6f4044e7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023871"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="ff595-103">Мониторинг эффективности продаж и маржи</span><span class="sxs-lookup"><span data-stu-id="ff595-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ff595-104">Можно отслеживать производительность продаж и маржи в реальном времени с помощью Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ff595-104">You can monitor sales and margin performance in real time using Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ff595-105">В Commerce пользователи смогут отслеживать производительность продажи и маржи в реальном времени на различных уровнях организационной иерархии для следующих аналитик:</span><span class="sxs-lookup"><span data-stu-id="ff595-105">As part of Commerce, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="ff595-106">Товары</span><span class="sxs-lookup"><span data-stu-id="ff595-106">Products</span></span>
- <span data-ttu-id="ff595-107">Категории</span><span class="sxs-lookup"><span data-stu-id="ff595-107">Categories</span></span>
- <span data-ttu-id="ff595-108">Скидки</span><span class="sxs-lookup"><span data-stu-id="ff595-108">Discounts</span></span>
- <span data-ttu-id="ff595-109">Годы как период времени</span><span class="sxs-lookup"><span data-stu-id="ff595-109">Years as time period</span></span>
- <span data-ttu-id="ff595-110">Регистры/терминалы</span><span class="sxs-lookup"><span data-stu-id="ff595-110">Registers/terminals</span></span>
- <span data-ttu-id="ff595-111">Персонал/сотрудники</span><span class="sxs-lookup"><span data-stu-id="ff595-111">Staff/employees</span></span>
- <span data-ttu-id="ff595-112">Клиенты</span><span class="sxs-lookup"><span data-stu-id="ff595-112">Customers</span></span>
- <span data-ttu-id="ff595-113">Операционные единицы</span><span class="sxs-lookup"><span data-stu-id="ff595-113">Operating units</span></span>

<span data-ttu-id="ff595-114">Кроме того, два уникальных отчета, в которых используются преимущества структуры иерархической сетки, позволяют пользователям контролировать производительность продажи и маржи, переходя от узла верхней категории к отдельным листовым узлам категории в иерархии категорий продукции по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff595-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default product category hierarchy.</span></span> <span data-ttu-id="ff595-115">Пользователи могут также переходить от верхней операционной единицы к отдельным каналам в организационной иерархии, которая определена как организационная иерархия по умолчанию для отчетов.</span><span class="sxs-lookup"><span data-stu-id="ff595-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for reporting.</span></span> <span data-ttu-id="ff595-116">Можно открывать отчеты из любого из следующих местонахождений:</span><span class="sxs-lookup"><span data-stu-id="ff595-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="ff595-117">Рабочая область **Управление магазином** &gt; **Retail и Commerce** &gt; **Каналы** &gt; **Управление магазином** &gt; **Отчеты**</span><span class="sxs-lookup"><span data-stu-id="ff595-117">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="ff595-118">Рабочая область **Управление категориями и продуктами** &gt; **Retail и Commerce** &gt; **Продукты и категории** &gt; **Управление магазинами** &gt; **Отчеты**</span><span class="sxs-lookup"><span data-stu-id="ff595-118">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Product and categories** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="ff595-119">Рабочая область **Управление ценообразованием и скидками** &gt; **Retail и Commerce** &gt; **Цены и скидки** &gt; **Управление магазинами** &gt; **Отчеты**</span><span class="sxs-lookup"><span data-stu-id="ff595-119">**Pricing and discount management** workspace &gt; **Retail and Commerce** &gt; **Pricing and discounts** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="ff595-120">Раздел **Запросы и отчеты** &gt; **Retail и Commerce** &gt; **Запросы и отчеты** &gt; **Отчеты о продажах**</span><span class="sxs-lookup"><span data-stu-id="ff595-120">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>
