---
title: Выбытие РБП (Россия)
description: В этом разделе описывается, как проводится выбытие расходов будущих периодов (РБП).
author: anasyash
manager: AnnBe
ms.date: 06/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: anasyash
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: e4a8667f083117f73c5ba4d017863ce4fbda8cd7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408579"
---
# <a name="dispose-of-deferrals-russia"></a><span data-ttu-id="45b3f-103">Выбытие РБП (Россия)</span><span class="sxs-lookup"><span data-stu-id="45b3f-103">Dispose of deferrals (Russia)</span></span>

[!include [banner](../includes/banner.md)]

1. <span data-ttu-id="45b3f-104">Перейдите к **Главная книга** \> **Журналы** \> **Журнал расходов будущих периодов**.</span><span class="sxs-lookup"><span data-stu-id="45b3f-104">Go to **General ledger** \> **Journals** \> **Deferrals journal**.</span></span>
2. <span data-ttu-id="45b3f-105">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="45b3f-105">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="45b3f-106">В поле **Имя** выберите имя журнала РБП.</span><span class="sxs-lookup"><span data-stu-id="45b3f-106">In the **Name** field, select the deferrals journal name.</span></span>
4. <span data-ttu-id="45b3f-107">В области действий выберите **Строки**, чтобы открыть страницу **Ваучер журнала**.</span><span class="sxs-lookup"><span data-stu-id="45b3f-107">On the Action Pane, select **Lines** to open the **Journal voucher** page.</span></span>
5. <span data-ttu-id="45b3f-108">На панели операций выберите **Групповые операции** \> **Выбытие**, чтобы открыть диалоговое окно **Выбытие**.</span><span class="sxs-lookup"><span data-stu-id="45b3f-108">On the Action Pane, select **Group operations** \> **Disposal** to open the **Disposal** dialog box.</span></span>
6. <span data-ttu-id="45b3f-109">В поле **Дата выбытия** выберите Дата выбытия для транзакции.</span><span class="sxs-lookup"><span data-stu-id="45b3f-109">In the **Disposal date** field, select the disposal date of the transaction.</span></span>
7. <span data-ttu-id="45b3f-110">Настройте параметр **Выбытие по сроку** на **Да**, чтобы удалить значение **Дата выбытия** в в модели стоимости РБП.</span><span class="sxs-lookup"><span data-stu-id="45b3f-110">Set the **Retirement on life time** option to **Yes** to remove of the **Disposal date** value in the deferrals value model.</span></span>
8. <span data-ttu-id="45b3f-111">На экспресс-вкладке **Включаемые записи** выберите **Фильтр**, чтобы открыть диалоговое окно **Запрос**, в котором можно задать критерии выбора.</span><span class="sxs-lookup"><span data-stu-id="45b3f-111">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can set up the selection criteria.</span></span>
9. <span data-ttu-id="45b3f-112">Выберите **OK**, чтобы вернуться к странице **Ваучер журнала**.</span><span class="sxs-lookup"><span data-stu-id="45b3f-112">Select **OK** to return to the **Journal voucher** page.</span></span> <span data-ttu-id="45b3f-113">Сведения об ваучере выбытия отображаются для выбранных расходов будущих периодов на указанную дату.</span><span class="sxs-lookup"><span data-stu-id="45b3f-113">The disposal voucher details are shown for the selected deferrals on the specified date.</span></span>
10. <span data-ttu-id="45b3f-114">Чтобы выбыть один ваучер РБП, на экспресс-вкладке **Обзор** выберите **Создать**, чтобы открыть диалоговое окно **Создать новую строку**.</span><span class="sxs-lookup"><span data-stu-id="45b3f-114">To dispose of one deferral voucher, on the **Overview** FastTab, select **New** to open the **Create new line** dialog box.</span></span>
11. <span data-ttu-id="45b3f-115">В поле **Дата транзакции** введите Дату выбытия для транзакции.</span><span class="sxs-lookup"><span data-stu-id="45b3f-115">In the **Transaction date** field, select the disposal date of the transaction.</span></span>
12. <span data-ttu-id="45b3f-116">В поле **Тип проводки** выберите **Выбытие**.</span><span class="sxs-lookup"><span data-stu-id="45b3f-116">In the **Transactions type** field, select **Disposal**.</span></span>
13. <span data-ttu-id="45b3f-117">В поле **Идентификатор РБП** выберите код расхода будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="45b3f-117">In the **Deferral ID** field, select the deferral code.</span></span>
14. <span data-ttu-id="45b3f-118">В поле **Код модели** выберите код моделей Расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="45b3f-118">In the **Model number** field, select the deferral models number.</span></span> <span data-ttu-id="45b3f-119">Если код модели не определен в журнале, все модели, которые были созданы для данного РБП, будут выбраны.</span><span class="sxs-lookup"><span data-stu-id="45b3f-119">If the model code isn't specified in the journal, all models that were created for the deferral will be selected.</span></span>
15. <span data-ttu-id="45b3f-120">Выберите **OK**, чтобы вернуться к странице **Ваучер журнала**.</span><span class="sxs-lookup"><span data-stu-id="45b3f-120">Select **OK** to return to the **Journal voucher** page.</span></span>
16. <span data-ttu-id="45b3f-121">На панели операций выберите **Функции** \> **Редактировать строку**, чтобы отредактировать журнал перед разноской.</span><span class="sxs-lookup"><span data-stu-id="45b3f-121">On the Action Pane, select **Functions** \> **Edit line** to edit the journal before you post it.</span></span>
17. <span data-ttu-id="45b3f-122">В области действий выберите **Разнести** \> **Разнести**, чтобы разнести ваучер.</span><span class="sxs-lookup"><span data-stu-id="45b3f-122">On the Action Pane, select **Post** \> **Post** to post the voucher.</span></span> <span data-ttu-id="45b3f-123">Выбытие по сроку отображается как значение **Даты выбытия** на модели стоимости РБП.</span><span class="sxs-lookup"><span data-stu-id="45b3f-123">Retirement on life time is shown as the **Disposal date** value on the deferrals value model.</span></span>

    ![Страница моделей РБП](media/rus-dispose-deferrals-01.png)

    > [!NOTE]
    > <span data-ttu-id="45b3f-125">Строка журнала будет разнесена только в том случае, если нет разрыва между последним разнесенным списанием и периодом выбытия.</span><span class="sxs-lookup"><span data-stu-id="45b3f-125">A journal line will be posted only if there is no gap between the last posted write-off and the disposal period.</span></span>

