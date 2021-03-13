---
title: Настройка метода платежа для счета клиента для сайтов электронной коммерции B2B
description: В этой теме описывается, как настроить метод оплаты для счетов клиентов для сайтов электронной коммерции "бизнес-бизнес" (B2B).
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 754e2f83d6c8ff5d3698d98062e54bba7ccd9836
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035956"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a><span data-ttu-id="9acda-103">Настройка метода платежа для счета клиента для сайтов электронной коммерции B2B</span><span class="sxs-lookup"><span data-stu-id="9acda-103">Configure the customer account payment method for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9acda-104">В этой теме описывается, как настроить метод оплаты для счетов клиентов для сайтов электронной коммерции "бизнес-бизнес" (B2B).</span><span class="sxs-lookup"><span data-stu-id="9acda-104">This topic describes how to configure the customer account payment method for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="9acda-105">Продавцы могут принимать различные типы платежей в обмен на продукты и услуги, которые они продают по каналу электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="9acda-105">Retailers can accept various types of payment in exchange for the products and services that they sell in an e-commerce channel.</span></span> <span data-ttu-id="9acda-106">Каждый тип платежа, принимаемый розничным магазином, нужно настроить в Microsoft Dynamics 365 Commerce в процессе настройки системы.</span><span class="sxs-lookup"><span data-stu-id="9acda-106">Each payment type that a retailer accepts must be configured in Microsoft Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="9acda-107">Метод платежа для счета клиента (или "в кредит") должен поддерживаться на сайтах электронной коммерции B2B.</span><span class="sxs-lookup"><span data-stu-id="9acda-107">The customer account (or "on account") payment method must be supported on B2B e-commerce sites.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="9acda-108">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="9acda-108">Prerequisites</span></span>

1. <span data-ttu-id="9acda-109">Добавьте метод платежа для счета клиента в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="9acda-109">Add the customer account payment method in Commerce headquarters.</span></span>
2. <span data-ttu-id="9acda-110">Свяжите метод оплаты для счета клиента с каналом электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="9acda-110">Associate the customer account payment method with the e-commerce channel.</span></span>
3. <span data-ttu-id="9acda-111">Убедитесь, что параметр **Разрешить в кредит** включен для клиентов в разделе **Retail и Commerce \> Клиенты \> Все клиенты \> Значения платежа по умолчанию** в Commerce headquarters.</span><span class="sxs-lookup"><span data-stu-id="9acda-111">Make sure that **Allow on account** is enabled for the customer at **Retail and Commerce \> Customers \> All customers \> Payment defaults** in Commerce headquarters.</span></span> <span data-ttu-id="9acda-112">Кроме того, убедитесь, что параметры **Кредитный лимит** установлены соответствующим образом для клиента в разделе **Retail и Commerce \> Клиенты \> Все клиенты \> Кредит и сборы** в Commerce headquarters.</span><span class="sxs-lookup"><span data-stu-id="9acda-112">Also make sure that **Credit limit** parameters are set appropriately for the customer at **Retail and Commerce \> Customers \> All customers \> Credit and Collections** in Commerce headquarters.</span></span> 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a><span data-ttu-id="9acda-113">Включение метода платежа для счета клиента в конструкторе сайта Commerce</span><span class="sxs-lookup"><span data-stu-id="9acda-113">Enable the customer account payment method in Commerce site builder</span></span> 

<span data-ttu-id="9acda-114">Чтобы включить метод платежа для счета клиента в конструкторе сайта Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9acda-114">To enable the customer account payment method in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9acda-115">Перейдите к разделу **Параметры сайта \> Расширения**.</span><span class="sxs-lookup"><span data-stu-id="9acda-115">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="9acda-116">Установите для свойства **Включить платежи со счета клиента** значение **Включено для клиентов B2B**.</span><span class="sxs-lookup"><span data-stu-id="9acda-116">Set the **Enable customer account payments** property to **Enabled for B2B customers**.</span></span> 
1. <span data-ttu-id="9acda-117">Выберите **Сохранить и опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="9acda-117">Select **Save and Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="9acda-118">Новые параметры сайта вступят в силу только после обновления файла app.settings.json.</span><span class="sxs-lookup"><span data-stu-id="9acda-118">The new site settings take effect only after the app.settings.json file is updated.</span></span> <span data-ttu-id="9acda-119">Дополнительные сведения см. в разделе [Обновления пакета SDK и библиотеки модулей](../e-commerce-extensibility/sdk-updates.md).</span><span class="sxs-lookup"><span data-stu-id="9acda-119">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md).</span></span>

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a><span data-ttu-id="9acda-120">Включение метода платежа для счета клиента на странице оформления заказа для сайта электронной коммерции B2B</span><span class="sxs-lookup"><span data-stu-id="9acda-120">Enable the customer account payment method on the checkout page for the B2B e-commerce site</span></span>

