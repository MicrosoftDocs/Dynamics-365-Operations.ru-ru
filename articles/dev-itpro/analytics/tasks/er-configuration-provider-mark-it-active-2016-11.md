---
title: Создание поставщиков конфигурации и пометка их как активных
description: В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать поставщика конфигурации для электронной отчетности.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13a27c2fec2a2b226e9ae8d5b8f9a61e8b79ceb0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544917"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="87903-103">Создание поставщиков конфигурации и пометка их как активных</span><span class="sxs-lookup"><span data-stu-id="87903-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="87903-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать поставщика конфигурации для электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="87903-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="87903-105">Конфигурация электронной отчетности будет ссылаться на поставщика как автора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="87903-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="87903-106">В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку поставщики конфигурации электронной отчетности используются всеми компаниями.</span><span class="sxs-lookup"><span data-stu-id="87903-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="87903-107">Создание поставщика</span><span class="sxs-lookup"><span data-stu-id="87903-107">Create a provider</span></span>
1. <span data-ttu-id="87903-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="87903-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="87903-109">Щелкните "Поставщики конфигурации".</span><span class="sxs-lookup"><span data-stu-id="87903-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="87903-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="87903-110">Click New.</span></span>
    * <span data-ttu-id="87903-111">Запись поставщика имеет уникальные имя и URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="87903-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="87903-112">Проверьте содержимое этой страницы и пропустите эту процедуру, если запись для Litware, Inc. (http://www.litware.com).</span><span class="sxs-lookup"><span data-stu-id="87903-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="87903-113">В поле "Имя" введите "Litware, Inc.".</span><span class="sxs-lookup"><span data-stu-id="87903-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="87903-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="87903-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="87903-115">В поле "Веб-адрес" введите "http://www.litware.com".</span><span class="sxs-lookup"><span data-stu-id="87903-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * http://www.litware.com  
6. <span data-ttu-id="87903-116">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="87903-116">Click Save.</span></span>
7. <span data-ttu-id="87903-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="87903-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="87903-118">Выбор поставщика как активного</span><span class="sxs-lookup"><span data-stu-id="87903-118">Select as an active provider</span></span>
1. <span data-ttu-id="87903-119">Выберите поставщика Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="87903-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="87903-120">Щелкните "Установить как активное".</span><span class="sxs-lookup"><span data-stu-id="87903-120">Click Set active.</span></span>

