---
title: Доступ к личным адресам по роли безопасности
description: В этой статье объясняется, как решить проблему, когда клиент не может получить доступ к частным адресам.
author: andreabichsel
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8daee1b645836e96a4bf3057cb317d5409d4583a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803929"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="86193-103">Доступ к частным адресам по роли безопасности</span><span class="sxs-lookup"><span data-stu-id="86193-103">Access to private addresses by security role</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="86193-104">**Расход**</span><span class="sxs-lookup"><span data-stu-id="86193-104">**Issue**</span></span>

<span data-ttu-id="86193-105">После того как клиент продублировал роль безопасности и выполнил вход с новой ролью, клиент не может увидеть адреса, которые были помечены как частные.</span><span class="sxs-lookup"><span data-stu-id="86193-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="86193-106">**Разрешение**</span><span class="sxs-lookup"><span data-stu-id="86193-106">**Resolution**</span></span>

<span data-ttu-id="86193-107">Для решения проблемы клиент должен выполнить следующие действия для дублированной роли безопасности.</span><span class="sxs-lookup"><span data-stu-id="86193-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="86193-108">Перейдите в раздел **Управление организацией \> Глобальная адресная книга \> Параметры глобальной адресной книги**.</span><span class="sxs-lookup"><span data-stu-id="86193-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="86193-109">На вкладке **Безопасность частного местоположения** переместить новую роль безопасности из списка **Доступные роли** в список **Выбранные роли**.</span><span class="sxs-lookup"><span data-stu-id="86193-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="86193-110">Выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="86193-110">Select **Save**.</span></span>

![Страница параметров глобальной адресной книги](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]