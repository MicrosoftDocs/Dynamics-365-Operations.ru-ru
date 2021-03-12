---
title: Хранилище отчетов о распределении запасов по срокам
description: В этой теме описываются функции, позволяющие выполнить отчет о распределении запасов по срокам и сделать выходные данные доступными в виде формы и диаграммы.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8a292bd7a7ccbb09af1955e1e253b45e230c1009
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005435"
---
# <a name="inventory-aging-report-storage"></a><span data-ttu-id="c2975-103">Хранилище отчетов о распределении запасов по срокам</span><span class="sxs-lookup"><span data-stu-id="c2975-103">Inventory aging report storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2975-104">В Microsoft Dynamics 365 Supply Chain Management можно выполнить отчет **Хранилище отчетов о распределении запасов по срокам** и сделать выходные данные доступными в виде формы и диаграммы.</span><span class="sxs-lookup"><span data-stu-id="c2975-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging report storage** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="c2975-105">В форме столбцы и агрегированные балансы динамически корректируются в зависимости от настроенного макета.</span><span class="sxs-lookup"><span data-stu-id="c2975-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="c2975-106">Диаграмма дает визуальное представление, поддерживающий фильтрацию, и позволяет детально просмотреть подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="c2975-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="c2975-107">Кроме того, информационный объект с именем **Отчет о распределении запасов по срокам** позволяет экспортировать результаты отчета **Хранилище отчетов о распределении запасов по срокам** в формат, такой как Microsoft Excel-файл или PDF-файл.</span><span class="sxs-lookup"><span data-stu-id="c2975-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging report storage** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="c2975-108">Этот метод выполнения отчета **Хранилище отчетов о распределении запасов по срокам** полезен в тех случаях, когда выходные данные содержат много строк.</span><span class="sxs-lookup"><span data-stu-id="c2975-108">This method of running an **Inventory aging report storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="c2975-109">Например, на выходе будет содержаться множество строк, если имеется 50 000 номенклатур и 300 магазинов, созданных как склады, и вы запрашиваете распределение запасов по срокам для номенклатуры, месту и складу.</span><span class="sxs-lookup"><span data-stu-id="c2975-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="enable-the-inventory-value-storage-report-feature"></a><span data-ttu-id="c2975-110">Включение функции отчета о стоимости запасов по складам</span><span class="sxs-lookup"><span data-stu-id="c2975-110">Enable the Inventory value storage report feature</span></span>

<span data-ttu-id="c2975-111">Прежде чем использовать эту функцию, необходимо включить ее в системе.</span><span class="sxs-lookup"><span data-stu-id="c2975-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="c2975-112">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса компонента и включения их при необходимости.</span><span class="sxs-lookup"><span data-stu-id="c2975-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="c2975-113">В этой статье функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c2975-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="c2975-114">**Модуль** — Управление затратами</span><span class="sxs-lookup"><span data-stu-id="c2975-114">**Module** - Cost management</span></span>
- <span data-ttu-id="c2975-115">**Имя функции** — хранилище отчетов о распределении запасов по срокам</span><span class="sxs-lookup"><span data-stu-id="c2975-115">**Feature name** - Inventory aging report storage</span></span>

## <a name="run-an-inventory-aging-report-storage"></a><span data-ttu-id="c2975-116">Запуск хранилища отчетов о распределении запасов по срокам</span><span class="sxs-lookup"><span data-stu-id="c2975-116">Run an Inventory aging report storage</span></span>

1. <span data-ttu-id="c2975-117">Перейдите **Управление затратами \> Запросы и отчеты \> Хранение отчета о распределении запасов по срокам**.</span><span class="sxs-lookup"><span data-stu-id="c2975-117">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="c2975-118">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="c2975-118">Select **New**.</span></span>
1. <span data-ttu-id="c2975-119">В поле **Код процесса — Имя** введите уникальное имя для отчета.</span><span class="sxs-lookup"><span data-stu-id="c2975-119">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="c2975-120">Выберите отчет **Идентификация — код** и отфильтруйте его, как требуется.</span><span class="sxs-lookup"><span data-stu-id="c2975-120">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="c2975-121">Выполнение отчета всегда выполняется в пакетном задании.</span><span class="sxs-lookup"><span data-stu-id="c2975-121">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="c2975-122">После завершения пакетного задания результаты отображаются на странице **Хранение отчета о распределении запасов по срокам**.</span><span class="sxs-lookup"><span data-stu-id="c2975-122">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="c2975-123">Для просмотра выходных данных в виде формы с традиционной табличной структурой выберите **Показать подробности**.</span><span class="sxs-lookup"><span data-stu-id="c2975-123">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="c2975-124">Для просмотра выходных данных в виде агрегированной диаграммы выберите **Показать диаграмму**.</span><span class="sxs-lookup"><span data-stu-id="c2975-124">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c2975-125">В форме не будут включены промежуточные итоги, определенные в макете отчета.</span><span class="sxs-lookup"><span data-stu-id="c2975-125">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="c2975-126">Информационный объект **Отчет о распределении запасов по срокам** позволяет экспортировать выходные данные отчета **Хранилище отчетов о распределении запасов по срокам**, применив фильтр к полю **Код процесса — имя** в любой формат, поддерживаемый системой управления данными.</span><span class="sxs-lookup"><span data-stu-id="c2975-126">The **Inventory aging report** data entity lets you export the output of an **Inventory aging report storage** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
