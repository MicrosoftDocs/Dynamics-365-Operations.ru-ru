---
title: Редактирование и аудит проводок розничного магазина
description: В этом разделе описываются функции редактирования и аудита проводок магазина.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004397"
---
# <a name="edit-and-audit-retail-store-transactions"></a><span data-ttu-id="b813d-103">Редактирование и аудит проводок розничного магазина</span><span class="sxs-lookup"><span data-stu-id="b813d-103">Edit and audit retail store transactions</span></span>

[!include [banner](includes/banner.md)]



<span data-ttu-id="b813d-104">Клиенты Dynamics 365 Commerce используют собственные и сторонние POS-приложения.</span><span class="sxs-lookup"><span data-stu-id="b813d-104">Dynamics 365 Commerce customers use first-party as well as third-party point of sale (POS) applications.</span></span> <span data-ttu-id="b813d-105">При работе с собственными POS-приложениями проводки магазина переносятся в Headquarters из каналов через процесс пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="b813d-105">With the first-party POS application, store transactions are pulled into Headquarters from the channels through a batch process.</span></span> <span data-ttu-id="b813d-106">В случае сторонних приложений проводки переносятся в Headquarters через интеграцию.</span><span class="sxs-lookup"><span data-stu-id="b813d-106">With third-party applications, transactions are pulled into Headquarters through integration.</span></span> <span data-ttu-id="b813d-107">В обоих случаях после передачи проводок в Headquarters необходимо выполнить проверку их согласованности, чтобы в журналы, которые будут разноситься в Headquarters, попали только проверенные проводки.</span><span class="sxs-lookup"><span data-stu-id="b813d-107">In both cases, after transactions are pulled into Headquarters, a consistency check process needs to be executed that runs multiple validations on the transactions so that only successfully validated transactions are pulled into the statement to be posted in Headquarters.</span></span> 

<span data-ttu-id="b813d-108">Проверка проводок Commerce может оказаться неудачной по разным причинам.</span><span class="sxs-lookup"><span data-stu-id="b813d-108">Commerce transactions fail validation for various reasons.</span></span> <span data-ttu-id="b813d-109">Например, расхождение в данных может быть вызвано ошибкой в коде интеграции или в POS-приложении, а также ошибкой пользователя, например удалением продукта после его синхронизации с каналом или закрытием финансового периода без разноски проводок.</span><span class="sxs-lookup"><span data-stu-id="b813d-109">For example, a bug in the integration code or a bug in the POS application may cause inconsistent data, or a user error, such as deleting a product after it was synchronized to the channel or closing a fiscal period without posting transactions for that period, can cause inconsistent data.</span></span>

<span data-ttu-id="b813d-110">Хотя эти проводки помечаются и исключаются из журналов, они могут повлиять на повседневные операции разноски операций.</span><span class="sxs-lookup"><span data-stu-id="b813d-110">While these transactions get flagged and are excluded from the statements, the transactions can disrupt a customer’s daily process of posting daily sales to the financials.</span></span>

<span data-ttu-id="b813d-111">В Commerce можно редактировать отдельные проводки, которые не прошли проверку, и при этом сохранять историю всех изменений.</span><span class="sxs-lookup"><span data-stu-id="b813d-111">In Commerce, you can edit the specific transactions that fail validation while maintaining audit of all the changes.</span></span> 

## <a name="edit-and-audit-transactions"></a><span data-ttu-id="b813d-112">Редактирование и аудит проводок</span><span class="sxs-lookup"><span data-stu-id="b813d-112">Edit and audit transactions</span></span>

<span data-ttu-id="b813d-113">В Retail 10.0.5 можно редактировать только проводки с использованием наличных, такие как продажи и возвраты.</span><span class="sxs-lookup"><span data-stu-id="b813d-113">In Retail version 10.0.5, cash and carry transactions like sales and returns are the only transactions that can be edited.</span></span> <span data-ttu-id="b813d-114">Редактирование заказов клиентов и интернет-заказов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b813d-114">Editing customer orders or online orders is not supported.</span></span> <span data-ttu-id="b813d-115">В Retail 10.0.6 и более поздних версий также поддерживается редактирование проводок управления кассами.</span><span class="sxs-lookup"><span data-stu-id="b813d-115">In Retail version 10.0.6 and higher, editing cash management transactions is also supported.</span></span>

1. <span data-ttu-id="b813d-116">Установите надстройку Dynamics Excel.</span><span class="sxs-lookup"><span data-stu-id="b813d-116">Install the Dynamics Excel Add-in.</span></span>

