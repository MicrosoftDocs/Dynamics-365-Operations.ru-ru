---
title: Реверсирование разнесенных проводок по аренде
description: В этой теме объясняется, как сторнировать разнесенную проводку по аренде. Любая проводка, созданная через модуль аренды активов, может быть реверсирована.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 259fd8f41eade1e873225f0d95c499c8cb8c1a6a
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4447402"
---
# <a name="reverse-posted-lease-transactions"></a><span data-ttu-id="0c6a7-104">Реверсирование разнесенных проводок по аренде</span><span class="sxs-lookup"><span data-stu-id="0c6a7-104">Reverse posted lease transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c6a7-105">Любая проводка, созданная через модуль аренды активов, может быть реверсирована.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-105">Any transaction that is created through Asset leasing can be reversed.</span></span> <span data-ttu-id="0c6a7-106">Проводки, сторнированные через модуль аренды активов, обновляют данные аренды.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-106">Transactions that are reversed through Asset leasing update your lease data.</span></span> <span data-ttu-id="0c6a7-107">Таким образом, они также обновляют учетные стоимости арендного обязательства и актива в форме права пользования (ФПП).</span><span class="sxs-lookup"><span data-stu-id="0c6a7-107">Therefore, they also update the carrying values of the lease liability and right-of-use (ROU) asset.</span></span>

<span data-ttu-id="0c6a7-108">Чтобы создать сторнирование проводки для аренды, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-108">To create a reversing transaction for a lease, follow these steps.</span></span>

1. <span data-ttu-id="0c6a7-109">На странице **Проводки по активам** или **Проводки по обязательствам** выберите проводку, а затем выберите **Сторнировать проводку**.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-109">On either the **Asset transactions** page or the **Liability transactions** page, select the transaction, and then select **Reverse transaction**.</span></span>
2. <span data-ttu-id="0c6a7-110">В появившемся диалоговом окне можно изменить дату, когда будет разнесена операция сторнирования.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-110">In the dialog box that appears, you can edit the date when the reversing entry will be posted.</span></span> <span data-ttu-id="0c6a7-111">По умолчанию поле **Дата** устанавливается равным дате разноски проводки для выбранной проводки.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-111">By default, the **Date** field is set to the transaction posting date of the transaction that you selected.</span></span> <span data-ttu-id="0c6a7-112">Запись сторнирования не может быть разнесена раньше исходной даты разноски для выбранной проводки.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-112">The reversing entry can't be posted earlier than the original posting date of the selected transaction.</span></span>
3. <span data-ttu-id="0c6a7-113">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-113">Select **OK**.</span></span> <span data-ttu-id="0c6a7-114">Запись журнала разносится, которая сторнирует выбранную запись.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-114">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="0c6a7-115">Сторнирование отображается на странице **Проводки по активам** или **Проводки по обязательствам**, и чистая сумма текущего сальдо, отображаемая на странице, обновляется.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-115">The reversal is shown on the **Asset transactions** or **Liability transactions** page, and the net total of the current balance that is shown on the page is updated.</span></span>

<span data-ttu-id="0c6a7-116">При выборе пункта **Трассировка сторнирования** отображается диалоговое окно, в котором отображаются как оригинальные проводки, так и сторнированные проводки вместе со связанным номером, который называется *номером трассировки*.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-116">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked number that is known as a *trace number*.</span></span> <span data-ttu-id="0c6a7-117">Чтобы упростить понимание сторнирований и повысить видимость, можно также отслеживать сторнирования с помощью расписаний аренды.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-117">To make the reversals easier to understand and to improve visibility, you can also track reversals by using the lease schedules.</span></span>

<span data-ttu-id="0c6a7-118">В поле **Последний номер журнала** на странице **График** отображаются номера журналов проводок.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-118">The **Latest journal number** field on the **Schedule** page shows the journal numbers of transactions.</span></span> <span data-ttu-id="0c6a7-119">При сторнировании проводки это поле обновляется номером журнала сторнирующей проводки.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-119">When a transaction is reversed, this field is updated with the journal number of a reversing transaction.</span></span> <span data-ttu-id="0c6a7-120">Кроме того, устанавливается флажок **Сторнировано**, чтобы указать, что проводка сторнирована, и выбрано поле **Разнесено**.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-120">Additionally, the **Reversed** check box is selected to indicate that the transaction is reversed, and the **Posted** field is selected.</span></span>

