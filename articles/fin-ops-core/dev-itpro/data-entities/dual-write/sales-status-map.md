---
title: Настройка сопоставления для столбцов статуса заказа на продажу
description: В этой теме объясняется, как настроить столбцы статуса заказа на продажу для двойной записи.
author: dasani-madipalli
ms.date: 06/25/2020
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
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 9afa64df73aa17e7a15a0ee4f4529ac74bcd3c67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750722"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="45fe3-103">Настройка сопоставления для столбцов статуса заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="45fe3-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="45fe3-104">Столбцы, которые показывают статус заказа на продажу, имеют разные значения перечисления в Microsoft Dynamics 365 Supply Chain Management и Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="45fe3-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="45fe3-105">Для сопоставления этих столбцов в двойной записи требуется дополнительная настройка.</span><span class="sxs-lookup"><span data-stu-id="45fe3-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="45fe3-106">Столбцы в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="45fe3-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="45fe3-107">В Supply Chain Management два столбца отражают статус заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="45fe3-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="45fe3-108">Столбцы, которые необходимо сопоставить, это **Статус** и **Статус документа**.</span><span class="sxs-lookup"><span data-stu-id="45fe3-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="45fe3-109">Перечисление **Статус** определяет общий статус заказа.</span><span class="sxs-lookup"><span data-stu-id="45fe3-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="45fe3-110">Этот статус отображается в заголовке заказа.</span><span class="sxs-lookup"><span data-stu-id="45fe3-110">This status is shown on the order header.</span></span>

<span data-ttu-id="45fe3-111">Перечисление **Статус** имеет следующие значения:</span><span class="sxs-lookup"><span data-stu-id="45fe3-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="45fe3-112">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="45fe3-112">Open Order</span></span>
- <span data-ttu-id="45fe3-113">Доставлено</span><span class="sxs-lookup"><span data-stu-id="45fe3-113">Delivered</span></span>
- <span data-ttu-id="45fe3-114">Оприходовано</span><span class="sxs-lookup"><span data-stu-id="45fe3-114">Invoiced</span></span>
- <span data-ttu-id="45fe3-115">Отменено</span><span class="sxs-lookup"><span data-stu-id="45fe3-115">Cancelled</span></span>

<span data-ttu-id="45fe3-116">Перечисление **Статус документа** указывает последний документ, созданный для данного заказа.</span><span class="sxs-lookup"><span data-stu-id="45fe3-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="45fe3-117">Например, если заказ подтвержден, этот документ является подтверждением заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="45fe3-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="45fe3-118">Если по заказу на продажу частично выставлены накладные, а затем подтверждена оставшаяся строка, статус документа остается **Накладная**, поскольку накладная создается позже в процессе.</span><span class="sxs-lookup"><span data-stu-id="45fe3-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="45fe3-119">Перечисление **Статус документа** имеет следующие значения:</span><span class="sxs-lookup"><span data-stu-id="45fe3-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="45fe3-120">Подтверждение</span><span class="sxs-lookup"><span data-stu-id="45fe3-120">Confirmation</span></span>
- <span data-ttu-id="45fe3-121">Сборочный лист</span><span class="sxs-lookup"><span data-stu-id="45fe3-121">Picking List</span></span>
- <span data-ttu-id="45fe3-122">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="45fe3-122">Packing Slip</span></span>
- <span data-ttu-id="45fe3-123">Счет-фактура</span><span class="sxs-lookup"><span data-stu-id="45fe3-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="45fe3-124">Столбцы в Sales</span><span class="sxs-lookup"><span data-stu-id="45fe3-124">columns in Sales</span></span>

<span data-ttu-id="45fe3-125">В Sales два столбца указывают статус заказа.</span><span class="sxs-lookup"><span data-stu-id="45fe3-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="45fe3-126">Столбцы, которые необходимо сопоставить, это **Статус** и **Статус обработки**.</span><span class="sxs-lookup"><span data-stu-id="45fe3-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="45fe3-127">Перечисление **Статус** определяет общий статус заказа.</span><span class="sxs-lookup"><span data-stu-id="45fe3-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="45fe3-128">Оно имеет следующие значения:</span><span class="sxs-lookup"><span data-stu-id="45fe3-128">It has the following values:</span></span>

