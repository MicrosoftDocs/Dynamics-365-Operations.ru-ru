---
title: Изменение валюты учета или валюты отчетности
description: В этом разделе описывается, как изменить валюту учета или валюту отчетности либо добавить валюту отчетности в настройку книги учета.
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0435deb009173684c7faaf5340e8095c019ec71c
ms.sourcegitcommit: 2cd82983357b32f70f4e4a0c15d4d1f69e08bd54
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/20/2021
ms.locfileid: "6085482"
---
# <a name="change-the-accounting-or-reporting-currency"></a><span data-ttu-id="9c4c2-103">Изменение валюты учета или валюты отчетности</span><span class="sxs-lookup"><span data-stu-id="9c4c2-103">Change the accounting or reporting currency</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c4c2-104">В этом разделе описывается, как изменить валюту учета или валюту отчетности либо добавить валюту отчетности в настройку книги учета.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-104">This topic explains how to change the accounting or reporting currency, or add a reporting currency to the setup of a ledger.</span></span>

## <a name="symptom"></a><span data-ttu-id="9c4c2-105">Симптом</span><span class="sxs-lookup"><span data-stu-id="9c4c2-105">Symptom</span></span>

<span data-ttu-id="9c4c2-106">Вам требуется изменить валюту учета или валюту отчетности либо добавить валюту отчетности в настройку книги учета.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-106">You want to change the accounting or reporting currency, or add a reporting currency to the ledger setup.</span></span> <span data-ttu-id="9c4c2-107">Обычно это происходит в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="9c4c2-107">This typically occurs in the following scenarios:</span></span>

- <span data-ttu-id="9c4c2-108">При настройке юридического лица была указана неправильная валюта учета или валюта отчетности.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-108">The wrong accounting or reporting currency was specified when a legal entity was set up.</span></span> <span data-ttu-id="9c4c2-109">Теперь вы хотите изменить эту валюту.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-109">You now want to change that currency.</span></span>
- <span data-ttu-id="9c4c2-110">Валюта отчетности была указана при настройке юридического лица, но теперь организация хочет удалить валюту отчетности.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-110">A reporting currency was specified when a legal entity was set up, but the organization now wants to remove the reporting currency.</span></span>
- <span data-ttu-id="9c4c2-111">Организация выполняет обновление или переход на Microsoft Dynamics 365 Finance и хочет изменить валюту учета или валюту отчетности.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-111">The organization is upgrading or migrating to Microsoft Dynamics 365 Finance, and wants to change the accounting or reporting currency.</span></span>

<span data-ttu-id="9c4c2-112">Организация, которая ранее не использовала возможность двойной валюты, хочет начать пользоваться ею.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-112">An organization that didn't previously use the Dual currency capability wants to start to use it.</span></span> <span data-ttu-id="9c4c2-113">Эта проблема обычно происходит в следующих сценариях.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-113">This issue typically occurs in the following scenarios.</span></span>

- <span data-ttu-id="9c4c2-114">При настройке юридического лица не была указана валюта отчетности.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-114">No reporting currency was specified when a legal entity was set up.</span></span> <span data-ttu-id="9c4c2-115">(Валюта отчетности необязательна.) Теперь вы хотите добавить валюту отчетности.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-115">(A reporting currency is optional.) You now want to add a reporting currency.</span></span>

## <a name="resolution"></a><span data-ttu-id="9c4c2-116">Решение</span><span class="sxs-lookup"><span data-stu-id="9c4c2-116">Resolution</span></span>

<span data-ttu-id="9c4c2-117">Прежде всего следует учитывать, были ли какие-либо проводки (фактические или бюджетные) разнесены в юридическое лицо для настройки книги учета.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-117">The most important consideration is whether any transactions (actual or budget) have been posted in the legal entity for the ledger setup.</span></span> <span data-ttu-id="9c4c2-118">**Невозможно изменить валюту учета или валюту отчетности либо добавить валюту отчетности, если какие-либо проводки (фактические или бюджетные) были разнесены в юридическое лицо.**</span><span class="sxs-lookup"><span data-stu-id="9c4c2-118">**You can't change the accounting or reporting currency, or add a reporting currency, if any transactions (actual or budget) have been posted in the legal entity.**</span></span> <span data-ttu-id="9c4c2-119">Выполните шаги в одном из следующих разделов в зависимости от того, были ли разнесены проводки.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-119">Follow the steps in one of the following sections, depending on whether transactions have been posted.</span></span>

