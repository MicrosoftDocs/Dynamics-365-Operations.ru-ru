---
title: Внедрение приложений PowerApps в Core HR
description: В этом разделе описан порядок решения проблемы, когда элемент меню PowerApps исчезает из модуля "Администрирование системы".
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 197b553f0b202ee29ad42274e2c0e03446ec782c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "305977"
---
# <a name="embed-powerapps-apps-in-core-hr"></a><span data-ttu-id="fb75d-103">Внедрение приложений PowerApps в Core HR</span><span class="sxs-lookup"><span data-stu-id="fb75d-103">Embed PowerApps apps in Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fb75d-104">**Расход**</span><span class="sxs-lookup"><span data-stu-id="fb75d-104">**Issue**</span></span>

<span data-ttu-id="fb75d-105">Пункт меню **PowerApps** исчез из модуля **Администрирование системы**.</span><span class="sxs-lookup"><span data-stu-id="fb75d-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="fb75d-106">**Причина**</span><span class="sxs-lookup"><span data-stu-id="fb75d-106">**Cause**</span></span>

<span data-ttu-id="fb75d-107">Дизайн пользовательского интерфейса был изменен, и Microsoft PowerApps теперь включены в стандартную модуль персонализации.</span><span class="sxs-lookup"><span data-stu-id="fb75d-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="fb75d-108">**Разрешение**</span><span class="sxs-lookup"><span data-stu-id="fb75d-108">**Resolution**</span></span>

<span data-ttu-id="fb75d-109">Был изменен способ внедрения приложений PowerApps.</span><span class="sxs-lookup"><span data-stu-id="fb75d-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="fb75d-110">Теперь приложения PowerApps добавляются с помощью модели персонализации.</span><span class="sxs-lookup"><span data-stu-id="fb75d-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="fb75d-111">Можно добавить приложения PowerApps почти на все страницы Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="fb75d-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 for Talent.</span></span>

<span data-ttu-id="fb75d-112">Информацию о том, как внедрить приложения PowerApps в Talent, см. раздел [Внедрение приложений PowerApps](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="fb75d-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="fb75d-113">Любой клиент PowerApps, который внедрял приложения перед изменением, должен был обновиться до новой модели.</span><span class="sxs-lookup"><span data-stu-id="fb75d-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="fb75d-114">Кнопка **PowerApps** находится в правом верхнем углу почти каждой страницы в Talent.</span><span class="sxs-lookup"><span data-stu-id="fb75d-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="fb75d-115">Эту кнопку можно использовать для вставки приложения PowerApps.</span><span class="sxs-lookup"><span data-stu-id="fb75d-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="fb75d-116">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="fb75d-116">Here is an example.</span></span>

1. <span data-ttu-id="fb75d-117">Выберите **Управление персоналом \> Ссылки \> Работники \> Сотрудники**.</span><span class="sxs-lookup"><span data-stu-id="fb75d-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="fb75d-118">Выберите кнопку **PowerApps**, затем выберите пункт **Вставить PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="fb75d-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![Кнопка PowerApps](media/png.png)

3. <span data-ttu-id="fb75d-120">Заполните поля в диалоговом окне **Вставить PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="fb75d-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Диалоговое окно "Вставить PowerApp"](media/insert-powerapp.png)

<span data-ttu-id="fb75d-122">Можно также выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fb75d-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="fb75d-123">В области действий на странице на вкладке **Параметры** в группе **Персонализация** выберите **Персонализировать эту форму**.</span><span class="sxs-lookup"><span data-stu-id="fb75d-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Настройка группы на вкладке "Параметры"](media/options.png)

    <span data-ttu-id="fb75d-125">Открывается панель инструментов персонализации.</span><span class="sxs-lookup"><span data-stu-id="fb75d-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="fb75d-126">На панели инструментов выберите **Вставить \> PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="fb75d-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Вставка приложения PowerApps с помощью панели инструментов персонализации](media/powerapp-bar.png)
