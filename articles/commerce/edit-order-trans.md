---
title: Редактирование и аудит проводок интернет-заказов и асинхронных проводок заказов клиентов
description: В этой теме описывается редактирование и аудит интернет-заказов и асинхронных проводок заказов клиентов в Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8fa6f7a71bae759e2b8feb3c5778200bb7bdbfe9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010159"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="32c97-103">Редактирование и аудит проводок интернет-заказов и асинхронных проводок заказов клиентов</span><span class="sxs-lookup"><span data-stu-id="32c97-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32c97-104">В этой теме описывается редактирование и аудит интернет-заказов и асинхронных проводок заказов клиентов в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="32c97-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="32c97-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="32c97-105">Overview</span></span>

<span data-ttu-id="32c97-106">В версиях Commerce с 10.0.5 по 10.0.6 добавлена поддержка редактирования кассовых проводок (таких как продажи и возвраты) и проводок управления кассами (таких как внесение и изъятие денежных средств).</span><span class="sxs-lookup"><span data-stu-id="32c97-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="32c97-107">В Commerce версии 10.0.7 добавлена поддержка редактирования проводок интернет-заказов и асинхронных проводок заказов клиентов.</span><span class="sxs-lookup"><span data-stu-id="32c97-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="32c97-108">Редактирование и аудит проводок заказов</span><span class="sxs-lookup"><span data-stu-id="32c97-108">Edit and audit order transactions</span></span>

<span data-ttu-id="32c97-109">Для изменения и аудита проводок в Commerce Headquarters выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="32c97-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="32c97-110">Установите [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span><span class="sxs-lookup"><span data-stu-id="32c97-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="32c97-111">На странице **Параметры розничной торговли** на вкладке **Клиентские заказы** на экспресс-вкладке **Заказ** укажите код удержания для параметра **Код удержания для ошибок синхронизации заказов**.</span><span class="sxs-lookup"><span data-stu-id="32c97-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="32c97-112">Откройте рабочую область **Финансовая информация магазина**.</span><span class="sxs-lookup"><span data-stu-id="32c97-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="32c97-113">Плитки **Ошибки синхронизации интернет-заказов** и **Ошибки синхронизации заказов клиентов** содержат предварительно отфильтрованное представление страницы проводок розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="32c97-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="32c97-114">На каждой плитке отображаются записи проводок, которые не удалось синхронизировать для соответствующего типа заказа.</span><span class="sxs-lookup"><span data-stu-id="32c97-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="32c97-115">Откройте страницу **Ошибки синхронизации интернет-заказов** или страницу **Ошибки синхронизации заказов клиентов**.</span><span class="sxs-lookup"><span data-stu-id="32c97-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="32c97-116">Выберите запись для просмотра сведений об ошибках синхронизации.</span><span class="sxs-lookup"><span data-stu-id="32c97-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="32c97-117">На экспресс-вкладке **Статус синхронизации** предоставляются следующие сведения об ошибках:</span><span class="sxs-lookup"><span data-stu-id="32c97-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="32c97-118">Статус заказа, ожидающего обработки</span><span class="sxs-lookup"><span data-stu-id="32c97-118">Pending order status</span></span>
    - <span data-ttu-id="32c97-119">Сведения об ошибке заказа</span><span class="sxs-lookup"><span data-stu-id="32c97-119">Order error details</span></span>
    - <span data-ttu-id="32c97-120">Дата и время изменения</span><span class="sxs-lookup"><span data-stu-id="32c97-120">Modified date and time</span></span>
    - <span data-ttu-id="32c97-121">Счетчик повторов</span><span class="sxs-lookup"><span data-stu-id="32c97-121">Retry count</span></span>

