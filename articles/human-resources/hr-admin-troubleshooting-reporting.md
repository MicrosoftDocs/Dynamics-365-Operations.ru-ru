---
title: Варианты отчетности
description: В этой статье описан порядок решения проблемы, когда клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 64a03724d81745373d028d76a8cc64aab66efdbb
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053307"
---
# <a name="reporting-options"></a><span data-ttu-id="f44bd-103">Варианты отчетности</span><span class="sxs-lookup"><span data-stu-id="f44bd-103">Reporting options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f44bd-104">**Сведения среды**</span><span class="sxs-lookup"><span data-stu-id="f44bd-104">**Environment details**</span></span>

<span data-ttu-id="f44bd-105">Эта проблема относится ко всем средам.</span><span class="sxs-lookup"><span data-stu-id="f44bd-105">This issue applies to all environments.</span></span>

<span data-ttu-id="f44bd-106">**Симптом**</span><span class="sxs-lookup"><span data-stu-id="f44bd-106">**Symptom**</span></span>

<span data-ttu-id="f44bd-107">Клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f44bd-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="f44bd-108">**Расход**</span><span class="sxs-lookup"><span data-stu-id="f44bd-108">**Issue**</span></span>

<span data-ttu-id="f44bd-109">Пользователь не может настраивать внедренные отчеты Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="f44bd-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="f44bd-110">**Решение**</span><span class="sxs-lookup"><span data-stu-id="f44bd-110">**Solution**</span></span>

- <span data-ttu-id="f44bd-111">Данные Human Resources, которые передаются в Dataverse, могут передаваться через соединитель Power Apps Dataverse в Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="f44bd-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="f44bd-112">Обратите внимание, что Dataverse содержит подмножество данных Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f44bd-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="f44bd-113">Дополнительные сведения о Power BI и панелях мониторинга см. в разделе [Создание отчетов и панелей мониторинга Power BI с помощью Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="f44bd-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="f44bd-114">Электронная отчетность (ER) доступна для некоторых отчетов в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f44bd-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="f44bd-115">Настройки, управляемые клиентом, можно сделать через параметры конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="f44bd-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="f44bd-116">Данные можно экспортировать в Microsoft Excel или Microsoft Word с использованием различных информационных объектов, предоставляемых Human Resources с помощью интеграции с Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="f44bd-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="f44bd-117">**Долгосрочное решение**</span><span class="sxs-lookup"><span data-stu-id="f44bd-117">**Long-term solution**</span></span>

<span data-ttu-id="f44bd-118">Будут доступны дополнительные параметры Power BI, и дополнительные данные и объекты будут входить в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f44bd-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]