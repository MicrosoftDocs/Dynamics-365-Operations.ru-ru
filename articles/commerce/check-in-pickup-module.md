---
title: Модуль прибытия для отправки
description: В этом разделе описывается модуль прибытия для отправки, а также описывается, как настраивать его в Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e7bae4ae7c2f3367132b03accb31c01c5f3b673e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937613"
---
# <a name="check-in-for-pickup-module"></a><span data-ttu-id="1eb60-103">Модуль прибытия для отправки</span><span class="sxs-lookup"><span data-stu-id="1eb60-103">Check-in for pickup module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="1eb60-104">В этом разделе описывается модуль прибытия для отправки, а также описывается, как настраивать его в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1eb60-104">This topic covers the check-in for pickup module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1eb60-105">Модуль прибытия для отправки содержит страницу подтверждения для клиентов, использующих возможности прибытия клиента Dynamics 365 Commerce для уведомления магазина о своем прибытии.</span><span class="sxs-lookup"><span data-stu-id="1eb60-105">The check-in for pickup module provides a confirmation page for customers who use the Dynamics 365 Commerce customer check-in capabilities to notify a store about their arrival.</span></span> <span data-ttu-id="1eb60-106">Модуль прибытия для отправки также позволяет настроить форму, которая собирает дополнительную информацию от клиентов, чтобы упростить доставку заказа.</span><span class="sxs-lookup"><span data-stu-id="1eb60-106">The check-in for pickup module also lets you configure a form that collects additional information from customers to facilitate order delivery.</span></span> <span data-ttu-id="1eb60-107">Эти сведения включают номер места парковки клиента, а также марку и модель автомобиля.</span><span class="sxs-lookup"><span data-stu-id="1eb60-107">This information includes a customer's parking spot number, and the make and model of their vehicle.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="1eb60-108">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="1eb60-108">Module properties</span></span>

| <span data-ttu-id="1eb60-109">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="1eb60-109">Property name</span></span> | <span data-ttu-id="1eb60-110">Значения</span><span class="sxs-lookup"><span data-stu-id="1eb60-110">Values</span></span> | <span data-ttu-id="1eb60-111">описание</span><span class="sxs-lookup"><span data-stu-id="1eb60-111">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="1eb60-112">Текст подтверждения</span><span class="sxs-lookup"><span data-stu-id="1eb60-112">Confirmation text</span></span> | <span data-ttu-id="1eb60-113">Текстовая строка</span><span class="sxs-lookup"><span data-stu-id="1eb60-113">Text string</span></span> | <span data-ttu-id="1eb60-114">Содержимое заголовка, которое отображается на странице подтверждения прибытия.</span><span class="sxs-lookup"><span data-stu-id="1eb60-114">Content for the heading that appears on the check-in confirmation page.</span></span> |
| <span data-ttu-id="1eb60-115">Показать QR-код</span><span class="sxs-lookup"><span data-stu-id="1eb60-115">Show QR code</span></span> | <span data-ttu-id="1eb60-116">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="1eb60-116">**True** or **False**</span></span> | <span data-ttu-id="1eb60-117">Если это свойство задано как **Истина**, страница подтверждения прибытия показывает QR-код, который представляет код подтверждения заказа.</span><span class="sxs-lookup"><span data-stu-id="1eb60-117">When this property is set to **True**, the check-in confirmation page shows a QR code that represents the order confirmation ID.</span></span> |
| <span data-ttu-id="1eb60-118">Заголовок дополнительных сведений</span><span class="sxs-lookup"><span data-stu-id="1eb60-118">Additional information heading</span></span> | <span data-ttu-id="1eb60-119">Текстовая строка</span><span class="sxs-lookup"><span data-stu-id="1eb60-119">Text string</span></span> | <span data-ttu-id="1eb60-120">Содержимое заголовка, которое появляется при настройке полей дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="1eb60-120">Content for the heading that appears when additional information fields have been configured.</span></span> |
| <span data-ttu-id="1eb60-121">Ключи дополнительных сведений</span><span class="sxs-lookup"><span data-stu-id="1eb60-121">Additional information keys</span></span> | <span data-ttu-id="1eb60-122">Пара код ресурса/значение ресурса</span><span class="sxs-lookup"><span data-stu-id="1eb60-122">Resource ID/resource value pair</span></span> | <span data-ttu-id="1eb60-123">Каждый ключ создает поле формы и связанную с ним метку, которые используются для сбора дополнительной информации от клиентов.</span><span class="sxs-lookup"><span data-stu-id="1eb60-123">Each key creates a form field and an associated label that are used to collect additional information from customers.</span></span> |
| <span data-ttu-id="1eb60-124">Ключ дополнительных сведений \> код ресурса</span><span class="sxs-lookup"><span data-stu-id="1eb60-124">Additional information keys \> Resource ID</span></span> | <span data-ttu-id="1eb60-125">Текстовая строка</span><span class="sxs-lookup"><span data-stu-id="1eb60-125">Text string</span></span> | <span data-ttu-id="1eb60-126">Каждый ключ информации создает поле формы и связанную с ним метку, которые используются для сбора дополнительной информации от клиентов.</span><span class="sxs-lookup"><span data-stu-id="1eb60-126">Each information key creates a form field and an associated label that are used to collect additional information from customers.</span></span> <span data-ttu-id="1eb60-127">Это свойство определяет ключ дополнительной информации.</span><span class="sxs-lookup"><span data-stu-id="1eb60-127">This property identifies the additional information key.</span></span> <span data-ttu-id="1eb60-128">В задаче, созданной в POS, значение этого свойства отображается как метка в поле инструкций.</span><span class="sxs-lookup"><span data-stu-id="1eb60-128">In the task that is created in point of sale (POS), the value of this property is shown as the label in the instructions field.</span></span> |
| <span data-ttu-id="1eb60-129">Ключ дополнительных сведений \> Значение ресурса</span><span class="sxs-lookup"><span data-stu-id="1eb60-129">Additional information keys \> Resource value</span></span> | <span data-ttu-id="1eb60-130">Текстовая строка</span><span class="sxs-lookup"><span data-stu-id="1eb60-130">Text string</span></span> | <span data-ttu-id="1eb60-131">Метка для текстового поля в задаче в POS.</span><span class="sxs-lookup"><span data-stu-id="1eb60-131">The label for the text field in the task in POS.</span></span> |
| <span data-ttu-id="1eb60-132">Ключи дополнительных сведений \> Требуемый</span><span class="sxs-lookup"><span data-stu-id="1eb60-132">Additional information keys \> Required</span></span> | <span data-ttu-id="1eb60-133">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="1eb60-133">**True** or **False**</span></span> | <span data-ttu-id="1eb60-134">Это свойство определяет, должны ли клиенты заполнять поле формы до того, как они смогут продолжать работу.</span><span class="sxs-lookup"><span data-stu-id="1eb60-134">This property specifies whether customers must fill in the form field before they can continue.</span></span> <span data-ttu-id="1eb60-135">Если это свойство имеет значение **Истина**, рядом с подписью формы отображается звездочка, а проверка пустого значения выполняется, чтобы предотвратить продолжение работы клиента, если не введено значение.</span><span class="sxs-lookup"><span data-stu-id="1eb60-135">When this property is set to **True**, an asterisk is rendered next to the form label, and a null check is done to prevent customers from continuing if no value is entered.</span></span> |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a><span data-ttu-id="1eb60-136">Добавление модуля прибытия для отправки на страницу</span><span class="sxs-lookup"><span data-stu-id="1eb60-136">Add the check-in for pickup module to a page</span></span>

