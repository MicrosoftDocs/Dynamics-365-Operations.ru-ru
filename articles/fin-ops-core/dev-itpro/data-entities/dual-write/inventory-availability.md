---
title: Доступность запасов в двойной записи
description: В этой теме приводятся сведения о проверке доступности запасов в случае двойной записи.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426990"
---
# <a name="inventory-availability"></a><span data-ttu-id="41272-103">Доступность запасов</span><span class="sxs-lookup"><span data-stu-id="41272-103">Inventory availability</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="41272-104">Используя доступность запасов, можно проверять запасы перед добавлением продукта в формы **Предложения**, **Заказы** или **Накладные** в приложениях на основе модели в Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="41272-104">Using inventory availability, you can check your inventory before you add a product into the **Quotes**, **Orders**, or **Invoices** forms in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="41272-105">Например, проверка запасов и определение даты выполнения являются ключевыми задачами в процессе [продажи перспективному клиенту](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="41272-105">For example, checking inventory and determining a fulfullment date is a key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span> <span data-ttu-id="41272-106">Если запасов не хватает, можно оценить дату поставки на основе прогнозируемых приходов и расходов на складе.</span><span class="sxs-lookup"><span data-stu-id="41272-106">If you don't have enough inventory, you can estimate a delivery date based on projected inventory receipts and issues.</span></span> <span data-ttu-id="41272-107">Можно также проверить информацию о доступных для заказа продуктов (ATP), в которой можно найти количество ATP по заранее определенной временной границе.</span><span class="sxs-lookup"><span data-stu-id="41272-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the pre-defined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="41272-108">Запасы в наличии</span><span class="sxs-lookup"><span data-stu-id="41272-108">On-hand Inventory</span></span> 

<span data-ttu-id="41272-109">В заголовке форм **Предложения**, **Заказы** или **Накладные** в Dynamics 365 Sales добавлена новая кнопка **Запасы в наличии**.</span><span class="sxs-lookup"><span data-stu-id="41272-109">In the header of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **On-hand Inventory** is added.</span></span> <span data-ttu-id="41272-110">При нажатии на кнопку появляется диалоговое окно, в котором можно указать компанию и продукт, для которого необходимо проверить запасы в наличии.</span><span class="sxs-lookup"><span data-stu-id="41272-110">When you click the button, a dialog box appears and you can specify the company and the product for which you want to check the on-hand inventory.</span></span> <span data-ttu-id="41272-111">Она возвращает данные о запасах из Dynamics 365 Supply Chain Management и отображает те же сведения, что и [Запасы в наличии](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="41272-111">It returns the inventory information from Dynamics 365 Supply Chain Management, and shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span> <span data-ttu-id="41272-112">Эти сведения включают в себя следующие количества:</span><span class="sxs-lookup"><span data-stu-id="41272-112">The information includes these quantities:</span></span>

- <span data-ttu-id="41272-113">**Количество в наличии**</span><span class="sxs-lookup"><span data-stu-id="41272-113">**On-hand Quantity**</span></span>
- <span data-ttu-id="41272-114">**Зарезервированное количество в наличии**</span><span class="sxs-lookup"><span data-stu-id="41272-114">**Reserved On-hand Quantity**</span></span>
- <span data-ttu-id="41272-115">**Доступное количество в наличии**</span><span class="sxs-lookup"><span data-stu-id="41272-115">**Available On-hand Quantity**</span></span>
- <span data-ttu-id="41272-116">**Заказанное количество**</span><span class="sxs-lookup"><span data-stu-id="41272-116">**Orderd Quantity**</span></span>
- <span data-ttu-id="41272-117">**Количество в заказе**</span><span class="sxs-lookup"><span data-stu-id="41272-117">**On-order Quantity**</span></span>
- <span data-ttu-id="41272-118">**Зарезервированное заказанное количество**</span><span class="sxs-lookup"><span data-stu-id="41272-118">**Reserved Ordered Quantity**</span></span>
- <span data-ttu-id="41272-119">**Общее доступное количество**</span><span class="sxs-lookup"><span data-stu-id="41272-119">**Total Available Quantity**</span></span>

## <a name="atp-information"></a><span data-ttu-id="41272-120">Информация о "доступно для резервирования"</span><span class="sxs-lookup"><span data-stu-id="41272-120">ATP information</span></span>

<span data-ttu-id="41272-121">В номенклатурах строки в формах **Предложения**, **Заказы** или **Накладные** в Dynamics 365 Sales добавлена новая кнопка **Информация ATP**.</span><span class="sxs-lookup"><span data-stu-id="41272-121">On line items of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **ATP Information** is added.</span></span> <span data-ttu-id="41272-122">При нажатии на кнопку появляется диалоговое окно, в котором можно указать компанию, продукт, сайт запасов, склад запасов и количество заказа.</span><span class="sxs-lookup"><span data-stu-id="41272-122">When you click the button, a dialog box appears and you can specify the company, product, inventory Site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="41272-123">Она возвращает **Информация ATP** из Supply Chain Management и отображает настройки, описанные в [Резервирование по заказам](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="41272-123">It returns the **ATP Information** from Supply Chain Management and shows the settings descrbed in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span> <span data-ttu-id="41272-124">Эти сведения включают в себя **Количество ATP**, **Полученное количество**, **Количество расходов** и **Количество в наличии**.</span><span class="sxs-lookup"><span data-stu-id="41272-124">The information includes **ATP quantity**, **Receipt quantity**, **Issue quantity**, and **On-hand quantity**.</span></span>