## <a name="revoke-a-reversed-transaction"></a><span data-ttu-id="0c6a7-121">Отмена реверсированной проводки</span><span class="sxs-lookup"><span data-stu-id="0c6a7-121">Revoke a reversed transaction</span></span>

<span data-ttu-id="0c6a7-122">Чтобы отменить сторнированную проводку, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-122">To revoke a reversed transaction, follow these steps.</span></span>

1. <span data-ttu-id="0c6a7-123">На странице **График** или на странице **Проводки** выберите исходную проводку.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-123">On either the **Schedule** page or the **Transactions** page, select the original transaction.</span></span>
2. <span data-ttu-id="0c6a7-124">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-124">Follow one of these steps:</span></span>

    - <span data-ttu-id="0c6a7-125">Если вы выбрали проводку на странице **График**, выполните шаги по созданию журнала в разделе [Создание ежемесячных записей журнала в пакетном режиме](create-monthly-journals-batch.md).</span><span class="sxs-lookup"><span data-stu-id="0c6a7-125">If you selected the transaction on the **Schedule** page, follow the steps for creating a journal in [Create monthly journal entries in a batch](create-monthly-journals-batch.md).</span></span> <span data-ttu-id="0c6a7-126">Журнал необходимо разнести вручную.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-126">You must manually post the journal.</span></span>
    - <span data-ttu-id="0c6a7-127">Если проводка выбрана на странице **Проводки**, выберите **Сторнировать проводку**.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-127">If you selected the transaction on the **Transactions** page, select **Reverse transaction**.</span></span> <span data-ttu-id="0c6a7-128">Появится сообщение о том, что отзыв является отзывом предыдущего сторнирования, и можно изменить дату разноски для этого отзыва.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-128">You receive a message that states that this revocation is a revocation of an earlier reversal, and that you can edit the posting date for this revocation.</span></span> <span data-ttu-id="0c6a7-129">Однако общие бизнес-проверки влияют на даты, которые могут быть введены в поле **Дата**.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-129">However, general business validations affect the dates that can be entered in the **Date** field.</span></span> 

3. <span data-ttu-id="0c6a7-130">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-130">Select **OK**.</span></span> <span data-ttu-id="0c6a7-131">Запись журнала разносится, которая сторнирует выбранную запись.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-131">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="0c6a7-132">Сторнирование отображается на странице **Проводки**, а чистая общая сумма текущего сальдо восстанавливается до суммы на момент перед первым сторнированием.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-132">The reversal is shown on the **Transactions** page, and the net total current balance is restored to what it was before the first reversal.</span></span> <span data-ttu-id="0c6a7-133">Таким образом, воздействие сторнирования на сальдо будет отменено.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-133">Therefore, the impact that the reversal had on the balances is negated.</span></span>

<span data-ttu-id="0c6a7-134">При выборе пункта **Трассировка сторнирования** отображается диалоговое окно, в котором отображаются как оригинальные проводки, так и сторнированные проводки, вместе со связанным номером.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-134">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked trace number.</span></span>

<span data-ttu-id="0c6a7-135">Кроме того, можно отследить отзывы, используя соответствующую страницу **Графики**.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-135">You can also track revocations by using the appropriate **Schedules** page.</span></span> <span data-ttu-id="0c6a7-136">Поле **Сторнирование** очищено, в то время как выбрано поле **Журнал разнесен**.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-136">The **Reverse** field is cleared, whereas the **Journal posted** field is selected.</span></span> <span data-ttu-id="0c6a7-137">Кроме того, в поле **Последний номер журнала** значение обновляется на номер журнала проводки отзыва, а в поле **Номер журнала** значение обновляется на номер журнала сторнирования.</span><span class="sxs-lookup"><span data-stu-id="0c6a7-137">Additionally, the **Latest journal number** field is updated with the journal number of the revocation transaction, and the **Journal number** field is updated with the reversal journal number.</span></span>
