---
title: Устранение неполадок операций с запасами
description: В этом разделе описывается устранение проблем, которые могут встретиться при работе с операциями с запасами.
author: sherry-zheng
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 24e41e35b3e810c509a16b91fffd1e796ab9d134
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832066"
---
# <a name="troubleshoot-inventory-operations"></a><span data-ttu-id="9ce02-103">Устранение неполадок операций с запасами</span><span class="sxs-lookup"><span data-stu-id="9ce02-103">Troubleshoot inventory operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ce02-104">В этом разделе описывается устранение проблем, которые могут встретиться при работе с операциями с запасами.</span><span class="sxs-lookup"><span data-stu-id="9ce02-104">This topic describes how to fix issues that you might encounter while you work with inventory operations.</span></span>

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a><span data-ttu-id="9ce02-105">Не удается найти раскрывающиеся диалоговое окно "Рабочий процесс" для журналов запасов.</span><span class="sxs-lookup"><span data-stu-id="9ce02-105">I can't find the "Workflow" drop-down dialog box for inventory journals.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9ce02-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="9ce02-106">Issue description</span></span>

<span data-ttu-id="9ce02-107">Вы не можете найти раскрывающееся диалоговое окно **Рабочий процесс** на странице журнала или связанные операции рабочего процесса недоступны.</span><span class="sxs-lookup"><span data-stu-id="9ce02-107">You can't find the **Workflow** drop-down dialog box on the journal page, or related workflow operations aren't available.</span></span>

<span data-ttu-id="9ce02-108">Эта проблема может возникнуть по трем причинам, как описано в следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="9ce02-108">This issue can occur for three reasons, as described in the following subsections.</span></span>

### <a name="issue-resolution-1"></a><span data-ttu-id="9ce02-109">Устранение проблемы 1</span><span class="sxs-lookup"><span data-stu-id="9ce02-109">Issue resolution 1</span></span>

<span data-ttu-id="9ce02-110">Если проблема относится ко всем пользователям, это может быть связано с тем, что рабочий процесс утверждения не был назначен имени журнала.</span><span class="sxs-lookup"><span data-stu-id="9ce02-110">If the issue applies to all users, it might be occurring because the approval workflow hasn't been assigned to the journal name.</span></span> <span data-ttu-id="9ce02-111">Чтобы устранить проблему, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9ce02-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="9ce02-112">Перейдите в раздел **Управление запасами &gt; Настройка &gt; Имена журналов &gt; Запасы**.</span><span class="sxs-lookup"><span data-stu-id="9ce02-112">Go to **Inventory Management &gt; Setup &gt; Journal names &gt; Inventory**.</span></span>
1. <span data-ttu-id="9ce02-113">В области списка выберите имя журнала, чтобы открыть его настройки.</span><span class="sxs-lookup"><span data-stu-id="9ce02-113">In the list pane, select a journal name to open its settings.</span></span>
1. <span data-ttu-id="9ce02-114">На экспресс-вкладке **Общие** задайте для параметра **Рабочий процесс утверждения** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="9ce02-114">On the **General** FastTab, set the **Approval workflow** option to *Yes*.</span></span> <span data-ttu-id="9ce02-115">Если выводится запрос подтверждения изменения, выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="9ce02-115">If you're prompted to confirm the change, select **Yes**.</span></span>
1. <span data-ttu-id="9ce02-116">В поле **Рабочий процесс** выберите рабочий процесс, который необходимо использовать для выбранного имени журнала.</span><span class="sxs-lookup"><span data-stu-id="9ce02-116">In the **Workflow** field, select the workflow that you want to use for the selected journal name.</span></span>

### <a name="issue-resolution-2"></a><span data-ttu-id="9ce02-117">Устранение проблемы 2</span><span class="sxs-lookup"><span data-stu-id="9ce02-117">Issue resolution 2</span></span>

<span data-ttu-id="9ce02-118">Если в рабочем процессе используется настраиваемый код, проблемы могут возникнуть после обновления системы.</span><span class="sxs-lookup"><span data-stu-id="9ce02-118">If your workflow uses customized code, issues might occur after you upgrade the system.</span></span> <span data-ttu-id="9ce02-119">Например, в рабочем процессе журнала кнопка **Отправить** может быть недоступна, поэтому вы не сможете выбрать ее, чтобы утвердить отправку.</span><span class="sxs-lookup"><span data-stu-id="9ce02-119">For example, in the journal workflow, the **Submit** button might be grayed out so you can't select it to approve a submission.</span></span>

