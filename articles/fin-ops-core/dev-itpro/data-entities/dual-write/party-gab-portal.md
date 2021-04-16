---
title: Использование портала Power с моделью данных субъекта
description: В этой теме описываются изменения в веб-ролях портала Power из-за модели данных субъекта в двойной записи.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833098"
---
# <a name="using-power-portal-with-the-party-data-model"></a><span data-ttu-id="a2eb2-103">Использование портала Power с моделью данных субъекта</span><span class="sxs-lookup"><span data-stu-id="a2eb2-103">Using Power Portal with the Party data model</span></span>

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a2eb2-104">Версия решения управления приложением двойной записи 2.0.999.0 и более поздних версий включает в себя изменения модели данных для субъекта и глобальной адресной книги для таблиц организаций и контактов.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-104">The Dual-write application orchestration solution version 2.0.999.0 and later includes data model changes to party and global address book for the Account and Contact tables.</span></span> <span data-ttu-id="a2eb2-105">Изменения разрешают связи "многие ко многим", которые поддерживают сложные бизнес-сценарии.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-105">The changes allow many-to-many relationships that support advanced business scenarios.</span></span> <span data-ttu-id="a2eb2-106">Эти изменения не поддерживаются веб-ролями портала, включая портал клиента, которые поставляются готовыми или находятся в вашей среде до установки двойной записи.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-106">These changes are not supported by portal web roles, including the customer portal, that are shipped out-of-the-box or that existed in your environment before you installed dual-write.</span></span> <span data-ttu-id="a2eb2-107">Для корректной работы веб-ролей необходимо создать новые веб-роли с использованием новой модели данных.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-107">For the web roles to work as expected, you need to create new web roles using the new data model.</span></span> 

<span data-ttu-id="a2eb2-108">В целом, способ взаимодействия таблиц изменился, но права доступа к таблице на портале клиента не изменились.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-108">In summary, the way the tables interact has changed, but the table permissions in the customer portal haven't changed.</span></span> <span data-ttu-id="a2eb2-109">В этой теме объясняется, как создавать новые веб-роли, которые работают с новой расширенной моделью данных.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-109">This topic explains how to create new web roles that work with the new advanced data model.</span></span>

<span data-ttu-id="a2eb2-110">На этой диаграмме показано отношение таблиц **без** модели данных субъектов и глобальной адресной книги:</span><span class="sxs-lookup"><span data-stu-id="a2eb2-110">This diagram shows the table relationship **without** the party and global address book data model:</span></span>

   ![без модели субъектов](media/without-party-model.PNG)

