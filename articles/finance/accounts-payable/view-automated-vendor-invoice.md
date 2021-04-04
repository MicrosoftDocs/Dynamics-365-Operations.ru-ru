---
title: Просмотр результатов автоматизации обработки накладных поставщиков (предварительная версия)
description: В этой теме объясняется, как просмотреть статус накладных поставщика, которые находятся в процессе автоматической отправки в рабочий процесс.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3b87af4c64f8021a1b23cca5d8f38ac21c8efbd4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248104"
---
# <a name="view-vendor-invoice-automation-results"></a><span data-ttu-id="6dee7-103">Просмотр результатов автоматизации обработки накладных поставщиков</span><span class="sxs-lookup"><span data-stu-id="6dee7-103">View vendor invoice automation results</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6dee7-104">В этой теме объясняется, как просмотреть статус накладных поставщика, которые находятся в процессе автоматической отправки в рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="6dee7-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="6dee7-105">Подробные сведения о журнале автоматизации хранятся для каждой импортированной накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="6dee7-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="6dee7-106">В зависимости от того, какие бизнес-процессы были автоматизированы, страница **Ожидающие накладные поставщиков** показывает значения параметров **Статус автоматического сопоставления приходов** и **Статус автоматической отправки в рабочий процесс**.</span><span class="sxs-lookup"><span data-stu-id="6dee7-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="6dee7-107">Можно просмотреть сведения и создать план для фокусировки на накладных, не прошедших автоматический этап.</span><span class="sxs-lookup"><span data-stu-id="6dee7-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="6dee7-108">Затем, после исправления проблемы, можно возобновить выполнение автоматического процесса для импортированной накладной.</span><span class="sxs-lookup"><span data-stu-id="6dee7-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="6dee7-109">Прежде чем можно будет редактировать накладную, которая была отправлена, следует приостановить автоматическую обработку.</span><span class="sxs-lookup"><span data-stu-id="6dee7-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="6dee7-110">Если накладная в ходе автоматического отправки в рабочий процесс должна быть приостановлена, установите в поле **Включить в автоматическую обработку** значение **Нет** на странице **Накладные поставщиков**.</span><span class="sxs-lookup"><span data-stu-id="6dee7-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="6dee7-111">Автоматизация затем будет выполняться только после того, как для параметра **Включить в автоматическую обработку** будет задано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="6dee7-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="6dee7-112">Накладную можно приостановить, чтобы для нее не выполнялась дальнейшая автоматизация, если она еще не находится в системе рабочего процесса и не используется автоматизированным процессом.</span><span class="sxs-lookup"><span data-stu-id="6dee7-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="6dee7-113">Если импортированная накладная подлежит отправке в рабочий процесс, можно просмотреть ее значение **Статус автоматизации** на странице **Накладные поставщиков**.</span><span class="sxs-lookup"><span data-stu-id="6dee7-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="6dee7-114">Отслеживаются следующие статусы:</span><span class="sxs-lookup"><span data-stu-id="6dee7-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="6dee7-115">**Включено** — автоматические процессы, определенные на странице **Параметры модуля расчетов с поставщиками**, выполняются правильно, но еще не были завершены.</span><span class="sxs-lookup"><span data-stu-id="6dee7-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="6dee7-116">**Приостановлено** — автоматические процессы, определенные на странице **Параметры модуля расчетов с поставщиками**, запущены, но по крайней мере один шаг в процессе закончился сбоем.</span><span class="sxs-lookup"><span data-stu-id="6dee7-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="6dee7-117">Статус **Приостановлено** также применяется, если в поле **Включить в автоматическую обработку** указано значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="6dee7-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="6dee7-118">Сбои можно просмотреть, выбрав **Просмотреть последние результаты**.</span><span class="sxs-lookup"><span data-stu-id="6dee7-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="6dee7-119">**В рабочем процессе** — импортированная накладная была отправлена в систему рабочих процессов с помощью автоматической отправки в рабочий процесс или вручную.</span><span class="sxs-lookup"><span data-stu-id="6dee7-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="6dee7-120">**Рабочий процесс завершен** — рабочий процесс был завершен для импортированной накладной.</span><span class="sxs-lookup"><span data-stu-id="6dee7-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]