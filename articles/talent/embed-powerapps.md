---
title: Внедрение приложений Power Apps в Dynamics 365 - Core HR
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
ms.openlocfilehash: 6d1b7f1dd71e6bcbf10c4d91fe33e9494b041a2c
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830217"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="3f19d-103">Внедрение приложений Power Apps в Dynamics 365 - Core HR</span><span class="sxs-lookup"><span data-stu-id="3f19d-103">Embed Power Apps apps in Dynamics 365 - Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f19d-104">**Выдать**</span><span class="sxs-lookup"><span data-stu-id="3f19d-104">**Issue**</span></span>

<span data-ttu-id="3f19d-105">Пункт меню **Power Apps** исчез из модуля **Администрирование системы**.</span><span class="sxs-lookup"><span data-stu-id="3f19d-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="3f19d-106">**Причина**</span><span class="sxs-lookup"><span data-stu-id="3f19d-106">**Cause**</span></span>

<span data-ttu-id="3f19d-107">Дизайн пользовательского интерфейса был изменен, и Microsoft Power Apps теперь включены в стандартную модуль персонализации.</span><span class="sxs-lookup"><span data-stu-id="3f19d-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="3f19d-108">**Приказ**</span><span class="sxs-lookup"><span data-stu-id="3f19d-108">**Resolution**</span></span>

<span data-ttu-id="3f19d-109">Был изменен способ внедрения Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3f19d-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="3f19d-110">Теперь Power Apps добавляются с помощью модели персонализации.</span><span class="sxs-lookup"><span data-stu-id="3f19d-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="3f19d-111">Можно добавить Power Apps почти на все страницы Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="3f19d-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="3f19d-112">Информацию о том, как внедрить приложения Power Apps в Talent, см. раздел [Внедрение приложений Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="3f19d-112">For information about how to embed Power Apps in Talent, see [Embed Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="3f19d-113">Любой клиент Power Apps, который внедрял приложения перед изменением, должен был обновиться до новой модели.</span><span class="sxs-lookup"><span data-stu-id="3f19d-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="3f19d-114">Кнопка **Power Apps** находится в правом верхнем углу почти каждой страницы в Talent.</span><span class="sxs-lookup"><span data-stu-id="3f19d-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="3f19d-115">Эту кнопку можно использовать для вставки Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3f19d-115">You can use this button to insert Power Apps.</span></span>

<span data-ttu-id="3f19d-116">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="3f19d-116">Here is an example.</span></span>

1. <span data-ttu-id="3f19d-117">Выберите **Управление персоналом \> Ссылки \> Работники \> Сотрудники**.</span><span class="sxs-lookup"><span data-stu-id="3f19d-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="3f19d-118">Выберите кнопку **Power Apps**, затем выберите пункт **Вставить PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="3f19d-118">Select the **Power Apps** button, and then select **Insert a PowerApp**.</span></span>

    ![Кнопка Power Apps](media/png.png)

3. <span data-ttu-id="3f19d-120">Заполните поля в диалоговом окне **Вставить PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="3f19d-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Диалоговое окно "Вставить PowerApp"](media/insert-powerapp.png)

<span data-ttu-id="3f19d-122">Можно также выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3f19d-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="3f19d-123">В области действий на странице на вкладке **Параметры** в группе **Персонализация** выберите **Персонализировать эту форму**.</span><span class="sxs-lookup"><span data-stu-id="3f19d-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Настройка группы на вкладке "Параметры"](media/options.png)

    <span data-ttu-id="3f19d-125">Открывается панель инструментов персонализации.</span><span class="sxs-lookup"><span data-stu-id="3f19d-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="3f19d-126">На панели инструментов выберите **Вставить \> PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="3f19d-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Вставка приложения Power Apps с помощью панели инструментов персонализации](media/powerapp-bar.png)
