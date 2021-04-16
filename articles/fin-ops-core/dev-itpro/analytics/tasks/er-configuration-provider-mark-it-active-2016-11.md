---
title: Создание поставщиков конфигураций и пометка их как активных
description: В этой теме поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать поставщика конфигурации.
author: NickSelin
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27e1275199d098fffb56db61ed6bfd2fc3cdb790
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755138"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="1bb32-103">Создание поставщиков конфигураций и пометка их как активных</span><span class="sxs-lookup"><span data-stu-id="1bb32-103">Create configuration providers and mark them as active</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1bb32-104">В этой теме поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать поставщика конфигурации для электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="1bb32-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="1bb32-105">Конфигурация электронной отчетности будет ссылаться на поставщика как автора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1bb32-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="1bb32-106">В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку поставщики конфигурации электронной отчетности используются всеми компаниями.</span><span class="sxs-lookup"><span data-stu-id="1bb32-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="1bb32-107">Создание поставщика</span><span class="sxs-lookup"><span data-stu-id="1bb32-107">Create a provider</span></span>
1. <span data-ttu-id="1bb32-108">Перейдите в **область навигации** в верхнем левом углу и выберите **Администрирование организации**.</span><span class="sxs-lookup"><span data-stu-id="1bb32-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="1bb32-109">Перейдите в раздел **Рабочие области > Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="1bb32-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="1bb32-110">Перейдите в раздел **Связанные ссылки > Поставщики конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="1bb32-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="1bb32-111">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1bb32-111">Select **New**.</span></span>
    - <span data-ttu-id="1bb32-112">Запись поставщика имеет уникальные имя и URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="1bb32-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="1bb32-113">Проверьте содержимое этой страницы и пропустите эту процедуру, если запись для Litware, Inc. (https://www.litware.com).</span><span class="sxs-lookup"><span data-stu-id="1bb32-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="1bb32-114">В поле "Имя" введите `Litware, Inc.`.</span><span class="sxs-lookup"><span data-stu-id="1bb32-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="1bb32-115">В поле веб-адреса введите `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="1bb32-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="1bb32-116">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1bb32-116">Select **Save**.</span></span>
8. <span data-ttu-id="1bb32-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1bb32-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="1bb32-118">Выбор поставщика как активного</span><span class="sxs-lookup"><span data-stu-id="1bb32-118">Select as an active provider</span></span>
1. <span data-ttu-id="1bb32-119">Выберите поставщика Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="1bb32-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="1bb32-120">Выберите **Установить активные**.</span><span class="sxs-lookup"><span data-stu-id="1bb32-120">Select **Set active**.</span></span>

![Страница рабочей области электронной отчетности](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]