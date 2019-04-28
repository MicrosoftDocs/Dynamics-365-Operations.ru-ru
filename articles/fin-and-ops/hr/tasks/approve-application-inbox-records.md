---
title: Одобрение записей входящих заявлений
description: В этой процедуре показано рассмотрение заявлений, полученных через портал самообслуживания сотрудников.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationBasket, HRMApplicationBasketApprove, HRMApplication
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 28a82ea8747fcbbceb835291ad5cd3d87091a736
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "857231"
---
# <a name="approve-application-inbox-records"></a><span data-ttu-id="2b4e0-103">Одобрение записей входящих заявлений</span><span class="sxs-lookup"><span data-stu-id="2b4e0-103">Approve application inbox records</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2b4e0-104">В этой процедуре показано рассмотрение заявлений, полученных через портал самообслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-104">This procedure shows how to review applications received through the Employee self-service pages.</span></span> <span data-ttu-id="2b4e0-105">Помимо рассмотрения заявлений, вы можете утверждать выбранные записи входящих заявлений.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-105">In addition to reviewing the applications, you can approve the application in box records that you select.</span></span> <span data-ttu-id="2b4e0-106">Записи входящих заявлений — это заявления о приеме на работу, отправленные в компанию на рассмотрение.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-106">Application inbox records represent employment applications that were submitted to the company for consideration.</span></span> <span data-ttu-id="2b4e0-107">После утверждения записи лица, отправившего заявление, будет создана запись кандидата.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-107">After approving a record, an applicant record will be created for the person who submitted the application.</span></span> <span data-ttu-id="2b4e0-108">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="review-application-inbox-record"></a><span data-ttu-id="2b4e0-109">Просмотр записи входящего заявления</span><span class="sxs-lookup"><span data-stu-id="2b4e0-109">Review application inbox record</span></span>
1. <span data-ttu-id="2b4e0-110">Перейдите в раздел > "Управление персоналом" > "Набор сотрудников" > "Входящее заявление".</span><span class="sxs-lookup"><span data-stu-id="2b4e0-110">Go to Human resources > Recruitment > Applications > Application inbox.</span></span>
2. <span data-ttu-id="2b4e0-111">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2b4e0-112">Разверните раздел "Адреса".</span><span class="sxs-lookup"><span data-stu-id="2b4e0-112">Expand the Addresses section.</span></span>
4. <span data-ttu-id="2b4e0-113">Разверните раздел "Контактная информация".</span><span class="sxs-lookup"><span data-stu-id="2b4e0-113">Expand the Contact information section.</span></span>
5. <span data-ttu-id="2b4e0-114">Разверните раздел "Вложения".</span><span class="sxs-lookup"><span data-stu-id="2b4e0-114">Expand the Attachments section.</span></span>

## <a name="approve-application-inbox-record"></a><span data-ttu-id="2b4e0-115">Утверждение записи входящего заявления</span><span class="sxs-lookup"><span data-stu-id="2b4e0-115">Approve application inbox record</span></span>
1. <span data-ttu-id="2b4e0-116">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-116">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="2b4e0-117">Запомните значение в поле "Имя"; в дальнейшем вам предстоит на него ссылаться</span><span class="sxs-lookup"><span data-stu-id="2b4e0-117">Note the value in the Name field to reference later</span></span>
3. <span data-ttu-id="2b4e0-118">Нажмите кнопку Одобрить.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-118">Click Approve.</span></span>
4. <span data-ttu-id="2b4e0-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2b4e0-119">Click OK.</span></span>
5. <span data-ttu-id="2b4e0-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-120">Close the page.</span></span>

## <a name="view-the-newly-created-application-record"></a><span data-ttu-id="2b4e0-121">Просмотр созданной записи заявления</span><span class="sxs-lookup"><span data-stu-id="2b4e0-121">View the newly created application record</span></span>
1. <span data-ttu-id="2b4e0-122">Перейдите в раздел "Управление персоналом" > "Набор сотрудников" > "Заявления" > "Заявления".</span><span class="sxs-lookup"><span data-stu-id="2b4e0-122">Go to Human resources > Recruitment > Applications > Applications.</span></span>
2. <span data-ttu-id="2b4e0-123">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-123">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="2b4e0-124">Разверните раздел "Вложения".</span><span class="sxs-lookup"><span data-stu-id="2b4e0-124">Expand the Attachments section.</span></span>

