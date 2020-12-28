---
title: Варианты отчетности
description: В этой статье описан порядок решения проблемы, когда клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51d84df5c3c29510e2742148b8c260a2cf402639
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527725"
---
# <a name="reporting-options"></a><span data-ttu-id="de5a6-103">Варианты отчетности</span><span class="sxs-lookup"><span data-stu-id="de5a6-103">Reporting options</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="de5a6-104">**Сведения среды**</span><span class="sxs-lookup"><span data-stu-id="de5a6-104">**Environment details**</span></span>

<span data-ttu-id="de5a6-105">Эта проблема относится ко всем средам.</span><span class="sxs-lookup"><span data-stu-id="de5a6-105">This issue applies to all environments.</span></span>

<span data-ttu-id="de5a6-106">**Симптом**</span><span class="sxs-lookup"><span data-stu-id="de5a6-106">**Symptom**</span></span>

<span data-ttu-id="de5a6-107">Клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="de5a6-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="de5a6-108">**Расход**</span><span class="sxs-lookup"><span data-stu-id="de5a6-108">**Issue**</span></span>

<span data-ttu-id="de5a6-109">Пользователь не может настраивать внедренные отчеты Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="de5a6-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="de5a6-110">**Решение**</span><span class="sxs-lookup"><span data-stu-id="de5a6-110">**Solution**</span></span>

- <span data-ttu-id="de5a6-111">Данные Human Resources, которые передаются в Common Data Service, могут передаваться через соединитель Power Apps Common Data Service в Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="de5a6-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="de5a6-112">Обратите внимание, что Common Data Service содержит подмножество данных Human Resources.</span><span class="sxs-lookup"><span data-stu-id="de5a6-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="de5a6-113">Дополнительные сведения о Power BI и панелях мониторинга см. в разделе [Создание отчетов и панелей мониторинга Power BI с помощью Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="de5a6-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="de5a6-114">Электронная отчетность (ER) доступна для некоторых отчетов в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="de5a6-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="de5a6-115">Настройки, управляемые клиентом, можно сделать через параметры конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="de5a6-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="de5a6-116">Данные можно экспортировать в Microsoft Excel или Microsoft Word с использованием различных информационных объектов, предоставляемых Human Resources с помощью интеграции с Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="de5a6-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="de5a6-117">**Долгосрочное решение**</span><span class="sxs-lookup"><span data-stu-id="de5a6-117">**Long-term solution**</span></span>

<span data-ttu-id="de5a6-118">Будут доступны дополнительные параметры Power BI, и дополнительные данные и объекты будут входить в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="de5a6-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
