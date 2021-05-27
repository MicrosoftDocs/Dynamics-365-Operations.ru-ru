---
title: Настройте параметры TDS в модуле "Расчеты с поставщиками" и "Расчеты с клиентами"
description: В этой теме объясняется, как настроить параметры модуля расчетов с поставщиками и расчетов с клиентами для поддержки вычета налога, удерживаемого в источнике (TDS).
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
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023538"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="62439-103">Настройте параметры TDS в модуле "Расчеты с поставщиками" и "Расчеты с клиентами"</span><span class="sxs-lookup"><span data-stu-id="62439-103">Set TDS parameters in Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62439-104">В этой теме объясняется, как настроить параметры модуля расчетов с поставщиками и расчетов с клиентами для поддержки вычета налога, удерживаемого в источнике (TDS).</span><span class="sxs-lookup"><span data-stu-id="62439-104">This topic explains how to set parameters in Accounts payable and Accounts receivable to support Tax Deducted at Source (TDS) deductions.</span></span>

1. <span data-ttu-id="62439-105">Перейдите в раздел **Налог \> Настройка \> Параметры \> Параметры модуля расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="62439-105">Go to **Tax \> Setup \> Parameters \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="62439-106">На вкладке **Обновления** выберите **Обновление строк заказа**, чтобы открыть диалоговое окно **Обновление строк заказа**.</span><span class="sxs-lookup"><span data-stu-id="62439-106">On the **Updates** tab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
3. <span data-ttu-id="62439-107">В разделе **Группа TDS** в поле **Обновление группы TDS** укажите метод, который будет использоваться для обновления группы TDS на уровне строк.</span><span class="sxs-lookup"><span data-stu-id="62439-107">In the **TDS group** section, in the **Updating TDS group** field, specify the method to use to update the TDS group at the line level.</span></span> <span data-ttu-id="62439-108">Этот параметр используется, если группа TDS обновлена в заголовке заказа.</span><span class="sxs-lookup"><span data-stu-id="62439-108">This setting is used when the TDS group is updated on an order header.</span></span> <span data-ttu-id="62439-109">Имеются следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="62439-109">The following options are available:</span></span>

    - <span data-ttu-id="62439-110">**Никогда** — группа TDS не обновляется в строках заказа при обновлении заголовка заказа.</span><span class="sxs-lookup"><span data-stu-id="62439-110">**Never** – The TDS group isn't updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="62439-111">**Всегда** — группа TDS обновляется в строках заказа при обновлении заголовка заказа.</span><span class="sxs-lookup"><span data-stu-id="62439-111">**Always** – The TDS group is automatically updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="62439-112">**Запрос** — пользователи получат сообщение, предлагающее обновить группу TDS в строках заказа.</span><span class="sxs-lookup"><span data-stu-id="62439-112">**Prompt** – Users receive a message that prompts them to update the TDS group on the order lines.</span></span>
4. <span data-ttu-id="62439-113">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="62439-113">Select **OK**.</span></span>

    <span data-ttu-id="62439-114">[![Диалоговое окно "Обновление строк заказа"](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span><span class="sxs-lookup"><span data-stu-id="62439-114">[![Update order lines dialog box](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span></span>

5. <span data-ttu-id="62439-115">Перейдите в раздел **Налог \> Настройка \> Параметры \> Параметры модуля расчетов с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="62439-115">Go to **Tax \> Setup \> Parameters \> Accounts payable parameters**.</span></span>
6. <span data-ttu-id="62439-116">На вкладке **Общие** на экспресс-вкладке **Разбивка по сведениям о доставке** установите для параметра **Поступление продуктов** значение **Да**, чтобы разнести и разделить поступление продуктов, у которых другие адреса поставки и номера налоговых счетов (TAN).</span><span class="sxs-lookup"><span data-stu-id="62439-116">On the **General** tab, on the **Split based on delivery information** FastTab, set the **Product receipt** option to **Yes** to post and split a product receipt that has different delivery addresses and tax account numbers (TANs).</span></span> <span data-ttu-id="62439-117">Если для этого параметра установлено значение **Нет**, разноска отборочной накладной по покупке с другими адресами доставки и номерами TAN.</span><span class="sxs-lookup"><span data-stu-id="62439-117">If this option is set to **No**, you can't post a purchase packing slip that has different delivery addresses and TANs.</span></span>
7. <span data-ttu-id="62439-118">Установите для параметра **Накладная** значение **Да**, чтобы разнести и разбить накладную по покупке, имеющую другие адреса доставки и номера TAN.</span><span class="sxs-lookup"><span data-stu-id="62439-118">Set the **Invoice** option to **Yes** to post and split a purchase invoice that has different delivery addresses and TANs.</span></span>

    <span data-ttu-id="62439-119">[![Экспресс-вкладка разбиения на основе информации о доставке](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span><span class="sxs-lookup"><span data-stu-id="62439-119">[![Split based on delivery information FastTab](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span></span>

8. <span data-ttu-id="62439-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="62439-120">Close the page.</span></span>
