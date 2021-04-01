---
title: Создание заказов на работу из запросов на обслуживание
description: В этом разделе объясняется, как создавать заказы на работу из запросов на обслуживание в управлении активами.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5bf147104909302173c32b8376f16c66784110cb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253341"
---
# <a name="create-work-orders-from-maintenance-requests"></a><span data-ttu-id="567e4-103">Создание заказов на работу из запросов на обслуживание</span><span class="sxs-lookup"><span data-stu-id="567e4-103">Create work orders from maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="567e4-104">После создания запросов на техническое обслуживание можно легко преобразовать их в заказы на работу.</span><span class="sxs-lookup"><span data-stu-id="567e4-104">After you've created maintenance requests, you can easily convert them to work orders.</span></span> <span data-ttu-id="567e4-105">Эта тема описывает самый быстрый способ работы с запросами на техническое обслуживание, обновления нескольких запросов на техническое обслуживание одновременно, а затем создания заказа на работу для нескольких запросов на техническое обслуживание одновременно.</span><span class="sxs-lookup"><span data-stu-id="567e4-105">This topic describes the quickest way to work with maintenance requests, update several maintenance requests at the same time, and then create a work order for several maintenance requests at the same time.</span></span> <span data-ttu-id="567e4-106">На странице **Активные запросы на обслуживание** или **Запросы на обслуживания для моего функционального местоположения** можно также работать с одним запросом на техническое обслуживание за раз и конвертировать один запрос на техническое обслуживание в заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="567e4-106">On the **Active maintenance requests** or **My functional location maintenance requests** page, you can also work with one maintenance request at a time and convert one maintenance request to a work order.</span></span>

> [!NOTE]
> <span data-ttu-id="567e4-107">Каждый запрос на техническое обслуживание может быть связан только с одним заказом на работу.</span><span class="sxs-lookup"><span data-stu-id="567e4-107">Every maintenance request can be related to only one work order.</span></span> <span data-ttu-id="567e4-108">Однако несколько запросов на техническое обслуживание могут быть включены в один заказ на работу, даже если запросы на техническое обслуживание имеют разные активы.</span><span class="sxs-lookup"><span data-stu-id="567e4-108">However, multiple maintenance requests can be included in one work order, even if the maintenance requests have different assets.</span></span>

1. <span data-ttu-id="567e4-109">Выберите **Управление активами** \> **Общее** \> **Запросы на обслуживание** \> **Все запросы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="567e4-109">Select **Asset management** \> **Common** \> **maintenance requests** \> **All maintenance requests**.</span></span>
2. <span data-ttu-id="567e4-110">Прежде чем создать заказ на работу из запросов на техническое обслуживание, необходимо выбрать, как минимум, тип работы по техническому обслуживанию для запросов на обслуживание, а также вариант типа работы по техническому обслуживанию и торговлю, если эта информация актуальна.</span><span class="sxs-lookup"><span data-stu-id="567e4-110">Before you can create a work order from maintenance requests, you must select, at a minimum, a maintenance job type for the maintenance requests, and also a maintenance job type variant and trade, if this information is relevant.</span></span> <span data-ttu-id="567e4-111">В представлении сетки можно легко обновить информацию для запроса на техническое обслуживание.</span><span class="sxs-lookup"><span data-stu-id="567e4-111">In the grid view, you can easily update information for a maintenance request.</span></span>
3. <span data-ttu-id="567e4-112">Когда вы будете готовы к созданию заказа на работу, выберите запросы на техническое обслуживание, чтобы включить в него.</span><span class="sxs-lookup"><span data-stu-id="567e4-112">When you're ready to create a work order, select the maintenance requests to include in it.</span></span>

    - <span data-ttu-id="567e4-113">При выборе нескольких запросов на обслуживание для преобразования в заказ на работу необходимо установить поле **Актив** и поле **Тип задания на обслуживание** перед созданием заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="567e4-113">If you select several maintenance requests to convert to a work order, both the **Asset** field and the **Maintenance job type** field must be set before you create the work order.</span></span>
    - <span data-ttu-id="567e4-114">При выборе одного запроса на техническое обслуживание для преобразования в заказ на работу необходимо установить только поле **Актив**, прежде чем создавать заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="567e4-114">If you select one maintenance request to convert to a work order, only the **Asset** field must be set before you create the work order.</span></span> <span data-ttu-id="567e4-115">Однако при создании заказа на работу можно выбрать тип задания на обслуживание (и связанный с этим вариант типа задания на обслуживание и торговлю, если эта информация актуальна) в диалоговом окне **Создание заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="567e4-115">However, when you create the work order, you can select a maintenance job type (and a related maintenance job type variant and trade, if this information is relevant) in the **Create work order** dialog box.</span></span>

4. <span data-ttu-id="567e4-116">Выберите **Заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="567e4-116">Select **Work order**.</span></span>
5. <span data-ttu-id="567e4-117">В диалоговом окне **Создание заказа на работу** установите поля, затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="567e4-117">In the **Create work order** dialog box, set the fields, and then select **OK**.</span></span>

    <span data-ttu-id="567e4-118">Панель сообщений может уведомить вас о создании нового заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="567e4-118">A message bar might notify you that a new work order has been created.</span></span>

    <span data-ttu-id="567e4-119">Кроме того, при создании заказа на работу, основанного на запросе на техническое обслуживание, если актив, связанный с запросом на техническое обслуживание, включен в гарантийное соглашение, панель сообщений уведомляет вас о гарантийном соглашении.</span><span class="sxs-lookup"><span data-stu-id="567e4-119">Additionally, when you create a work order that is based on a maintenance request, if the asset that is related to the maintenance request is included in a warranty agreement, a message bar notifies you about the warranty agreement.</span></span>

6. <span data-ttu-id="567e4-120">Выберите **Управление активами** \> **Общее** \> **Заказы на работу** \> **Все заказы на работу** и откройте новый заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="567e4-120">Select **Asset management** \> **Common** \> **Work orders** \> **All work orders**, and open the new work order.</span></span>

    ![Открыть новый заказ на работу](media/05-manage-maintenance-requests.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]