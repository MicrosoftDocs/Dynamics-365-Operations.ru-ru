---
title: Требования к системе
description: В этой статье описаны требования для Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f86cd60466661c87d762f2e2f0765b92351ee2b8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053595"
---
# <a name="system-requirements"></a><span data-ttu-id="f7853-103">Требования к системе</span><span class="sxs-lookup"><span data-stu-id="f7853-103">System requirements</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f7853-104">В этой статье описаны требования для Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f7853-104">This article describes requirements for Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="f7853-105">Кроме того, в ней описываются страны и регионы, в которых доступно Human Resources, а также сведения о языках и локализации для данных Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f7853-105">It also outlines the countries and regions where Human Resources is available, and information about languages and localization for Human Resources data.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="f7853-106">Поддерживаемые веб-браузеры</span><span class="sxs-lookup"><span data-stu-id="f7853-106">Supported web browsers</span></span>

<span data-ttu-id="f7853-107">Human Resources может выполняться в любом веб-браузере, который работает в указанных операционных системах:</span><span class="sxs-lookup"><span data-stu-id="f7853-107">Human Resources can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="f7853-108">Microsoft Edge (последняя публично доступная версия) в Windows 10</span><span class="sxs-lookup"><span data-stu-id="f7853-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="f7853-109">Internet Explorer 11 в Windows 10, Windows 8.1 или Windows 7</span><span class="sxs-lookup"><span data-stu-id="f7853-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="f7853-110">Google Chrome (последняя публично доступная версия)</span><span class="sxs-lookup"><span data-stu-id="f7853-110">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="f7853-111">Apple Safari (последняя публично доступная версия)</span><span class="sxs-lookup"><span data-stu-id="f7853-111">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="f7853-112">Чтобы найти последний выпуск для каждого веб-браузера, перейдите на веб-сайт производителя программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="f7853-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="f7853-113">Для захвата изображений, создаваемых в регистраторе задач, и включения их в документы Microsoft Word должно быть установлено расширение Chrome.</span><span class="sxs-lookup"><span data-stu-id="f7853-113">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="f7853-114">Редактор workflow-процессов запускается в виде приложения ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="f7853-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="f7853-115">Только Microsoft Edge и Internet Explorer (на поддерживаемой версии Microsoft Windows) поддерживают приложения ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="f7853-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="f7853-116">Для приложения ClickOnce редактора workflow-процессов требуется 64-разрядная совместимая операционная система.</span><span class="sxs-lookup"><span data-stu-id="f7853-116">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="f7853-117">Для предварительного просмотра PDF-файлов рекомендуется использовать современные браузеры, такие как Microsoft Edge (последней общедоступной версии) в Windows 10 или Google Chrome (последней общедоступной версии) в Windows 10, Windows 8.1, Windows 8, Windows 7 или на планшете Google Nexus 10.</span><span class="sxs-lookup"><span data-stu-id="f7853-117">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="f7853-118">Требования к сети</span><span class="sxs-lookup"><span data-stu-id="f7853-118">Network requirements</span></span>
> * <span data-ttu-id="f7853-119">Human Resources предназначено для сетей с задержкой не более 250-300 мс.</span><span class="sxs-lookup"><span data-stu-id="f7853-119">Human Resources is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="f7853-120">Это задержка от клиента браузера до центра данных Microsoft Azure, на котором размещено Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f7853-120">This is the latency from a browser client to the Microsoft Azure data center that hosts Human Resources.</span></span> <span data-ttu-id="f7853-121">Рекомендуется проверить задержку в сети на сайте [www.azurespeed.com](https://www.azurespeed.com "Проверка задержки для Azure").</span><span class="sxs-lookup"><span data-stu-id="f7853-121">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="f7853-122">Требования к пропускной способности для Human Resources зависят от конкретного сценария реализации.</span><span class="sxs-lookup"><span data-stu-id="f7853-122">Bandwidth requirements for Human Resources depend on your scenario.</span></span> <span data-ttu-id="f7853-123">В большинстве типичных сценариев требуется пропускная способность более 50 Кбайт в секунду (КБ/с).</span><span class="sxs-lookup"><span data-stu-id="f7853-123">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="f7853-124">Не вычисляйте требования к пропускной способности из местоположения клиента путем умножения числа пользователей на минимальные требования к пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="f7853-124">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="f7853-125">Параллельное использование для конкретного местоположения очень сложно рассчитать.</span><span class="sxs-lookup"><span data-stu-id="f7853-125">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="f7853-126">Клиентам, которых беспокоят требования к пропускной способности, следует использовать пробную версию Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f7853-126">For customers who are concerned about bandwidth requirements, use a trial version of Human Resources.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="f7853-127">Поддерживаемые приложения Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="f7853-127">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="f7853-128">Для запуска надстроек Microsoft Excel и Word должен быть установлен Microsoft Office 2016 для Windows или Mac.</span><span class="sxs-lookup"><span data-stu-id="f7853-128">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="f7853-129">Дополнительные сведения о требованиях к версии см. в разделе [Устранение неполадок при интеграции Office](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Устранение неполадок интеграции с Office").</span><span class="sxs-lookup"><span data-stu-id="f7853-129">For more details about version requirements, see [Office integration troubleshooting](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="f7853-130">Для просмотра документов, созданных с помощью функции экспорта в Excel или экспорта в Word должен быть установлен пакет Microsoft Office 2007 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="f7853-130">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="f7853-131">Региональная доступность, языки и локализация</span><span class="sxs-lookup"><span data-stu-id="f7853-131">Regional availability, languages, and localization</span></span>

<span data-ttu-id="f7853-132">Можно загрузить PDF-файл для стран, регионов и языков, которые поддерживаются в Human Resources, из [международной доступности Microsoft Dynamics 365](/dynamics365/get-started/availability).</span><span class="sxs-lookup"><span data-stu-id="f7853-132">You can download a PDF file of the countries, regions, and languages Human Resources supports at [International availability of Microsoft Dynamics 365](/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="f7853-133">Хотя интерфейса пользователя локализован на другие языки, все пользовательские данные хранятся на том языке, на котором они были введены.</span><span class="sxs-lookup"><span data-stu-id="f7853-133">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="f7853-134">Можно создавать сообщения и шаблоны на других языках, но на данный момент такие данные, как сведения о планировании, доступны только на английском языке.</span><span class="sxs-lookup"><span data-stu-id="f7853-134">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="f7853-135">Если вы являетесь разработчиком, заинтересованным в создании настроек, связанных со страной или регионом, или в создании решения для страны или региона, которые в настоящее время не поддерживаются корпорацией Майкрософт, см. раздел [Глобализация](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span><span class="sxs-lookup"><span data-stu-id="f7853-135">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]