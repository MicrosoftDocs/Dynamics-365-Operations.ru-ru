---
title: "Параметры отчетности в Talent"
description: "В этом разделе описан порядок решения проблемы, когда клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 for Talent."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.contentlocale: ru-ru
ms.lasthandoff: 12/04/2018

---

# <a name="reporting-options-in-talent"></a><span data-ttu-id="e3b08-103">Параметры отчетности в Talent</span><span class="sxs-lookup"><span data-stu-id="e3b08-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e3b08-104">**Сведения среды**</span><span class="sxs-lookup"><span data-stu-id="e3b08-104">**Environment details**</span></span>

<span data-ttu-id="e3b08-105">Эта проблема относится ко всем средам.</span><span class="sxs-lookup"><span data-stu-id="e3b08-105">This issue applies to all environments.</span></span>

<span data-ttu-id="e3b08-106">**Симптом**</span><span class="sxs-lookup"><span data-stu-id="e3b08-106">**Symptom**</span></span>

<span data-ttu-id="e3b08-107">Клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="e3b08-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="e3b08-108">**Расход**</span><span class="sxs-lookup"><span data-stu-id="e3b08-108">**Issue**</span></span>

<span data-ttu-id="e3b08-109">Пользователь не может настраивать внедренные отчеты Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="e3b08-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="e3b08-110">**Решение**</span><span class="sxs-lookup"><span data-stu-id="e3b08-110">**Solution**</span></span>

- <span data-ttu-id="e3b08-111">Данные Core HR, которые передаются в Common Data Service для приложений, могут передаваться через соединитель PowerApps CDS в Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="e3b08-111">The Core HR data that flows to Common Data Service for Apps can be reported on via the PowerApps CDS connector to Power BI Desktop.</span></span> <span data-ttu-id="e3b08-112">Обратите внимание, что Common Data Service для приложений содержит подмножество данных Core HR.</span><span class="sxs-lookup"><span data-stu-id="e3b08-112">Note that Common Data Service for Apps contains a subset of Core HR data.</span></span> <span data-ttu-id="e3b08-113">Дополнительные сведения о Power BI и панелях мониторинга см. в разделе [Создание отчетов и панелей мониторинга Power BI с помощью Common Data Service PowerApps](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="e3b08-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="e3b08-114">Электронная отчетность (ER) доступна для некоторых отчетов в Talent.</span><span class="sxs-lookup"><span data-stu-id="e3b08-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="e3b08-115">Настройки, управляемые клиентом, можно сделать через параметры конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="e3b08-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="e3b08-116">Данные можно экспортировать в Microsoft Excel или Microsoft Word с использованием различных информационных объектов, предоставляемых Talent с помощью интеграции с Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="e3b08-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="e3b08-117">**Долгосрочное решение**</span><span class="sxs-lookup"><span data-stu-id="e3b08-117">**Long-term solution**</span></span>

<span data-ttu-id="e3b08-118">Будут доступны дополнительные параметры Power BI, и дополнительные данные и объекты будут входить в Common Data Service для приложений.</span><span class="sxs-lookup"><span data-stu-id="e3b08-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service for Apps.</span></span>

