---
title: Создание или генерация РБП (Россия)
description: В этом разделе объясняется, как вручную создавать РБП и как их генерировать с помощью периодической задачи.
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
ms.openlocfilehash: 6ed2f33fc5503355b320266621004570a48072dc
ms.sourcegitcommit: 4fd51830be21b95a1398dc80d5429a74bcec73fc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2019
ms.locfileid: "1736977"
---
# <a name="create-or-generate-deferrals-russia"></a><span data-ttu-id="ce1c3-103">Создание или генерация РБП (Россия)</span><span class="sxs-lookup"><span data-stu-id="ce1c3-103">Create or generate deferrals (Russia)</span></span>

[!include [banner](../includes/banner.md)]

## <a name="manually-create-deferrals"></a><span data-ttu-id="ce1c3-104">Создание РБП вручную</span><span class="sxs-lookup"><span data-stu-id="ce1c3-104">Manually create deferrals</span></span>

<span data-ttu-id="ce1c3-105">Можно использовать страницу **Расходы будущего периода** для создания РБП вручную.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-105">You can use the **Deferrals** page to manually create a deferral.</span></span> <span data-ttu-id="ce1c3-106">Необходимо указать модель РБП для РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-106">You must specify the deferrals model for a deferral.</span></span> <span data-ttu-id="ce1c3-107">Статус РБП, который создан вручную, обновляется до **Запланированный**.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-107">The status of a deferral that is manually created is updated to **Scheduled**.</span></span> <span data-ttu-id="ce1c3-108">Нельзя изменить статус вручную.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-108">You can't manually modify the status.</span></span>

1. <span data-ttu-id="ce1c3-109">Перейти к **главная книга** \> **Расходы будущих периодов** \> **Расходы будущих периодов**.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-109">Go to **General ledger** \> **Deferrals** \> **Deferrals**.</span></span>
2. <span data-ttu-id="ce1c3-110">На панели операций выберите **Создать** для создания РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-110">On the Action Pane, select **New** to create a deferral.</span></span>
3. <span data-ttu-id="ce1c3-111">В поле **Идентификатор РБП** введите уникальный идентификационный номер РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-111">In the **Deferral ID** field, enter the unique identification number of the deferral.</span></span>
4. <span data-ttu-id="ce1c3-112">В поле **Имя** введите имя РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-112">In the **Name** field, enter a name for the deferral.</span></span>
5. <span data-ttu-id="ce1c3-113">В поле **Комментарий** введите подробное описание РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-113">In the **Comment** field, enter a detailed description of the deferral.</span></span>
6. <span data-ttu-id="ce1c3-114">В поле **Дата присоединения** выберите дату, когда создан РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-114">In the **Date attached** field, select the date when the deferral is created.</span></span>
7. <span data-ttu-id="ce1c3-115">В поле **Код расхода** выберите код расходов.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-115">In the **Expense code** field, select the expense code.</span></span>
8. <span data-ttu-id="ce1c3-116">В поле **Метод зачета НДС для РБП** выберите метод, который используется, чтобы вычитать налог на добавленную стоимость (НДС) для РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-116">In the **VAT offset method for deferrals** field, select the method that is used to deduct value-added tax (VAT) for the deferral.</span></span> <span data-ttu-id="ce1c3-117">Имеются следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="ce1c3-117">The following options are available:</span></span>

    - <span data-ttu-id="ce1c3-118">**Стандарт** — обработка входящего НДС для счетов-фактур, связанных с расходами будущих периодов с использованием стандартного метода вычета НДС.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-118">**Standard** – Process the incoming VAT for factures that are related to deferrals by using the standard VAT deduction method.</span></span>
    - <span data-ttu-id="ce1c3-119">**Пропорциональный** — обработка входящего НДС для счетов-фактур, связанных с расходами будущих периодов с использованием пропорционального метода вычета НДС.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-119">**Proportionate** – Process the incoming VAT for factures that are related to deferrals by using the proportional VAT deduction method.</span></span>

    ![Страница РБП](media/rus-create-generate-deferrals-01.png)

9. <span data-ttu-id="ce1c3-121">На панели операций на вкладке **Расходы будущих периодов** в группе **Книги** выберите **Модели РБП**, чтобы открыть страницу **Модели РБП**.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-121">On the Action Pane, on the **Deferrals** tab, in the **Books** group, select **Deferrals models** to open the **Deferrals models** page.</span></span>
10. <span data-ttu-id="ce1c3-122">Определите модель РБП, которая должна быть применена для РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-122">Define the deferrals model that must be applied for the deferral.</span></span>

    ![Страница моделей РБП](media/rus-create-generate-deferrals-02.png)

11. <span data-ttu-id="ce1c3-124">На панели операций выберите **Проводки**, чтобы открыть страницу **Проводки по РБП**.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-124">On the Action Pane, select **Transactions** to open the **Deferrals transactions** page.</span></span>
12. <span data-ttu-id="ce1c3-125">Просмотрите проводки, связанные с выбранной моделью для РБП, а затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-125">Review the transactions that are related to the selected model for the deferral, and then close the page.</span></span>

    ![Страница проводок по РБП](media/rus-create-generate-deferrals-03.png)