### <a name="no-transactions-have-been-posted"></a><span data-ttu-id="9c4c2-120">Проводки не были разнесены</span><span class="sxs-lookup"><span data-stu-id="9c4c2-120">No transactions have been posted</span></span>

1. <span data-ttu-id="9c4c2-121">В юридическом лице, для которого обновляются валюты, перейдите в раздел **Главная книга \> Настройка книги учета \> Книга учета**.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-121">In the legal entity that you're updating currencies for, go to **General ledger \> Ledger setup \> Ledger**.</span></span>
2. <span data-ttu-id="9c4c2-122">На странице **Книга учета** выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-122">On the **Ledger** page, select **Edit**.</span></span>
3. <span data-ttu-id="9c4c2-123">На экспресс-вкладке **Валюта** выберите валюту учета и валюту отчетности для использования в юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-123">On the **Currency** FastTab, select the accounting currency and reporting currency to use for the legal entity.</span></span>
4. <span data-ttu-id="9c4c2-124">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-124">Select **Save**.</span></span>

<span data-ttu-id="9c4c2-125">Если поля для валюты учета и валюты отчетности недоступны на странице **Книга учета**, одна или несколько проводок (фактических или бюджетных) были разнесены в юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-125">If the fields for the accounting currency and the reporting currency aren't available on the **Ledger** page, one or more transactions (actual or budget) have been posted in the legal entity.</span></span> <span data-ttu-id="9c4c2-126">Следовательно, изменить валюты невозможно.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-126">Therefore, the currencies can't be changed.</span></span> <span data-ttu-id="9c4c2-127">В этом случае выполните шаги в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-127">In this case, follow the steps in the next section.</span></span>

### <a name="transactions-have-been-posted"></a><span data-ttu-id="9c4c2-128">Проводки были разнесены</span><span class="sxs-lookup"><span data-stu-id="9c4c2-128">Transactions have been posted</span></span>

<span data-ttu-id="9c4c2-129">**Если проводки были разнесены в юридическое лицо, единственный способ изменить или добавить валюту учета и валюту отчетности — создать новое юридическое лицо с правильными валютами.**</span><span class="sxs-lookup"><span data-stu-id="9c4c2-129">**If transactions have been posted in the legal entity, the only way to change or add accounting and reporting currencies is to create a new legal entity that has the correct currencies.**</span></span> <span data-ttu-id="9c4c2-130">Чтобы облегчить этот процесс, функция управления данными в системе позволяет копировать записи настройки и записи справочника из текущего юридического лица в новое юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-130">To help make this process easier, Data management in the system lets you copy setup records and master records from the current legal entity to a new legal entity.</span></span>

<span data-ttu-id="9c4c2-131">Изменения в валюте учета и валюте отчетности носят глобальный характер.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-131">Changes to the accounting and reporting currencies are pervasive.</span></span> <span data-ttu-id="9c4c2-132">Они затрагивают не только главную книгу, но и каждую субкнигу учета (расчеты с клиентами, расчеты с поставщиками, запасы, проект и так далее), всех независимых поставщиков программного обеспечения (ISV) и все добавленные расширения, в которых хранятся суммы.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-132">They affect not only General ledger but also every subledger (Accounts receivable, Accounts payable, Inventory, Project, and so on), every independent software vendor (ISV) solutions, and any extension that you've made that stores amounts.</span></span>

<span data-ttu-id="9c4c2-133">В процессе поиска и перевода каждой суммы в другую валюту могут возникать ошибки.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-133">The process of finding and translating each amount to a different currency is subject to error.</span></span> <span data-ttu-id="9c4c2-134">Следовательно, группа разработчиков не утвердит скрипт, который изменяет или добавляет валюту учета и валюту отчетности.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-134">Therefore, the engineering team won't approve a script that changes or adds accounting and reporting currencies.</span></span> <span data-ttu-id="9c4c2-135">Кроме того, хотя инструмент, который раньше был доступен для Microsoft Dynamics AX 2012, позволяет изменять или добавлять валюту учета и валюту отчетности, этот инструмент был выведен из эксплуатации в AX 2012 R3 и Finance.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-135">Additionally, although a tool that used to be available for Microsoft Dynamics AX 2012 let you change or add accounting and reporting currencies, that tool was deprecated for both AX 2012 R3 and Finance.</span></span>

<span data-ttu-id="9c4c2-136">Выполните следующие шаги, чтобы скопировать настройку и справочник из текущего юридического лица в новое юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-136">Follow these steps to copy the setup and master data from the current legal entity to a new legal entity.</span></span>

