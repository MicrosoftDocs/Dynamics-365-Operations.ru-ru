---
title: Системные требования и политика обновления Talent
description: В этом разделе перечислены требования к Dynamics 365 for Talent. Также рассматривается политика обновления.
author: andreabichsel
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 2389f00b22ec3b5284eeffb2c015533b7a3d13e0
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "856309"
---
# <a name="talent-system-requirements-and-update-policy"></a><span data-ttu-id="2425a-104">Системные требования и политика обновления Talent</span><span class="sxs-lookup"><span data-stu-id="2425a-104">Talent system requirements and update policy</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2425a-105">В этом разделе перечислены требования к Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="2425a-105">This topic lists requirements for Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="2425a-106">Также рассматривается политика обновления.</span><span class="sxs-lookup"><span data-stu-id="2425a-106">The update policy is outlined, as well.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="2425a-107">Поддерживаемые веб-браузеры</span><span class="sxs-lookup"><span data-stu-id="2425a-107">Supported web browsers</span></span>

<span data-ttu-id="2425a-108">Веб-приложение Microsoft Dynamics 365 for Talent может выполняться в любом веб-браузере, который работает в указанных операционных системах:</span><span class="sxs-lookup"><span data-stu-id="2425a-108">The Microsoft Dynamics 365 for Talent web application can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="2425a-109">Microsoft Edge (последняя публично доступная версия) в Windows 10</span><span class="sxs-lookup"><span data-stu-id="2425a-109">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="2425a-110">Internet Explorer 11 в Windows 10, Windows 8.1 или Windows 7</span><span class="sxs-lookup"><span data-stu-id="2425a-110">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="2425a-111">Google Chrome (последняя публично доступная версия)</span><span class="sxs-lookup"><span data-stu-id="2425a-111">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="2425a-112">Apple Safari (последняя публично доступная версия)</span><span class="sxs-lookup"><span data-stu-id="2425a-112">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="2425a-113">Чтобы найти последний выпуск для каждого веб-браузера, перейдите на веб-сайт производителя программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="2425a-113">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="2425a-114">Для захвата изображений, создаваемых в регистраторе задач, и включения их в документы Microsoft Word должно быть установлено расширение Chrome.</span><span class="sxs-lookup"><span data-stu-id="2425a-114">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="2425a-115">Редактор workflow-процессов запускается в виде приложения ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="2425a-115">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="2425a-116">Только Microsoft Edge и Internet Explorer (на поддерживаемой версии Microsoft Windows) поддерживают приложения ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="2425a-116">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="2425a-117">Для приложения ClickOnce редактора workflow-процессов требуется 64-разрядная совместимая операционная система.</span><span class="sxs-lookup"><span data-stu-id="2425a-117">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="2425a-118">Для предварительного просмотра PDF-файлов рекомендуется использовать современные браузеры, такие как Microsoft Edge (последней общедоступной версии) в Windows 10 или Google Chrome (последней общедоступной версии) в Windows 10, Windows 8.1, Windows 8, Windows 7 или на планшете Google Nexus 10.</span><span class="sxs-lookup"><span data-stu-id="2425a-118">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="2425a-119">Требования к сети</span><span class="sxs-lookup"><span data-stu-id="2425a-119">Network requirements</span></span>
> * <span data-ttu-id="2425a-120">Приложение Dynamics 365 for Talent предназначено для сетей с задержкой не более 250-300 мс.</span><span class="sxs-lookup"><span data-stu-id="2425a-120">Dynamics 365 for Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="2425a-121">Это задержка от клиента браузера до центра данных Microsoft Azure, на котором размещено приложение Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="2425a-121">This is the latency from a browser client to the Microsoft Azure data center that hosts Dynamics 365 for Talent.</span></span> <span data-ttu-id="2425a-122">Рекомендуется проверить задержку в сети на сайте [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span><span class="sxs-lookup"><span data-stu-id="2425a-122">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="2425a-123">Требования к пропускной способности для Dynamics 365 for Talent зависят от конкретного сценария реализации.</span><span class="sxs-lookup"><span data-stu-id="2425a-123">Bandwidth requirements for Dynamics 365 for Talent depend on your scenario.</span></span> <span data-ttu-id="2425a-124">В большинстве типичных сценариев требуется пропускная способность более 50 Кбайт в секунду (КБ/с).</span><span class="sxs-lookup"><span data-stu-id="2425a-124">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="2425a-125">Не вычисляйте требования к пропускной способности из местоположения клиента путем умножения числа пользователей на минимальные требования к пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="2425a-125">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="2425a-126">Параллельное использование для конкретного местоположения очень сложно рассчитать.</span><span class="sxs-lookup"><span data-stu-id="2425a-126">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="2425a-127">Клиентам, которых беспокоят требования к пропускной способности, следует использовать пробную версию Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="2425a-127">For customers who are concerned about bandwidth requirements, use a trial version of Dynamics 365 for Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="2425a-128">Поддерживаемые приложения Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="2425a-128">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="2425a-129">Для запуска надстроек Microsoft Excel и Word должен быть установлен Microsoft Office 2016 для Windows или Mac.</span><span class="sxs-lookup"><span data-stu-id="2425a-129">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="2425a-130">Дополнительные сведения о требованиях к версии см. в разделе [Устранение неполадок при интеграции Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "Устранение неполадок при интеграции Office").</span><span class="sxs-lookup"><span data-stu-id="2425a-130">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="2425a-131">Для просмотра документов, созданных с помощью функции экспорта в Excel или экспорта в Word должен быть установлен пакет Microsoft Office 2007 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="2425a-131">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="update-policy"></a><span data-ttu-id="2425a-132">Политика обновления</span><span class="sxs-lookup"><span data-stu-id="2425a-132">Update policy</span></span>

<span data-ttu-id="2425a-133">Microsoft Dynamics 365 for Talent обслуживается как облачное предложение.</span><span class="sxs-lookup"><span data-stu-id="2425a-133">Microsoft Dynamics 365 for Talent is serviced as a cloud offering.</span></span> <span data-ttu-id="2425a-134">Dynamics 365 for Talent постоянно обновляется, и обновления автоматически применяются корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2425a-134">Updates to Dynamics 365 for Talent are continuous and applied automatically by Microsoft.</span></span>

<span data-ttu-id="2425a-135">Обновления выпускаются регулярно и применяются ко всем средам.</span><span class="sxs-lookup"><span data-stu-id="2425a-135">Updates are released on a regular cadence, updates will be made to all environments.</span></span>  <span data-ttu-id="2425a-136">Dynamics 365 for Talent поддерживается в соответствии с [политикой жизненного цикла поддержки Майкрософт](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Политика жизненного цикла поддержки Майкрософт"), которая обеспечивает единообразную и предсказуемую поддержку продукта.</span><span class="sxs-lookup"><span data-stu-id="2425a-136">Dynamics 365 for Talent is supported according to the [Microsoft Support Lifecycle policy](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), which provides consistent and predictable guidelines for product support availability.</span></span>
