---
title: Настройка сопоставления для полей статуса заказа на продажу
description: В этой теме объясняется, как настроить поля статуса заказа на продажу для двойной записи.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 5855581100606003c1faf6b88a0ab234ae378893
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997682"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a><span data-ttu-id="226ce-103">Настройка сопоставления для полей статуса заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="226ce-103">Set up the mapping for the sales order status fields</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="226ce-104">Поля, которые показывают статус заказа на продажу, имеют разные значения перечисления в Microsoft Dynamics 365 Supply Chain Management и Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="226ce-104">The fields that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="226ce-105">Для сопоставления этих полей в двойной записи требуется дополнительная настройка.</span><span class="sxs-lookup"><span data-stu-id="226ce-105">Additional setup is required to map these fields in dual-write.</span></span>

## <a name="fields-in-supply-chain-management"></a><span data-ttu-id="226ce-106">Поля в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="226ce-106">Fields in Supply Chain Management</span></span>

<span data-ttu-id="226ce-107">В Supply Chain Management два поля отражают статус заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="226ce-107">In Supply Chain Management, two fields reflect the status of the sales order.</span></span> <span data-ttu-id="226ce-108">Поля, которые необходимо сопоставить, это **Статус** и **Статус документа**.</span><span class="sxs-lookup"><span data-stu-id="226ce-108">The fields that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="226ce-109">Перечисление **Статус** определяет общий статус заказа.</span><span class="sxs-lookup"><span data-stu-id="226ce-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="226ce-110">Этот статус отображается в заголовке заказа.</span><span class="sxs-lookup"><span data-stu-id="226ce-110">This status is shown on the order header.</span></span>

<span data-ttu-id="226ce-111">Перечисление **Статус** имеет следующие значения:</span><span class="sxs-lookup"><span data-stu-id="226ce-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="226ce-112">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="226ce-112">Open Order</span></span>
- <span data-ttu-id="226ce-113">Доставлено</span><span class="sxs-lookup"><span data-stu-id="226ce-113">Delivered</span></span>
- <span data-ttu-id="226ce-114">Оприходовано</span><span class="sxs-lookup"><span data-stu-id="226ce-114">Invoiced</span></span>
- <span data-ttu-id="226ce-115">Отменено</span><span class="sxs-lookup"><span data-stu-id="226ce-115">Cancelled</span></span>

<span data-ttu-id="226ce-116">Перечисление **Статус документа** указывает последний документ, созданный для данного заказа.</span><span class="sxs-lookup"><span data-stu-id="226ce-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="226ce-117">Например, если заказ подтвержден, этот документ является подтверждением заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="226ce-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="226ce-118">Если по заказу на продажу частично выставлены накладные, а затем подтверждена оставшаяся строка, статус документа остается **Накладная** , поскольку накладная создается позже в процессе.</span><span class="sxs-lookup"><span data-stu-id="226ce-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice** , because the invoice is generated later in the process.</span></span>

<span data-ttu-id="226ce-119">Перечисление **Статус документа** имеет следующие значения:</span><span class="sxs-lookup"><span data-stu-id="226ce-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="226ce-120">Подтверждение</span><span class="sxs-lookup"><span data-stu-id="226ce-120">Confirmation</span></span>
- <span data-ttu-id="226ce-121">Лист подбора</span><span class="sxs-lookup"><span data-stu-id="226ce-121">Picking List</span></span>
- <span data-ttu-id="226ce-122">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="226ce-122">Packing Slip</span></span>
- <span data-ttu-id="226ce-123">Счет-фактура</span><span class="sxs-lookup"><span data-stu-id="226ce-123">Invoice</span></span>

## <a name="fields-in-sales"></a><span data-ttu-id="226ce-124">Поля в Sales</span><span class="sxs-lookup"><span data-stu-id="226ce-124">Fields in Sales</span></span>

