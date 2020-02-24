---
title: Параметры приложения POS и языка пользователя
description: В этом разделе описано изменение настроек языка в Modern POS (MPOS) и Cloud POS.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 49bfcaa4c05ea8e6cc6bf0a8f855f2474cea35bc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023863"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a><span data-ttu-id="18912-103">Параметры приложения POS и языка пользователя</span><span class="sxs-lookup"><span data-stu-id="18912-103">Point of sale (POS) application and user language settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="18912-104">В этом разделе описано изменение настроек языка в Modern POS (MPOS) и Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="18912-104">This topic describes how to change language settings in Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="18912-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="18912-105">Overview</span></span>
<span data-ttu-id="18912-106">Modern POS (MPOS) и Cloud POS поддерживают среды, в которых языковые параметры и переводы могут варьироваться между магазинами и пользовательскими параметрами.</span><span class="sxs-lookup"><span data-stu-id="18912-106">Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="18912-107">Так, магазин может находиться в регионе, где основным языком покупателей является английский, однако некоторые сотрудники этого магазина могут предпочитать пользоваться приложением с французским переводом.</span><span class="sxs-lookup"><span data-stu-id="18912-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="18912-108">Язык данных</span><span class="sxs-lookup"><span data-stu-id="18912-108">Data language</span></span>

<span data-ttu-id="18912-109">Независимо от параметров пользователя, в MPOS и Cloud POS для определения переводов, используемых для данных, всегда будут использоваться настройки языка магазина.</span><span class="sxs-lookup"><span data-stu-id="18912-109">Regardless of the user's settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="18912-110">Это обеспечит единообразие работы всех пользователей и обслуживания клиентов.</span><span class="sxs-lookup"><span data-stu-id="18912-110">This will ensure that all users and customers will have a consistent experience.</span></span> <span data-ttu-id="18912-111">В качестве примеров данных можно привести следующие.</span><span class="sxs-lookup"><span data-stu-id="18912-111">Examples of data include:</span></span>

- <span data-ttu-id="18912-112">Товары</span><span class="sxs-lookup"><span data-stu-id="18912-112">Products</span></span>
- <span data-ttu-id="18912-113">Атрибуты и значения</span><span class="sxs-lookup"><span data-stu-id="18912-113">Attributes and values</span></span>
- <span data-ttu-id="18912-114">Названия категорий</span><span class="sxs-lookup"><span data-stu-id="18912-114">Category names</span></span>
- <span data-ttu-id="18912-115">Напечатанные или отправленные по электронной почте приходы по транзакциям</span><span class="sxs-lookup"><span data-stu-id="18912-115">Printed or emailed transaction receipts</span></span>
- <span data-ttu-id="18912-116">Названия способа оплаты</span><span class="sxs-lookup"><span data-stu-id="18912-116">Payment method names</span></span>
- <span data-ttu-id="18912-117">Сообщения строкового дисплея</span><span class="sxs-lookup"><span data-stu-id="18912-117">Line display messages</span></span>

<span data-ttu-id="18912-118">Язык магазина также будет использоваться для главного экрана входа POS, поскольку пока не выполнен вход, пользователь неизвестен.</span><span class="sxs-lookup"><span data-stu-id="18912-118">The store's language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="18912-119">Если перевод для языка магазина недоступен, POS вернется к языку компании.</span><span class="sxs-lookup"><span data-stu-id="18912-119">If a translation is not available for the store's language, the POS will revert to the company's language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="18912-120">Конфигурация настройки языка магазина</span><span class="sxs-lookup"><span data-stu-id="18912-120">Configuring the store's language setting</span></span>

<span data-ttu-id="18912-121">Язык магазина настраивается в разделе **Все магазины** на странице **Магазин** в меню **Общие &gt; Региональные параметры &gt; Язык**.</span><span class="sxs-lookup"><span data-stu-id="18912-121">The store's language setting is set from **All stores** on the **Store** page under **General &gt; Regional Settings &gt; Language**.</span></span> <span data-ttu-id="18912-122">Используйте раскрывающийся список, чтобы выбрать язык для каждого магазина.</span><span class="sxs-lookup"><span data-stu-id="18912-122">Use the drop-down list to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="18912-123">Язык пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="18912-123">User interface language</span></span>

