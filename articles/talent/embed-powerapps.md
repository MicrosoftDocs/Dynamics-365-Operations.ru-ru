---
title: Внедрение приложений PowerApps в Dynamics 365 - Core HR
description: В этом разделе описан порядок решения проблемы, когда элемент меню PowerApps исчезает из модуля "Администрирование системы".
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4fbc24c5ceb73389b84b125eb942ac31757928aa
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008438"
---
# <a name="embed-powerapps-apps-in-core-hr"></a><span data-ttu-id="7b8b7-103">Внедрение приложений PowerApps в Core HR</span><span class="sxs-lookup"><span data-stu-id="7b8b7-103">Embed PowerApps apps in Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7b8b7-104">**Выдать**</span><span class="sxs-lookup"><span data-stu-id="7b8b7-104">**Issue**</span></span>

<span data-ttu-id="7b8b7-105">Пункт меню **PowerApps** исчез из модуля **Администрирование системы**.</span><span class="sxs-lookup"><span data-stu-id="7b8b7-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="7b8b7-106">**Причина**</span><span class="sxs-lookup"><span data-stu-id="7b8b7-106">**Cause**</span></span>

<span data-ttu-id="7b8b7-107">Дизайн пользовательского интерфейса был изменен, и Microsoft PowerApps теперь включены в стандартную модуль персонализации.</span><span class="sxs-lookup"><span data-stu-id="7b8b7-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="7b8b7-108">**Приказ**</span><span class="sxs-lookup"><span data-stu-id="7b8b7-108">**Resolution**</span></span>

<span data-ttu-id="7b8b7-109">Был изменен способ внедрения приложений PowerApps.</span><span class="sxs-lookup"><span data-stu-id="7b8b7-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="7b8b7-110">Теперь приложения PowerApps добавляются с помощью модели персонализации.</span><span class="sxs-lookup"><span data-stu-id="7b8b7-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="7b8b7-111">Можно добавить приложения PowerApps почти на все страницы Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="7b8b7-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="7b8b7-112">Информацию о том, как внедрить приложения PowerApps в Talent, см. раздел [Внедрение приложений PowerApps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="7b8b7-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="7b8b7-113">Любой клиент PowerApps, который внедрял приложения перед изменением, должен был обновиться до новой модели.</span><span class="sxs-lookup"><span data-stu-id="7b8b7-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="7b8b7-114">Кнопка **PowerApps** находится в правом верхнем углу почти каждой страницы в Talent.</span><span class="sxs-lookup"><span data-stu-id="7b8b7-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="7b8b7-115">Эту кнопку можно использовать для вставки приложения PowerApps.</span><span class="sxs-lookup"><span data-stu-id="7b8b7-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="7b8b7-116">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="7b8b7-116">Here is an example.</span></span>

1. <span data-ttu-id="7b8b7-117">Выберите **Управление персоналом \> Ссылки \> Работники \> Сотрудники**.</span><span class="sxs-lookup"><span data-stu-id="7b8b7-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="7b8b7-118">Выберите кнопку **PowerApps**, затем выберите пункт **Вставить PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="7b8b7-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![Кнопка PowerApps](media/png.png)

3. <span data-ttu-id="7b8b7-120">Заполните поля в диалоговом окне **Вставить PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="7b8b7-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Диалоговое окно "Вставить PowerApp"](media/insert-powerapp.png)

<span data-ttu-id="7b8b7-122">Можно также выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b8b7-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="7b8b7-123">В области действий на странице на вкладке **Параметры** в группе **Персонализация** выберите **Персонализировать эту форму**.</span><span class="sxs-lookup"><span data-stu-id="7b8b7-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Настройка группы на вкладке "Параметры"](media/options.png)

    <span data-ttu-id="7b8b7-125">Открывается панель инструментов персонализации.</span><span class="sxs-lookup"><span data-stu-id="7b8b7-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="7b8b7-126">На панели инструментов выберите **Вставить \> PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="7b8b7-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Вставка приложения PowerApps с помощью панели инструментов персонализации](media/powerapp-bar.png)