<span data-ttu-id="226ce-125">В Sales два поля указывают статус заказа.</span><span class="sxs-lookup"><span data-stu-id="226ce-125">In Sales, two fields indicate the status of the order.</span></span> <span data-ttu-id="226ce-126">Поля, которые необходимо сопоставить, это **Статус** и **Статус обработки**.</span><span class="sxs-lookup"><span data-stu-id="226ce-126">The fields that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="226ce-127">Перечисление **Статус** определяет общий статус заказа.</span><span class="sxs-lookup"><span data-stu-id="226ce-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="226ce-128">Оно имеет следующие значения:</span><span class="sxs-lookup"><span data-stu-id="226ce-128">It has the following values:</span></span>

- <span data-ttu-id="226ce-129">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="226ce-129">Active</span></span>
- <span data-ttu-id="226ce-130">Отправлена</span><span class="sxs-lookup"><span data-stu-id="226ce-130">Submitted</span></span>
- <span data-ttu-id="226ce-131">Выполнено</span><span class="sxs-lookup"><span data-stu-id="226ce-131">Fulfilled</span></span>
- <span data-ttu-id="226ce-132">Оприходовано</span><span class="sxs-lookup"><span data-stu-id="226ce-132">Invoiced</span></span>
- <span data-ttu-id="226ce-133">Отменено</span><span class="sxs-lookup"><span data-stu-id="226ce-133">Cancelled</span></span>

<span data-ttu-id="226ce-134">Перечисление **Статус обработки** было введено так, чтобы можно было более точно сопоставить статус с Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="226ce-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="226ce-135">В следующей таблице показано сопоставление поля **Статус обработки** в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="226ce-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="226ce-136">Статус обработки</span><span class="sxs-lookup"><span data-stu-id="226ce-136">Processing Status</span></span>   | <span data-ttu-id="226ce-137">Статус в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="226ce-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="226ce-138">Статус документа в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="226ce-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="226ce-139">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="226ce-139">Active</span></span>              | <span data-ttu-id="226ce-140">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="226ce-140">Open Order</span></span>                        | <span data-ttu-id="226ce-141">Не допускается</span><span class="sxs-lookup"><span data-stu-id="226ce-141">None</span></span>                                       |
| <span data-ttu-id="226ce-142">Подтверждено</span><span class="sxs-lookup"><span data-stu-id="226ce-142">Confirmed</span></span>           | <span data-ttu-id="226ce-143">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="226ce-143">Open Order</span></span>                        | <span data-ttu-id="226ce-144">Подтверждение</span><span class="sxs-lookup"><span data-stu-id="226ce-144">Confirmation</span></span>                               |
| <span data-ttu-id="226ce-145">Скомплектовано</span><span class="sxs-lookup"><span data-stu-id="226ce-145">Picked</span></span>              | <span data-ttu-id="226ce-146">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="226ce-146">Open Order</span></span>                        | <span data-ttu-id="226ce-147">Лист подбора</span><span class="sxs-lookup"><span data-stu-id="226ce-147">Picking List</span></span>                               |
| <span data-ttu-id="226ce-148">Частично доставлено</span><span class="sxs-lookup"><span data-stu-id="226ce-148">Partially Delivered</span></span> | <span data-ttu-id="226ce-149">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="226ce-149">Open Order</span></span>                        | <span data-ttu-id="226ce-150">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="226ce-150">Packing Slip</span></span>                               |
| <span data-ttu-id="226ce-151">Доставлено</span><span class="sxs-lookup"><span data-stu-id="226ce-151">Delivered</span></span>           | <span data-ttu-id="226ce-152">Доставлено</span><span class="sxs-lookup"><span data-stu-id="226ce-152">Delivered</span></span>                         | <span data-ttu-id="226ce-153">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="226ce-153">Packing Slip</span></span>                               |
| <span data-ttu-id="226ce-154">Частично выставлен счет</span><span class="sxs-lookup"><span data-stu-id="226ce-154">Partially Invoiced</span></span>  | <span data-ttu-id="226ce-155">Доставлено</span><span class="sxs-lookup"><span data-stu-id="226ce-155">Delivered</span></span>                         | <span data-ttu-id="226ce-156">Счет-фактура</span><span class="sxs-lookup"><span data-stu-id="226ce-156">Invoice</span></span>                                    |
| <span data-ttu-id="226ce-157">Оприходовано</span><span class="sxs-lookup"><span data-stu-id="226ce-157">Invoiced</span></span>            | <span data-ttu-id="226ce-158">Оприходовано</span><span class="sxs-lookup"><span data-stu-id="226ce-158">Invoiced</span></span>                          | <span data-ttu-id="226ce-159">Счет-фактура</span><span class="sxs-lookup"><span data-stu-id="226ce-159">Invoice</span></span>                                    |
| <span data-ttu-id="226ce-160">Отменено</span><span class="sxs-lookup"><span data-stu-id="226ce-160">Cancelled</span></span>           | <span data-ttu-id="226ce-161">Отменено</span><span class="sxs-lookup"><span data-stu-id="226ce-161">Cancelled</span></span>                         | <span data-ttu-id="226ce-162">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="226ce-162">Not applicable</span></span>                             |

