---
title: Включение уведомлений о прибытии клиентов в POS
description: В этом разделе описывается, как включить уведомления о прибытии клиентов в POS Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b42dc7766f8a69a7409c28d21b49cc96eca18dd4
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271433"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a><span data-ttu-id="e2f8a-103">Включение уведомлений о прибытии клиентов в POS</span><span class="sxs-lookup"><span data-stu-id="e2f8a-103">Enable customer check-in notifications in point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e2f8a-104">В этом разделе описывается, как включить уведомления о прибытии клиентов в POS Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-104">This topic describes how to enable customer check-in notifications in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="e2f8a-105">В сообщениях по электронной почте "заказ готов для отправки" организации могут создать ссылку или кнопку, которые позволяют пользователям уведомлять магазин о том, что они находятся в помещении компании, и ожидают получения товара.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-105">In their "order ready for pickup" emails, organizations can provide a link or button that lets customers notify the store that they are on the premises and waiting for their package to be brought out to them.</span></span> <span data-ttu-id="e2f8a-106">После этого клиенты получают подтверждение прибытия, и магазин получает уведомление в качестве задачи в своем приложении POS.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-106">Customers then receive a check-in confirmation, and the store receives a notification as a task in its POS application.</span></span> <span data-ttu-id="e2f8a-107">Эта задача выступает в качестве напоминания для продавца для доставки заказа к автомобилю клиента.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-107">This task serves as a prompt for a sales associate to deliver the order to the customer's vehicle.</span></span> <span data-ttu-id="e2f8a-108">Поэтому клиент не должен входить магазин.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-108">Therefore, the customer doesn't have to enter the store.</span></span>

<span data-ttu-id="e2f8a-109">Workflow-процесс прибытия клиента также может быть настроен для сбора дополнительных сведений от клиентов, таких как номер места стоянки, марка, модель и цвет автомобиля, и инструкции по доставке.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-109">The customer check-in workflow can also be configured to collect additional information from customers, such as their parking spot number, the make, model, and color of their vehicle, and delivery instructions.</span></span> <span data-ttu-id="e2f8a-110">Помощник по розничному магазину может использовать эту информацию для облегчения выполнения заказов.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-110">The retail store attendant can use this information to facilitate order fulfillment.</span></span>

## <a name="enable-customer-check-in"></a><span data-ttu-id="e2f8a-111">Включение прибытия клиента</span><span class="sxs-lookup"><span data-stu-id="e2f8a-111">Enable customer check-in</span></span>

<span data-ttu-id="e2f8a-112">Когда функция прибытия клиента включена, Commerce создает код подтверждения заказа (также называемый кодом ссылки на канал).</span><span class="sxs-lookup"><span data-stu-id="e2f8a-112">When the customer check-in feature is turned on, Commerce generates an order confirmation ID (also known as the channel reference ID).</span></span> <span data-ttu-id="e2f8a-113">Кроме того, в нем создаются коды подтверждения заказа для заказов, созданных через POS или каналы центра обработки звонков.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-113">It also generates order confirmation IDs for orders that are created through point of sale (POS) or call center channels.</span></span> 

<span data-ttu-id="e2f8a-114">Чтобы включить функцию прибытия клиента в Commerce Headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-114">To turn on the customer check-in feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e2f8a-115">Перейдите в раздел **Рабочие области \> Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-115">Go to **Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="e2f8a-116">Выполните поиск на вкладке **Создание согласованного формата кода ссылки для канала по каналам**.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-116">Search for the **Generate a consistent channel reference ID format across channels** feature.</span></span> 
3. <span data-ttu-id="e2f8a-117">Выберите функцию, затем в области свойств выберите **Включить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-117">Select the feature, and then select **Enable now** in the properties pane.</span></span> 

## <a name="create-a-check-in-confirmation-page"></a><span data-ttu-id="e2f8a-118">Создание страницы подтверждения прибытия</span><span class="sxs-lookup"><span data-stu-id="e2f8a-118">Create a check-in confirmation page</span></span>

