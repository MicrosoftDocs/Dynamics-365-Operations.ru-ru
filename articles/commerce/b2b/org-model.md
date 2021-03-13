---
title: Создание иерархий моделирования организации для организаций B2B
description: В этом разделе описывается создание иерархий моделирования организаций для организаций "бизнес-бизнес" (B2B).
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 450efd595a1cc1b72b2e62afbdd4518bcca59cb0
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035955"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a><span data-ttu-id="6b717-103">Создание иерархий моделирования организации для организаций B2B</span><span class="sxs-lookup"><span data-stu-id="6b717-103">Create org modeling hierarchies for B2B organizations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6b717-104">В этом разделе описывается создание иерархий моделирования организаций для организаций "бизнес-бизнес" (B2B) в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6b717-104">This topic describes how to create organizational modeling hierarchies for business-to-business (B2B) organizations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6b717-105">В Commerce headquarters организации деловых партнеров представлены сущностями клиента и иерархии клиентов.</span><span class="sxs-lookup"><span data-stu-id="6b717-105">In Commerce headquarters, business partner organizations are represented by customer and customer hierarchy entities.</span></span> <span data-ttu-id="6b717-106">Организация делового партнера и ее пользователи представлены как клиенты, а иерархии клиентов используются для связи этих клиентов друг с другом.</span><span class="sxs-lookup"><span data-stu-id="6b717-106">The business partner organization and its users are represented as customers, and customer hierarchies are used to associate those customers with each other.</span></span>

<span data-ttu-id="6b717-107">Когда запрос делового партнера на присоединение к сайту электронной коммерции B2B утвержден, выполняются следующие действия:</span><span class="sxs-lookup"><span data-stu-id="6b717-107">When a business partner request to join a B2B e-commerce site is approved, the following actions are performed:</span></span>

- <span data-ttu-id="6b717-108">В системе создаются две новые записи клиента: запись клиента **Тип организации** для организации делового партнера и запись клиента **Тип лица** для запрашивающего лица (то есть, для пользователя делового партнера, который отправил запрос).</span><span class="sxs-lookup"><span data-stu-id="6b717-108">Two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor (that is, the business partner user who submitted the request).</span></span>
- <span data-ttu-id="6b717-109">Новая запись иерархии клиентов создается в разделе **Клиент \> Иерархия клиентов**.</span><span class="sxs-lookup"><span data-stu-id="6b717-109">A new customer hierarchy record is created under **Customer \> Customer hierarchy**.</span></span> <span data-ttu-id="6b717-110">Эта запись имеет следующие свойства заголовка:</span><span class="sxs-lookup"><span data-stu-id="6b717-110">This record has the following header properties:</span></span>

    - <span data-ttu-id="6b717-111">**Код иерархии клиентов** — уникальный код иерархии клиентов.</span><span class="sxs-lookup"><span data-stu-id="6b717-111">**Customer hierarchy ID** – A unique ID for the customer hierarchy.</span></span> <span data-ttu-id="6b717-112">Этот код использует номерную серию, которая определена в общих параметрах Commerce в Commerce headquarters.</span><span class="sxs-lookup"><span data-stu-id="6b717-112">This ID uses the number sequence that is defined in Commerce shared parameters in Commerce headquarters.</span></span>
    - <span data-ttu-id="6b717-113">**Имя** — название организации делового партнера, как указано в запросе на подключение.</span><span class="sxs-lookup"><span data-stu-id="6b717-113">**Name** – The organization name of the business partner, as specified in the onboarding request.</span></span>
    - <span data-ttu-id="6b717-114">**Назначение** — для этого свойства устанавливается предопределенное значение **Организация B2B**.</span><span class="sxs-lookup"><span data-stu-id="6b717-114">**Purpose** – This property is set to the predefined value **B2B organization**.</span></span>
    - <span data-ttu-id="6b717-115">**Организация** — код клиента делового партнера.</span><span class="sxs-lookup"><span data-stu-id="6b717-115">**Organization** – The customer ID of the business partner.</span></span>

<span data-ttu-id="6b717-116">Ниже приведены подробные сведения о записи иерархии клиентов:</span><span class="sxs-lookup"><span data-stu-id="6b717-116">Here are the details of the customer hierarchy record:</span></span>