<span data-ttu-id="226ce-163">В следующей таблице показано сопоставление поля **Статус обработки** между Sales и Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="226ce-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="226ce-164">Статус обработки</span><span class="sxs-lookup"><span data-stu-id="226ce-164">Processing Status</span></span>   | <span data-ttu-id="226ce-165">Статус в Sales</span><span class="sxs-lookup"><span data-stu-id="226ce-165">Status in Sales</span></span> | <span data-ttu-id="226ce-166">Статус в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="226ce-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="226ce-167">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="226ce-167">Active</span></span>              | <span data-ttu-id="226ce-168">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="226ce-168">Active</span></span>          | <span data-ttu-id="226ce-169">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="226ce-169">Open Order</span></span>                        |
| <span data-ttu-id="226ce-170">Подтверждено</span><span class="sxs-lookup"><span data-stu-id="226ce-170">Confirmed</span></span>           | <span data-ttu-id="226ce-171">Отправлена</span><span class="sxs-lookup"><span data-stu-id="226ce-171">Submitted</span></span>       | <span data-ttu-id="226ce-172">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="226ce-172">Open Order</span></span>                        |
| <span data-ttu-id="226ce-173">Скомплектовано</span><span class="sxs-lookup"><span data-stu-id="226ce-173">Picked</span></span>              | <span data-ttu-id="226ce-174">Отправлена</span><span class="sxs-lookup"><span data-stu-id="226ce-174">Submitted</span></span>       | <span data-ttu-id="226ce-175">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="226ce-175">Open Order</span></span>                        |
| <span data-ttu-id="226ce-176">Частично доставлено</span><span class="sxs-lookup"><span data-stu-id="226ce-176">Partially Delivered</span></span> | <span data-ttu-id="226ce-177">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="226ce-177">Active</span></span>          | <span data-ttu-id="226ce-178">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="226ce-178">Open Order</span></span>                        |
| <span data-ttu-id="226ce-179">Частично выставлен счет</span><span class="sxs-lookup"><span data-stu-id="226ce-179">Partially Invoiced</span></span>  | <span data-ttu-id="226ce-180">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="226ce-180">Active</span></span>          | <span data-ttu-id="226ce-181">Открытый заказ</span><span class="sxs-lookup"><span data-stu-id="226ce-181">Open Order</span></span>                        |
| <span data-ttu-id="226ce-182">Частично выставлен счет</span><span class="sxs-lookup"><span data-stu-id="226ce-182">Partially Invoiced</span></span>  | <span data-ttu-id="226ce-183">Выполнено</span><span class="sxs-lookup"><span data-stu-id="226ce-183">Fulfilled</span></span>       | <span data-ttu-id="226ce-184">Доставлено</span><span class="sxs-lookup"><span data-stu-id="226ce-184">Delivered</span></span>                         |
| <span data-ttu-id="226ce-185">Оприходовано</span><span class="sxs-lookup"><span data-stu-id="226ce-185">Invoiced</span></span>            | <span data-ttu-id="226ce-186">Оприходовано</span><span class="sxs-lookup"><span data-stu-id="226ce-186">Invoiced</span></span>        | <span data-ttu-id="226ce-187">Оприходовано</span><span class="sxs-lookup"><span data-stu-id="226ce-187">Invoiced</span></span>                          |
| <span data-ttu-id="226ce-188">Отменено</span><span class="sxs-lookup"><span data-stu-id="226ce-188">Cancelled</span></span>           | <span data-ttu-id="226ce-189">Отменено</span><span class="sxs-lookup"><span data-stu-id="226ce-189">Cancelled</span></span>       | <span data-ttu-id="226ce-190">Отменено</span><span class="sxs-lookup"><span data-stu-id="226ce-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="226ce-191">Настройка</span><span class="sxs-lookup"><span data-stu-id="226ce-191">Setup</span></span>

