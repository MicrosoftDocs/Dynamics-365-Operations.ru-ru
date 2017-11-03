---
title: "Требования к системе для облачных развертываний"
description: "В этой теме перечислены требования к системе для текущей версии Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, для облачных сред."
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 83637b4b2ccc01950e68569b3b8bee1a7cd69855
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="8a900-103">Требования к системе для облачных развертываний</span><span class="sxs-lookup"><span data-stu-id="8a900-103">System requirements for cloud deployments</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8a900-104">В этой теме перечислены требования к системе для текущей версии Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, для облачных сред.</span><span class="sxs-lookup"><span data-stu-id="8a900-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for cloud deployments.</span></span> <span data-ttu-id="8a900-105">Перед установкой Finance and Operations при необходимости убедитесь, что система, с которой вы работаете, соответствует минимальным требованиям к сети, оборудованию и программному обеспечению или превышает их.</span><span class="sxs-lookup"><span data-stu-id="8a900-105">Before you install Finance and Operations, when this step is appropriate, verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="8a900-106">Поддерживаемые веб-браузеры</span><span class="sxs-lookup"><span data-stu-id="8a900-106">Supported web browsers</span></span>
<span data-ttu-id="8a900-107">Веб-приложение может выполняться в любом веб-браузере, который работает в указанных операционных системах:</span><span class="sxs-lookup"><span data-stu-id="8a900-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="8a900-108">Microsoft Edge (последняя публично доступная версия) в Windows 10</span><span class="sxs-lookup"><span data-stu-id="8a900-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="8a900-109">Internet Explorer 11 в Windows 10, Windows 8.1 или Windows 7</span><span class="sxs-lookup"><span data-stu-id="8a900-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="8a900-110">Google Chrome (последняя публично доступная версия) в Windows 10, Windows 8.1, Windows 8, Windows 7 или на планшете Google Nexus 10</span><span class="sxs-lookup"><span data-stu-id="8a900-110">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
-   <span data-ttu-id="8a900-111">Apple Safari (последняя публично доступная версия) в Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) или 10.12 (Sierra) или Apple iPad</span><span class="sxs-lookup"><span data-stu-id="8a900-111">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) or 10.12 (Sierra), or Apple iPad</span></span>

<span data-ttu-id="8a900-112">Чтобы найти последний выпуск для каждого веб-браузера, перейдите на веб-сайт производителя программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="8a900-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> -   <span data-ttu-id="8a900-113">Чтобы регистратор задач мог захватывать снимки экрана и включать их в формируемые документы Microsoft Word, необходимо установить предварительную версию расширения Chrome.</span><span class="sxs-lookup"><span data-stu-id="8a900-113">You must install a pre-release Chrome extension to enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> -   <span data-ttu-id="8a900-114">Редактор workflow-процессов запускается в виде приложения ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="8a900-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="8a900-115">Только Microsoft Edge и Internet Explorer (на поддерживаемой версии Microsoft Windows) поддерживают приложение ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="8a900-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="8a900-116">Для приложения ClickOnce редактора workflow-процессов требуется 64-разрядная совместимая операционная система.</span><span class="sxs-lookup"><span data-stu-id="8a900-116">The Workflow Editor ClickOnce application requires a 64-bit-compatible operating system.</span></span>
> -   <span data-ttu-id="8a900-117">Конструктор отчетов для финансовой отчетности запускается в виде приложения ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="8a900-117">The Report Designer for Financial reporting is started as a ClickOnce application.</span></span> <span data-ttu-id="8a900-118">Для него требуется 64-разрядная совместимая операционная система.</span><span class="sxs-lookup"><span data-stu-id="8a900-118">It requires a 64-bit-compatible operating system.</span></span> <span data-ttu-id="8a900-119">При использовании браузера Chrome необходимо установить расширение ClickOnce, чтобы можно было загрузить клиент Конструктора отчетов.</span><span class="sxs-lookup"><span data-stu-id="8a900-119">If you’re using Chrome, you must install a ClickOnce extension to download the Report Designer client.</span></span> <span data-ttu-id="8a900-120">При работе с Chrome в режиме инкогнито убедитесь, что расширение ClickOnce также включено для работы в режиме инкогнито.</span><span class="sxs-lookup"><span data-stu-id="8a900-120">If you use Chrome in Incognito mode, make sure that the ClickOnce extension is also enabled for Incognito mode.</span></span>
> -   <span data-ttu-id="8a900-121">Для предварительного просмотра PDF-файлов рекомендуется использовать такие браузеры, как Microsoft Edge (последней общедоступной версии) в Windows 10 или Google Chrome (последней общедоступной версии) в Windows 10, Windows 8.1, Windows 8, Windows 7 или на планшете Google Nexus 10.</span><span class="sxs-lookup"><span data-stu-id="8a900-121">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-retail-cloud-pos"></a><span data-ttu-id="8a900-122">Поддерживаемые веб-браузеры для Retail Cloud POS</span><span class="sxs-lookup"><span data-stu-id="8a900-122">Supported web browsers for Retail Cloud POS</span></span>

