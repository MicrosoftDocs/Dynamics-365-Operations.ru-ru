---
title: Интеграция примечания
description: Эта тема описывает интеграцию данных примечания в двойной записи.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: ceb5b7c90cc7efa0049d0278e2c245228e5b52bd
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186794"
---
# <a name="note-integration"></a><span data-ttu-id="a7022-103">Интеграция примечания</span><span class="sxs-lookup"><span data-stu-id="a7022-103">Note integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a7022-104">В процессе бизнес-процессов пользователи Microsoft Dynamics 365 часто собирают информацию о своих клиентах.</span><span class="sxs-lookup"><span data-stu-id="a7022-104">During business processes, Microsoft Dynamics 365 users often gather information about their customers.</span></span> <span data-ttu-id="a7022-105">Эти сведения записываются в виде мероприятий и примечаний.</span><span class="sxs-lookup"><span data-stu-id="a7022-105">This information is recorded as activities and notes.</span></span> <span data-ttu-id="a7022-106">Эта тема описывает интеграцию данных примечания в двойной записи.</span><span class="sxs-lookup"><span data-stu-id="a7022-106">This topic describes the integration of note data in dual-write.</span></span>

<span data-ttu-id="a7022-107">Информацию по клиенту можно классифицировать следующими способами:</span><span class="sxs-lookup"><span data-stu-id="a7022-107">Customer information can be classified in the following ways:</span></span>

+ <span data-ttu-id="a7022-108">**Обрабатываемая информация, обрабатываемая пользователем Dynamics 365 от имени клиента** — например, Contoso (пользователь Dynamics 365), осуществляет проведение игры.</span><span class="sxs-lookup"><span data-stu-id="a7022-108">**Actionable information that a Dynamics 365 user handles on behalf of a customer** – For example, Contoso (a Dynamics 365 user) is conducting a game show.</span></span> <span data-ttu-id="a7022-109">Один из клиентов Contoso (клиент) хочет посетить игру.</span><span class="sxs-lookup"><span data-stu-id="a7022-109">One of Contoso's customers (a customer) wants to attend the game show.</span></span> <span data-ttu-id="a7022-110">Заказчик просит сотрудника Contoso зарезервировать для него место в игре.</span><span class="sxs-lookup"><span data-stu-id="a7022-110">The customer asks a Contoso employee to book a slot in the game show for them.</span></span> <span data-ttu-id="a7022-111">Резервирование выполняется в календаре участника события Contoso.</span><span class="sxs-lookup"><span data-stu-id="a7022-111">The booking occurs in Contoso's event attendee's calendar.</span></span>
+ <span data-ttu-id="a7022-112">**Обрабатываемая информация для пользователя Dynamics 365** — например, клиент, который покупает единицу Surface, вводит специальные инструкции, указывающие на то, что перед доставкой устройство должно быть упаковано.</span><span class="sxs-lookup"><span data-stu-id="a7022-112">**Actionable information for a Dynamics 365 user** – For example, a customer who is purchasing a Surface unit enters special instructions that indicate that the device should be gift wrapped before delivery.</span></span> <span data-ttu-id="a7022-113">Эти инструкции представляют собой информацию, которая должна обрабатываться сотрудником компании Contoso, ответственным за упаковку.</span><span class="sxs-lookup"><span data-stu-id="a7022-113">These instructions are actionable information that should be handled by the Contoso employee who is responsible for packaging.</span></span>
+ <span data-ttu-id="a7022-114">**Необрабатываемая информация** — например, клиент посещает магазин Contoso и, в ходе общения с сотрудником магазина, выражает интерес в играх и игровых аксессуарах *Halo*.</span><span class="sxs-lookup"><span data-stu-id="a7022-114">**Non-actionable information** – For example, a customer visits the Contoso store and, during their conversation with a store associate, expresses interest in *Halo* games and gaming accessories.</span></span> <span data-ttu-id="a7022-115">Сотрудник магазина записывает эту информацию.</span><span class="sxs-lookup"><span data-stu-id="a7022-115">The store associate makes a note of this information.</span></span> <span data-ttu-id="a7022-116">Затем ядро рекомендаций продукта использует его для создания рекомендаций для клиента.</span><span class="sxs-lookup"><span data-stu-id="a7022-116">The product recommendations engine then uses it to make recommendations to the customer.</span></span>

