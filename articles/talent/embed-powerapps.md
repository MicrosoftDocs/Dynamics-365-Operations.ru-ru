---
title: Внедрение приложений Power Apps в Dynamics 365 Human Resources
description: В этом разделе описан порядок решения проблемы, когда элемент меню Microsoft Power Apps исчезает из модуля "Администрирование системы".
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
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017881"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a><span data-ttu-id="16ec1-103">Внедрение приложений Power Apps в Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="16ec1-103">Embed Power Apps apps in Dynamics 365 Human Resources</span></span>

<span data-ttu-id="16ec1-104">**Выдать**</span><span class="sxs-lookup"><span data-stu-id="16ec1-104">**Issue**</span></span>

<span data-ttu-id="16ec1-105">Пункт меню **Power Apps** исчез из модуля **Администрирование системы**.</span><span class="sxs-lookup"><span data-stu-id="16ec1-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="16ec1-106">**Причина**</span><span class="sxs-lookup"><span data-stu-id="16ec1-106">**Cause**</span></span>

<span data-ttu-id="16ec1-107">Дизайн пользовательского интерфейса был изменен, и Microsoft Power Apps теперь включены в стандартную модуль персонализации.</span><span class="sxs-lookup"><span data-stu-id="16ec1-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="16ec1-108">**Приказ**</span><span class="sxs-lookup"><span data-stu-id="16ec1-108">**Resolution**</span></span>

<span data-ttu-id="16ec1-109">Был изменен способ внедрения Power Apps.</span><span class="sxs-lookup"><span data-stu-id="16ec1-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="16ec1-110">Теперь Power Apps добавляются с помощью модели персонализации.</span><span class="sxs-lookup"><span data-stu-id="16ec1-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="16ec1-111">Можно добавить Power Apps почти на все страницы Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="16ec1-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="16ec1-112">Информацию о том, как внедрить приложения Power Apps в Talent, см. раздел [Внедрение приложений Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="16ec1-112">For information about how to embed Power Apps in Talent, see [Embed Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="16ec1-113">Любой клиент Power Apps, который внедрял приложения перед изменением, должен был обновиться до новой модели.</span><span class="sxs-lookup"><span data-stu-id="16ec1-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="16ec1-114">Кнопка **Power Apps** находится в правом верхнем углу почти каждой страницы в Talent.</span><span class="sxs-lookup"><span data-stu-id="16ec1-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="16ec1-115">Эту кнопку можно использовать для вставки приложений.</span><span class="sxs-lookup"><span data-stu-id="16ec1-115">You can use this button to insert apps.</span></span>

<span data-ttu-id="16ec1-116">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="16ec1-116">Here is an example.</span></span>

1. <span data-ttu-id="16ec1-117">Выберите **Управление персоналом \> Ссылки \> Работники \> Сотрудники**.</span><span class="sxs-lookup"><span data-stu-id="16ec1-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="16ec1-118">Выберите кнопку **Power Apps**, а затем выберите **Добавить приложение из Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="16ec1-118">Select the **Power Apps** button, and then select **Add an app from Power Apps**.</span></span>

    ![Кнопка Power Apps](media/png.png)

3. <span data-ttu-id="16ec1-120">Заполните поля в диалоговом окне **Добавление приложения из Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="16ec1-120">Complete the fields in the **Add an app from Power Apps** dialog box.</span></span>

    ![Диалоговое окно добавления приложения из Power Apps](media/insert-powerapp.png)

<span data-ttu-id="16ec1-122">Можно также выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="16ec1-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="16ec1-123">В области действий на странице на вкладке **Параметры** в группе **Персонализация** выберите **Персонализировать эту страницу**.</span><span class="sxs-lookup"><span data-stu-id="16ec1-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this page**.</span></span>

    ![Настройка группы на вкладке "Параметры"](media/options.png)

    <span data-ttu-id="16ec1-125">Открывается панель инструментов персонализации.</span><span class="sxs-lookup"><span data-stu-id="16ec1-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="16ec1-126">На панели инструментов выберите **Добавить приложение из Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="16ec1-126">On the toolbar, select **Add an app from Power Apps**.</span></span>

    ![Добавьте приложение из Power Apps с помощью панели инструментов персонализации](media/powerapp-bar.png)