<span data-ttu-id="9ce02-120">Если кнопка **Отправить** неактивна, возможно, ваш рабочий процесс был настроен, что означает, что метод рабочего процесса `canSubmitToWorkflow()` в `FormDataUtil` был расширен.</span><span class="sxs-lookup"><span data-stu-id="9ce02-120">If the **Submit** button is grayed out, your workflow might have been customized, which means the method of the workflow, `canSubmitToWorkflow()` in `FormDataUtil`, has been extended.</span></span> <span data-ttu-id="9ce02-121">Чтобы устранить эту проблему, измените способ, которым вы расширяете метод `canSubmitToWorkflow()` для использования структуры в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="9ce02-121">To fix this issue, change the way that you extend the method of the `canSubmitToWorkflow()` to use the structure in the following example.</span></span>

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a><span data-ttu-id="9ce02-122">Устранение проблемы 3</span><span class="sxs-lookup"><span data-stu-id="9ce02-122">Issue resolution 3</span></span>

<span data-ttu-id="9ce02-123">Если проблема относится только к нескольким определенным пользователям, у этих пользователей могут отсутствовать права доступа, необходимые для выполнения операций с рабочим процессом в журналах запасов.</span><span class="sxs-lookup"><span data-stu-id="9ce02-123">If the issue applies only to a few specific users, those users might not have the security privileges that are required to run workflow operations on inventory journals.</span></span> <span data-ttu-id="9ce02-124">Убедитесь, что у каждого затронутого пользователя имеется привилегия безопасности *Ведение рабочего процесса журнала запасов*.</span><span class="sxs-lookup"><span data-stu-id="9ce02-124">Verify that each affected user has the *Maintain inventory journal workflow* security privilege.</span></span> <span data-ttu-id="9ce02-125">По умолчанию эта привилегия назначается полномочиям с тем же именем, и эти полномочия применяются к ролям *Сотрудник склада* и *Менеджер склада*.</span><span class="sxs-lookup"><span data-stu-id="9ce02-125">By default, this privilege is assigned to a duty that has same name, and that duty is applied to the *Warehouse worker* and *Warehouse manager* roles.</span></span>

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a><span data-ttu-id="9ce02-126">Мой журнал запасов остается в состоянии заблокированного системой, и пакетное задание рабочего процесса не работает.</span><span class="sxs-lookup"><span data-stu-id="9ce02-126">My inventory journal remains in system-locked status, and the workflow batch job doesn't work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9ce02-127">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="9ce02-127">Issue description</span></span>

<span data-ttu-id="9ce02-128">Один из журналов запасов заблокирован какой-либо операцией и не освобождается.</span><span class="sxs-lookup"><span data-stu-id="9ce02-128">One of your inventory journals is locked by some operation and isn't being released.</span></span> <span data-ttu-id="9ce02-129">Например, если во время разноски (которая является операцией с системной блокировкой) произошла неизвестная ошибка, журнал может остаться в статусе заблокированного системой.</span><span class="sxs-lookup"><span data-stu-id="9ce02-129">For example, if an unknown error occurs during posting (which is a system lock operation), the journal might remain in system-locked status.</span></span> <span data-ttu-id="9ce02-130">В этом случае обработчик рабочего элемента рабочего процесса вызовет ошибку, когда он выполняет проверку блокировки.</span><span class="sxs-lookup"><span data-stu-id="9ce02-130">In this case, the workflow work item handler will throw an error while it does lock validation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9ce02-131">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="9ce02-131">Issue resolution</span></span>

