---
title: Настройка и использование клиентского портала
description: В этой теме объясняется, как настроить клиентский портал после его добавления в систему.
author: dasani-madipalli
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6d4cc52a90b25406080032c7a98caa59f53ce188
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909008"
---
# <a name="customize-and-use-the-customer-portal"></a><span data-ttu-id="6d937-103">Настройка и использование клиентского портала</span><span class="sxs-lookup"><span data-stu-id="6d937-103">Customize and use the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6d937-104">В этом разделе описываются отдельные страницы, доступные на готовом клиентском портале.</span><span class="sxs-lookup"><span data-stu-id="6d937-104">This topic describes the different pages that available in the Customer portal out of the box.</span></span> <span data-ttu-id="6d937-105">Даны объяснения, что представляют собой страницы и как их можно настраивать.</span><span class="sxs-lookup"><span data-stu-id="6d937-105">It explains what the pages do and how you can customize them.</span></span>

<span data-ttu-id="6d937-106">Клиентский портал содержит несколько готовых веб-страниц и действий.</span><span class="sxs-lookup"><span data-stu-id="6d937-106">The Customer portal offers a few webpages and actions out of the box.</span></span> <span data-ttu-id="6d937-107">На следующей карте сайта дан обзор таких веб-страниц и действий, а также ролей, которые могут выполнять эти действия.</span><span class="sxs-lookup"><span data-stu-id="6d937-107">The following site map provides an overview of those webpages and actions, and the roles that can perform the actions.</span></span>

<span data-ttu-id="6d937-108">![Карта сайта клиентского портала](media/customer-portal-site-map.png "Карта сайта клиентского портала")</span><span class="sxs-lookup"><span data-stu-id="6d937-108">![Customer portal site map](media/customer-portal-site-map.png "Customer portal site map")</span></span>

## <a name="typical-customizations"></a><span data-ttu-id="6d937-109">Типичные настройки</span><span class="sxs-lookup"><span data-stu-id="6d937-109">Typical customizations</span></span>

<span data-ttu-id="6d937-110">Следующие темы содержат общие сведения о порталах Power Apps и способах настройки порталов:</span><span class="sxs-lookup"><span data-stu-id="6d937-110">The following topics will help you learn the basics about Power Apps portals and how you can customize portals:</span></span>

- <span data-ttu-id="6d937-111">[Работа с шаблонами](/powerapps/maker/portals/work-with-templates) — в этой теме представлен общий обзор принципа работы порталов Power Apps и способов выполнения простых настроек порталов.</span><span class="sxs-lookup"><span data-stu-id="6d937-111">[Work with templates](/powerapps/maker/portals/work-with-templates) – This topic provides a general overview of how Power Apps portals works and how you can do simple customizations of portals.</span></span>
- <span data-ttu-id="6d937-112">[Управление содержимым портала](/dynamics365/portals/manage-portal-content) — в этой теме объясняется, как управлять и настраивать содержимое портала.</span><span class="sxs-lookup"><span data-stu-id="6d937-112">[Manage portal content](/dynamics365/portals/manage-portal-content) – This topic explains how you can manage and customize the content that you surface in your portal.</span></span>
- <span data-ttu-id="6d937-113">[Правка CSS](/powerapps/maker/portals/edit-css) — в этой теме указано, как выполнить более сложную настройку пользовательского интерфейса (UI) портала.</span><span class="sxs-lookup"><span data-stu-id="6d937-113">[Edit CSS](/powerapps/maker/portals/edit-css) – This topic helps you make more complex customizations to the user interface (UI) of your portal.</span></span>
- <span data-ttu-id="6d937-114">[Создать тему для своего портала](/dynamics365/portals/create-theme) — эта тема поможет создать тему пользовательского интерфейса для своего портала.</span><span class="sxs-lookup"><span data-stu-id="6d937-114">[Create a theme for your portal](/dynamics365/portals/create-theme) – This topic helps you create a UI theme for your portal.</span></span>
- <span data-ttu-id="6d937-115">[Простое создание и представление содержимого портала](/dynamics365/portals/create-expose-portal-content) — эта тема поможет управлять основными данными и таблицами, используемыми для портала.</span><span class="sxs-lookup"><span data-stu-id="6d937-115">[Create and expose portal content easily](/dynamics365/portals/create-expose-portal-content) – This topic helps you manage the underlying data and tables that you use for your portal.</span></span>
- <span data-ttu-id="6d937-116">[Настройка контакта для использования на портале](/powerapps/maker/portals/configure/configure-contacts) — в этой теме объясняется, как создавать и настраивать роли пользователей и как работают безопасность и аутентификация на порталах Power Apps.</span><span class="sxs-lookup"><span data-stu-id="6d937-116">[Configure a contact for use on a portal](/powerapps/maker/portals/configure/configure-contacts) – This topic explains how to create and customize user roles, and how security and authentication work in Power Apps portals.</span></span>
- <span data-ttu-id="6d937-117">[Настройка примечаний для форм таблиц и веб-форм на порталах](/powerapps/maker/portals/configure-notes) — в этой теме объясняется, как добавлять документы и дополнительные хранилища на свой портал.</span><span class="sxs-lookup"><span data-stu-id="6d937-117">[Configure notes for table forms and web forms on portals](/powerapps/maker/portals/configure-notes) – This topic explains how to add documents and additional storage to your portal.</span></span>
- <span data-ttu-id="6d937-118">[Обработка ошибок для веб-сайта портала](/powerapps/maker/portals/admin/view-portal-error-log) — в этой теме объясняется, как просмотреть журналы ошибок портала и сохранить их в учетной записи хранилища BLOB-объектов Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6d937-118">[Error handling for portal website](/powerapps/maker/portals/admin/view-portal-error-log) – This topic explains how to view portal error logs and store them in your Microsoft Azure Blob storage account.</span></span>

