---
title: Управление шаблонами электронной почты
description: В этом разделе описывается, как управлять шаблонами сообщений электронной почты.
author: andreabichsel
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMApplicationWordBookmark, HRMApplicationEmailTemplate
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0fac7a8332e21f0fa767d1926c63833ebd90c78c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563904"
---
# <a name="manage-email-templates"></a><span data-ttu-id="9f068-103">Управление шаблонами электронной почты</span><span class="sxs-lookup"><span data-stu-id="9f068-103">Manage email templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9f068-104">Информацию из базы данных вашей организации можно перенести в закладки в новом документе и использовать ее в шаблонах, помогающих эффективно переписываться с отправителями заявлений и кандидатами.</span><span class="sxs-lookup"><span data-stu-id="9f068-104">You can transfer information from your organization's database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="9f068-105">Для этого необходимо создать шаблон, содержащий стандартный текст и закладки в местах вставки системных данных.</span><span class="sxs-lookup"><span data-stu-id="9f068-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="9f068-106">Например, можно вставить адрес и контактные данные кандидата в документ Microsoft Word и использовать этот документ при переписке с этим кандидатом.</span><span class="sxs-lookup"><span data-stu-id="9f068-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="9f068-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="9f068-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="9f068-108">Выбор закладок для использования в шаблонах сообщений электронной почты</span><span class="sxs-lookup"><span data-stu-id="9f068-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="9f068-109">В области переходов выберите **Модули > Управление персоналом > Набор сотрудников > Связь > Закладки приложения**.</span><span class="sxs-lookup"><span data-stu-id="9f068-109">In the navigation pane, go to **Modules > Human Resources > Recruitment > Communication > Application bookmarks**.</span></span>
2. <span data-ttu-id="9f068-110">Найдите в списке требуемое действие по обмену корреспонденцией и выберите его.</span><span class="sxs-lookup"><span data-stu-id="9f068-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="9f068-111">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="9f068-111">Select **Edit**.</span></span>
4. <span data-ttu-id="9f068-112">Выберите поля, которые вы хотите использовать в шаблоне электронного сообщения для выбранного действия по обмену корреспонденцией, и переместите их в поля закладок.</span><span class="sxs-lookup"><span data-stu-id="9f068-112">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="9f068-113">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f068-113">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="9f068-114">Создание шаблона сообщения эл. почты</span><span class="sxs-lookup"><span data-stu-id="9f068-114">Create an email template</span></span>
1. <span data-ttu-id="9f068-115">В области переходов выберите **Модули > Управление персоналом > Набор сотрудников > Связь > Шаблоны приложения электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="9f068-115">In the navigation pane, go to **Modules > Human resources > Recruitment > Communication > Application e-mail templates**.</span></span>
2. <span data-ttu-id="9f068-116">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9f068-116">Select **New**.</span></span>
3. <span data-ttu-id="9f068-117">В поле **Соответствующее действие** выберите **Собеседование**.</span><span class="sxs-lookup"><span data-stu-id="9f068-117">In the **Correspondence action** field, select **Interview**.</span></span> <span data-ttu-id="9f068-118">Выберите действие по обмену корреспонденцией, содержащее закладки, которые требуется использовать для данного типа переписки по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="9f068-118">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="9f068-119">В поле **Шаблон сообщения** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f068-119">In the **E-mail template** field, type a value.</span></span>
5. <span data-ttu-id="9f068-120">В поле **Тема** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f068-120">In the **Subject** field, type a value.</span></span>
6. <span data-ttu-id="9f068-121">В поле **Текст** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f068-121">In the **Text** field, type a value.</span></span>
7. <span data-ttu-id="9f068-122">Найдите в списке требуемое поле закладки и выберите его.</span><span class="sxs-lookup"><span data-stu-id="9f068-122">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="9f068-123">Продолжайте вводить электронное сообщение, вставляя, где необходимо, поля закладок.</span><span class="sxs-lookup"><span data-stu-id="9f068-123">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
9. <span data-ttu-id="9f068-124">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9f068-124">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]