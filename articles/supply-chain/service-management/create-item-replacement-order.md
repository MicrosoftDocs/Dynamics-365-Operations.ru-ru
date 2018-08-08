---
title: "Создание заказа на замену номенклатуры"
description: "Заказы на замену номенклатуры обычно используются после того, как продукт возвращен и осмотрен."
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 784a2522c27e8131f211ffc52319552b3b928cc3
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---

# <a name="create-an-item-replacement-order"></a><span data-ttu-id="c95da-103">Создание заказа на замену номенклатуры</span><span class="sxs-lookup"><span data-stu-id="c95da-103">Create an item replacement order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c95da-104">Заказы на замену номенклатуры обычно используются после того, как продукт возвращен и осмотрен.</span><span class="sxs-lookup"><span data-stu-id="c95da-104">Item replacement orders are usually created after a product is returned and inspected.</span></span> <span data-ttu-id="c95da-105">Однако, когда номенклатура должна быть заменена до того,как она будет возвращена, или когда исходная номенклатура не будет возвращена, можно создать заказ на замену номенклатуры сразу же после создания заказа на возврат.</span><span class="sxs-lookup"><span data-stu-id="c95da-105">However, when an item must be replaced before it has been returned, or when the original item will not be returned, you can create an item replacement order immediately after you create a return order.</span></span>

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a><span data-ttu-id="c95da-106">Создайте заказ на замену после получения возвращенной номенклатуры</span><span class="sxs-lookup"><span data-stu-id="c95da-106">Create a replacement order after you receive an item that is returned</span></span>

1.  <span data-ttu-id="c95da-107">Выберите **Продажи и маркетинг** \> **Общее** \> **Заказы на возврат** \> **Все заказы на возврат**.</span><span class="sxs-lookup"><span data-stu-id="c95da-107">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="c95da-108">Создайте новый заказ на возврат или выберите возвращенный заказ в списке, чтобы открыть форму **Заказ на возврат - номер RMA: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="c95da-108">Create a new return order, or select a returned order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="c95da-109">Щелкните **Строка возврата**, а затем выберите **Позиция на замену**.</span><span class="sxs-lookup"><span data-stu-id="c95da-109">Click **Return line**, and then select **Replacement item**.</span></span>

4.  <span data-ttu-id="c95da-110">Выберите номенклатуру для замены возвращенной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="c95da-110">Select the item to replace the returned item with.</span></span> <span data-ttu-id="c95da-111">Введите спецификации номенклатуры и нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="c95da-111">Enter the item specifications, and then click **Apply**.</span></span>

5.  <span data-ttu-id="c95da-112">Щелкните **Отборочная накладная**, чтобы создать отборочную накладную для заказа на возврат.</span><span class="sxs-lookup"><span data-stu-id="c95da-112">Click **Packing slip** to generate the packing slip for the return order.</span></span> <span data-ttu-id="c95da-113">Заказ на продажу создается для выбранном номенклатуры замены.</span><span class="sxs-lookup"><span data-stu-id="c95da-113">A sales order is generated for the replacement item that you selected.</span></span>
    
    <span data-ttu-id="c95da-114">После того как заказ на продажу создан для номенклатуры замены, договоры продажи автоматически просматриваются и при наличии применимого договора продажи он применяется к данному заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="c95da-114">After the sales order is created for the replacement item, sales agreements are automatically searched and if there is an applicable sales agreement, it is applied to the sales order.</span></span>

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a><span data-ttu-id="c95da-115">Создайте заказ на замену до получения номенклатуры, которая будет возвращена</span><span class="sxs-lookup"><span data-stu-id="c95da-115">Create a replacement order before you receive an item that will be returned</span></span>

