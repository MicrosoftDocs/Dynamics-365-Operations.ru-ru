---
title: Настройка информации о группе TDS, PAN и TAN для поставщиков и клиентов
description: В этой теме объясняется, как настроить сведения о группе налога, удержанного в источнике (TDS), номере постоянного счета (PAN) и номере налогового счета (TAN) для поставщиков и клиентов.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023539"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a><span data-ttu-id="cc09a-103">Настройка информации о группе TDS, PAN и TAN для поставщиков и клиентов</span><span class="sxs-lookup"><span data-stu-id="cc09a-103">TDS group, PAN, and TAN information setup for vendors and customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc09a-104">В этой теме объясняется, как настроить сведения о группе налога, удержанного в источнике (TDS), номере постоянного счета (PAN) и номере налогового счета (TAN) для поставщиков и клиентов.</span><span class="sxs-lookup"><span data-stu-id="cc09a-104">This topic explains how to set up information about the Tax Deducted at Source (TDS) group, permanent account number (PAN), and tax account number (TAN) for vendors and customers.</span></span>

1. <span data-ttu-id="cc09a-105">Перейдите **Расчеты с поставщиками \> Поставщики \> Все поставщики** или **Расчеты с клиентами \> Клиенты \> Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="cc09a-105">Go to **Accounts payable \> Vendors \> All vendors** or **Accounts receivable \> Customers \> All customers**.</span></span>

    <span data-ttu-id="cc09a-106">[![Страница "Все поставщики"](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span><span class="sxs-lookup"><span data-stu-id="cc09a-106">[![All vendors page](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span></span>

2. <span data-ttu-id="cc09a-107">В области действий выберите **Создать**, чтобы создать поставщика или клиента, и введите требуемые сведения.</span><span class="sxs-lookup"><span data-stu-id="cc09a-107">On the Action Pane, select **New** to create a vendor or customer, and enter the required details.</span></span> <span data-ttu-id="cc09a-108">Или выберите существующего поставщика или клиента.</span><span class="sxs-lookup"><span data-stu-id="cc09a-108">Alternatively, select an existing vendor or customer.</span></span>
3. <span data-ttu-id="cc09a-109">На экспресс-вкладке **Накладные и поставка** в разделе **Подоходный налог** установите параметр **Рассчитать подоходный налог** как **Да**, чтобы рассчитать подоходный налог, TDS или налог, удержанный в источнике (TDS), для поставщика или клиента.</span><span class="sxs-lookup"><span data-stu-id="cc09a-109">On the **Invoice and delivery** FastTab, in the **Withholding tax** section, set the **Calculate withholding tax** option to **Yes** to calculate withholding tax, TDS, or Tax Collected at Source (TCS) for the vendor or customer.</span></span>
4. <span data-ttu-id="cc09a-110">TDS для накладной по покупке рассчитывается на основе группы TDS по умолчанию, которая определена для поставщика или клиента.</span><span class="sxs-lookup"><span data-stu-id="cc09a-110">TDS for a purchase invoice is calculated based on the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="cc09a-111">В поле **Группа TDS** выберите группу TDS по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cc09a-111">In the **TDS group** field, select the default TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cc09a-112">Если выбрать группу TDS в поле **Группа TDS**, поля **Группа подоходного налога** и **Группа TCS** становятся недоступными.</span><span class="sxs-lookup"><span data-stu-id="cc09a-112">When you select a TDS group in the **TDS group** field, the **Withholding tax group** and **TCS group** fields become unavailable.</span></span>

5. <span data-ttu-id="cc09a-113">На экспресс-вкладке **Сведения о налоге** в разделе **Сведения о PAN** в поле **Статус** выберите статус постоянного номера счета для поставщика или клиента:</span><span class="sxs-lookup"><span data-stu-id="cc09a-113">On the **Tax information** FastTab, in the **PAN information** section, in the **Status** field, select the status of the permanent account number for the vendor or customer:</span></span>

    - <span data-ttu-id="cc09a-114">**Недоступно** — у поставщика или клиента нет PAN.</span><span class="sxs-lookup"><span data-stu-id="cc09a-114">**Not available** – The vendor or customer doesn't have a PAN.</span></span>
    - <span data-ttu-id="cc09a-115">**Получено** — у поставщика или клиента есть PAN.</span><span class="sxs-lookup"><span data-stu-id="cc09a-115">**Received** – The vendor or customer has a PAN.</span></span>
    - <span data-ttu-id="cc09a-116">**Применяется** — поставщик или клиент подали заявку на PAN.</span><span class="sxs-lookup"><span data-stu-id="cc09a-116">**Applied** – The vendor or customer has applied for a PAN.</span></span>
    - <span data-ttu-id="cc09a-117">**Недопустимо** — у поставщика или клиента есть PAN, но он недопустимый.</span><span class="sxs-lookup"><span data-stu-id="cc09a-117">**Invalid** – The vendor or customer has a PAN, but it isn't valid.</span></span>

6. <span data-ttu-id="cc09a-118">Если выбрано **Получено** в поле **Статус**, чтобы указать, что у поставщика или клиента есть PAN, введите PAN в поле **Номер**.</span><span class="sxs-lookup"><span data-stu-id="cc09a-118">If you selected **Received** in the **Status** field to indicate that the vendor or customer has a PAN, enter the PAN in the **Number** field.</span></span> <span data-ttu-id="cc09a-119">PAN должен состоять из пяти букв, затем четырех цифр, а затем одной буквы.</span><span class="sxs-lookup"><span data-stu-id="cc09a-119">The PAN must consist of five alphabetic characters, then four numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="cc09a-120">Пример: **ABCDE1260A**.</span><span class="sxs-lookup"><span data-stu-id="cc09a-120">Here is an example: **ABCDE1260A**.</span></span>
7. <span data-ttu-id="cc09a-121">Если выбрано **Применено** в поле **Статус**, чтобы указать, что поставщик или клиент подал заявку на PAN, введите справочный номер в поле **Справочный номер**.</span><span class="sxs-lookup"><span data-stu-id="cc09a-121">If you selected **Applied** in the **Status** field to indicate that the vendor or customer has applied for PAN, enter the reference number in the **Reference number** field.</span></span>
8. <span data-ttu-id="cc09a-122">В поле **Суть налогоплательщика** выберите суть категории налогоплательщика, к которой относятся поставщик или клиент:</span><span class="sxs-lookup"><span data-stu-id="cc09a-122">In the **Nature of assessee** field, select the nature of assessee category that the vendor or customer belongs to:</span></span>

    - <span data-ttu-id="cc09a-123">Организация</span><span class="sxs-lookup"><span data-stu-id="cc09a-123">Company</span></span>
    - <span data-ttu-id="cc09a-124">HUF</span><span class="sxs-lookup"><span data-stu-id="cc09a-124">HUF</span></span>
    - <span data-ttu-id="cc09a-125">Утверждение</span><span class="sxs-lookup"><span data-stu-id="cc09a-125">Firm</span></span>
    - <span data-ttu-id="cc09a-126">Индивидуальный</span><span class="sxs-lookup"><span data-stu-id="cc09a-126">Individual</span></span>
    - <span data-ttu-id="cc09a-127">AOP</span><span class="sxs-lookup"><span data-stu-id="cc09a-127">AOP</span></span>
    - <span data-ttu-id="cc09a-128">BOI</span><span class="sxs-lookup"><span data-stu-id="cc09a-128">BOI</span></span>
    - <span data-ttu-id="cc09a-129">Локальный орган</span><span class="sxs-lookup"><span data-stu-id="cc09a-129">Local authority</span></span>
    - <span data-ttu-id="cc09a-130">Прочее</span><span class="sxs-lookup"><span data-stu-id="cc09a-130">Others</span></span>

    <span data-ttu-id="cc09a-131">[![Экспресс-вкладка "Сведения о налоге"](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span><span class="sxs-lookup"><span data-stu-id="cc09a-131">[![Tax information FastTab](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span></span>

9. <span data-ttu-id="cc09a-132">На панели операций на вкладке **Поставщик** в группе **Регистрация** выберите **Регистрационные номера**, чтобы открыть страницу **Управление адресами**.</span><span class="sxs-lookup"><span data-stu-id="cc09a-132">On the Action Pane, on the **Vendor** tab, in the **Registration** group, select **Registration IDs** to open the **Manage addresses** page.</span></span>
10. <span data-ttu-id="cc09a-133">На странице **Управление адресами** на экспресс-вкладке **Сведения о налоге** выберите **Добавить** или **Изменить**, чтобы открыть страницу **Управление сведениями о налогах**, где можно вести запись регистрации налога.</span><span class="sxs-lookup"><span data-stu-id="cc09a-133">On the **Manage addresses** page, on the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>
11. <span data-ttu-id="cc09a-134">На странице **Управление сведениями о налоге** на экспресс-вкладке **Подоходный налог** в поле **Номер налогового счета (TAN)** введите TAN.</span><span class="sxs-lookup"><span data-stu-id="cc09a-134">On the **Manage tax information** page, on the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the TAN.</span></span> <span data-ttu-id="cc09a-135">TAN должен состоять из четырех букв, затем пяти цифр, а затем одной буквы.</span><span class="sxs-lookup"><span data-stu-id="cc09a-135">The TAN must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="cc09a-136">Пример: **AFGH54821T**.</span><span class="sxs-lookup"><span data-stu-id="cc09a-136">Here is an example: **AFGH54821T**.</span></span>
12. <span data-ttu-id="cc09a-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="cc09a-137">Close the page.</span></span>
