---
title: Создание юридических лиц
description: В этом разделе описывается создание юридических лиц в Microsoft Dynamics 365 Commerce, которые должны быть созданы и настроены перед созданием каналов.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 28cbcc42505f1dc90c420adc812735841541c8e0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415202"
---
# <a name="create-legal-entities"></a><span data-ttu-id="5fb15-103">Создание юридических лиц</span><span class="sxs-lookup"><span data-stu-id="5fb15-103">Create legal entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5fb15-104">В этом разделе описывается создание юридических лиц в Microsoft Dynamics 365 Commerce, которые должны быть созданы и настроены перед созданием каналов.</span><span class="sxs-lookup"><span data-stu-id="5fb15-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

## <a name="overview"></a><span data-ttu-id="5fb15-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="5fb15-105">Overview</span></span>

<span data-ttu-id="5fb15-106">Юридическое лицо — это организация, имеющая зарегистрированную или узаконенную правовую структуру.</span><span class="sxs-lookup"><span data-stu-id="5fb15-106">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="5fb15-107">Юридические лица могут заключать юридические соглашения и обязаны подготавливать отчетность по результатам своей деятельности.</span><span class="sxs-lookup"><span data-stu-id="5fb15-107">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="5fb15-108">Компания — это тип юридического лица.</span><span class="sxs-lookup"><span data-stu-id="5fb15-108">A company is a type of legal entity.</span></span> <span data-ttu-id="5fb15-109">В настоящее время компании являются единственным доступным для создания типом юридического лица. Каждое юридическое лицо имеет свой ИД компании.</span><span class="sxs-lookup"><span data-stu-id="5fb15-109">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="5fb15-110">Эта связь существует, поскольку некоторые функциональные области программы используется код компании или код *DataAreaId* в своих моделях данных.</span><span class="sxs-lookup"><span data-stu-id="5fb15-110">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="5fb15-111">В этих функциональных областях компании используются в качестве границы для обеспечения безопасности данных.</span><span class="sxs-lookup"><span data-stu-id="5fb15-111">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="5fb15-112">Пользователи могут осуществлять доступ только к данным компании, вход в систему которой они выполнили.</span><span class="sxs-lookup"><span data-stu-id="5fb15-112">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="5fb15-113">При создании канала необходимо указать юридическое лицо, к которому относится данный канал.</span><span class="sxs-lookup"><span data-stu-id="5fb15-113">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="5fb15-114">Создание юридического лица</span><span class="sxs-lookup"><span data-stu-id="5fb15-114">Create a new legal entity</span></span>

<span data-ttu-id="5fb15-115">Чтобы создать юридическое лицо в Dynamics 365 Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fb15-115">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5fb15-116">В области переходов перейдите **Модули \> Настройка центрального офиса \> Юридические лица**.</span><span class="sxs-lookup"><span data-stu-id="5fb15-116">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="5fb15-117">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="5fb15-117">On the action pane, select **New**.</span></span> <span data-ttu-id="5fb15-118">В правой части появится **Новое юридическое лицо**.</span><span class="sxs-lookup"><span data-stu-id="5fb15-118">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="5fb15-119">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5fb15-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="5fb15-120">В поле **Компания** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5fb15-120">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="5fb15-121">В поле **Страна/регион** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="5fb15-121">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="5fb15-122">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5fb15-122">Select **OK**.</span></span> 

   ![Создание юридического лица](media/legal-entities.png)