18. <span data-ttu-id="45b3f-126">Чтобы просмотреть разнесенные проводки, перейдите к **Главная книга** \> **Расходы будущих периодов** \> **Расходы будущих периодов**.</span><span class="sxs-lookup"><span data-stu-id="45b3f-126">To view the posted transactions, go to **General ledger** \> **Deferrals** \> **Deferrals**.</span></span> <span data-ttu-id="45b3f-127">На панели операций выберите **Модели РБП**, а затем выберите **Операции списания**.</span><span class="sxs-lookup"><span data-stu-id="45b3f-127">On the Action Pane, select **Deferrals models**, and then select **Writing off transactions**.</span></span>

    <span data-ttu-id="45b3f-128">Когда статус РБП **Закрыт** а строка затенена серым цветом на странице **Модели РБП**, моделей Deferrals, вы можете разнести ваучер реверсирования только в том случае, если его тип проводки является **Списание** и статус **Закрыто**.</span><span class="sxs-lookup"><span data-stu-id="45b3f-128">When the status of a deferral is **Closed**, and the line is shaded gray on the **Deferrals models** page, you can post the reversal voucher only if its transaction type is **Writing off** and its status is **Closed**.</span></span> 

    <span data-ttu-id="45b3f-129">Для просмотра РБП, которые сгенерированы, перейдите к **Главная книга** \> **Расходы будущих периодов** \> **Расходы будущих периодов**.</span><span class="sxs-lookup"><span data-stu-id="45b3f-129">The view the deferrals that are generated, go to **General ledger** \> **Deferrals** \> **Deferrals**.</span></span> <span data-ttu-id="45b3f-130">Для просмотра сведений о проводках на странице **Проводки по РБП**, выберите **Модели РБП**, а затем выберите **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="45b3f-130">To view the transaction details on the **Deferrals transactions** page, select **Deferrals models**, and then select **Transactions**.</span></span>
