---
title: Создание и обновление часов работы
description: В этом разделе описывается создание и обновление часов работы магазина в Commerce Headquarters.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 4706432234437d2dc7943fb194cd01004ab7e6b7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687519"
---
# <a name="create-and-update-store-hours"></a><span data-ttu-id="19981-103">Создание и обновление часов работы</span><span class="sxs-lookup"><span data-stu-id="19981-103">Create and update store hours</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="19981-104">Обзор</span><span class="sxs-lookup"><span data-stu-id="19981-104">Overview</span></span>

<span data-ttu-id="19981-105">В одном месте розничные торговцы могут создавать, обслуживать и управлять временем работы магазинов для разных магазинов в географических регионах.</span><span class="sxs-lookup"><span data-stu-id="19981-105">From a single place, retailers can create, maintain, and manage the store hours for different stores across geographic regions.</span></span> <span data-ttu-id="19981-106">Часы работы магазина могут затем отображаться в POS-терминалах.</span><span class="sxs-lookup"><span data-stu-id="19981-106">The store hours can then be shown on point of sale (POS) terminals.</span></span> <span data-ttu-id="19981-107">Таким образом кассиры могут сообщать часы работы магазинов клиентами и лучше помогать покупателям, заинтересованным в запасах в других магазинах.</span><span class="sxs-lookup"><span data-stu-id="19981-107">In this way, cashiers can share store hours with customers and better help shoppers who are interested in inventory in other stores.</span></span> <span data-ttu-id="19981-108">Часы работы магазина могут также печататься на чеках, в том случае, когда клиенты хотят позже вернуться в магазин.</span><span class="sxs-lookup"><span data-stu-id="19981-108">The store hours can also be printed on receipts, in case customers want to return to the store later.</span></span>

<span data-ttu-id="19981-109">Можно настроить несколько часов работы магазина для различных каналов.</span><span class="sxs-lookup"><span data-stu-id="19981-109">Multiple store hours can be configured across different channels.</span></span> <span data-ttu-id="19981-110">Эти каналы включают в себя физические магазины, центры обработки звонков, мобильные устройства и сайты электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="19981-110">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

<span data-ttu-id="19981-111">Если клиент имеет заказ с получением в другом магазине, кассир может выбрать даты, когда товары можно забрать в том магазине.</span><span class="sxs-lookup"><span data-stu-id="19981-111">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="19981-112">Поиск магазинов обеспечит ссылку на даты и время работы магазина.</span><span class="sxs-lookup"><span data-stu-id="19981-112">The store lookup will provide a reference to the dates and store times.</span></span> <span data-ttu-id="19981-113">Кассир может выбрать дату и местоположение, а также напечатать чек для получения товара, содержащий часы работы магазина.</span><span class="sxs-lookup"><span data-stu-id="19981-113">The cashier can select a date and location, and can also print a pickup receipt that includes the store hours.</span></span>

<span data-ttu-id="19981-114">Эта функция доступна в Microsoft Dynamics 365 Retail версии 8.1.2 и выше.</span><span class="sxs-lookup"><span data-stu-id="19981-114">This functionality is available in Microsoft Dynamics 365 Retail versions 8.1.2 and later.</span></span>

## <a name="configure-store-hours"></a><span data-ttu-id="19981-115">Настройка часов работы магазина</span><span class="sxs-lookup"><span data-stu-id="19981-115">Configure store hours</span></span>

<span data-ttu-id="19981-116">Чтобы настроить часы работы магазина, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="19981-116">Follow these steps to configure store hours.</span></span>

1. <span data-ttu-id="19981-117">Выберите **Retail и Commerce** \> **Настройка канала** \> **Часы работы магазина**.</span><span class="sxs-lookup"><span data-stu-id="19981-117">Go to **Retail and Commerce** \> **Channel Setup** \> **Store hours**.</span></span>
2. <span data-ttu-id="19981-118">Выберите **Создать** для создания нового шаблона часов работы магазина.</span><span class="sxs-lookup"><span data-stu-id="19981-118">Select **New** to create a new store hours template.</span></span> <span data-ttu-id="19981-119">Для использования существующего шаблона выберите шаблон в левой области.</span><span class="sxs-lookup"><span data-stu-id="19981-119">To use an existing template, select the template in the left pane.</span></span>
3. <span data-ttu-id="19981-120">В диалоговом окне **Добавить диапазон** определите диапазон дат, часы работы магазина и все необходимые выходные.</span><span class="sxs-lookup"><span data-stu-id="19981-120">In the **Add range** dialog box, define the date range, the store hours, and any holidays that are required.</span></span>

    - <span data-ttu-id="19981-121">Если часы работы магазина не изменяются, выберите значение **Никогда не заканчивается** в поле **Дата окончания**.</span><span class="sxs-lookup"><span data-stu-id="19981-121">If store hours don't change, select **Never ends** in the **End date** field.</span></span>
    - <span data-ttu-id="19981-122">Если часы работы магазина действительны на определенный месяц, неделю или день, установите соответствующие даты в полях **Начальная дата** и **Конечная дата**.</span><span class="sxs-lookup"><span data-stu-id="19981-122">If the store hours are for a specific month, week, or day, set the appropriate dates in the **Start Date** and **End date** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="19981-123">Можно создать несколько шаблонов, которые имеют перекрывающиеся даты начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="19981-123">You can create multiple templates that have overlapping start and end dates.</span></span> <span data-ttu-id="19981-124">Таким образом, имеется возможность, например, определить часы работы магазина для магазинов в других часовых поясах.</span><span class="sxs-lookup"><span data-stu-id="19981-124">Therefore, you can, for example, define store hours for stores in different time zones.</span></span>

    <span data-ttu-id="19981-125">![Диалоговое окно добавления диапазона](../dev-itpro/media/Storehours1.png "Диалоговое окно добавления диапазона")</span><span class="sxs-lookup"><span data-stu-id="19981-125">![Add range dialog box](../dev-itpro/media/Storehours1.png "Add range dialog box")</span></span>