1. <span data-ttu-id="5fb15-124">В разделе **Общее** укажите следующие общие сведения о юридическом лице:</span><span class="sxs-lookup"><span data-stu-id="5fb15-124">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="5fb15-125">Введите Краткое наименование, если Краткое наименование необходимо.</span><span class="sxs-lookup"><span data-stu-id="5fb15-125">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="5fb15-126">Краткое наименование — это альтернативное имя, которое можно использовать для поиска этого юридического лица.</span><span class="sxs-lookup"><span data-stu-id="5fb15-126">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="5fb15-127">Выберите используется ли это юридическое лицо как консолидированная компания.</span><span class="sxs-lookup"><span data-stu-id="5fb15-127">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="5fb15-128">Выберите используется ли это юридическое лицо как Компания элиминирования.</span><span class="sxs-lookup"><span data-stu-id="5fb15-128">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="5fb15-129">Выберите **язык по умолчанию** для юридического лица.</span><span class="sxs-lookup"><span data-stu-id="5fb15-129">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="5fb15-130">Выберите **часовой пояс** для юридического лица.</span><span class="sxs-lookup"><span data-stu-id="5fb15-130">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="5fb15-131">В разделе **Адреса** выберите **Изменить**, чтобы ввести информацию об адресе, например название улицы, номер дома, почтовый индекс и название города.</span><span class="sxs-lookup"><span data-stu-id="5fb15-131">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="5fb15-132">В разделе **Контактная информация** введите сведения о методах связи, например адреса электронной почты, URL-адреса и номера телефонов.</span><span class="sxs-lookup"><span data-stu-id="5fb15-132">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="5fb15-133">В разделе **Предусмотренная отчетность** введите регистрационные номера, которые используются для предусмотренной отчетности.</span><span class="sxs-lookup"><span data-stu-id="5fb15-133">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="5fb15-134">В разделе **Регистрационные номера** введите любую информацию, требуемую юридическим лицом.</span><span class="sxs-lookup"><span data-stu-id="5fb15-134">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="5fb15-135">В разделе **Сведения о банковском счете** введите банковские счета и внутренние номера для юридического лица.</span><span class="sxs-lookup"><span data-stu-id="5fb15-135">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="5fb15-136">В разделе **Внешняя торговля и логистика** введите сведения об отгрузке для юридического лица.</span><span class="sxs-lookup"><span data-stu-id="5fb15-136">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="5fb15-137">В разделе **Номерные серии** можно просмотреть номерные серии, которые связаны с юридическим лицом.</span><span class="sxs-lookup"><span data-stu-id="5fb15-137">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="5fb15-138">Это значение будет пустым.</span><span class="sxs-lookup"><span data-stu-id="5fb15-138">This will be empty to start with.</span></span>
1. <span data-ttu-id="5fb15-139">В разделе **Изображение на панели мониторинга** просмотрите или измените изображение эмблемы или панели мониторинга, связанной с юридическим лицом.</span><span class="sxs-lookup"><span data-stu-id="5fb15-139">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="5fb15-140">В разделе **Налоговая регистрация** введите регистрационные номера, которые используются для отчета в налоговые органы.</span><span class="sxs-lookup"><span data-stu-id="5fb15-140">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="5fb15-141">В разделе **Налог по форме 1099** введите сведения 1099 для юридического лица.</span><span class="sxs-lookup"><span data-stu-id="5fb15-141">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="5fb15-142">В разделе **Информация о налогах** введите информацию о налогах для юридического лица.</span><span class="sxs-lookup"><span data-stu-id="5fb15-142">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="5fb15-143">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5fb15-143">Select **Save**.</span></span>

<span data-ttu-id="5fb15-144">На следующем рисунке показаны сведения с примером юридического лица.</span><span class="sxs-lookup"><span data-stu-id="5fb15-144">The following image shows details of an example legal entity.</span></span>

![Общий раздел юридического лица](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="5fb15-146">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5fb15-146">Additional resources</span></span>

[<span data-ttu-id="5fb15-147">Обзор организаций и организационных иерархий</span><span class="sxs-lookup"><span data-stu-id="5fb15-147">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="5fb15-148">Планирование организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="5fb15-148">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="5fb15-149">Организационные иерархии</span><span class="sxs-lookup"><span data-stu-id="5fb15-149">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="5fb15-150">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="5fb15-150">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="5fb15-151">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="5fb15-151">Channel setup prerequisites</span></span>](channels-prerequisites.md)
