---
title: Управление шаблонами электронной почты
description: В этом разделе описывается, как управлять шаблонами сообщений электронной почты.
author: andreabichsel
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationWordBookmark, HRMApplicationEmailTemplate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a911fea9e7d1009160a021e53533c0ce49efbfe
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143704"
---
# <a name="manage-email-templates"></a><span data-ttu-id="51318-103">Управление шаблонами электронной почты</span><span class="sxs-lookup"><span data-stu-id="51318-103">Manage email templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51318-104">Информацию из базы данных вашей организации можно перенести в закладки в новом документе и использовать ее в шаблонах, помогающих эффективно переписываться с отправителями заявлений и кандидатами.</span><span class="sxs-lookup"><span data-stu-id="51318-104">You can transfer information from your organization's database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="51318-105">Для этого необходимо создать шаблон, содержащий стандартный текст и закладки в местах вставки системных данных.</span><span class="sxs-lookup"><span data-stu-id="51318-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="51318-106">Например, можно вставить адрес и контактные данные кандидата в документ Microsoft Word и использовать этот документ при переписке с этим кандидатом.</span><span class="sxs-lookup"><span data-stu-id="51318-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="51318-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="51318-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="51318-108">Выбор закладок для использования в шаблонах сообщений электронной почты</span><span class="sxs-lookup"><span data-stu-id="51318-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="51318-109">В области переходов выберите **Модули > Управление персоналом > Набор сотрудников > Связь > Закладки приложения**.</span><span class="sxs-lookup"><span data-stu-id="51318-109">In the navigation pane, go to **Modules > Human Resources > Recruitment > Communication > Application bookmarks**.</span></span>
2. <span data-ttu-id="51318-110">Найдите в списке требуемое действие по обмену корреспонденцией и выберите его.</span><span class="sxs-lookup"><span data-stu-id="51318-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="51318-111">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="51318-111">Select **Edit**.</span></span>
4. <span data-ttu-id="51318-112">Выберите поля, которые вы хотите использовать в шаблоне электронного сообщения для выбранного действия по обмену корреспонденцией, и переместите их в поля закладок.</span><span class="sxs-lookup"><span data-stu-id="51318-112">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="51318-113">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="51318-113">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="51318-114">Создание шаблона сообщения эл. почты</span><span class="sxs-lookup"><span data-stu-id="51318-114">Create an email template</span></span>
1. <span data-ttu-id="51318-115">В области переходов выберите **Модули > Управление персоналом > Набор сотрудников > Связь > Шаблоны приложения электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="51318-115">In the navigation pane, go to **Modules > Human resources > Recruitment > Communication > Application e-mail templates**.</span></span>
2. <span data-ttu-id="51318-116">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="51318-116">Select **New**.</span></span>
3. <span data-ttu-id="51318-117">В поле **Соответствующее действие** выберите **Собеседование**.</span><span class="sxs-lookup"><span data-stu-id="51318-117">In the **Correspondence action** field, select **Interview**.</span></span> <span data-ttu-id="51318-118">Выберите действие по обмену корреспонденцией, содержащее закладки, которые требуется использовать для данного типа переписки по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="51318-118">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="51318-119">В поле **Шаблон сообщения** введите значение.</span><span class="sxs-lookup"><span data-stu-id="51318-119">In the **E-mail template** field, type a value.</span></span>
5. <span data-ttu-id="51318-120">В поле **Тема** введите значение.</span><span class="sxs-lookup"><span data-stu-id="51318-120">In the **Subject** field, type a value.</span></span>
6. <span data-ttu-id="51318-121">В поле **Текст** введите значение.</span><span class="sxs-lookup"><span data-stu-id="51318-121">In the **Text** field, type a value.</span></span>
7. <span data-ttu-id="51318-122">Найдите в списке требуемое поле закладки и выберите его.</span><span class="sxs-lookup"><span data-stu-id="51318-122">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="51318-123">Продолжайте вводить электронное сообщение, вставляя, где необходимо, поля закладок.</span><span class="sxs-lookup"><span data-stu-id="51318-123">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
9. <span data-ttu-id="51318-124">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="51318-124">Select **Save**.</span></span>