<span data-ttu-id="e2f8a-119">На веб-сайте электронной коммерции необходимо создать новую страницу, которая будет использоваться в качестве подтверждения прибытия.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-119">On your e-commerce site, you must create a new page that will serve as the check-in confirmation experience.</span></span> <span data-ttu-id="e2f8a-120">С помощью дополнительной настройки страница также может включать в себя форму, которая собирает дополнительные сведения от клиентов, чтобы облегчить выполнение заказа.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-120">Through additional configuration, the page can also include a form that collects additional information from customers to facilitate order fulfillment.</span></span> <span data-ttu-id="e2f8a-121">Сведения о настройке страницы и модуля см. в разделе [Модуль прибытия клиента](check-in-pickup-module.md).</span><span class="sxs-lookup"><span data-stu-id="e2f8a-121">For information about how to set up the page and module, see [Customer check-in module](check-in-pickup-module.md).</span></span>

## <a name="configure-the-transactional-email-template"></a><span data-ttu-id="e2f8a-122">Настройка шаблона транзакционных писем</span><span class="sxs-lookup"><span data-stu-id="e2f8a-122">Configure the transactional email template</span></span>

<span data-ttu-id="e2f8a-123">Необходимо добавить ссылку или кнопку **Я здесь** в шаблон для транзакционного письма, которое клиенты получают, когда их заказ готов к отправке.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-123">You must add an **I am here** link or button to the template for the transactional email that customers receive when their order is ready for pickup.</span></span> <span data-ttu-id="e2f8a-124">Клиенты будут использовать эту ссылку или кнопку для уведомления магазина о том, что они прибыли забрать свой заказ.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-124">Customers will use this link or button to notify the store that they have arrived to pick up their order.</span></span> 

<span data-ttu-id="e2f8a-125">Добавьте ссылку или кнопку в шаблон, который сопоставлен с типом уведомления **Упаковка завершена** и режимом доставки, используемым для выполнения заказа самовывоза.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-125">Add the link or button to the template that is mapped to the **Packing completed** notification type and the mode of delivery that you're using for curbside order fulfillment.</span></span> <span data-ttu-id="e2f8a-126">В шаблоне создайте HTML-ссылку или кнопку, указывающую на URL-адрес созданной страницы подтверждения прибытия.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-126">In the template, create an HTML link or button that points to the URL of the check-in confirmation page that you created.</span></span> <span data-ttu-id="e2f8a-127">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="e2f8a-127">Here is an example.</span></span>

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
<span data-ttu-id="e2f8a-128">Дополнительные сведения о настройке шаблонов электронной почты см. в разделе [Настройка транзакционных писем по режиму доставки](customize-email-delivery-mode.md).</span><span class="sxs-lookup"><span data-stu-id="e2f8a-128">For more information about how to configure email templates, see [Customize transactional emails by mode of delivery](customize-email-delivery-mode.md).</span></span> 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a><span data-ttu-id="e2f8a-129">Задача подтверждения прибытия создается в POS</span><span class="sxs-lookup"><span data-stu-id="e2f8a-129">A check-in confirmation task is created in POS</span></span>

<span data-ttu-id="e2f8a-130">После того как клиент сообщит магазину о своем прибытии, он получит уведомление о подтверждении прибытия, задача создается в списке задач в POS для магазина, в котором клиент забирает заказ.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-130">After a customer notifies the store that they are present for pickup, they receive a check-in confirmation notification, and a task is created in the tasks list in POS for the store where the customer is picking up the order.</span></span> <span data-ttu-id="e2f8a-131">Задача содержит все сведения о клиенте и заказе, необходимые для выполнения заказа.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-131">The task contains all the customer and order information that is required to fulfill the order.</span></span> <span data-ttu-id="e2f8a-132">В поле задачи в окне инструкции отображается вся информация, которая была собрана от клиента через форму дополнительной информации.</span><span class="sxs-lookup"><span data-stu-id="e2f8a-132">In the task, the instructions field shows any information that was collected from the customer through the additional information form.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="e2f8a-133">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e2f8a-133">Additional resources</span></span>

[<span data-ttu-id="e2f8a-134">Модуль прибытия для отправки</span><span class="sxs-lookup"><span data-stu-id="e2f8a-134">Check-in for pickup module</span></span>](check-in-pickup-module.md)