## <a name="customize-the-order-creation-process"></a><span data-ttu-id="6d937-119">Настройка процесса создания заказов</span><span class="sxs-lookup"><span data-stu-id="6d937-119">Customize the order creation process</span></span>

<span data-ttu-id="6d937-120">Когда пользователь отправляет заказ с помощью клиентского портала, заказ автоматически синхронизируется с соответствующей средой Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6d937-120">When a user submits an order by using the Customer portal, the order is automatically synced to the corresponding Dynamics 365 Supply Chain Management environment.</span></span> <span data-ttu-id="6d937-121">Так как пользователь является внешним клиентом, некоторые требуемые сведения преднамеренно скрыты от него.</span><span class="sxs-lookup"><span data-stu-id="6d937-121">Because the user is an external customer, some required information is intentionally hidden from him or her.</span></span> <span data-ttu-id="6d937-122">Эти сведения будут автоматически заполнены при отправке формы.</span><span class="sxs-lookup"><span data-stu-id="6d937-122">This information will automatically be filled in when the form is submitted.</span></span>

<span data-ttu-id="6d937-123">В этом разделе показано, как настроить контакты, чтобы избежать ошибок.</span><span class="sxs-lookup"><span data-stu-id="6d937-123">This section shows how you should set up contacts to avoid errors.</span></span> <span data-ttu-id="6d937-124">В нем объясняются автоматически задаваемые поля и способ изменения значений этих полей, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="6d937-124">It explains fields that are automatically set and how you can modify the value of those fields if you must.</span></span>

### <a name="the-out-of-box-order-creation-process"></a><span data-ttu-id="6d937-125">Готовый процесс создания заказов</span><span class="sxs-lookup"><span data-stu-id="6d937-125">The out-of-box order creation process</span></span>

<span data-ttu-id="6d937-126">Ниже приведены стандартные шаги для отправки заказа с клиентского портала.</span><span class="sxs-lookup"><span data-stu-id="6d937-126">Here are the standard steps for submitting an order from the Customer portal.</span></span>

