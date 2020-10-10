---
title: Входящие и исходящие активы
description: В этом разделе объясняется, как регистрировать входящие и исходящие активы в «Управлении активами».
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a7239bf5f8e53e61c4259abbcbf2ff740f4cef55
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889945"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="6ce5a-103">Входящие и исходящие активы</span><span class="sxs-lookup"><span data-stu-id="6ce5a-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6ce5a-104">Если ваша компания выполняет ремонтные работы или задания обслуживания по активам, полученные из других местоположений или клиентов, «Управление активами» может отслеживать как входящие активы, которые находятся на пути к вашей компании, так и исходящие активы, которые возвращаются.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="6ce5a-105">Если требуется использовать состояния входящего и исходящего жизненного цикла для управления активами, которые поступают и возвращаются, необходимо настроить состояния жизненного цикла и модели жизненного цикла запроса на обслуживание для поддержки этих действий.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="6ce5a-106">Дополнительные сведения о запросах новых поставщиков см. в разделе [Запросы на обслуживание](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="6ce5a-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="6ce5a-107">Настройка «Управления активами» определяет, можно ли работать с входящими и исходящими активами.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="6ce5a-108">Регистрация активов в качестве входящих</span><span class="sxs-lookup"><span data-stu-id="6ce5a-108">Register assets as inbound</span></span>

1. <span data-ttu-id="6ce5a-109">Выберите **Управление активами** \> **Общее** \> **Запросы на обслуживание** \> **Активные запросы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="6ce5a-110">Выберите запрос на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="6ce5a-111">Выберите **Обновить состояние запроса на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="6ce5a-112">Выберите **Входящие** (или другое состояние жизненного цикла, созданное для входящих активов), а затем выберите **OK.**</span><span class="sxs-lookup"><span data-stu-id="6ce5a-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Регистрация активов в качестве входящих](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="6ce5a-114">Регистрация входящих активов в качестве полученных</span><span class="sxs-lookup"><span data-stu-id="6ce5a-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="6ce5a-115">Выберите **Управление активами** \> **Общее** \> **Входящие/Исходящие** \> **Входящие активы**.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="6ce5a-116">Выберите актив или запрос на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="6ce5a-117">ВЫберите **Получить активы**.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="6ce5a-118">В поле **Получено** введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="6ce5a-119">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-119">Then select **OK**.</span></span> <span data-ttu-id="6ce5a-120">Запись удаляется со страницы списка **Входящие активы**.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-120">The record is removed from the **Inbound assets** list page.</span></span>

![Регистрация входящих активов в качестве полученных](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="6ce5a-122">Регистрация активов в качестве исходящих</span><span class="sxs-lookup"><span data-stu-id="6ce5a-122">Register assets as outbound</span></span>

<span data-ttu-id="6ce5a-123">После завершения задания обслуживания или ремонта актив можно зарегистрировать в качестве возвращенного.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="6ce5a-124">Выберите **Управление активами** \> **Общее** \> **Запросы на обслуживание** \> **Активные запросы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="6ce5a-125">Выберите запрос на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="6ce5a-126">Выберите **Обновить состояние запроса на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="6ce5a-127">Выберите **Исходящие** (или другое состояние жизненного цикла, созданное для исходящих активов), а затем выберите **OK.**</span><span class="sxs-lookup"><span data-stu-id="6ce5a-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="6ce5a-128">Регистрация исходящих активов в качестве отобранных</span><span class="sxs-lookup"><span data-stu-id="6ce5a-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="6ce5a-129">Выберите **Управление активами** \> **Общее** \> **Входящие/Исходящие** \> **Исходящие активы**.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="6ce5a-130">Выберите актив или запрос на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="6ce5a-131">Выберите **Доставить активы**.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="6ce5a-132">В поле **Отобрано** введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="6ce5a-133">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-133">Then select **OK**.</span></span> <span data-ttu-id="6ce5a-134">Запись удаляется со страницы списка **Исходящие активы**.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-134">The record is removed from the **Outbound assets** list page.</span></span>
