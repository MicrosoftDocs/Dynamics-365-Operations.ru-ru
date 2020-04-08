---
title: Тип места назначения ER принтера
description: В этой теме приводятся сведения о настройке места назначения принтера для каждого компонента ПАПКА или ФАЙЛ формата электронной отчетности (ER), настроенного для создания исходящих документов в формате PDF или Microsoft Office (Excel, Word).
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 148da191ce4ea99c237895c40ec007a1aa0cd537
ms.sourcegitcommit: 0d9ca44b48fb2e33d8160faccc1e6bd932e58934
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150800"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="e0b99-103">Назначение принтера</span><span class="sxs-lookup"><span data-stu-id="e0b99-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0b99-104">Созданный документ можно отправить непосредственно на сетевой принтер для непосредственной печати.</span><span class="sxs-lookup"><span data-stu-id="e0b99-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e0b99-105">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="e0b99-105">Prerequisites</span></span>

<span data-ttu-id="e0b99-106">Перед началом необходимо установить и настроить агент маршрутизации документов, а затем зарегистрировать сетевые принтеры.</span><span class="sxs-lookup"><span data-stu-id="e0b99-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="e0b99-107">Дополнительные сведения см. в [Установка агента маршрутизации документов для включения сетевой печати](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="e0b99-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="e0b99-108">Убедитесь, что место назначения принтера доступно</span><span class="sxs-lookup"><span data-stu-id="e0b99-108">Make the Printer destination available</span></span>

<span data-ttu-id="e0b99-109">Чтобы сделать место назначения **Принтер** доступным в текущем экземпляре Microsoft Dynamics 365 Finance, перейдите в рабочую область **Управление функциями** и включите следующие функции в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="e0b99-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="e0b99-110">Преобразовать исходящие документы электронной отчетности из форматов Microsoft Office в PDF</span><span class="sxs-lookup"><span data-stu-id="e0b99-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="e0b99-111">Агент маршрутизации документов как назначение электронной отчетности для исходящих документов</span><span class="sxs-lookup"><span data-stu-id="e0b99-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="e0b99-112">[![Включение функции места назначения ER принтера в управлении функциями](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="e0b99-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="e0b99-113">Применимость</span><span class="sxs-lookup"><span data-stu-id="e0b99-113">Applicability</span></span>

<span data-ttu-id="e0b99-114">Место назначения **Принтер** может быть настроено только для тех компонентов файлов, которые используются для создания выходных данных в формате PDF для печати (слияние PDF или формат PDF) или Microsoft Office Excel/Word (файл Excel).</span><span class="sxs-lookup"><span data-stu-id="e0b99-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="e0b99-115">При создании выходных данных в формате PDF они отправляются на принтер.</span><span class="sxs-lookup"><span data-stu-id="e0b99-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="e0b99-116">Когда выходные данные создаются в формате Microsoft Office, они автоматически преобразуются в формат PDF и затем отправляются на принтер.</span><span class="sxs-lookup"><span data-stu-id="e0b99-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="e0b99-117">Ограничения</span><span class="sxs-lookup"><span data-stu-id="e0b99-117">Limitations</span></span>

<span data-ttu-id="e0b99-118">Эта функция предназначена для предварительного просмотра и подчиняется условиям использования, которые описаны в [Дополнительные условия использования предварительных версий Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274).</span><span class="sxs-lookup"><span data-stu-id="e0b99-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="e0b99-119">Место назначения **Принтер** реализовано только для развертываний в облаке.</span><span class="sxs-lookup"><span data-stu-id="e0b99-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="e0b99-120">Использование места назначения принтера</span><span class="sxs-lookup"><span data-stu-id="e0b99-120">Use the Printer destination</span></span>

1. <span data-ttu-id="e0b99-121">Установите для параметра **Включен** задано значение **Да**, чтобы отправить созданный документ на принтер.</span><span class="sxs-lookup"><span data-stu-id="e0b99-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="e0b99-122">В поле **Имя принтера** выберите нужный сетевой принтер.</span><span class="sxs-lookup"><span data-stu-id="e0b99-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="e0b99-123">Задайте для **Сохранить в архиве печати?** значение **Да** для сохранения созданных выходных данных в архиве печати, чтобы они были доступны для дальнейшей печати.</span><span class="sxs-lookup"><span data-stu-id="e0b99-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="e0b99-124">Чтобы получить доступ к архивированным выходным данным позже, перейдите **Управление организацией** \> **Запросы и отчеты** \> **Архив отчетов**.</span><span class="sxs-lookup"><span data-stu-id="e0b99-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="e0b99-125">[![Использование места назначения принтера](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="e0b99-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="e0b99-126">Параметр **Преобразовать в PDF** не должен быть включен при настройке места назначения **Принтер**.</span><span class="sxs-lookup"><span data-stu-id="e0b99-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="e0b99-127">Преобразование PDF для печати выполняется даже в том случае, если этот параметр отключен.</span><span class="sxs-lookup"><span data-stu-id="e0b99-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="e0b99-128">Чтобы использовать определенную [ориентацию страницы](electronic-reporting-destinations.md#SelectPdfPageOrientation) при печати исходящего документа в формате Excel, необходимо включить параметр **Преобразовать в PDF**.</span><span class="sxs-lookup"><span data-stu-id="e0b99-128">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="e0b99-129">При установке для параметра **Преобразовать в PDF** значения **Да**, поле **Ориентации страницы** становится доступным.</span><span class="sxs-lookup"><span data-stu-id="e0b99-129">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="e0b99-130">В поле **Ориентация страницы** можно выбрать ориентацию страницы.</span><span class="sxs-lookup"><span data-stu-id="e0b99-130">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0b99-131">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e0b99-131">Additional resources</span></span>

- [<span data-ttu-id="e0b99-132">Обзор электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="e0b99-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="e0b99-133">Места назначения электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="e0b99-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
