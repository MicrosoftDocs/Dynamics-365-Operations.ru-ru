---
title: Связывание основных средств с арендами
description: В теме объясняется, как связать существующее основное средство с новой арендой.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0e2261755d98ee38564b4b864daf8e79551d1239
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814088"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="90064-103">Связывание основных средств с арендами</span><span class="sxs-lookup"><span data-stu-id="90064-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90064-104">В теме объясняется, как связать существующее основное средство с новой арендой.</span><span class="sxs-lookup"><span data-stu-id="90064-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="90064-105">При связывании основных средств с арендой, в качестве значения актива в форме права пользования (ФПП) при первоначальном признании будет использоваться стоимость приобретения основного средства.</span><span class="sxs-lookup"><span data-stu-id="90064-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="90064-106">Прежде чем можно будет связать основное средство с арендой, необходимо создать запись для ОС в модуле основных средств.</span><span class="sxs-lookup"><span data-stu-id="90064-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="90064-107">Затем на странице **Сводка по аренде** необходимо создать аренду и связать актив с этой арендой.</span><span class="sxs-lookup"><span data-stu-id="90064-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="90064-108">Добавьте аренду, следуя шагам в разделе [Добавление или копирование аренд](add-lease.md).</span><span class="sxs-lookup"><span data-stu-id="90064-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="90064-109">На странице **Добавление аренды** в поле **Номер основного средства** выберите актив, который еще не был приобретен.</span><span class="sxs-lookup"><span data-stu-id="90064-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="90064-110">Выберите **Книги** и подтвердите график оплаты.</span><span class="sxs-lookup"><span data-stu-id="90064-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="90064-111">Выберите **Первоначальное признание**.</span><span class="sxs-lookup"><span data-stu-id="90064-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="90064-112">Выберите **Журнал аренды активов**.</span><span class="sxs-lookup"><span data-stu-id="90064-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="90064-113">Запись журнала первоначального признания для аренды дебетует основное средство на сумму, которая обычно дебетуется на счет актива ФПП.</span><span class="sxs-lookup"><span data-stu-id="90064-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="90064-114">Теперь можно просмотреть тип проводки и книгу для основного средства.</span><span class="sxs-lookup"><span data-stu-id="90064-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="90064-115">Выберите **Сведения о журнале**.</span><span class="sxs-lookup"><span data-stu-id="90064-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="90064-116">Выберите **Строки** для просмотра отдельных строк для записи журнала.</span><span class="sxs-lookup"><span data-stu-id="90064-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="90064-117">Выберите строку журнала, содержащую актив, а затем выберите вкладку **Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="90064-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="90064-118">На вкладке **Основные средства** отображается тип проводки и книга.</span><span class="sxs-lookup"><span data-stu-id="90064-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="90064-119">По умолчанию в поле **Тип проводки** установлено значение **Приобретение**, а в поле **Книга** устанавливается текущая книга для основного средства.</span><span class="sxs-lookup"><span data-stu-id="90064-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="90064-120">После разноски записи журнала первоначального признания проводка появится в качестве проводки приобретения для основных средств.</span><span class="sxs-lookup"><span data-stu-id="90064-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="90064-121">Для просмотра таблицы проводок перейдите в раздел **Основные средства \> Основные средства \> Основные средства**, выберите соответствующий актив, а затем выберите **Оценки**.</span><span class="sxs-lookup"><span data-stu-id="90064-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="90064-122">Вы должны видеть, что запись журнала первоначального признания создала проводку приобретения для указанного основного средства.</span><span class="sxs-lookup"><span data-stu-id="90064-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="90064-123">Основное средство теперь можно амортизировать с помощью стандартных функций амортизации в модуле основных средств.</span><span class="sxs-lookup"><span data-stu-id="90064-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="90064-124">Дополнительные сведения об амортизации см. в разделе [Методы амортизации и соглашения по амортизации](../fixed-assets/depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="90064-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="90064-125">Если вы связываете основное средство с арендой, кнопки **Амортизация актива** и **Обесценение аренды** отключаются в модуле аренды активов.</span><span class="sxs-lookup"><span data-stu-id="90064-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="90064-126">Можно просмотреть проводки амортизации и обесценения аренды из модуля основных средств.</span><span class="sxs-lookup"><span data-stu-id="90064-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="90064-127">Кнопка **Проводки по активам**, которая открывает форму запроса, также отключена.</span><span class="sxs-lookup"><span data-stu-id="90064-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="90064-128">Форму запроса **Проводки по активам** можно также открыть в модуле основных средств.</span><span class="sxs-lookup"><span data-stu-id="90064-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]