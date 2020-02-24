---
title: Тип места назначения ER принтера
description: В этой теме приводятся сведения о настройке места назначения принтера для каждого компонента ПАПКА или ФАЙЛ формата электронной отчетности (ER), настроенного для создания исходящих документов в формате PDF или Microsoft Office (Excel, Word).
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
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
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019967"
---
# <a name="PrinterDestinationType"></a><span data-ttu-id="26ab4-103">Назначение принтера</span><span class="sxs-lookup"><span data-stu-id="26ab4-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26ab4-104">Созданный документ можно отправить непосредственно на сетевой принтер для непосредственной печати.</span><span class="sxs-lookup"><span data-stu-id="26ab4-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="26ab4-105">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="26ab4-105">Prerequisites</span></span>

<span data-ttu-id="26ab4-106">Перед началом необходимо установить и настроить агент маршрутизации документов, а затем зарегистрировать сетевые принтеры.</span><span class="sxs-lookup"><span data-stu-id="26ab4-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="26ab4-107">Дополнительные сведения см. в [Установка агента маршрутизации документов для включения сетевой печати](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="26ab4-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="26ab4-108">Убедитесь, что место назначения принтера доступно</span><span class="sxs-lookup"><span data-stu-id="26ab4-108">Make the Printer destination available</span></span>

<span data-ttu-id="26ab4-109">Чтобы сделать место назначения **Принтер** доступным в текущем экземпляре Microsoft Dynamics 365 Finance, перейдите в рабочую область **Управление функциями** и включите следующие функции в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="26ab4-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="26ab4-110">Преобразовать исходящие документы электронной отчетности из форматов Microsoft Office в PDF</span><span class="sxs-lookup"><span data-stu-id="26ab4-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="26ab4-111">Агент маршрутизации документов как назначение электронной отчетности для исходящих документов</span><span class="sxs-lookup"><span data-stu-id="26ab4-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="26ab4-112">[![Включение функции места назначения ER принтера в управлении функциями](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="26ab4-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="26ab4-113">Применимость</span><span class="sxs-lookup"><span data-stu-id="26ab4-113">Applicability</span></span>

<span data-ttu-id="26ab4-114">Место назначения **Принтер** может быть настроено только для тех компонентов файлов, которые используются для создания выходных данных в формате PDF для печати (слияние PDF или формат PDF) или Microsoft Office Excel/Word (файл Excel).</span><span class="sxs-lookup"><span data-stu-id="26ab4-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="26ab4-115">При создании выходных данных в формате PDF они отправляются на принтер.</span><span class="sxs-lookup"><span data-stu-id="26ab4-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="26ab4-116">Когда выходные данные создаются в формате Microsoft Office, они автоматически преобразуются в формат PDF и затем отправляются на принтер.</span><span class="sxs-lookup"><span data-stu-id="26ab4-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="26ab4-117">Ограничения</span><span class="sxs-lookup"><span data-stu-id="26ab4-117">Limitations</span></span>

<span data-ttu-id="26ab4-118">Эта функция предназначена для предварительного просмотра и подчиняется условиям использования, которые описаны в [Дополнительные условия использования предварительных версий Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274).</span><span class="sxs-lookup"><span data-stu-id="26ab4-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="26ab4-119">Место назначения **Принтер** реализовано только для развертываний в облаке.</span><span class="sxs-lookup"><span data-stu-id="26ab4-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="26ab4-120">Использование места назначения принтера</span><span class="sxs-lookup"><span data-stu-id="26ab4-120">Use the Printer destination</span></span>

1. <span data-ttu-id="26ab4-121">Установите для параметра **Включен** задано значение **Да**, чтобы отправить созданный документ на принтер.</span><span class="sxs-lookup"><span data-stu-id="26ab4-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="26ab4-122">В поле **Имя принтера** выберите нужный сетевой принтер.</span><span class="sxs-lookup"><span data-stu-id="26ab4-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="26ab4-123">Задайте для **Сохранить в архиве печати?** значение **Да** для сохранения созданных выходных данных в архиве печати, чтобы они были доступны для дальнейшей печати.</span><span class="sxs-lookup"><span data-stu-id="26ab4-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="26ab4-124">Чтобы получить доступ к архивированным выходным данным позже, перейдите **Управление организацией** \> **Запросы и отчеты** \> **Архив отчетов**.</span><span class="sxs-lookup"><span data-stu-id="26ab4-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="26ab4-125">[![Использование места назначения принтера](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="26ab4-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="26ab4-126">Параметр **Преобразовать в PDF** не должен быть включен при настройке места назначения **Принтер**.</span><span class="sxs-lookup"><span data-stu-id="26ab4-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="26ab4-127">Преобразование PDF для печати выполняется даже в том случае, если этот параметр отключен.</span><span class="sxs-lookup"><span data-stu-id="26ab4-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26ab4-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="26ab4-128">Additional resources</span></span>

- [<span data-ttu-id="26ab4-129">Обзор электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="26ab4-129">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="26ab4-130">Места назначения электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="26ab4-130">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
