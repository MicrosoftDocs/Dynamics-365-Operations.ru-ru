---
title: Интегрированный мастер клиентов
description: Эта тема описывает интеграцию данных клиента между Finance and Operations и Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 402342b459c366d0e198e3d0e946deb1f9e81739
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568134"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="6778d-103">Интегрированный справочник клиентов</span><span class="sxs-lookup"><span data-stu-id="6778d-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="6778d-104">Данные клиентов могут обрабатываться в нескольких приложениях Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6778d-104">Customer data can be mastered in more than one Dynamics 365 application.</span></span> <span data-ttu-id="6778d-105">Например, строка клиента может быть получена через действия продажи в Dynamics 365 Sales (приложение на основе модели в Dynamics 365) или строка может происходить из розничной деятельности в Dynamics 365 Commerce (приложение Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="6778d-105">For example, a customer row can originate though sales activity in Dynamics 365 Sales (a model-driven app in Dynamics 365), or a row can originate through retail activity in Dynamics 365 Commerce (a Finance and Operations app).</span></span> <span data-ttu-id="6778d-106">Вне зависимости от того, где созданы данные клиента, они интегрируются в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="6778d-106">No matter where where the customer data originates, it is integrated behind the scenes.</span></span> <span data-ttu-id="6778d-107">Интегрированная главная база данных клиентов предоставляет гибкие возможности контролировать данные клиентов в любом приложении Dynamics 365 и обеспечивает полное представление клиента во всем наборе приложений Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6778d-107">Integrated customer master gives you the flexibility to master customer data in any Dynamics 365 application and provides a comprehensive view of the customer across the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="6778d-108">Поток данных клиентов</span><span class="sxs-lookup"><span data-stu-id="6778d-108">Customer data flow</span></span>

<span data-ttu-id="6778d-109">*Клиент* — это хорошо определенная концепция в приложениях.</span><span class="sxs-lookup"><span data-stu-id="6778d-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="6778d-110">Таким образом, интеграция данных клиентов просто включает в себя согласование концепции клиента между двумя приложениями.</span><span class="sxs-lookup"><span data-stu-id="6778d-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="6778d-111">На следующем рисунке показан поток данных клиентов.</span><span class="sxs-lookup"><span data-stu-id="6778d-111">The following illustration shows the customer data flow.</span></span>

![Поток данных клиентов](media/dual-write-customer-data-flow.png)

<span data-ttu-id="6778d-113">Клиенты могут быть широко классифицированы на два типа: коммерческие/организационные клиенты и потребители/конечные пользователи.</span><span class="sxs-lookup"><span data-stu-id="6778d-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="6778d-114">Эти два типа клиентов хранятся и обрабатываются по-разному в Finance and Operations и Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6778d-114">These two types of customers are stored and handled differently in Finance and Operations and Dataverse.</span></span>

<span data-ttu-id="6778d-115">В Finance and Operations как коммерческие/организационные клиенты, так и потребители/конечные пользователи обрабатываются в одной таблице, которая называется **CustTable** (CustCustomerV3Entity), и классифицируются на основе атрибута **Тип**.</span><span class="sxs-lookup"><span data-stu-id="6778d-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="6778d-116">(Если для параметра **Тип** задано значение **Организация**, клиент является коммерческим/организационным клиентом, а если для параметра **Тип** задано значение **Физическое лицо**, то клиент является потребителем/конечным пользователем.) Информация об основном контактном лице обрабатывается через таблицу SMMContactPersonEntity.</span><span class="sxs-lookup"><span data-stu-id="6778d-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity table.</span></span>

<span data-ttu-id="6778d-117">В Dataverse коммерческие/организационные клиенты обрабатываются в таблице "Организация" и идентифицируются в качестве клиентов, когда атрибут **RelationshipType** имеет значение **Клиент**.</span><span class="sxs-lookup"><span data-stu-id="6778d-117">In Dataverse, commercial/organizational customers are mastered in the Account table and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="6778d-118">Как потребители/конечные пользователи, так и контактное лицо представлены таблицей "Контакт".</span><span class="sxs-lookup"><span data-stu-id="6778d-118">Both consumers/end users and the contact person are represented by the Contact table.</span></span> <span data-ttu-id="6778d-119">Чтобы обеспечить четкое разделение между потребителем/конечным пользователем и контактным лицом, таблица **Контакт** имеет флаг типа Boolean, который называется **Для продажи**.</span><span class="sxs-lookup"><span data-stu-id="6778d-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** table has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="6778d-120">Когда параметр **Для продажи** имеет значение **True**, контакт является потребителем/конечным пользователем, и для этого контакта могут быть созданы предложения с расценками и заказы.</span><span class="sxs-lookup"><span data-stu-id="6778d-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="6778d-121">Когда параметр **Для продажи** имеет значение **False**, контакт является просто основным контактным лицом клиента.</span><span class="sxs-lookup"><span data-stu-id="6778d-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="6778d-122">Когда контакт, для которого невозможны продажи, участвует в процессе предложений с расценками или заказа, для параметра **Для продажи** устанавливается значение **True**, чтобы пометить контакт как контакт для продажи.</span><span class="sxs-lookup"><span data-stu-id="6778d-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="6778d-123">Контакт, который стал контактом для продажи, остается контактом для продажи.</span><span class="sxs-lookup"><span data-stu-id="6778d-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="6778d-124">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="6778d-124">Templates</span></span>