2. <span data-ttu-id="b813d-117">Перейдите в рабочую область **Финансовая информация магазина**.</span><span class="sxs-lookup"><span data-stu-id="b813d-117">Go to the **Store financials** workspace.</span></span> <span data-ttu-id="b813d-118">Плитка **Ошибки проверки проводок** содержит предварительно отфильтрованное представление формы проводки, для которой не соблюдается одно или несколько правил проверки.</span><span class="sxs-lookup"><span data-stu-id="b813d-118">The **Transaction validation failures** tile provides a pre-filtered view of the transaction form that failed one or more of the validation rules.</span></span>
 
3. <span data-ttu-id="b813d-119">Откройте форму.</span><span class="sxs-lookup"><span data-stu-id="b813d-119">Open the form.</span></span> <span data-ttu-id="b813d-120">Щелкните запись, не прошедшую проверку, выберите **Надстройка Office**, а затем выберите **Изменить выбранную проводку**.</span><span class="sxs-lookup"><span data-stu-id="b813d-120">Click the record that failed validation, click **Office Add in**, and then click **Edit selected transaction**.</span></span> <span data-ttu-id="b813d-121">Откроется файл Excel с информацией о выбранной проводке. Он содержит следующие листы:</span><span class="sxs-lookup"><span data-stu-id="b813d-121">An Excel file with the details of the selected transaction opens, with the following worksheets:</span></span>

    - <span data-ttu-id="b813d-122">Строки: на этом листе имеются строки заголовка и продуктов, а также соответствующие данные по проводкам.</span><span class="sxs-lookup"><span data-stu-id="b813d-122">Lines: This worksheet has the header and product lines and related data for the transaction.</span></span>
    - <span data-ttu-id="b813d-123">Платежи: на этом листе содержатся подробные сведения о строках оплаты для проводки.</span><span class="sxs-lookup"><span data-stu-id="b813d-123">Payments: This worksheet has the details of the payment lines for the transaction.</span></span>
    - <span data-ttu-id="b813d-124">Скидки: на этом листе содержатся сведения о скидках по проводкам.</span><span class="sxs-lookup"><span data-stu-id="b813d-124">Discounts: This worksheet has the discount-related details for the transaction.</span></span>
    - <span data-ttu-id="b813d-125">Налоги: на этом листе содержатся сведения о налогах по проводкам.</span><span class="sxs-lookup"><span data-stu-id="b813d-125">Taxes: This worksheet has the tax-related details for the transaction.</span></span>
    - <span data-ttu-id="b813d-126">Расходы: на этом листе содержатся сведения о расходах по проводкам.</span><span class="sxs-lookup"><span data-stu-id="b813d-126">Charges: This worksheet has the charges-related data for the transaction.</span></span>

4. <span data-ttu-id="b813d-127">В файле Excel необходимо изменить соответствующие поля, а затем загрузить эти данные в Headquarters с помощью функции публикации в надстройке Dynamics Excel.</span><span class="sxs-lookup"><span data-stu-id="b813d-127">In the Excel file, you modify the appropriate fields and then upload the data back into Headquarters using the Dynamics Excel Add-in publish functionality.</span></span> <span data-ttu-id="b813d-128">После публикации изменения будут отражены в системе.</span><span class="sxs-lookup"><span data-stu-id="b813d-128">Once published, the changes will be reflected in the system.</span></span> <span data-ttu-id="b813d-129">Во время публикации вносимые пользователями изменения не проверяются.</span><span class="sxs-lookup"><span data-stu-id="b813d-129">During publish, no validation is done on changes that users make.</span></span>

5. <span data-ttu-id="b813d-130">Чтобы открыть полный аудиторский след, выберите **Просмотр данных аудиторского следа** под заголовком **Проводка розничной торговли** для изменений на уровне заголовка или в соответствующем разделе и записи на странице проводки.</span><span class="sxs-lookup"><span data-stu-id="b813d-130">A complete audit trail of the changes can be viewed by clicking **View audit trail** in the **Retail transaction** header for the header-level changes and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="b813d-131">Например, все изменения, относящиеся к строкам продажи, отображаются на странице **Проводки по продажам**, к платежам — на странице **Проводки по оплате** и т. д. Для аудита изменений сохраняются следующие данные:</span><span class="sxs-lookup"><span data-stu-id="b813d-131">For example, all changes relating to sales lines will be visible on the **Sales transactions** page, changes relating to payments will be visible on the **Payment transactions** page, etc. The audit details that are maintained for the changes are as follows.</span></span>

   - <span data-ttu-id="b813d-132">Дата и время изменения</span><span class="sxs-lookup"><span data-stu-id="b813d-132">Modified date and time</span></span>
   - <span data-ttu-id="b813d-133">Поле</span><span class="sxs-lookup"><span data-stu-id="b813d-133">Field</span></span> 
   - <span data-ttu-id="b813d-134">Старое значение</span><span class="sxs-lookup"><span data-stu-id="b813d-134">Old value</span></span>
   - <span data-ttu-id="b813d-135">Новое значение</span><span class="sxs-lookup"><span data-stu-id="b813d-135">New value</span></span>
   - <span data-ttu-id="b813d-136">Кто изменил</span><span class="sxs-lookup"><span data-stu-id="b813d-136">Modified by</span></span>

