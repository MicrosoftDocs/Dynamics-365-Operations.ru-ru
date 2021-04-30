---
title: Запись аренды в иностранной валюте
description: В этой теме объясняется, как записывать аренду в валютах, отличных от валюты учета или валюты отчетности.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 989977fd038ecc6e3276085d795192f5dcab42eb
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881598"
---
# <a name="record-leases-in-foreign-currencies"></a><span data-ttu-id="5ae22-103">Запись аренды в иностранной валюте</span><span class="sxs-lookup"><span data-stu-id="5ae22-103">Record leases in foreign currencies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ae22-104">Счета аренды актива для аренд, которые ведутся в валютах, отличных от валюты учета или валюты отчетности, задаются на странице **Настройка книги учета**.</span><span class="sxs-lookup"><span data-stu-id="5ae22-104">Asset leasing accounts for leases that are in currencies other than the accounting currency or the reporting currency are established on the **Ledger setup** page.</span></span> <span data-ttu-id="5ae22-105">Все аренды должны быть введены в валюте проводки.</span><span class="sxs-lookup"><span data-stu-id="5ae22-105">All leases should be entered in their transaction currency.</span></span> <span data-ttu-id="5ae22-106">Другими словами, они должны вводиться в валюте, указанной в контракте аренды.</span><span class="sxs-lookup"><span data-stu-id="5ae22-106">In other words, they should be entered in the currency that is specified in the lease contract.</span></span> <span data-ttu-id="5ae22-107">В этой теме объясняется, как записывать аренду в валютах, отличных от валюты учета или валюты отчетности.</span><span class="sxs-lookup"><span data-stu-id="5ae22-107">This topic explains how to record leases in currencies other than the accounting or reporting currency.</span></span>

<span data-ttu-id="5ae22-108">При вводе аренды в иностранной валюте, актив в форме права пользования (ФПП) амортизируется как в валюте учета, так и в валюте отчетности.</span><span class="sxs-lookup"><span data-stu-id="5ae22-108">If you enter a lease in a foreign currency, the right-of-use (ROU) asset is depreciated in both the accounting currency and the reporting currency.</span></span> <span data-ttu-id="5ae22-109">Эти валюты настраиваются на странице **Настройка книги учета**.</span><span class="sxs-lookup"><span data-stu-id="5ae22-109">These currencies are configured on the **Ledger setup** page.</span></span> <span data-ttu-id="5ae22-110">Это поведение также используется в модуле основных средств.</span><span class="sxs-lookup"><span data-stu-id="5ae22-110">This behavior is also used in Fixed assets.</span></span> <span data-ttu-id="5ae22-111">При создании аренды в иностранной валюте выберите валюту проводки в поле **Валюта**.</span><span class="sxs-lookup"><span data-stu-id="5ae22-111">When you create a lease in a foreign currency, select the transaction currency in the **Currency** field.</span></span>

<span data-ttu-id="5ae22-112">Валютный курс валюты учета является значением по умолчанию в поле **Валютный курс валюты учета**.</span><span class="sxs-lookup"><span data-stu-id="5ae22-112">The exchange rate of the accounting currency is the default value in **Accounting currency exchange rate** field.</span></span> <span data-ttu-id="5ae22-113">Валютный курс валюты отчетности является значением по умолчанию в поле **Валютный курс валюты отчетности**.</span><span class="sxs-lookup"><span data-stu-id="5ae22-113">The exchange rate of the reporting currency is the default value in the **Reporting currency exchange rate** field.</span></span> <span data-ttu-id="5ae22-114">Эти валютные курсы действовали на дату начала аренды.</span><span class="sxs-lookup"><span data-stu-id="5ae22-114">These exchange rates were effective on the commencement date of the lease.</span></span> <span data-ttu-id="5ae22-115">Поля **Валютный курс валюты учета** и **Валютный курс валюты отчетности** находятся на экспресс-вкладке **Сведения об обмене для финансов и отчетности** на странице **Сведения об аренде**.</span><span class="sxs-lookup"><span data-stu-id="5ae22-115">The **Accounting currency exchange rate** and **Reporting currency exchange rate** fields, are in the **Financial and reporting exchange information** FastTab, on the **Lease details** page.</span></span>

