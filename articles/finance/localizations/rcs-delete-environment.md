---
title: Regulatory Configuration Service (RCS) — Удаление среды RCS
description: В этой теме объясняется, как системный администратор Regulatory Configuration Service (RCS) может удалить среду RCS и соответствующие данные.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295826"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a><span data-ttu-id="5d935-103">Regulatory Configuration Service (RCS) — Удаление среды RCS</span><span class="sxs-lookup"><span data-stu-id="5d935-103">Regulatory Configuration Service (RCS) - Delete an RCS environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d935-104">В этой теме объясняется, как системный администратор Regulatory Configuration Service (RCS) может удалить среду RCS и соответствующие данные.</span><span class="sxs-lookup"><span data-stu-id="5d935-104">This topic explains how a Regulatory Configuration Service (RCS) system administrator can delete an RCS environment and related data.</span></span>

<span data-ttu-id="5d935-105">Прежде чем вы сможете выполнить процедуру из данной темы, необходимо выполнить следующие предварительные требования:</span><span class="sxs-lookup"><span data-stu-id="5d935-105">Before you can complete the procedure in this topic, the following prerequisites must be met:</span></span>

- <span data-ttu-id="5d935-106">Пользователю должна быть назначена роль **Системный администратор** для среды RCS.</span><span class="sxs-lookup"><span data-stu-id="5d935-106">You must have the **System Admin** role assigned to you for the RCS environment.</span></span>
- <span data-ttu-id="5d935-107">Роли **Системный администратор** должна быть назначена роль **RCSDeleteEnvironmentDuty**.</span><span class="sxs-lookup"><span data-stu-id="5d935-107">The **System Admin** role must have the **RCSDeleteEnvironmentDuty** role assigned to it.</span></span>

## <a name="delete-an-rcs-environment"></a><span data-ttu-id="5d935-108">Удаление среды RCS</span><span class="sxs-lookup"><span data-stu-id="5d935-108">Delete an RCS environment</span></span>

1. <span data-ttu-id="5d935-109">Откройте RCS и выберите плитку **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="5d935-109">Open RCS, and select the **Electronic reporting** workspace tile.</span></span>
2. <span data-ttu-id="5d935-110">В разделе **Связанные ссылки** выберите **Удалить среду RCS**.</span><span class="sxs-lookup"><span data-stu-id="5d935-110">In the **Related links** section, select **Delete RCS environment**.</span></span>

    ![Ссылка на удаление среды RCS в разделе связанных ссылок](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. <span data-ttu-id="5d935-112">В появившемся диалоговом окне проверьте сообщения об области удаления среды.</span><span class="sxs-lookup"><span data-stu-id="5d935-112">In the dialog box that appears, review the messages about the scope of environment deletion.</span></span>

    ![Сообщения в диалоговом окне "Удаление среды RCS"](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > <span data-ttu-id="5d935-114">Удаление среды RCS не может быть отменено.</span><span class="sxs-lookup"><span data-stu-id="5d935-114">Deletion of an RCS environment can't be reversed.</span></span>
    >
    > <span data-ttu-id="5d935-115">Операция удаляет выбранную среду RCS и все связанные с ней данные, включая возможности и конфигурации, хранящиеся в глобальном репозитории.</span><span class="sxs-lookup"><span data-stu-id="5d935-115">The operation deletes the selected RCS environment and any related data, including features and configurations that are stored in the Global repository.</span></span> <span data-ttu-id="5d935-116">Функции и конфигурации, которые используются совместно с другими организациями, будут отключены от общего доступа и удалены, если они не имеют зависимостей.</span><span class="sxs-lookup"><span data-stu-id="5d935-116">Features and configurations that are shared with other organizations will be unshared and deleted if they have no dependencies.</span></span> <span data-ttu-id="5d935-117">Функции и конфигурации с зависимостями будут помечены как отключенные.</span><span class="sxs-lookup"><span data-stu-id="5d935-117">Features and configurations that have dependencies will be marked as discontinued.</span></span>

4. <span data-ttu-id="5d935-118">В предоставленном поле введите глобальный уникальный идентификатор (GUID) среды RCS для подтверждения того, что вы хотите ее удалить.</span><span class="sxs-lookup"><span data-stu-id="5d935-118">In the field that is provided, enter the globally unique identifier (GUID) of the RCS environment to confirm that you want to delete it.</span></span> <span data-ttu-id="5d935-119">GUID среды включен в сообщение об удалении.</span><span class="sxs-lookup"><span data-stu-id="5d935-119">The environment's GUID is included in the deletion message.</span></span>
5. <span data-ttu-id="5d935-120">Выберите **Удалить среду**.</span><span class="sxs-lookup"><span data-stu-id="5d935-120">Select **Delete environment**.</span></span>
    
<span data-ttu-id="5d935-121">Среда RCS и все соответствующие данные будут удалены.</span><span class="sxs-lookup"><span data-stu-id="5d935-121">Your RCS environment and any related data are now deleted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d935-122">После удаления среды RCS восстановить данные невозможно.</span><span class="sxs-lookup"><span data-stu-id="5d935-122">After you delete an RCS environment, there is no way to recover the data.</span></span> <span data-ttu-id="5d935-123">Новую среду RCS можно создать в любом доступном регионе RCS.</span><span class="sxs-lookup"><span data-stu-id="5d935-123">A new RCS environment can be created in any available RCS region.</span></span>
