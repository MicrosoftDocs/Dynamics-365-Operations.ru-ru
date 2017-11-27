--- 
title: "Создание поставщика конфигурации и пометка его как активного для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как пользователь с ролью \"Системный администратор\" или \"Разработчик электронной отчетности\" может создать поставщика конфигурации для электронной отчетности."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 809a1466b0f4674f503bc654175d8f94b37a6508
ms.openlocfilehash: 2dfa04f280249884af2a237807fb283059444a6c
ms.contentlocale: ru-ru
ms.lasthandoff: 11/02/2017

---
# <a name="create-a-configuration-provider-and-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="a0c24-103">Создание поставщика конфигурации и пометка его как активного для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="a0c24-103">Create a configuration provider and mark it as active for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a0c24-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать поставщика конфигурации для электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="a0c24-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="a0c24-105">Конфигурация электронной отчетности будет ссылаться на поставщика как автора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a0c24-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="a0c24-106">В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку поставщики конфигурации электронной отчетности используются всеми компаниями.</span><span class="sxs-lookup"><span data-stu-id="a0c24-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="a0c24-107">Создание поставщика</span><span class="sxs-lookup"><span data-stu-id="a0c24-107">Create a provider</span></span>
1. <span data-ttu-id="a0c24-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="a0c24-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a0c24-109">Щелкните "Поставщики конфигурации".</span><span class="sxs-lookup"><span data-stu-id="a0c24-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="a0c24-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a0c24-110">Click New.</span></span>
    * <span data-ttu-id="a0c24-111">Запись поставщика имеет уникальные имя и URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="a0c24-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="a0c24-112">Проверьте содержимое этой страницы и пропустите эту процедуру, если запись для Litware, Inc. (http://www.litware.com) уже существует.</span><span class="sxs-lookup"><span data-stu-id="a0c24-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="a0c24-113">В поле "Имя" введите "Litware, Inc.".</span><span class="sxs-lookup"><span data-stu-id="a0c24-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="a0c24-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="a0c24-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="a0c24-115">В поле веб-адреса введите "http://www.litware.com".</span><span class="sxs-lookup"><span data-stu-id="a0c24-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * <span data-ttu-id="a0c24-116">http://www.litware.com</span><span class="sxs-lookup"><span data-stu-id="a0c24-116">http://www.litware.com</span></span>  
6. <span data-ttu-id="a0c24-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a0c24-117">Click Save.</span></span>
7. <span data-ttu-id="a0c24-118">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a0c24-118">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="a0c24-119">Выбор поставщика как активного</span><span class="sxs-lookup"><span data-stu-id="a0c24-119">Select as an active provider</span></span>
1. <span data-ttu-id="a0c24-120">Выберите поставщика Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="a0c24-120">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="a0c24-121">Щелкните "Установить как активное".</span><span class="sxs-lookup"><span data-stu-id="a0c24-121">Click Set active.</span></span>