1. <span data-ttu-id="6d937-127">На домашней странице выберите плитку **Создать заказ**, чтобы открыть мастер **Создать заказ**.</span><span class="sxs-lookup"><span data-stu-id="6d937-127">On the home page, select the **Create order** tile to open the **Create Order** wizard.</span></span>
1. <span data-ttu-id="6d937-128">На странице **Информация о заказе** задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="6d937-128">On the **Order Information** page, set the following fields:</span></span>

    - <span data-ttu-id="6d937-129">**Запрошенная дата поступления** — укажите дату поставки.</span><span class="sxs-lookup"><span data-stu-id="6d937-129">**Requested receipt date** – Specify the date of delivery.</span></span>
    - <span data-ttu-id="6d937-130">**Адрес поставки** — введите адрес, по которому должен быть поставлен заказ.</span><span class="sxs-lookup"><span data-stu-id="6d937-130">**Delivery address** – Enter the address that the order should be delivered to.</span></span>
    - <span data-ttu-id="6d937-131">**Компания** — выберите название компании клиента.</span><span class="sxs-lookup"><span data-stu-id="6d937-131">**Company** – Select the name of the customer company.</span></span> <span data-ttu-id="6d937-132">Это поле автоматически задается для пользователей, не являющихся администраторами.</span><span class="sxs-lookup"><span data-stu-id="6d937-132">This field is automatically set for non-admin users.</span></span>
    - <span data-ttu-id="6d937-133">**Номер заявки** — введите номер заявки для заказа.</span><span class="sxs-lookup"><span data-stu-id="6d937-133">**Requisition number** – Enter the requisition number of the order.</span></span> <span data-ttu-id="6d937-134">Это поле необязательно для заполнения.</span><span class="sxs-lookup"><span data-stu-id="6d937-134">This field isn't required.</span></span>
    - <span data-ttu-id="6d937-135">**Поставка в страну/регион** — введите страну или регион, в которые будут поставлены номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="6d937-135">**Ship to country/region** – Enter the country or region that the items will be delivered to.</span></span> <span data-ttu-id="6d937-136">Это поле автоматически задается для пользователей, не являющихся администраторами.</span><span class="sxs-lookup"><span data-stu-id="6d937-136">This field is automatically set for non-admin users.</span></span>

    <span data-ttu-id="6d937-137">![Страница информации о заказе](media/customer-portal-order-information.png "Страница информации о заказе")</span><span class="sxs-lookup"><span data-stu-id="6d937-137">![Order Information page](media/customer-portal-order-information.png "Order Information page")</span></span>

1. <span data-ttu-id="6d937-138">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="6d937-138">Select **Next**.</span></span>
1. <span data-ttu-id="6d937-139">На странице **Номенклатуры** выберите **Добавить номенклатуру**.</span><span class="sxs-lookup"><span data-stu-id="6d937-139">On the **Items** page, select **Add Item**.</span></span>

    <span data-ttu-id="6d937-140">![Страница номенклатур](media/customer-portal-items.png "Страница номенклатур")</span><span class="sxs-lookup"><span data-stu-id="6d937-140">![Items page](media/customer-portal-items.png "Items page")</span></span>

1. <span data-ttu-id="6d937-141">В диалоговом окне **Сведения о номенклатуре** задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="6d937-141">In the **Item Information** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="6d937-142">**Название продукта** — найдите и выберите продукт, который требуется добавить в заказ.</span><span class="sxs-lookup"><span data-stu-id="6d937-142">**Product Name** – Find and select a product to add to the order.</span></span>
    - <span data-ttu-id="6d937-143">**Количество** — введите количество выбранного продукта.</span><span class="sxs-lookup"><span data-stu-id="6d937-143">**Quantity** – Enter the quantity of the selected product.</span></span>
    - <span data-ttu-id="6d937-144">**Единица измерения** — укажите единицу измерения (например, **шт.**, **кг** или **коробка**).</span><span class="sxs-lookup"><span data-stu-id="6d937-144">**Unit** – Specify the unit of measure (for example, **ea.**, **kgs**, or **box**).</span></span>
    - <span data-ttu-id="6d937-145">**Расчетная чистая сумма** — значение рассчитывается как расчетная цена номенклатуры × количество выбранной единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="6d937-145">**Estimated net amount** – The value is calculated as the estimated price of the item × the quantity for the selected unit.</span></span>

    <span data-ttu-id="6d937-146">![Диалоговое окно информации о номенклатуре](media/customer-portal-item-information.png "Диалоговое окно информации о номенклатуре")</span><span class="sxs-lookup"><span data-stu-id="6d937-146">![Item Information dialog box](media/customer-portal-item-information.png "Item Information dialog box")</span></span>

