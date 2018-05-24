---
title: "Отменить заказы на сервисное обслуживание"
description: "Можно отменить заказ на сервисное обслуживание или строку заказа на сервисное обслуживание непосредственно из самого заказа на сервисное обслуживание, а также можно отменить несколько заказов на сервисное обслуживание, запустив периодическое задание."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8e5ad119c28bba18b75bb5ed7854e94a4e734d55
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="cancel-service-orders"></a><span data-ttu-id="f30a5-103">Отменить заказы на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="f30a5-103">Cancel service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f30a5-104">Можно отменить заказ на сервисное обслуживание или строку заказа на сервисное обслуживание непосредственно из самого заказа на сервисное обслуживание, а также можно отменить несколько заказов на сервисное обслуживание, запустив периодическое задание.</span><span class="sxs-lookup"><span data-stu-id="f30a5-104">You can cancel a service order or service order line from the service order itself, or you can cancel multiple service orders by running a periodic job.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f30a5-105">Заказы на сервисное обслуживание невозможно отменить, если стадия заказа на сервисное обслуживание уже не допускает отмены, если для заказа создана потребность в номенклатуре или если заказ уже разнесен.</span><span class="sxs-lookup"><span data-stu-id="f30a5-105">Service orders cannot be canceled if the stage of the service order does not allow cancelation, if the service order has item requirements, or if the service order has already been posted.</span></span></P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a><span data-ttu-id="f30a5-106">Отмена заказа на обслуживание в форме "Заказ на обслуживание"</span><span class="sxs-lookup"><span data-stu-id="f30a5-106">Cancel a service order in the Service orders form</span></span>

1.  <span data-ttu-id="f30a5-107">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="f30a5-107">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="f30a5-108">Выберите заказ на обслуживание и в области действий щелкните **Отмена заказа**.</span><span class="sxs-lookup"><span data-stu-id="f30a5-108">Select the service order, and on the Action Pane, click **Cancel order**.</span></span>

## <a name="cancel-a-service-order-line"></a><span data-ttu-id="f30a5-109">Отмена строки заказа на обслуживание</span><span class="sxs-lookup"><span data-stu-id="f30a5-109">Cancel a service order line</span></span>

1.  <span data-ttu-id="f30a5-110">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="f30a5-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="f30a5-111">Дважды щелкните заказ на сервисное обслуживание, содержащий строку, которую требуется отменить.</span><span class="sxs-lookup"><span data-stu-id="f30a5-111">Double-click the service order that contains the line you want to cancel.</span></span>

2.  <span data-ttu-id="f30a5-112">Выберите строку заказа на сервисное обслуживание и щелкните **Отменить строку заказа**, чтобы изменить статус строки на **Отмененно**.</span><span class="sxs-lookup"><span data-stu-id="f30a5-112">Select the service order line that you want to cancel, and then click **Cancel order line** to change the status of the line to **Canceled**.</span></span>


> [!TIP]
> <P><span data-ttu-id="f30a5-113">Чтобы реверсировать отмену строки заказа на сервисное обслуживание и изменить статус обратно на <STRONG>Создано</STRONG>, щелкните <STRONG>Аннулировать отмену</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f30a5-113">To reverse the cancellation of a service order line and change the status back to <STRONG>Created</STRONG>, click <STRONG>Revoke cancel</STRONG>.</span></span></P>


## <a name="cancel-multiple-service-orders"></a><span data-ttu-id="f30a5-114">Отмена нескольких заказов на обслуживание</span><span class="sxs-lookup"><span data-stu-id="f30a5-114">Cancel multiple service orders</span></span>

1.  <span data-ttu-id="f30a5-115">Щелкните **Управление сервисным обслуживанием** \> **Периодические операции** \> **Заказы на сервисное обслуживание** \> **Отмена заказов на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="f30a5-115">Click **Service management** \> **Periodic** \> **Service orders** \> **Cancel service orders**.</span></span>

2.  <span data-ttu-id="f30a5-116">Нажмите кнопку **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="f30a5-116">Click the **Select** button.</span></span>

3.  <span data-ttu-id="f30a5-117">В форме **Запрос** в столбце **Критерии** выберите заказы на сервисное обслуживание, которые требуется отменить.</span><span class="sxs-lookup"><span data-stu-id="f30a5-117">In the **Inquiry** form, in the **Criteria** column, select the service orders that you want to cancel.</span></span>

4.  <span data-ttu-id="f30a5-118">Щелкните **OK**, чтобы закрыть форму **Запрос**.</span><span class="sxs-lookup"><span data-stu-id="f30a5-118">Click **OK** to close the **Inquiry** form.</span></span>

5.  <span data-ttu-id="f30a5-119">Чтобы создать Infolog со списком отмененных заказов на сервисное обслуживание, установите флажок **Отобразить Infolog**.</span><span class="sxs-lookup"><span data-stu-id="f30a5-119">Select the **Show Infolog** check box to generate an Infolog that lists the canceled service orders.</span></span>

6.  <span data-ttu-id="f30a5-120">Установите флажок **Аннулировать отмену**, если необходимо реверсировать статус **Отмененно** заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f30a5-120">Select the **Revoke cancel** check box if you want to reverse the **Canceled** status of a service order.</span></span>

7.  <span data-ttu-id="f30a5-121">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f30a5-121">Click **OK**.</span></span>

<span data-ttu-id="f30a5-122">Выбранные заказы на сервисное обслуживание либо отменяются, либо статус их выполнения меняется с **Отмененно** снова на **В работе**.</span><span class="sxs-lookup"><span data-stu-id="f30a5-122">The selected service orders are either canceled or their progress status of **Canceled** has been reversed to **In process**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f30a5-123">Если установить флажок <STRONG>Аннулировать отмену</STRONG>, заказы на сервисное обслуживание со статусом выполнения <STRONG>Отменено</STRONG> реверсируются, а заказы со статусом выполнения <STRONG>В работе</STRONG> не отменяются.</span><span class="sxs-lookup"><span data-stu-id="f30a5-123">If you select the <STRONG>Revoke cancel</STRONG> check box, service orders with a progress status of <STRONG>Canceled</STRONG> are reversed and service orders with a progress status of <STRONG>In process</STRONG> are not canceled.</span></span></P>


  