<span data-ttu-id="1eb60-137">Модуль прибытия для отправки необходимо добавить на новую страницу, созданную для подтверждения прибытия.</span><span class="sxs-lookup"><span data-stu-id="1eb60-137">The check-in for pickup module should be added to the new page that you create for check-in confirmation.</span></span> <span data-ttu-id="1eb60-138">Эта страница будет служить в качестве подтверждения прибытия для клиентов, которые выбирают **Я здесь** или кнопку в их электронной почте.</span><span class="sxs-lookup"><span data-stu-id="1eb60-138">That page will serve as the check-in confirmation experience for customers who select the **I am here** link or button in their email.</span></span> 

## <a name="configure-the-additional-information-form"></a><span data-ttu-id="1eb60-139">Настройка формы дополнительной информации</span><span class="sxs-lookup"><span data-stu-id="1eb60-139">Configure the additional information form</span></span>

<span data-ttu-id="1eb60-140">По умолчанию, если не настроены ключи дополнительной информации, в модуле отображается страница подтверждения прибытия клиента.</span><span class="sxs-lookup"><span data-stu-id="1eb60-140">By default, if no additional information keys are configured, the module shows customers the check-in confirmation page.</span></span> <span data-ttu-id="1eb60-141">Когда отображается подтверждение прибытия, в POS создается задача для магазина, в котором выполняется комплектация заказа.</span><span class="sxs-lookup"><span data-stu-id="1eb60-141">As the check-in confirmation is shown, a task is created in POS for the store where the order is being picked up.</span></span>

<span data-ttu-id="1eb60-142">Когда настроен один или несколько ключей дополнительной информации, клиентам сначала выводится запрос на ввод данных.</span><span class="sxs-lookup"><span data-stu-id="1eb60-142">When one or more additional information keys are configured, customers are first prompted to enter information.</span></span> <span data-ttu-id="1eb60-143">При выборе **Отправить** они отображаются с подтверждением прибытия, и задача создается в POS.</span><span class="sxs-lookup"><span data-stu-id="1eb60-143">When they select **Submit**, they are shown the check-in confirmation, and a task is created in POS.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="1eb60-144">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1eb60-144">Additional resources</span></span>

[<span data-ttu-id="1eb60-145">Включение уведомлений о прибытии клиентов в POS</span><span class="sxs-lookup"><span data-stu-id="1eb60-145">Enable customer check-in notifications in point of sale (POS)</span></span>](enable-customer-check-in.md)
