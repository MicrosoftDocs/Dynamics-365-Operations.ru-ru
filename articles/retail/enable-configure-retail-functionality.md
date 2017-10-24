---
title: "Инициализация начальных данных в новой среде розничной торговли"
description: "В этой статье описываются данные, создаваемые в процессе инициализации для Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ac4f651cd7e5df912ea2535eafd5e54c11377253
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a><span data-ttu-id="ec944-103">Инициализация начальных данных в новой среде розничной торговли</span><span class="sxs-lookup"><span data-stu-id="ec944-103">Initialize seed data in a new Retail environment</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="ec944-104">В этой статье описываются данные, создаваемые в процессе инициализации для Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="ec944-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="ec944-105">После развертывания решения "Розничная торговля" посредством Microsoft Dynamics Lifecycle Services (LCS) необходимо инициализировать конфигурацию розничной торговли, чтобы создать базовые данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ec944-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span> <span data-ttu-id="ec944-106">**Важно:** прежде чем инициализировать конфигурацию розничной торговли, убедитесь, что вы указали язык и почтовый адрес для каждого юридического лица, в котором вы будете настраивать розничные магазины.</span><span class="sxs-lookup"><span data-stu-id="ec944-106">**Important:** Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="ec944-107">Этот шаг необходимо выполнить для каждого юридического лица, которое вы используете для розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="ec944-107">This step must be completed for each legal entity that you use for retail.</span></span> <span data-ttu-id="ec944-108">Чтобы инициализировать конфигурацию розничной торговли, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ec944-108">To initialize the retail configuration, follow these steps.</span></span>

1.  <span data-ttu-id="ec944-109">Запустите клиент Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="ec944-109">Start the Dynamics 365 for Retail client.</span></span>
2.  <span data-ttu-id="ec944-110">Выберите **Розничная торговля** &gt; **Настройка центрального офиса** &gt; **Параметры** &gt; **Параметры розничной торговли**.</span><span class="sxs-lookup"><span data-stu-id="ec944-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3.  <span data-ttu-id="ec944-111">Щелкните **Инициализировать**.</span><span class="sxs-lookup"><span data-stu-id="ec944-111">Click **Initialize**.</span></span>

<span data-ttu-id="ec944-112">В результате инициализации создаются следующие данные конфигурации по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="ec944-112">Initialization creates the following default configuration data:</span></span>

-   <span data-ttu-id="ec944-113">Задания и подзадания планировщика розничной торговли</span><span class="sxs-lookup"><span data-stu-id="ec944-113">Retail scheduler jobs and subjobs</span></span>
-   <span data-ttu-id="ec944-114">Схема канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="ec944-114">Retail channel schema</span></span>
-   <span data-ttu-id="ec944-115">Графики распределения розничной торговли</span><span class="sxs-lookup"><span data-stu-id="ec944-115">Retail distribution schedules</span></span>
-   <span data-ttu-id="ec944-116">Макеты экранов по умолчанию, которые включают в себя сетки кнопок, изображения и темы</span><span class="sxs-lookup"><span data-stu-id="ec944-116">Default screen layouts, which include button grids, images, and themes</span></span>
-   <span data-ttu-id="ec944-117">Информация о часовом поясе</span><span class="sxs-lookup"><span data-stu-id="ec944-117">Time zone information</span></span>
-   <span data-ttu-id="ec944-118">POS-операции</span><span class="sxs-lookup"><span data-stu-id="ec944-118">Point-of-sale (POS) operations</span></span>
-   <span data-ttu-id="ec944-119">POS-разрешения</span><span class="sxs-lookup"><span data-stu-id="ec944-119">POS permissions</span></span>
-   <span data-ttu-id="ec944-120">Отчеты по каналу</span><span class="sxs-lookup"><span data-stu-id="ec944-120">Channel reports</span></span>
-   <span data-ttu-id="ec944-121">Метаданные атрибута</span><span class="sxs-lookup"><span data-stu-id="ec944-121">Attribute metadata</span></span>
-   <span data-ttu-id="ec944-122">Шаблоны проверки объектов</span><span class="sxs-lookup"><span data-stu-id="ec944-122">Entity validation templates</span></span>
-   <span data-ttu-id="ec944-123">Пакетное задание для очистки истории сессии Commerce Data Exchange</span><span class="sxs-lookup"><span data-stu-id="ec944-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="ec944-124">Кроме того, для базы данных Dynamics 365 for Retail включается ведение журналов, связанных с платежными картами (PCI).</span><span class="sxs-lookup"><span data-stu-id="ec944-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span> <span data-ttu-id="ec944-125">**Примечание.** Также предусмотрен параметр, позволяющий отдельно сконфигурировать планировщик розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="ec944-125">**Note:** There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="ec944-126">Этот параметр позволяет сбросить конфигурацию планировщика розничной торговли к его настройкам по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ec944-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span> <span data-ttu-id="ec944-127">После завершения инициализации необходимо сконфигурировать дополнительные данные розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="ec944-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="ec944-128">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="ec944-128">Here are some examples:</span></span>

-   <span data-ttu-id="ec944-129">Параметры розничной торговли</span><span class="sxs-lookup"><span data-stu-id="ec944-129">Retail parameters</span></span>
-   <span data-ttu-id="ec944-130">Параметры модуля "Розничная сеть - Планировщик"</span><span class="sxs-lookup"><span data-stu-id="ec944-130">Retail scheduler parameters</span></span>
-   <span data-ttu-id="ec944-131">Каналы розничной торговли</span><span class="sxs-lookup"><span data-stu-id="ec944-131">Retail channels</span></span>
-   <span data-ttu-id="ec944-132">Регистры и устройства</span><span class="sxs-lookup"><span data-stu-id="ec944-132">Registers and devices</span></span>
-   <span data-ttu-id="ec944-133">Ассортименты</span><span class="sxs-lookup"><span data-stu-id="ec944-133">Assortments</span></span>