<span data-ttu-id="8a900-123">Retail Cloud POS может выполняться в любом веб-браузере, который работает в указанных операционных системах:</span><span class="sxs-lookup"><span data-stu-id="8a900-123">Retail Cloud POS can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="8a900-124">Microsoft Edge (последняя публично доступная версия) в Windows 10</span><span class="sxs-lookup"><span data-stu-id="8a900-124">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="8a900-125">Internet Explorer 11 в Windows 10, Windows 8.1 или Windows 7</span><span class="sxs-lookup"><span data-stu-id="8a900-125">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="8a900-126">Chrome (последняя общедоступная версия) на Windows 10, Windows 8.1 или Windows 7</span><span class="sxs-lookup"><span data-stu-id="8a900-126">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="8a900-127">Требования к сети</span><span class="sxs-lookup"><span data-stu-id="8a900-127">Network requirements</span></span>
-   <span data-ttu-id="8a900-128">Система Finance and Operations предназначена для сетей с задержкой не более 250-300 мс.</span><span class="sxs-lookup"><span data-stu-id="8a900-128">Finance and Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="8a900-129">Это задержка от клиента браузера до центра данных Microsoft Azure, на котором размещена система Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8a900-129">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Finance and Operations.</span></span> <span data-ttu-id="8a900-130">Рекомендуется проверить задержку в сети на сайте <http://www.azurespeed.com>.</span><span class="sxs-lookup"><span data-stu-id="8a900-130">We recommend that you test network latency at <http://www.azurespeed.com>.</span></span>
-   <span data-ttu-id="8a900-131">Требования к пропускной способности для Finance and Operations зависят от конкретного сценария.</span><span class="sxs-lookup"><span data-stu-id="8a900-131">Bandwidth requirements for Finance and Operations depend on your scenario.</span></span> <span data-ttu-id="8a900-132">В большинстве типичных сценариев требуется пропускная способность более 50 Кбайт в секунду (КБ/с).</span><span class="sxs-lookup"><span data-stu-id="8a900-132">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="8a900-133">Однако для сценариев с высокими требованиями к полезной нагрузке, например при использовании рабочих областей или широкой индивидуальной настройке, рекомендуется большая пропускная способность.</span><span class="sxs-lookup"><span data-stu-id="8a900-133">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="8a900-134">В целом система Finance and Operations оптимизирована для работы в Интернете.</span><span class="sxs-lookup"><span data-stu-id="8a900-134">In general, Finance and Operations is optimized for the internet.</span></span> <span data-ttu-id="8a900-135">Число пересылок данных туда и обратно с клиента браузера до центра данных Azure очень мало, и все полезные данные сжимаются.</span><span class="sxs-lookup"><span data-stu-id="8a900-135">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span> 

