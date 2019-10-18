---
title: Talent отсутствует среди приложений Microsoft Dynamics 365 (Common Data Service 1.0)
description: В этом разделе объясняется, что делать, если клиент не видит приложение Microsoft Dynamics 365 Talent среди приложений Microsoft Dynamics 365.
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
ms.openlocfilehash: 956af80a8ab2f454d9f523d3c74dda754ef0f793
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009384"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a><span data-ttu-id="b77e5-103">Talent отсутствует среди приложений Microsoft Dynamics 365 (Common Data Service 1.0)</span><span class="sxs-lookup"><span data-stu-id="b77e5-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (Common Data Service 1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b77e5-104">**Выдать**</span><span class="sxs-lookup"><span data-stu-id="b77e5-104">**Issue**</span></span>

<span data-ttu-id="b77e5-105">Клиент не видит приложения Microsoft Dynamics 365 Talent среди приложений Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b77e5-105">The customer doesn't see the Microsoft Dynamics 365 Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="b77e5-106">**Разрешение**</span><span class="sxs-lookup"><span data-stu-id="b77e5-106">**Resolution**</span></span>

<span data-ttu-id="b77e5-107">Пользователь должен быть добавлен к роли "Создатель среды" для среды в Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="b77e5-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="b77e5-108">Пользователь-администратор, имеющий лицензию PowerApps Plan 2, должен открыть [портал администратора PowerApps](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="b77e5-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="b77e5-109">Выберите **Среды**и выберите правильную среду для Talent.</span><span class="sxs-lookup"><span data-stu-id="b77e5-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="b77e5-110">На вкладке **Безопасность** на вкладке **Роли среды** выберите **Создатель среды**.</span><span class="sxs-lookup"><span data-stu-id="b77e5-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Вкладка ролей среды](media/environment-roles.png)

4. <span data-ttu-id="b77e5-112">На вкладке **Пользователи** добавьте пользователя или вашу организацию.</span><span class="sxs-lookup"><span data-stu-id="b77e5-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Вкладка пользователей](media/environment-maker.png)

5. <span data-ttu-id="b77e5-114">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b77e5-114">Select **Save**.</span></span>
6. <span data-ttu-id="b77e5-115">Теперь пользователь должен выполнить вход в [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="b77e5-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="b77e5-116">Выберите **Синхронизация**, чтобы обновить приложения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b77e5-116">Select **Sync** to update the user apps.</span></span>

    ![Кнопка "Синхронизация"](media/get-more.png)

    <span data-ttu-id="b77e5-118">По завершении синхронизации Talent появится на домашней странице.</span><span class="sxs-lookup"><span data-stu-id="b77e5-118">After synchronization is completed, Talent will appear on the home page.</span></span>