<span data-ttu-id="a7022-117">В общем случае сведения о действии фиксируются в качестве *действий* в приложениях Finance and Operations и приложениях взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="a7022-117">In general, actionable information is captured as *activities* in Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="a7022-118">Необрабатываемая информация фиксируется в качестве *примечаний* в приложениях Finance and Operations и в качестве *заметок* в приложениях взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="a7022-118">Non-actionable information is captured as *notes* in Finance and Operations apps, and as *annotations* in customer engagement apps.</span></span>

> [!TIP]
> <span data-ttu-id="a7022-119">Хотя примечания предназначены для необрабатываемой информации, приложения не смогут использовать их для хранения и обработки обрабатываемой информации, если их необходимо использовать таким образом.</span><span class="sxs-lookup"><span data-stu-id="a7022-119">Although notes are intended for non-actionable information, the apps won't prevent you from using them to store and handle actionable information if you want to use them in that way.</span></span>

<span data-ttu-id="a7022-120">В настоящее время Microsoft выпускает функциональность для интеграции примечаний.</span><span class="sxs-lookup"><span data-stu-id="a7022-120">Microsoft is currently releasing functionality for note integration.</span></span> <span data-ttu-id="a7022-121">(Функциональность для интеграции мероприятий будет выпущена позже). Интеграция примечаний доступна для клиентов, поставщиков, заказов на продажу и заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="a7022-121">(Functionality for activity integration will be released later.) Note integration is available for customers, vendors, sales orders, and purchase orders.</span></span>

## <a name="create-a-note-in-a-customer-engagement-app"></a><span data-ttu-id="a7022-122">Создание примечания в приложении взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="a7022-122">Create a note in a customer engagement app</span></span>

<span data-ttu-id="a7022-123">Чтобы создать примечание в приложении взаимодействия с клиентами, а затем синхронизировать его с приложением Finance and Operations, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a7022-123">To create a note in a customer engagement app and then sync it to a Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="a7022-124">В приложении взаимодействия с клиентам откройте запись учетной записи для клиента.</span><span class="sxs-lookup"><span data-stu-id="a7022-124">In the customer engagement app, open the account record for a customer.</span></span>
2. <span data-ttu-id="a7022-125">В панели **временная шкала** выберите знак "плюс" (**+**), а затем выберите **Примечание**, чтобы создать примечание.</span><span class="sxs-lookup"><span data-stu-id="a7022-125">In the **Timeline** pane, select the plus sign (**+**), and then select **Note** to create a note.</span></span>

    ![Создание примечания в приложении взаимодействия с клиентами](media/notes-ce-1.png)

3. <span data-ttu-id="a7022-127">Введите заголовок и описание, а затем выберите **Добавить примечание**.</span><span class="sxs-lookup"><span data-stu-id="a7022-127">Enter a title and description, and then select **Add note**.</span></span>

    ![Введите заголовок и описание](media/notes-ce-2.png)

    <span data-ttu-id="a7022-129">Новое примечание добавляется к временной шкале клиента.</span><span class="sxs-lookup"><span data-stu-id="a7022-129">The new note is added to the customer timeline.</span></span>

    ![Новое примечание на временной шкале клиента](media/notes-ce-3.png)

4. <span data-ttu-id="a7022-131">Выполните вход в приложение Finance and Operations и откройте ту же запись клиента.</span><span class="sxs-lookup"><span data-stu-id="a7022-131">Sign in to the Finance and Operations app, and open the same customer record.</span></span> <span data-ttu-id="a7022-132">Обратите внимание, что кнопка **вложения** (символ скрепки) в верхнем правом углу показывает, что запись имеет вложение.</span><span class="sxs-lookup"><span data-stu-id="a7022-132">Notice that the **Attachments** button (paperclip symbol) in the upper-right corner indicates that the record has an attachment.</span></span>

    ![Уведомление о вложении](media/notes-ce-4.png)