1.  <span data-ttu-id="c95da-116">Выберите **Продажи и маркетинг** \> **Общее** \> **Заказы на возврат** \> **Все заказы на возврат**.</span><span class="sxs-lookup"><span data-stu-id="c95da-116">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="c95da-117">Создайте новый заказ на возврат или выберите заказ на возврат в списке, чтобы открыть форму **Заказ на возврат - номер RMA: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="c95da-117">Create a new return order, or select a return order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="c95da-118">Щелкните **Найти заказ на продажу**, если вы хотите определить заказ на продажу для возврата.</span><span class="sxs-lookup"><span data-stu-id="c95da-118">Click **Find sales order** if you want to identify the sales order for the returned item.</span></span> <span data-ttu-id="c95da-119">Заполните форму **Найти заказ на продажу** и нажмите кнопку **OK**, чтобы закрыть форму и вернуться в форму **Заказ на возврат - номер RMA: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="c95da-119">Complete the **Find sales order** form and then click **OK** to close the form and return to the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="c95da-120">Строка заказа на продажу для возвращенной номенклатуры копируется в заказ на возврат.</span><span class="sxs-lookup"><span data-stu-id="c95da-120">The sales order line for the returned item is copied to the return order.</span></span>

4.  <span data-ttu-id="c95da-121">Щелкните **Заказ на замену**, чтобы открыть форму **Создать заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="c95da-121">Click **Replacement order** to open the **Create sales order** form.</span></span>

5.  <span data-ttu-id="c95da-122">Установите флажок **Копировать строки заказа на возврат**,чтобы перенести сведения из заказа на возврат, выбранный в форме **Заказ на возврат - номер RMA: %1, %2**, в этот заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="c95da-122">Select the **Copy return order lines** check box to transfer details from the return order you selected on the **Return order - RMA number: %1, %2** form to this sales order.</span></span>

6.  <span data-ttu-id="c95da-123">Введите или измените сведения, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="c95da-123">Enter or modify details, as required.</span></span>
    
    <span data-ttu-id="c95da-124">Если используется заказ на продажу на шаге 3 и если строка заказа на продажу для возвращенной номенклатуры привязана к договору продажи, идентификатор применимого договора продажи для заказа на замену номенклатуры автоматически будет отображаться в поле **Код договора продажи**.</span><span class="sxs-lookup"><span data-stu-id="c95da-124">If you identified the sales order in step 3, and if the sales order line for the returned item is linked to a sales agreement, the identifier of the applicable sales agreement for the item replacement order will be automatically displayed in the **Sales agreement ID** field.</span></span>

7.  <span data-ttu-id="c95da-125">Щелкните **OK**, чтобы закрыть форму **Создать заказ на продажу** и открыть форму **Заказ на продажу**, где можно продолжать ввод данных для нового заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="c95da-125">Click **OK** to close the **Create sales order** form and open the **Sales order** form, where you can continue to enter information for the new sales order.</span></span> <span data-ttu-id="c95da-126">Все соответствующие строки заказа на возврат копируются в новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="c95da-126">Any applicable return order lines will be copied to the new sales order.</span></span> 
    
    <span data-ttu-id="c95da-127">Если идентификатор договора продажи автоматически отображается в поле **Код договора продажи**, договор продажи подключается к заголовку заказа на продажу для заказа на замену номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="c95da-127">If the identifier of the sales agreement is automatically displayed in the **Sales agreement ID** field, then the sales agreement has been linked to the sales order header for the item replacement order.</span></span> <span data-ttu-id="c95da-128">Если применяемое обязательство в договоре продажи еще не выполнено и заказ на продажу создается до истечения срока действия заказа на продажу, между строкой договора продажи и строкой заказа на продажу создается связь.</span><span class="sxs-lookup"><span data-stu-id="c95da-128">If there is an applicable commitment in the sales agreement that has not been fulfilled yet, and the sales order is created before the sales agreement expires, a link is established between the sales agreement line and the sales order line.</span></span> <span data-ttu-id="c95da-129">Следовательно, сведения из договора продажи, такие как цена номенклатуры, копируются в новую строку заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="c95da-129">Therefore, information from the sales agreement, such as item price, is copied to the new sales order line.</span></span> 
  



