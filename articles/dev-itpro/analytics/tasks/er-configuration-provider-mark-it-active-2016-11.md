--- 
title: "Создание поставщиков конфигурации и пометка их как активных"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 37957f224cb57fd9f6c5014740bcea124a99a03a
ms.contentlocale: ru-ru
ms.lasthandoff: 08/09/2018

---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="89865-103">Создание поставщиков конфигурации и пометка их как активных</span><span class="sxs-lookup"><span data-stu-id="89865-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="89865-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать поставщика конфигурации для электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="89865-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="89865-105">Конфигурация электронной отчетности будет ссылаться на поставщика как автора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="89865-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="89865-106">В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку поставщики конфигурации электронной отчетности используются всеми компаниями.</span><span class="sxs-lookup"><span data-stu-id="89865-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="89865-107">Создание поставщика</span><span class="sxs-lookup"><span data-stu-id="89865-107">Create a provider</span></span>
1. <span data-ttu-id="89865-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="89865-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="89865-109">Щелкните "Поставщики конфигурации".</span><span class="sxs-lookup"><span data-stu-id="89865-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="89865-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="89865-110">Click New.</span></span>
    * <span data-ttu-id="89865-111">Запись поставщика имеет уникальные имя и URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="89865-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="89865-112">Проверьте содержимое этой страницы и пропустите эту процедуру, если запись для Litware, Inc. (`http://www.litware.com`).</span><span class="sxs-lookup"><span data-stu-id="89865-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (`http://www.litware.com`) already exists.</span></span>  
4. <span data-ttu-id="89865-113">В поле "Имя" введите "Litware, Inc.".</span><span class="sxs-lookup"><span data-stu-id="89865-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="89865-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="89865-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="89865-115">В поле "Веб-адрес" введите `http://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="89865-115">In the Internet address field, type `http://www.litware.com`.</span></span>
6. <span data-ttu-id="89865-116">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="89865-116">Click Save.</span></span>
7. <span data-ttu-id="89865-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="89865-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="89865-118">Выбор поставщика как активного</span><span class="sxs-lookup"><span data-stu-id="89865-118">Select as an active provider</span></span>
1. <span data-ttu-id="89865-119">Выберите поставщика Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="89865-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="89865-120">Щелкните "Установить как активное".</span><span class="sxs-lookup"><span data-stu-id="89865-120">Click Set active.</span></span>


