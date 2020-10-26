---
title: Переклассификация основных средств
description: Чтобы реклассифицировать основное средство, необходимо переместить его в новую группу основных средств или назначить ему новый номер основных средств в той же группе.
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd108f2e778b31749c66b2787d9f59467cae97dd
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977223"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="a8b14-103">Переклассификация основных средств</span><span class="sxs-lookup"><span data-stu-id="a8b14-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8b14-104">Чтобы реклассифицировать основное средство, необходимо переместить его в новую группу основных средств или назначить ему новый номер основных средств в той же группе.</span><span class="sxs-lookup"><span data-stu-id="a8b14-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="a8b14-105">При реклассификации основного средства:</span><span class="sxs-lookup"><span data-stu-id="a8b14-105">When a fixed asset is reclassified:</span></span>

* <span data-ttu-id="a8b14-106">Для нового основного средства создаются все книги для существующих основных средств.</span><span class="sxs-lookup"><span data-stu-id="a8b14-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="a8b14-107">Вся информация, которая была настроена для исходного основного средства, копируется в новое основное средство.</span><span class="sxs-lookup"><span data-stu-id="a8b14-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="a8b14-108">Книги для исходных основных средств имеют статус "Закрыто".</span><span class="sxs-lookup"><span data-stu-id="a8b14-108">The status of the books for the original fixed asset is Closed.</span></span> 

* <span data-ttu-id="a8b14-109">Новые книги новых основных средств содержат дату реклассификации в поле **Дата приобретения**.</span><span class="sxs-lookup"><span data-stu-id="a8b14-109">The new books of the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="a8b14-110">Дата в поле **Дата начала амортизации** копируется из исходной информации об ОС.</span><span class="sxs-lookup"><span data-stu-id="a8b14-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="a8b14-111">Если амортизация уже начата, в поле **Дата последней амортизации** отображается дата реклассификации.</span><span class="sxs-lookup"><span data-stu-id="a8b14-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

* <span data-ttu-id="a8b14-112">Существующие проводки по основным средствам для исходного основного средства отменяются, и создаются проводки для нового основного средства.</span><span class="sxs-lookup"><span data-stu-id="a8b14-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

<span data-ttu-id="a8b14-113">Выполните следующие действия, чтобы изменить классификацию основного средства:</span><span class="sxs-lookup"><span data-stu-id="a8b14-113">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="a8b14-114">Перейдите в раздел **Основные средства > Периодические задачи > Реклассификация**.</span><span class="sxs-lookup"><span data-stu-id="a8b14-114">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="a8b14-115">В поле **Группа ОС** выберите группу, которую требуется реклассифицировать.</span><span class="sxs-lookup"><span data-stu-id="a8b14-115">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="a8b14-116">В поле **Номер основного средства** выберите основное средство для реклассификации.</span><span class="sxs-lookup"><span data-stu-id="a8b14-116">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="a8b14-117">В поле **Новая группа основных средств** выберите группу, в которую требуется переместить основное средство.</span><span class="sxs-lookup"><span data-stu-id="a8b14-117">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="a8b14-118">Если новая группа основных средств прикреплена к номерной серии, поле **Новый инвентарный номер ОС** обновляется с учетом номера из новой номерной серии группы основных средств.</span><span class="sxs-lookup"><span data-stu-id="a8b14-118">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="a8b14-119">В противном случае поле **Новый инвентарный номер ОС** обновляется с учетом номера из новой номерной серии, настроенной на странице **Параметры основных средств**.</span><span class="sxs-lookup"><span data-stu-id="a8b14-119">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="a8b14-120">Если номерная серия не настроена на странице **Параметры основных средств**, введите номер в поле **Новый инвентарный номер ОС**.</span><span class="sxs-lookup"><span data-stu-id="a8b14-120">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="a8b14-121">В поле **Дата реклассификации** введите дату.</span><span class="sxs-lookup"><span data-stu-id="a8b14-121">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="a8b14-122">В поле **Серии ваучеров** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a8b14-122">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="a8b14-123">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8b14-123">Click **OK**.</span></span>
