---
title: Доступ к частным адресам по роли безопасности
description: В этом разделе объясняется, как решить проблему, когда клиент не может получить доступ к частным адресам.
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
ms.openlocfilehash: f8aaa33e5fda404b48548f9a57977dd0ccd53dc1
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "859490"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="97fd1-103">Доступ к частным адресам по роли безопасности</span><span class="sxs-lookup"><span data-stu-id="97fd1-103">Access to private addresses by security role</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="97fd1-104">**Расход**</span><span class="sxs-lookup"><span data-stu-id="97fd1-104">**Issue**</span></span>

<span data-ttu-id="97fd1-105">После того как клиент продублировал роль безопасности и выполнил вход с новой ролью, клиент не может увидеть адреса, которые были помечены как частные.</span><span class="sxs-lookup"><span data-stu-id="97fd1-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="97fd1-106">**Разрешение**</span><span class="sxs-lookup"><span data-stu-id="97fd1-106">**Resolution**</span></span>

<span data-ttu-id="97fd1-107">Для решения проблемы клиент должен выполнить следующие действия для дублированной роли безопасности.</span><span class="sxs-lookup"><span data-stu-id="97fd1-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="97fd1-108">Перейдите в раздел **Управление организацией \> Глобальная адресная книга \> Параметры глобальной адресной книги**.</span><span class="sxs-lookup"><span data-stu-id="97fd1-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="97fd1-109">На вкладке **Безопасность частного местоположения** переместить новую роль безопасности из списка **Доступные роли** в список **Выбранные роли**.</span><span class="sxs-lookup"><span data-stu-id="97fd1-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="97fd1-110">Выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="97fd1-110">Select **Save**.</span></span>

![Страница параметров глобальной адресной книги](media/GAD-parameters.png)
