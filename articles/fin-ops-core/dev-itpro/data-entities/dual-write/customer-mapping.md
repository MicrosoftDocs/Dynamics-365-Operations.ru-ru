---
title: Интегрированный мастер клиентов
description: Эта тема описывает интеграцию данных клиента между Finance and Operations и Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 269346d38eeb3812c352d16f9d50fbcd09307c12
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019983"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="f527e-103">Интегрированный справочник клиентов</span><span class="sxs-lookup"><span data-stu-id="f527e-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="f527e-104">Это типично для записей клиентов, что они обрабатываются в нескольких приложениях.</span><span class="sxs-lookup"><span data-stu-id="f527e-104">It's typical for customer records to be mastered in more than one application.</span></span> <span data-ttu-id="f527e-105">Например, деятельность по продажам может использовать записи коммерческих клиентов через приложение Sales, а электронная коммерция или розничные продажи могут использовать записи клиентов через приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f527e-105">For example, sales activity can bring in commercial customer records through a Sales application, and e-Commerce or retail sales can bring in customer records through a Finance and Operations application.</span></span> <span data-ttu-id="f527e-106">Независимо от того, откуда берет начало запись клиента, она интегрируется за кулисами вне зависимости от границ приложений и различий в инфраструктуре.</span><span class="sxs-lookup"><span data-stu-id="f527e-106">Regardless of where the customer record originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> <span data-ttu-id="f527e-107">Интегрированная обработка клиентов помогает обрабатывать сценарии мультимастеринга и обеспечивает полное представление клиентов для набора приложений Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f527e-107">Integrated customer mastering helps handle multi-mastering scenarios and provides a comprehensive view of the customer to the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="f527e-108">Поток данных клиентов</span><span class="sxs-lookup"><span data-stu-id="f527e-108">Customer data flow</span></span>

<span data-ttu-id="f527e-109">*Клиент* — это хорошо определенная концепция в приложениях.</span><span class="sxs-lookup"><span data-stu-id="f527e-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="f527e-110">Таким образом, интеграция данных клиентов просто включает в себя согласование концепции клиента между двумя приложениями.</span><span class="sxs-lookup"><span data-stu-id="f527e-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="f527e-111">На следующем рисунке показан поток данных клиентов.</span><span class="sxs-lookup"><span data-stu-id="f527e-111">The following illustration shows the customer data flow.</span></span>

![Поток данных клиентов](media/dual-write-customer-data-flow.png)

<span data-ttu-id="f527e-113">Клиенты могут быть широко классифицированы на два типа: коммерческие/организационные клиенты и потребители/конечные пользователи.</span><span class="sxs-lookup"><span data-stu-id="f527e-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="f527e-114">Эти два типа клиентов хранятся и обрабатываются по-разному в Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f527e-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="f527e-115">В Finance and Operations как коммерческие/организационные клиенты, так и потребители/конечные пользователи обрабатываются в одной таблице, которая называется **CustTable** (CustomerCustomerV3Entity), и классифицируются на основе атрибута **Тип**.</span><span class="sxs-lookup"><span data-stu-id="f527e-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustomerCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="f527e-116">(Если для параметра **Тип** задано значение **Организация**, клиент является коммерческим/организационным клиентом, а если для параметра **Тип** задано значение **Физическое лицо**, то клиент является потребителем/конечным пользователем.) Информация об основном контактном лице обрабатывается через сущность SMMContactPersonEntity.</span><span class="sxs-lookup"><span data-stu-id="f527e-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="f527e-117">В Common Data Service коммерческие/организационные клиенты обрабатываются в сущности "Организация" и идентифицируются в качестве клиентов, когда атрибут **RelationshipType** имеет значение **Клиент**.</span><span class="sxs-lookup"><span data-stu-id="f527e-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="f527e-118">Как потребители/конечные пользователи, так и контактное лицо представлены сущностью "Контакт".</span><span class="sxs-lookup"><span data-stu-id="f527e-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="f527e-119">Чтобы обеспечить четкое разделение между потребителем/конечным пользователем и контактным лицом, сущность **Контакт** имеет флаг типа Boolean, который называется **Для продажи**.</span><span class="sxs-lookup"><span data-stu-id="f527e-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="f527e-120">Когда параметр **Для продажи** имеет значение **True**, контакт является потребителем/конечным пользователем, и для этого контакта могут быть созданы предложения с расценками и заказы.</span><span class="sxs-lookup"><span data-stu-id="f527e-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="f527e-121">Когда параметр **Для продажи** имеет значение **False**, контакт является просто основным контактным лицом клиента.</span><span class="sxs-lookup"><span data-stu-id="f527e-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="f527e-122">Когда контакт, для которого невозможны продажи, участвует в процессе предложений с расценками или заказа, для параметра **Для продажи** устанавливается значение **True**, чтобы пометить контакт как контакт для продажи.</span><span class="sxs-lookup"><span data-stu-id="f527e-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="f527e-123">Контакт, который стал контактом для продажи, остается контактом для продажи.</span><span class="sxs-lookup"><span data-stu-id="f527e-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="f527e-124">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="f527e-124">Templates</span></span>