- <span data-ttu-id="45fe3-129">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="45fe3-129">Active</span></span>
- <span data-ttu-id="45fe3-130">Отправлена</span><span class="sxs-lookup"><span data-stu-id="45fe3-130">Submitted</span></span>
- <span data-ttu-id="45fe3-131">Выполнено</span><span class="sxs-lookup"><span data-stu-id="45fe3-131">Fulfilled</span></span>
- <span data-ttu-id="45fe3-132">Оприходовано</span><span class="sxs-lookup"><span data-stu-id="45fe3-132">Invoiced</span></span>
- <span data-ttu-id="45fe3-133">Отменено</span><span class="sxs-lookup"><span data-stu-id="45fe3-133">Cancelled</span></span>

<span data-ttu-id="45fe3-134">Перечисление **Статус обработки** было введено так, чтобы можно было более точно сопоставить статус с Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="45fe3-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="45fe3-135">В следующей таблице показано сопоставление поля **Статус обработки** в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="45fe3-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="45fe3-136">Статус обработки</span><span class="sxs-lookup"><span data-stu-id="45fe3-136">Processing Status</span></span>   | <span data-ttu-id="45fe3-137">Статус в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="45fe3-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="45fe3-138">Статус документа в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="45fe3-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="45fe3-139">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="45fe3-139">Active</span></span>              | <span data-ttu-id="45fe3-140">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="45fe3-140">Open Order</span></span>                        | <span data-ttu-id="45fe3-141">Не допускается</span><span class="sxs-lookup"><span data-stu-id="45fe3-141">None</span></span>                                       |
| <span data-ttu-id="45fe3-142">Подтверждено</span><span class="sxs-lookup"><span data-stu-id="45fe3-142">Confirmed</span></span>           | <span data-ttu-id="45fe3-143">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="45fe3-143">Open Order</span></span>                        | <span data-ttu-id="45fe3-144">Подтверждение</span><span class="sxs-lookup"><span data-stu-id="45fe3-144">Confirmation</span></span>                               |
| <span data-ttu-id="45fe3-145">Скомплектовано</span><span class="sxs-lookup"><span data-stu-id="45fe3-145">Picked</span></span>              | <span data-ttu-id="45fe3-146">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="45fe3-146">Open Order</span></span>                        | <span data-ttu-id="45fe3-147">Лист подбора</span><span class="sxs-lookup"><span data-stu-id="45fe3-147">Picking List</span></span>                               |
| <span data-ttu-id="45fe3-148">Частично доставлено</span><span class="sxs-lookup"><span data-stu-id="45fe3-148">Partially Delivered</span></span> | <span data-ttu-id="45fe3-149">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="45fe3-149">Open Order</span></span>                        | <span data-ttu-id="45fe3-150">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="45fe3-150">Packing Slip</span></span>                               |
| <span data-ttu-id="45fe3-151">Доставлено</span><span class="sxs-lookup"><span data-stu-id="45fe3-151">Delivered</span></span>           | <span data-ttu-id="45fe3-152">Доставлено</span><span class="sxs-lookup"><span data-stu-id="45fe3-152">Delivered</span></span>                         | <span data-ttu-id="45fe3-153">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="45fe3-153">Packing Slip</span></span>                               |
| <span data-ttu-id="45fe3-154">Частично выставлен счет</span><span class="sxs-lookup"><span data-stu-id="45fe3-154">Partially Invoiced</span></span>  | <span data-ttu-id="45fe3-155">Доставлено</span><span class="sxs-lookup"><span data-stu-id="45fe3-155">Delivered</span></span>                         | <span data-ttu-id="45fe3-156">Счет-фактура</span><span class="sxs-lookup"><span data-stu-id="45fe3-156">Invoice</span></span>                                    |
| <span data-ttu-id="45fe3-157">Оприходовано</span><span class="sxs-lookup"><span data-stu-id="45fe3-157">Invoiced</span></span>            | <span data-ttu-id="45fe3-158">Оприходовано</span><span class="sxs-lookup"><span data-stu-id="45fe3-158">Invoiced</span></span>                          | <span data-ttu-id="45fe3-159">Счет-фактура</span><span class="sxs-lookup"><span data-stu-id="45fe3-159">Invoice</span></span>                                    |
| <span data-ttu-id="45fe3-160">Отменено</span><span class="sxs-lookup"><span data-stu-id="45fe3-160">Cancelled</span></span>           | <span data-ttu-id="45fe3-161">Отменено</span><span class="sxs-lookup"><span data-stu-id="45fe3-161">Cancelled</span></span>                         | <span data-ttu-id="45fe3-162">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="45fe3-162">Not applicable</span></span>                             |

