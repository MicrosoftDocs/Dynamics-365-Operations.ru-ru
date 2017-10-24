--- 
title: "Деактивация версии производственного потока"
description: "Когда активная версия производственного потока больше не требуется, ее можно отключить."
author: cvocph
manager: AnnBe
ms.date: 10/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4a7eee6617e12d59a3d06207f5f6b58c93e28240
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="b9d9d-103">Деактивация версии производственного потока</span><span class="sxs-lookup"><span data-stu-id="b9d9d-103">Deactivate a production flow version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9d9d-104">Когда активная версия производственного потока больше не требуется, ее можно отключить.</span><span class="sxs-lookup"><span data-stu-id="b9d9d-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="b9d9d-105">Необходимо использовать эту возможность только в том случае, если правила канбана и действия завершены и не будут активированы снова.</span><span class="sxs-lookup"><span data-stu-id="b9d9d-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="b9d9d-106">Обратите внимание, что дата окончания срока действия всех правил канбана, связанных с этой версии производственного потока, будет обновлена на текущую дату и время.</span><span class="sxs-lookup"><span data-stu-id="b9d9d-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="b9d9d-107">Для изменения активной версии производственного потока рекомендуется установить дату окончания для активной версии и создать новую версию.</span><span class="sxs-lookup"><span data-stu-id="b9d9d-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="b9d9d-108">Это позволит вам продолжать ваши производственные операции, пока подготавливается новая версия и связанные правила канбана.</span><span class="sxs-lookup"><span data-stu-id="b9d9d-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="b9d9d-109">Чтобы завершить срок действия активной версии производственного потока, необходимо задать дату окончания.</span><span class="sxs-lookup"><span data-stu-id="b9d9d-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="b9d9d-110">В этом смысле деактивация больше похожа на исключение, чем на правило.</span><span class="sxs-lookup"><span data-stu-id="b9d9d-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="b9d9d-111">Для этой процедуры требуется производственный поток с версией, которую можно отключить.</span><span class="sxs-lookup"><span data-stu-id="b9d9d-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="b9d9d-112">Не попробуйте выполнить это в производственной среде, пока не будете на 100% уверены, что данная версия является полностью устаревшей.</span><span class="sxs-lookup"><span data-stu-id="b9d9d-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="b9d9d-113">Деактивация версии производственного потока</span><span class="sxs-lookup"><span data-stu-id="b9d9d-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="b9d9d-114">Перейдите в раздел "Управление производством" > "Настройка" > "Поток бережливого производства" > "Производственные потоки".</span><span class="sxs-lookup"><span data-stu-id="b9d9d-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="b9d9d-115">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b9d9d-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b9d9d-116">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b9d9d-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b9d9d-117">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b9d9d-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b9d9d-118">Нажмите кнопку "Деактивировать".</span><span class="sxs-lookup"><span data-stu-id="b9d9d-118">Click Deactivate.</span></span>
    * <span data-ttu-id="b9d9d-119">Не продолжайте, если вы не уверены на 100%, что эта версия производственного потока является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="b9d9d-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="b9d9d-120">При нажатии ОК истекает срок действия всех активных правил канбана и происходит немедленная остановка всех действий по производству и пополнению этой версии производственного потока.</span><span class="sxs-lookup"><span data-stu-id="b9d9d-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="b9d9d-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b9d9d-121">Click OK.</span></span>