1. <span data-ttu-id="6d937-147">Выберите **Отправить**, чтобы добавить номенклатуру в заказ.</span><span class="sxs-lookup"><span data-stu-id="6d937-147">Select **Submit** to add the item to the order.</span></span>
1. <span data-ttu-id="6d937-148">Повторяйте шаги с 4 по 6 до тех пор, пока не будут добавлены все номенклатуры, которые требуется заказать.</span><span class="sxs-lookup"><span data-stu-id="6d937-148">Repeat steps 4 through 6 until you've added all the items that you want to order.</span></span>
1. <span data-ttu-id="6d937-149">После завершения добавления номенклатур нажмите **Далее** на странице **Номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="6d937-149">When you've finished adding items, select **Next** on the **Items** page.</span></span>
1. <span data-ttu-id="6d937-150">На странице **Информация о заказе** дана сводка по заказу.</span><span class="sxs-lookup"><span data-stu-id="6d937-150">The **Order Information** page provides a summary of the order.</span></span> <span data-ttu-id="6d937-151">Изучите содержимое заказа и сведения о поставке.</span><span class="sxs-lookup"><span data-stu-id="6d937-151">Review the order contents and delivery details.</span></span> <span data-ttu-id="6d937-152">Если все выглядит правильно, нажмите **Отправить**, чтобы отправить заказ.</span><span class="sxs-lookup"><span data-stu-id="6d937-152">If everything looks correct, select **Submit** to submit the order.</span></span>

    <span data-ttu-id="6d937-153">![Страница информации о заказе](media/customer-portal-order-submit.png "Страница информации о заказе")</span><span class="sxs-lookup"><span data-stu-id="6d937-153">![Order Information page](media/customer-portal-order-submit.png "Order Information page")</span></span>

### <a name="standard-data-setup"></a><span data-ttu-id="6d937-154">Настройка стандартных данных</span><span class="sxs-lookup"><span data-stu-id="6d937-154">Standard data setup</span></span>

<span data-ttu-id="6d937-155">Чтобы обеспечить удобное взаимодействие с пользователем, клиентский портал автоматически заполняет значения для нескольких обязательных полей.</span><span class="sxs-lookup"><span data-stu-id="6d937-155">To help ensure a smooth user experience, the Customer portal automatically fills in values for several required fields.</span></span> <span data-ttu-id="6d937-156">Эти значения основаны на информации в записи контакта клиента, отправляющего заказ.</span><span class="sxs-lookup"><span data-stu-id="6d937-156">These values are based on information in the contact record of the customer who is submitting the order.</span></span>

<span data-ttu-id="6d937-157">Для каждой [строки контакта](/powerapps/maker/portals/configure/configure-contacts), принадлежащей клиенту, который будет использовать клиентский портал для отправки заказов, необходимо указать значения для следующих обязательных полей.</span><span class="sxs-lookup"><span data-stu-id="6d937-157">For each [contact row](/powerapps/maker/portals/configure/configure-contacts) that belongs to a customer who will use the Customer portal to submit orders, values must be specified for the following required fields.</span></span> <span data-ttu-id="6d937-158">В противном случае произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="6d937-158">Otherwise, errors will occur.</span></span>

- <span data-ttu-id="6d937-159">**Компания** — юридическое лицо, к которому относится заказ</span><span class="sxs-lookup"><span data-stu-id="6d937-159">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="6d937-160">**Потенциальный клиент** — счет клиента, связанный с заказом</span><span class="sxs-lookup"><span data-stu-id="6d937-160">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="6d937-161">**Прайс-лист** — настраиваемый прайс-лист для клиента</span><span class="sxs-lookup"><span data-stu-id="6d937-161">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="6d937-162">**Валюта** — валюта для цены</span><span class="sxs-lookup"><span data-stu-id="6d937-162">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="6d937-163">**Поставка в страну/регион** — страна или регион, в которые будут поставлены номенклатуры</span><span class="sxs-lookup"><span data-stu-id="6d937-163">**Ship to country/region** – The country or region that the items will be delivered to</span></span>

<span data-ttu-id="6d937-164">Для таблицы "заказ на продажу" автоматически устанавливаются следующие поля:</span><span class="sxs-lookup"><span data-stu-id="6d937-164">The following fields are automatically set for the sales order table:</span></span>