6. <span data-ttu-id="b813d-137">После внесения и публикации изменений снова выберите команду **Проверить проводки магазина**, чтобы убедиться в том, что изменения правильны и согласованы.</span><span class="sxs-lookup"><span data-stu-id="b813d-137">After your changes are made and published, run the **Validate store transactions** option again to validate that the changes you made are consistent and valid.</span></span>

> [!NOTE]
> <span data-ttu-id="b813d-138">Редактировать можно только проводки, не прошедшие проверку.</span><span class="sxs-lookup"><span data-stu-id="b813d-138">You can only edit transactions that failed validation.</span></span> <span data-ttu-id="b813d-139">Если необходимо изменить проводку, которая прошла проверку, измените статус проверки такой проводки на **Ошибка** или **Нет**, после чего она станет доступной для изменений.</span><span class="sxs-lookup"><span data-stu-id="b813d-139">If you want to edit transactions that passed validation, change the validation status of the transaction you want to change to **Error** or **None** and then you will be able to edit it.</span></span> 


## <a name="bulk-edit-transactions"></a><span data-ttu-id="b813d-140">Массовое изменение проводок</span><span class="sxs-lookup"><span data-stu-id="b813d-140">Bulk edit transactions</span></span>

<span data-ttu-id="b813d-141">В Retail 10.0.6 и более поздних версий поддерживается массовое изменения проводок на уровне журнала операций.</span><span class="sxs-lookup"><span data-stu-id="b813d-141">In Retail version 10.0.6 and higher, the option to bulk edit transactions at a statement level is supported.</span></span> 

1. <span data-ttu-id="b813d-142">Воспользуйтесь надстройкой Excel, чтобы открыть журнал операций с нужными проводками, как было описано в шагах 1–3 выше.</span><span class="sxs-lookup"><span data-stu-id="b813d-142">Use the Excel Add-in to open a statement that has transactions you want to modify using steps 1-3 above.</span></span>

