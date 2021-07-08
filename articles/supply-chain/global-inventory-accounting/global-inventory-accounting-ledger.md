---
title: Книга глобального учета запасов
description: В этой теме описываются книги глобального учета запасов, которые определяются комбинацией валюты, календаря, соглашения и связи с юридическим лицом.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273214"
---
# <a name="global-inventory-accounting-ledger"></a><span data-ttu-id="6e2f9-103">Книга глобального учета запасов</span><span class="sxs-lookup"><span data-stu-id="6e2f9-103">Global Inventory Accounting ledger</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="6e2f9-104">Глобальный учет запасов имеет свой собственный набор книг.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-104">Global Inventory Accounting has its own set of ledgers.</span></span> <span data-ttu-id="6e2f9-105">Каждый раз, когда проводка, связанная с запасами, обрабатывается для соответствующего юридического лица, система может учитывать эту проводку в любом количестве книг глобального учета запасов по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-105">Each time an inventory-related transaction is processed for a relevant legal entity, the system can account for that transaction in any number of Global Inventory Accounting ledgers, as required.</span></span>

<span data-ttu-id="6e2f9-106">Книга — это реестр дебетовых и кредитовых мер.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-106">A ledger is a register of debit and credit measures.</span></span> <span data-ttu-id="6e2f9-107">Эти меры классифицируются с помощью элементов затрат и счетов субкниги.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-107">These measures are classified by using cost elements and subledger accounts.</span></span> <span data-ttu-id="6e2f9-108">Книга глобального учета запасов — определяется комбинацией валюты, календаря, соглашения и связи с юридическим лицом.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-108">A Global Inventory Accounting ledger is defined by its combination of a currency, a calendar, a convention, and an association with a legal entity.</span></span>

<span data-ttu-id="6e2f9-109">Для настройки книг глобального учета запасов перейдите в раздел **Глобальный учет запасов \> Настройка \> Книги глобального учета запасов**.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-109">To set up your Global Inventory Accounting ledgers, go to **Global inventory accounting \> Setup \> Global inventory accounting ledgers**.</span></span> <span data-ttu-id="6e2f9-110">Для каждой книги установите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="6e2f9-110">For each ledger, set the following fields:</span></span>

- <span data-ttu-id="6e2f9-111">**Имя** — введите имя книги.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-111">**Name** – Enter the name of the ledger.</span></span>
- <span data-ttu-id="6e2f9-112">**Описание** — введите описание книги.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-112">**Description** – Enter a description of the ledger.</span></span>
- <span data-ttu-id="6e2f9-113">**Финансовый календарь** — укажите финансовый календарь для книги учета.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-113">**Fiscal calendar** – Specify the fiscal calendar for the ledger.</span></span>
- <span data-ttu-id="6e2f9-114">**Валютный курс и тип валютного курса** — используйте поля на этой экспресс-вкладке, чтобы выбрать валюту учета, используемую в книге, и тип валютного курса.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-114">**Currency and exchange rate type** – Use the fields on this FastTab to select the accounting currency that the ledger uses, and the exchange rate type.</span></span> <span data-ttu-id="6e2f9-115">Выбранная валюта может отличаться от валюты, используемой юридическим лицом.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-115">The currency that you select can differ from the currency that the legal entity uses.</span></span> <span data-ttu-id="6e2f9-116">В глобальном учете запасов пользователи могут определять столько книг учета затрат, сколько требуется.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-116">In Global Inventory Accounting, users can define as many costing ledgers as they require.</span></span> <span data-ttu-id="6e2f9-117">Глобальный учет запасов поддерживает учет запасов в нескольких валютах и в нескольких оценках.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-117">Global Inventory Accounting supports inventory accounting in multiple currencies and in multiple valuations.</span></span> <span data-ttu-id="6e2f9-118">Задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="6e2f9-118">Set the following fields:</span></span>

    - <span data-ttu-id="6e2f9-119">**Валюта** — выберите валюту затрат, в которой поддерживаются значения, имеющие отношение к складским запасам.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-119">**Currency** – Select the costing currency that inventory-related values are maintained in.</span></span> <span data-ttu-id="6e2f9-120">Эти значения включают стоимость запасов, себестоимость проданных товаров, запасы в пути и все типы отклонений.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-120">These values include the inventory value, cost of goods sold, inventory in transit, and all kinds of variance.</span></span>
    - <span data-ttu-id="6e2f9-121">**Тип валютного курса** — выберите валютный курс, который система должна использовать для преобразования суммы проводки в валюте проводки и стандартную себестоимость номенклатур в валюту учета.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-121">**Exchange rate type** – Select the exchange rate that the system should use to convert the transaction amount in the transaction currency and the standard cost of the items into the costing currency.</span></span>

- <span data-ttu-id="6e2f9-122">**Название соглашения** — определение соглашения.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-122">**Convention name** – Specify a convention.</span></span> <span data-ttu-id="6e2f9-123">Соглашение — это совокупность политик, которые определяют, как будут учитываться затраты в этой книге.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-123">A convention is a collection of policies that establish how costs will be accounted in this ledger.</span></span>
- <span data-ttu-id="6e2f9-124">**Юридическое лицо** — в книге будут учитываться документы, разнесенные в выбранное юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-124">**Legal entity** – The ledger will account the documents that are posted to the selected legal entity.</span></span>
- <span data-ttu-id="6e2f9-125">**Предварительно** — выберите, должны ли складские проводки, созданные до создания книги, обрабатываться в соответствии с валютой и соглашением в книге.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-125">**Priming** – Select whether inventory transactions that were created before the ledger was created should be processed according to the currency and convention in the ledger.</span></span> <span data-ttu-id="6e2f9-126">Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="6e2f9-126">Select one of the following values:</span></span>

    - <span data-ttu-id="6e2f9-127">**Активировано** — в книге должны быть обработаны проводки, созданные до создания книги.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-127">**Activated** – The ledger should process transactions that were created before the ledger was created.</span></span>
    - <span data-ttu-id="6e2f9-128">**Деактивировано** — в книге должны быть обработаны только проводки, созданные после создания книги.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-128">**Deactivated** – The ledger should process only transactions that are created after the ledger was created.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="6e2f9-129">После ввода новых документов вернуть и настроить это поле будет **невозможно**.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-129">You will **not** be able to come back and set this field after you enter new documents.</span></span>

- <span data-ttu-id="6e2f9-130">**Статус** — система автоматически устанавливает статус вновь созданных книг как *Подготовка*.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-130">**Status** – The system automatically sets the status of newly created ledgers to *Prepare*.</span></span>