<span data-ttu-id="6778d-125">Данные о клиентах включают всю информацию о клиенте, например, группу клиентов, адреса, контактную информацию, профиль платежа, профиль счета-фактуры и статус лояльности.</span><span class="sxs-lookup"><span data-stu-id="6778d-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="6778d-126">Коллекция сопоставлений таблиц работает совместно во время взаимодействия данных клиентов, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6778d-126">A collection of table maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="6778d-127">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6778d-127">Finance and Operations apps</span></span> | <span data-ttu-id="6778d-128">Другие приложения Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6778d-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="6778d-129">Описание</span><span class="sxs-lookup"><span data-stu-id="6778d-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="6778d-130">Контакты CDS V2</span><span class="sxs-lookup"><span data-stu-id="6778d-130">CDS Contacts V2</span></span>             | <span data-ttu-id="6778d-131">контакты</span><span class="sxs-lookup"><span data-stu-id="6778d-131">contacts</span></span>                        | <span data-ttu-id="6778d-132">Этот шаблон синхронизирует все первичные, вторичные и третичные контактные данные клиентов и поставщиков.</span><span class="sxs-lookup"><span data-stu-id="6778d-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="6778d-133">Группы клиентов</span><span class="sxs-lookup"><span data-stu-id="6778d-133">Customer groups</span></span>             | <span data-ttu-id="6778d-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="6778d-134">msdyn_customergroups</span></span>            | <span data-ttu-id="6778d-135">Этот шаблон синхронизирует сведения о группах клиентов.</span><span class="sxs-lookup"><span data-stu-id="6778d-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="6778d-136">Способ оплаты клиента</span><span class="sxs-lookup"><span data-stu-id="6778d-136">Customer payment method</span></span>     | <span data-ttu-id="6778d-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="6778d-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="6778d-138">Этот шаблон синхронизирует сведения о способах оплаты клиентов.</span><span class="sxs-lookup"><span data-stu-id="6778d-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="6778d-139">Клиенты V3</span><span class="sxs-lookup"><span data-stu-id="6778d-139">Customers V3</span></span>                | <span data-ttu-id="6778d-140">счета</span><span class="sxs-lookup"><span data-stu-id="6778d-140">accounts</span></span>                        | <span data-ttu-id="6778d-141">Этот шаблон синхронизирует основную информацию о клиентах для коммерческих и организационных клиентов.</span><span class="sxs-lookup"><span data-stu-id="6778d-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="6778d-142">Клиенты V3</span><span class="sxs-lookup"><span data-stu-id="6778d-142">Customers V3</span></span>                | <span data-ttu-id="6778d-143">контакты</span><span class="sxs-lookup"><span data-stu-id="6778d-143">contacts</span></span>                        | <span data-ttu-id="6778d-144">Этот шаблон синхронизирует справочник клиентов для клиентов и конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="6778d-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="6778d-145">Аффиксы имен</span><span class="sxs-lookup"><span data-stu-id="6778d-145">Name affixes</span></span>                | <span data-ttu-id="6778d-146">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="6778d-146">msdyn_nameaffixes</span></span>               | <span data-ttu-id="6778d-147">Этот шаблон синхронизирует ссылочные данные аффиксов имен как для клиентов, так и для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="6778d-147">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="6778d-148">Строки платежных дней CDS V2</span><span class="sxs-lookup"><span data-stu-id="6778d-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="6778d-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="6778d-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="6778d-150">Этот шаблон синхронизирует ссылочные данные строк дней оплаты как для клиентов, так и для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="6778d-150">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="6778d-151">Платежные дни CDS</span><span class="sxs-lookup"><span data-stu-id="6778d-151">Payment days CDS</span></span>            | <span data-ttu-id="6778d-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="6778d-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="6778d-153">Этот шаблон синхронизирует ссылочные данные дней оплаты как для клиентов, так и для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="6778d-153">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="6778d-154">Строки графика платежей</span><span class="sxs-lookup"><span data-stu-id="6778d-154">Payment schedule lines</span></span>      | <span data-ttu-id="6778d-155">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="6778d-155">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="6778d-156">Синхронизирует ссылочные данные строк графиков оплаты как для клиентов, так и для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="6778d-156">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="6778d-157">График оплаты</span><span class="sxs-lookup"><span data-stu-id="6778d-157">Payment schedule</span></span>            | <span data-ttu-id="6778d-158">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="6778d-158">msdyn_paymentschedules</span></span>          | <span data-ttu-id="6778d-159">Этот шаблон синхронизирует ссылочные данные графиков оплаты как для клиентов, так и для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="6778d-159">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="6778d-160">Условия оплаты</span><span class="sxs-lookup"><span data-stu-id="6778d-160">Terms of payment</span></span>            | <span data-ttu-id="6778d-161">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="6778d-161">msdyn_paymentterms</span></span>              | <span data-ttu-id="6778d-162">Этот шаблон синхронизирует ссылочные данные условий оплаты (условия оплаты) как для клиентов, так и для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="6778d-162">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]