<span data-ttu-id="a2eb2-112">На этой диаграмме показано отношение таблиц **с** моделью данных субъектов и глобальной адресной книги:</span><span class="sxs-lookup"><span data-stu-id="a2eb2-112">This diagram shows the table relationship **with** the party and global address book data model:</span></span>

   ![с моделью субъектов](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a><span data-ttu-id="a2eb2-114">Создание новых разрешений для таблицы</span><span class="sxs-lookup"><span data-stu-id="a2eb2-114">Create a new table permission</span></span>

<span data-ttu-id="a2eb2-115">Чтобы создать эти новые разрешения для таблицы, необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a2eb2-115">To create these new table permissions, follow these steps:</span></span>

1. <span data-ttu-id="a2eb2-116">Выполните вход в [Power Apps](https://make.powerapps.com) и перейдите к вашим приложениям.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-116">Sign in to [Power Apps](https://make.powerapps.com), and go to your apps.</span></span>
2. <span data-ttu-id="a2eb2-117">Выберите приложение управления порталом.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-117">Select your Portal Management app.</span></span>
3. <span data-ttu-id="a2eb2-118">В боковой области выберите **Безопасность > Разрешения таблиц**.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-118">In the side bar, select **Security > Table permissions**.</span></span>

    <span data-ttu-id="a2eb2-119">Необходимо создать три новых разрешения:</span><span class="sxs-lookup"><span data-stu-id="a2eb2-119">You must create three new permissions:</span></span>

    + <span data-ttu-id="a2eb2-120">Подключение от контакта к субъекту</span><span class="sxs-lookup"><span data-stu-id="a2eb2-120">Contact to Party connection</span></span>
    + <span data-ttu-id="a2eb2-121">Подключение от субъекта к организации</span><span class="sxs-lookup"><span data-stu-id="a2eb2-121">Party to Account connection</span></span>
    + <span data-ttu-id="a2eb2-122">Подключение от организации к заказу</span><span class="sxs-lookup"><span data-stu-id="a2eb2-122">Account to Order connection</span></span>

4. <span data-ttu-id="a2eb2-123">Создайте и сохраните новое разрешение для подключения контакта к субъекту, задав следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="a2eb2-123">Create and save a new permission for the Contact to Party connection, setting these parameters:</span></span>

    + <span data-ttu-id="a2eb2-124">**Имя**: Подключение субъекта к организации (или по вашему выбору)</span><span class="sxs-lookup"><span data-stu-id="a2eb2-124">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="a2eb2-125">**Имя таблицы**: msdyn_contactforparty</span><span class="sxs-lookup"><span data-stu-id="a2eb2-125">**Table Name**: msdyn_contactforparty</span></span>
    + <span data-ttu-id="a2eb2-126">**Веб-сайт**: Клиентский портал</span><span class="sxs-lookup"><span data-stu-id="a2eb2-126">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="a2eb2-127">**Область действия**: контакт</span><span class="sxs-lookup"><span data-stu-id="a2eb2-127">**Scope**: Contact</span></span>
    + <span data-ttu-id="a2eb2-128">**Привилегии**: выберите все</span><span class="sxs-lookup"><span data-stu-id="a2eb2-128">**Privileges**: Select all</span></span>
    + <span data-ttu-id="a2eb2-129">**Веб-роли**: прошедшие проверку пользователи, представитель клиента (или на ваше усмотрение)</span><span class="sxs-lookup"><span data-stu-id="a2eb2-129">**Web roles**: Authenticated Users, Customer Representative (or your choice)</span></span>

5. <span data-ttu-id="a2eb2-130">Создайте и сохраните новое разрешение для подключения субъекта к организации, задав следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="a2eb2-130">Create and save a new permission for the Party to Account connection, setting these parameters:</span></span>

    + <span data-ttu-id="a2eb2-131">**Имя**: Подключение субъекта к организации (или по вашему выбору)</span><span class="sxs-lookup"><span data-stu-id="a2eb2-131">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="a2eb2-132">**Имя таблицы**: account</span><span class="sxs-lookup"><span data-stu-id="a2eb2-132">**Table Name**: account</span></span>
    + <span data-ttu-id="a2eb2-133">**Веб-сайт**: Клиентский портал</span><span class="sxs-lookup"><span data-stu-id="a2eb2-133">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="a2eb2-134">**Область действия**: родитель</span><span class="sxs-lookup"><span data-stu-id="a2eb2-134">**Scope**: Parent</span></span>
    + <span data-ttu-id="a2eb2-135">**Привилегии**: выберите все</span><span class="sxs-lookup"><span data-stu-id="a2eb2-135">**Privileges**: Select all</span></span>
    + <span data-ttu-id="a2eb2-136">**Разрешение родительской таблицы**: подключение контакта к субъекту</span><span class="sxs-lookup"><span data-stu-id="a2eb2-136">**Parent Table Permission**: Contact to Party Connection</span></span>

6. <span data-ttu-id="a2eb2-137">Создайте и сохраните новое разрешение для подключения организации к заказу, задав следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="a2eb2-137">Create and save a new permission for the Account to Order connection, setting these parameters:</span></span>

    + <span data-ttu-id="a2eb2-138">**Имя**: Подключение организации к заказу (или по вашему выбору)</span><span class="sxs-lookup"><span data-stu-id="a2eb2-138">**Name**: Account to Order Connection (or your choice)</span></span>
    + <span data-ttu-id="a2eb2-139">**Имя таблицы**: salesorder</span><span class="sxs-lookup"><span data-stu-id="a2eb2-139">**Table Name**: salesorder</span></span>
    + <span data-ttu-id="a2eb2-140">**Веб-сайт**: Клиентский портал</span><span class="sxs-lookup"><span data-stu-id="a2eb2-140">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="a2eb2-141">**Область действия**: родитель</span><span class="sxs-lookup"><span data-stu-id="a2eb2-141">**Scope**: Parent</span></span>
    + <span data-ttu-id="a2eb2-142">**Привилегии**: выберите все</span><span class="sxs-lookup"><span data-stu-id="a2eb2-142">**Privileges**: Select all</span></span>
    + <span data-ttu-id="a2eb2-143">**Разрешение родительской таблицы**: подключение субъекта к организации</span><span class="sxs-lookup"><span data-stu-id="a2eb2-143">**Parent Table Permission**: Party to Account Connection</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
