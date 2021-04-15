---
title: Планирование глобальной адресной книги и других адресных книг
description: Эта тема описывает вопросы и решения, которые следует принять во время процесса планирования.
author: msftbrking
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1d3a476a183453f170dae9b812949822ea60edd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747617"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a><span data-ttu-id="1d823-103">План для глобальной адресной книги и других адресных книг</span><span class="sxs-lookup"><span data-stu-id="1d823-103">Plan for the global address book and other address books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d823-104">Эта тема описывает вопросы и решения, которые следует принять во время процесса планирования, прежде чем настраивать и устанавливать глобальную адресную книгу и любые дополнительные адресные книги.</span><span class="sxs-lookup"><span data-stu-id="1d823-104">This topic describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books.</span></span> <span data-ttu-id="1d823-105">Некоторые из решений потребуют от вас подтвердить решения, которые были сделаны в других зонах продукта, таких как организационная иерархия.</span><span class="sxs-lookup"><span data-stu-id="1d823-105">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

## <a name="global-address-book"></a><span data-ttu-id="1d823-106">Глобальная адресная книга</span><span class="sxs-lookup"><span data-stu-id="1d823-106">Global address book</span></span>

<span data-ttu-id="1d823-107">Прежде чем начать работу с глобальной адресной книгой, необходимо определить значения по умолчанию для нее.</span><span class="sxs-lookup"><span data-stu-id="1d823-107">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="1d823-108">Эти значения по умолчанию будут использоваться для всех дополнительных создаваемых адресных книг.</span><span class="sxs-lookup"><span data-stu-id="1d823-108">These default values are then used for any additional address books that you create.</span></span>

<span data-ttu-id="1d823-109">**Решения**</span><span class="sxs-lookup"><span data-stu-id="1d823-109">**Decisions**</span></span>

- <span data-ttu-id="1d823-110">В какой последовательности должны отображаться имена в записях субъектов типа **Лицо**?</span><span class="sxs-lookup"><span data-stu-id="1d823-110">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="1d823-111">Например, фамилия, отчество, имя.</span><span class="sxs-lookup"><span data-stu-id="1d823-111">For example, one sequence is last name, middle name, first name.</span></span>
- <span data-ttu-id="1d823-112">Должны записи субъекта удаляться из адресной книги при удалении записи роли?</span><span class="sxs-lookup"><span data-stu-id="1d823-112">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="1d823-113">Например, если удаляется запись клиента, должна ли удаляться запись субъекта?</span><span class="sxs-lookup"><span data-stu-id="1d823-113">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
- <span data-ttu-id="1d823-114">При создании новой записи должны ли пользователи получать уведомление, если в глобальной адресной книге найдена дублирующая запись?</span><span class="sxs-lookup"><span data-stu-id="1d823-114">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
- <span data-ttu-id="1d823-115">Должен ли номер номерной системы (DUNS) отображаться в сведениях записи субъекта?</span><span class="sxs-lookup"><span data-stu-id="1d823-115">Should the Data Universal Numbering System (DUNS) number be included in a party record's information?</span></span>
- <span data-ttu-id="1d823-116">Если номер DUNS включен в запись субъекта, должна ли проверяться уникальность номера?</span><span class="sxs-lookup"><span data-stu-id="1d823-116">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
- <span data-ttu-id="1d823-117">При создании записи субъекта в глобальной адресной книге следует ли указывать тип субъекта, лицо или организацию по умолчанию?</span><span class="sxs-lookup"><span data-stu-id="1d823-117">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
- <span data-ttu-id="1d823-118">Какие роли пользователя могут получать доступ к личным адресам и контактной информации записей субъектов?</span><span class="sxs-lookup"><span data-stu-id="1d823-118">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="1d823-119">Дополнительные адресные книги</span><span class="sxs-lookup"><span data-stu-id="1d823-119">Additional address books</span></span>

<span data-ttu-id="1d823-120">После создания глобальной адресной книги вы можете создать дополнительные адресные книги согласно своим потребностям, например отдельную адресную книгу для каждой компании в вашей организации или для каждой сферы деятельности.</span><span class="sxs-lookup"><span data-stu-id="1d823-120">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="1d823-121">Например, Fabrikam — международная организация, которая имеет несколько компаний и несколько сфер деятельности.</span><span class="sxs-lookup"><span data-stu-id="1d823-121">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="1d823-122">Fabrikam планирует создать адресную книгу для каждой сферы бизнеса.</span><span class="sxs-lookup"><span data-stu-id="1d823-122">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="1d823-123">Для сфер деятельности, которые выполняются в нескольких расположениях, например производство пневматических инструментов, Fabrikam создает адресную книгу для каждого расположения.</span><span class="sxs-lookup"><span data-stu-id="1d823-123">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="1d823-124">Крис, ИТ-менеджер в Fabrikam, создал следующий список необходимых адресных книг.</span><span class="sxs-lookup"><span data-stu-id="1d823-124">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="1d823-125">Этот список также описывает записи субъектов, которые должна включить каждая адресная книга.</span><span class="sxs-lookup"><span data-stu-id="1d823-125">This list also describes the party records that each address book must include.</span></span>

- <span data-ttu-id="1d823-126">**Договора в государственном секторе (PubSC)** — записи субъектов для всех субъектов, связанных с договорами в государственного секторе, подписанными Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="1d823-126">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="1d823-127">**Договора в частном секторе (PriSC)** — записи субъектов для всех субъектов, связанных с договорами в частном секторе, подписанными Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="1d823-127">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="1d823-128">**Электроинструменты (ET)** — записи субъектов для всех субъектов, связанных с покупкой или продажей электроинструментов или иным образом связанных с электроинструментами, поставляемыми или приобретаемыми для Fabrikam компанией Fabrikam-Япония.</span><span class="sxs-lookup"><span data-stu-id="1d823-128">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="1d823-129">**Пневматические инструменты (PTJPN)** — записи субъектов для всех субъектов, связанных с покупкой или продажей пневматических инструментов или иным образом связанных с пневматическими инструментами, поставляемыми или приобретаемыми для Fabrikam компанией Fabrikam-Япония.</span><span class="sxs-lookup"><span data-stu-id="1d823-129">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="1d823-130">**Пневматические инструменты (PTUSA)** — записи субъектов для всех субъектов, связанных с покупкой или продажей пневматических инструментов или иным образом связанных с пневматическими инструментами, поставляемыми или приобретаемыми для Fabrikam компанией Fabrikam-США.</span><span class="sxs-lookup"><span data-stu-id="1d823-130">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="1d823-131">**Решение.**</span><span class="sxs-lookup"><span data-stu-id="1d823-131">**Decision:**</span></span>

- <span data-ttu-id="1d823-132">Сколько дополнительных адресных книг требуется создать?</span><span class="sxs-lookup"><span data-stu-id="1d823-132">How many additional address books will you create?</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]