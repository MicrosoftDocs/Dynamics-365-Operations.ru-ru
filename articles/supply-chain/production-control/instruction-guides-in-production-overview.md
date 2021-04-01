---
title: Предоставление руководств с использованием смешанной реальности для работников на производстве
description: В этом разделе содержатся указания по интеграции модуля управления производством в Microsoft Dynamics 365 Supply Chain Management с Dynamics 365 Guides.
author: cabeln
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 48e0dfeba1a9744c90608d4d9009484df91c4b85
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246149"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a><span data-ttu-id="38ab5-103">Предоставление руководств с использованием смешанной реальности для работников на производстве</span><span class="sxs-lookup"><span data-stu-id="38ab5-103">Provide mixed-reality Guides for workers in production</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="38ab5-104">Работники производственных процессов получат преимущества от соответствующих инструкций, предоставляемых в нужное время в контексте их работы.</span><span class="sxs-lookup"><span data-stu-id="38ab5-104">Workers in production processes will benefit from relevant instructions that are provided at the right time in the context of their work.</span></span> <span data-ttu-id="38ab5-105">*Инструкции* применимы в нескольких доменах работы, включая следующие: сборка, обслуживание, эксплуатация, сертификация и безопасность.</span><span class="sxs-lookup"><span data-stu-id="38ab5-105">*Instructions* apply in several domains of work, including: assembly, service, operations, certification, and safety.</span></span> <span data-ttu-id="38ab5-106">Во всех этих основных бизнес-функциях текущие обучающие инструкции помогут сотрудникам повысить эффективность работы и достигнуть большего.</span><span class="sxs-lookup"><span data-stu-id="38ab5-106">Across all of these core business functions, ongoing training instructions can help empower workers to achieve more and work better.</span></span>

## <a name="introduction"></a><span data-ttu-id="38ab5-107">Введение</span><span class="sxs-lookup"><span data-stu-id="38ab5-107">Introduction</span></span>

