---
title: Финансовая отчетность
description: Финансовая отчетность позволяет профессионалам в сфере финансов и бизнеса создавать, вести, развертывать и просматривать финансовые отчеты. Она выходит за пределы традиционных ограничений отчетности для эффективной разработки различных типов отчетов.
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4e9fe8f78121428770e6516159f5eceb6976c4c9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181803"
---
# <a name="financial-reporting"></a><span data-ttu-id="82d4e-104">Финансовая отчетность</span><span class="sxs-lookup"><span data-stu-id="82d4e-104">Financial reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82d4e-105">Финансовая отчетность для приложения позволяет профессионалам в сфере финансов и бизнеса создавать, вести, развертывать и просматривать финансовые отчеты.</span><span class="sxs-lookup"><span data-stu-id="82d4e-105">Financial reporting for the application allows financial and business professionals to create, maintain, deploy, and view financial statements.</span></span> <span data-ttu-id="82d4e-106">Она выходит за пределы традиционных ограничений отчетности для эффективной разработки различных типов отчетов.</span><span class="sxs-lookup"><span data-stu-id="82d4e-106">It moves beyond traditional reporting constraints to help you efficiently design various types of reports.</span></span>

<span data-ttu-id="82d4e-107">Финансовая отчетность включает поддержку аналитик.</span><span class="sxs-lookup"><span data-stu-id="82d4e-107">Financial reporting includes dimension support.</span></span> <span data-ttu-id="82d4e-108">Таким образом, сегменты или аналитики счетов доступны незамедлительно.</span><span class="sxs-lookup"><span data-stu-id="82d4e-108">Therefore, account segments or dimensions are immediately available.</span></span> <span data-ttu-id="82d4e-109">Не требуются дополнительные средства или шаги настройки.</span><span class="sxs-lookup"><span data-stu-id="82d4e-109">No additional tools or configuration steps are required.</span></span>

## <a name="financial-reporting-setup"></a><span data-ttu-id="82d4e-110">Настройка финансовой отчетности</span><span class="sxs-lookup"><span data-stu-id="82d4e-110">Financial reporting setup</span></span>
<span data-ttu-id="82d4e-111">Страница **Настройка финансовой отчетности** содержит список всех финансовых аналитик в системе.</span><span class="sxs-lookup"><span data-stu-id="82d4e-111">The **Financial reporting setup** page has a list of all financial dimensions in the system.</span></span> <span data-ttu-id="82d4e-112">**Главная книга** \> **Настройка главной книги** \> **Настройка финансовой отчетности**.</span><span class="sxs-lookup"><span data-stu-id="82d4e-112">**General ledger** \> **Ledger setup** \> **Financial reporting setup**.</span></span>

<span data-ttu-id="82d4e-113">Страница **Настройка финансовой отчетности** состоит из двух разделов, определяющих данные, по которым составляется отчет в Financial reporting:</span><span class="sxs-lookup"><span data-stu-id="82d4e-113">The **Financial reporting setup** page has two sections that determine the data you report on in Financial reporting:</span></span>

- <span data-ttu-id="82d4e-114">**Вкладка "Аналитики"** — так как разные компании используют различные аналитики и планы счетов, невозможно определить порядок, в котором пользователю требуется просматривать все финансовые аналитики в отчетах.</span><span class="sxs-lookup"><span data-stu-id="82d4e-114">**Dimensions tab** - Because different companies use different dimensions and account structures, there is no way to determine the order in which users want to view all financial dimensions on reports.</span></span> <span data-ttu-id="82d4e-115">Эта страница позволяет задать порядок, в который финансовые аналитики должны отображаться при построении и просмотре отчетов в решении Financial reporting.</span><span class="sxs-lookup"><span data-stu-id="82d4e-115">This page allows you set the order in which you want financial dimensions to appear when you build and view a report in Financial reporting.</span></span>
- <span data-ttu-id="82d4e-116">На **вкладке "Атрибуты"** можно указать, требуется ли возможность использовать поля **Поставщики** и **Клиенты** как атрибуты для фильтрации и разработки отчетов.</span><span class="sxs-lookup"><span data-stu-id="82d4e-116">**Attributes tab** is where you can select whether you want the ability to use **Vendors** and **Customers** as attributes for filtering and report design.</span></span> <span data-ttu-id="82d4e-117">Отчетность по поставщикам и клиентам будет иметь смысл только в том случае, если вы не вводите нескольких поставщиков или клиентов в один ваучер при разноске проводок.</span><span class="sxs-lookup"><span data-stu-id="82d4e-117">Reporting on Vendor and Customer will only be valuable if you do not enter multiple vendors or customers in a single voucher when posting transactions.</span></span> <span data-ttu-id="82d4e-118">При выборе поставщика и/или клиента увеличивается время, требуемое для интеграции.</span><span class="sxs-lookup"><span data-stu-id="82d4e-118">Choosing Vendor and/or Customer will add additional time to the integration.</span></span>