<span data-ttu-id="f527e-125">Данные о клиентах включают всю информацию о клиенте, например, группу клиентов, адреса, контактную информацию, профиль платежа, профиль счета-фактуры и статус лояльности.</span><span class="sxs-lookup"><span data-stu-id="f527e-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="f527e-126">Коллекция сопоставлений сущностей работает совместно во время взаимодействия данных клиентов, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f527e-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="f527e-127">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f527e-127">Finance and Operations apps</span></span> | <span data-ttu-id="f527e-128">Другие приложения Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f527e-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="f527e-129">Описание</span><span class="sxs-lookup"><span data-stu-id="f527e-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="f527e-130">Контакты CDS V2</span><span class="sxs-lookup"><span data-stu-id="f527e-130">CDS Contacts V2</span></span>             | <span data-ttu-id="f527e-131">контакты</span><span class="sxs-lookup"><span data-stu-id="f527e-131">contacts</span></span>                        | <span data-ttu-id="f527e-132">Этот шаблон синхронизирует все первичные, вторичные и третичные контактные данные клиентов и поставщиков.</span><span class="sxs-lookup"><span data-stu-id="f527e-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="f527e-133">Группы клиентов</span><span class="sxs-lookup"><span data-stu-id="f527e-133">Customer groups</span></span>             | <span data-ttu-id="f527e-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="f527e-134">msdyn_customergroups</span></span>            | <span data-ttu-id="f527e-135">Этот шаблон синхронизирует сведения о группах клиентов.</span><span class="sxs-lookup"><span data-stu-id="f527e-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="f527e-136">Способ оплаты клиента</span><span class="sxs-lookup"><span data-stu-id="f527e-136">Customer payment method</span></span>     | <span data-ttu-id="f527e-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="f527e-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="f527e-138">Этот шаблон синхронизирует сведения о способах оплаты клиентов.</span><span class="sxs-lookup"><span data-stu-id="f527e-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="f527e-139">Клиенты V3</span><span class="sxs-lookup"><span data-stu-id="f527e-139">Customers V3</span></span>                | <span data-ttu-id="f527e-140">счета</span><span class="sxs-lookup"><span data-stu-id="f527e-140">accounts</span></span>                        | <span data-ttu-id="f527e-141">Этот шаблон синхронизирует основную информацию о клиентах для коммерческих и организационных клиентов.</span><span class="sxs-lookup"><span data-stu-id="f527e-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="f527e-142">Клиенты V3</span><span class="sxs-lookup"><span data-stu-id="f527e-142">Customers V3</span></span>                | <span data-ttu-id="f527e-143">контакты</span><span class="sxs-lookup"><span data-stu-id="f527e-143">contacts</span></span>                        | <span data-ttu-id="f527e-144">Этот шаблон синхронизирует справочник клиентов для клиентов и конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="f527e-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="f527e-145">Карта постоянного клиента</span><span class="sxs-lookup"><span data-stu-id="f527e-145">Loyalty card</span></span>                | <span data-ttu-id="f527e-146">msdyn_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="f527e-146">msdyn_loyaltycards</span></span>              | <span data-ttu-id="f527e-147">Этот шаблон синхронизирует сведения о картах лояльности клиентов.</span><span class="sxs-lookup"><span data-stu-id="f527e-147">This template synchronizes customer loyalty card information.</span></span>
<span data-ttu-id="f527e-148">Аффиксы имен</span><span class="sxs-lookup"><span data-stu-id="f527e-148">Name affixes</span></span>                | <span data-ttu-id="f527e-149">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="f527e-149">msdyn_nameaffixes</span></span>               | <span data-ttu-id="f527e-150">Этот шаблон синхронизирует ссылочные данные аффиксов имен как для клиентов, так и для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="f527e-150">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="f527e-151">Строки платежных дней CDS V2</span><span class="sxs-lookup"><span data-stu-id="f527e-151">Payment day lines CDS V2</span></span>    | <span data-ttu-id="f527e-152">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="f527e-152">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="f527e-153">Этот шаблон синхронизирует ссылочные данные строк дней оплаты как для клиентов, так и для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="f527e-153">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="f527e-154">Платежные дни CDS</span><span class="sxs-lookup"><span data-stu-id="f527e-154">Payment days CDS</span></span>            | <span data-ttu-id="f527e-155">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="f527e-155">msdyn_paymentdays</span></span>               | <span data-ttu-id="f527e-156">Этот шаблон синхронизирует ссылочные данные дней оплаты как для клиентов, так и для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="f527e-156">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="f527e-157">Строки графика платежей</span><span class="sxs-lookup"><span data-stu-id="f527e-157">Payment schedule lines</span></span>      | <span data-ttu-id="f527e-158">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="f527e-158">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="f527e-159">Синхронизирует ссылочные данные строк графиков оплаты как для клиентов, так и для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="f527e-159">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="f527e-160">График оплаты</span><span class="sxs-lookup"><span data-stu-id="f527e-160">Payment schedule</span></span>            | <span data-ttu-id="f527e-161">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="f527e-161">msdyn_paymentschedules</span></span>          | <span data-ttu-id="f527e-162">Этот шаблон синхронизирует ссылочные данные графиков оплаты как для клиентов, так и для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="f527e-162">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="f527e-163">Условия оплаты</span><span class="sxs-lookup"><span data-stu-id="f527e-163">Terms of payment</span></span>            | <span data-ttu-id="f527e-164">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="f527e-164">msdyn_paymentterms</span></span>              | <span data-ttu-id="f527e-165">Этот шаблон синхронизирует ссылочные данные условий оплаты (условия оплаты) как для клиентов, так и для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="f527e-165">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