<span data-ttu-id="18912-124">Настройка языка пользователя POS определяет переводы, используемые в пользовательском интерфейсе приложения.</span><span class="sxs-lookup"><span data-stu-id="18912-124">The POS user's language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="18912-125">Сюда относятся все метки, меню и списки, которые не относятся к данным.</span><span class="sxs-lookup"><span data-stu-id="18912-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="18912-126">Одно исключение — это текст, отображаемый в сетках кнопок POS.</span><span class="sxs-lookup"><span data-stu-id="18912-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="18912-127">Сетки кнопок не поддерживают переводы, поэтому текст на них всегда будет отображаться так, как определен на кнопке.</span><span class="sxs-lookup"><span data-stu-id="18912-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="18912-128">Чтобы обеспечить поддержку перевода кнопок, потребуется копировать и обслуживать отдельные сетки кнопок и назначить их соответствующим пользователям.</span><span class="sxs-lookup"><span data-stu-id="18912-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="18912-129">Конфигурация настройки языка пользователя</span><span class="sxs-lookup"><span data-stu-id="18912-129">Configuring the user's language setting</span></span>

<span data-ttu-id="18912-130">Язык пользователя POS настраивается в разделе **Все рабочие** на странице **Рабочий** в меню **Retail и Commerce &gt; Язык**.</span><span class="sxs-lookup"><span data-stu-id="18912-130">The POS user's language setting is set from **All workers** on the **Worker** page under **Retail and Commerce &gt; Language**.</span></span> <span data-ttu-id="18912-131">Язык не задается на главной вкладке профиля. Эта настройка не используется POS.</span><span class="sxs-lookup"><span data-stu-id="18912-131">It is not set on the main Profile tab. This setting is not used by POS.</span></span> <span data-ttu-id="18912-132">Если язык пользователя не задан или задан как язык, для которого недоступны переводы, POS перейдет к использованию языка магазина.</span><span class="sxs-lookup"><span data-stu-id="18912-132">If the user's language is not set or it is set to a language where translations are not available, the POS will revert to the store's language.</span></span>

|             | <span data-ttu-id="18912-133">Язык пользовательского интерфейса  </span><span class="sxs-lookup"><span data-stu-id="18912-133">UI language</span></span>                | <span data-ttu-id="18912-134">Язык данных (продукты, форматы поступлений, строковый дисплей и т. д.)</span><span class="sxs-lookup"><span data-stu-id="18912-134">Data language (products, receipt formats, line display, etc.)</span></span> |
|-------------|----------------------------|---------------------------------------------------------------|
| <span data-ttu-id="18912-135">**Компания**</span><span class="sxs-lookup"><span data-stu-id="18912-135">**Company**</span></span> | <span data-ttu-id="18912-136">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="18912-136">Default</span></span>                    | <span data-ttu-id="18912-137">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="18912-137">Default</span></span>                                                       |
| <span data-ttu-id="18912-138">**Магазин**</span><span class="sxs-lookup"><span data-stu-id="18912-138">**Store**</span></span>   | <span data-ttu-id="18912-139">Переопределяет компанию</span><span class="sxs-lookup"><span data-stu-id="18912-139">Overrides company</span></span>          | <span data-ttu-id="18912-140">Переопределяет компанию</span><span class="sxs-lookup"><span data-stu-id="18912-140">Overrides company</span></span>                                             |
| <span data-ttu-id="18912-141">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="18912-141">**User**</span></span>    | <span data-ttu-id="18912-142">Переопределяет магазин или компанию</span><span class="sxs-lookup"><span data-stu-id="18912-142">Overrides store or company</span></span> | <span data-ttu-id="18912-143">Никогда</span><span class="sxs-lookup"><span data-stu-id="18912-143">Never</span></span>                                                         |