<span data-ttu-id="9ce02-132">Выполните вход в экземпляр SQL Server для Supply Chain Management и проверьте, установлено ли для параметра **InventJournalTable.SystemBlocked** значение *1*.</span><span class="sxs-lookup"><span data-stu-id="9ce02-132">Sign in to the SQL Server instance for Supply Chain Management, and check whether **InventJournalTable.SystemBlocked** is set to *1*.</span></span> <span data-ttu-id="9ce02-133">Если это так, убедитесь, что журнал не должен находиться в состоянии блокировки, затем сбросьте параметр **InventJournalTable.SystemBlocked** на значение *0*.</span><span class="sxs-lookup"><span data-stu-id="9ce02-133">If it is, make sure that the journal should not be in locked status, and then reset **InventJournalTable.SystemBlocked** to *0*.</span></span>

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a><span data-ttu-id="9ce02-134">Мой рабочий процесс журнала запасов никогда не завершается, и журнал не может редактироваться или разноситься.</span><span class="sxs-lookup"><span data-stu-id="9ce02-134">My inventory journal workflow is never completed, and the journal can't be edited or posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9ce02-135">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="9ce02-135">Issue description</span></span>

<span data-ttu-id="9ce02-136">После отправки рабочего процесса утверждения журнала обработка рабочего процесса перестает отвечать, и вы не сможете редактировать или обрабатывать свои журналы.</span><span class="sxs-lookup"><span data-stu-id="9ce02-136">After you submit a journal approval workflow, workflow processing stops responding, and you can't edit or process your journals.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9ce02-137">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="9ce02-137">Issue resolution</span></span>

<span data-ttu-id="9ce02-138">Имеется несколько причин, по которым обработка рабочего процесса может быть не завершена.</span><span class="sxs-lookup"><span data-stu-id="9ce02-138">There are several reasons why workflow processing might not be completed.</span></span> <span data-ttu-id="9ce02-139">Проверьте наличие следующих проблем:</span><span class="sxs-lookup"><span data-stu-id="9ce02-139">Check for the following issues:</span></span>

