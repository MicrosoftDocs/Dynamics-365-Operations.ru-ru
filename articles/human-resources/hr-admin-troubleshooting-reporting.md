---
title: Варианты отчетности
description: В этой статье описан порядок решения проблемы, когда клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 830c8c32128a8dfc1b009557afb272e48ae3a1ff
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113972"
---
# <a name="reporting-options"></a><span data-ttu-id="dbfa4-103">Варианты отчетности</span><span class="sxs-lookup"><span data-stu-id="dbfa4-103">Reporting options</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="dbfa4-104">**Сведения среды**</span><span class="sxs-lookup"><span data-stu-id="dbfa4-104">**Environment details**</span></span>

<span data-ttu-id="dbfa4-105">Эта проблема относится ко всем средам.</span><span class="sxs-lookup"><span data-stu-id="dbfa4-105">This issue applies to all environments.</span></span>

<span data-ttu-id="dbfa4-106">**Симптом**</span><span class="sxs-lookup"><span data-stu-id="dbfa4-106">**Symptom**</span></span>

<span data-ttu-id="dbfa4-107">Клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dbfa4-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="dbfa4-108">**Расход**</span><span class="sxs-lookup"><span data-stu-id="dbfa4-108">**Issue**</span></span>

<span data-ttu-id="dbfa4-109">Пользователь не может настраивать внедренные отчеты Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="dbfa4-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="dbfa4-110">**Решение**</span><span class="sxs-lookup"><span data-stu-id="dbfa4-110">**Solution**</span></span>

- <span data-ttu-id="dbfa4-111">Данные Human Resources, которые передаются в Dataverse, могут передаваться через соединитель Power Apps Dataverse в Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="dbfa4-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="dbfa4-112">Обратите внимание, что Dataverse содержит подмножество данных Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dbfa4-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="dbfa4-113">Дополнительные сведения о Power BI и панелях мониторинга см. в разделе [Создание отчетов и панелей мониторинга Power BI с помощью Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="dbfa4-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="dbfa4-114">Электронная отчетность (ER) доступна для некоторых отчетов в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dbfa4-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="dbfa4-115">Настройки, управляемые клиентом, можно сделать через параметры конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="dbfa4-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="dbfa4-116">Данные можно экспортировать в Microsoft Excel или Microsoft Word с использованием различных информационных объектов, предоставляемых Human Resources с помощью интеграции с Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="dbfa4-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="dbfa4-117">**Долгосрочное решение**</span><span class="sxs-lookup"><span data-stu-id="dbfa4-117">**Long-term solution**</span></span>

<span data-ttu-id="dbfa4-118">Будут доступны дополнительные параметры Power BI, и дополнительные данные и объекты будут входить в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="dbfa4-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>
