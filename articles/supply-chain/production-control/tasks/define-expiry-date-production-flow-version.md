---
title: Определение даты окончания срока действия для версии производственного потока
description: Чтобы завершить срок действия и обработку версии производственного потока на определенную дату или запланировать замену активной версии новой версией, необходимо задать дату окончания для версии.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d8df396abc3ac4a2c3920e6bf2b21d8a4463df2
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146867"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="db241-103">Определение даты окончания срока действия для версии производственного потока</span><span class="sxs-lookup"><span data-stu-id="db241-103">Define an expiry date for a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="db241-104">Чтобы завершить срок действия и обработку версии производственного потока на определенную дату или запланировать замену активной версии новой версией, необходимо задать дату окончания для версии.</span><span class="sxs-lookup"><span data-stu-id="db241-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="db241-105">Нет необходимости деактивировать версию.</span><span class="sxs-lookup"><span data-stu-id="db241-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="db241-106">Установка даты окончания для завершения версии производственного потока</span><span class="sxs-lookup"><span data-stu-id="db241-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="db241-107">Перейдите в раздел "Управление производством" > "Настройка" > "Поток бережливого производства" > "Производственные потоки".</span><span class="sxs-lookup"><span data-stu-id="db241-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="db241-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="db241-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="db241-109">Выберите любой производственный поток, который имеет уже определенную версию.</span><span class="sxs-lookup"><span data-stu-id="db241-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="db241-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="db241-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="db241-111">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="db241-111">Click Edit.</span></span>
5. <span data-ttu-id="db241-112">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="db241-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="db241-113">В поле "Дата окончания срока действия" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="db241-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="db241-114">Для даты окончания срока действия новая версия не начнется и не станет активной.</span><span class="sxs-lookup"><span data-stu-id="db241-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="db241-115">Также будет невозможно создавать или запускать задания для данного производственного потока.</span><span class="sxs-lookup"><span data-stu-id="db241-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="db241-116">Тем не менее можно завершать запущенные задания после окончании срока действия.</span><span class="sxs-lookup"><span data-stu-id="db241-116">You can still complete started jobs after the expiration date.</span></span>  

