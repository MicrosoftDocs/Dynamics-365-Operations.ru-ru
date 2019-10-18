---
title: Отслеживание производительности продаж и маржи
description: Можно отслеживать производительность продаж и маржи в реальном времени с помощью Dynamics 365 Retail.
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
ms.openlocfilehash: 46ecefdd15a3a208588aaf630571764047464cdb
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018072"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="c5816-103">Мониторинг эффективности продаж и маржи</span><span class="sxs-lookup"><span data-stu-id="c5816-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c5816-104">Можно отслеживать производительность продаж и маржи в реальном времени с помощью Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="c5816-104">You can monitor sales and margin performance in real time using Dynamics 365 Retail.</span></span>

<span data-ttu-id="c5816-105">В Retail пользователи смогут отслеживать производительность продажи и маржи в реальном времени на различных уровнях организационной иерархии для следующих аналитик:</span><span class="sxs-lookup"><span data-stu-id="c5816-105">As part of Retail, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="c5816-106">Товары</span><span class="sxs-lookup"><span data-stu-id="c5816-106">Products</span></span>
- <span data-ttu-id="c5816-107">Категории</span><span class="sxs-lookup"><span data-stu-id="c5816-107">Categories</span></span>
- <span data-ttu-id="c5816-108">Скидки</span><span class="sxs-lookup"><span data-stu-id="c5816-108">Discounts</span></span>
- <span data-ttu-id="c5816-109">Годы как период времени</span><span class="sxs-lookup"><span data-stu-id="c5816-109">Years as time period</span></span>
- <span data-ttu-id="c5816-110">Регистры/терминалы</span><span class="sxs-lookup"><span data-stu-id="c5816-110">Registers/terminals</span></span>
- <span data-ttu-id="c5816-111">Персонал/сотрудники</span><span class="sxs-lookup"><span data-stu-id="c5816-111">Staff/employees</span></span>
- <span data-ttu-id="c5816-112">Клиенты</span><span class="sxs-lookup"><span data-stu-id="c5816-112">Customers</span></span>
- <span data-ttu-id="c5816-113">Операционные единицы</span><span class="sxs-lookup"><span data-stu-id="c5816-113">Operating units</span></span>

<span data-ttu-id="c5816-114">Кроме того, два уникальных отчета, в которых используются преимущества структуры иерархической сетки, позволяют пользователям контролировать производительность продажи и маржи, переходя от узла верхней категории к отдельным листовым узлам категории в иерархии категорий розничной продукции по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c5816-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default retail product category hierarchy.</span></span> <span data-ttu-id="c5816-115">Пользователи могут также переходить от верхней операционной единицы к отдельным каналам в организационной иерархии, которая определена как организационная иерархия по умолчанию для целей иерархии розничных отчетов.</span><span class="sxs-lookup"><span data-stu-id="c5816-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for retail reporting hierarchy purposes.</span></span> <span data-ttu-id="c5816-116">Можно открывать отчеты из любого из следующих местонахождений:</span><span class="sxs-lookup"><span data-stu-id="c5816-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="c5816-117">Рабочая область **Руководство розничного магазина** &gt; **Розничная торговля** &gt; **Каналы** &gt; **Управление розничными магазинами** &gt; **Отчеты**</span><span class="sxs-lookup"><span data-stu-id="c5816-117">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="c5816-118">Рабочая область **Управление категориями и продуктами** &gt; **Розничная торговля** &gt; **Продукты и категории** &gt; **Управление розничными магазинами** &gt; **Отчеты**</span><span class="sxs-lookup"><span data-stu-id="c5816-118">**Category and product management** workspace &gt; **Retail** &gt; **Product and categories** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="c5816-119">Рабочая область **Управление ценообразованием и скидками** &gt; **Розничная торговля** &gt; **Цены и скидки** &gt; **Управление розничными магазинами** &gt; **Отчеты**</span><span class="sxs-lookup"><span data-stu-id="c5816-119">**Pricing and discount management** workspace &gt; **Retail** &gt; **Pricing and discounts** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="c5816-120">Раздел **Запросы и отчеты** &gt; **Розничная торговля** &gt; **Запросы и отчеты** &gt; **Отчеты о продажах**</span><span class="sxs-lookup"><span data-stu-id="c5816-120">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>