> [!WARNING]
> <span data-ttu-id="8a900-136">Не вычисляйте требования к пропускной способности из местоположения клиента путем умножения числа пользователей на минимальные требования к пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="8a900-136">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="8a900-137">Параллельное использование для конкретного местоположения очень сложно рассчитать.</span><span class="sxs-lookup"><span data-stu-id="8a900-137">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="8a900-138">Клиентам, которых беспокоят требования к пропускной способности, следует воспользоваться предварительной версией Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8a900-138">Customers who are concerned about bandwidth requirements should use a preview version of Finance and Operations.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="8a900-139">Требования к .NET Framework</span><span class="sxs-lookup"><span data-stu-id="8a900-139">.NET Framework requirements</span></span>
<span data-ttu-id="8a900-140">Finance and Operations требует наличия Microsoft .NET Framework версии 4.6.2 для всех приложений ClickOnce, таких как агент маршрутизации документов.</span><span class="sxs-lookup"><span data-stu-id="8a900-140">Finance and Operations requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="8a900-141">Инструкции по установке см. в разделе [Установка .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="8a900-141">For installation instructions, see [Installing the .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="8a900-142">Поддерживаемые приложения Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="8a900-142">Supported Microsoft Office applications</span></span>
<span data-ttu-id="8a900-143">Следующие приложения Microsoft Office поддерживаются в облачных и локальных развертываниях Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="8a900-143">The following Microsoft Office applications are supported in cloud and on-premises deployments of Finance and Operations:</span></span>

-   <span data-ttu-id="8a900-144">Для запуска надстроек Microsoft Excel и Word должен быть установлен Microsoft Office 2016 для Windows или Mac.</span><span class="sxs-lookup"><span data-stu-id="8a900-144">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="8a900-145">Дополнительные сведения о требованиях к версиям см. в разделе [Устранение неполадок при интеграции Office](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="8a900-145">For more information about version requirements, see [Office integration troubleshooting](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
-   <span data-ttu-id="8a900-146">Для просмотра документов, созданных с помощью функции экспорта в Excel или экспорта в Word должен быть установлен пакет Microsoft Office 2007 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="8a900-146">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="retail-modern-pos-requirements"></a><span data-ttu-id="8a900-147">Требования для Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="8a900-147">Retail Modern POS requirements</span></span>

> [!NOTE]
> <span data-ttu-id="8a900-148">Если в Retail Modern POS будет использоваться автономная база данных, компьютер должен удовлетворять всем требованиям к системе для Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8a900-148">If Retail Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server.</span></span> <span data-ttu-id="8a900-149">Автономная база данных Retail Modern POS будет работать в Microsoft SQL Server 2012 с пакетом обновления 3 или более поздним, Microsoft SQL Server 2014 с пакетом обновления 2 или более поздним, а также в Microsoft SQL Server 2016.</span><span class="sxs-lookup"><span data-stu-id="8a900-149">A Retail Modern POS offline database will work on Microsoft SQL Server 2012 with Service Pack 3 or later, Microsoft SQL Server 2014 with Service Pack 2 or later, and Microsoft SQL Server 2016.</span></span> <span data-ttu-id="8a900-150">Рекомендуем всегда использовать последнюю доступную версию и устанавливать все последние пакеты обновления.</span><span class="sxs-lookup"><span data-stu-id="8a900-150">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="8a900-151">Поддерживаемые операционные системы</span><span class="sxs-lookup"><span data-stu-id="8a900-151">Supported operating systems</span></span>

-   <span data-ttu-id="8a900-152">Retail Modern POS — это 32-разрядное приложение, но оно будет работать как в архитектуре x86, так и в архитектуре x64.</span><span class="sxs-lookup"><span data-stu-id="8a900-152">Retail Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="8a900-153">Retail Modern POS поддерживается только в выпусках Windows 10 Pro, Корпоративная и Корпоративная с долгосрочным обслуживанием (LTSB).</span><span class="sxs-lookup"><span data-stu-id="8a900-153">Retail Modern POS is supported only on Windows 10 Pro, Enterprise, and Enterprise Long Term Servicing Branch (LTSB) editions.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="8a900-154">Минимальные требования к системе</span><span class="sxs-lookup"><span data-stu-id="8a900-154">Minimum system requirements</span></span>

-   <span data-ttu-id="8a900-155">Минимальное поддерживаемое разрешение: 1280 × 1024.</span><span class="sxs-lookup"><span data-stu-id="8a900-155">The minimum supported resolution is 1,280 × 1,024.</span></span>
-   <span data-ttu-id="8a900-156">Компьютер, на котором будет выполняться Retail Modern POS, должен соответствовать следующим требованиям:</span><span class="sxs-lookup"><span data-stu-id="8a900-156">The computer that Retail Modern POS runs on must meet these requirements:</span></span>

    -   <span data-ttu-id="8a900-157">Он должен иметь, как минимум, двухъядерный процессор, работающий на частоте не менее 2 ГГц.</span><span class="sxs-lookup"><span data-stu-id="8a900-157">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    -   <span data-ttu-id="8a900-158">Он должен иметь не менее 3 ГБ ОЗУ.</span><span class="sxs-lookup"><span data-stu-id="8a900-158">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span>
    -   <span data-ttu-id="8a900-159">Он должен быть подключен к Интернету.</span><span class="sxs-lookup"><span data-stu-id="8a900-159">It must have internet access.</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="8a900-160">Требования для станции оборудования Retail</span><span class="sxs-lookup"><span data-stu-id="8a900-160">Retail hardware station requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="8a900-161">Поддерживаемые операционные системы</span><span class="sxs-lookup"><span data-stu-id="8a900-161">Supported operating systems</span></span>

-   <span data-ttu-id="8a900-162">Станция оборудования Retail — это 32-разрядное приложение, но оно будет работать как в архитектуре x86, так и в архитектуре x64.</span><span class="sxs-lookup"><span data-stu-id="8a900-162">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="8a900-163">Станция оборудования Retail поддерживается в следующих операционных системах:</span><span class="sxs-lookup"><span data-stu-id="8a900-163">Retail hardware station is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="8a900-164">Выпуски Windows 7 Профессиональная, Корпоративная и Максимальная</span><span class="sxs-lookup"><span data-stu-id="8a900-164">Windows 7 Professional, Enterprise, and Ultimate editions</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="8a900-165">Windows 7 поддерживается, только если Internet Explorer 11 вручную установлен в системе.</span><span class="sxs-lookup"><span data-stu-id="8a900-165">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    -   <span data-ttu-id="8a900-166">Windows 8.1 с обновлением 1, выпуски Профессиональная, Корпоративная и Встроенная</span><span class="sxs-lookup"><span data-stu-id="8a900-166">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="8a900-167">Выпуски Windows 10 Pro, Корпоративная и Корпоративная LTSB</span><span class="sxs-lookup"><span data-stu-id="8a900-167">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="8a900-168">Минимальные требования к системе</span><span class="sxs-lookup"><span data-stu-id="8a900-168">Minimum system requirements</span></span>

<span data-ttu-id="8a900-169">Компьютер должен удовлетворять всем требованиям к системе для установки и использования следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="8a900-169">The computer must meet all system requirements for installing and using the following items:</span></span>

-   <span data-ttu-id="8a900-170">Службы IIS (Internet Information Services)</span><span class="sxs-lookup"><span data-stu-id="8a900-170">Internet Information Services (IIS)</span></span>
-   <span data-ttu-id="8a900-171">Оборудование независимых производителей</span><span class="sxs-lookup"><span data-stu-id="8a900-171">Third-party hardware</span></span>

## <a name="retail-store-scale-unit-requirements"></a><span data-ttu-id="8a900-172">Требования к модулю весов для розничного магазина Retail Store Scale Unit</span><span class="sxs-lookup"><span data-stu-id="8a900-172">Retail Store Scale Unit requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="8a900-173">Поддерживаемые операционные системы</span><span class="sxs-lookup"><span data-stu-id="8a900-173">Supported operating systems</span></span>

-   <span data-ttu-id="8a900-174">Retail Store Scale Unit — это 32-разрядное приложение, но оно будет работать как в архитектуре x86, так и в архитектуре x64.</span><span class="sxs-lookup"><span data-stu-id="8a900-174">Retail Store Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="8a900-175">Retail Store Scale Unit поддерживается в следующих операционных системах:</span><span class="sxs-lookup"><span data-stu-id="8a900-175">Retail Store Scale Unit is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="8a900-176">Выпуски Windows 7 Профессиональная, Корпоративная и Максимальная</span><span class="sxs-lookup"><span data-stu-id="8a900-176">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="8a900-177">Windows 8.1 с обновлением 1, выпуски Профессиональная, Корпоративная и Встроенная</span><span class="sxs-lookup"><span data-stu-id="8a900-177">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="8a900-178">Выпуски Windows 10 Pro, Корпоративная и Корпоративная LTSB</span><span class="sxs-lookup"><span data-stu-id="8a900-178">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="8a900-179">Минимальные требования к системе</span><span class="sxs-lookup"><span data-stu-id="8a900-179">Minimum system requirements</span></span>

-   <span data-ttu-id="8a900-180">4 ГБ ОЗУ</span><span class="sxs-lookup"><span data-stu-id="8a900-180">4 GB of RAM</span></span>
-   <span data-ttu-id="8a900-181">Пиковая скорость работы процессора 1,6 ГГц на ядро (Не менее двух ядер.)</span><span class="sxs-lookup"><span data-stu-id="8a900-181">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="8a900-182">По крайней мере 10 ГБ свободного места (Для канала базы данных может потребоваться большой объем пространства.)</span><span class="sxs-lookup"><span data-stu-id="8a900-182">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="8a900-183">Рекомендуемые требования к системе</span><span class="sxs-lookup"><span data-stu-id="8a900-183">Recommended system requirements</span></span>

-   <span data-ttu-id="8a900-184">6 ГБ ОЗУ</span><span class="sxs-lookup"><span data-stu-id="8a900-184">6 GB of RAM</span></span>
-   <span data-ttu-id="8a900-185">Процессор i7 (или аналогичный) с пиковой скоростью работы 2,4 ГГц на ядро (Рекомендуется четыре ядра.)</span><span class="sxs-lookup"><span data-stu-id="8a900-185">2.4 GHz i7 (or equivalent) peak CPU speed per core (Four cores are recommended.)</span></span>
-   <span data-ttu-id="8a900-186">По крайней мере 10 ГБ свободного места (Для канала базы данных может потребоваться большой объем пространства.)</span><span class="sxs-lookup"><span data-stu-id="8a900-186">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="connector-requirements"></a><span data-ttu-id="8a900-187">Требования соединителя</span><span class="sxs-lookup"><span data-stu-id="8a900-187">Connector requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="8a900-188">Поддерживаемые операционные системы</span><span class="sxs-lookup"><span data-stu-id="8a900-188">Supported operating systems</span></span>

-   <span data-ttu-id="8a900-189">Для соединителя Microsoft Dynamics AX предусмотрено два отдельных установщика: один для службы Async Server Connector и один для службы Real-time service for Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="8a900-189">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Dynamics AX 2012 R3.</span></span>
-   <span data-ttu-id="8a900-190">Оба компонента представляют собой 32-разрядные приложения, но будут работать как в архитектуре x86, так и в архитектуре x64.</span><span class="sxs-lookup"><span data-stu-id="8a900-190">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="8a900-191">Оба компонента поддерживаются в следующих операционных системах:</span><span class="sxs-lookup"><span data-stu-id="8a900-191">Both components are supported on the following operating systems:</span></span>

    -   <span data-ttu-id="8a900-192">Выпуски Windows 7 Профессиональная, Корпоративная и Максимальная</span><span class="sxs-lookup"><span data-stu-id="8a900-192">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="8a900-193">Windows 8.1 с обновлением 1, выпуски Профессиональная, Корпоративная и Встроенная</span><span class="sxs-lookup"><span data-stu-id="8a900-193">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="8a900-194">Выпуски Windows 10 Pro, Корпоративная и Корпоративная LTSB</span><span class="sxs-lookup"><span data-stu-id="8a900-194">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>
    -   <span data-ttu-id="8a900-195">Microsoft Windows Server 2012 R2 и Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8a900-195">Microsoft Windows Server 2012 R2 and Microsoft Windows Server 2016</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="8a900-196">Минимальные требования к системе</span><span class="sxs-lookup"><span data-stu-id="8a900-196">Minimum system requirements</span></span>
-   <span data-ttu-id="8a900-197">2 ГБ ОЗУ (рекомендуется 4 ГБ ОЗУ)</span><span class="sxs-lookup"><span data-stu-id="8a900-197">2 GB of RAM (4 GB of RAM are recommended.)</span></span>
-   <span data-ttu-id="8a900-198">Пиковая скорость работы процессора 1,6 ГГц на ядро (Не менее двух ядер.)</span><span class="sxs-lookup"><span data-stu-id="8a900-198">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="8a900-199">По крайней мере 10 ГБ свободного места (Для канала базы данных может потребоваться большой объем пространства.)</span><span class="sxs-lookup"><span data-stu-id="8a900-199">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="8a900-200">Требования для разработки на локальных виртуальных машинах</span><span class="sxs-lookup"><span data-stu-id="8a900-200">Requirements for development on local VMs</span></span>
<span data-ttu-id="8a900-201">Сведения о требованиях к разработке на локальных виртуальных машинах (VM) в разделе [Локальные виртуальные машины](../../dev-itpro/dev-tools/access-instances.md).</span><span class="sxs-lookup"><span data-stu-id="8a900-201">For information about the requirements for development on local virtual machines (VMs), see [VM running on-premises](../../dev-itpro/dev-tools/access-instances.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="8a900-202">См. также</span><span class="sxs-lookup"><span data-stu-id="8a900-202">See also</span></span>

[<span data-ttu-id="8a900-203">Получение ознакомительной версии Dynamics 365 for Finance and Operations, Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="8a900-203">Get an evaluation copy of Dynamics 365 for Finance and Operations, Enterprise edition</span></span>](../../dev-itpro/dev-tools/get-evaluation-copy.md)

