---
title: Кредитные группы клиентов
description: В этом разделе приводятся сведения о кредитных группах клиента.
author: mikefalkner
manager: AnnBe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fb17a94cd4a472ad609a0c2f688c4a700f072072
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979122"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="60ea5-103">Кредитные группы клиентов</span><span class="sxs-lookup"><span data-stu-id="60ea5-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60ea5-104">Можно определить группы клиентов с общим кредитным лимитом.</span><span class="sxs-lookup"><span data-stu-id="60ea5-104">You can define groups of customers who have a shared credit limit.</span></span> <span data-ttu-id="60ea5-105">Также учитывается индивидуальный кредитный лимит, определенный в счете клиента в накладной.</span><span class="sxs-lookup"><span data-stu-id="60ea5-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="60ea5-106">Участники кредитной группы клиентов могут быть выбраны из других юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="60ea5-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="60ea5-107">При добавлении клиента в список клиентов в кредитной группе клиентов дата окончания кредитного лимита для каждого клиента изменяется на дату окончания срока действия, назначенную группе.</span><span class="sxs-lookup"><span data-stu-id="60ea5-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="60ea5-108">Группы кредитных клиентов можно настроить на странице **Кредитная группа клиентов** (**Управление кредитом \> Кредитные группы клиентов \> Кредитные группы клиентов**).</span><span class="sxs-lookup"><span data-stu-id="60ea5-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="60ea5-109">В полях **номер группы** и **Описание** введите код и описание для группы.</span><span class="sxs-lookup"><span data-stu-id="60ea5-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="60ea5-110">В полях **Кредитный лимит** и **Валюта** введите кредитный лимит и валюту, которые должны использоваться, когда система проверяет кредитный лимит для любого участника группы.</span><span class="sxs-lookup"><span data-stu-id="60ea5-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="60ea5-111">В поле **Дата окончания срока действия кредитного лимита** введите дату окончания кредитного лимита.</span><span class="sxs-lookup"><span data-stu-id="60ea5-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="60ea5-112">Для кредитной группы должна быть указана дата окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="60ea5-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="60ea5-113">После завершения настройки кредитной группы клиентов можно добавлять в нее клиентов, указывая их юридическое лицо и код счета клиента.</span><span class="sxs-lookup"><span data-stu-id="60ea5-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="60ea5-114">При добавлении нового клиента в кредитную группу клиентов система выполняет поиск по одному и тому же счету клиента по всем юридическим лицам и предлагает добавить его в кредитную группу клиента.</span><span class="sxs-lookup"><span data-stu-id="60ea5-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="60ea5-115">Используйте меню **Сальдо по срокам** для просмотра сведений о сальдо по срокам оплаты для всех клиентов накладных в кредитной группе клиентов.</span><span class="sxs-lookup"><span data-stu-id="60ea5-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="60ea5-116">Страница **Сальдо периода распределения по срокам** показывает сводку сальдо по накладным для счетов клиентов.</span><span class="sxs-lookup"><span data-stu-id="60ea5-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>
