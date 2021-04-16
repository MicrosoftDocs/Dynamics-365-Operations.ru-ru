---
title: Рабочая области выставления накладных при совместной работе с поставщиками
description: В этом разделе описан порядок просмотра накладных поставщика и отправки накладных из рабочей области совместной работы с поставщиками.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 73f16b00f2af884387e0b135f3b220179eecad86
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822451"
---
# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="03eee-103">Рабочая области выставления накладных при совместной работе с поставщиками</span><span class="sxs-lookup"><span data-stu-id="03eee-103">Vendor collaboration invoicing workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03eee-104">В этом разделе описан порядок просмотра накладных поставщика и отправки накладных из рабочей области совместной работы с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="03eee-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="03eee-105">Рабочая область **Выставление накладных при совместной работе с поставщиками** можно использовать для просмотра данных по накладным поставщика и для представления накладных в системе с использованием возможностей рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="03eee-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to the system using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="03eee-106">Рабочая область выставления накладных по совместной работе с поставщиками</span><span class="sxs-lookup"><span data-stu-id="03eee-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="03eee-107">Плитки сводки</span><span class="sxs-lookup"><span data-stu-id="03eee-107">Summary tiles</span></span>

<span data-ttu-id="03eee-108">Плитки **Сводка** обеспечивают обзор накладных для выбранного поставщика.</span><span class="sxs-lookup"><span data-stu-id="03eee-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="03eee-109">Можно просмотреть накладные по их состоянию.</span><span class="sxs-lookup"><span data-stu-id="03eee-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="03eee-110">Черновики накладных не были отправлены в workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="03eee-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="03eee-111">Отправленные, но не утвержденные накладные — это накладные, которые поставщик отправил, но они не были разнесены в приложении.</span><span class="sxs-lookup"><span data-stu-id="03eee-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in the application.</span></span>
-   <span data-ttu-id="03eee-112">Утвержденные, но неоплаченные накладные — это накладные, которые разнесены, но еще не оплачены в полном объеме.</span><span class="sxs-lookup"><span data-stu-id="03eee-112">Approved, not paid invoices are those that have been posted, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="03eee-113">Оплаченные накладные — это накладные, полностью оплаченные в приложении.</span><span class="sxs-lookup"><span data-stu-id="03eee-113">Paid invoices are those that have been fully paid in the application.</span></span>

<span data-ttu-id="03eee-114">При нажатии на плитке открывается отфильтрованное представление страницы **Список накладных**.</span><span class="sxs-lookup"><span data-stu-id="03eee-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="03eee-115">Списки в виде таблицы</span><span class="sxs-lookup"><span data-stu-id="03eee-115">Tabular lists</span></span>

<span data-ttu-id="03eee-116">В разделе **Списки в виде таблицы** статус выставления накладных разделяется аналогично разделению сводных плиток: списки "Черновики" и "Отправленные, но не утвержденные".</span><span class="sxs-lookup"><span data-stu-id="03eee-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="03eee-117">В состоянии "Черновик" накладную можно передать в workflow-процесс или удалить.</span><span class="sxs-lookup"><span data-stu-id="03eee-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="03eee-118">Последний список в виде таблицы представляет собой параметр для поиска накладных.</span><span class="sxs-lookup"><span data-stu-id="03eee-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="03eee-119">Можно отфильтровать при поиске, чтобы ускорить поиск.</span><span class="sxs-lookup"><span data-stu-id="03eee-119">You can filter as you search, to allow for faster searches.</span></span>

### <a name="all-vendor-invoices-list-page"></a><span data-ttu-id="03eee-120">Страница списка "Все накладные поставщиков"</span><span class="sxs-lookup"><span data-stu-id="03eee-120">All vendor invoices list page</span></span>

<span data-ttu-id="03eee-121">Можно просмотреть все разнесенные или неразнесенные накладные поставщика на странице списка **Просмотр накладных по совместной работе с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="03eee-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="03eee-122">Вы можете использовать эту страницу списка для просмотра статуса оплаты накладных.</span><span class="sxs-lookup"><span data-stu-id="03eee-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="03eee-123">Статусы платежа включают: "Не разнесен", "Не оплачен", "Частично оплачен" и "Полностью оплачен".</span><span class="sxs-lookup"><span data-stu-id="03eee-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="03eee-124">Создание новой накладной на основе заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="03eee-124">Creating a new invoice from a purchase order</span></span>

<span data-ttu-id="03eee-125">Можно создать новую накладную поставщика, выбрав действие **Создать** в рабочей области **Выставление накладных при совместной работе с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="03eee-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="03eee-126">Номер заказа на покупку и номер накладной должны быть предоставлены поставщиком.</span><span class="sxs-lookup"><span data-stu-id="03eee-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="03eee-127">По умолчанию все строки из заказа на покупку поставщика отображаются в новой накладной.</span><span class="sxs-lookup"><span data-stu-id="03eee-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="03eee-128">Сведения о количестве и затратах можно изменить до передачи накладной поставщика в workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="03eee-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="03eee-129">Можно прикрепить файлы, примечания, изображения и URL-адреса у накладной, прежде чем отправить ее.</span><span class="sxs-lookup"><span data-stu-id="03eee-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>

<span data-ttu-id="03eee-130">Дополнительные сведения см. в разделе [Совместная работа с внешними поставщиками](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span><span class="sxs-lookup"><span data-stu-id="03eee-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]