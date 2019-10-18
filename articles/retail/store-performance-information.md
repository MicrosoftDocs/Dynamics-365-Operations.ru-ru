---
title: Анализ эффективности магазина
description: В этой статье описывается, как можно использовать размещенные в памяти аналитики и аналитики реального времени для получения доступа, изучения и анализа эффективности магазина на основе данных Dynamics 365 Retail.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelReport, RetailChannelManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b2ea6ad2e3d9589face06cd5f950973209c17d41
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017790"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="adbca-103">Анализ производительности магазина</span><span class="sxs-lookup"><span data-stu-id="adbca-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="adbca-104">В этой статье описывается, как можно использовать размещенные в памяти аналитики и аналитики реального времени для получения доступа, изучения и анализа эффективности магазина на основе данных Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="adbca-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Dynamics 365 Retail data.</span></span>

<span data-ttu-id="adbca-105">В рамках использования Retail пользователи могут проанализировать эффективность работы магазина в реальном времени на разных уровнях иерархии организации за выбранный период, открыв готовый отчет **Сводка по каналам** в любом из следующих расположений.</span><span class="sxs-lookup"><span data-stu-id="adbca-105">As part of Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="adbca-106">Рабочая область **Руководство розничного магазина** &gt; **Розничная торговля** &gt; **Каналы** &gt; **Управление розничными магазинами** &gt; **Отчеты** &gt; **Сводный отчет по каналу**</span><span class="sxs-lookup"><span data-stu-id="adbca-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="adbca-107">Рабочая область **Финансовая информация розничного магазина** &gt; **Розничная торговля** &gt; **Каналы** &gt; **Финансовая информация розничного магазина** &gt; **Отчеты** &gt; **Сводный отчет по каналу**</span><span class="sxs-lookup"><span data-stu-id="adbca-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="adbca-108">Раздел **Запросы и отчеты** &gt; **Розничная торговля** &gt; **Запросы и отчеты** &gt; **Отчеты о продажах** &gt; **Сводный отчет по каналу**</span><span class="sxs-lookup"><span data-stu-id="adbca-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="adbca-109">Этот отчет содержит снимок следующих сводок об эффективности работы магазина.</span><span class="sxs-lookup"><span data-stu-id="adbca-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="adbca-110">Сводка по валовым продажам</span><span class="sxs-lookup"><span data-stu-id="adbca-110">Gross sales summary</span></span>
- <span data-ttu-id="adbca-111">Сводка по типу платежного средства</span><span class="sxs-lookup"><span data-stu-id="adbca-111">Tender type summary</span></span>
- <span data-ttu-id="adbca-112">Сводка по налогам</span><span class="sxs-lookup"><span data-stu-id="adbca-112">Tax summary</span></span>
- <span data-ttu-id="adbca-113">Сводка переопределения цены</span><span class="sxs-lookup"><span data-stu-id="adbca-113">Price overrides summary</span></span>
- <span data-ttu-id="adbca-114">Сводка по скидке</span><span class="sxs-lookup"><span data-stu-id="adbca-114">Discounts summary</span></span>