4. <span data-ttu-id="19981-126">Свяжите шаблон часов работы магазина с магазинами, в которых он будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="19981-126">Associate the store hours template with the stores where it will be used.</span></span> <span data-ttu-id="19981-127">В диалоговом окне **Выбор узлов организации** выберите магазины, регионы и организации, с которыми должен быть связан шаблон.</span><span class="sxs-lookup"><span data-stu-id="19981-127">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>

    - <span data-ttu-id="19981-128">С каждым магазином можно связать только один шаблон часов работы магазина.</span><span class="sxs-lookup"><span data-stu-id="19981-128">Only one store hours template can be associated with each store.</span></span>
    - <span data-ttu-id="19981-129">С помощью кнопок со стрелками выберите магазины, регионы или организации.</span><span class="sxs-lookup"><span data-stu-id="19981-129">Use the arrow buttons to select stores, regions, or organizations.</span></span> <span data-ttu-id="19981-130">Календарь будет доступен для магазинов или групп магазинов, и он будет отображаться на POS-терминалах для справки.</span><span class="sxs-lookup"><span data-stu-id="19981-130">The calendar will be available to the stores or store groups, and it will be visible at the POS for reference.</span></span>

    <span data-ttu-id="19981-131">![Диалоговое окно выборы узлов организации](../dev-itpro/media/Storehours2.png "Диалоговое окно выборы узлов организации")</span><span class="sxs-lookup"><span data-stu-id="19981-131">![Choose organization nodes dialog box](../dev-itpro/media/Storehours2.png "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="19981-132">На странице **График распределения** выполните задания **1070** и **1090**, чтобы сделать часы работы магазина доступными для POS-терминала.</span><span class="sxs-lookup"><span data-stu-id="19981-132">On the **Distribution schedule** page, run the **1070** and **1090** jobs to make the store hours available to the POS.</span></span>

## <a name="add-store-hours-to-printed-receipts"></a><span data-ttu-id="19981-133">Добавление часов работы магазина на печатаемые чеки</span><span class="sxs-lookup"><span data-stu-id="19981-133">Add store hours to printed receipts</span></span>

<span data-ttu-id="19981-134">Выполните следующие действия, чтобы добавить часы работы магазина на печатаемые POS-терминалом чеки.</span><span class="sxs-lookup"><span data-stu-id="19981-134">Follow these steps to add store hours to the printed POS receipts.</span></span>

1. <span data-ttu-id="19981-135">Откройте конструктор чеков.</span><span class="sxs-lookup"><span data-stu-id="19981-135">Open the receipt designer.</span></span>
2. <span data-ttu-id="19981-136">В нижнем левом углу выберите **Нижний колонтитул**.</span><span class="sxs-lookup"><span data-stu-id="19981-136">Select **Footer** in the lower-left corner.</span></span>
3. <span data-ttu-id="19981-137">Перетащите элемент **Часы работы магазина** из левой области в нижний колонтитул в нижней части шаблона чека.</span><span class="sxs-lookup"><span data-stu-id="19981-137">Drag the **Store hours** element from the left pane to the footer at the bottom of the receipt template.</span></span>
4. <span data-ttu-id="19981-138">Можно изменить метку по умолчанию в элементе **Часы работы магазина** по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="19981-138">You can edit the default label on the **Store hours** element as you require.</span></span>
5. <span data-ttu-id="19981-139">Сохраните чек и закройте конструктор чеков.</span><span class="sxs-lookup"><span data-stu-id="19981-139">Save the receipt, and close the receipt designer.</span></span>
6. <span data-ttu-id="19981-140">На странице **График распределения** выполните задания **1070** и **1090**.</span><span class="sxs-lookup"><span data-stu-id="19981-140">On the **Distribution schedule** page, run the **1070** and **1090** jobs.</span></span>
7. <span data-ttu-id="19981-141">Войдите в POS.</span><span class="sxs-lookup"><span data-stu-id="19981-141">Sign in to the POS.</span></span>
8. <span data-ttu-id="19981-142">Выполните продажу и выберите печать чека.</span><span class="sxs-lookup"><span data-stu-id="19981-142">Complete a sale, and select to print a receipt.</span></span>

<span data-ttu-id="19981-143">Теперь чеки с POS-терминала включают в себя часы работы магазина.</span><span class="sxs-lookup"><span data-stu-id="19981-143">POS receipts now include the store hours.</span></span> <span data-ttu-id="19981-144">Если в шаблон были включены праздники, они будут показаны в чеке.</span><span class="sxs-lookup"><span data-stu-id="19981-144">If any holidays were included in the template, they are shown on the receipt.</span></span>

<span data-ttu-id="19981-145">![Пример чека](../dev-itpro/media/Storehours3.png "Пример чека")</span><span class="sxs-lookup"><span data-stu-id="19981-145">![Receipt example](../dev-itpro/media/Storehours3.png "Receipt example")</span></span>
