---
title: "Настройки приложения POS и языка пользователя"
description: "В этом разделе описано изменение настроек языка в Retail Modern POS (MPOS) и Cloud POS."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cabb63aea0da4b264aec8e0cc4d43b3e1014e71b
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="pos-application-and-user-language-settings"></a><span data-ttu-id="ad828-103">Настройки приложения POS и языка пользователя</span><span class="sxs-lookup"><span data-stu-id="ad828-103">POS application and user language settings</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="ad828-104">В этом разделе описано изменение настроек языка в Retail Modern POS (MPOS) и Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="ad828-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

<a name="overview"></a><span data-ttu-id="ad828-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="ad828-105">Overview</span></span>
========

<span data-ttu-id="ad828-106">Retail Modern POS (MPOS) и Cloud POS поддерживают среды, в которых языковые параметры и переводы могут варьироваться между магазинами и пользовательскими параметрами.</span><span class="sxs-lookup"><span data-stu-id="ad828-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="ad828-107">Так, магазин может находиться в регионе, где основным языком покупателей является английский, однако некоторые сотрудники этого магазина могут предпочитать пользоваться приложением с французским переводом.</span><span class="sxs-lookup"><span data-stu-id="ad828-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="ad828-108">Язык данных</span><span class="sxs-lookup"><span data-stu-id="ad828-108">Data language</span></span>
<span data-ttu-id="ad828-109">Независимо от параметров пользователя, в MPOS и Cloud POS для определения переводов, используемых для данных, всегда будут использоваться настройки языка магазина.</span><span class="sxs-lookup"><span data-stu-id="ad828-109">Regardless of the user’s settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="ad828-110">Это обеспечит единообразие работы всех пользователей и обслуживания клиентов.</span><span class="sxs-lookup"><span data-stu-id="ad828-110">This will ensure that all users and customers will have a consistent experience.</span></span>  <span data-ttu-id="ad828-111">В качестве примеров данных можно привести следующие.</span><span class="sxs-lookup"><span data-stu-id="ad828-111">Examples of data include:</span></span>

-   <span data-ttu-id="ad828-112">Товары</span><span class="sxs-lookup"><span data-stu-id="ad828-112">Products</span></span>
-   <span data-ttu-id="ad828-113">Атрибуты и значения</span><span class="sxs-lookup"><span data-stu-id="ad828-113">Attributes and values</span></span>
-   <span data-ttu-id="ad828-114">Названия категорий</span><span class="sxs-lookup"><span data-stu-id="ad828-114">Category names</span></span>
-   <span data-ttu-id="ad828-115">Напечатанные или отправленные по электронной почте приходы по транзакциям</span><span class="sxs-lookup"><span data-stu-id="ad828-115">Printed or emailed transaction receipts</span></span>
-   <span data-ttu-id="ad828-116">Названия способа оплаты</span><span class="sxs-lookup"><span data-stu-id="ad828-116">Payment method names</span></span>
-   <span data-ttu-id="ad828-117">Сообщения строкового дисплея</span><span class="sxs-lookup"><span data-stu-id="ad828-117">Line display messages</span></span>

<span data-ttu-id="ad828-118">Язык магазина также будет использоваться для главного экрана входа POS, поскольку пока не выполнен вход, пользователь неизвестен.</span><span class="sxs-lookup"><span data-stu-id="ad828-118">The store’s language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="ad828-119">Если перевод для языка магазина недоступен, POS вернется к языку компании.</span><span class="sxs-lookup"><span data-stu-id="ad828-119">If a translation is not available for the store’s language, the POS will revert to the company’s language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="ad828-120">Конфигурация настройки языка магазина</span><span class="sxs-lookup"><span data-stu-id="ad828-120">Configuring the store’s language setting</span></span>

