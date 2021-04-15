---
title: Тип места назначения ER принтера
description: В этой теме объясняется, как можно настроить место назначения принтера для каждого компонента ПАПКА или ФАЙЛ в формате электронной отчетности (ER).
author: NickSelin
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 83081f8c17a903cd447a34596df2e61ebda0cafc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753440"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="2ea63-103">Назначение принтера</span><span class="sxs-lookup"><span data-stu-id="2ea63-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ea63-104">Созданный документ можно отправить непосредственно на сетевой принтер для непосредственной печати.</span><span class="sxs-lookup"><span data-stu-id="2ea63-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2ea63-105">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="2ea63-105">Prerequisites</span></span>

<span data-ttu-id="2ea63-106">Перед началом необходимо установить и настроить агент маршрутизации документов, а затем зарегистрировать сетевые принтеры.</span><span class="sxs-lookup"><span data-stu-id="2ea63-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="2ea63-107">Дополнительные сведения см. в [Установка агента маршрутизации документов для включения сетевой печати](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="2ea63-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="2ea63-108">Убедитесь, что место назначения принтера доступно</span><span class="sxs-lookup"><span data-stu-id="2ea63-108">Make the Printer destination available</span></span>

<span data-ttu-id="2ea63-109">Чтобы сделать место назначения **Принтер** доступным в текущем экземпляре Microsoft Dynamics 365 Finance, перейдите в рабочую область **Управление функциями** и включите следующие функции в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="2ea63-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="2ea63-110">Преобразовать исходящие документы электронной отчетности из форматов Microsoft Office в PDF</span><span class="sxs-lookup"><span data-stu-id="2ea63-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="2ea63-111">Агент маршрутизации документов как назначение электронной отчетности для исходящих документов</span><span class="sxs-lookup"><span data-stu-id="2ea63-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="2ea63-112">[![Включение функции места назначения ER принтера в управлении функциями](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="2ea63-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="2ea63-113">Применимость</span><span class="sxs-lookup"><span data-stu-id="2ea63-113">Applicability</span></span>

<span data-ttu-id="2ea63-114">Место назначения **Принтер** может быть настроено только для тех компонентов файлов, которые используются для создания выходных данных в формате PDF для печати (слияние PDF или формат PDF) или Microsoft Office Excel/Word (файл Excel).</span><span class="sxs-lookup"><span data-stu-id="2ea63-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="2ea63-115">При создании выходных данных в формате PDF они отправляются на принтер.</span><span class="sxs-lookup"><span data-stu-id="2ea63-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="2ea63-116">Когда выходные данные создаются в формате Microsoft Office, они автоматически преобразуются в формат PDF и затем отправляются на принтер.</span><span class="sxs-lookup"><span data-stu-id="2ea63-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="2ea63-117">Ограничения</span><span class="sxs-lookup"><span data-stu-id="2ea63-117">Limitations</span></span>

<span data-ttu-id="2ea63-118">Место назначения **Принтер** реализовано только для развертываний в облаке.</span><span class="sxs-lookup"><span data-stu-id="2ea63-118">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="2ea63-119">Использование места назначения принтера</span><span class="sxs-lookup"><span data-stu-id="2ea63-119">Use the Printer destination</span></span>

1. <span data-ttu-id="2ea63-120">Установите для параметра **Включен** задано значение **Да**, чтобы отправить созданный документ на принтер.</span><span class="sxs-lookup"><span data-stu-id="2ea63-120">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="2ea63-121">В поле **Имя принтера** выберите нужный сетевой принтер.</span><span class="sxs-lookup"><span data-stu-id="2ea63-121">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="2ea63-122">Задайте для **Сохранить в архиве печати?** значение **Да** для сохранения созданных выходных данных в архиве печати, чтобы они были доступны для дальнейшей печати.</span><span class="sxs-lookup"><span data-stu-id="2ea63-122">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="2ea63-123">Чтобы получить доступ к архивированным выходным данным позже, перейдите **Управление организацией** \> **Запросы и отчеты** \> **Архив отчетов**.</span><span class="sxs-lookup"><span data-stu-id="2ea63-123">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="2ea63-124">[![Использование места назначения принтера](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="2ea63-124">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="2ea63-125">Параметр **Преобразовать в PDF** не должен быть включен при настройке места назначения **Принтер**.</span><span class="sxs-lookup"><span data-stu-id="2ea63-125">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="2ea63-126">Преобразование PDF для печати выполняется даже в том случае, если этот параметр отключен.</span><span class="sxs-lookup"><span data-stu-id="2ea63-126">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="2ea63-127">Чтобы использовать определенную [ориентацию страницы](electronic-reporting-destinations.md#SelectPdfPageOrientation) при печати исходящего документа в формате Excel, необходимо включить параметр **Преобразовать в PDF**.</span><span class="sxs-lookup"><span data-stu-id="2ea63-127">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="2ea63-128">При установке для параметра **Преобразовать в PDF** значения **Да**, поле **Ориентации страницы** становится доступным.</span><span class="sxs-lookup"><span data-stu-id="2ea63-128">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="2ea63-129">В поле **Ориентация страницы** можно выбрать ориентацию страницы.</span><span class="sxs-lookup"><span data-stu-id="2ea63-129">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ea63-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2ea63-130">Additional resources</span></span>

- [<span data-ttu-id="2ea63-131">Обзор электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="2ea63-131">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="2ea63-132">Места назначения электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="2ea63-132">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
