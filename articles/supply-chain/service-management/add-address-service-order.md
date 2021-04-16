---
title: Добавление адреса в заказ на сервисное обслуживание
description: В этом разделе описывается, как добавить адрес клиента в заказ на сервисное обслуживание.
author: ShylaThompson
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a54ec439fc88dc9688bbb3d6b833b5d80482f024
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824662"
---
# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="369a9-103">Добавление адреса в заказ на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="369a9-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="369a9-104">В этом разделе описывается, как добавить адрес клиента в заказ на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="369a9-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="369a9-105">При создании заказа на обслуживание адресная информация переносится из проекта, к которому присоединен заказ на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="369a9-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="369a9-106">Однако можно выбрать альтернативное местоположение из адресов, которые уже введены в Microsoft Dynamics AX для клиентов, поставщиков, сайтов, складов, заказов на сервисное обслуживание и проектов.</span><span class="sxs-lookup"><span data-stu-id="369a9-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="369a9-107">Также можно создать новый адрес.</span><span class="sxs-lookup"><span data-stu-id="369a9-107">You can also create a new address.</span></span> <span data-ttu-id="369a9-108">По умолчанию новый адрес добавляется в проект.</span><span class="sxs-lookup"><span data-stu-id="369a9-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="369a9-109">Однако можно указать, чтобы новый адрес применялся только к данному экземпляру службы.</span><span class="sxs-lookup"><span data-stu-id="369a9-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="369a9-110">В этом случае новый адрес не будет добавлен в проект.</span><span class="sxs-lookup"><span data-stu-id="369a9-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="369a9-111">Создание адреса клиента для заказа на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="369a9-111">Create a customer address for a service order</span></span>

<span data-ttu-id="369a9-112">Чтобы добавить адрес в заказ на сервисное обслуживание, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="369a9-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="369a9-113">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="369a9-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="369a9-114">Откройте заказ на сервисное обслуживание, для которого необходимо создать адрес.</span><span class="sxs-lookup"><span data-stu-id="369a9-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="369a9-115">В разделе **Панель операций** щелкните **Изменить** и выберите **Представление заголовка**.</span><span class="sxs-lookup"><span data-stu-id="369a9-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="369a9-116">На экспресс-вкладке **Адрес** нажмите кнопку **Добавить адрес**.</span><span class="sxs-lookup"><span data-stu-id="369a9-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="369a9-117">В форме **Создать адрес** введите уникальное имя адреса и заполните оставшиеся поля.</span><span class="sxs-lookup"><span data-stu-id="369a9-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="369a9-118">Если ввести имя уже существующего адреса, вводимая в остальные поля информация переопределит сведения, указанные для существующего адреса.</span><span class="sxs-lookup"><span data-stu-id="369a9-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="369a9-119">Нажмите кнопку **ОК**, чтобы скопировать новый адрес в заказ на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="369a9-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="369a9-120">Указание альтернативного адреса в заказе на обслуживание</span><span class="sxs-lookup"><span data-stu-id="369a9-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="369a9-121">Чтобы добавить альтернативный адрес в заказ на сервисное обслуживание, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="369a9-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="369a9-122">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="369a9-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="369a9-123">Откройте заказ на сервисное обслуживание, для которого необходимо ввести альтернативный адрес.</span><span class="sxs-lookup"><span data-stu-id="369a9-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="369a9-124">В разделе **Панель операций** щелкните **Изменить** и выберите **Представление заголовка**.</span><span class="sxs-lookup"><span data-stu-id="369a9-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="369a9-125">На экспресс-вкладке **Адрес** нажмите кнопку **Другой адрес**.</span><span class="sxs-lookup"><span data-stu-id="369a9-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="369a9-126">В форме **Выбор адреса**, в поле **Тип записи** выберите **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="369a9-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="369a9-127">Выберите адрес и нажмите кнопку **ОК**, чтобы скопировать его в заказ на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="369a9-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]