5. <span data-ttu-id="a7022-134">Нажмите кнопку **Вложения**, чтобы открыть страницу **Вложения**.</span><span class="sxs-lookup"><span data-stu-id="a7022-134">Select the **Attachments** button to open the **Attachments** page.</span></span> <span data-ttu-id="a7022-135">Следует найти примечание, созданное в приложении взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="a7022-135">You should find the note that you created in the customer engagement app.</span></span>

    ![Примечание из приложения взаимодействия с клиентами](media/notes-ce-5.png)

<span data-ttu-id="a7022-137">Любые обновления примечания синхронизируются вперед и назад между приложением Finance and Operations и приложением взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="a7022-137">Any updates to the note are synced back and forth between the Finance and Operations app and the customer engagement app.</span></span>

## <a name="create-a-note-in-a-finance-and-operations-app"></a><span data-ttu-id="a7022-138">Создание примечания в приложении Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a7022-138">Create a note in a Finance and Operations app</span></span>

<span data-ttu-id="a7022-139">Можно также создать примечание в приложении Finance and Operations, и оно будет синхронизировано с приложением взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="a7022-139">You can also create a note in a Finance and Operations app, and it will be synced to a customer engagement app.</span></span>

<span data-ttu-id="a7022-140">Чтобы создать примечание в приложении Finance and Operations, а затем синхронизировать его с приложением взаимодействия с клиентами, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a7022-140">To create a note in a Finance and Operations app and then sync it to a customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="a7022-141">В приложении Finance and Operations на странице **вложения** выберите **создать** \> **Примечание**.</span><span class="sxs-lookup"><span data-stu-id="a7022-141">In the Finance and Operations app, on the **Attachments** page, select **New** \> **Note**.</span></span>

    ![Создание примечания в приложении Finance and Operations](media/notes-fo-1.png)

2. <span data-ttu-id="a7022-143">Введите заголовок и краткий набор инструкций, а затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a7022-143">Enter a title and a brief set of instructions, and then select **Save**.</span></span>

    ![Введите заголовок и инструкции](media/notes-fo-2.png)

3. <span data-ttu-id="a7022-145">В приложении взаимодействия с клиентами обновите запись.</span><span class="sxs-lookup"><span data-stu-id="a7022-145">In the customer engagement app, update the record.</span></span> <span data-ttu-id="a7022-146">Новое примечание на временной шкале должно быть обнаружено.</span><span class="sxs-lookup"><span data-stu-id="a7022-146">You should find the new note on the timeline.</span></span>

    ![Новое примечание на временной шкале в приложении взаимодействия с клиентами](media/notes-fo-3.png)

<span data-ttu-id="a7022-148">Можно классифицировать примечание как внутреннее или внешнее.</span><span class="sxs-lookup"><span data-stu-id="a7022-148">You can classify a note as either internal or external.</span></span>

- <span data-ttu-id="a7022-149">В приложении Finance and Operations, на странице **вложения**, откройте примечание, а затем в поле **ограничение** выберите **внутренние** или **Внешние**.</span><span class="sxs-lookup"><span data-stu-id="a7022-149">In the Finance and Operations app, on the **Attachments** page, open the note, and then, in the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Поле ограничение](media/notes-fo-4.png)

<span data-ttu-id="a7022-151">Можно также создать URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="a7022-151">You can also create a URL.</span></span>

1. <span data-ttu-id="a7022-152">В приложении Finance and Operations на странице **вложения** выберите **создать** \> **URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="a7022-152">In the Finance and Operations app, on the **Attachments** page, select **New** \> **URL**.</span></span>
2. <span data-ttu-id="a7022-153">Введите заголовок и URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="a7022-153">Enter a title and the URL.</span></span>
3. <span data-ttu-id="a7022-154">В поле **ограничение** выберите **внутренние** или **Внешние**.</span><span class="sxs-lookup"><span data-stu-id="a7022-154">In the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Создание URL-адреса в приложении Finance and Operations](media/notes-fo-5.png)

