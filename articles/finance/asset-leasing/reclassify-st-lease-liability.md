---
title: Реклассификация краткосрочной части арендного обязательства
description: В этой теме объясняется, как создать ежемесячную запись журнала для повторной классификации части арендного обязательства в качестве краткосрочной.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 08ca824bb4c4a02a80f2187fb5f8fe4e8b7327c9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992922"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a><span data-ttu-id="7f967-103">Реклассификация краткосрочной части арендного обязательства</span><span class="sxs-lookup"><span data-stu-id="7f967-103">Reclassify the short-term portion of lease liability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f967-104">В этой теме объясняется, как создать ежемесячную запись журнала для повторной классификации части арендного обязательства в качестве краткосрочной.</span><span class="sxs-lookup"><span data-stu-id="7f967-104">This topic explains how to create a monthly journal entry to reclassify a portion of the lease liability as short-term.</span></span> <span data-ttu-id="7f967-105">Если график, выбранный в процессе пакетной обработки, является графиком **Переклассификация обязательств по краткосрочной аренде**, создается запись журнала.</span><span class="sxs-lookup"><span data-stu-id="7f967-105">When the schedule that is selected in the batch process is **Short-term lease liability reclass**, a journal entry is created.</span></span> <span data-ttu-id="7f967-106">Эта запись используется для разноски текущей части арендного обязательства в последний день месяца.</span><span class="sxs-lookup"><span data-stu-id="7f967-106">This entry is used to post the current portion of the lease liability on the last day of the month.</span></span> <span data-ttu-id="7f967-107">В то же время запись сторнирования разносится на первый день следующего месяца.</span><span class="sxs-lookup"><span data-stu-id="7f967-107">At the same time, a reversal entry is posted as of the first day of the next month.</span></span>

<span data-ttu-id="7f967-108">Краткосрочная часть арендного обязательства показана в графике амортизации обязательства.</span><span class="sxs-lookup"><span data-stu-id="7f967-108">The short-term portion of the lease liability is shown on the liability amortization schedule.</span></span> <span data-ttu-id="7f967-109">При разноске записи журнала становится доступным столбец **Создан журнал изменения классификации обязательства**, а код журнала также заполняется на графике.</span><span class="sxs-lookup"><span data-stu-id="7f967-109">When the journal entry is posted, the **Liability reclass journal created** column becomes available, and the journal ID is also filled in on the schedule.</span></span>

<span data-ttu-id="7f967-110">Чтобы создать и разнести запись журнала изменения классификации краткосрочных обязательств, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7f967-110">To create and post the short-term liability reclassification journal entry, follow these steps.</span></span>

1. <span data-ttu-id="7f967-111">Перейдите в раздел **Аренда активов \> Периодические задачи \> Создание журнала пакетных заданий**.</span><span class="sxs-lookup"><span data-stu-id="7f967-111">Go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span>
2. <span data-ttu-id="7f967-112">В диалоговом окне **Создание журнала пакетных заданий** в поле **Выберите график** выберите вариант **Изменение классификации краткосрочных арендных обязательств**.</span><span class="sxs-lookup"><span data-stu-id="7f967-112">In the **Batch journal creation** dialog box, in the **Select schedule** field, select **Short-term lease liability reclass**.</span></span>
3. <span data-ttu-id="7f967-113">В поле **Группа аренды** выберите группу аренды.</span><span class="sxs-lookup"><span data-stu-id="7f967-113">In the **Lease group** field, select a lease group.</span></span> <span data-ttu-id="7f967-114">В качестве альтернативы, в поле **Код книги** выберите код книги.</span><span class="sxs-lookup"><span data-stu-id="7f967-114">Alternatively, in the **Book ID** field, select the book ID.</span></span>
4. <span data-ttu-id="7f967-115">Включите параметр **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="7f967-115">Turn on the **Post** parameter.</span></span> <span data-ttu-id="7f967-116">В качестве альтернативы, если запись должна быть создана, но не разнесена, оставьте этот параметр отключенным.</span><span class="sxs-lookup"><span data-stu-id="7f967-116">Alternatively, if the entry should be created but not posted, leave this parameter turned off.</span></span>
5. <span data-ttu-id="7f967-117">Включите параметр **Предварительный просмотр перед разноской**, чтобы просмотреть запись до ее разноски.</span><span class="sxs-lookup"><span data-stu-id="7f967-117">Turn on the **Preview before posting** parameter to view the entry before it's posted.</span></span>
6. <span data-ttu-id="7f967-118">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7f967-118">Select **OK**.</span></span>