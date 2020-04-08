---
title: Переключение между вариантами дизайна поставщиков
description: Эта тема описывает способ переключения интеграции данных поставщиков между приложениями Finance and Operations и Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: ffd7a4c01810578b4abb6942aeff76e5147fafa9
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173047"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="0b0a8-103">Переключение между вариантами дизайна поставщиков</span><span class="sxs-lookup"><span data-stu-id="0b0a8-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="0b0a8-104">Поток данных поставщика</span><span class="sxs-lookup"><span data-stu-id="0b0a8-104">Vendor data flow</span></span> 

<span data-ttu-id="0b0a8-105">Если выбрано использование объекта **Организация** для хранения поставщиков типа **Организация** и объекта **Контакт** для хранения поставщиков типа **Физическое лицо**, настройте следующие рабочие процессы.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="0b0a8-106">В противном случае такая конфигурация не требуется.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="0b0a8-107">Использование расширенного дизайна поставщиков для поставщиков типа "Организация"</span><span class="sxs-lookup"><span data-stu-id="0b0a8-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="0b0a8-108">Пакет решения **Dynamics365FinanceExtended** содержит следующие шаблоны рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="0b0a8-109">Будет создан рабочий процесс для каждого шаблона.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="0b0a8-110">Создание поставщиков в объекте "Организации"</span><span class="sxs-lookup"><span data-stu-id="0b0a8-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="0b0a8-111">Создание поставщиков в объекте "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="0b0a8-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="0b0a8-112">Обновление поставщиков в объекте "Организации"</span><span class="sxs-lookup"><span data-stu-id="0b0a8-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="0b0a8-113">Обновление поставщиков в объекте "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="0b0a8-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="0b0a8-114">Чтобы создать новые рабочие процессы с помощью шаблонов рабочих процессов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="0b0a8-115">Создайте рабочий процесс для объекта **Поставщик** и выберите шаблон рабочих процессов **Создание поставщиков в объекте "Организации"**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="0b0a8-116">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-116">Then select **OK**.</span></span> <span data-ttu-id="0b0a8-117">Этот workflow-процесс обрабатывает сценарий создания поставщиков для объекта **Организация**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Рабочий процесс создания поставщиков в объекте "Организации"](media/create_process.png)

2. <span data-ttu-id="0b0a8-119">Создайте рабочий процесс для объекта **Поставщик** и выберите шаблон рабочих процессов **Обновление поставщиков в объекте "Организации"**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="0b0a8-120">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-120">Then select **OK**.</span></span> <span data-ttu-id="0b0a8-121">Этот workflow-процесс обрабатывает сценарий обновления поставщиков для объекта **Организация**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="0b0a8-122">Создайте рабочий процесс для объекта **Организация** и выберите шаблон рабочих процессов **Создание поставщиков в объекте "Поставщики"**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="0b0a8-123">Создайте рабочий процесс для объекта **Организация** и выберите шаблон рабочих процессов **Обновление поставщиков в объекте "Поставщики"**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="0b0a8-124">Рабочие процессы можно настроить как рабочие процессы в реальном времени или в фоновом режиме, в зависимости от требований пользователя.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="0b0a8-125">Чтобы настроить рабочий процесс в качестве фонового рабочего процесса, выберите **Преобразовать в фоновый рабочий процесс**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Кнопка преобразования в фоновый рабочий процесс](media/background_workflow.png)

6. <span data-ttu-id="0b0a8-127">Активируйте рабочие процессы, созданные для объектов **Организация** и **Поставщик**, чтобы начать использовать объект **Организация** для хранения информации о поставщиках типа **Организация**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="0b0a8-128">Использование расширенного дизайна поставщиков для поставщиков типа "Физическое лицо"</span><span class="sxs-lookup"><span data-stu-id="0b0a8-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="0b0a8-129">Пакет решения **Dynamics365FinanceExtended** содержит следующие шаблоны рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="0b0a8-130">Будет создан рабочий процесс для каждого шаблона.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="0b0a8-131">Создание поставщиков типа "Физическое лицо" в объекте "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="0b0a8-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="0b0a8-132">Создание поставщиков типа "Физическое лицо" в объекте "Контакты"</span><span class="sxs-lookup"><span data-stu-id="0b0a8-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="0b0a8-133">Обновление поставщиков типа "Физическое лицо" в объекте "Контакты"</span><span class="sxs-lookup"><span data-stu-id="0b0a8-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="0b0a8-134">Обновление поставщиков типа "Физическое лицо" в объекте "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="0b0a8-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="0b0a8-135">Чтобы создать новые рабочие процессы с помощью шаблонов рабочих процессов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="0b0a8-136">Создайте рабочий процесс для объекта **Поставщик** и выберите шаблон рабочих процессов **Создание поставщиков типа "Физическое лицо" в объекте "Контакты"**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="0b0a8-137">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-137">Then select **OK**.</span></span> <span data-ttu-id="0b0a8-138">Этот workflow-процесс обрабатывает сценарий создания поставщиков для объекта **Контакты**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="0b0a8-139">Создайте рабочий процесс для объекта **Поставщик** и выберите шаблон рабочих процессов **Обновление поставщиков типа "Физическое лицо" в объекте "Контакты"**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="0b0a8-140">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-140">Then select **OK**.</span></span> <span data-ttu-id="0b0a8-141">Этот workflow-процесс обрабатывает сценарий обновления поставщиков для объекта **Контакт**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="0b0a8-142">Создайте рабочий процесс для объекта **Контакт** и выберите шаблон рабочих процессов **Создание поставщиков типа "Физическое лицо" в объекте "Поставщики"**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="0b0a8-143">Создайте рабочий процесс для объекта **Контакт** и выберите шаблон рабочих процессов **Обновление поставщиков типа "Физическое лицо" в объекте "Поставщики"**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="0b0a8-144">Рабочие процессы можно настроить как рабочие процессы в реальном времени или в фоновом режиме, в зависимости от требований пользователя.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="0b0a8-145">Чтобы настроить рабочий процесс в качестве фонового рабочего процесса, выберите **Преобразовать в фоновый рабочий процесс**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="0b0a8-146">Активируйте рабочие процессы, созданные для объектов **Контакт** и **Поставщик**, чтобы начать использовать объект **Контакт** для хранения информации о поставщиках типа **Физическое лицо**.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