4. <span data-ttu-id="a7022-156">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a7022-156">Select **Save**.</span></span>

    <span data-ttu-id="a7022-157">Так как у приложений для взаимодействия с клиентами нет типа URL-адреса, этот URL-адрес интегрируется с двойной записью в качестве примечания.</span><span class="sxs-lookup"><span data-stu-id="a7022-157">Because customer engagement apps don't have a URL type, the URL is integrated with dual-write as a note.</span></span>

    ![URL-адрес появляется в качестве примечания в приложении взаимодействия с клиентами](media/notes-ce-6.png)

> [!NOTE]
> <span data-ttu-id="a7022-159">Файловые вложения не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="a7022-159">File attachments aren't supported.</span></span>

## <a name="templates"></a><span data-ttu-id="a7022-160">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="a7022-160">Templates</span></span>

<span data-ttu-id="a7022-161">Интеграция примечания включает коллекцию сопоставлений таблиц, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a7022-161">Note integration includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="a7022-162">Приложение Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a7022-162">Finance and Operations app</span></span> | <span data-ttu-id="a7022-163">Приложение для взаимодействия с клиентами</span><span class="sxs-lookup"><span data-stu-id="a7022-163">Customer engagement app</span></span> | <span data-ttu-id="a7022-164">описание</span><span class="sxs-lookup"><span data-stu-id="a7022-164">Description</span></span> |
|----------------------------|-------------------------|-------------|
| [<span data-ttu-id="a7022-165">Вложения клиента</span><span class="sxs-lookup"><span data-stu-id="a7022-165">Customer Attachments</span></span>](mapping-reference.md#230) | <span data-ttu-id="a7022-166">Заметки</span><span class="sxs-lookup"><span data-stu-id="a7022-166">Annotations</span></span> | <span data-ttu-id="a7022-167">Компании, использующие обычный текст и URL-адреса для сбора информации, относящейся к клиенту (для компаний и лиц).</span><span class="sxs-lookup"><span data-stu-id="a7022-167">Businesses that use plain text and URLs to capture customer-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="a7022-168">Вложения документов поставщика</span><span class="sxs-lookup"><span data-stu-id="a7022-168">Vendor document attachments</span></span>](mapping-reference.md#231) | <span data-ttu-id="a7022-169">Заметки</span><span class="sxs-lookup"><span data-stu-id="a7022-169">Annotations</span></span> | <span data-ttu-id="a7022-170">Компании, использующие обычный текст и URL-адреса для сбора информации, относящейся к поставщику (для компаний и лиц).</span><span class="sxs-lookup"><span data-stu-id="a7022-170">Businesses that use plain text and URLs to capture vendor-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="a7022-171">Вложения документа заголовка заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="a7022-171">Sales order header document attachments</span></span>](mapping-reference.md#229) | <span data-ttu-id="a7022-172">Заметки</span><span class="sxs-lookup"><span data-stu-id="a7022-172">Annotations</span></span> | <span data-ttu-id="a7022-173">Компании, которые используют обычный текст и URL-адреса для сбора информации, относящейся к заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="a7022-173">Businesses that use plain text and URLs to capture sales order–specific information.</span></span> |
| [<span data-ttu-id="a7022-174">Вложения документа заголовка заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="a7022-174">Purchase order header document attachments</span></span>](mapping-reference.md#232) | <span data-ttu-id="a7022-175">Заметки</span><span class="sxs-lookup"><span data-stu-id="a7022-175">Annotations</span></span> | <span data-ttu-id="a7022-176">Компании, которые используют обычный текст и URL-адреса для сбора информации, относящейся к заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="a7022-176">Businesses that use plain text and URLs to capture purchase order–specific information.</span></span> |

## <a name="limitations"></a><span data-ttu-id="a7022-177">Ограничения</span><span class="sxs-lookup"><span data-stu-id="a7022-177">Limitations</span></span>

<span data-ttu-id="a7022-178">После установки решения примечаний оно не может быть удалено.</span><span class="sxs-lookup"><span data-stu-id="a7022-178">Once you install the notes solution, you cannot uninstall it.</span></span> 

<span data-ttu-id="a7022-179">Дополнительные сведения см. в разделе [Ссылка сопоставления с двойной записью](mapping-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a7022-179">For more information, see [Dual-write mapping reference](mapping-reference.md).</span></span>