<span data-ttu-id="45fe3-163">В следующей таблице показано сопоставление поля **Статус обработки** между Sales и Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="45fe3-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="45fe3-164">Статус обработки</span><span class="sxs-lookup"><span data-stu-id="45fe3-164">Processing Status</span></span>   | <span data-ttu-id="45fe3-165">Статус в Sales</span><span class="sxs-lookup"><span data-stu-id="45fe3-165">Status in Sales</span></span> | <span data-ttu-id="45fe3-166">Статус в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="45fe3-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="45fe3-167">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="45fe3-167">Active</span></span>              | <span data-ttu-id="45fe3-168">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="45fe3-168">Active</span></span>          | <span data-ttu-id="45fe3-169">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="45fe3-169">Open Order</span></span>                        |
| <span data-ttu-id="45fe3-170">Подтверждено</span><span class="sxs-lookup"><span data-stu-id="45fe3-170">Confirmed</span></span>           | <span data-ttu-id="45fe3-171">Отправлена</span><span class="sxs-lookup"><span data-stu-id="45fe3-171">Submitted</span></span>       | <span data-ttu-id="45fe3-172">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="45fe3-172">Open Order</span></span>                        |
| <span data-ttu-id="45fe3-173">Скомплектовано</span><span class="sxs-lookup"><span data-stu-id="45fe3-173">Picked</span></span>              | <span data-ttu-id="45fe3-174">Отправлена</span><span class="sxs-lookup"><span data-stu-id="45fe3-174">Submitted</span></span>       | <span data-ttu-id="45fe3-175">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="45fe3-175">Open Order</span></span>                        |
| <span data-ttu-id="45fe3-176">Частично доставлено</span><span class="sxs-lookup"><span data-stu-id="45fe3-176">Partially Delivered</span></span> | <span data-ttu-id="45fe3-177">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="45fe3-177">Active</span></span>          | <span data-ttu-id="45fe3-178">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="45fe3-178">Open Order</span></span>                        |
| <span data-ttu-id="45fe3-179">Частично выставлен счет</span><span class="sxs-lookup"><span data-stu-id="45fe3-179">Partially Invoiced</span></span>  | <span data-ttu-id="45fe3-180">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="45fe3-180">Active</span></span>          | <span data-ttu-id="45fe3-181">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="45fe3-181">Open Order</span></span>                        |
| <span data-ttu-id="45fe3-182">Частично выставлен счет</span><span class="sxs-lookup"><span data-stu-id="45fe3-182">Partially Invoiced</span></span>  | <span data-ttu-id="45fe3-183">Выполнено</span><span class="sxs-lookup"><span data-stu-id="45fe3-183">Fulfilled</span></span>       | <span data-ttu-id="45fe3-184">Доставлено</span><span class="sxs-lookup"><span data-stu-id="45fe3-184">Delivered</span></span>                         |
| <span data-ttu-id="45fe3-185">Оприходовано</span><span class="sxs-lookup"><span data-stu-id="45fe3-185">Invoiced</span></span>            | <span data-ttu-id="45fe3-186">Оприходовано</span><span class="sxs-lookup"><span data-stu-id="45fe3-186">Invoiced</span></span>        | <span data-ttu-id="45fe3-187">Оприходовано</span><span class="sxs-lookup"><span data-stu-id="45fe3-187">Invoiced</span></span>                          |
| <span data-ttu-id="45fe3-188">Отменено</span><span class="sxs-lookup"><span data-stu-id="45fe3-188">Cancelled</span></span>           | <span data-ttu-id="45fe3-189">Отменено</span><span class="sxs-lookup"><span data-stu-id="45fe3-189">Cancelled</span></span>       | <span data-ttu-id="45fe3-190">Отменено</span><span class="sxs-lookup"><span data-stu-id="45fe3-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="45fe3-191">Настройка</span><span class="sxs-lookup"><span data-stu-id="45fe3-191">Setup</span></span>

