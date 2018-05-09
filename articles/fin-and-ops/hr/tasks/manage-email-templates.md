--- 
title: "Управление шаблонами электронной почты"
description: "Информацию из базы данных вашей организации можно перенести в закладки в новом документе и использовать ее в шаблонах, помогающих эффективно переписываться с отправителями заявлений и кандидатами."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f09d18e39c58385cfdbbbbb0ff398d1a11bbcbe0
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="manage-email-templates"></a><span data-ttu-id="5b9b4-103">Управление шаблонами электронной почты</span><span class="sxs-lookup"><span data-stu-id="5b9b4-103">Manage email templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5b9b4-104">Информацию из базы данных вашей организации можно перенести в закладки в новом документе и использовать ее в шаблонах, помогающих эффективно переписываться с отправителями заявлений и кандидатами.</span><span class="sxs-lookup"><span data-stu-id="5b9b4-104">You can transfer information from your organization’s database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="5b9b4-105">Для этого необходимо создать шаблон, содержащий стандартный текст и закладки в местах вставки системных данных.</span><span class="sxs-lookup"><span data-stu-id="5b9b4-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="5b9b4-106">Например, можно вставить адрес и контактные данные кандидата в документ Microsoft Word и использовать этот документ при переписке с этим кандидатом.</span><span class="sxs-lookup"><span data-stu-id="5b9b4-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="5b9b4-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="5b9b4-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="5b9b4-108">Выбор закладок для использования в шаблонах сообщений электронной почты</span><span class="sxs-lookup"><span data-stu-id="5b9b4-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="5b9b4-109">Перейдите в раздел "Закладки приложения".</span><span class="sxs-lookup"><span data-stu-id="5b9b4-109">Go to Application bookmarks.</span></span>
2. <span data-ttu-id="5b9b4-110">Найдите в списке требуемое действие по обмену корреспонденцией и выберите его.</span><span class="sxs-lookup"><span data-stu-id="5b9b4-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="5b9b4-111">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="5b9b4-111">Click Edit.</span></span>
4. <span data-ttu-id="5b9b4-112">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="5b9b4-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5b9b4-113">Выберите поля, которые вы хотите использовать в шаблоне электронного сообщения для выбранного действия по обмену корреспонденцией, и переместите их в поля закладок.</span><span class="sxs-lookup"><span data-stu-id="5b9b4-113">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="5b9b4-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5b9b4-114">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="5b9b4-115">Создание шаблона эл. почты</span><span class="sxs-lookup"><span data-stu-id="5b9b4-115">Create an email template</span></span>
1. <span data-ttu-id="5b9b4-116">Перейдите в раздел "Управление персоналом" > "Набор сотрудников" > "Связь" > "Шаблоны электронной почты приложения".</span><span class="sxs-lookup"><span data-stu-id="5b9b4-116">Go to Human resources > Recruitment > Communication > Application e-mail templates.</span></span>
2. <span data-ttu-id="5b9b4-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="5b9b4-117">Click New.</span></span>
3. <span data-ttu-id="5b9b4-118">В поле "Соответствующее действие" выберите "Собеседование".</span><span class="sxs-lookup"><span data-stu-id="5b9b4-118">In the Correspondence action field, select 'Interview'.</span></span>
    * <span data-ttu-id="5b9b4-119">Выберите действие по обмену корреспонденцией, содержащее закладки, которые требуется использовать для данного типа переписки по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="5b9b4-119">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="5b9b4-120">В поле "Шаблон сообщения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5b9b4-120">In the E-mail template field, type a value.</span></span>
5. <span data-ttu-id="5b9b4-121">В поле "Тема" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5b9b4-121">In the Subject field, type a value.</span></span>
6. <span data-ttu-id="5b9b4-122">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="5b9b4-122">In the Text field, type a value.</span></span>
7. <span data-ttu-id="5b9b4-123">Найдите в списке требуемое поле закладки и выберите его.</span><span class="sxs-lookup"><span data-stu-id="5b9b4-123">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="5b9b4-124">Продолжайте вводить электронное сообщение, вставляя, где необходимо, поля закладок.</span><span class="sxs-lookup"><span data-stu-id="5b9b4-124">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
    * <span data-ttu-id="5b9b4-125">Продолжайте вводить свое электронное сообщение, вставляя, где необходимо, поля закладок.</span><span class="sxs-lookup"><span data-stu-id="5b9b4-125">Continue typing your email message inserting the bookmark fields where desired.</span></span>  
9. <span data-ttu-id="5b9b4-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="5b9b4-126">Click Save.</span></span>