13. <span data-ttu-id="ce1c3-127">На странице **Модели РБП** на панели операций выберите **Баланс**, чтобы открыть страницу **Баланс по РБП**.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-127">On the **Deferrals models** page, on the Action Pane, select **Balance** to open the **Deferral balances** page.</span></span>
14. <span data-ttu-id="ce1c3-128">Просмотрите балансы, связанные с выбранной моделью для РБП, а затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-128">Review the balances that are related to the selected model for the deferral, and then close the page.</span></span>

    ![Страница балансов по РБП](media/rus-create-generate-deferrals-04.png)

15. <span data-ttu-id="ce1c3-130">На странице **Модели РБП** на панели операций выберите **Сумма списания**, чтобы открыть страницу **Профиль списания расходов будущего периода**.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-130">On the **Deferrals models** page, on the Action Pane, select **Writing off sum** to open **Deferrals writing off profile** page.</span></span>
16. <span data-ttu-id="ce1c3-131">На панели операций выберите **Рассчитать** для рассмотрения рассчитанных сумм списания, которые связаны с выбранной моделью для РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-131">On the Action Pane, select **Calculate** to review calculated writing-off amounts that are related to the selected model for the deferral.</span></span>

    ![Страница профиля списания РБП](media/rus-create-generate-deferrals-05.png)

## <a name="generate-deferrals-by-using-a-periodic-task"></a><span data-ttu-id="ce1c3-133">Создание РБП с помощью периодической задачи</span><span class="sxs-lookup"><span data-stu-id="ce1c3-133">Generate deferrals by using a periodic task</span></span>

<span data-ttu-id="ce1c3-134">Чтобы автоматически создавать РБП, необходимо настроить последовательности расчета и счетчиков для групп РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-134">To automatically generate deferrals, you must set up the sequences of calculation and counters for the deferrals groups.</span></span>

1. <span data-ttu-id="ce1c3-135">Перейдите к **Главная книга** \> **Периодические задачи** \> **Расходы будущих периодов** \> **Создание РБП**.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-135">Go to **General ledger** \> **Periodic tasks** \> **Deferrals** \> **Deferrals creating**.</span></span>

    <span data-ttu-id="ce1c3-136">Можно использовать страницу **Создание РБП** для обновления расчета для РБП или автоматического создания РБП с помощью периодической задачи.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-136">You can use the **Deferrals creating** page to update calculation sequences for deferrals or to automatically generate deferrals by using the periodic task.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ce1c3-137">Прежде чем создавать РБП с использованием периодической задачи, необходимо создать и разнести накладные поставщиков.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-137">Before you can generate deferrals by using the periodic task, you must create and post vendor invoices.</span></span>

    <span data-ttu-id="ce1c3-138">В следующей таблице описаны поля на странице **Создание РБП**.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-138">The following table describes the fields on **Deferrals creating** page.</span></span>

    | <span data-ttu-id="ce1c3-139">Поле</span><span class="sxs-lookup"><span data-stu-id="ce1c3-139">Field</span></span>             | <span data-ttu-id="ce1c3-140">Описание</span><span class="sxs-lookup"><span data-stu-id="ce1c3-140">Description</span></span>                                                                       |
    |-------------------|-----------------------------------------------------------------------------------|
    | <span data-ttu-id="ce1c3-141">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="ce1c3-141">Start date</span></span>        | <span data-ttu-id="ce1c3-142">Дата начала периода расчета РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-142">The start date of the deferral calculation period.</span></span>                                |
    | <span data-ttu-id="ce1c3-143">Дата завершения</span><span class="sxs-lookup"><span data-stu-id="ce1c3-143">End date</span></span>          | <span data-ttu-id="ce1c3-144">Дата окончания периода расчета РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-144">The end date of the deferral calculation period.</span></span>                                  |
    | <span data-ttu-id="ce1c3-145">Последовательность</span><span class="sxs-lookup"><span data-stu-id="ce1c3-145">Sequence</span></span>          | <span data-ttu-id="ce1c3-146">Номер последовательности, указанный на странице **Нормативные расходы — последовательности**.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-146">The sequence number that is specified on the **Standard expenses sequence** page.</span></span> |
    | <span data-ttu-id="ce1c3-147">Описание</span><span class="sxs-lookup"><span data-stu-id="ce1c3-147">Description</span></span>       | <span data-ttu-id="ce1c3-148">Имя последовательности.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-148">The sequence name.</span></span>                                                                |
    | <span data-ttu-id="ce1c3-149">Канал</span><span class="sxs-lookup"><span data-stu-id="ce1c3-149">Channel</span></span>           | <span data-ttu-id="ce1c3-150">Канал вывода РБП для выбранной последовательности.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-150">The deferral output channel for the selected sequence.</span></span>                            |
    | <span data-ttu-id="ce1c3-151">Ссылка на канал</span><span class="sxs-lookup"><span data-stu-id="ce1c3-151">Channel reference</span></span> | <span data-ttu-id="ce1c3-152">Группа РБП, в которой вводятся рассчитанные результаты.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-152">The deferrals group where the calculated results are entered.</span></span>                     |

    <span data-ttu-id="ce1c3-153">В следующей таблице описаны кнопки на панели операций страницы **Создание РБП**.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-153">The following table describes the buttons on the Action Pane of the **Deferrals creating** page.</span></span>

    | <span data-ttu-id="ce1c3-154">Кнопка</span><span class="sxs-lookup"><span data-stu-id="ce1c3-154">Button</span></span>           | <span data-ttu-id="ce1c3-155">Описание</span><span class="sxs-lookup"><span data-stu-id="ce1c3-155">Description</span></span>                                                                               |
    |------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="ce1c3-156">Счетчики</span><span class="sxs-lookup"><span data-stu-id="ce1c3-156">Counters</span></span>         | <span data-ttu-id="ce1c3-157">Откройте страницу **Настройка счетчика**, где можно настроить счетчики для последовательностей расчета.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-157">Open the **Counter setup** page, where you can set up counters for calculation sequences.</span></span> |
    | <span data-ttu-id="ce1c3-158">Рассчитать все</span><span class="sxs-lookup"><span data-stu-id="ce1c3-158">Calculate all</span></span>    | <span data-ttu-id="ce1c3-159">Расчет всех последовательностей коэффициента списания РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-159">Calculate all the deferrals write-off factor sequences.</span></span>                                   |
    | <span data-ttu-id="ce1c3-160">Рассчитать выделенные</span><span class="sxs-lookup"><span data-stu-id="ce1c3-160">Calculate marked</span></span> | <span data-ttu-id="ce1c3-161">Расчет выбранной последовательности коэффициента списания РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-161">Calculate the selected deferrals write-off factor sequence.</span></span>                               |

