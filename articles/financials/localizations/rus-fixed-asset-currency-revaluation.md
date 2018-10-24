---
title: "Переоценка ОС в иностранной валюте"
description: "В этой теме содержится информация о переоценке основных средств в иностранной валюте для России."
author: Anasyash
manager: AnnBe
ms.date: 10/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: Anasyash
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: c82de977ce3e23b77c0a56a5efbbac1da6696d52
ms.contentlocale: ru-ru
ms.lasthandoff: 10/01/2018

---

# <a name="fixed-asset-currency-revaluation"></a><span data-ttu-id="cfd6d-103">Переоценка ОС в иностранной валюте</span><span class="sxs-lookup"><span data-stu-id="cfd6d-103">Fixed asset currency revaluation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cfd6d-104">Представители иностранных организаций имеют право вести учет основных средств в иностранной валюте.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-104">Foreign representatives have the right to keep an account of the fixed assets in the foreign currency.</span></span> <span data-ttu-id="cfd6d-105">Учет основных средств (например, бухгалтерский учет и налоговый учет) может вестись в разных валютах.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-105">Fixed asset accounting (for example, business accounting and tax accounting) can be executed in different currencies.</span></span> <span data-ttu-id="cfd6d-106">Если модель стоимости основных средств вводится в иностранной валюте, валюта учета указывается в записи основного средства.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-106">If a fixed asset value model is entered in a foreign currency, the accounting currency is specified in the asset record.</span></span> <span data-ttu-id="cfd6d-107">Суммы проводок по основным средствам указываются и в валюте учета, и в исходной валюте компании (рублях) по курсу, который действовал на дату проводки.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-107">Fixed asset transaction amounts are specified in both the accounting currency and the original company currency (rubles) at the exchange rate that applied on the transaction date.</span></span> <span data-ttu-id="cfd6d-108">При изменении курса валюты вычисляется переоценка, после чего и для модуля "Основные средства", и для проводок ГК создаются корректирующие проводки прибыли или убытка от курсовой разницы.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-108">When the currency exchange rate is changed, a revaluation is calculated and profit or loss exchange rate adjustment transactions are created both for fixed asset module and ledger transactions.</span></span>

<span data-ttu-id="cfd6d-109">Отдельные или групповые проводки переоценки в иностранной валюте могут рассчитываться для стоимости объектов амортизируемого имущества.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-109">Individual or group currency revaluation transactions can be calculated for the value of objects of depreciated property.</span></span> <span data-ttu-id="cfd6d-110">По окончании групповых проводок записи для переоценки в иностранной валюте и амортизации, рассчитанные по курсу, действующему на дату создания проводок, обновляются.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-110">When group transactions are ended, records for the currency revaluation and depreciation that were calculated at the rate that applied on the date when the transactions were created are updated.</span></span> <span data-ttu-id="cfd6d-111">По окончании отдельных проводок переоценка в иностранной валюте и амортизация должны рассчитываться отдельно в двух разных проводках.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-111">When individual transactions are ended, the currency revaluation and depreciation must be calculated separately in two different transactions.</span></span>

<span data-ttu-id="cfd6d-112">При переоценке валюты (амортизации) происходят следующие изменения:</span><span class="sxs-lookup"><span data-stu-id="cfd6d-112">The following changes occur when currency is revaluated (depreciated):</span></span>

- <span data-ttu-id="cfd6d-113">В главной книге создаются корреспондирующие проводки.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-113">Corresponding transactions are created in the ledger.</span></span>
- <span data-ttu-id="cfd6d-114">Поля **Переоценка стоимости в валюте** в диалоговом окне **Баланс по ОС** обновляются.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-114">The **Currency cost revaluate** fields in the **Balance by FA** dialog box are updated.</span></span>
- <span data-ttu-id="cfd6d-115">Амортизированная стоимость основного средства обновляется.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-115">The depreciated cost of the fixed asset is updated.</span></span>