- <span data-ttu-id="6d937-165">**Язык** — язык заказа (по умолчанию значение берется из записи контакта).</span><span class="sxs-lookup"><span data-stu-id="6d937-165">**Language** – The language of the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="6d937-166">**Поставка в страну/регион** — страна или регион, куда должны быть поставлены номенклатуры (по умолчанию значение берется из записи контакта).</span><span class="sxs-lookup"><span data-stu-id="6d937-166">**Ship to country/region** – The country or region that the items will be delivered to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="6d937-167">**Контактное лицо** — пользователь, с которым можно связаться для получения сведений о заказе (по умолчанию значение берется из записи контакта).</span><span class="sxs-lookup"><span data-stu-id="6d937-167">**Contact person** – The user who can be contacted for information about the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="6d937-168">**Компания** — юридическое лицо, к которому относится заказ (по умолчанию значение берется из записи контакта).</span><span class="sxs-lookup"><span data-stu-id="6d937-168">**Company** – The legal entity that the order belongs to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="6d937-169">**Потенциальный клиент** — счет клиента, связанный с заказом (по умолчанию значение берется из записи контакта).</span><span class="sxs-lookup"><span data-stu-id="6d937-169">**Potential customer** – The customer account that is associated with the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="6d937-170">**Клиент по накладной** — организация для выставления счетов, связанная с заказом (по умолчанию это потенциальный клиент из записи контакта).</span><span class="sxs-lookup"><span data-stu-id="6d937-170">**Invoice customer** – The billing account of the order (The default value is the potential customer from the contact record.)</span></span>
- <span data-ttu-id="6d937-171">**Наименование заказа на продажу** — наименование заказа на продажу (значение по умолчанию — **заказ на продажу**).</span><span class="sxs-lookup"><span data-stu-id="6d937-171">**Sales order name** – The name of the sales order (The default value is **sales order**.)</span></span>
- <span data-ttu-id="6d937-172">**Валюта** — валюта цены (по умолчанию значение берется из записи контакта).</span><span class="sxs-lookup"><span data-stu-id="6d937-172">**Currency** – The currency of the price (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="6d937-173">**Прайс-лист** — настраиваемый прайс-лист для клиента (по умолчанию значение берется из записи контакта).</span><span class="sxs-lookup"><span data-stu-id="6d937-173">**Price list** – The custom price list for the customer (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="6d937-174">**Описание адреса поставки** — адрес поставки заказа на продажу (значение по умолчанию — **описание адреса поставки**).</span><span class="sxs-lookup"><span data-stu-id="6d937-174">**Delivery address description** – The delivery address of the sales order (The default value is **delivery address description**.)</span></span>

### <a name="modify-the-order-creation-process"></a><span data-ttu-id="6d937-175">Изменение процесса создания заказов</span><span class="sxs-lookup"><span data-stu-id="6d937-175">Modify the order creation process</span></span>

<span data-ttu-id="6d937-176">Можно свободно изменять внешний вид и пользовательский интерфейс клиентского портала, если основной процесс создания заказов не изменяется.</span><span class="sxs-lookup"><span data-stu-id="6d937-176">You can freely modify the appearance and UI of the Customer portal if you don't change the basic order creation process.</span></span> <span data-ttu-id="6d937-177">Если необходимо изменить процесс создания заказа, необходимо иметь в виду несколько моментов.</span><span class="sxs-lookup"><span data-stu-id="6d937-177">If you want to change the order creation process, there are a few points that you must keep in mind.</span></span>

<span data-ttu-id="6d937-178">Не удаляйте следующие столбцы из таблицы "заказ на продажу" в Microsoft Dataverse, поскольку они необходимы для создания заказа на продажу в двойной записи:</span><span class="sxs-lookup"><span data-stu-id="6d937-178">Don't remove the following columns from the sales order table in Microsoft Dataverse, because they are required to create a sales order in dual-write:</span></span>

- <span data-ttu-id="6d937-179">**Компания** — юридическое лицо, к которому относится заказ</span><span class="sxs-lookup"><span data-stu-id="6d937-179">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="6d937-180">**Имя** — наименование заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="6d937-180">**Name** – The name of the sales order</span></span>
- <span data-ttu-id="6d937-181">**Валюта** — валюта для цены</span><span class="sxs-lookup"><span data-stu-id="6d937-181">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="6d937-182">**Прайс-лист** — настраиваемый прайс-лист для клиента</span><span class="sxs-lookup"><span data-stu-id="6d937-182">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="6d937-183">**Поставка в страну/регион** — страна или регион, в которые будут поставлены номенклатуры</span><span class="sxs-lookup"><span data-stu-id="6d937-183">**Ship to country/region** – The country or region that the items will be delivered to</span></span>
- <span data-ttu-id="6d937-184">**Потенциальный клиент** — счет клиента, связанный с заказом</span><span class="sxs-lookup"><span data-stu-id="6d937-184">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="6d937-185">**Язык** — язык заказа (обычно этот язык является языком потенциального клиента).</span><span class="sxs-lookup"><span data-stu-id="6d937-185">**Language** – The language of the order (Typically, this language is the language of the potential customer.)</span></span>
- <span data-ttu-id="6d937-186">**Описание адреса поставки** — адрес поставки заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="6d937-186">**Delivery address description** – The delivery address of the sales order</span></span>

<span data-ttu-id="6d937-187">Для номенклатур требуются следующие столбцы:</span><span class="sxs-lookup"><span data-stu-id="6d937-187">For items, the following columns are required:</span></span>

- <span data-ttu-id="6d937-188">**Продукт** — продукт для заказа</span><span class="sxs-lookup"><span data-stu-id="6d937-188">**Product** – The product to order</span></span>
- <span data-ttu-id="6d937-189">**Количество** — количество выбранного продукта</span><span class="sxs-lookup"><span data-stu-id="6d937-189">**Quantity** – The quantity of the selected product</span></span>
- <span data-ttu-id="6d937-190">**Единица измерения** — единица измерения (например, **шт.**, **кг** или **коробка**)</span><span class="sxs-lookup"><span data-stu-id="6d937-190">**Unit** – The unit of measure (for example, **ea.**, **kgs**, or **box**)</span></span>
- <span data-ttu-id="6d937-191">**Поставка в страну/регион** — страна или регион поставки</span><span class="sxs-lookup"><span data-stu-id="6d937-191">**Ship to country/region** – The country or region of delivery</span></span>
- <span data-ttu-id="6d937-192">**Описание адреса поставки** — адрес поставки заказа</span><span class="sxs-lookup"><span data-stu-id="6d937-192">**Delivery address description** – The delivery address of the order</span></span>

<span data-ttu-id="6d937-193">Необходимо обеспечить, чтобы ваш клиентский портал каким-либо образом отправил значения для всех этих столбцов.</span><span class="sxs-lookup"><span data-stu-id="6d937-193">You must make sure that your Customer portal somehow submits values for all these columns.</span></span>

<span data-ttu-id="6d937-194">Если требуется добавить столбцы на страницу или удалить столбцы, см. раздел [Быстрое создание или изменение форм для упрощения ввода данных](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span><span class="sxs-lookup"><span data-stu-id="6d937-194">If you want to add columns to the page, or remove columns, see [Create or edit quick create forms for a streamlined data entry experience](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span></span>

<span data-ttu-id="6d937-195">Если необходимо изменить способ предустановки столбцов и способ задания значений при сохранении страницы, см. следующие сведения в документации по порталам Power Apps:</span><span class="sxs-lookup"><span data-stu-id="6d937-195">If you want to change how columns are preset and how values are set when the page is saved, see the following information in the Power Apps portals documentation:</span></span>

- [<span data-ttu-id="6d937-196">Предварительное заполнение полей</span><span class="sxs-lookup"><span data-stu-id="6d937-196">Prepopulate field</span></span>](/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [<span data-ttu-id="6d937-197">Задание значения при сохранении</span><span class="sxs-lookup"><span data-stu-id="6d937-197">Set Value On Save</span></span>](/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a><span data-ttu-id="6d937-198">Настройка домашней страницы</span><span class="sxs-lookup"><span data-stu-id="6d937-198">Customize the home page</span></span>

<span data-ttu-id="6d937-199">Все элементы управления на клиентском портале являются встроенными элементами управления портала Power Apps.</span><span class="sxs-lookup"><span data-stu-id="6d937-199">All the controls in the Customer portal are built-in Power Apps portals controls.</span></span> <span data-ttu-id="6d937-200">Их можно настроить, следуя шагам в разделе [Создание страницы](/powerapps/maker/portals/compose-page) в документации по порталам Power Apps.</span><span class="sxs-lookup"><span data-stu-id="6d937-200">You can customize them by following the steps in [Compose a page](/powerapps/maker/portals/compose-page) in the Power Apps portals documentation.</span></span>

<span data-ttu-id="6d937-201">Для создания плиток на домашней странице используется единственный настраиваемый элемент управления, включенный в шаблон клиентского портала.</span><span class="sxs-lookup"><span data-stu-id="6d937-201">The only custom control that is included in the Customer portal template is used to create the tiles on the home page.</span></span>

<span data-ttu-id="6d937-202">![Плитки на домашней странице](media/customer-portal-home-page-tiles.png "Плитки на домашней странице")</span><span class="sxs-lookup"><span data-stu-id="6d937-202">![Tiles on the home page](media/customer-portal-home-page-tiles.png "Tiles on the home page")</span></span>

<span data-ttu-id="6d937-203">Для изменения плиток выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6d937-203">To modify the tiles, follow these steps.</span></span>

1. <span data-ttu-id="6d937-204">Откройте [Приложение управления порталом](/powerapps/maker/portals/configure/configure-portal).</span><span class="sxs-lookup"><span data-stu-id="6d937-204">Open the [Portal Management app](/powerapps/maker/portals/configure/configure-portal).</span></span>
1. <span data-ttu-id="6d937-205">В области перехода слева выберите **Шаблоны страницы**.</span><span class="sxs-lookup"><span data-stu-id="6d937-205">In the navigation pane on the left, select **Page Templates**.</span></span>

    <span data-ttu-id="6d937-206">![Область перехода управления порталом](media/customer-portal-nav.png "Область перехода управления порталом")</span><span class="sxs-lookup"><span data-stu-id="6d937-206">![Portal Management navigation pane](media/customer-portal-nav.png "Portal Management navigation pane")</span></span>

1. <span data-ttu-id="6d937-207">Выберите шаблон страницы под названием **Домашняя страница**.</span><span class="sxs-lookup"><span data-stu-id="6d937-207">Select the page template that is named **Home**.</span></span>
1. <span data-ttu-id="6d937-208">В поле **Веб-шаблон** выберите ссылку **Домашняя страница**, чтобы открыть исходный код для этой страницы.</span><span class="sxs-lookup"><span data-stu-id="6d937-208">In the **Web Template** field, select the **Home** link to open the source code for that page.</span></span>

    <span data-ttu-id="6d937-209">![Поле веб-шаблона](media/customer-portal-web-template.png "Поле веб-шаблона")</span><span class="sxs-lookup"><span data-stu-id="6d937-209">![Web Template field](media/customer-portal-web-template.png "Web Template field")</span></span>

1. <span data-ttu-id="6d937-210">Теперь будет показан весь исходный код для домашней страницы, измените его нужным образом.</span><span class="sxs-lookup"><span data-stu-id="6d937-210">You should now see all the source code for the home page and can modify it as you require.</span></span>

## <a name="resources"></a><span data-ttu-id="6d937-211">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="6d937-211">Resources</span></span>

<span data-ttu-id="6d937-212">Для получения дополнительных сведений о настройке клиентского портала см. следующие ресурсы:</span><span class="sxs-lookup"><span data-stu-id="6d937-212">To learn more about how you can set up and customize the Customer portal, see the following resources:</span></span>

- [<span data-ttu-id="6d937-213">Документация по порталам Power Apps</span><span class="sxs-lookup"><span data-stu-id="6d937-213">Power Apps portals documentation</span></span>](/powerapps/maker/portals/overview)
- [<span data-ttu-id="6d937-214">Документация по двойной записи</span><span class="sxs-lookup"><span data-stu-id="6d937-214">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [<span data-ttu-id="6d937-215">О жизненном цикле портала</span><span class="sxs-lookup"><span data-stu-id="6d937-215">About portal lifecycle</span></span>](/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="6d937-216">Обновление портала</span><span class="sxs-lookup"><span data-stu-id="6d937-216">Upgrade a portal</span></span>](/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="6d937-217">Миграция конфигурации портала</span><span class="sxs-lookup"><span data-stu-id="6d937-217">Migrate portal configuration</span></span>](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="6d937-218">Управление жизненным циклом решения: Dynamics 365 для приложений Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="6d937-218">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]