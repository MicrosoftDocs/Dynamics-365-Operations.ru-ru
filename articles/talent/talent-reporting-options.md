---
title: Параметры отчетности в Talent
description: В этом разделе описан порядок решения проблемы, когда клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ecbeb03b535f19131ddc6649d005702876bab65c
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772973"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="59e40-103">Варианты отчетов в Talent</span><span class="sxs-lookup"><span data-stu-id="59e40-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="59e40-104">**Сведения среды**</span><span class="sxs-lookup"><span data-stu-id="59e40-104">**Environment details**</span></span>

<span data-ttu-id="59e40-105">Эта проблема относится ко всем средам.</span><span class="sxs-lookup"><span data-stu-id="59e40-105">This issue applies to all environments.</span></span>

<span data-ttu-id="59e40-106">**Симптом**</span><span class="sxs-lookup"><span data-stu-id="59e40-106">**Symptom**</span></span>

<span data-ttu-id="59e40-107">Клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="59e40-107">The customer wants to customize Microsoft Dynamics 365 Talent reports or create new reports.</span></span>

<span data-ttu-id="59e40-108">**Расход**</span><span class="sxs-lookup"><span data-stu-id="59e40-108">**Issue**</span></span>

<span data-ttu-id="59e40-109">Пользователь не может настраивать внедренные отчеты Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="59e40-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="59e40-110">**Решение**</span><span class="sxs-lookup"><span data-stu-id="59e40-110">**Solution**</span></span>

- <span data-ttu-id="59e40-111">Данные Core HR, которые передаются в Common Data Service, могут передаваться через соединитель Power Apps Common Data Service в Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="59e40-111">The Core HR data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="59e40-112">Обратите внимание, что Common Data Service содержит подмножество данных Core HR.</span><span class="sxs-lookup"><span data-stu-id="59e40-112">Note that Common Data Service contains a subset of Core HR data.</span></span> <span data-ttu-id="59e40-113">Дополнительные сведения о Power BI и панелях мониторинга см. в разделе [Создание отчетов и панелей мониторинга Power BI с помощью Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="59e40-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="59e40-114">Электронная отчетность (ER) доступна для некоторых отчетов в Talent.</span><span class="sxs-lookup"><span data-stu-id="59e40-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="59e40-115">Настройки, управляемые клиентом, можно сделать через параметры конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="59e40-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="59e40-116">Данные можно экспортировать в Microsoft Excel или Microsoft Word с использованием различных информационных объектов, предоставляемых Talent с помощью интеграции с Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="59e40-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="59e40-117">**Долгосрочное решение**</span><span class="sxs-lookup"><span data-stu-id="59e40-117">**Long-term solution**</span></span>

<span data-ttu-id="59e40-118">Будут доступны дополнительные параметры Power BI, и дополнительные данные и объекты будут входить в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="59e40-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
