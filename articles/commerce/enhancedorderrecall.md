---
title: Операция отзыва заказа в POS-терминале
description: В этом разделе описываются возможности, доступные для усовершенствования страниц отзыва заказов в POS-терминале.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 41944fb7819b5527f6bc023a60acd9450d9e43c2
ms.sourcegitcommit: 25909c6ad3616e4f75a2fe006057dda18d7cc856
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974846"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="0d858-103">Операция отзыва заказа в POS-терминале</span><span class="sxs-lookup"><span data-stu-id="0d858-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0d858-104">Операция отзыва заказа в POS-терминала Commerce обеспечивает обновление функций поиска и фильтрации заказов и информации, относящейся к заказу.</span><span class="sxs-lookup"><span data-stu-id="0d858-104">The Recall order operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="0d858-105">Эта функция доступна в версиях Commerce 10.0.15 и выше.</span><span class="sxs-lookup"><span data-stu-id="0d858-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="0d858-106">Чтобы включить эту функцию, необходимо включить функцию **Усовершенствованная операция отзыва заказов в POS-терминале** в рабочей области **Управления функциями** в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="0d858-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="0d858-107">После включения функции обновите [макеты экрана](pos-screen-layouts.md) в POS-терминале, чтобы воспользоваться преимуществами некоторых измененных возможностей.</span><span class="sxs-lookup"><span data-stu-id="0d858-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="0d858-108">Настройка кнопки **Отозвать заказ** позволяет организациям разворачивать операцию с предварительно определенным экраном.</span><span class="sxs-lookup"><span data-stu-id="0d858-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Настройка сетки кнопок](media/recallorderbuttongrid.png)

<span data-ttu-id="0d858-110">Доступны следующие параметры отображения.</span><span class="sxs-lookup"><span data-stu-id="0d858-110">The display options are as follows.</span></span>
- <span data-ttu-id="0d858-111">**Нет** — при выборе этого параметра выполняется развертывание операции без специального представления.</span><span class="sxs-lookup"><span data-stu-id="0d858-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="0d858-112">Когда пользователь открывает операцию с данной конфигурацией, ему будет предложено искать и находить заказы или выбрать из заранее определенного фильтров заказов.</span><span class="sxs-lookup"><span data-stu-id="0d858-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="0d858-113">**Заказы для выполнения** — когда пользователь запускает операцию, запрос будет запущен автоматически для поиска и показа списка заказов, которые должны быть выполнены магазином.</span><span class="sxs-lookup"><span data-stu-id="0d858-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the store.</span></span> <span data-ttu-id="0d858-114">Эти заказы настроены для самовывоза из магазина или отгрузки из магазина, а строки этих заказов еще не скомплектованы или не упакованы.</span><span class="sxs-lookup"><span data-stu-id="0d858-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="0d858-115">**Заказы для самовывоза** — когда пользователь запускает операцию, запрос будет запущен автоматически для поиска и показа списка заказов, которые настроены для самовывоза из текущего магазина пользователя.</span><span class="sxs-lookup"><span data-stu-id="0d858-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="0d858-116">**Заказы для отгрузки** — когда пользователь запускает операцию, запрос будет запущен автоматически для поиска и показа списка заказов, которые настроены для отгрузки из текущего магазина пользователя.</span><span class="sxs-lookup"><span data-stu-id="0d858-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="0d858-117">Если при запуске операции **Отозвать заказ** из POS-терминала дисплей настроен на **Нет**, пользователь сможет искать и извлекать заказы одним из следующих способов.</span><span class="sxs-lookup"><span data-stu-id="0d858-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="0d858-118">Сканировать штрих-коды заказов.</span><span class="sxs-lookup"><span data-stu-id="0d858-118">Scan order barcodes.</span></span> <span data-ttu-id="0d858-119">При этом поиск совпадений будет выполняться в полях номера заказа, ссылки канала и кода прихода.</span><span class="sxs-lookup"><span data-stu-id="0d858-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="0d858-120">Выберите значок **Поиск заказов** или **Поиск и фильтр** на панели приложений, чтобы использовать механизм фильтрации для поиска заказов, удовлетворяющих критериям фильтрации.</span><span class="sxs-lookup"><span data-stu-id="0d858-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="0d858-121">Выберите предварительно определенный фильтр в раскрывающемся меню **Показать заказы** (заказы для выполнения, заказы для самовывоза или заказы для отгрузки).</span><span class="sxs-lookup"><span data-stu-id="0d858-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="0d858-123">После применения критериев поиска приложение отобразит список соответствующих заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="0d858-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="0d858-125">Пользователь может выбрать заказ в списке, чтобы просмотреть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0d858-125">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="0d858-126">На панели информации в правой части экрана отображаются сведения о выбранном заказе, включая детали строки заказа, сведения о поставке и сведения о выполнении.</span><span class="sxs-lookup"><span data-stu-id="0d858-126">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="0d858-127">Из панели приложений пользователь может выбрать операцию.</span><span class="sxs-lookup"><span data-stu-id="0d858-127">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="0d858-128">В зависимости от статуса заказа некоторые операции могут быть не активированы.</span><span class="sxs-lookup"><span data-stu-id="0d858-128">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="0d858-129">**Возврат** — выполняет возврат для одной или нескольких накладных, которые связаны с выбранным заказом клиента.</span><span class="sxs-lookup"><span data-stu-id="0d858-129">**Return** – Executes a return for one or more invoices related to the selected customer order.</span></span>

- <span data-ttu-id="0d858-130">**Отменить** — выдает полную отмену выбранного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="0d858-130">**Cancel** – Issue a full cancellation of the selected sales order.</span></span>

- <span data-ttu-id="0d858-131">**Выполнить** — переносит пользователя на страницу выполнение заказа, которая будет предварительно отфильтрована для выбранного заказа.</span><span class="sxs-lookup"><span data-stu-id="0d858-131">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="0d858-132">Будут отображены только те строки заказа, которые открыты для выполнения в магазине пользователя для выбранного заказа.</span><span class="sxs-lookup"><span data-stu-id="0d858-132">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="0d858-133">**Правка** — позволяет пользователям вносить изменения в выбранный заказ клиента.</span><span class="sxs-lookup"><span data-stu-id="0d858-133">**Edit** – Allows users to make changes to the selected customer order.</span></span>

- <span data-ttu-id="0d858-134">**Скомплектовать** — запускает поток комплектации, который позволяет пользователю выбирать продукты для комплектации и создавать проводку комплектации продажи.</span><span class="sxs-lookup"><span data-stu-id="0d858-134">**Pick up** – Launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>
