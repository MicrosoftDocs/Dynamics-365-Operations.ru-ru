---
title: Разноска записей журнала корректировки перехода в аренде активов
description: В этой теме описываются функции, которые позволяют перевести портфель аренды в новые стандарты учета аренды, тема 842 кодификации стандартов бухгалтерского учета (ASC 842) и международный стандарт финансовой отчетности 16 (МСФО 16).
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 7ed62f52753a6697a7547ada0317041669cf3506
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207213"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a><span data-ttu-id="042fb-103">Разноска записей журнала корректировки перехода в аренде активов</span><span class="sxs-lookup"><span data-stu-id="042fb-103">Post transition adjustment journal entries in Asset leasing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="042fb-104">В этой теме описываются функции, которые позволяют перевести портфель аренды в новые стандарты учета аренды: тема 842 кодификации бухгалтерских стандартов (ASC 842), которая является стандартом в общепринятых принципах учета в США (US GAAP), и международный стандарт финансовой отчетности 16 (МСФО 16).</span><span class="sxs-lookup"><span data-stu-id="042fb-104">This topic describes the functionality that lets you transition a lease portfolio to the new lease accounting standards: Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), and International Financial Reporting Standard 16 (IFRS 16).</span></span>

<span data-ttu-id="042fb-105">Сведения о порядке настройки книги для перехода к новым стандартам см. в разделе [Настройка книг аренды](set-up-lease-books.md).</span><span class="sxs-lookup"><span data-stu-id="042fb-105">For information about how to set up a book for the transition to the new standards, see [Set up lease books](set-up-lease-books.md).</span></span>

<span data-ttu-id="042fb-106">При создании записи журнала корректировок перехода создается запись журнала.</span><span class="sxs-lookup"><span data-stu-id="042fb-106">When you create a transition adjustment journal entry, a journal entry is generated.</span></span> <span data-ttu-id="042fb-107">Эта запись отражает влияние на балансовый отчет записи аренды на новые новых стандартов на эту дату.</span><span class="sxs-lookup"><span data-stu-id="042fb-107">This entry reflects the balance sheet impact of recording the lease under the new standards on that date.</span></span> <span data-ttu-id="042fb-108">Соответствующий счет актива дебетуется на учетную сумму на эту дату, а счет обязательств кредитуется.</span><span class="sxs-lookup"><span data-stu-id="042fb-108">The appropriate asset account is debited for the carrying amount on that date, and the liability account is credited.</span></span> <span data-ttu-id="042fb-109">Разница дебетуется или кредитуется на нераспределенную прибыль.</span><span class="sxs-lookup"><span data-stu-id="042fb-109">The difference is either debited or credited to retained earnings.</span></span>

<span data-ttu-id="042fb-110">Чтобы разнести корректировку перехода в соответствие с новыми стандартами учета, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="042fb-110">To post a transition adjustment in compliance with the new accounting standards, follow these steps.</span></span>

1. <span data-ttu-id="042fb-111">На странице **Сводка по аренде** выберите аренду, а затем выберите **Книги**.</span><span class="sxs-lookup"><span data-stu-id="042fb-111">On the **Lease summary** page, select the lease, and then select **Books**.</span></span>
2. <span data-ttu-id="042fb-112">В книге выберите **График оплаты**.</span><span class="sxs-lookup"><span data-stu-id="042fb-112">In the book, select **Payment schedule**.</span></span>
3. <span data-ttu-id="042fb-113">В диалоговом окне **График оплаты** выберите **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="042fb-113">In the **Payment schedule** dialog box, select **Confirm**.</span></span> <span data-ttu-id="042fb-114">Затем закройте диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="042fb-114">Then close the dialog box.</span></span>
4. <span data-ttu-id="042fb-115">Выберите **Корректировка перехода**.</span><span class="sxs-lookup"><span data-stu-id="042fb-115">Select **Transition adjustment**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="042fb-116">Корректировка перехода может быть создана только для тех книг аренды, которые назначены книге, в которой доступно поле **Книга перехода**.</span><span class="sxs-lookup"><span data-stu-id="042fb-116">A transition adjustment can be created only for lease books that are assigned to a book where the **Transition book** field is available.</span></span> <span data-ttu-id="042fb-117">Если значение в поле **Начало аренды** позже даты перехода, значение в поле **Корректировка перехода** не обновляется.</span><span class="sxs-lookup"><span data-stu-id="042fb-117">If the value in the **Lease commencement** field is later than the transition date, the value in the **Transition adjustment** field won't be updated.</span></span>

5. <span data-ttu-id="042fb-118">Для просмотра записи журнала выберите **Журналы аренды активов**.</span><span class="sxs-lookup"><span data-stu-id="042fb-118">To view the journal entry, select **Asset leasing journals**.</span></span>
6. <span data-ttu-id="042fb-119">Выберите новый журнал, затем выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="042fb-119">Select the new journal, and then select **Post**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]