- <span data-ttu-id="6b717-117">Запись клиента для инициатора запроса связана с иерархией клиентов.</span><span class="sxs-lookup"><span data-stu-id="6b717-117">The customer record of the requestor is associated with the customer hierarchy.</span></span>
- <span data-ttu-id="6b717-118">Роль администратора связана с инициатором запроса.</span><span class="sxs-lookup"><span data-stu-id="6b717-118">The administrator role is associated with the requestor.</span></span>

<span data-ttu-id="6b717-119">Когда администратор добавляет пользователей к организации делового партнера на сайте B2B, новая запись клиента для каждого пользователя создается в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="6b717-119">When the administrator adds more users are to the business partner organization on a B2B site, a new customer record for each user is created in Commerce headquarters.</span></span> <span data-ttu-id="6b717-120">Эта запись клиента также добавляется к соответствующей записи иерархии клиентов для делового партнера и имеет роль "пользователь".</span><span class="sxs-lookup"><span data-stu-id="6b717-120">This customer record is also added to the relevant customer hierarchy record for the business partner and has the role of a "user."</span></span>

> [!NOTE]
> <span data-ttu-id="6b717-121">В большинстве случаев должны совпадать значения соответствующих свойств всех записей клиентов в иерархии.</span><span class="sxs-lookup"><span data-stu-id="6b717-121">In most cases, the corresponding property values of all customer records in a hierarchy should match.</span></span> <span data-ttu-id="6b717-122">Например, так как все пользователи делового партнера должны получить аналогичные цены для продуктов, их ценовая группа и соответствующие конфигурации должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="6b717-122">For example, because all business partner users should get similar prices for products, their price group and associated configurations should match.</span></span> <span data-ttu-id="6b717-123">Однако система не обеспечивает принудительно такую согласованность.</span><span class="sxs-lookup"><span data-stu-id="6b717-123">However, the system doesn't enforce this consistency.</span></span> <span data-ttu-id="6b717-124">Таким образом, соответствующие пользователи Commerce headquarters несут ответственность за обеспечение соответствия значений и конфигураций свойств для всех клиентов в определенной иерархии.</span><span class="sxs-lookup"><span data-stu-id="6b717-124">Therefore, the relevant Commerce headquarters users are responsible for ensuring that the property values and configurations match for all customers in a given hierarchy.</span></span>

<span data-ttu-id="6b717-125">Пользователи Commerce headquarters могут просмотреть значения свойств для всех записей клиентов в иерархии в параллельном режиме.</span><span class="sxs-lookup"><span data-stu-id="6b717-125">Commerce headquarters users can look at the property values for all customer records in the hierarchy in a side-by-side view.</span></span> <span data-ttu-id="6b717-126">Выберите соответствующие свойства записей клиентов, выбрав имена вкладок в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="6b717-126">Select the relevant customer record properties by selecting the tab names on the drop-down menu.</span></span> <span data-ttu-id="6b717-127">Пользователи могут непосредственно просматривать и редактировать значения свойств из этого представления.</span><span class="sxs-lookup"><span data-stu-id="6b717-127">Users can directly view and edit the property values from this view.</span></span> <span data-ttu-id="6b717-128">В качестве альтернативы, если требуется применить все значения из записи клиента-администратора для всех записей клиентов-пользователей, выберите **Переопределить** в данных иерархии клиентов.</span><span class="sxs-lookup"><span data-stu-id="6b717-128">Alternatively, if you want to apply all the values from the administrator customer record to all the user customer records, select **Override** in the customer hierarchy details.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6b717-129">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6b717-129">Additional resources</span></span>

[<span data-ttu-id="6b717-130">Настройка сайта электронной коммерции B2B</span><span class="sxs-lookup"><span data-stu-id="6b717-130">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="6b717-131">Управление пользователями деловых партнеров на сайтах электронной коммерции B2B</span><span class="sxs-lookup"><span data-stu-id="6b717-131">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="6b717-132">Настройка метода платежа для счета клиента для сайтов электронной коммерции B2B</span><span class="sxs-lookup"><span data-stu-id="6b717-132">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="6b717-133">Настройка лимитов количества продуктов для сайтов электронной коммерции B2B</span><span class="sxs-lookup"><span data-stu-id="6b717-133">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)