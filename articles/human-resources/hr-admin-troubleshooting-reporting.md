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
ms.openlocfilehash: 9ee6dba5e37877f1c0b3b9df8306b3194ea2f3e4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010407"
---
# <a name="reporting-options"></a><span data-ttu-id="406e7-103">Варианты отчетности</span><span class="sxs-lookup"><span data-stu-id="406e7-103">Reporting options</span></span>

<span data-ttu-id="406e7-104">**Сведения среды**</span><span class="sxs-lookup"><span data-stu-id="406e7-104">**Environment details**</span></span>

<span data-ttu-id="406e7-105">Эта проблема относится ко всем средам.</span><span class="sxs-lookup"><span data-stu-id="406e7-105">This issue applies to all environments.</span></span>

<span data-ttu-id="406e7-106">**Симптом**</span><span class="sxs-lookup"><span data-stu-id="406e7-106">**Symptom**</span></span>

<span data-ttu-id="406e7-107">Клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="406e7-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="406e7-108">**Расход**</span><span class="sxs-lookup"><span data-stu-id="406e7-108">**Issue**</span></span>

<span data-ttu-id="406e7-109">Пользователь не может настраивать внедренные отчеты Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="406e7-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="406e7-110">**Решение**</span><span class="sxs-lookup"><span data-stu-id="406e7-110">**Solution**</span></span>

- <span data-ttu-id="406e7-111">Данные Human Resources, которые передаются в Common Data Service, могут передаваться через соединитель Power Apps Common Data Service в Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="406e7-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="406e7-112">Обратите внимание, что Common Data Service содержит подмножество данных Human Resources.</span><span class="sxs-lookup"><span data-stu-id="406e7-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="406e7-113">Дополнительные сведения о Power BI и панелях мониторинга см. в разделе [Создание отчетов и панелей мониторинга Power BI с помощью Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="406e7-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="406e7-114">Электронная отчетность (ER) доступна для некоторых отчетов в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="406e7-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="406e7-115">Настройки, управляемые клиентом, можно сделать через параметры конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="406e7-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="406e7-116">Данные можно экспортировать в Microsoft Excel или Microsoft Word с использованием различных информационных объектов, предоставляемых Human Resources с помощью интеграции с Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="406e7-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="406e7-117">**Долгосрочное решение**</span><span class="sxs-lookup"><span data-stu-id="406e7-117">**Long-term solution**</span></span>

<span data-ttu-id="406e7-118">Будут доступны дополнительные параметры Power BI, и дополнительные данные и объекты будут входить в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="406e7-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
