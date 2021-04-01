---
title: Приостановка и возобновление транзакции в POS
description: В этом разделе объясняется, как пользователи могут приостановить выполняющиеся транзакции и возобновить их позже или на другой ККМ с помощью Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fb92de200690b03a55a3a173fd433478c8e3175d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231280"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a><span data-ttu-id="f0cf0-103">Приостановка и возобновление транзакции в POS</span><span class="sxs-lookup"><span data-stu-id="f0cf0-103">Suspend and resume a transaction in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="f0cf0-104">Пользователи POS могут приостановить выполняющиеся транзакции и возобновить их позже или на другой ККМ.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="f0cf0-105">Транзакции часто приостанавливаются, чтобы быстро освободить ККМ для другой задачи, не теряя никаких действий для текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="f0cf0-106">Например, сотрудник магазина начинает обрабатывать транзакцию клиента на мобильном устройстве, но должен завершить ее на ККМ с кассовым лотком.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="f0cf0-107">В этом случае сотрудник магазина может приостановить проводку на мобильном устройстве, затем вызвать и возобновить ее на ККМ.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="f0cf0-108">Настройка функции приостановки и возобновления</span><span class="sxs-lookup"><span data-stu-id="f0cf0-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="f0cf0-109">Операции POS</span><span class="sxs-lookup"><span data-stu-id="f0cf0-109">POS operations</span></span>

<span data-ttu-id="f0cf0-110">Два [операции POS](pos-operations.md) позволяют POS поддерживать сценарии приостановки и возобновления.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="f0cf0-111">Можно назначить эти операции [сеткам кнопок](pos-screen-layouts.md) на странице проводки или странице приветствия.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="f0cf0-112">503: Приостановить проводку</span><span class="sxs-lookup"><span data-stu-id="f0cf0-112">503: Suspend transaction</span></span>
- <span data-ttu-id="f0cf0-113">504: Вызвать проводку</span><span class="sxs-lookup"><span data-stu-id="f0cf0-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="f0cf0-114">Шаблон чека</span><span class="sxs-lookup"><span data-stu-id="f0cf0-114">Receipt template</span></span>

<span data-ttu-id="f0cf0-115">POS можно настроить для создания печатного бланка при приостановке транзакции.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="f0cf0-116">Затем этот бланк можно использовать для быстрого определения и вызова проводки в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="f0cf0-117">Чтобы включить в POS печать бланка, необходимо добавить формат чека **Приостановленная проводка** в профиль чеков магазина.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="f0cf0-118">Можно разработать формат чека, чтобы он включал или исключал конкретные сведения о проводке.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="f0cf0-119">Например, формат может включать штрих-код для поддержки сканирования.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="f0cf0-120">Нумерация чеков</span><span class="sxs-lookup"><span data-stu-id="f0cf0-120">Receipt numbering</span></span>

<span data-ttu-id="f0cf0-121">Как и для других типов проводок POS, создающих печатный чек, можно определить номерную серию для приостановленных проводок в разделе **Нумерация чеков** профиля функциональности для магазина.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="f0cf0-122">Аннулировать при закрытии смены</span><span class="sxs-lookup"><span data-stu-id="f0cf0-122">Void when closing shift</span></span>

<span data-ttu-id="f0cf0-123">Можно использовать параметр **Аннулировать при закрытии смены**, чтобы пользователи либо завершали, либо аннулировали все приостановленные проводки до закрытия своей смены.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="f0cf0-124">Во время операции **Закрыть смену** POS будет предлагать пользователям либо просмотреть, либо аннулировать все ожидающие приостановленные проводки.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="f0cf0-125">Приостановка и возобновление проводки</span><span class="sxs-lookup"><span data-stu-id="f0cf0-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="f0cf0-126">Приостановка проводки</span><span class="sxs-lookup"><span data-stu-id="f0cf0-126">Suspend a transaction</span></span>

<span data-ttu-id="f0cf0-127">Пользователи, которые имеют достаточные права и макета экрана которых включает операцию **Приостановить проводку**, могут приостановить проводку, чтобы вызвать ее позже или на другой ККМ.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="f0cf0-128">Проводки можно приостановить только в том случае, если они **не** содержат следующие типы строк:</span><span class="sxs-lookup"><span data-stu-id="f0cf0-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="f0cf0-129">Активные строки платежа</span><span class="sxs-lookup"><span data-stu-id="f0cf0-129">Active payment lines</span></span>
- <span data-ttu-id="f0cf0-130">Строки подарочных сертификатов (либо по выдаче подарочного сертификата, либо по пополнению сальдо подарочного сертификата)</span><span class="sxs-lookup"><span data-stu-id="f0cf0-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="f0cf0-131">Приостановленная проводка не влияет на сведения о продажах или сведения о доступности запасов в магазине.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="f0cf0-132">Возобновление приостановленной проводки</span><span class="sxs-lookup"><span data-stu-id="f0cf0-132">Resume a suspended transaction</span></span>

<span data-ttu-id="f0cf0-133">Приостановленные проводки можно вызвать и возобновить в том же магазине любым пользователем, который имеет достаточно прав, а также макет экрана которого включает в себя операцию **Отозвать проводку**.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="f0cf0-134">Чтобы быстро и легко вызвать приостановленную проводку, выполните сканирование штрих-кода на напечатанном бланке во время просмотра списка проводок из операции **Отозвать проводку**.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="f0cf0-135">Вопросы для автономного режима</span><span class="sxs-lookup"><span data-stu-id="f0cf0-135">Considerations for offline mode</span></span>

- <span data-ttu-id="f0cf0-136">Любая проводка, приостановленная в то время, когда POS работает в интерактивном режиме, не может быть возобновлена в автономном режиме, поскольку данные не синхронизированы с автономной базой данных.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="f0cf0-137">Если проводка была приостановлена, когда POS находился в автономном режиме, можно вызвать проводку в автономном режиме, при условии, что POS не был переключен обратно в интерактивный режим в любое время с момента приостановки проводки.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="f0cf0-138">Когда POS переключается обратно в интерактивный режим, данные о приостановленных проводках перемещаются в оперативную базу данных и удаляются из базы данных автономного режима.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="f0cf0-139">Таким образом, эти проводки можно возобновить только в интерактивном режиме.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="f0cf0-140">При переключении POS обратно в автономный режим вы не сможете возобновить эти приостановленные проводки, поскольку они уже были удалены из базы данных автономного режима.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="f0cf0-141">Аннулирование приостановленной проводки</span><span class="sxs-lookup"><span data-stu-id="f0cf0-141">Void a suspended transaction</span></span>

<span data-ttu-id="f0cf0-142">Можно аннулировать приостановленные проводки, либо вызвав проводку с последующим выполнением операции **Аннулировать проводку**, либо выбрав проводку в списке **Отозвать проводку** и выбрав **Аннулировать** на панели приложения.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="f0cf0-143">Кроме того, можно настроить магазин, чтобы пользователям предлагалось аннулировать приостановленные проводки при закрытии смены.</span><span class="sxs-lookup"><span data-stu-id="f0cf0-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]