## <a name="revalue-the-currency-of-fixed-assets"></a><span data-ttu-id="cfd6d-116">Переоценка валюты основных средств</span><span class="sxs-lookup"><span data-stu-id="cfd6d-116">Revalue the currency of fixed assets</span></span>

1. <span data-ttu-id="cfd6d-117">Выберите **Основные средства (Россия) \> Журналы \> Журнал ОС**.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-117">Select **Fixed assets (Russia) \> Journals \> FA journal**.</span></span>
2. <span data-ttu-id="cfd6d-118">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-118">Select **New**.</span></span> <span data-ttu-id="cfd6d-119">В поле **Описание** введите краткое описание журнала.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-119">In the **Description** field, enter a short description of the journal.</span></span>
3. <span data-ttu-id="cfd6d-120">Выберите **Строки**, чтобы открыть страницу **Ваучер журнала**, на которой можно вводить проводки по основным средствам.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-120">Select **Lines** to open the **Journal voucher** page, where you can enter fixed asset transactions.</span></span>
4. <span data-ttu-id="cfd6d-121">Выберите **Создать**, чтобы открыть диалоговое окно **Добавление в журнал**.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-121">Select **New** to open the **Add to journal** dialog box.</span></span>
5. <span data-ttu-id="cfd6d-122">В поле **Тип проводки** выберите **Переоценка валюты**, а затем в поле **Инвентарный номер ОС**, выберите основное средство.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-122">In the **Transaction type** field, select **Currency cost revaluation**, and then, in the **FA inventory number**, select the fixed asset.</span></span> <span data-ttu-id="cfd6d-123">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-123">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cfd6d-124">Строки журнала создаются только в том случае, если валютный курс для основного средства отличается от валютного курса, действовавшего на дату ввода основного средства в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-124">Journal lines are created only if the exchange rate for the fixed asset differs from the exchange rate that applied on the date when the fixed asset was put into operation.</span></span>

6. <span data-ttu-id="cfd6d-125">Проверьте информацию в полях **Дебет**, **Дата** и **Валюта**.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-125">Verify the information in the **Debit**, **Date**, and **Currency** fields.</span></span> <span data-ttu-id="cfd6d-126">Измените сумму переоценки стоимости и дату проводки, если требуются другие значения.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-126">Change the cost revaluation amount and transaction date if different values are required.</span></span>
7. <span data-ttu-id="cfd6d-127">Выберите **Разнести \> Разнести**.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-127">Select **Post \> Post**.</span></span> <span data-ttu-id="cfd6d-128">Создаются проводки основных средств и главной книги, и значение в поле **Переоценка стоимости в валюте** в диалоговом окне **Баланс по ОС** обновляется.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-128">The fixed asset and ledger transactions are created, and the value in the **Currency cost revaluate** field in the **Balance by FA** dialog box is updated.</span></span> <span data-ttu-id="cfd6d-129">Также обновляется переоценка амортизации в валюте.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-129">The currency revaluation of depreciation is also updated.</span></span>

## <a name="reverse-revaluation-transactions"></a><span data-ttu-id="cfd6d-130">Реверсирование проводок переоценки</span><span class="sxs-lookup"><span data-stu-id="cfd6d-130">Reverse revaluation transactions</span></span>

<span data-ttu-id="cfd6d-131">Проводки переоценки реверсируются так же, как проводки приобретения (проводки ввода в эксплуатацию).</span><span class="sxs-lookup"><span data-stu-id="cfd6d-131">Revaluation transactions are reversed in the same way as acquisition transactions (putting into operation transactions).</span></span> <span data-ttu-id="cfd6d-132">Создается две проводки: проводка переоценки стоимости и проводка переоценки амортизации.</span><span class="sxs-lookup"><span data-stu-id="cfd6d-132">Two transactions are created: a cost revaluation transaction and a depreciation revaluation transaction.</span></span>