1. <span data-ttu-id="9c4c2-137">Перейдите в раздел **Рабочие области \> Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-137">Go to **Workspaces \> Data management**.</span></span>
2. <span data-ttu-id="9c4c2-138">Выберите **Шаблоны** в группе **Импорт и экспорт**.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-138">Select **Templates** under the **Import/Export** group.</span></span>
3. <span data-ttu-id="9c4c2-139">Убедитесь, что шаблоны доступны.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-139">Make sure that templates are available.</span></span> <span data-ttu-id="9c4c2-140">Если шаблоны недоступны, выберите **Загрузить шаблоны по умолчанию** и подождите, пока не будут созданы шаблоны.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-140">If no templates are available, select **Load default templates**, and wait for the templates to be generated.</span></span>
4. <span data-ttu-id="9c4c2-141">Вернитесь в рабочую область **Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-141">Return to the **Data management** workspace.</span></span>
5. <span data-ttu-id="9c4c2-142">Выберите **Копировать в юридическое лицо**.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-142">Select **Copy into legal entity**.</span></span>
6. <span data-ttu-id="9c4c2-143">Введите имя и описание группы.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-143">Enter a group name and description.</span></span>
7. <span data-ttu-id="9c4c2-144">В поле **Исходное юридическое лицо** выберите юридическое лицо для копирования данных.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-144">In the **Source legal entity** field, select the legal entity to copy data from.</span></span>
8. <span data-ttu-id="9c4c2-145">На экспресс-вкладке **Юридические лица назначения** выберите **Создать юридические лица**, чтобы создать новое юридическое лицо, в которое можно скопировать данные исходного юридического лица.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-145">In the **Destination legal entities** FastTab, select **Create legal entities** to create a new legal entity that you can copy the source legal entity data to.</span></span> <span data-ttu-id="9c4c2-146">Выберите **Выбрать существующее**, чтобы скопировать данные в существующее юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-146">Select **Select existing** to copy data to an existing legal entity.</span></span>
9. <span data-ttu-id="9c4c2-147">Дополнительно: задайте для поля **Копировать номерные серии** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-147">Optional: Set the **Copy number sequences** field to **Yes**.</span></span> <span data-ttu-id="9c4c2-148">(Этот шаг рекомендуется при копировании данных.)</span><span class="sxs-lookup"><span data-stu-id="9c4c2-148">(This step is recommended when you copy data.)</span></span>
10. <span data-ttu-id="9c4c2-149">В области **Выбранные объекты** выберите **Добавить шаблон**.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-149">In the **Selected entities** area, select **Add template**.</span></span>
11. <span data-ttu-id="9c4c2-150">Выберите шаблоны для использования.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-150">Select the templates to use.</span></span> <span data-ttu-id="9c4c2-151">Предлагаемые шаблоны для нового юридического лица включают **025 - главная книга** и **Статистика**.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-151">Suggested templates for a new legal entity include **025 - General Ledger** and **Financials**.</span></span> <span data-ttu-id="9c4c2-152">Рекомендуется просмотреть все другие доступные шаблоны, чтобы определить, относится ли какой-либо из них к вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-152">We recommend that you review all the other available templates to determine whether any of them apply to your requirements.</span></span>
12. <span data-ttu-id="9c4c2-153">Выберите **Копировать в юридическое лицо**, чтобы начать процесс пакетной обработки, в результате которого будут созданы выбранные объекты, а затем скопированы в юридическое лицо назначения.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-153">Select **Copy into legal entity** to start a batch process that will create the selected entities and copy them into the destination legal entity.</span></span>
13. <span data-ttu-id="9c4c2-154">По завершении процесса, но до разноски проводок перейдите в книгу учета и обновите валюту учета и валюту отчетности, как описано ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-154">After the process is completed, but before any transaction are posted, go to the ledger, and update the accounting and reporting currencies as described earlier in this topic.</span></span>

<span data-ttu-id="9c4c2-155">Если вы создали новое юридическое лицо, чтобы можно было изменить валюту учета или валюту отчетности, убедитесь, что валюты начальных сальдо старого юридического лица изменены на новые валюты.</span><span class="sxs-lookup"><span data-stu-id="9c4c2-155">If you created a new legal entity so that you can change the accounting or reporting currency, verify that the beginning balances are translated from the currencies of the old legal entity to the new currencies.</span></span>

<span data-ttu-id="9c4c2-156">Видео с предыдущими шагами см. в разделе [Копирование в юридическое лицо](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).</span><span class="sxs-lookup"><span data-stu-id="9c4c2-156">For a video that shows the preceding steps, see [Copy Into Legal Entity](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).</span></span>