- <span data-ttu-id="9ce02-140">Перейдите в раздел **Управление запасами &gt; Настройка &gt; Рабочие процессы управления запасами** и проверьте конфигурацию соответствующего рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="9ce02-140">Go to **Inventory management &gt; Setup &gt; Inventory management workflows**, and review the configuration of the affected workflow.</span></span> <span data-ttu-id="9ce02-141">Дополнительные сведения см. в разделе [Рабочие процессы утверждения журналов запасов](inventory-journal-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="9ce02-141">For more information, see [Inventory journal approval workflows](inventory-journal-workflow.md).</span></span>
- <span data-ttu-id="9ce02-142">Возможно, в рабочем процессе возникло исключение или ошибка.</span><span class="sxs-lookup"><span data-stu-id="9ce02-142">The workflow might be encountering an exception or error.</span></span> <span data-ttu-id="9ce02-143">Проверьте историю рабочих элементов затрагиваемого рабочего процесса и проверьте, не содержит ли она ошибку приложения, которая прерывает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="9ce02-143">Review the work item history of the affected workflow to see whether it includes an application error that terminates the workflow.</span></span>
- <span data-ttu-id="9ce02-144">Журнал запасов можно обновить или изменить только в том случае, если он утвержден.</span><span class="sxs-lookup"><span data-stu-id="9ce02-144">The inventory journal can be updated or edited only if it's approved.</span></span> <span data-ttu-id="9ce02-145">Если отзыв активен, можно попытаться отозвать журнал.</span><span class="sxs-lookup"><span data-stu-id="9ce02-145">If recall is active, you can try to recall the journal.</span></span> <span data-ttu-id="9ce02-146">Выполнение пакетного задания рабочего процесса может быть приостановлено по нескольким причинам.</span><span class="sxs-lookup"><span data-stu-id="9ce02-146">Execution of the workflow batch job might be suspended for multiple reasons.</span></span> <span data-ttu-id="9ce02-147">Некоторые из этих причин могут быть вызваны проблемой с платформой рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="9ce02-147">Some of these reasons might be caused by the workflow framework issue.</span></span>

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a><span data-ttu-id="9ce02-148">Условия рабочего процесса журнала запасов применяются только на уровне журнала, а не на уровне строки</span><span class="sxs-lookup"><span data-stu-id="9ce02-148">Inventory journal workflow conditions apply only at the journal level, not at the line level</span></span>

### <a name="issue-description"></a><span data-ttu-id="9ce02-149">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="9ce02-149">Issue description</span></span>

<span data-ttu-id="9ce02-150">Эта проблема может возникнуть, например, при попытке настроить условие рабочего процесса журнала запасов для суммы затрат.</span><span class="sxs-lookup"><span data-stu-id="9ce02-150">You might experience this issue if, for example, you try to set up an inventory journal workflow condition on the cost amount.</span></span> <span data-ttu-id="9ce02-151">Вы настраиваете условие, так что шаг 1 выполняется только в том случае, когда сумма затрат меньше 100.</span><span class="sxs-lookup"><span data-stu-id="9ce02-151">You set up the condition so that step 1 is run only when the cost amount is less than 100.</span></span> <span data-ttu-id="9ce02-152">Вы затем настраиваете другое условие, так что шаг 2 выполняется только в том случае, когда сумма затрат больше или равна 100.</span><span class="sxs-lookup"><span data-stu-id="9ce02-152">You then set up another condition so that step 2 is run only when the cost amount is more than or equal to 100.</span></span> <span data-ttu-id="9ce02-153">Затем, после выполнения рабочего процесса, журнал рабочего процесса показывает только одну строку, а первое условие всегда оценивается как *истинное*, независимо от значения, которое было отправлено.</span><span class="sxs-lookup"><span data-stu-id="9ce02-153">Then, when the workflow is run, the workflow history shows only one line, and the first condition is always evaluated as *true*, regardless of the value that is submitted.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="9ce02-154">Временное решение проблемы</span><span class="sxs-lookup"><span data-stu-id="9ce02-154">Issue workaround</span></span>

<span data-ttu-id="9ce02-155">В текущем выпуске условия рабочего процесса запасов применяются только на уровне журнала, а не на уровне строки.</span><span class="sxs-lookup"><span data-stu-id="9ce02-155">In the current release, inventory workflow conditions apply only at the journal level, not at the line level.</span></span> <span data-ttu-id="9ce02-156">Такое поведение предусмотрено разработчиками.</span><span class="sxs-lookup"><span data-stu-id="9ce02-156">This behavior is by design.</span></span> <span data-ttu-id="9ce02-157">Рекомендуется задавать критерии условий только для атрибутов уровня журнала.</span><span class="sxs-lookup"><span data-stu-id="9ce02-157">We recommend that you set your condition criteria only on journal-level attributes.</span></span>

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a><span data-ttu-id="9ce02-158">Панель фильтра на странице списка запасов в наличии не фильтрует результаты так, как ожидается.</span><span class="sxs-lookup"><span data-stu-id="9ce02-158">The filter pane on the On-hand list page doesn't filter results as I expect.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9ce02-159">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="9ce02-159">Issue description</span></span>

<span data-ttu-id="9ce02-160">Фильтры на панель фильтра на странице **Список запасов в наличии** не фильтрует результаты так, как вы ожидаете.</span><span class="sxs-lookup"><span data-stu-id="9ce02-160">The filters in the filter pane on the **On-hand list** page don't filter results as you expect.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9ce02-161">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="9ce02-161">Issue resolution</span></span>

<span data-ttu-id="9ce02-162">Такое поведение предусмотрено разработчиками.</span><span class="sxs-lookup"><span data-stu-id="9ce02-162">This behavior is by design.</span></span>

<span data-ttu-id="9ce02-163">Страница  **Список запасов в наличии** составляется из подробной таблицы запасов в наличии, которая включает все доступные аналитики.</span><span class="sxs-lookup"><span data-stu-id="9ce02-163">The **On-hand list** page is assembled from a detailed on-hand inventory table that includes all available dimensions.</span></span> <span data-ttu-id="9ce02-164">Однако список на этой странице является сводным.</span><span class="sxs-lookup"><span data-stu-id="9ce02-164">However, the list on this page is a summary.</span></span> <span data-ttu-id="9ce02-165">Таким образом, это может быть сочетание строк из исходной таблицы путем агрегирования значений в соответствии с отображаемыми аналитиками.</span><span class="sxs-lookup"><span data-stu-id="9ce02-165">Therefore, it might combine rows from the source table by aggregating values according to the dimensions that are shown.</span></span>

<span data-ttu-id="9ce02-166">Фильтры, которые настроены в области фильтров, применяются к исходной таблице, а не к сводному списку.</span><span class="sxs-lookup"><span data-stu-id="9ce02-166">Filters that are set up in the filter pane apply to the source table, not to the aggregated list.</span></span> <span data-ttu-id="9ce02-167">Такое поведение может иногда привести к неожиданным результатам, как показано в [следующих примерах](inventory-on-hand-list.md#examples).</span><span class="sxs-lookup"><span data-stu-id="9ce02-167">This behavior can sometimes produce unexpected results, as shown in [these examples](inventory-on-hand-list.md#examples).</span></span>

<span data-ttu-id="9ce02-168">Однако,  [указанные в сетке фильтры](inventory-on-hand-list.md#grid-filters) *применяются*  к сводному списку.</span><span class="sxs-lookup"><span data-stu-id="9ce02-168">However, the [filters that are provided in the grid](inventory-on-hand-list.md#grid-filters) *do* apply to the aggregated list.</span></span> <span data-ttu-id="9ce02-169">К этим фильтрам относятся QuickFilter в верхней части сетки и фильтр для каждого заголовка столбца.</span><span class="sxs-lookup"><span data-stu-id="9ce02-169">These filters include both the QuickFilter at the top of the grid and the filter for each column heading.</span></span>

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a><span data-ttu-id="9ce02-170">Единица измерения и количество в единицах измерения неправильно работают в журнале запасов.</span><span class="sxs-lookup"><span data-stu-id="9ce02-170">The unit and unit quantity aren't working correctly in the inventory journal.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9ce02-171">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="9ce02-171">Issue description</span></span>

<span data-ttu-id="9ce02-172">При работе с единицами измерения и количествами в журнале запасов можно столкнуться с одной или несколькими из перечисленных ниже проблем:</span><span class="sxs-lookup"><span data-stu-id="9ce02-172">You might encounter one or both of the following issues when you work with units and quantities in an inventory journal:</span></span>

- <span data-ttu-id="9ce02-173">Вы не видите единицы измерения или количества в единицах измерения в журнале запасов, когда единица преобразования настроена для выпущенного продукта, и нельзя изменить единицу измерения в журнале запасов.</span><span class="sxs-lookup"><span data-stu-id="9ce02-173">You don't see units or unit quantities in the inventory journal while a unit of conversion is set up for the released product, and you can't change the unit in the inventory journal.</span></span>
- <span data-ttu-id="9ce02-174">Вы видите поля **Количество** и **Единица измерения** в журнале запасов, но не видите поле **Количество в единицах измерения**.</span><span class="sxs-lookup"><span data-stu-id="9ce02-174">You see the **Quantity** and **Unit** fields in the inventory journal, but you don't see the **Unit quantity** field.</span></span> <span data-ttu-id="9ce02-175">Если изменить единицу измерения, ввести количество и разнести журнал, журнал по-прежнему отображает исходную единицу измерения для этого количества.</span><span class="sxs-lookup"><span data-stu-id="9ce02-175">If you change the unit, enter a quantity, and post the journal, the journal still shows the original unit of measurement for that quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9ce02-176">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="9ce02-176">Issue resolution</span></span>

<span data-ttu-id="9ce02-177">Чтобы устранить эту проблему, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9ce02-177">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="9ce02-178">В рабочей области **Управление функциями** убедитесь, что функция *Использование единицы измерения и количества в единицах измерения в журналах запасов* включена.</span><span class="sxs-lookup"><span data-stu-id="9ce02-178">In the **Feature management** workspace, make sure that the *Using unit of measure and unit quantity in inventory journals* feature is turned on.</span></span> <span data-ttu-id="9ce02-179">Эта функция добавляет поля **Единица измерения** и **Количество в единицах измерения** в журнал.</span><span class="sxs-lookup"><span data-stu-id="9ce02-179">This feature adds the **Unit** and **Unit quantity** fields to the journal.</span></span>
1. <span data-ttu-id="9ce02-180">После включения этой функции используйте поля **Количество**, **Количество в единицах измерения** и **Единица измерения** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9ce02-180">After the feature is turned on, use the **Quantity**, **Unit quantity**, and **Unit** fields in the following way:</span></span>

    - <span data-ttu-id="9ce02-181">**Количество** — укажите количество, используя единицу измерения по умолчанию, которая определена для выпущенного продукта.</span><span class="sxs-lookup"><span data-stu-id="9ce02-181">**Quantity** – Specify the quantity by using the default unit that is defined for the released product.</span></span> <span data-ttu-id="9ce02-182">Однако сама единица измерения по умолчанию здесь не отображается.</span><span class="sxs-lookup"><span data-stu-id="9ce02-182">However, the default unit itself isn't shown here.</span></span> <span data-ttu-id="9ce02-183">Если преобразование настроено между единицей измерения по умолчанию и единицей измерения, выбранной в поле **Единица измерения**, поле **Количество** обновляется автоматически в зависимости от значений, выбранных в полях **Количество в единицах измерения** и **Единица измерения**.</span><span class="sxs-lookup"><span data-stu-id="9ce02-183">If a conversion is set up between the default unit and the unit that is selected in the **Unit** field, the **Quantity** field is automatically updated, based on the selections in the **Unit quantity** and **Unit** fields.</span></span>
    - <span data-ttu-id="9ce02-184">**Количество в единицах измерения** — укажите количество, используя единицу измерения, выбранную в поле **Единица измерения**.</span><span class="sxs-lookup"><span data-stu-id="9ce02-184">**Unit quantity** – Specify the quantity by using the unit that is selected in the **Unit** field.</span></span>
    - <span data-ttu-id="9ce02-185">**Единица измерения** — выберите единицу измерения для применения к значению в поле **Количество в единицах измерения**.</span><span class="sxs-lookup"><span data-stu-id="9ce02-185">**Unit** – Select the unit to apply to the value in the **Unit quantity** field.</span></span>

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a><span data-ttu-id="9ce02-186">Я получаю следующее сообщение об ошибке: "Максимальное число десятичных знаков для единицы складского хранения равно 0".</span><span class="sxs-lookup"><span data-stu-id="9ce02-186">I receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9ce02-187">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="9ce02-187">Issue description</span></span>

<span data-ttu-id="9ce02-188">При попытке разноски складской проводки или резервирования запасов появляется следующее сообщение об ошибке: "Максимальное число десятичных знаков для единицы складского хранения равно 0".</span><span class="sxs-lookup"><span data-stu-id="9ce02-188">When you try to post an inventory transaction or an inventory reservation, you receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

<span data-ttu-id="9ce02-189">Эта проблема возникает, когда количество складской проводки указывается в виде десятичного значения, которое меньше уровня точности, поддерживаемого данным полем.</span><span class="sxs-lookup"><span data-stu-id="9ce02-189">This issue occurs when the inventory transaction quantity is specified as a decimal value that is below the level of precision that the field supports.</span></span> <span data-ttu-id="9ce02-190">Например, количество *0,5* было определено для складской проводки, но поддерживаются только целые количества.</span><span class="sxs-lookup"><span data-stu-id="9ce02-190">For example, a quantity of *0.5* has been specified for an inventory transaction, but only integer quantities are supported.</span></span> <span data-ttu-id="9ce02-191">Таким образом, значение должно быть равно *1* вместо *0,5*.</span><span class="sxs-lookup"><span data-stu-id="9ce02-191">Therefore, the value should be *1* instead of *0.5*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9ce02-192">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="9ce02-192">Issue resolution</span></span>

1. <span data-ttu-id="9ce02-193">Выполните следующий сценарий в экземпляре SQL Server для округления количеств в складских проводках.</span><span class="sxs-lookup"><span data-stu-id="9ce02-193">Run the following script on your SQL Server instance to round quantities in the inventory transactions.</span></span> <span data-ttu-id="9ce02-194">Этот сценарий будет исправлять значения в таблице **inventTrans**.</span><span class="sxs-lookup"><span data-stu-id="9ce02-194">This script will correct values in the **inventTrans** table.</span></span>

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. <span data-ttu-id="9ce02-195">Выполните проверку целостности запасов в наличии, когда включен параметр **исправления ошибок**.</span><span class="sxs-lookup"><span data-stu-id="9ce02-195">Run an on-hand consistency check where the **fix error** option is turned on.</span></span> <span data-ttu-id="9ce02-196">Эта проверка исправит значения в таблице **inventSum**.</span><span class="sxs-lookup"><span data-stu-id="9ce02-196">This check will correct values in the **inventSum** table.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9ce02-197">Настоятельно рекомендуется аккуратно изменять сценарий в соответствии с требованиями среды, проверять его в тестовой среде, а затем проверять полученные данные перед выполнением сценария в производственной среде.</span><span class="sxs-lookup"><span data-stu-id="9ce02-197">We strongly recommend that you carefully edit the script as required for your environment, test it in a test environment, and then check the resulting data before you run the script in a production environment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]