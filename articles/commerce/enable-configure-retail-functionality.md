---
title: Инициализация начальных данных в новых средах Commerce
description: В этой статье описываются данные, создаваемые в процессе инициализации для Dynamics 365 Commerce.
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
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8fd0b2743deab758538922f312853b622a512c0a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000753"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a><span data-ttu-id="d2e9e-103">Инициализация начальных данных в новых средах Commerce</span><span class="sxs-lookup"><span data-stu-id="d2e9e-103">Initialize seed data in new Commerce environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d2e9e-104">В этой статье описываются данные, создаваемые в процессе инициализации для Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d2e9e-105">После развертывания решения Commerce посредством Microsoft Dynamics Lifecycle Services (LCS) необходимо инициализировать конфигурацию Commerce, чтобы создать базовые данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d2e9e-106">Прежде чем инициализировать конфигурацию Commerce, убедитесь, что вы указали язык и почтовый адрес для каждого юридического лица, в котором вы будете настраивать магазины.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="d2e9e-107">Этот шаг необходимо выполнить для каждого юридического лица, которое вы используете для Commerce.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="d2e9e-108">Чтобы инициализировать конфигурацию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="d2e9e-109">Запустите клиент Commerce.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="d2e9e-110">Перейдите в раздел **Retail и Commerce** &gt; **Настройка Headquarters** &gt; **Параметры** &gt; **Параметры Commerce**.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="d2e9e-111">Щелкните **Инициализировать**.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-111">Click **Initialize**.</span></span>

<span data-ttu-id="d2e9e-112">В результате инициализации создаются следующие данные конфигурации по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="d2e9e-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="d2e9e-113">Задания и подзадания планировщика Commerce</span><span class="sxs-lookup"><span data-stu-id="d2e9e-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="d2e9e-114">Схема канала коммерции</span><span class="sxs-lookup"><span data-stu-id="d2e9e-114">Commerce channel schema</span></span>
- <span data-ttu-id="d2e9e-115">Графики распределения Commerce</span><span class="sxs-lookup"><span data-stu-id="d2e9e-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="d2e9e-116">Макеты экранов по умолчанию, которые включают в себя сетки кнопок, изображения и темы</span><span class="sxs-lookup"><span data-stu-id="d2e9e-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="d2e9e-117">Информация о часовом поясе</span><span class="sxs-lookup"><span data-stu-id="d2e9e-117">Time zone information</span></span>
- <span data-ttu-id="d2e9e-118">POS-операции</span><span class="sxs-lookup"><span data-stu-id="d2e9e-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="d2e9e-119">POS-разрешения</span><span class="sxs-lookup"><span data-stu-id="d2e9e-119">POS permissions</span></span>
- <span data-ttu-id="d2e9e-120">Отчеты по каналу</span><span class="sxs-lookup"><span data-stu-id="d2e9e-120">Channel reports</span></span>
- <span data-ttu-id="d2e9e-121">Метаданные атрибута</span><span class="sxs-lookup"><span data-stu-id="d2e9e-121">Attribute metadata</span></span>
- <span data-ttu-id="d2e9e-122">Шаблоны проверки объектов</span><span class="sxs-lookup"><span data-stu-id="d2e9e-122">Entity validation templates</span></span>
- <span data-ttu-id="d2e9e-123">Пакетное задание для очистки истории сессии Commerce Data Exchange</span><span class="sxs-lookup"><span data-stu-id="d2e9e-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="d2e9e-124">Кроме того, для базы данных Commerce включается ведение журналов, связанных с платежными картами (PCI).</span><span class="sxs-lookup"><span data-stu-id="d2e9e-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="d2e9e-125">Также предусмотрен параметр, позволяющий отдельно сконфигурировать планировщик Commerce.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="d2e9e-126">Этот параметр позволяет сбросить конфигурацию планировщика Commerce к его настройкам по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="d2e9e-127">После завершения инициализации необходимо сконфигурировать дополнительные данные Commerce.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="d2e9e-128">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="d2e9e-128">Here are some examples:</span></span>

- <span data-ttu-id="d2e9e-129">Параметры коммерции</span><span class="sxs-lookup"><span data-stu-id="d2e9e-129">Commerce parameters</span></span>
- <span data-ttu-id="d2e9e-130">Параметры планировщика коммерции</span><span class="sxs-lookup"><span data-stu-id="d2e9e-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="d2e9e-131">Каналы Commerce</span><span class="sxs-lookup"><span data-stu-id="d2e9e-131">Commerce channels</span></span>
- <span data-ttu-id="d2e9e-132">Регистры и устройства</span><span class="sxs-lookup"><span data-stu-id="d2e9e-132">Registers and devices</span></span>
- <span data-ttu-id="d2e9e-133">Ассортименты</span><span class="sxs-lookup"><span data-stu-id="d2e9e-133">Assortments</span></span>