<span data-ttu-id="9acda-121">Чтобы включить метод платежа для счета клиента на странице оформления заказа для сайта электронной коммерции B2B, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9acda-121">To enable the customer account payment method on the checkout page for the B2B e-commerce site, follow these steps.</span></span>

1. <span data-ttu-id="9acda-122">В конструкторе сайтов Commerce найдите и измените страницу или фрагмент оформления заказа, содержащий модуль оформления заказа для сайта электронной коммерции B2B.</span><span class="sxs-lookup"><span data-stu-id="9acda-122">In Commerce site builder, find and edit the checkout page or fragment that contains the checkout module for the B2B e-commerce site.</span></span>
1. <span data-ttu-id="9acda-123">В области **Контейнер раздела оформления заказа** выберите **Добавить модуль**, затем добавьте модуль **Платеж со счета клиента**.</span><span class="sxs-lookup"><span data-stu-id="9acda-123">In the **Checkout section container** slot, select **Add Module**, and then add a **Customer account payment** module.</span></span>
1. <span data-ttu-id="9acda-124">Расположите модуль **Платеж со счета клиента**, выбрав многоточие (**...**), затем выберите **Вверх** или **Вниз** по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="9acda-124">Position the **Customer account payment** module by selecting the ellipsis (**...**), and then selecting **Move Up** or **Move Down** as required.</span></span>
1. <span data-ttu-id="9acda-125">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="9acda-125">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a><span data-ttu-id="9acda-126">Проверка того, что метод платежа со счета клиента был включен и опубликован</span><span class="sxs-lookup"><span data-stu-id="9acda-126">Confirm that the customer account payment method has been enabled and published</span></span>

<span data-ttu-id="9acda-127">Чтобы проверить, что метод платежа со счета клиента был включен и опубликован, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9acda-127">To confirm that the customer account payment method has been enabled, follow these steps.</span></span>

1. <span data-ttu-id="9acda-128">Войдите на сайт электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="9acda-128">Sign in to the e-commerce site.</span></span>
1. <span data-ttu-id="9acda-129">Добавьте продукты в корзину.</span><span class="sxs-lookup"><span data-stu-id="9acda-129">Add a product to the cart.</span></span>
1. <span data-ttu-id="9acda-130">Перейдите на страницу оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="9acda-130">Go to the checkout page.</span></span> <span data-ttu-id="9acda-131">Должен отобразиться новый метод платежа **Счет клиента**.</span><span class="sxs-lookup"><span data-stu-id="9acda-131">You should see the new **Customer Account** payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9acda-132">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9acda-132">Additional resources</span></span>

[<span data-ttu-id="9acda-133">Настройка сайта электронной коммерции B2B</span><span class="sxs-lookup"><span data-stu-id="9acda-133">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="9acda-134">Создание иерархий моделирования организации для организаций B2B</span><span class="sxs-lookup"><span data-stu-id="9acda-134">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="9acda-135">Управление пользователями деловых партнеров на сайтах электронной коммерции B2B</span><span class="sxs-lookup"><span data-stu-id="9acda-135">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="9acda-136">Настройка лимитов количества продуктов для сайтов электронной коммерции B2B</span><span class="sxs-lookup"><span data-stu-id="9acda-136">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="9acda-137">Обновления SDK и библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="9acda-137">SDK and Module library updates</span></span>](../e-commerce-extensibility/sdk-updates.md)
