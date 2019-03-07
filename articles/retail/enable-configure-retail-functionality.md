---
title: Инициализация начальных данных в новых средах Retail
description: В этой статье описываются данные, создаваемые в процессе инициализации для Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 52f0c52748958f0bebb6c40df01cfac10c0ed427
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "327903"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="49ca8-103">Инициализация начальных данных в новых средах Retail</span><span class="sxs-lookup"><span data-stu-id="49ca8-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="49ca8-104">В этой статье описываются данные, создаваемые в процессе инициализации для Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="49ca8-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="49ca8-105">После развертывания решения "Розничная торговля" посредством Microsoft Dynamics Lifecycle Services (LCS) необходимо инициализировать конфигурацию розничной торговли, чтобы создать базовые данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="49ca8-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49ca8-106">Прежде чем инициализировать конфигурацию розничной торговли, убедитесь, что вы указали язык и почтовый адрес для каждого юридического лица, в котором вы будете настраивать розничные магазины.</span><span class="sxs-lookup"><span data-stu-id="49ca8-106">Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="49ca8-107">Этот шаг необходимо выполнить для каждого юридического лица, которое вы используете для розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="49ca8-107">This step must be completed for each legal entity that you use for retail.</span></span>

<span data-ttu-id="49ca8-108">Чтобы инициализировать конфигурацию розничной торговли, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="49ca8-108">To initialize the retail configuration, follow these steps.</span></span>

1. <span data-ttu-id="49ca8-109">Запустите клиент Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="49ca8-109">Start the Dynamics 365 for Retail client.</span></span>
2. <span data-ttu-id="49ca8-110">Выберите **Розничная торговля** &gt; **Настройка центрального офиса** &gt; **Параметры** &gt; **Параметры розничной торговли**.</span><span class="sxs-lookup"><span data-stu-id="49ca8-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3. <span data-ttu-id="49ca8-111">Щелкните **Инициализировать**.</span><span class="sxs-lookup"><span data-stu-id="49ca8-111">Click **Initialize**.</span></span>

<span data-ttu-id="49ca8-112">В результате инициализации создаются следующие данные конфигурации по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="49ca8-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="49ca8-113">Задания и подзадания планировщика розничной торговли</span><span class="sxs-lookup"><span data-stu-id="49ca8-113">Retail scheduler jobs and subjobs</span></span>
- <span data-ttu-id="49ca8-114">Схема канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="49ca8-114">Retail channel schema</span></span>
- <span data-ttu-id="49ca8-115">Графики распределения розничной торговли</span><span class="sxs-lookup"><span data-stu-id="49ca8-115">Retail distribution schedules</span></span>
- <span data-ttu-id="49ca8-116">Макеты экранов по умолчанию, которые включают в себя сетки кнопок, изображения и темы</span><span class="sxs-lookup"><span data-stu-id="49ca8-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="49ca8-117">Информация о часовом поясе</span><span class="sxs-lookup"><span data-stu-id="49ca8-117">Time zone information</span></span>
- <span data-ttu-id="49ca8-118">POS-операции</span><span class="sxs-lookup"><span data-stu-id="49ca8-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="49ca8-119">POS-разрешения</span><span class="sxs-lookup"><span data-stu-id="49ca8-119">POS permissions</span></span>
- <span data-ttu-id="49ca8-120">Отчеты по каналу</span><span class="sxs-lookup"><span data-stu-id="49ca8-120">Channel reports</span></span>
- <span data-ttu-id="49ca8-121">Метаданные атрибута</span><span class="sxs-lookup"><span data-stu-id="49ca8-121">Attribute metadata</span></span>
- <span data-ttu-id="49ca8-122">Шаблоны проверки объектов</span><span class="sxs-lookup"><span data-stu-id="49ca8-122">Entity validation templates</span></span>
- <span data-ttu-id="49ca8-123">Пакетное задание для очистки истории сессии Commerce Data Exchange</span><span class="sxs-lookup"><span data-stu-id="49ca8-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="49ca8-124">Кроме того, для базы данных Dynamics 365 for Retail включается ведение журналов, связанных с платежными картами (PCI).</span><span class="sxs-lookup"><span data-stu-id="49ca8-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span>

> [!NOTE]
> <span data-ttu-id="49ca8-125">Также предусмотрен параметр, позволяющий отдельно сконфигурировать планировщик розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="49ca8-125">There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="49ca8-126">Этот параметр позволяет сбросить конфигурацию планировщика розничной торговли к его настройкам по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="49ca8-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span>

<span data-ttu-id="49ca8-127">После завершения инициализации необходимо сконфигурировать дополнительные данные розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="49ca8-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="49ca8-128">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="49ca8-128">Here are some examples:</span></span>

- <span data-ttu-id="49ca8-129">Параметры розничной торговли</span><span class="sxs-lookup"><span data-stu-id="49ca8-129">Retail parameters</span></span>
- <span data-ttu-id="49ca8-130">Параметры модуля "Розничная сеть - Планировщик"</span><span class="sxs-lookup"><span data-stu-id="49ca8-130">Retail scheduler parameters</span></span>
- <span data-ttu-id="49ca8-131">Каналы розничной торговли</span><span class="sxs-lookup"><span data-stu-id="49ca8-131">Retail channels</span></span>
- <span data-ttu-id="49ca8-132">Регистры и устройства</span><span class="sxs-lookup"><span data-stu-id="49ca8-132">Registers and devices</span></span>
- <span data-ttu-id="49ca8-133">Ассортименты</span><span class="sxs-lookup"><span data-stu-id="49ca8-133">Assortments</span></span>
