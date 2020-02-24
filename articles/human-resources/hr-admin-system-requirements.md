---
title: Требования к системе
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 72379e91ace61f5e33ac6cab259b5c32902c7b3b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010284"
---
# <a name="system-requirements"></a><span data-ttu-id="63e75-102">Требования к системе</span><span class="sxs-lookup"><span data-stu-id="63e75-102">System requirements</span></span>

<span data-ttu-id="63e75-103">В этой статье описаны требования для Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="63e75-103">This article describes requirements for Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="63e75-104">Кроме того, в ней описываются страны и регионы, в которых доступно Human Resources, а также сведения о языках и локализации для данных Human Resources.</span><span class="sxs-lookup"><span data-stu-id="63e75-104">It also outlines the countries and regions where Human Resources is available, and information about languages and localization for Human Resources data.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="63e75-105">Поддерживаемые веб-браузеры</span><span class="sxs-lookup"><span data-stu-id="63e75-105">Supported web browsers</span></span>

<span data-ttu-id="63e75-106">Human Resources может выполняться в любом веб-браузере, который работает в указанных операционных системах:</span><span class="sxs-lookup"><span data-stu-id="63e75-106">Human Resources can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="63e75-107">Microsoft Edge (последняя публично доступная версия) в Windows 10</span><span class="sxs-lookup"><span data-stu-id="63e75-107">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="63e75-108">Internet Explorer 11 в Windows 10, Windows 8.1 или Windows 7</span><span class="sxs-lookup"><span data-stu-id="63e75-108">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="63e75-109">Google Chrome (последняя публично доступная версия)</span><span class="sxs-lookup"><span data-stu-id="63e75-109">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="63e75-110">Apple Safari (последняя публично доступная версия)</span><span class="sxs-lookup"><span data-stu-id="63e75-110">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="63e75-111">Чтобы найти последний выпуск для каждого веб-браузера, перейдите на веб-сайт производителя программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="63e75-111">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="63e75-112">Для захвата изображений, создаваемых в регистраторе задач, и включения их в документы Microsoft Word должно быть установлено расширение Chrome.</span><span class="sxs-lookup"><span data-stu-id="63e75-112">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="63e75-113">Редактор workflow-процессов запускается в виде приложения ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="63e75-113">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="63e75-114">Только Microsoft Edge и Internet Explorer (на поддерживаемой версии Microsoft Windows) поддерживают приложения ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="63e75-114">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="63e75-115">Для приложения ClickOnce редактора workflow-процессов требуется 64-разрядная совместимая операционная система.</span><span class="sxs-lookup"><span data-stu-id="63e75-115">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="63e75-116">Для предварительного просмотра PDF-файлов рекомендуется использовать современные браузеры, такие как Microsoft Edge (последней общедоступной версии) в Windows 10 или Google Chrome (последней общедоступной версии) в Windows 10, Windows 8.1, Windows 8, Windows 7 или на планшете Google Nexus 10.</span><span class="sxs-lookup"><span data-stu-id="63e75-116">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="63e75-117">Требования к сети</span><span class="sxs-lookup"><span data-stu-id="63e75-117">Network requirements</span></span>
> * <span data-ttu-id="63e75-118">Human Resources предназначено для сетей с задержкой не более 250-300 мс.</span><span class="sxs-lookup"><span data-stu-id="63e75-118">Human Resources is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="63e75-119">Это задержка от клиента браузера до центра данных Microsoft Azure, на котором размещено Human Resources.</span><span class="sxs-lookup"><span data-stu-id="63e75-119">This is the latency from a browser client to the Microsoft Azure data center that hosts Human Resources.</span></span> <span data-ttu-id="63e75-120">Рекомендуется проверить задержку в сети на сайте [www.azurespeed.com](https://www.azurespeed.com "Проверка задержки для Azure").</span><span class="sxs-lookup"><span data-stu-id="63e75-120">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="63e75-121">Требования к пропускной способности для Human Resources зависят от конкретного сценария реализации.</span><span class="sxs-lookup"><span data-stu-id="63e75-121">Bandwidth requirements for Human Resources depend on your scenario.</span></span> <span data-ttu-id="63e75-122">В большинстве типичных сценариев требуется пропускная способность более 50 Кбайт в секунду (КБ/с).</span><span class="sxs-lookup"><span data-stu-id="63e75-122">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="63e75-123">Не вычисляйте требования к пропускной способности из местоположения клиента путем умножения числа пользователей на минимальные требования к пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="63e75-123">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="63e75-124">Параллельное использование для конкретного местоположения очень сложно рассчитать.</span><span class="sxs-lookup"><span data-stu-id="63e75-124">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="63e75-125">Клиентам, которых беспокоят требования к пропускной способности, следует использовать пробную версию Human Resources.</span><span class="sxs-lookup"><span data-stu-id="63e75-125">For customers who are concerned about bandwidth requirements, use a trial version of Human Resources.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="63e75-126">Поддерживаемые приложения Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="63e75-126">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="63e75-127">Для запуска надстроек Microsoft Excel и Word должен быть установлен Microsoft Office 2016 для Windows или Mac.</span><span class="sxs-lookup"><span data-stu-id="63e75-127">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="63e75-128">Дополнительные сведения о требованиях к версии см. в разделе [Устранение неполадок при интеграции Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "Устранение неполадок интеграции с Office").</span><span class="sxs-lookup"><span data-stu-id="63e75-128">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="63e75-129">Для просмотра документов, созданных с помощью функции экспорта в Excel или экспорта в Word должен быть установлен пакет Microsoft Office 2007 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="63e75-129">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="63e75-130">Региональная доступность, языки и локализация</span><span class="sxs-lookup"><span data-stu-id="63e75-130">Regional availability, languages, and localization</span></span>

<span data-ttu-id="63e75-131">Можно загрузить PDF-файл для стран, регионов и языков, которые поддерживаются в Human Resources, из [международной доступности Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span><span class="sxs-lookup"><span data-stu-id="63e75-131">You can download a PDF file of the countries, regions, and languages Human Resources supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="63e75-132">Хотя интерфейса пользователя локализован на другие языки, все пользовательские данные хранятся на том языке, на котором они были введены.</span><span class="sxs-lookup"><span data-stu-id="63e75-132">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="63e75-133">Можно создавать сообщения и шаблоны на других языках, но на данный момент такие данные, как сведения о планировании, доступны только на английском языке.</span><span class="sxs-lookup"><span data-stu-id="63e75-133">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="63e75-134">Если вы являетесь разработчиком, заинтересованным в создании настроек, связанных со страной или регионом, или в создании решения для страны или региона, которые в настоящее время не поддерживаются корпорацией Майкрософт, см. раздел [Глобализация](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span><span class="sxs-lookup"><span data-stu-id="63e75-134">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>
