---
title: Переключение между вариантами дизайна поставщиков
description: Эта тема описывает способ переключения интеграции данных поставщиков между приложениями Finance and Operations и Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 5a18fed2eac4c120dca20a1d7797d047639275b9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750602"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="dc61a-103">Переключение между вариантами дизайна поставщиков</span><span class="sxs-lookup"><span data-stu-id="dc61a-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="dc61a-104">Поток данных поставщика</span><span class="sxs-lookup"><span data-stu-id="dc61a-104">Vendor data flow</span></span> 

<span data-ttu-id="dc61a-105">Если выбрано использование таблицы **Организация** для хранения поставщиков типа **Организация** и таблицы **Контакт** для хранения поставщиков типа **Физическое лицо**, настройте следующие рабочие процессы.</span><span class="sxs-lookup"><span data-stu-id="dc61a-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="dc61a-106">В противном случае такая конфигурация не требуется.</span><span class="sxs-lookup"><span data-stu-id="dc61a-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="dc61a-107">Использование расширенного дизайна поставщиков для поставщиков типа "Организация"</span><span class="sxs-lookup"><span data-stu-id="dc61a-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="dc61a-108">Пакет решения **Dynamics365FinanceExtended** содержит следующие шаблоны рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="dc61a-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="dc61a-109">Будет создан рабочий процесс для каждого шаблона.</span><span class="sxs-lookup"><span data-stu-id="dc61a-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="dc61a-110">Создание поставщиков в таблице "Организации"</span><span class="sxs-lookup"><span data-stu-id="dc61a-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="dc61a-111">Создание поставщиков в таблице "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="dc61a-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="dc61a-112">Обновление поставщиков в таблице "Организации"</span><span class="sxs-lookup"><span data-stu-id="dc61a-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="dc61a-113">Обновление поставщиков в таблице "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="dc61a-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="dc61a-114">Чтобы создать новые рабочие процессы с помощью шаблонов рабочих процессов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dc61a-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="dc61a-115">Создайте рабочий процесс для таблицы **Поставщик** и выберите шаблон рабочих процессов **Создание поставщиков в таблице "Организации"**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="dc61a-116">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-116">Then select **OK**.</span></span> <span data-ttu-id="dc61a-117">Этот workflow-процесс обрабатывает сценарий создания поставщиков для таблицы **Организация**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![Рабочий процесс создания поставщиков в таблице "Организации"](media/create_process.png)

2. <span data-ttu-id="dc61a-119">Создайте рабочий процесс для таблицы **Поставщик** и выберите шаблон рабочих процессов **Обновление поставщиков в таблице "Организации"**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="dc61a-120">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-120">Then select **OK**.</span></span> <span data-ttu-id="dc61a-121">Этот workflow-процесс обрабатывает сценарий обновления поставщиков для таблицы **Организация**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="dc61a-122">Создайте рабочий процесс для таблицы **Организация** и выберите шаблон рабочих процессов **Создание поставщиков в таблице поставщиков**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="dc61a-123">Создайте рабочий процесс для таблицы **Организация** и выберите шаблон рабочих процессов **Обновление поставщиков в таблице поставщиков**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="dc61a-124">Рабочие процессы можно настроить как рабочие процессы в реальном времени или в фоновом режиме, в зависимости от требований пользователя.</span><span class="sxs-lookup"><span data-stu-id="dc61a-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="dc61a-125">Чтобы настроить рабочий процесс в качестве фонового рабочего процесса, выберите **Преобразовать в фоновый рабочий процесс**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Кнопка преобразования в фоновый рабочий процесс](media/background_workflow.png)

6. <span data-ttu-id="dc61a-127">Активируйте рабочие процессы, созданные для таблиц **Организация** и **Поставщик**, чтобы начать использовать таблицу **Организация** для хранения информации о поставщиках типа **Организация**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="dc61a-128">Использование расширенного дизайна поставщиков для поставщиков типа "Физическое лицо"</span><span class="sxs-lookup"><span data-stu-id="dc61a-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="dc61a-129">Пакет решения **Dynamics365FinanceExtended** содержит следующие шаблоны рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="dc61a-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="dc61a-130">Будет создан рабочий процесс для каждого шаблона.</span><span class="sxs-lookup"><span data-stu-id="dc61a-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="dc61a-131">Создание поставщиков типа "Физическое лицо" в таблице "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="dc61a-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="dc61a-132">Создание поставщиков типа "Физическое лицо" в таблице "Контакты"</span><span class="sxs-lookup"><span data-stu-id="dc61a-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="dc61a-133">Обновление поставщиков типа "Физическое лицо" в таблице "Контакты"</span><span class="sxs-lookup"><span data-stu-id="dc61a-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="dc61a-134">Обновление поставщиков типа "Физическое лицо" в таблице "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="dc61a-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="dc61a-135">Чтобы создать новые рабочие процессы с помощью шаблонов рабочих процессов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dc61a-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="dc61a-136">Создайте рабочий процесс для таблицы **Поставщик** и выберите шаблон рабочих процессов **Создание поставщиков типа "Физическое лицо" в таблице "Контакты"**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="dc61a-137">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-137">Then select **OK**.</span></span> <span data-ttu-id="dc61a-138">Этот workflow-процесс обрабатывает сценарий создания поставщиков для таблицы **Контакты**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="dc61a-139">Создайте рабочий процесс для таблицы **Поставщик** и выберите шаблон рабочих процессов **Обновление поставщиков типа "Физическое лицо" в таблице "Контакты"**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="dc61a-140">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-140">Then select **OK**.</span></span> <span data-ttu-id="dc61a-141">Этот workflow-процесс обрабатывает сценарий обновления поставщиков для таблицы **Контакт**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="dc61a-142">Создайте рабочий процесс для таблицы **Контакт** и выберите шаблон рабочих процессов **Создание поставщиков типа "Физическое лицо" в таблице "Поставщики"**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="dc61a-143">Создайте рабочий процесс для таблицы **Контакт** и выберите шаблон рабочих процессов **Обновление поставщиков типа "Физическое лицо" в таблице "Поставщики"**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="dc61a-144">Рабочие процессы можно настроить как рабочие процессы в реальном времени или в фоновом режиме, в зависимости от требований пользователя.</span><span class="sxs-lookup"><span data-stu-id="dc61a-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="dc61a-145">Чтобы настроить рабочий процесс в качестве фонового рабочего процесса, выберите **Преобразовать в фоновый рабочий процесс**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="dc61a-146">Активируйте рабочие процессы, созданные для таблиц **Контакт** и **Поставщик**, чтобы начать использовать таблицу **Контакт** для хранения информации о поставщиках типа **Физическое лицо**.</span><span class="sxs-lookup"><span data-stu-id="dc61a-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]