1. <span data-ttu-id="32c97-122">Если в сведениях об ошибке указывается, что запись следует исправить, выберите **Office Add in** и нажмите **Изменить выбранную проводку**.</span><span class="sxs-lookup"><span data-stu-id="32c97-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="32c97-123">Откроется файл Excel, содержащий сведения о выбранной проводке.</span><span class="sxs-lookup"><span data-stu-id="32c97-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="32c97-124">Если редактируемая проводка является проводкой интернет-заказа, файл Excel содержит следующие листы:</span><span class="sxs-lookup"><span data-stu-id="32c97-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="32c97-125">**Проводка** — на этом листе содержатся сведения заголовка для проводки.</span><span class="sxs-lookup"><span data-stu-id="32c97-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="32c97-126">**Проводка по продаже** — на этом листе содержатся сведения строки для проводки.</span><span class="sxs-lookup"><span data-stu-id="32c97-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="32c97-127">**Проводки по оплате** — на этом листе содержатся сведения о строках платежей для проводки.</span><span class="sxs-lookup"><span data-stu-id="32c97-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="32c97-128">**Проводки по скидкам** — на этом листе содержатся сведения о скидках для проводки.</span><span class="sxs-lookup"><span data-stu-id="32c97-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="32c97-129">**Налоговые проводки** — на этом листе содержатся сведения о налогах для проводки.</span><span class="sxs-lookup"><span data-stu-id="32c97-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="32c97-130">**Проводки по накладным расходам** — на этом листе содержатся сведения о накладных расходах для проводки.</span><span class="sxs-lookup"><span data-stu-id="32c97-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="32c97-131">Если редактируемая проводка является асинхронной проводкой заказа клиента, файл Excel содержит следующие листы:</span><span class="sxs-lookup"><span data-stu-id="32c97-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="32c97-132">**Строки** — на этом листе содержатся сведения заголовка и строки для проводки.</span><span class="sxs-lookup"><span data-stu-id="32c97-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="32c97-133">**Платежи** — на этом листе содержатся сведения о строках платежей для проводки.</span><span class="sxs-lookup"><span data-stu-id="32c97-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="32c97-134">**Скидки** — на этом листе содержатся сведения о скидках для проводки.</span><span class="sxs-lookup"><span data-stu-id="32c97-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="32c97-135">**Налоги** — на этом листе содержатся сведения о налогах для проводки.</span><span class="sxs-lookup"><span data-stu-id="32c97-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="32c97-136">**Накладные расходы** — на этом листе содержатся сведения о накладных расходах для проводки.</span><span class="sxs-lookup"><span data-stu-id="32c97-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="32c97-137">В файле Excel в поле **Статус заказа, ожидающего обработки** введите **Редактирование**, а затем опубликуйте изменение.</span><span class="sxs-lookup"><span data-stu-id="32c97-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="32c97-138">Таким образом эта запись не будет пропущена в задании **Синхронизировать заказ**, выполняемом в пакетном режиме, во время обработки.</span><span class="sxs-lookup"><span data-stu-id="32c97-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="32c97-139">В файле Excel измените соответствующие поля, а затем отправьте эти данные назад в Commerce Headquarters с помощью функции публикации в надстройке Dynamics Excel.</span><span class="sxs-lookup"><span data-stu-id="32c97-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="32c97-140">После публикации данных изменения будут отражены в системе.</span><span class="sxs-lookup"><span data-stu-id="32c97-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="32c97-141">Во время публикации вносимые пользователями изменения не проверяются.</span><span class="sxs-lookup"><span data-stu-id="32c97-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="32c97-142">Чтобы просмотреть полный журнал аудита, выберите **Просмотреть журнал аудита** в заголовке **Проводка розничной торговли** для изменений на уровне заголовка или откройте соответствующий раздел и запись на соответствующей странице проводки.</span><span class="sxs-lookup"><span data-stu-id="32c97-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="32c97-143">Например, все изменения, связанные со строками продаж, будут отображаться на странице **Проводки по продажам**, а все изменения, связанные с платежами, будут отображаться на странице **Проводки по оплате**.</span><span class="sxs-lookup"><span data-stu-id="32c97-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="32c97-144">Для изменений сохраняются следующие сведения аудита:</span><span class="sxs-lookup"><span data-stu-id="32c97-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="32c97-145">Дата и время изменения</span><span class="sxs-lookup"><span data-stu-id="32c97-145">Modified date and time</span></span>
    - <span data-ttu-id="32c97-146">Поле</span><span class="sxs-lookup"><span data-stu-id="32c97-146">Field</span></span>
    - <span data-ttu-id="32c97-147">Старое значение</span><span class="sxs-lookup"><span data-stu-id="32c97-147">Old value</span></span>
    - <span data-ttu-id="32c97-148">Новое значение</span><span class="sxs-lookup"><span data-stu-id="32c97-148">New value</span></span>
    - <span data-ttu-id="32c97-149">Кем изменено</span><span class="sxs-lookup"><span data-stu-id="32c97-149">Modified by</span></span>

1. <span data-ttu-id="32c97-150">После внесения и публикации изменений выберите **Синхронизировать заказ**, чтобы немедленно начать процесс синхронизации.</span><span class="sxs-lookup"><span data-stu-id="32c97-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="32c97-151">Также можно подождать процесса синхронизации, который выполняется в пакетном режиме, для обработки проводки.</span><span class="sxs-lookup"><span data-stu-id="32c97-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="32c97-152">По умолчанию после успешной синхронизации заказов они получают статус удержания на основе кода удержания, определенного в параметрах Commerce.</span><span class="sxs-lookup"><span data-stu-id="32c97-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="32c97-153">Удержание заказов должно быть удалено, прежде чем заказы можно будет обрабатывать для выполнения или других операций.</span><span class="sxs-lookup"><span data-stu-id="32c97-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32c97-154">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="32c97-154">Additional resources</span></span>

[<span data-ttu-id="32c97-155">Редактирование и аудит кассовых проводок и проводок управления кассами</span><span class="sxs-lookup"><span data-stu-id="32c97-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="32c97-156">Изменение финансовых аналитик для проводок розничной торговли</span><span class="sxs-lookup"><span data-stu-id="32c97-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="32c97-157">Создание книги Excel для редактирования проводок розничной торговли</span><span class="sxs-lookup"><span data-stu-id="32c97-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="32c97-158">Добавление полей в книгу Excel для редактирования проводок розничной торговли</span><span class="sxs-lookup"><span data-stu-id="32c97-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