## <a name="financial-reporting-components"></a><span data-ttu-id="82d4e-119">Компоненты финансовой отчетности</span><span class="sxs-lookup"><span data-stu-id="82d4e-119">Financial reporting components</span></span>
<span data-ttu-id="82d4e-120">Следующие компоненты финансовой отчетности упрощают создание, просмотр и планирование отчетов.</span><span class="sxs-lookup"><span data-stu-id="82d4e-120">The following components of financial reporting make it easy to create, view, and schedule reports.</span></span>

| <span data-ttu-id="82d4e-121">Компонент</span><span class="sxs-lookup"><span data-stu-id="82d4e-121">Component</span></span>        | <span data-ttu-id="82d4e-122">Функции</span><span class="sxs-lookup"><span data-stu-id="82d4e-122">Functions</span></span> | <span data-ttu-id="82d4e-123">Дополнительная информация</span><span class="sxs-lookup"><span data-stu-id="82d4e-123">Additional information</span></span> |
|------------------|-----------|------------------------|
| <span data-ttu-id="82d4e-124">Конструктор отчетов</span><span class="sxs-lookup"><span data-stu-id="82d4e-124">Report Designer</span></span>  | <span data-ttu-id="82d4e-125">Создавайте строительные блоки отчета, которые можно сочетать для определения и создания отчета.</span><span class="sxs-lookup"><span data-stu-id="82d4e-125">Create report building blocks that can be combined to define and generate a report.</span></span> <span data-ttu-id="82d4e-126">Мастер отчетов помогает менее опытным пользователям в процессе конструирования.</span><span class="sxs-lookup"><span data-stu-id="82d4e-126">The report wizard guides less experienced users through the design process.</span></span> <span data-ttu-id="82d4e-127">Опытные пользователи могут создать новые строительные блоки отчета или изменить существующие строительные блоки для того, чтобы они отвечали их требованиям.</span><span class="sxs-lookup"><span data-stu-id="82d4e-127">Advanced users can create new report building blocks or modify existing building blocks to meet their requirements.</span></span> | |
| <span data-ttu-id="82d4e-128">Графики отчетов</span><span class="sxs-lookup"><span data-stu-id="82d4e-128">Report schedules</span></span> | <span data-ttu-id="82d4e-129">Запланируйте один отчет или группу отчетов таким образом, чтобы они создавались на регулярной основе.</span><span class="sxs-lookup"><span data-stu-id="82d4e-129">Schedule a single report or a group of reports so that it is generated on a regular basis.</span></span> | [<span data-ttu-id="82d4e-130">Создание финансового отчета</span><span class="sxs-lookup"><span data-stu-id="82d4e-130">Generate a financial report</span></span>](generate-financial-report.md) |

