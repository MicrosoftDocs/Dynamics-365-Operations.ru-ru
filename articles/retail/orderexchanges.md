---
title: "Настройка и обработка обмена по заказу на возврат"
description: "В этом разделе описан порядок настройки обмена при возврате в Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3331b984693c58c6ee8c49b98ed7d3a8df5b79ff
ms.openlocfilehash: 45b628376a483d3d639e5c018dd93570ed8ce7af
ms.contentlocale: ru-ru
ms.lasthandoff: 12/04/2018

---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="2471a-103">Настройка и обработка обмена по заказу на возврат</span><span class="sxs-lookup"><span data-stu-id="2471a-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2471a-104">В предыдущих версиях Microsoft Dynamics 365 for Retail возвраты по заказам клиентов обрабатывались с помощью документа заказа на возврат в разделе "Розничная сеть - Центральный офис".</span><span class="sxs-lookup"><span data-stu-id="2471a-104">In previous versions of Microsoft Dynamics 365 for Retail, returns against customer orders were processed by using the return order document in Retail headquarters.</span></span> <span data-ttu-id="2471a-105">Тем не менее с помощью документа заказа на возврат можно обрабатывать только возвращаемые продукты.</span><span class="sxs-lookup"><span data-stu-id="2471a-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="2471a-106">Возвращаемые продукты можно определить по отрицательному количеству в строках заказа на возврат.</span><span class="sxs-lookup"><span data-stu-id="2471a-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="2471a-107">Продажам же, наоборот, соответствуют положительные количества.</span><span class="sxs-lookup"><span data-stu-id="2471a-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="2471a-108">Однако документ заказа на возврат не поддерживает положительные количества.</span><span class="sxs-lookup"><span data-stu-id="2471a-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="2471a-109">Из-за этого ограничения предыдущие версии Retail не поддерживают ситуации, когда с помощью документа заказа на возврат осуществляется обмен продукта.</span><span class="sxs-lookup"><span data-stu-id="2471a-109">Because of this limitation, previous versions of Retail didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="2471a-110">Поэтому была добавлена поддержка сценариев, в которых с помощью заказов на возврат выполняется обмен.</span><span class="sxs-lookup"><span data-stu-id="2471a-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="2471a-111">Теперь в Retail для обработки таких транзакций используется документ заказа на продажу, а не документ заказа на возврат.</span><span class="sxs-lookup"><span data-stu-id="2471a-111">Retail now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a><span data-ttu-id="2471a-112">Настройка Retail для поддержки обмена по заказам на возврат</span><span class="sxs-lookup"><span data-stu-id="2471a-112">Configure Retail to support exchanges on return orders</span></span>

<span data-ttu-id="2471a-113">Чтобы настроить в системе поддержку обмена по заказам на возврат, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2471a-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="2471a-114">Перейдите в раздел **Розничная торговля \> Настройка центрального офиса \> Параметры \> Параметры розничной торговли**.</span><span class="sxs-lookup"><span data-stu-id="2471a-114">Go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="2471a-115">На экспресс-вкладке **Клиентские заказы** для параметра **Обрабатывать заказы на возврат как заказы на продажу** установите значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="2471a-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="2471a-116">Запустите задание **График распределения глобальной конфигурации** (**1110**).</span><span class="sxs-lookup"><span data-stu-id="2471a-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="2471a-117">Обработка обмена</span><span class="sxs-lookup"><span data-stu-id="2471a-117">Make an exchange</span></span>

<span data-ttu-id="2471a-118">После настройки системы, как было описано выше, пользователь POS для обработки возврата должен будет выбирать заказ на продажу или накладную по продаже, как и в предыдущих версиях Retail.</span><span class="sxs-lookup"><span data-stu-id="2471a-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of Retail.</span></span> <span data-ttu-id="2471a-119">Однако после добавления возвращаемых номенклатур в корзину пользователь теперь имеет возможность добавить в корзину новые строки продажи.</span><span class="sxs-lookup"><span data-stu-id="2471a-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="2471a-120">Для них он должен определить все обязательные атрибуты, чтобы обработать строку заказа клиента.</span><span class="sxs-lookup"><span data-stu-id="2471a-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="2471a-121">К таким атрибутам относятся метод доставки и точка выполнения.</span><span class="sxs-lookup"><span data-stu-id="2471a-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="2471a-122">Сумма платежа по транзакции будет равна разности между строками заказа на возврат и заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="2471a-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="2471a-123">При приеме платежа заказ на возврат будет разнесен как документ заказа на продажу в разделе "Розничная сеть - Центральный офис", и система сразу же сформирует накладную по строкам возврата.</span><span class="sxs-lookup"><span data-stu-id="2471a-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Retail headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="2471a-124">Чтобы сделать более наглядным представление различных сумм в корзине, в корзину были добавлены три новые поля суммы.</span><span class="sxs-lookup"><span data-stu-id="2471a-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="2471a-125">Чтобы они были доступны в пользовательском интерфейсе POS, воспользуйтесь конструктором экрана.</span><span class="sxs-lookup"><span data-stu-id="2471a-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="2471a-126">**Примененный депозит** — сумма депозита, применяемая к транзакции, когда пользователь отправляет клиентский заказ.</span><span class="sxs-lookup"><span data-stu-id="2471a-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="2471a-127">Если депозит не переопределен и настроен депозит в размере 10 процентов, то сумма в этом поле равняется 90 процентам от общей суммы клиентского заказа.</span><span class="sxs-lookup"><span data-stu-id="2471a-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="2471a-128">**Сумма "На вынос"**  — общая сумма строк, для которых при создании или изменении клиентского заказа, а также во время обмена клиентского заказа был выбран режим доставки для **На вынос**.</span><span class="sxs-lookup"><span data-stu-id="2471a-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="2471a-129">Сумма в этом поле включает налоги и сборы.</span><span class="sxs-lookup"><span data-stu-id="2471a-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="2471a-130">**Сумма возврата** — общая сумма строк с отрицательными количествами при обмене клиентского заказа.</span><span class="sxs-lookup"><span data-stu-id="2471a-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="2471a-131">Сумма в этом поле включает налоги и сборы.</span><span class="sxs-lookup"><span data-stu-id="2471a-131">The amount in this field includes taxes and charges.</span></span>

