---
title: Изменение способа поставки в POS-терминале
description: В этом разделе описывается, как настроить и использовать операцию изменения режима поставки в POS-терминале.
author: hhainesms
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: fd69d82536047c06e94ba4a7e860ef54680619a4
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193139"
---
# <a name="change-mode-of-delivery-in-pos"></a><span data-ttu-id="03a83-103">Изменение способа поставки в POS-терминале</span><span class="sxs-lookup"><span data-stu-id="03a83-103">Change mode of delivery in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="03a83-104">В этом разделе описывается, как настроить и использовать функцию "изменение режима поставки" в среде POS-терминала.</span><span class="sxs-lookup"><span data-stu-id="03a83-104">This topic describes how to set up and use the "change mode of delivery" functionality in your point of sale (POS) environment.</span></span> 

<span data-ttu-id="03a83-105">В Dynamics 365 Commerce версии 10.0.10 и более поздних операция **Изменить способ поставки** (647) доступна для добавления на макеты экрана POS-терминала.</span><span class="sxs-lookup"><span data-stu-id="03a83-105">In Dynamics 365 Commerce versions 10.0.10 and later, the **Change mode of delivery** operation (647) is available to add to your POS screen layouts.</span></span>

<span data-ttu-id="03a83-106">Функция изменения режима поставки предоставляет возможность изменить способ поставки для одной или нескольких строк продаж, настроенных для поставки, в POS-проводке.</span><span class="sxs-lookup"><span data-stu-id="03a83-106">The change mode of delivery feature provides you with the option to change the mode of delivery for one or more shipment-configured sales lines on the POS transaction.</span></span> <span data-ttu-id="03a83-107">В предыдущих версиях Commerce необходимо было выполнить полные потоки конфигурации **Отгрузить все** и **Отгрузить выбранное**, если необходимо изменить способ поставки в существующей строке, которая была настроена для отгрузки.</span><span class="sxs-lookup"><span data-stu-id="03a83-107">In previous versions of Commerce, you had to go through the full **Ship all** or **Ship selected** configuration flows if you wanted to change the mode of delivery on an existing line that was configured for shipment.</span></span> <span data-ttu-id="03a83-108">Этот процесс требует много времени и может привести к случайным изменениям происхождения поставки или дат поставки для строки.</span><span class="sxs-lookup"><span data-stu-id="03a83-108">This process was time consuming and could result in accidental changes to the delivery origin or delivery dates for the line.</span></span> <span data-ttu-id="03a83-109">Новая функциональность предоставляет альтернативный метод эффективного обновления способа поставки по этим строкам продаж.</span><span class="sxs-lookup"><span data-stu-id="03a83-109">The new functionality provides an alternative method for efficiently updating the mode of delivery on these sales lines.</span></span>