<span data-ttu-id="38ab5-108">Инструкции можно предоставить различными способами.</span><span class="sxs-lookup"><span data-stu-id="38ab5-108">You can provide instructions in different ways.</span></span> <span data-ttu-id="38ab5-109">Одна эффективная система, поставляемая в готовом виде, это [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span><span class="sxs-lookup"><span data-stu-id="38ab5-109">One efficient system that ships out of the box uses [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span></span>

<span data-ttu-id="38ab5-110">Dynamics 365 Guides может помочь предоставить сотрудникам практические навыки.</span><span class="sxs-lookup"><span data-stu-id="38ab5-110">Dynamics 365 Guides can help empower your employees with hands-on learning.</span></span> <span data-ttu-id="38ab5-111">Можно определить стандартизированные процессы с пошаговыми инструкциями, которые позволяют сотрудникам работать с инструментами и компонентами, которые им необходимы, и показывать сотрудникам, как использовать эти средства в реальных условиях работы.</span><span class="sxs-lookup"><span data-stu-id="38ab5-111">You can define standardized processes with step-by-step instructions that guide your employees to the tools and parts they need and show employees how to use these tools in real work situations.</span></span>

<span data-ttu-id="38ab5-112">Можно привязывать руководства к различным аспектам управления производством, в том числе:</span><span class="sxs-lookup"><span data-stu-id="38ab5-112">You can attach guides to various aspects of production control including:</span></span>

- [<span data-ttu-id="38ab5-113">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="38ab5-113">Resources</span></span>](#resources)
- [<span data-ttu-id="38ab5-114">Группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="38ab5-114">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="38ab5-115">Используемые продукты</span><span class="sxs-lookup"><span data-stu-id="38ab5-115">Released products</span></span>](#released-products)
- [<span data-ttu-id="38ab5-116">Формулы</span><span class="sxs-lookup"><span data-stu-id="38ab5-116">Formulas</span></span>](#formulas)
- [<span data-ttu-id="38ab5-117">Версии формулы</span><span class="sxs-lookup"><span data-stu-id="38ab5-117">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="38ab5-118">Спецификации (BOM)</span><span class="sxs-lookup"><span data-stu-id="38ab5-118">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="38ab5-119">Версии BOM</span><span class="sxs-lookup"><span data-stu-id="38ab5-119">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="38ab5-120">Маршруты</span><span class="sxs-lookup"><span data-stu-id="38ab5-120">Routes</span></span>](#routes)
- [<span data-ttu-id="38ab5-121">Версии маршрута</span><span class="sxs-lookup"><span data-stu-id="38ab5-121">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="38ab5-122">Отношения операций маршрута</span><span class="sxs-lookup"><span data-stu-id="38ab5-122">Route operation relations</span></span>](#route-operation-relations)

> [!NOTE]
> <span data-ttu-id="38ab5-123">Также можно привязать Guides к управлению активами.</span><span class="sxs-lookup"><span data-stu-id="38ab5-123">You can also attach Guides with Asset Management.</span></span> <span data-ttu-id="38ab5-124">Дополнительные сведения об этой возможности см. в разделе [Интеграция Dynamics 365 Supply Chain Management (Управление активами) с Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span><span class="sxs-lookup"><span data-stu-id="38ab5-124">For more information about that option, see [Integrate Dynamics 365 Supply Chain Management (Asset Management) with Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span></span>

<span data-ttu-id="38ab5-125">Когда работник первой линии выбирает задание в цехе через Supply Chain Management, работник может просмотреть [соответствующие руководства](#logic) в карте задания.</span><span class="sxs-lookup"><span data-stu-id="38ab5-125">When a first-line worker chooses a job on the shop floor through Supply Chain Management, the worker can see [the relevant guides](#logic) on the job card.</span></span> <span data-ttu-id="38ab5-126">Когда работник выбирает конкретное руководство, на экране отображается QR-код для этого руководства.</span><span class="sxs-lookup"><span data-stu-id="38ab5-126">When the worker chooses a specific guide, a QR code for that guide is shown on the screen.</span></span> <span data-ttu-id="38ab5-127">Затем работник использует свои очки HoloLens для сканирования QR-кода, который запускает Guides и отображает необходимые инструкции.</span><span class="sxs-lookup"><span data-stu-id="38ab5-127">The worker then uses their HoloLens to scan the QR code, which launches Guides and shows the required instructions.</span></span>

<span data-ttu-id="38ab5-128">В следующих подразделах описывается несколько выбранных сценариев, в которых компании в различных отраслях могут видеть самое большое значение при использовании Guides для представления инструкций для производства.</span><span class="sxs-lookup"><span data-stu-id="38ab5-128">The following subsections describe a few selected scenarios where companies across industries can see the biggest value when using Guides to present instructions for manufacturing.</span></span>

### <a name="assembly"></a><span data-ttu-id="38ab5-129">Сборка</span><span class="sxs-lookup"><span data-stu-id="38ab5-129">Assembly</span></span>

<span data-ttu-id="38ab5-130">![Использование Guides в задачах сборки](media/instruction-guides-hero-assembly.png "Использование Guides в задачах сервиса")</span><span class="sxs-lookup"><span data-stu-id="38ab5-130">![Use Guides in assembly tasks](media/instruction-guides-hero-assembly.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="38ab5-131">Инструкции в операциях сборки показывают сотрудникам необходимые инструменты и компоненты, а также порядок их использования в реальных условиях работы.</span><span class="sxs-lookup"><span data-stu-id="38ab5-131">Instructions in assembly operations show workers the tools and parts they need and how to use them in real work situations.</span></span>

<span data-ttu-id="38ab5-132">Производственные менеджеры могут создавать и назначать руководства Guides, например, для [производственных маршрутов](routes-operations.md), [отношений операций](routes-operations.md#operation-relations) или [спецификаций](bill-of-material-bom.md).</span><span class="sxs-lookup"><span data-stu-id="38ab5-132">Production managers can create and assign Guides, for example, for [production routes](routes-operations.md), [operation relations](routes-operations.md#operation-relations), or [bills of material](bill-of-material-bom.md).</span></span> <span data-ttu-id="38ab5-133">Работники найдут соответствующие инструкции по соответствующему опыту работы в цехе.</span><span class="sxs-lookup"><span data-stu-id="38ab5-133">Workers will find the relevant instructions on the respective operation experience on the shop floor.</span></span>

### <a name="service"></a><span data-ttu-id="38ab5-134">Сервис</span><span class="sxs-lookup"><span data-stu-id="38ab5-134">Service</span></span>

<span data-ttu-id="38ab5-135">![Использование Guides в задачах сервиса](media/instruction-guides-hero-service.png "Использование Guides в задачах сервиса")</span><span class="sxs-lookup"><span data-stu-id="38ab5-135">![Use Guides in service tasks](media/instruction-guides-hero-service.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="38ab5-136">Предоставьте техническим специалистам руководящие инструкции на месте работы, устраняющие необходимость планирования дополнительных посещений.</span><span class="sxs-lookup"><span data-stu-id="38ab5-136">Equip technicians with guided instructions at the job site, eliminating the need to schedule additional visits.</span></span>

<span data-ttu-id="38ab5-137">Менеджеры по обслуживанию могут назначать руководства Guides, например, для отдельных [продуктов](../../commerce/product.md), которые проходят повседневную оценку качества.</span><span class="sxs-lookup"><span data-stu-id="38ab5-137">Service managers can assign Guides, for example, to specific [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="quality"></a><span data-ttu-id="38ab5-138">Качество</span><span class="sxs-lookup"><span data-stu-id="38ab5-138">Quality</span></span>

<span data-ttu-id="38ab5-139">![Использование Guides в задачах обеспечения качества](media/instruction-guides-hero-quality.png "Использование Guides в задачах обеспечения качества")</span><span class="sxs-lookup"><span data-stu-id="38ab5-139">![Use Guides in quality assurance tasks](media/instruction-guides-hero-quality.png "Use Guides in quality assurance tasks")</span></span>

<span data-ttu-id="38ab5-140">Развертывайте новые процессы и обеспечьте повышенную согласованность, превратив знания сотрудников в воспроизводимое средство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-140">Rollout new processes and ensure increased consistency by turning employee knowledge into a repeatable tool.</span></span>

<span data-ttu-id="38ab5-141">Менеджеры по обеспечению качества могут назначать руководства, например, для отдельных [продуктов](../../commerce/product.md), которые проходят повседневную оценку качества.</span><span class="sxs-lookup"><span data-stu-id="38ab5-141">Quality assurance managers can assign guides, for example, to [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="certifications"></a><span data-ttu-id="38ab5-142">Сертификации</span><span class="sxs-lookup"><span data-stu-id="38ab5-142">Certifications</span></span>

<span data-ttu-id="38ab5-143">![Использование Guides для задач, касающихся сертификации](media/instruction-guides-hero-certification.png "Использование Guides для задач, касающихся сертификации")</span><span class="sxs-lookup"><span data-stu-id="38ab5-143">![Use Guides for certification related tasks](media/instruction-guides-hero-certification.png "Use Guides for certification related tasks")</span></span>

<span data-ttu-id="38ab5-144">Убедитесь, что все сотрудники отвечают требованиям высокого стандарта, быстро определяя, кому требуются помощь и где.</span><span class="sxs-lookup"><span data-stu-id="38ab5-144">Ensure every employee meets high standards by quickly identifying who needs help and where.</span></span>

### <a name="safety"></a><span data-ttu-id="38ab5-145">Безопасность</span><span class="sxs-lookup"><span data-stu-id="38ab5-145">Safety</span></span>

<span data-ttu-id="38ab5-146">![Использование Guides в инструкциях по технике безопасности работы](media/instruction-guides-hero-safety.png "Использование Guides в инструкциях по технике безопасности работы")</span><span class="sxs-lookup"><span data-stu-id="38ab5-146">![Use Guides in work safety instructions](media/instruction-guides-hero-safety.png "Use Guides in work safety instructions")</span></span>

<span data-ttu-id="38ab5-147">Предоставьте инструкции, в которых виртуально полностью рассматриваются опасные процедуры перед их выполнением в физической среде.</span><span class="sxs-lookup"><span data-stu-id="38ab5-147">Provide instructions that walk through dangerous procedures virtually before attempting in the physical environment.</span></span> <span data-ttu-id="38ab5-148">Благодаря подходу смешанной реальности работники могут виртуально изучить опасные процедуры.</span><span class="sxs-lookup"><span data-stu-id="38ab5-148">With a mixed reality approach, workers can experience dangerous procedures virtually.</span></span>

<span data-ttu-id="38ab5-149">Менеджеры производства могут предоставить специальные инструкции по обращению с вредными материалами или процедуры бережного обращения, назначая инструкции [номенклатурам продуктов](../../commerce/product.md), [маршрутам](routes-operations.md) и [операциям](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="38ab5-149">Production managers can provide dedicated handling instructions for hazardous material handling or delicate handling procedures by assigning instructions to [product items](../../commerce/product.md), [routes](routes-operations.md), and [operations](routes-operations.md#operation-relations).</span></span>

## <a name="get-started-with-instructions-and-guides"></a><span data-ttu-id="38ab5-150">Приступая к работе с инструкциями и приложением Guides</span><span class="sxs-lookup"><span data-stu-id="38ab5-150">Get started with instructions and Guides</span></span>

<span data-ttu-id="38ab5-151">Чтобы включить инструкции в производственных процессах, Supply Chain Management обеспечивает готовую интеграцию с Dynamics 365 Guides.</span><span class="sxs-lookup"><span data-stu-id="38ab5-151">To enable instructions in production processes, Supply Chain Management provides an out-of-the-box integration with Dynamics 365 Guides.</span></span> <span data-ttu-id="38ab5-152">Лицензированный и установленный экземпляр приложения Guides требуется для создания, поддержки и назначения инструкций смешанной реальности для производственных активов и работы.</span><span class="sxs-lookup"><span data-stu-id="38ab5-152">A licensed and installed application instance of Guides is required to build, maintain, and assign mixed reality instructions to production assets and work.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="38ab5-153">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="38ab5-153">Prerequisites</span></span>

<span data-ttu-id="38ab5-154">Для использования этой функции в систему должны быть включены следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="38ab5-154">To use this feature, your system must include the following:</span></span>

- <span data-ttu-id="38ab5-155">Dynamics 365 Supply Chain Management версии 10.0.15 или более новая версия</span><span class="sxs-lookup"><span data-stu-id="38ab5-155">Dynamics 365 Supply Chain Management version 10.0.15 or later</span></span>
- <span data-ttu-id="38ab5-156">[Двойная запись](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) для приложений Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="38ab5-156">[Dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) for Supply Chain Management apps.</span></span>
- <span data-ttu-id="38ab5-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) версии 400.0.1.48 или более новая версия</span><span class="sxs-lookup"><span data-stu-id="38ab5-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 or later</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="38ab5-158">Включение функции</span><span class="sxs-lookup"><span data-stu-id="38ab5-158">Turn on the feature</span></span>

<span data-ttu-id="38ab5-159">Чтобы функция была доступна в системе, необходимо активировать ее конфигурационные ключи.</span><span class="sxs-lookup"><span data-stu-id="38ab5-159">To make the feature available on your system, you must enable its configuration keys.</span></span> <span data-ttu-id="38ab5-160">Это необходимо сделать только один раз.</span><span class="sxs-lookup"><span data-stu-id="38ab5-160">You only need to do this once.</span></span> <span data-ttu-id="38ab5-161">Для этого администратор должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="38ab5-161">To do this, an administrator must do the following:</span></span>

1. <span data-ttu-id="38ab5-162">Переведите систему в режим обслуживания, как описано в разделе [Режим обслуживания](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="38ab5-162">Place your system into maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="38ab5-163">Перейдите в раздел **Администрирование системы \> Настройка \> Конфигурация лицензии**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-163">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="38ab5-164">Разверните раздел **Смешанная реальность**, затем установите флажок **Руководство в смешанной реальности**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-164">Expand the **Mixed reality** section and then select the **Mixed reality guide** check box.</span></span>
1. <span data-ttu-id="38ab5-165">Разверните раздел **Управление производством**, затем установите флажок **Производственные инструкции**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-165">Expand the **Production management** section and then select the **Production instructions** check box.</span></span>
1. <span data-ttu-id="38ab5-166">Выключите режим обслуживания, как описано в разделе [Режим обслуживания](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="38ab5-166">Turn off maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a><span data-ttu-id="38ab5-167">Настройка отображения Guides в цехе</span><span class="sxs-lookup"><span data-stu-id="38ab5-167">Configure how Guides appear on the shop floor</span></span>

<span data-ttu-id="38ab5-168">Чтобы настроить отображение Guides в цехе, перейдите в раздел **Смешанная реальность \> Dynamics 365 Guides \> Настройка интеграции Guides**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-168">To configure how Guides appear on the shop floor, go to **Mixed Reality \> Dynamics 365 Guides \> Configure Guides integration**.</span></span>

<span data-ttu-id="38ab5-169">![Настройка интеграции Guides для производства](media/instruction-guides-configure-integration.png "Настройка интеграции Guides для производства")</span><span class="sxs-lookup"><span data-stu-id="38ab5-169">![Configure Guide integration for manufacturing](media/instruction-guides-configure-integration.png "Configure Guide integration for manufacturing")</span></span>

<span data-ttu-id="38ab5-170">Задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="38ab5-170">Set the following fields:</span></span>

- <span data-ttu-id="38ab5-171">**URL-адрес Microsoft Dataverse** — указывается URL-адрес среды Microsoft Dataverse, в которой создаются руководства Guides.</span><span class="sxs-lookup"><span data-stu-id="38ab5-171">**Microsoft Dataverse URL** - Specify the URL for the Microsoft Dataverse environment where you create your Guides.</span></span> <span data-ttu-id="38ab5-172">Форматом является "contoso.crm4.dynamics.com", где первая часть URL-адреса обычно называется по названию организации (например, "contoso."), вторая часть относится к области данных среды (например, "crm4."), а последняя часть — это домен (например, "dynamics.com").</span><span class="sxs-lookup"><span data-stu-id="38ab5-172">The format is "contoso.crm4.dynamics.com", where the first part of the URL is typically named after your organization (such as "contoso."), the second part is specific to the data region of your environment (such as "crm4."), and the last part is the domain (such as "dynamics.com").</span></span> <span data-ttu-id="38ab5-173">Одним из способов поиска правильного URL-адреса является переход на [home.dynamics.com](https://home.dynamics.com/) и последующее открытие приложения Guides.</span><span class="sxs-lookup"><span data-stu-id="38ab5-173">One way to find the right URL is to go to [home.dynamics.com](https://home.dynamics.com/) and then open your Guides app.</span></span> <span data-ttu-id="38ab5-174">При открытии Guides в адресной строке браузера вы увидите URL-адрес (берите только базовый URL-адрес, который должен быть аналогичен предыдущему примеру).</span><span class="sxs-lookup"><span data-stu-id="38ab5-174">When Guides opens, you will see the URL in the address bar of your browser (only take the base URL, which should resemble the previous example).</span></span> <span data-ttu-id="38ab5-175">Это значение используется для составления адресов для ваших руководств и будет закодировано в QR-коды."</span><span class="sxs-lookup"><span data-stu-id="38ab5-175">This value is used to compose addresses for your guides and will be encoded into the QR codes."</span></span>
- <span data-ttu-id="38ab5-176">**Размер QR-кода** — устанавливает размер визуализированного QR-кода.</span><span class="sxs-lookup"><span data-stu-id="38ab5-176">**QR code size** - Set the size of the rendered QR code.</span></span> <span data-ttu-id="38ab5-177">Рекомендуется выбирать размер, который будет занимать большую часть экрана отображения, но не более.</span><span class="sxs-lookup"><span data-stu-id="38ab5-177">We recommend choosing a size that will fill most of your display screen, but not more.</span></span> <span data-ttu-id="38ab5-178">Обычно значение *15* является хорошим значением.</span><span class="sxs-lookup"><span data-stu-id="38ab5-178">Typically, *15* is a good value.</span></span>
- <span data-ttu-id="38ab5-179">**Уровень коррекции ошибок QR-кода** — настройка степени детализации QR-кода.</span><span class="sxs-lookup"><span data-stu-id="38ab5-179">**QR code error correction level** - Set the granularity of the QR code.</span></span> <span data-ttu-id="38ab5-180">Повышение детализации может способствовать повышению надежности кода, но **Размер QR-кода** должен быть достаточным для того, чтобы поддерживать уровень детализации, необходимый для выбранного уровня коррекции.</span><span class="sxs-lookup"><span data-stu-id="38ab5-180">Higher granularity can help increase the code's reliability, but your **QR code size** must be large enough to support the level of detail required by your selected correction level.</span></span>

> [!TIP]
> - <span data-ttu-id="38ab5-181">Размеры QR-кодов, которые слишком велики для дисплея, будут отрисовываться несколько дольше, а затем будут масштабироваться в соответствии с размером экрана.</span><span class="sxs-lookup"><span data-stu-id="38ab5-181">QR codes sizes that are too large for your display will take a bit longer to render and then be scaled down to fit your display.</span></span> <span data-ttu-id="38ab5-182">Это не предоставляет преимуществ.</span><span class="sxs-lookup"><span data-stu-id="38ab5-182">These do not provide a benefit.</span></span>
> - <span data-ttu-id="38ab5-183">Слишком маленькие размеры QR-кода могут привести к снижению возможности HoloLens по чтению кода в некоторых средах.</span><span class="sxs-lookup"><span data-stu-id="38ab5-183">QR code sizes that are too small may decrease the ability of HoloLens to read the code properly in some environments.</span></span>
> - <span data-ttu-id="38ab5-184">Рекомендуется проверить настройки для каждого устройства, которое будет выводить QR-коды для пользователей HoloLens.</span><span class="sxs-lookup"><span data-stu-id="38ab5-184">We recommend that you test the settings for each device that will display QR codes for HoloLens users.</span></span> <span data-ttu-id="38ab5-185">Выберите настройки, обеспечивающие достаточную удобочитаемость в ваших производственных условиях.</span><span class="sxs-lookup"><span data-stu-id="38ab5-185">Choose settings that provide sufficient readability in your shop floor environment.</span></span>  

## <a name="get-an-overview-of-all-guide-assignments"></a><span data-ttu-id="38ab5-186">Обзор всех назначений для руководств</span><span class="sxs-lookup"><span data-stu-id="38ab5-186">Get an overview of all Guide assignments</span></span>

<span data-ttu-id="38ab5-187">Страница **Все руководства** предназначена для просмотра списка всех доступных руководств в вашей организации и всех назначений в производственных процессах и ресурсах.</span><span class="sxs-lookup"><span data-stu-id="38ab5-187">Use the **All Guides** page to see the list of all available Guides in your organization and all assignments to your production processes and resources.</span></span> <span data-ttu-id="38ab5-188">Чтобы открыть ее, перейдите в раздел **Смешанная реальность \> Guides \> Все руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-188">To open it, go to **Mixed reality \> Guides \> All Guides**.</span></span> <span data-ttu-id="38ab5-189">В списке в верхней части отображаются все доступные руководства Guides, и для фильтрации списка можно использовать это поле.</span><span class="sxs-lookup"><span data-stu-id="38ab5-189">The list at the top shows all the available Guides and you can use the field here to filter the list.</span></span> <span data-ttu-id="38ab5-190">В списке, расположенном в нижней части экрана, показаны все назначения руководств Guides и представлена панель инструментов для управления ими.</span><span class="sxs-lookup"><span data-stu-id="38ab5-190">The list at the bottom shows all Guide assignments and provides a toolbar for managing them.</span></span>

<span data-ttu-id="38ab5-191">![Управление руководствами Guides](media/instruction-guides-allguides.png "Управление руководствами Guides")</span><span class="sxs-lookup"><span data-stu-id="38ab5-191">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

<span data-ttu-id="38ab5-192">В следующих разделах описываются типы объектов, которым можно назначить руководства Guides.</span><span class="sxs-lookup"><span data-stu-id="38ab5-192">The following sections describe the types of objects that you can assign Guides to.</span></span> <span data-ttu-id="38ab5-193">Каждое назначенное руководство содержит инструкции, которые автоматически присоединяются к соответствующим производственным заданиям и будут доступны в цехе.</span><span class="sxs-lookup"><span data-stu-id="38ab5-193">Each assigned guide provides instructions that are automatically attached to the respective production jobs and will be available on the shop floor.</span></span>

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a><span data-ttu-id="38ab5-194">Связывание руководства с ресурсом</span><span class="sxs-lookup"><span data-stu-id="38ab5-194">Associate a Guide to a resource</span></span>

<span data-ttu-id="38ab5-195">Добавьте руководство к [ресурсу](operations-resources.md) для предложения руководства в контексте соответствующих производственных заданий.</span><span class="sxs-lookup"><span data-stu-id="38ab5-195">Add a Guide to a [resource](operations-resources.md) to offer the Guide in the context of relevant production jobs.</span></span>

### <a name="typical-scenario-using-resources"></a><span data-ttu-id="38ab5-196">Типичный сценарий использования ресурсов</span><span class="sxs-lookup"><span data-stu-id="38ab5-196">Typical scenario using resources</span></span>

<span data-ttu-id="38ab5-197">Например, можно привязать к ресурсу типа "машина" руководство по общей технике безопасности или инструкции по обращению.</span><span class="sxs-lookup"><span data-stu-id="38ab5-197">For example, you could attach a Guide with general machine security or handling instructions to a resource of type machine.</span></span> <span data-ttu-id="38ab5-198">Затем руководство будет доступно для каждого задания, выполняемого на машине.</span><span class="sxs-lookup"><span data-stu-id="38ab5-198">Then, the Guide will be available on every job that is performed on the machine.</span></span>

### <a name="add-a-guide-to-a-resource"></a><span data-ttu-id="38ab5-199">Добавление руководства к ресурсу</span><span class="sxs-lookup"><span data-stu-id="38ab5-199">Add a Guide to a resource</span></span>

<span data-ttu-id="38ab5-200">Для добавление руководства к ресурсу:</span><span class="sxs-lookup"><span data-stu-id="38ab5-200">To add a Guide to a resource:</span></span>

1. <span data-ttu-id="38ab5-201">Перейдите в раздел **Управление производством \> Настройка \> Ресурсы \> Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-201">Go to **Production control \> Setup \> Resources \> Resources**.</span></span>
1. <span data-ttu-id="38ab5-202">В области списка выберите ресурс, которому требуется назначить руководство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-202">From the list pane, select the resource you want to assign a Guide to.</span></span>
1. <span data-ttu-id="38ab5-203">Разверните экспресс-вкладку **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-203">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="38ab5-204">Выберите **Добавить** на панели инструментов **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-204">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="38ab5-205">В сетку добавляется новая строка.</span><span class="sxs-lookup"><span data-stu-id="38ab5-205">A new line is added to the grid.</span></span>
1. <span data-ttu-id="38ab5-206">Для новой строки воспользуйтесь раскрывающимся списком в столбце **Имя**, чтобы выбрать руководство, которое требуется назначить.</span><span class="sxs-lookup"><span data-stu-id="38ab5-206">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="38ab5-207">Если имеется большое число руководств, можно отфильтровать список, чтобы найти нужное.</span><span class="sxs-lookup"><span data-stu-id="38ab5-207">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="38ab5-208">![Управление руководствами Guides](media/instruction-guides-allguides.png "Управление руководствами Guides")</span><span class="sxs-lookup"><span data-stu-id="38ab5-208">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a><span data-ttu-id="38ab5-209">Связывание руководства с группой ресурсов</span><span class="sxs-lookup"><span data-stu-id="38ab5-209">Associate a Guide to a resource group</span></span>

<span data-ttu-id="38ab5-210">Можно добавить руководство к [группам ресурсов](tasks/define-discrete-manufacturing-resource-group.md), если вы используете их для управления группами машин, производственных линий или рабочих ячеек.</span><span class="sxs-lookup"><span data-stu-id="38ab5-210">You can add a guide to [resource groups](tasks/define-discrete-manufacturing-resource-group.md) if you use them to manage groups of machines, production lines, or work cells.</span></span>

### <a name="typical-scenarios-using-resource-groups"></a><span data-ttu-id="38ab5-211">Типичные сценарии использования групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="38ab5-211">Typical scenarios using resource groups</span></span>

<span data-ttu-id="38ab5-212">**Пример 1:** группа ресурсов определена для нескольких машин одной модели.</span><span class="sxs-lookup"><span data-stu-id="38ab5-212">**Example 1:** You have defined a resource group for several machines of the same model.</span></span> <span data-ttu-id="38ab5-213">Вместо назначения соответствующей инструкции по обращению для этой модели машины каждому соответствующему ресурсу, можно назначить руководство группе ресурсов, отражающей эту модель машины.</span><span class="sxs-lookup"><span data-stu-id="38ab5-213">Instead of assigning the relevant handling instruction guide for the machine model to every relevant resource, you could instead assign the Guide to the resource group that reflects that machine model.</span></span>

<span data-ttu-id="38ab5-214">**Пример 2:** определена группа ресурсов для производственной ячейки, содержащей различные машины, и имеется руководство, содержащее общие инструкции по поддержке производственной ячейки.</span><span class="sxs-lookup"><span data-stu-id="38ab5-214">**Example 2:** You have defined a resource group for a work cell that contains different machines and you have a Guide that provides general instructions for how to maintain the work cell.</span></span> <span data-ttu-id="38ab5-215">Руководство применяется ко всем производственным мероприятиям в этой производственной ячейке.</span><span class="sxs-lookup"><span data-stu-id="38ab5-215">The Guide applies to any production activity in this work cell.</span></span>

### <a name="add-a-guide-to-a-resource-group"></a><span data-ttu-id="38ab5-216">Добавление руководства к группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="38ab5-216">Add a Guide to a resource group</span></span>

<span data-ttu-id="38ab5-217">Чтобы добавить руководство к группе ресурсов:</span><span class="sxs-lookup"><span data-stu-id="38ab5-217">To add a Guide to a resource group:</span></span>

1. <span data-ttu-id="38ab5-218">Перейдите в раздел **Управление производством \> Настройка \> Ресурсы \> Группы ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-218">Go to **Production control \> Setup \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="38ab5-219">В области списка выберите группу ресурсов, которой требуется назначить руководство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-219">From the list pane, select the resource group you want to assign a Guide to.</span></span>
1. <span data-ttu-id="38ab5-220">Разверните экспресс-вкладку **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-220">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="38ab5-221">Выберите **Добавить** на панели инструментов **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-221">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="38ab5-222">В сетку добавляется новая строка.</span><span class="sxs-lookup"><span data-stu-id="38ab5-222">A new line is added to the grid.</span></span>
1. <span data-ttu-id="38ab5-223">Для новой строки воспользуйтесь раскрывающимся списком в столбце **Имя**, чтобы выбрать руководство, которое требуется назначить.</span><span class="sxs-lookup"><span data-stu-id="38ab5-223">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="38ab5-224">Если имеется большое число руководств, можно отфильтровать список, чтобы найти нужное.</span><span class="sxs-lookup"><span data-stu-id="38ab5-224">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="38ab5-225">![Добавление руководства к группе ресурсов](media/instruction-guides-resourcegroup.png "Добавление руководства к группе ресурсов")</span><span class="sxs-lookup"><span data-stu-id="38ab5-225">![Adding a Guide to a resource group](media/instruction-guides-resourcegroup.png "Adding a Guide to a resource group")</span></span>

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a><span data-ttu-id="38ab5-226">Связывание руководства с выпущенным продуктом</span><span class="sxs-lookup"><span data-stu-id="38ab5-226">Associate a Guide to a released product</span></span>

<span data-ttu-id="38ab5-227">Можно добавить руководство к любому [выпущенному продукту](../pim/tasks/create-released-product-single-company.md).</span><span class="sxs-lookup"><span data-stu-id="38ab5-227">You can add a guide to any [released product](../pim/tasks/create-released-product-single-company.md).</span></span>

### <a name="typical-scenario-using-released-products"></a><span data-ttu-id="38ab5-228">Типичный сценарий использования выпущенных продуктов</span><span class="sxs-lookup"><span data-stu-id="38ab5-228">Typical scenario using released products</span></span>

<span data-ttu-id="38ab5-229">Руководства уровня продукта помогают сотрудникам цеха с инструкциями, относящимися к работе или обращению с конкретным выпущенным продуктом или номенклатурой.</span><span class="sxs-lookup"><span data-stu-id="38ab5-229">Product-level Guides help shop floor workers with instructions relevant to operating or handling a specific released product or item.</span></span>

### <a name="add-a-guide-to-a-released-product"></a><span data-ttu-id="38ab5-230">Добавление руководства к выпущенному продукту</span><span class="sxs-lookup"><span data-stu-id="38ab5-230">Add a Guide to a released product</span></span>

<span data-ttu-id="38ab5-231">Чтобы добавить руководство к выпущенному продукту:</span><span class="sxs-lookup"><span data-stu-id="38ab5-231">To add a Guide to a released product:</span></span>

1. <span data-ttu-id="38ab5-232">Выберите **Управление сведениями о производстве \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-232">Go to **Production information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="38ab5-233">Откройте продукт, для которого требуется назначить руководство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-233">Open the product you want to assign a Guide to.</span></span>
1. <span data-ttu-id="38ab5-234">В области действий откройте вкладку **Инженер** и в группе **Представление** выберите **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-234">On the Action Pane, open the **Engineer** tab and from the **View** group, select **Associated Guides**.</span></span>
1. <span data-ttu-id="38ab5-235">Для выбранного продукта будет открыта страница **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-235">The **Associated Guides** page opens for your selected product.</span></span>
1. <span data-ttu-id="38ab5-236">Выберите **Добавить** на панели операций, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="38ab5-236">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="38ab5-237">Для новой строки воспользуйтесь раскрывающимся списком в столбце **Имя**, чтобы выбрать руководство, которое требуется назначить.</span><span class="sxs-lookup"><span data-stu-id="38ab5-237">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="38ab5-238">![Добавление руководства к выпущенному продукту](media/instruction-guides-ReleasedProduct-AddGuides.png "Добавление руководства к выпущенному продукту")</span><span class="sxs-lookup"><span data-stu-id="38ab5-238">![Adding a Guide to a released product](media/instruction-guides-ReleasedProduct-AddGuides.png "Adding a Guide to a released product")</span></span>

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a><span data-ttu-id="38ab5-239">Связывание руководства с формулой</span><span class="sxs-lookup"><span data-stu-id="38ab5-239">Associate a Guide to a formula</span></span>

<span data-ttu-id="38ab5-240">Можно добавить руководство к любой [формуле](bill-of-material-bom.md#formulas-co-products-and-by-products).</span><span class="sxs-lookup"><span data-stu-id="38ab5-240">You can add a guide to any [formula](bill-of-material-bom.md#formulas-co-products-and-by-products).</span></span>

### <a name="typical-scenario-using-formulas"></a><span data-ttu-id="38ab5-241">Типичный сценарий использования формул</span><span class="sxs-lookup"><span data-stu-id="38ab5-241">Typical scenario using formulas</span></span>
  
<span data-ttu-id="38ab5-242">Руководства на уровне формул обеспечивают работников цеха направляющими инструкциями по обращению в контексте формулы или рецепта.</span><span class="sxs-lookup"><span data-stu-id="38ab5-242">Formula-level Guides provide shop floor workers with guided handling instructions in the context of a formula or recipe.</span></span> <span data-ttu-id="38ab5-243">Руководства также могут быть назначены версиям формулы.</span><span class="sxs-lookup"><span data-stu-id="38ab5-243">Guides can also be assigned to versions of a formula.</span></span>

> [!NOTE]
> <span data-ttu-id="38ab5-244">Можно назначить руководство, соответствующее производственным процессам на основе формулы для маршрута, версии маршрута или отношений операций маршрута.</span><span class="sxs-lookup"><span data-stu-id="38ab5-244">You can assign guidance relevant for production processes based on a formula to a route, route version, or route operation relations.</span></span>  

> <span data-ttu-id="38ab5-245">В настоящее время руководства не могут прикрепляться к отдельным строкам формулы.</span><span class="sxs-lookup"><span data-stu-id="38ab5-245">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula"></a><span data-ttu-id="38ab5-246">Добавление руководства к формуле</span><span class="sxs-lookup"><span data-stu-id="38ab5-246">Add a Guide to a formula</span></span>

<span data-ttu-id="38ab5-247">Чтобы добавить руководство к формуле:</span><span class="sxs-lookup"><span data-stu-id="38ab5-247">To add a Guide to a formula:</span></span>

1. <span data-ttu-id="38ab5-248">Перейдите в раздел **Управление сведениями о производстве \> Спецификации и формулы \> Формулы**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-248">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="38ab5-249">Откройте формулу, для которой требуется назначить руководство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-249">Open the formula you want to assign a Guide to.</span></span>
1. <span data-ttu-id="38ab5-250">Откройте вкладку **Верхний колонтитул** над верхней экспресс-вкладкой.</span><span class="sxs-lookup"><span data-stu-id="38ab5-250">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="38ab5-251">Разверните экспресс-вкладку **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-251">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="38ab5-252">Выберите **Добавить** на панели инструментов **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-252">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="38ab5-253">В сетку добавляется новая строка.</span><span class="sxs-lookup"><span data-stu-id="38ab5-253">A new line is added to the grid.</span></span>
1. <span data-ttu-id="38ab5-254">Для новой строки воспользуйтесь раскрывающимся списком в столбце **Имя**, чтобы выбрать руководство, которое требуется назначить.</span><span class="sxs-lookup"><span data-stu-id="38ab5-254">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="38ab5-255">![Добавление руководства к формуле](media/instruction-guides-Formula.png "Добавление руководства к формуле")</span><span class="sxs-lookup"><span data-stu-id="38ab5-255">![Adding a Guide to a formula](media/instruction-guides-Formula.png "Adding a Guide to a formula")</span></span>

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a><span data-ttu-id="38ab5-256">Связывание руководства с версией формулы</span><span class="sxs-lookup"><span data-stu-id="38ab5-256">Associate a Guide to a formula version</span></span>

<span data-ttu-id="38ab5-257">Можно добавить руководство к любой [версии формулы](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="38ab5-257">You can add a guide to any [formula version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-formula-versions"></a><span data-ttu-id="38ab5-258">Типичный сценарий использования версий формулы</span><span class="sxs-lookup"><span data-stu-id="38ab5-258">Typical scenario using formula versions</span></span>

<span data-ttu-id="38ab5-259">Руководства, присоединенные к отдельной версии формулы, предоставляют сотрудникам цеха инструкции, которые проходят все этапы производства данной версии рецепта формулы.</span><span class="sxs-lookup"><span data-stu-id="38ab5-259">Guides attached to an individual version of a formula provide shop floor workers with instructions that walk through the production of that version of the formula recipe.</span></span>

> [!TIP]
> <span data-ttu-id="38ab5-260">Можно назначить руководство, соответствующее производственным процессам на основе этой версии формулы для маршрута, версии маршрута или отношений операций маршрута.</span><span class="sxs-lookup"><span data-stu-id="38ab5-260">You can assign guidance relevant for production processes based on this formula version to a route, route version, or route operation relations.</span></span>  

> [!NOTE]
> <span data-ttu-id="38ab5-261">В настоящее время руководства не могут прикрепляться к отдельным строкам формулы.</span><span class="sxs-lookup"><span data-stu-id="38ab5-261">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula-version"></a><span data-ttu-id="38ab5-262">Добавление руководства к версии формулы</span><span class="sxs-lookup"><span data-stu-id="38ab5-262">Add a Guide to a formula version</span></span>

<span data-ttu-id="38ab5-263">Чтобы добавить руководство к версии формулы:</span><span class="sxs-lookup"><span data-stu-id="38ab5-263">To add a Guide to a formula version:</span></span>

1. <span data-ttu-id="38ab5-264">Перейдите в раздел **Управление сведениями о производстве \> Спецификации и формулы \> Формулы**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-264">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="38ab5-265">Откройте формулу, содержащую версию, для которой необходимо назначить руководство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-265">Open the formula that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="38ab5-266">Откройте вкладку **Верхний колонтитул** над верхней экспресс-вкладкой.</span><span class="sxs-lookup"><span data-stu-id="38ab5-266">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="38ab5-267">На экспресс-вкладке **Версии формулы** выберите версию, для которой необходимо назначить руководство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-267">On the **Formula versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="38ab5-268">На панели инструментов **Версии формулы** выберите **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-268">On the **Formula versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="38ab5-269">![Открытие руководств, связанных с выбранной версией формулы](media/instruction-guides-FormulaVersion.png "Открытие руководств, связанных с выбранной версией формулы")</span><span class="sxs-lookup"><span data-stu-id="38ab5-269">![Open the Guides associated with a selected formula version](media/instruction-guides-FormulaVersion.png "Open the Guides associated with a selected formula version")</span></span>
1. <span data-ttu-id="38ab5-270">Для версии формула будет открыта страница **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-270">The **Associated Guides** page opens for your formula version.</span></span>
1. <span data-ttu-id="38ab5-271">Выберите **Добавить** на панели операций, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="38ab5-271">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="38ab5-272">Для новой строки воспользуйтесь раскрывающимся списком в столбце **Имя**, чтобы выбрать руководство, которое требуется назначить.</span><span class="sxs-lookup"><span data-stu-id="38ab5-272">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="38ab5-273">![Добавление руководства к версии формулы](media/instruction-guides-FormulaVersionAddGuide.png "Добавление руководства к версии формулы")</span><span class="sxs-lookup"><span data-stu-id="38ab5-273">![Adding a Guide to a formula version](media/instruction-guides-FormulaVersionAddGuide.png "Adding a Guide to a formula version")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a><span data-ttu-id="38ab5-274">Связывание руководства со спецификацией</span><span class="sxs-lookup"><span data-stu-id="38ab5-274">Associate a Guide to a bill of materials</span></span>

<span data-ttu-id="38ab5-275">Можно добавить руководство к любой [спецификации](bill-of-material-bom.md) (BOM).</span><span class="sxs-lookup"><span data-stu-id="38ab5-275">You can add a guide to any [bill of materials](bill-of-material-bom.md) (BOM).</span></span>

### <a name="typical-scenario-using-bills-of-materials"></a><span data-ttu-id="38ab5-276">Типичный сценарий использования спецификации</span><span class="sxs-lookup"><span data-stu-id="38ab5-276">Typical scenario using bills of materials</span></span>

<span data-ttu-id="38ab5-277">Руководства, присоединенные к спецификации, предоставляют сотрудникам цеха инструкции, объясняющие, как подготавливать и обрабатывать материал из спецификации.</span><span class="sxs-lookup"><span data-stu-id="38ab5-277">Guides attached to a BOM provide shop floor workers with instructions that explain how to prepare and handle material from a BOM.</span></span> <span data-ttu-id="38ab5-278">Руководства также могут быть назначены версиям спецификаций.</span><span class="sxs-lookup"><span data-stu-id="38ab5-278">Guides can also be assigned to versions of a BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="38ab5-279">В настоящее время руководства не могут прикрепляться к отдельным строкам спецификации.</span><span class="sxs-lookup"><span data-stu-id="38ab5-279">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials"></a><span data-ttu-id="38ab5-280">Добавление руководства к спецификации</span><span class="sxs-lookup"><span data-stu-id="38ab5-280">Add a Guide to a bill of materials</span></span>

<span data-ttu-id="38ab5-281">Чтобы добавить руководство к спецификации:</span><span class="sxs-lookup"><span data-stu-id="38ab5-281">To add a Guide to a bill of material:</span></span>

1. <span data-ttu-id="38ab5-282">Перейдите в раздел **Управление сведениями о производстве \> Спецификации и формулы \> Спецификации**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-282">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="38ab5-283">Откройте спецификацию, для которой требуется назначить руководство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-283">Open the bill of materials that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="38ab5-284">Откройте вкладку **Верхний колонтитул** над верхней экспресс-вкладкой.</span><span class="sxs-lookup"><span data-stu-id="38ab5-284">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="38ab5-285">Разверните экспресс-вкладку **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-285">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="38ab5-286">Выберите **Добавить** на панели инструментов **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-286">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="38ab5-287">В сетку добавляется новая строка.</span><span class="sxs-lookup"><span data-stu-id="38ab5-287">A new line is added to the grid.</span></span>
1. <span data-ttu-id="38ab5-288">Для новой строки воспользуйтесь раскрывающимся списком в столбце **Имя**, чтобы выбрать руководство, которое требуется назначить.</span><span class="sxs-lookup"><span data-stu-id="38ab5-288">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="38ab5-289">![Добавление руководства к спецификации](media/instruction-guides-BOM.png "Добавление руководства к спецификации")</span><span class="sxs-lookup"><span data-stu-id="38ab5-289">![Adding a Guide to a BOM](media/instruction-guides-BOM.png "Adding a Guide to a BOM")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a><span data-ttu-id="38ab5-290">Связывание руководства с версией спецификации</span><span class="sxs-lookup"><span data-stu-id="38ab5-290">Associate a Guide to a bill of materials version</span></span>

<span data-ttu-id="38ab5-291">Можно добавить руководство к любой [версии спецификации](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="38ab5-291">You can add a guide to any [bill of materials version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-bill-of-materials-versions"></a><span data-ttu-id="38ab5-292">Типичный сценарий использования версий спецификации</span><span class="sxs-lookup"><span data-stu-id="38ab5-292">Typical scenario using bill of materials versions</span></span>

<span data-ttu-id="38ab5-293">Руководства, присоединенные к отдельной версии спецификации, предоставляют работникам цеха инструкции, описывающие, как подготавливать и обрабатывать материал для версии спецификации, отличной от общей спецификации или других ее версий.</span><span class="sxs-lookup"><span data-stu-id="38ab5-293">Guides attached to an individual BOM version provide shop floor workers with instructions that explain how to prepare and handle material for a version of a BOM that is different from the generic BOM or other versions of it.</span></span>

> [!NOTE]
> <span data-ttu-id="38ab5-294">В настоящее время руководства не могут прикрепляться к отдельным строкам спецификации.</span><span class="sxs-lookup"><span data-stu-id="38ab5-294">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials-version"></a><span data-ttu-id="38ab5-295">Добавление руководства к версии спецификации</span><span class="sxs-lookup"><span data-stu-id="38ab5-295">Add a Guide to a bill of materials version</span></span>

<span data-ttu-id="38ab5-296">Чтобы добавить руководство к версии спецификации:</span><span class="sxs-lookup"><span data-stu-id="38ab5-296">To add a Guide to a bill of materials version:</span></span>

1. <span data-ttu-id="38ab5-297">Перейдите в раздел **Управление сведениями о производстве \> Спецификации и формулы \> Спецификации**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-297">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="38ab5-298">Откройте спецификацию, содержащую версию, для которой необходимо назначить руководство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-298">Open the BOM that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="38ab5-299">Откройте вкладку **Верхний колонтитул** над верхней экспресс-вкладкой.</span><span class="sxs-lookup"><span data-stu-id="38ab5-299">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="38ab5-300">На экспресс-вкладке **Версии спецификации** выберите версию, для которой необходимо назначить руководство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-300">On the **BOM versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="38ab5-301">На панели инструментов **Версии спецификации** выберите **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-301">On the **BOM versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="38ab5-302">![Открытие руководств, связанных с выбранной версией спецификации](media/instruction-guides-BOMVersion.png "Открытие руководств, связанных с выбранной версией спецификации")</span><span class="sxs-lookup"><span data-stu-id="38ab5-302">![Open the Guides associated with a selected BOM version](media/instruction-guides-BOMVersion.png "Open the Guides associated with a selected BOM version")</span></span>
1. <span data-ttu-id="38ab5-303">Для версии спецификации будет открыта страница **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-303">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="38ab5-304">Выберите **Добавить** на панели операций, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="38ab5-304">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="38ab5-305">Для новой строки воспользуйтесь раскрывающимся списком в столбце **Имя**, чтобы выбрать руководство, которое требуется назначить.</span><span class="sxs-lookup"><span data-stu-id="38ab5-305">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="38ab5-306">![Добавление руководства к версии спецификации](media/instruction-guides-BOMVersionAddGuide.png "Добавление руководства к версии спецификации")</span><span class="sxs-lookup"><span data-stu-id="38ab5-306">![Adding a Guide to a BOM version](media/instruction-guides-BOMVersionAddGuide.png "Adding a Guide to a BOM version")</span></span>

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a><span data-ttu-id="38ab5-307">Связывание руководства с маршрутом</span><span class="sxs-lookup"><span data-stu-id="38ab5-307">Associate a Guide to a route</span></span>

<span data-ttu-id="38ab5-308">Можно добавить руководство к любому [маршруту](routes-operations.md).</span><span class="sxs-lookup"><span data-stu-id="38ab5-308">You can add a guide to any [route](routes-operations.md).</span></span>

### <a name="typical-scenario-using-routes"></a><span data-ttu-id="38ab5-309">Типичный сценарий использования маршрутов</span><span class="sxs-lookup"><span data-stu-id="38ab5-309">Typical scenario using routes</span></span>

<span data-ttu-id="38ab5-310">Маршруты обычно используются, чтобы указать, как должен производиться определенный выпущенный продукт на основе спецификации или версии спецификации, а также с набором ресурсов или групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38ab5-310">Routes are typically used to specify how a certain released product shall be produced based on a BOM or BOM version and with a set of resources or resource groups.</span></span>

<span data-ttu-id="38ab5-311">Назначьте руководство маршруту, чтобы предоставить пошаговые инструкции для соответствующего производственного процесса.</span><span class="sxs-lookup"><span data-stu-id="38ab5-311">Assign a Guide to a route to provide step-by-step instructions for the respective production process.</span></span>

### <a name="add-a-guide-to-a-route"></a><span data-ttu-id="38ab5-312">Добавление руководства к маршруту</span><span class="sxs-lookup"><span data-stu-id="38ab5-312">Add a Guide to a route</span></span>

<span data-ttu-id="38ab5-313">Чтобы добавить руководство к маршруту:</span><span class="sxs-lookup"><span data-stu-id="38ab5-313">To add a Guide to a route:</span></span>

1. <span data-ttu-id="38ab5-314">Перейдите в раздел **Управление производством \> Все маршруты**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-314">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="38ab5-315">Откройте маршрут, для которого требуется назначить руководство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-315">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="38ab5-316">Разверните экспресс-вкладку **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-316">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="38ab5-317">Выберите **Добавить** на панели инструментов **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-317">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="38ab5-318">В сетку добавляется новая строка.</span><span class="sxs-lookup"><span data-stu-id="38ab5-318">A new line is added to the grid.</span></span>
1. <span data-ttu-id="38ab5-319">Для новой строки воспользуйтесь раскрывающимся списком в столбце **Имя**, чтобы выбрать руководство, которое требуется назначить.</span><span class="sxs-lookup"><span data-stu-id="38ab5-319">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="38ab5-320">![Добавление руководства к маршруту](media/instruction-guides-Route.png "Добавление руководства к маршруту")</span><span class="sxs-lookup"><span data-stu-id="38ab5-320">![Adding a Guide to a route](media/instruction-guides-Route.png "Adding a Guide to a route")</span></span>

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a><span data-ttu-id="38ab5-321">Связывание руководства с версией маршрута</span><span class="sxs-lookup"><span data-stu-id="38ab5-321">Associate a Guide to a route version</span></span>

<span data-ttu-id="38ab5-322">Можно добавить руководство к любой [версии маршрута](routes-operations.md#route-versions).</span><span class="sxs-lookup"><span data-stu-id="38ab5-322">You can add a guide to any [route version](routes-operations.md#route-versions).</span></span>

### <a name="typical-scenario-using-route-versions"></a><span data-ttu-id="38ab5-323">Типичный сценарий использования версий маршрута</span><span class="sxs-lookup"><span data-stu-id="38ab5-323">Typical scenario using route versions</span></span>

<span data-ttu-id="38ab5-324">Версии маршрутов обычно используются для указания вариантов производственных процессов на основе существующего маршрута.</span><span class="sxs-lookup"><span data-stu-id="38ab5-324">Routes versions are typically used to specify variants of production processes based on an existing route.</span></span> <span data-ttu-id="38ab5-325">Каждой версии маршрута можно присвоить другие руководства.</span><span class="sxs-lookup"><span data-stu-id="38ab5-325">You can assign different Guides to each route version.</span></span>

### <a name="add-a-guide-to-a-route-version"></a><span data-ttu-id="38ab5-326">Добавление руководства к версии маршрута</span><span class="sxs-lookup"><span data-stu-id="38ab5-326">Add a Guide to a route version</span></span>

<span data-ttu-id="38ab5-327">Чтобы добавить руководство к версии маршрута:</span><span class="sxs-lookup"><span data-stu-id="38ab5-327">To add a Guide to a route version:</span></span>

1. <span data-ttu-id="38ab5-328">Перейдите в раздел **Управление производством \> Все маршруты**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-328">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="38ab5-329">Откройте маршрут, для которого требуется назначить руководство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-329">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="38ab5-330">На экспресс-вкладке **Версии** выберите версию, для которой необходимо назначить руководство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-330">On the **Versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="38ab5-331">На панели инструментов **Версии** выберите **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-331">On the **Versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="38ab5-332">![Открытие руководств, связанных с выбранной версией маршрута](media/instruction-guides-RouteVersion.png "Открытие руководств, связанных с выбранной версией маршрута")</span><span class="sxs-lookup"><span data-stu-id="38ab5-332">![Open the Guides associated with a selected route version](media/instruction-guides-RouteVersion.png "Open the Guides associated with a selected route version")</span></span>
1. <span data-ttu-id="38ab5-333">Для версии спецификации будет открыта страница **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-333">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="38ab5-334">Выберите **Добавить** на панели операций, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="38ab5-334">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="38ab5-335">Для новой строки воспользуйтесь раскрывающимся списком в столбце **Имя**, чтобы выбрать руководство, которое требуется назначить.</span><span class="sxs-lookup"><span data-stu-id="38ab5-335">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="38ab5-336">![Добавление руководства к версии маршрута](media/instruction-guides-RouteVersionAddGuide.png "Добавление руководства к версии маршрута")</span><span class="sxs-lookup"><span data-stu-id="38ab5-336">![Adding a Guide to a route version](media/instruction-guides-RouteVersionAddGuide.png "Adding a Guide to a route version")</span></span>

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a><span data-ttu-id="38ab5-337">Связывание руководства с отношением операций маршрута</span><span class="sxs-lookup"><span data-stu-id="38ab5-337">Associate a Guide to a route operation relation</span></span>

<span data-ttu-id="38ab5-338">Можно добавить руководство к любому [отношению операций маршрута](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="38ab5-338">You can add a guide to any [route operation relation](routes-operations.md#operation-relations).</span></span>

### <a name="typical-scenario-using-route-operation-relations"></a><span data-ttu-id="38ab5-339">Типичный сценарий с использованием отношений операций маршрута</span><span class="sxs-lookup"><span data-stu-id="38ab5-339">Typical scenario using route operation relations</span></span>

<span data-ttu-id="38ab5-340">Отношения операций — это наиболее конкретный способ добавления руководства к процессу продукта и сопутствующим операциям.</span><span class="sxs-lookup"><span data-stu-id="38ab5-340">Operation relations are the most specific way to add guidance to a product process and its related operations.</span></span> <span data-ttu-id="38ab5-341">Можно указать руководство для каждой операции в маршруте и указать другое руководство для любого типа контекста отношений, указанного для маршрута, например для конкретных номенклатур, конфигураций и т. д.</span><span class="sxs-lookup"><span data-stu-id="38ab5-341">You can specify guidance for each operation in a route and specify different guidance for any type of relation context specified for a route, such as for specific items, configurations, and more.</span></span> <span data-ttu-id="38ab5-342">Можно также указать, к каким этапам операции применяются руководства (такие как настройка, постановка в очередь, обработка или транспортировка).</span><span class="sxs-lookup"><span data-stu-id="38ab5-342">You can also specify to which stages in the operation the guidance applies (such as setup, queueing, process, or transport).</span></span>

> [!NOTE]
> <span data-ttu-id="38ab5-343">При указании руководств для нескольких отношений операций маршрута, среди этих руководств в цехе для создаваемого задания будет отображаться только руководство из наиболее конкретного отношения.</span><span class="sxs-lookup"><span data-stu-id="38ab5-343">If you specify guides for several operation relations of a route, among those guides, only the guide from the most specific relation will be show on the shop floor for the generated job.</span></span>

### <a name="add-a-guide-to-a-route-operation-relation"></a><span data-ttu-id="38ab5-344">Добавление руководства к отношению операций маршрута</span><span class="sxs-lookup"><span data-stu-id="38ab5-344">Add a Guide to a route operation relation</span></span>

<span data-ttu-id="38ab5-345">Чтобы добавить руководство к отношению операций маршрута:</span><span class="sxs-lookup"><span data-stu-id="38ab5-345">To add a Guide to a route operation relation:</span></span>

1. <span data-ttu-id="38ab5-346">Перейдите в раздел **Управление производством \> Все маршруты**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-346">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="38ab5-347">Откройте маршрут, для которого требуется назначить руководство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-347">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="38ab5-348">В области действий откройте вкладку **Маршрут** и в группе **Ведение** выберите **Сведения о маршруте**.</span><span class="sxs-lookup"><span data-stu-id="38ab5-348">On the Action Pane, open the **Route** tab and from the **Maintain** group, select **Route details**.</span></span>
1. <span data-ttu-id="38ab5-349">Будет открыта страница **Сведения о маршруте** для выбранного маршрута.</span><span class="sxs-lookup"><span data-stu-id="38ab5-349">The **Route details** page opens for your selected rout.</span></span>
1. <span data-ttu-id="38ab5-350">В верхней сетке выберите операцию, для которой необходимо предоставить руководство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-350">In the top grid, select the operation you want to provide guidance for.</span></span>
1. <span data-ttu-id="38ab5-351">В нижней сетке выберите конкретное отношение (или общее отношение **Все**).</span><span class="sxs-lookup"><span data-stu-id="38ab5-351">In the bottom grid, select a specific relation (or the generic **All** relation).</span></span>
    <span data-ttu-id="38ab5-352">![Выбор операции, затем отношения](media/instruction-guides-RouteOperationRelation.png "Выбор операции, затем отношения")</span><span class="sxs-lookup"><span data-stu-id="38ab5-352">![Select an operation and then a relation](media/instruction-guides-RouteOperationRelation.png "Select an operation and then a relation")</span></span>
1. <span data-ttu-id="38ab5-353">Над нижней сеткой откройте вкладку **Связанные руководства**. ![Вкладка "Связанные руководства"](media/instruction-guides-RouteOperationRelation-AddGuide.png "Вкладка "Связанные руководства"")</span><span class="sxs-lookup"><span data-stu-id="38ab5-353">Above the bottom gird, open the **Associated Guides** tab.  ![The Associated Guides tab](media/instruction-guides-RouteOperationRelation-AddGuide.png "The Associated Guides tab")</span></span>
1. <span data-ttu-id="38ab5-354">Выберите **Добавить** из панели инструментов в верхней части нижней сетки, чтобы добавить новую строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="38ab5-354">Select **Add** from the toolbar at the top of the bottom grid to add a new line to the grid.</span></span>
1. <span data-ttu-id="38ab5-355">Для новой строки воспользуйтесь раскрывающимся списком в столбце **Имя**, чтобы выбрать руководство, которое требуется назначить.</span><span class="sxs-lookup"><span data-stu-id="38ab5-355">For the new row, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="38ab5-356">В оставшейся части строки установите флажок для каждого контекста, в котором должно быть доступно выбранное руководство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-356">In the rest of the row, select the check box for each context where the selected Guide should be available.</span></span>

> [!NOTE]
> <span data-ttu-id="38ab5-357">Можно добавить одно или несколько руководств для каждого этапа каждой операции.</span><span class="sxs-lookup"><span data-stu-id="38ab5-357">You can add one or more guides for each stage of each operation.</span></span>

## <a name="select-guides-from-the-shop-floor-execution-interface"></a><span data-ttu-id="38ab5-358">Выбор руководств из интерфейса выполнения цеха</span><span class="sxs-lookup"><span data-stu-id="38ab5-358">Select guides from the shop floor execution interface</span></span>

<span data-ttu-id="38ab5-359">Когда работник открывает список заданий в интерфейсе выполнения цеха, Supply Chain Management находит соответствующие руководства для показанных заданий.</span><span class="sxs-lookup"><span data-stu-id="38ab5-359">When a worker opens a job list on the shop floor execution interface, Supply Chain Management finds the relevant guides for the jobs shown.</span></span> <span data-ttu-id="38ab5-360">Используйте кнопку **Руководства** для просмотра соответствующих руководств.</span><span class="sxs-lookup"><span data-stu-id="38ab5-360">Use the **Guides** button to view the relevant guides.</span></span>

<span data-ttu-id="38ab5-361">![Кнопка "Руководства" в интерфейсе выполнения цеха](media/instruction-guides-Shopfloor1.png "Кнопка "Руководства" в интерфейсе выполнения цеха")</span><span class="sxs-lookup"><span data-stu-id="38ab5-361">![Guides button in the shop floor execution interface](media/instruction-guides-Shopfloor1.png "Guides button in the shop floor execution interface")</span></span>

<span data-ttu-id="38ab5-362">Затем наденьте очки HoloLens и перейдите к соответствующему руководству, посмотрев на QR-код, чтобы активировать соответствующее руководство.</span><span class="sxs-lookup"><span data-stu-id="38ab5-362">Then put on a HoloLens and access the respective guide by glancing at the QR code and activating the respective Guide.</span></span>

<span data-ttu-id="38ab5-363">![QR-код для доступа к руководствам с помощью HoloLens](media/instruction-guides-Shopfloor2.png "QR-код для доступа к руководствам с помощью HoloLens")</span><span class="sxs-lookup"><span data-stu-id="38ab5-363">![QR code to access guides using a HoloLens](media/instruction-guides-Shopfloor2.png "QR code to access guides using a HoloLens")</span></span>

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a><span data-ttu-id="38ab5-364">Разрешение логики выбора руководств</span><span class="sxs-lookup"><span data-stu-id="38ab5-364">Resolving the logic for selecting Guides</span></span>

<span data-ttu-id="38ab5-365">Можно добавлять руководства к следующим производственным данным:</span><span class="sxs-lookup"><span data-stu-id="38ab5-365">You can add Guides to the following production data:</span></span>

- [<span data-ttu-id="38ab5-366">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="38ab5-366">Resources</span></span>](#resources)
- [<span data-ttu-id="38ab5-367">Группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="38ab5-367">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="38ab5-368">Используемые продукты</span><span class="sxs-lookup"><span data-stu-id="38ab5-368">Released products</span></span>](#released-products)
- [<span data-ttu-id="38ab5-369">Формулы</span><span class="sxs-lookup"><span data-stu-id="38ab5-369">Formulas</span></span>](#formulas)
- [<span data-ttu-id="38ab5-370">Версии формулы</span><span class="sxs-lookup"><span data-stu-id="38ab5-370">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="38ab5-371">Спецификации (BOM)</span><span class="sxs-lookup"><span data-stu-id="38ab5-371">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="38ab5-372">Версии BOM</span><span class="sxs-lookup"><span data-stu-id="38ab5-372">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="38ab5-373">Маршруты</span><span class="sxs-lookup"><span data-stu-id="38ab5-373">Routes</span></span>](#routes)
- [<span data-ttu-id="38ab5-374">Версии маршрута</span><span class="sxs-lookup"><span data-stu-id="38ab5-374">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="38ab5-375">Отношения операций маршрута</span><span class="sxs-lookup"><span data-stu-id="38ab5-375">Route operation relations</span></span>](#route-operation-relations)

<span data-ttu-id="38ab5-376">Когда Supply Chain Management создает задания для производственного цеха, оно будет собирать соответствующие руководства из этих источников.</span><span class="sxs-lookup"><span data-stu-id="38ab5-376">When Supply Chain Management generates the jobs for the production floor, it will collect the relevant Guides from those sources.</span></span> <span data-ttu-id="38ab5-377">Обратите внимание на следующие важные правила.</span><span class="sxs-lookup"><span data-stu-id="38ab5-377">Take note of the following important rules.</span></span>

- <span data-ttu-id="38ab5-378">Если присоединить версию спецификации или версию формулы к маршруту или производственному заказу, то в задании будут показаны все руководства, прикрепленные к данной версии, а также руководства, прикрепленные к родительской спецификации или формуле этой версии.</span><span class="sxs-lookup"><span data-stu-id="38ab5-378">If you attach a BOM version or formula version to a route or production order, then any Guides attached to this version, and also the Guides attached to the parent BOM or formula of that version, will be shown on the job.</span></span>
- <span data-ttu-id="38ab5-379">Если присоединить версию маршрута к производственному заказу, то в задании будут показаны все руководства, прикрепленные к данной версии, а также руководства, прикрепленные к родительскому маршруту этой версии.</span><span class="sxs-lookup"><span data-stu-id="38ab5-379">If you attach a route version to a production order, then any Guides attached to this version, and also the Guides attached to the parent route of that version, will be shown on the job.</span></span>
- <span data-ttu-id="38ab5-380">Если определить несколько отношений операций маршрута, включающих отношение *Все*, и назначить им руководства, для задания будут показаны только руководства из наиболее конкретного отношения.</span><span class="sxs-lookup"><span data-stu-id="38ab5-380">If you define several route operation relations that include the *All* relation and assign Guides to those, only the Guides from the most specific relation will be shown for the job.</span></span>  

<span data-ttu-id="38ab5-381">![Диаграмма по разрешению соответствующих руководств](media/instruction-guides-Resolve.png "Диаграмма по разрешению соответствующих руководств")</span><span class="sxs-lookup"><span data-stu-id="38ab5-381">![Diagram on resolving the relevant Guides](media/instruction-guides-Resolve.png "Diagram on resolving the relevant Guides")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]