---
title: Создание книги Excel для редактирования проводок розничной торговли
description: В этой теме описывается, как создать книгу Excel, чтобы можно было редактировать проводки розничной торговли в Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 73a3387d1e7251168002ff683b5b58e0c82a620c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965385"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="5afcd-103">Создание книги Excel для редактирования проводок розничной торговли</span><span class="sxs-lookup"><span data-stu-id="5afcd-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5afcd-104">В этой теме описывается, как создать книгу Excel, чтобы можно было редактировать проводки розничной торговли в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5afcd-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5afcd-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="5afcd-105">Overview</span></span>

<span data-ttu-id="5afcd-106">Существует предопределенный шаблон Excel, который клиенты могут открыть из разных частей системы и использовать для редактирования и аудита проводок розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="5afcd-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="5afcd-107">Однако клиенты также могут создать пользовательскую книгу Excel для этой цели.</span><span class="sxs-lookup"><span data-stu-id="5afcd-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="5afcd-108">Создание и настройка книги Excel</span><span class="sxs-lookup"><span data-stu-id="5afcd-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="5afcd-109">Чтобы создать и настроить книгу Excel для редактирования проводок розничной торговли, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5afcd-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="5afcd-110">Откройте Excel и создайте пустую книгу.</span><span class="sxs-lookup"><span data-stu-id="5afcd-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="5afcd-111">На вкладке **Вставка** выберите **Мои надстройки**.</span><span class="sxs-lookup"><span data-stu-id="5afcd-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="5afcd-112">В правой области перейдите по ссылке **Добавить сведения о сервере**.</span><span class="sxs-lookup"><span data-stu-id="5afcd-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="5afcd-113">Введите URL-адрес сервера и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5afcd-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="5afcd-114">Если вы получили сообщение об ошибке "Регистрации приложений не найдены", выполните следующие действия, чтобы устранить эту проблему:</span><span class="sxs-lookup"><span data-stu-id="5afcd-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="5afcd-115">В Commerce перейдите в раздел **Администрирование системы \> Настройка \> Параметры приложения Office**.</span><span class="sxs-lookup"><span data-stu-id="5afcd-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="5afcd-116">На экспресс-вкладке **Параметры приложения** выберите **Инициализировать параметры приложения**.</span><span class="sxs-lookup"><span data-stu-id="5afcd-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="5afcd-117">В диалоговом окне подтверждения выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5afcd-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="5afcd-118">На экспресс-вкладке **Зарегистрированные приложения** выберите **Инициализировать регистрацию приложения**.</span><span class="sxs-lookup"><span data-stu-id="5afcd-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="5afcd-119">Повторите предыдущие три шага при необходимости.</span><span class="sxs-lookup"><span data-stu-id="5afcd-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="5afcd-120">Выберите **Разработка** и нажмите **Добавить таблицу**.</span><span class="sxs-lookup"><span data-stu-id="5afcd-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="5afcd-121">На основе данных, которые должны быть изменены, выберите объекты, которые должны быть добавлены в книгу Excel для редактирования.</span><span class="sxs-lookup"><span data-stu-id="5afcd-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="5afcd-122">Используйте следующую таблицу для справки.</span><span class="sxs-lookup"><span data-stu-id="5afcd-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="5afcd-123">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="5afcd-123">Transaction type</span></span> | <span data-ttu-id="5afcd-124">Информационные объекты для использования</span><span class="sxs-lookup"><span data-stu-id="5afcd-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="5afcd-125">Кассовые проводки, интернет-заказы, асинхронные заказы клиентов, асинхронные предложения клиентов</span><span class="sxs-lookup"><span data-stu-id="5afcd-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="5afcd-126">Проводка (доступно для аудита), проводка по продаже (доступно для аудита), проводки по оплате (доступно для аудита), налоговые проводки (доступно для аудита), проводки по скидкам (доступно для аудита), проводки по накладным расходам (доступно для аудита)</span><span class="sxs-lookup"><span data-stu-id="5afcd-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="5afcd-127">Инкассация</span><span class="sxs-lookup"><span data-stu-id="5afcd-127">Bank drop</span></span> | <span data-ttu-id="5afcd-128">Проводка (доступно для аудита), проводки по платежному средству для внесения в банк (доступно для аудита)</span><span class="sxs-lookup"><span data-stu-id="5afcd-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="5afcd-129">Сдача наличных средств в сейф</span><span class="sxs-lookup"><span data-stu-id="5afcd-129">Safe drop</span></span> | <span data-ttu-id="5afcd-130">Проводка (доступно для аудита), проводки по платежному средству для внесения в сейф (доступно для аудита)</span><span class="sxs-lookup"><span data-stu-id="5afcd-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="5afcd-131">Декларирование платежного средства</span><span class="sxs-lookup"><span data-stu-id="5afcd-131">Tender declaration</span></span> | <span data-ttu-id="5afcd-132">Проводка (доступно для аудита), проводки декларирования платежных средств (доступно для аудита)</span><span class="sxs-lookup"><span data-stu-id="5afcd-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="5afcd-133">Доход, расход</span><span class="sxs-lookup"><span data-stu-id="5afcd-133">Income, Expense</span></span> | <span data-ttu-id="5afcd-134">Проводка (доступно для аудита), проводки по доходам/расходам (доступно для аудита), проводки по оплате (доступно для аудита)</span><span class="sxs-lookup"><span data-stu-id="5afcd-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="5afcd-135">Объявление начальной суммы, изъятие денежных средств, внесение денежных средств, платежное средство для сдачи, платеж по накладной,депозит клиента</span><span class="sxs-lookup"><span data-stu-id="5afcd-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="5afcd-136">Проводка (доступно для аудита), проводки по оплате (доступно для аудита)</span><span class="sxs-lookup"><span data-stu-id="5afcd-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="5afcd-137">В каждую книгу Excel можно добавить только один информационный объект.</span><span class="sxs-lookup"><span data-stu-id="5afcd-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="5afcd-138">Кроме того, все поля, помеченные символом ключа, должны быть добавлены в соответствующую книгу.</span><span class="sxs-lookup"><span data-stu-id="5afcd-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="5afcd-139">После настройки книги примените необходимые фильтры.</span><span class="sxs-lookup"><span data-stu-id="5afcd-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="5afcd-140">Обязательно примените одинаковые фильтры ко всем листам в файле.</span><span class="sxs-lookup"><span data-stu-id="5afcd-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="5afcd-141">Старайтесь не загружать большие объемы данных в файл Excel.</span><span class="sxs-lookup"><span data-stu-id="5afcd-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="5afcd-142">В противном случае это может повлиять на производительность и замедлить работу Excel и системы.</span><span class="sxs-lookup"><span data-stu-id="5afcd-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="5afcd-143">Рекомендуется всегда использовать фильтры "Компания" и "Номер журнала операций" или "Номер проводки" в качестве фильтров для файла.</span><span class="sxs-lookup"><span data-stu-id="5afcd-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="5afcd-144">После настройки фильтров выберите **Обновить**, чтобы загрузить данные.</span><span class="sxs-lookup"><span data-stu-id="5afcd-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="5afcd-145">Измените необходимые данные и опубликуйте их.</span><span class="sxs-lookup"><span data-stu-id="5afcd-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="5afcd-146">Если кнопка **Опубликовать** недоступна, скорее всего, некоторые ключевые поля не были добавлены в книгу Excel.</span><span class="sxs-lookup"><span data-stu-id="5afcd-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5afcd-147">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5afcd-147">Additional resources</span></span>

[<span data-ttu-id="5afcd-148">Редактирование и аудит кассовых проводок и проводок управления кассами</span><span class="sxs-lookup"><span data-stu-id="5afcd-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="5afcd-149">Редактирование и аудит проводок интернет-заказов и асинхронных проводок заказов клиентов</span><span class="sxs-lookup"><span data-stu-id="5afcd-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="5afcd-150">Изменение финансовых аналитик для проводок розничной торговли</span><span class="sxs-lookup"><span data-stu-id="5afcd-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="5afcd-151">Добавление полей в книгу Excel для редактирования проводок розничной торговли</span><span class="sxs-lookup"><span data-stu-id="5afcd-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
