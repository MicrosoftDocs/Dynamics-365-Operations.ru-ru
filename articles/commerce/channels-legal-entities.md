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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 016b67631a53139d12d65dfaf594f49b030326b1
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478220"
---
# <a name="create-legal-entities"></a><span data-ttu-id="78631-103">Создание юридических лиц</span><span class="sxs-lookup"><span data-stu-id="78631-103">Create legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="78631-104">В этом разделе описывается создание юридических лиц в Microsoft Dynamics 365 Commerce, которые должны быть созданы и настроены перед созданием каналов.</span><span class="sxs-lookup"><span data-stu-id="78631-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

<span data-ttu-id="78631-105">Юридическое лицо — это организация, имеющая зарегистрированную или узаконенную правовую структуру.</span><span class="sxs-lookup"><span data-stu-id="78631-105">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="78631-106">Юридические лица могут заключать юридические соглашения и обязаны подготавливать отчетность по результатам своей деятельности.</span><span class="sxs-lookup"><span data-stu-id="78631-106">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="78631-107">Компания — это тип юридического лица.</span><span class="sxs-lookup"><span data-stu-id="78631-107">A company is a type of legal entity.</span></span> <span data-ttu-id="78631-108">В настоящее время компании являются единственным доступным для создания типом юридического лица. Каждое юридическое лицо имеет свой ИД компании.</span><span class="sxs-lookup"><span data-stu-id="78631-108">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="78631-109">Эта связь существует, поскольку некоторые функциональные области программы используется код компании или код *DataAreaId* в своих моделях данных.</span><span class="sxs-lookup"><span data-stu-id="78631-109">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="78631-110">В этих функциональных областях компании используются в качестве границы для обеспечения безопасности данных.</span><span class="sxs-lookup"><span data-stu-id="78631-110">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="78631-111">Пользователи могут осуществлять доступ только к данным компании, вход в систему которой они выполнили.</span><span class="sxs-lookup"><span data-stu-id="78631-111">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="78631-112">При создании канала необходимо указать юридическое лицо, к которому относится данный канал.</span><span class="sxs-lookup"><span data-stu-id="78631-112">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="78631-113">Создание юридического лица</span><span class="sxs-lookup"><span data-stu-id="78631-113">Create a new legal entity</span></span>

<span data-ttu-id="78631-114">Чтобы создать юридическое лицо в Dynamics 365 Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="78631-114">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="78631-115">В области переходов перейдите **Модули \> Настройка центрального офиса \> Юридические лица**.</span><span class="sxs-lookup"><span data-stu-id="78631-115">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="78631-116">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="78631-116">On the action pane, select **New**.</span></span> <span data-ttu-id="78631-117">В правой части появится **Новое юридическое лицо**.</span><span class="sxs-lookup"><span data-stu-id="78631-117">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="78631-118">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="78631-118">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="78631-119">В поле **Компания** введите значение.</span><span class="sxs-lookup"><span data-stu-id="78631-119">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="78631-120">В поле **Страна/регион** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="78631-120">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="78631-121">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78631-121">Select **OK**.</span></span> 

   ![Создание юридического лица](media/legal-entities.png)

1. <span data-ttu-id="78631-123">В разделе **Общее** укажите следующие общие сведения о юридическом лице:</span><span class="sxs-lookup"><span data-stu-id="78631-123">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="78631-124">Введите Краткое наименование, если Краткое наименование необходимо.</span><span class="sxs-lookup"><span data-stu-id="78631-124">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="78631-125">Краткое наименование — это альтернативное имя, которое можно использовать для поиска этого юридического лица.</span><span class="sxs-lookup"><span data-stu-id="78631-125">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="78631-126">Выберите используется ли это юридическое лицо как консолидированная компания.</span><span class="sxs-lookup"><span data-stu-id="78631-126">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="78631-127">Выберите используется ли это юридическое лицо как Компания элиминирования.</span><span class="sxs-lookup"><span data-stu-id="78631-127">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="78631-128">Выберите **язык по умолчанию** для юридического лица.</span><span class="sxs-lookup"><span data-stu-id="78631-128">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="78631-129">Выберите **часовой пояс** для юридического лица.</span><span class="sxs-lookup"><span data-stu-id="78631-129">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="78631-130">В разделе **Адреса** выберите **Изменить**, чтобы ввести информацию об адресе, например название улицы, номер дома, почтовый индекс и название города.</span><span class="sxs-lookup"><span data-stu-id="78631-130">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="78631-131">В разделе **Контактная информация** введите сведения о методах связи, например адреса электронной почты, URL-адреса и номера телефонов.</span><span class="sxs-lookup"><span data-stu-id="78631-131">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="78631-132">В разделе **Предусмотренная отчетность** введите регистрационные номера, которые используются для предусмотренной отчетности.</span><span class="sxs-lookup"><span data-stu-id="78631-132">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="78631-133">В разделе **Регистрационные номера** введите любую информацию, требуемую юридическим лицом.</span><span class="sxs-lookup"><span data-stu-id="78631-133">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="78631-134">В разделе **Сведения о банковском счете** введите банковские счета и внутренние номера для юридического лица.</span><span class="sxs-lookup"><span data-stu-id="78631-134">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="78631-135">В разделе **Внешняя торговля и логистика** введите сведения об отгрузке для юридического лица.</span><span class="sxs-lookup"><span data-stu-id="78631-135">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="78631-136">В разделе **Номерные серии** можно просмотреть номерные серии, которые связаны с юридическим лицом.</span><span class="sxs-lookup"><span data-stu-id="78631-136">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="78631-137">Это значение будет пустым.</span><span class="sxs-lookup"><span data-stu-id="78631-137">This will be empty to start with.</span></span>
1. <span data-ttu-id="78631-138">В разделе **Изображение на панели мониторинга** просмотрите или измените изображение эмблемы или панели мониторинга, связанной с юридическим лицом.</span><span class="sxs-lookup"><span data-stu-id="78631-138">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="78631-139">В разделе **Налоговая регистрация** введите регистрационные номера, которые используются для отчета в налоговые органы.</span><span class="sxs-lookup"><span data-stu-id="78631-139">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="78631-140">В разделе **Налог по форме 1099** введите сведения 1099 для юридического лица.</span><span class="sxs-lookup"><span data-stu-id="78631-140">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="78631-141">В разделе **Информация о налогах** введите информацию о налогах для юридического лица.</span><span class="sxs-lookup"><span data-stu-id="78631-141">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="78631-142">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="78631-142">Select **Save**.</span></span>

<span data-ttu-id="78631-143">На следующем рисунке показаны сведения с примером юридического лица.</span><span class="sxs-lookup"><span data-stu-id="78631-143">The following image shows details of an example legal entity.</span></span>

![Общий раздел юридического лица](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="78631-145">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="78631-145">Additional resources</span></span>

[<span data-ttu-id="78631-146">Обзор организаций и организационных иерархий</span><span class="sxs-lookup"><span data-stu-id="78631-146">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="78631-147">Планирование организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="78631-147">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="78631-148">Организационные иерархии</span><span class="sxs-lookup"><span data-stu-id="78631-148">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="78631-149">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="78631-149">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="78631-150">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="78631-150">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
