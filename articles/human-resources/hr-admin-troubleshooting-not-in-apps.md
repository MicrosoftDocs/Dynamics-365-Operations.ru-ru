---
title: Human Resources отсутствует в списке приложений Microsoft Dynamics 365
description: В этой статье объясняется, что делать, если клиент не видит приложение Microsoft Dynamics 365 Human Resources среди приложений Microsoft Dynamics 365.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cbf47b4673e1c97965bba7728e5669b7639c4d56
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431092"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="e7f6a-103">Human Resources отсутствует в списке приложений Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="e7f6a-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

<span data-ttu-id="e7f6a-104">**Выдать**</span><span class="sxs-lookup"><span data-stu-id="e7f6a-104">**Issue**</span></span>

<span data-ttu-id="e7f6a-105">Клиент не видит Dynamics 365 Human Resources среди приложений Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="e7f6a-106">**Приказ**</span><span class="sxs-lookup"><span data-stu-id="e7f6a-106">**Resolution**</span></span>

<span data-ttu-id="e7f6a-107">Пользователь должен быть добавлен к роли "Создатель среды" для среды в Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="e7f6a-108">Пользователь-администратор, имеющий лицензию Power Apps Plan 2, должен открыть [портал администратора Power Apps](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="e7f6a-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="e7f6a-109">Выберите **Среды**и выберите правильную среду для Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="e7f6a-110">На вкладке **Безопасность** на вкладке **Роли среды** выберите **Создатель среды**.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Вкладка ролей среды](media/environment-roles.png)

4. <span data-ttu-id="e7f6a-112">На вкладке **Пользователи** добавьте пользователя или вашу организацию.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Вкладка пользователей](media/environment-maker.png)

5. <span data-ttu-id="e7f6a-114">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-114">Select **Save**.</span></span>

6. <span data-ttu-id="e7f6a-115">Теперь пользователь должен выполнить вход в [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="e7f6a-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="e7f6a-116">Выберите **Синхронизация**, чтобы обновить приложения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-116">Select **Sync** to update the user apps.</span></span>

    ![Кнопка "Синхронизация"](media/get-more.png)

    <span data-ttu-id="e7f6a-118">По завершении синхронизации Human Resources появится на домашней странице.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>