## <a name="features"></a><span data-ttu-id="82d4e-131">Функциональность</span><span class="sxs-lookup"><span data-stu-id="82d4e-131">Features</span></span>
<table>
<thead>
<tr>
<th><span data-ttu-id="82d4e-132">Функция</span><span class="sxs-lookup"><span data-stu-id="82d4e-132">Feature</span></span></th>
<th><span data-ttu-id="82d4e-133">описание</span><span class="sxs-lookup"><span data-stu-id="82d4e-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="82d4e-134">Гибкость конструирования отчетов</span><span class="sxs-lookup"><span data-stu-id="82d4e-134">Report design flexibility</span></span></td>
<td><span data-ttu-id="82d4e-135">В конструкторе отчетов доступны следующие параметры отчетности при создании отчета:</span><span class="sxs-lookup"><span data-stu-id="82d4e-135">Report Designer provides the following reporting options when you design a report:</span></span>
<ul>
<li><span data-ttu-id="82d4e-136">Сохраните комбинации аналитик и используйте аналитики повторно для нескольких отчетов.</span><span class="sxs-lookup"><span data-stu-id="82d4e-136">Save dimension combinations, and reuse the dimensions for multiple reports.</span></span></li>
<li><span data-ttu-id="82d4e-137">Контролируйте, как описания аналитик форматируются и отображаются.</span><span class="sxs-lookup"><span data-stu-id="82d4e-137">Control how dimension descriptions are formatted and displayed.</span></span></li>
<li><span data-ttu-id="82d4e-138">Обнаружение счетов или измерений, пропущенных в шаблонах отчетов.</span><span class="sxs-lookup"><span data-stu-id="82d4e-138">Identify accounts or dimensions that have been omitted from report building blocks.</span></span></li>
<li><span data-ttu-id="82d4e-139">Форматирование заголовков для скользящих прогнозов.</span><span class="sxs-lookup"><span data-stu-id="82d4e-139">Format headers for rolling forecasts.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="82d4e-140">Совместная работа над финансовой отчетностью</span><span class="sxs-lookup"><span data-stu-id="82d4e-140">Financial report collaboration</span></span></td>
<td><span data-ttu-id="82d4e-141">Следующие характеристики помогают вам управлять созданием и распределением отчетов:</span><span class="sxs-lookup"><span data-stu-id="82d4e-141">The following features help you manage the generation and distribution of reports:</span></span>
<ul>
<li><span data-ttu-id="82d4e-142">Планирование автоматического создания отчетов на ежедневной, еженедельной, ежемесячной или ежегодной основе.</span><span class="sxs-lookup"><span data-stu-id="82d4e-142">Schedule reports so that they are automatically generated on a daily, weekly, monthly, or annual basis.</span></span></li>
<li><span data-ttu-id="82d4e-143">Экспорт в доступный только для чтения формат XPS, который обеспечивает лучшую безопасность документа за счет цифровых подписей.</span><span class="sxs-lookup"><span data-stu-id="82d4e-143">Export to the read-only XPS format, which provides better document security through digital signatures.</span></span></li>
<li><span data-ttu-id="82d4e-144">Экспорт в лист Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="82d4e-144">Export to a Microsoft Excel worksheet.</span></span></li>
<li><span data-ttu-id="82d4e-145">Чтобы поделиться отчетами, вы можете создать сообщения электронной почты, которые содержат ссылки на отчеты.</span><span class="sxs-lookup"><span data-stu-id="82d4e-145">To share reports, you can create email messages that contain links to the reports.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="82d4e-146">Интерактивный просмотр отчета</span><span class="sxs-lookup"><span data-stu-id="82d4e-146">Interactive report viewing</span></span></td>
<td><span data-ttu-id="82d4e-147">Интерактивные функции позволяют выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="82d4e-147">Interactive features let you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="82d4e-148">Изменение даты отчета для просматриваемого отчета.</span><span class="sxs-lookup"><span data-stu-id="82d4e-148">Change the report date for the report that you're viewing.</span></span></li>
<li><span data-ttu-id="82d4e-149">Изменение валюты просматриваемого отчета.</span><span class="sxs-lookup"><span data-stu-id="82d4e-149">Change the currency of the report that you're viewing.</span></span></li>
<li><span data-ttu-id="82d4e-150">Просмотр отчеты в представление сводки или в подробном представлении.</span><span class="sxs-lookup"><span data-stu-id="82d4e-150">View the report in either a summary view or a detailed view.</span></span></li>
<li><span data-ttu-id="82d4e-151">Добавление фильтров аналитик для ограничения содержимого отчета конкретными аналитиками или комбинациями аналитик.</span><span class="sxs-lookup"><span data-stu-id="82d4e-151">Add dimension filters to limit the report content to a specific dimension or combination of dimensions.</span></span></li>
<li><span data-ttu-id="82d4e-152">Добавление фильтров атрибутов для ограничения содержимого отчета конкретными атрибутами или комбинациями атрибутов.</span><span class="sxs-lookup"><span data-stu-id="82d4e-152">Add attribute filters to limit the report content to a specific attribute or combination of attributes.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="82d4e-153">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="82d4e-153">Additional resources</span></span>
[<span data-ttu-id="82d4e-154">Создание финансового отчета</span><span class="sxs-lookup"><span data-stu-id="82d4e-154">Generate a financial report</span></span>](generate-financial-report.md)