2. <span data-ttu-id="ce1c3-162">Для создания РБП с помощью периодических задач выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ce1c3-162">To generate deferrals by using the periodic task, follow these steps:</span></span>

    1. <span data-ttu-id="ce1c3-163">Выберите строку, которая включает в себя настроенный счетчик, а затем на панели операций выберите **Рассчитать все** или **Рассчитать выделенные**.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-163">Select the line that includes the counter that you set up, and then, on the Action Pane, select **Calculate all** or **Calculate marked**.</span></span>
    2. <span data-ttu-id="ce1c3-164">В полях **Дата начала** и **Дата окончания** введите диапазон дат для расчета периода РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-164">In the **Start date** and **End date** fields, enter the date range for the deferral calculation period.</span></span>
    3. <span data-ttu-id="ce1c3-165">Установите флажок **Перезаписать**, чтобы перезаписать любые существующие расходы будущих периодов за указанный период, которые не содержат ваучеров списания или выбытия.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-165">Select the **Overwrite** check box to overwrite existing deferrals for the specified period that don't contain write-off vouchers or disposal vouchers.</span></span>
    4. <span data-ttu-id="ce1c3-166">Установите флажок **Предварительный просмотр**, чтобы просмотреть или изменить расходы будущих периодов перед их созданием.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-166">Select the **Preview** check box to view or modify the deferrals before they are created.</span></span>

        <span data-ttu-id="ce1c3-167">При установке этого флажка перед созданием РБП появляется страница, отображая информацию о РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-167">When this check box is selected, a page that shows deferrals information appears before deferrals are created.</span></span> <span data-ttu-id="ce1c3-168">Таким образом, можно изменить параметры для создаваемых РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-168">Therefore, you can change the parameters for the deferrals that are created.</span></span> <span data-ttu-id="ce1c3-169">Если флажок снят, расходы будущих периодов автоматически создаются на основе параметров, введенных на странице **Создание РБП**.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-169">When the check box is cleared, deferrals are automatically generated based on the parameters that were entered on the **Deferrals creating** page.</span></span>

    5. <span data-ttu-id="ce1c3-170">Установите флажок **Только по ваучерам ГК**, чтобы создать расходы будущих периодов только из документов главной книги.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-170">Select the **Only from ledger vouchers** check box to create deferrals only from the ledger documents.</span></span> <span data-ttu-id="ce1c3-171">Все расходы будущих периодов, которые создаются на основе покупок, не будут учитываться.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-171">No deferrals that are generated based on purchases will be accounted for.</span></span>
    6. <span data-ttu-id="ce1c3-172">Перейдите к **Главная книга** \> **Расходы будущих периодов** \> **Расходы будущих периодов** для просмотра создаваемых РБП.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-172">Go to **General ledger** \> **Deferrals** \> **Deferrals** to view the deferrals that are generated.</span></span> <span data-ttu-id="ce1c3-173">Для просмотра сведений о проводках на странице **Проводки по РБП**, на панели операций выберите **Модели РБП**, а затем выберите **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-173">To view the transaction details on the **Deferrals transactions** page, on the Action Pane, select **Deferrals models**, and then select **Transactions**.</span></span>

<span data-ttu-id="ce1c3-174">При создании РБП для накладных поставщика с помощью периодической задачи создаются ваучеры проводки РБП с типом проводки **Приход**.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-174">When you generate deferrals for vendor invoices by using the periodic task, deferral transaction vouchers of **Receipt** type are created.</span></span>