<span data-ttu-id="226ce-192">Чтобы настроить сопоставление для полей статуса заказа на продажу, необходимо включить атрибуты **IsSOPIntegrationEnabled** и **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="226ce-192">To set up the mapping for the sales order status fields, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="226ce-193">Для включения атрибута **IsSOPIntegrationEnabled** выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="226ce-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="226ce-194">В браузере перейдите к `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="226ce-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="226ce-195">Замените **\<test-name\>** ссылкой вашей компании на Sales.</span><span class="sxs-lookup"><span data-stu-id="226ce-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="226ce-196">На открытой странице найдите **organizationid** и запишите значение.</span><span class="sxs-lookup"><span data-stu-id="226ce-196">On the page that is opened, find **organizationid** , and make a note of the value.</span></span>

    ![Поиск organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="226ce-198">В Sales откройте консоль браузера и запустите следующий сценарий.</span><span class="sxs-lookup"><span data-stu-id="226ce-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="226ce-199">Используйте значение **organizationid** из шага 2.</span><span class="sxs-lookup"><span data-stu-id="226ce-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![Код JavaScript в консоли браузера](media/sales-map-script.png)

4. <span data-ttu-id="226ce-201">Убедитесь, что для атрибута **IsSOPIntegrationEnabled** установлено значение **true**.</span><span class="sxs-lookup"><span data-stu-id="226ce-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="226ce-202">Для проверки значения используйте URL-адрес из шага 1.</span><span class="sxs-lookup"><span data-stu-id="226ce-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled со значением true](media/sales-map-integration-enabled.png)

<span data-ttu-id="226ce-204">Для включения атрибута **isIntegrationUser** выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="226ce-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="226ce-205">В Sales перейдите в раздел **Параметр \> Настройка \> Настроить систему** , выберите пункт **Сущность пользователя** и откройте **Форма \> Пользователь**.</span><span class="sxs-lookup"><span data-stu-id="226ce-205">In Sales, go to **Setting \> Customization \> Customize the System** , select **User entity** , and then open **Form \> User**.</span></span>

    ![Открытие формы пользователя](media/sales-map-user.png)

2. <span data-ttu-id="226ce-207">В обозревателе полей найдите **Пользовательский режим интеграции** и дважды щелкните его, чтобы добавить в форму.</span><span class="sxs-lookup"><span data-stu-id="226ce-207">In Field Explorer, find **Integration user mode** , and double-click it to add it to the form.</span></span> <span data-ttu-id="226ce-208">Сохраните изменение.</span><span class="sxs-lookup"><span data-stu-id="226ce-208">Save your change.</span></span>

    ![Добавление поля пользовательского режима интеграции в форму](media/sales-map-field-explorer.png)

3. <span data-ttu-id="226ce-210">В Sales перейдите к разделу **Параметр \> Безопасность \> Пользователи** и измените представление с **Разрешенные пользователи** на **Пользователи приложения**.</span><span class="sxs-lookup"><span data-stu-id="226ce-210">In Sales, go to **Setting \> Security \> Users** , and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Изменение представления с разрешенных пользователей на пользователей приложения](media/sales-map-enabled-users.png)

4. <span data-ttu-id="226ce-212">Выберите две записи для **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="226ce-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Список пользователей приложения](media/sales-map-user-mode.png)

5. <span data-ttu-id="226ce-214">Измените значение поля **Пользовательский режим интеграции** на **Да**.</span><span class="sxs-lookup"><span data-stu-id="226ce-214">Change the value of the **Integration user mode** field to **Yes**.</span></span>

    ![Изменение значение поля пользовательского режима интеграции](media/sales-map-user-mode-yes.png)

<span data-ttu-id="226ce-216">Заказы на продажу теперь сопоставлены.</span><span class="sxs-lookup"><span data-stu-id="226ce-216">Your sales orders are now mapped.</span></span>
