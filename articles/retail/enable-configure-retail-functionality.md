---
title: "Инициализация начальных данных в новых средах Retail"
description: "В этой статье описываются данные, создаваемые в процессе инициализации для Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 80fa443fc235496a111a8a866d2e703202721268
ms.contentlocale: ru-ru
ms.lasthandoff: 08/09/2018

---

# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="0b5bc-103">Инициализация начальных данных в новых средах Retail</span><span class="sxs-lookup"><span data-stu-id="0b5bc-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0b5bc-104">В этой статье описываются данные, создаваемые в процессе инициализации для Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="0b5bc-105">После развертывания решения "Розничная торговля" посредством Microsoft Dynamics Lifecycle Services (LCS) необходимо инициализировать конфигурацию розничной торговли, чтобы создать базовые данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span> <span data-ttu-id="0b5bc-106">**Важно:** прежде чем инициализировать конфигурацию розничной торговли, убедитесь, что вы указали язык и почтовый адрес для каждого юридического лица, в котором вы будете настраивать розничные магазины.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-106">**Important:** Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="0b5bc-107">Этот шаг необходимо выполнить для каждого юридического лица, которое вы используете для розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-107">This step must be completed for each legal entity that you use for retail.</span></span> <span data-ttu-id="0b5bc-108">Чтобы инициализировать конфигурацию розничной торговли, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-108">To initialize the retail configuration, follow these steps.</span></span>

1.  <span data-ttu-id="0b5bc-109">Запустите клиент Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-109">Start the Dynamics 365 for Retail client.</span></span>
2.  <span data-ttu-id="0b5bc-110">Выберите **Розничная торговля** &gt; **Настройка центрального офиса** &gt; **Параметры** &gt; **Параметры розничной торговли**.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3.  <span data-ttu-id="0b5bc-111">Щелкните **Инициализировать**.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-111">Click **Initialize**.</span></span>

<span data-ttu-id="0b5bc-112">В результате инициализации создаются следующие данные конфигурации по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="0b5bc-112">Initialization creates the following default configuration data:</span></span>

-   <span data-ttu-id="0b5bc-113">Задания и подзадания планировщика розничной торговли</span><span class="sxs-lookup"><span data-stu-id="0b5bc-113">Retail scheduler jobs and subjobs</span></span>
-   <span data-ttu-id="0b5bc-114">Схема канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="0b5bc-114">Retail channel schema</span></span>
-   <span data-ttu-id="0b5bc-115">Графики распределения розничной торговли</span><span class="sxs-lookup"><span data-stu-id="0b5bc-115">Retail distribution schedules</span></span>
-   <span data-ttu-id="0b5bc-116">Макеты экранов по умолчанию, которые включают в себя сетки кнопок, изображения и темы</span><span class="sxs-lookup"><span data-stu-id="0b5bc-116">Default screen layouts, which include button grids, images, and themes</span></span>
-   <span data-ttu-id="0b5bc-117">Информация о часовом поясе</span><span class="sxs-lookup"><span data-stu-id="0b5bc-117">Time zone information</span></span>
-   <span data-ttu-id="0b5bc-118">POS-операции</span><span class="sxs-lookup"><span data-stu-id="0b5bc-118">Point-of-sale (POS) operations</span></span>
-   <span data-ttu-id="0b5bc-119">POS-разрешения</span><span class="sxs-lookup"><span data-stu-id="0b5bc-119">POS permissions</span></span>
-   <span data-ttu-id="0b5bc-120">Отчеты по каналу</span><span class="sxs-lookup"><span data-stu-id="0b5bc-120">Channel reports</span></span>
-   <span data-ttu-id="0b5bc-121">Метаданные атрибута</span><span class="sxs-lookup"><span data-stu-id="0b5bc-121">Attribute metadata</span></span>
-   <span data-ttu-id="0b5bc-122">Шаблоны проверки объектов</span><span class="sxs-lookup"><span data-stu-id="0b5bc-122">Entity validation templates</span></span>
-   <span data-ttu-id="0b5bc-123">Пакетное задание для очистки истории сессии Commerce Data Exchange</span><span class="sxs-lookup"><span data-stu-id="0b5bc-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="0b5bc-124">Кроме того, для базы данных Dynamics 365 for Retail включается ведение журналов, связанных с платежными картами (PCI).</span><span class="sxs-lookup"><span data-stu-id="0b5bc-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span> <span data-ttu-id="0b5bc-125">**Примечание.** Также предусмотрен параметр, позволяющий отдельно сконфигурировать планировщик розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-125">**Note:** There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="0b5bc-126">Этот параметр позволяет сбросить конфигурацию планировщика розничной торговли к его настройкам по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span> <span data-ttu-id="0b5bc-127">После завершения инициализации необходимо сконфигурировать дополнительные данные розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="0b5bc-128">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-128">Here are some examples:</span></span>

-   <span data-ttu-id="0b5bc-129">Параметры розничной торговли</span><span class="sxs-lookup"><span data-stu-id="0b5bc-129">Retail parameters</span></span>
-   <span data-ttu-id="0b5bc-130">Параметры модуля "Розничная сеть - Планировщик"</span><span class="sxs-lookup"><span data-stu-id="0b5bc-130">Retail scheduler parameters</span></span>
-   <span data-ttu-id="0b5bc-131">Каналы розничной торговли</span><span class="sxs-lookup"><span data-stu-id="0b5bc-131">Retail channels</span></span>
-   <span data-ttu-id="0b5bc-132">Регистры и устройства</span><span class="sxs-lookup"><span data-stu-id="0b5bc-132">Registers and devices</span></span>
-   <span data-ttu-id="0b5bc-133">Ассортименты</span><span class="sxs-lookup"><span data-stu-id="0b5bc-133">Assortments</span></span>