<span data-ttu-id="03a83-110">Дополнительные сведения о порядке добавления операции в кнопку в сетке кнопок POS-терминала см. в разделе [Макеты экрана для POS-терминала](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="03a83-110">For more information about how to add an operation to a button on your POS button grid, see [Screen layouts for the point of sale](pos-screen-layouts.md).</span></span>

<span data-ttu-id="03a83-111">После того, как эта функция будет настроена в POS-терминале, при выборе команды **Изменить способ поставки** будет открыта страница со списком, в которой можно выбрать строки проводки, для которой требуется изменить режим поставки.</span><span class="sxs-lookup"><span data-stu-id="03a83-111">After this feature is configured in POS, when you select **Change mode of delivery**, you will be presented with a list page that allows you to choose the lines of the transaction that you want to change the mode of delivery for.</span></span> <span data-ttu-id="03a83-112">Можно выбрать некоторые или все строки или выйти без внесения каких-либо изменений.</span><span class="sxs-lookup"><span data-stu-id="03a83-112">You can choose some or all of the lines, or exit without making any changes.</span></span> <span data-ttu-id="03a83-113">Строки продажи, которые ранее были настроены для отгрузки, являются единственными строками в списке, которые можно изменить.</span><span class="sxs-lookup"><span data-stu-id="03a83-113">The sales lines that were previously configured for shipment are the only lines in the list that you can change.</span></span> <span data-ttu-id="03a83-114">Если необходимо изменить строку, назначенную для получения в магазине или на вынос для отправки, следует использовать операции **Отгрузить все** или **Отгрузить выбранное**.</span><span class="sxs-lookup"><span data-stu-id="03a83-114">If you want to change a line designated for pickup or carryout to ship, you must use the **Ship all** or **Ship selected** operations.</span></span> <span data-ttu-id="03a83-115">И наоборот, если необходимо изменить строку, обозначенную как отгрузка для получения в магазине или на вынос, следует использовать операции **Забрать все**, **Забрать выбранное**, **На вынос все** или **На вынос выбранное**.</span><span class="sxs-lookup"><span data-stu-id="03a83-115">Conversely, if you want to change a line designated as a shipment to a pickup or carryout, you must use the  **Pickup all**, **Pickup selected**, **Carryout all**, or **Carryout selected** operations.</span></span>

<span data-ttu-id="03a83-116">После выбора строк, которые необходимо изменить, щелкните **Изменить способ поставки**, и будет предложено выбрать вариант способа поставки.</span><span class="sxs-lookup"><span data-stu-id="03a83-116">After you select the lines that you want to change, click **Change mode of delivery** to be prompted to select the delivery mode options.</span></span> <span data-ttu-id="03a83-117">Если для изменения выбрано несколько строк, в POS-терминале будут отображены только режимы доставки, которые были настроены как допустимые для всех выбранных продуктов.</span><span class="sxs-lookup"><span data-stu-id="03a83-117">If you selected multiple lines to change, POS will only display modes of delivery that have been configured as allowable for all of the selected products.</span></span> <span data-ttu-id="03a83-118">Способы поставки могут быть настроены для поддержки различных продуктов и адресов поставки.</span><span class="sxs-lookup"><span data-stu-id="03a83-118">Modes of delivery can be configured to support specific products and delivery addresses.</span></span> <span data-ttu-id="03a83-119">Если имеется способ доставки, допустимый для одной комбинации продукта и адреса, но неприемлемый для другого выбранного сочетания продукта и адреса, этот режим доставки будет недоступен.</span><span class="sxs-lookup"><span data-stu-id="03a83-119">If there is a mode of delivery that is acceptable for one product and address combination but is not acceptable for another selected product and address combination, the mode of delivery is not available.</span></span> <span data-ttu-id="03a83-120">Возможно, потребуется выбрать строки по одной и изменить режим доставки для каждой строки отдельно, если требуется выбрать режим поставки для одного продукта, который не поддерживается другим продуктом.</span><span class="sxs-lookup"><span data-stu-id="03a83-120">You may need to select lines one by one and change the mode of delivery for each line separately if you want to select a mode of delivery for one product that is not supported by another product.</span></span>  

<span data-ttu-id="03a83-121">После выбора нового способа поставки отображается страница проводки.</span><span class="sxs-lookup"><span data-stu-id="03a83-121">After you select the new mode of delivery, the transaction page is displayed.</span></span> <span data-ttu-id="03a83-122">Для просмотра нового выбора режима поставки выберите вкладку **Поставка** в списке проводок.</span><span class="sxs-lookup"><span data-stu-id="03a83-122">To review your new delivery mode selections, select the **Delivery** tab on the transaction list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03a83-123">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="03a83-123">Additional resources</span></span>

[<span data-ttu-id="03a83-124">Создание заказов центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="03a83-124">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="03a83-125">Настройка транзакционных писем по способу доставки</span><span class="sxs-lookup"><span data-stu-id="03a83-125">Customize transactional emails by mode of delivery</span></span>](customize-email-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]