1. <span data-ttu-id="5ae22-116">Установите флажок **Фиксированный курс**, чтобы переопределить введенный автоматически валютный курс, а затем введите новый курс.</span><span class="sxs-lookup"><span data-stu-id="5ae22-116">Select the **Fixed rate** check box to override the exchange rate that was automatically entered, and then enter the new rate.</span></span>
2. <span data-ttu-id="5ae22-117">В других полях введите сведения, необходимые для аренды, а затем выберите **Создать расписания**.</span><span class="sxs-lookup"><span data-stu-id="5ae22-117">In the other fields, enter the information that is required for the lease, and then select **Create schedules**.</span></span>
3. <span data-ttu-id="5ae22-118">На странице **Сведения об аренде** выберите **Книги**.</span><span class="sxs-lookup"><span data-stu-id="5ae22-118">On the new **Lease details** page, select **Books**.</span></span>
4. <span data-ttu-id="5ae22-119">На странице **Книга аренды** на вкладке **Сведения об обмене для финансов и отчетности** проверьте значения полей **Первоначальный актив в форме права пользования в валюте учета** и **Первоначальный актив в форме права пользования в валюте отчетности**.</span><span class="sxs-lookup"><span data-stu-id="5ae22-119">On the **Lease book** page, on the **Financial and reporting exchange information** tab, verify the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span> <span data-ttu-id="5ae22-120">Каждое из этих полей показывает переведенное сальдо актива ФПП в соответствующей валюте.</span><span class="sxs-lookup"><span data-stu-id="5ae22-120">Each of these fields shows the translated ROU asset balance in the corresponding currency.</span></span> <span data-ttu-id="5ae22-121">Эти поля обновляются при каждом изменении любой финансовой информации.</span><span class="sxs-lookup"><span data-stu-id="5ae22-121">These fields are updated whenever you change any financial information.</span></span> <span data-ttu-id="5ae22-122">Выберите **Создать расписания** до подтверждения графика оплаты.</span><span class="sxs-lookup"><span data-stu-id="5ae22-122">Select **Create schedules** before you confirm the payment schedule.</span></span>

    <span data-ttu-id="5ae22-123">Запись журнала первоначального признания записывает актив ФПП, который использует валютные курсы, перечисленные в аренде.</span><span class="sxs-lookup"><span data-stu-id="5ae22-123">The initial recognition journal entry records the ROU asset that uses the currency exchange rates that are listed on the lease.</span></span> <span data-ttu-id="5ae22-124">Запись журнала также включает значения в полях **Первоначальный актив в форме права пользования в валюте учета** и **Первоначальный актив в форме права пользования в валюте отчетности**.</span><span class="sxs-lookup"><span data-stu-id="5ae22-124">The journal entry also includes the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

## <a name="subsequent-measurement-for-foreign-currency-leases"></a><span data-ttu-id="5ae22-125">Последующее измерение для аренды в иностранной валюте</span><span class="sxs-lookup"><span data-stu-id="5ae22-125">Subsequent measurement for foreign currency leases</span></span>

<span data-ttu-id="5ae22-126">График амортизации показывает ожидаемые суммы расходов по амортизации в валюте отчетности, валюте учета и валюте проводки.</span><span class="sxs-lookup"><span data-stu-id="5ae22-126">The depreciation schedule shows the expected depreciation expense amounts in the reporting currency, the accounting currency, and the transaction currency.</span></span>

<span data-ttu-id="5ae22-127">Чтобы просмотреть сальдо актива ФПП и суммы амортизации в валюте отчетности или в валюте учета, откройте страницу **График амортизации актива** и установите флажок **Показать суммы в валюте учета** или **Показать суммы в валюте отчетности**.</span><span class="sxs-lookup"><span data-stu-id="5ae22-127">To view the ROU asset balances and depreciation amounts in either the reporting currency or the accounting currency, open the **Asset depreciation schedule** page, and select the **Show accounting currency amounts** or **Show reporting currency amounts** check box.</span></span>

<span data-ttu-id="5ae22-128">При создании записей журнала расходов на амортизацию по аренде, которая была определена в иностранной валюте, в записи используются валютные курсы, перечисленные в аренде.</span><span class="sxs-lookup"><span data-stu-id="5ae22-128">When you create the depreciation expense journal entries against a lease that is denominated in a foreign currency, the entry uses the exchange rates that are listed on the lease.</span></span> <span data-ttu-id="5ae22-129">Также используются значения в полях **Первоначальный актив в форме права пользования в валюте учета** и **Первоначальный актив в форме права пользования в валюте отчетности**.</span><span class="sxs-lookup"><span data-stu-id="5ae22-129">It also uses the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

<span data-ttu-id="5ae22-130">Окончательную сумму расходов на амортизацию можно рассчитать, используя слегка отличающийся валютный курс, чтобы актив ФПП был полностью амортизировать в валюте учета и в валюте отчетности.</span><span class="sxs-lookup"><span data-stu-id="5ae22-130">The final depreciation expense amount can be calculated by using a slightly different exchange rate, so that the ROU asset is fully depreciated in both the accounting currency and the reporting currency.</span></span>

<span data-ttu-id="5ae22-131">Если аренда была реклассифицирована как **Отложенная рента**, система автоматически очищает обменные курсы в валютах учета и отчетности, если они уже были определены.</span><span class="sxs-lookup"><span data-stu-id="5ae22-131">If the lease has been reclassified as **Deferred rent**, the system automatically clears the exchange rates of the accounting and reporting currencies, if they have already been defined.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