<span data-ttu-id="45fe3-192">Чтобы настроить сопоставление для столбцов статуса заказа на продажу, необходимо включить атрибуты **IsSOPIntegrationEnabled** и **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="45fe3-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="45fe3-193">Для включения атрибута **IsSOPIntegrationEnabled** выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="45fe3-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="45fe3-194">В браузере перейдите к `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="45fe3-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="45fe3-195">Замените **\<test-name\>** ссылкой вашей компании на Sales.</span><span class="sxs-lookup"><span data-stu-id="45fe3-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="45fe3-196">На открытой странице найдите **organizationid** и запишите значение.</span><span class="sxs-lookup"><span data-stu-id="45fe3-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Поиск organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="45fe3-198">В Sales откройте консоль браузера и запустите следующий сценарий.</span><span class="sxs-lookup"><span data-stu-id="45fe3-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="45fe3-199">Используйте значение **organizationid** из шага 2.</span><span class="sxs-lookup"><span data-stu-id="45fe3-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![Код JavaScript в консоли браузера](media/sales-map-script.png)

4. <span data-ttu-id="45fe3-201">Убедитесь, что для атрибута **IsSOPIntegrationEnabled** установлено значение **true**.</span><span class="sxs-lookup"><span data-stu-id="45fe3-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="45fe3-202">Для проверки значения используйте URL-адрес из шага 1.</span><span class="sxs-lookup"><span data-stu-id="45fe3-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled со значением true](media/sales-map-integration-enabled.png)

<span data-ttu-id="45fe3-204">Для включения атрибута **isIntegrationUser** выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="45fe3-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="45fe3-205">В Sales перейдите в раздел **Параметр \> Настройка \> Настроить систему**, выберите пункт **Таблица пользователя** и откройте **Форма \> Пользователь**.</span><span class="sxs-lookup"><span data-stu-id="45fe3-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![Открытие формы пользователя](media/sales-map-user.png)

2. <span data-ttu-id="45fe3-207">В обозревателе полей найдите **Пользовательский режим интеграции** и дважды щелкните его, чтобы добавить в форму.</span><span class="sxs-lookup"><span data-stu-id="45fe3-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="45fe3-208">Сохраните изменение.</span><span class="sxs-lookup"><span data-stu-id="45fe3-208">Save your change.</span></span>

    ![Добавление столбца пользовательского режима интеграции в форму](media/sales-map-field-explorer.png)

3. <span data-ttu-id="45fe3-210">В Sales перейдите к разделу **Параметр \> Безопасность \> Пользователи** и измените представление с **Разрешенные пользователи** на **Пользователи приложения**.</span><span class="sxs-lookup"><span data-stu-id="45fe3-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Изменение представления с разрешенных пользователей на пользователей приложения](media/sales-map-enabled-users.png)

4. <span data-ttu-id="45fe3-212">Выберите две записи для **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="45fe3-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Список пользователей приложения](media/sales-map-user-mode.png)

5. <span data-ttu-id="45fe3-214">Измените значение столбца **Пользовательский режим интеграции** на **Да**.</span><span class="sxs-lookup"><span data-stu-id="45fe3-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![Изменение значение столбца пользовательского режима интеграции](media/sales-map-user-mode-yes.png)

<span data-ttu-id="45fe3-216">Заказы на продажу теперь сопоставлены.</span><span class="sxs-lookup"><span data-stu-id="45fe3-216">Your sales orders are now mapped.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]