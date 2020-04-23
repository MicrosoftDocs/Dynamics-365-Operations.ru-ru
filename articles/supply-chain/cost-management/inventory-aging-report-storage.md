---
title: Отчет о распределении запасов по срокам
description: В этой теме описываются функции, позволяющие выполнить отчет о распределении запасов по срокам и сделать выходные данные доступными в виде формы и диаграммы.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 790c8fe3a52bce652227f1cef97eff6496476100
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201632"
---
# <a name="inventory-aging-report"></a><span data-ttu-id="19f16-103">Отчет о распределении запасов по срокам</span><span class="sxs-lookup"><span data-stu-id="19f16-103">Inventory aging report</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="19f16-104">В Microsoft Dynamics 365 Supply Chain Management можно выполнить отчет **Распределение запасов по срокам** и сделать выходные данные доступными в виде формы и диаграммы.</span><span class="sxs-lookup"><span data-stu-id="19f16-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="19f16-105">В форме столбцы и агрегированные балансы динамически корректируются в зависимости от настроенного макета.</span><span class="sxs-lookup"><span data-stu-id="19f16-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="19f16-106">Диаграмма дает визуальное представление, поддерживающий фильтрацию, и позволяет детально просмотреть подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="19f16-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="19f16-107">Кроме того, информационный объект с именем **Отчет о распределении запасов по срокам** позволяет экспортировать результаты отчета **Распределение запасов по срокам** в формат, такой как Microsoft Excel-файл или PDF-файл.</span><span class="sxs-lookup"><span data-stu-id="19f16-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="19f16-108">Этот метод выполнения отчета **Распределение запасов по срокам** полезен в тех случаях, когда выходные данные содержат много строк.</span><span class="sxs-lookup"><span data-stu-id="19f16-108">This method of running an **Inventory aging** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="19f16-109">Например, на выходе будет содержаться множество строк, если имеется 50 000 номенклатур и 300 магазинов, созданных как склады, и вы запрашиваете распределение запасов по срокам для номенклатуры, месту и складу.</span><span class="sxs-lookup"><span data-stu-id="19f16-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="run-an-inventory-aging-report"></a><span data-ttu-id="19f16-110">Выполнение отчета о распределении запасов по срокам</span><span class="sxs-lookup"><span data-stu-id="19f16-110">Run an Inventory aging report</span></span>

1. <span data-ttu-id="19f16-111">Перейдите **Управление затратами \> Запросы и отчеты \> Хранение отчета о распределении запасов по срокам**.</span><span class="sxs-lookup"><span data-stu-id="19f16-111">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="19f16-112">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="19f16-112">Select **New**.</span></span>
1. <span data-ttu-id="19f16-113">В поле **Код процесса — Имя** введите уникальное имя для отчета.</span><span class="sxs-lookup"><span data-stu-id="19f16-113">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="19f16-114">Выберите отчет **Идентификация — код** и отфильтруйте его, как требуется.</span><span class="sxs-lookup"><span data-stu-id="19f16-114">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="19f16-115">Выполнение отчета всегда выполняется в пакетном задании.</span><span class="sxs-lookup"><span data-stu-id="19f16-115">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="19f16-116">После завершения пакетного задания результаты отображаются на странице **Хранение отчета о распределении запасов по срокам**.</span><span class="sxs-lookup"><span data-stu-id="19f16-116">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="19f16-117">Для просмотра выходных данных в виде формы с традиционной табличной структурой выберите **Показать подробности**.</span><span class="sxs-lookup"><span data-stu-id="19f16-117">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="19f16-118">Для просмотра выходных данных в виде агрегированной диаграммы выберите **Показать диаграмму**.</span><span class="sxs-lookup"><span data-stu-id="19f16-118">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="19f16-119">В форме не будут включены промежуточные итоги, определенные в макете отчета.</span><span class="sxs-lookup"><span data-stu-id="19f16-119">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="19f16-120">Информационный объект **Отчет о распределении запасов по срокам** позволяет экспортировать выходные данные отчета **Распределение запасов по срокам**, применив фильтр к полю **Код процесса — имя** в любой формат, поддерживаемый системой управления данными.</span><span class="sxs-lookup"><span data-stu-id="19f16-120">The **Inventory aging report** data entity lets you export the output of an **Inventory aging** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