2. <span data-ttu-id="b813d-143">Выберите один из перечисленных ниже параметров.</span><span class="sxs-lookup"><span data-stu-id="b813d-143">Choose one of the options below.</span></span>

    - <span data-ttu-id="b813d-144">**Изменить кассовые проводки**.</span><span class="sxs-lookup"><span data-stu-id="b813d-144">**Edit cash and carry transactions**.</span></span> <span data-ttu-id="b813d-145">Этот параметр позволяет редактировать все кассовые проводки в журнале операций</span><span class="sxs-lookup"><span data-stu-id="b813d-145">This option enables you to edit all the cash and carry transactions included in the statement.</span></span> <span data-ttu-id="b813d-146">Доступны следующие листы Excel.</span><span class="sxs-lookup"><span data-stu-id="b813d-146">The following Excel worksheets are available.</span></span>
    
       - <span data-ttu-id="b813d-147">**Проводка**: на этом листе приведена вся информация уровня заголовков по всем проводкам продаж.</span><span class="sxs-lookup"><span data-stu-id="b813d-147">**Transaction**: This worksheet has all the header-level information for the sales transactions.</span></span>
       - <span data-ttu-id="b813d-148">**Проводка продаж**: на этом листе приведена вся информация уровня строк по всем проводкам продаж.</span><span class="sxs-lookup"><span data-stu-id="b813d-148">**Sales transaction**: This worksheet has all the lines-level information for the sales transactions.</span></span>
       - <span data-ttu-id="b813d-149">**Проводки по оплате**: на этом листе приведена вся информация строк оплаты по всем проводкам продаж.</span><span class="sxs-lookup"><span data-stu-id="b813d-149">**Payment transactions**: This worksheet has all the payment lines information for the sales transactions.</span></span>
       - <span data-ttu-id="b813d-150">**Проводки по скидкам**: на этом листе приведена вся информация строк скидок по всем проводкам продаж.</span><span class="sxs-lookup"><span data-stu-id="b813d-150">**Discount transactions**: This worksheet has all the discount lines information for the sales transactions.</span></span>
       - <span data-ttu-id="b813d-151">**Налоговые проводки**: на этом листе приведена вся информация строк налогов по всем проводкам продаж.</span><span class="sxs-lookup"><span data-stu-id="b813d-151">**Tax transactions**: This worksheet has all the tax lines information for the sales transactions.</span></span>
       - <span data-ttu-id="b813d-152">**Проводки расходов**: на этом листе приведена вся информация строк расходов по всем проводкам продаж.</span><span class="sxs-lookup"><span data-stu-id="b813d-152">**Charge transactions**: This worksheet has all the charge lines information for the sales transactions.</span></span>

    - <span data-ttu-id="b813d-153">**Изменить проводки управления кассой**.</span><span class="sxs-lookup"><span data-stu-id="b813d-153">**Edit cash management transactions**.</span></span> <span data-ttu-id="b813d-154">Этот параметр позволяет редактировать все проводки управления кассой в журнале операций</span><span class="sxs-lookup"><span data-stu-id="b813d-154">This option enables you to edit all the cash management transactions included in the statement.</span></span> <span data-ttu-id="b813d-155">Доступны следующие листы Excel.</span><span class="sxs-lookup"><span data-stu-id="b813d-155">The following Excel worksheets are available.</span></span>
     
       - <span data-ttu-id="b813d-156">**Проводка**: на этом листе приведена вся информация уровня заголовков по всем проводкам управления кассой.</span><span class="sxs-lookup"><span data-stu-id="b813d-156">**Transaction**: This worksheet has all the header-level information for the cash management transactions.</span></span>
       - <span data-ttu-id="b813d-157">**Проводки по платежному средству для внесения в банк**: на этом листе приведена вся информация по проводкам внесения средств в банк.</span><span class="sxs-lookup"><span data-stu-id="b813d-157">**Bank tender transactions**: This worksheet has all the bank drop transaction details.</span></span>
       - <span data-ttu-id="b813d-158">**Проводки по платежному средству для внесения в сейф**: на этом листе приведена вся информация по проводкам внесения средств в сейф.</span><span class="sxs-lookup"><span data-stu-id="b813d-158">**Safe tender transactions**: This worksheet has all the safe drop transaction details.</span></span>
       - <span data-ttu-id="b813d-159">**Декларирование платежных средств**: на этом листе приведена вся информация по проводкам декларирования платежных средств.</span><span class="sxs-lookup"><span data-stu-id="b813d-159">**Tender declaration**: This worksheet has all the tender declaration transaction details.</span></span>
       - <span data-ttu-id="b813d-160">**Проводки по доходам/расходам**: на этом листе приведена вся информация по строкам проводок по доходам и расходам.</span><span class="sxs-lookup"><span data-stu-id="b813d-160">**Income-expense transaction**: This worksheet has all the income-expense transaction line details.</span></span>
       - <span data-ttu-id="b813d-161">**Проводки по оплате**: на этом листе приведена вся информация по платежам для операции **Оплата накладной**, а также по проводкам по доходам и расходам.</span><span class="sxs-lookup"><span data-stu-id="b813d-161">**Payment transactions**: This worksheet has all the payment-related information for the **Pay invoice** operation as well as the income-expense transaction.</span></span>

3.  <span data-ttu-id="b813d-162">При публикации массовых изменений проводок проверка не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b813d-162">Validations are not performed when you publish bulk edited transactions.</span></span> <span data-ttu-id="b813d-163">Вы должны самостоятельно следить точностью изменений и согласованностью данных на всех листах.</span><span class="sxs-lookup"><span data-stu-id="b813d-163">You must ensure that all your edits are accurate and the fidelity of data across the worksheets is maintained.</span></span> <span data-ttu-id="b813d-164">Например, если вам нужно изменить дату проводки в ситуации, когда финансовый или учетный период для открытой проводки был закрыт, необходимо изменить эту дату на всех листах Excel, на которых есть столбец **Бизнес-дата**.</span><span class="sxs-lookup"><span data-stu-id="b813d-164">For example, if you want to change the transaction date to manage the scenarios where the fiscal or inventory period for the open transactions is closed, you need to change the date on all the Excel worksheets that have the **Business date** column.</span></span> <span data-ttu-id="b813d-165">Чтобы проверить проводки после их изменения воспользуйтесь командой **Заново проверить проводки** на странице **Журналы операций**.</span><span class="sxs-lookup"><span data-stu-id="b813d-165">To validate transactions after they have been edited, you can use **Revalidate transactions** on the **Statements** page.</span></span>