<span data-ttu-id="ad828-121">Язык магазина настраивается в разделе **Все розничные магазины** на странице **Розничный магазин** в меню **Общие &gt; Региональные параметры &gt; Язык.</span><span class="sxs-lookup"><span data-stu-id="ad828-121">The store’s language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language.</span></span> <span data-ttu-id="ad828-122">**Используйте раскрывающийся список, чтобы выбрать язык для каждого магазина.</span><span class="sxs-lookup"><span data-stu-id="ad828-122">**Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="ad828-123">Язык пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="ad828-123">User interface language</span></span>
<span data-ttu-id="ad828-124">Настройка языка пользователя POS определяет переводы, используемые в пользовательском интерфейсе приложения.</span><span class="sxs-lookup"><span data-stu-id="ad828-124">The POS user’s language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="ad828-125">Сюда относятся все метки, меню и списки, которые не относятся к данным.</span><span class="sxs-lookup"><span data-stu-id="ad828-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="ad828-126">Одно исключение — это текст, отображаемый в сетках кнопок POS.</span><span class="sxs-lookup"><span data-stu-id="ad828-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="ad828-127">Сетки кнопок не поддерживают переводы, поэтому текст на них всегда будет отображаться так, как определен на кнопке.</span><span class="sxs-lookup"><span data-stu-id="ad828-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="ad828-128">Чтобы обеспечить поддержку перевода кнопок, потребуется копировать и обслуживать отдельные сетки кнопок и назначить их соответствующим пользователям.</span><span class="sxs-lookup"><span data-stu-id="ad828-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="ad828-129">Конфигурация настройки языка пользователя</span><span class="sxs-lookup"><span data-stu-id="ad828-129">Configuring the user’s language setting</span></span>

<span data-ttu-id="ad828-130">Язык пользователя POS настраивается в разделе **Все рабочие** на странице **Рабочий** в меню **Розница &gt; Язык**.</span><span class="sxs-lookup"><span data-stu-id="ad828-130">The POS user’s language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span>  <span data-ttu-id="ad828-131">Язык не задается на главной вкладке профиля. Эта настройка не используется POS.</span><span class="sxs-lookup"><span data-stu-id="ad828-131">It is not set on the main Profile tab.  This setting is not used by POS.</span></span> <span data-ttu-id="ad828-132">Если язык пользователя не задан или задан как язык, для которого недоступны переводы, POS перейдет к использованию языка магазина.</span><span class="sxs-lookup"><span data-stu-id="ad828-132">If the user’s language is not set or it is set to a language where translations are not available, the POS will revert to the store’s language.</span></span>  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ad828-133">** **</span><span class="sxs-lookup"><span data-stu-id="ad828-133">** **</span></span>       | <span data-ttu-id="ad828-134">**Язык пользовательского интерфейса** ** **</span><span class="sxs-lookup"><span data-stu-id="ad828-134">**UI language** ** **</span></span>      | <span data-ttu-id="ad828-135">**Язык данных (продукты, форматы поступлений, строковый дисплей и т. д.)**</span><span class="sxs-lookup"><span data-stu-id="ad828-135">**Data language (products, receipt formats, line display, etc.)**</span></span> |
| <span data-ttu-id="ad828-136">**Компания**</span><span class="sxs-lookup"><span data-stu-id="ad828-136">**Company**</span></span> | <span data-ttu-id="ad828-137">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad828-137">Default</span></span>                    | <span data-ttu-id="ad828-138">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad828-138">Default</span></span>                                                           |
| <span data-ttu-id="ad828-139">**Магазин**</span><span class="sxs-lookup"><span data-stu-id="ad828-139">**Store**</span></span>   | <span data-ttu-id="ad828-140">Переопределяет компанию</span><span class="sxs-lookup"><span data-stu-id="ad828-140">Overrides company</span></span>          | <span data-ttu-id="ad828-141">Переопределяет компанию</span><span class="sxs-lookup"><span data-stu-id="ad828-141">Overrides company</span></span>                                                 |
| <span data-ttu-id="ad828-142">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="ad828-142">**User**</span></span>    | <span data-ttu-id="ad828-143">Переопределяет магазин или компанию</span><span class="sxs-lookup"><span data-stu-id="ad828-143">Overrides store or company</span></span> | <span data-ttu-id="ad828-144">Никогда</span><span class="sxs-lookup"><span data-stu-id="ad828-144">Never</span></span>                                                             |





