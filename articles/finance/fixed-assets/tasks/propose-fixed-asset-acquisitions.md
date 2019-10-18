---
title: Предложение по приобретению ОС
description: Этот раздел описывает, как приобрести основное средство с помощью предложения по приобретению в журнале основных средств.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b35b13dc266fd5bccde437526400832d394b9aa
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179566"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="8678f-103">Предложение по приобретению ОС</span><span class="sxs-lookup"><span data-stu-id="8678f-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8678f-104">Этот раздел описывает, как приобрести основное средство с помощью предложения по приобретению в журнале основных средств.</span><span class="sxs-lookup"><span data-stu-id="8678f-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="8678f-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="8678f-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="8678f-106">В области перехода, перейдите к **Модули > Основные средства > Записи журнала > Журнал основных средств**.</span><span class="sxs-lookup"><span data-stu-id="8678f-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="8678f-107">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="8678f-107">Select **New**.</span></span>
3. <span data-ttu-id="8678f-108">В поле **Имя** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8678f-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="8678f-109">На панели операций выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="8678f-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="8678f-110">Выберите **Предложения**.</span><span class="sxs-lookup"><span data-stu-id="8678f-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="8678f-111">Выберите в **Предложение по вводу в эксплуатацию**.</span><span class="sxs-lookup"><span data-stu-id="8678f-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="8678f-112">Выберите **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="8678f-112">Select **Filter**.</span></span> <span data-ttu-id="8678f-113">Выберите **Сброс**, чтобы сбросить вне предыдущие значения.</span><span class="sxs-lookup"><span data-stu-id="8678f-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="8678f-114">Выберите строку **Инв. номер ОС**.</span><span class="sxs-lookup"><span data-stu-id="8678f-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="8678f-115">В поле **Критерии** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8678f-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="8678f-116">Настройте оставшиеся критерии для основных средств, которые необходимо приобрести с этим предложением.</span><span class="sxs-lookup"><span data-stu-id="8678f-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="8678f-117">Выберите **OK** дважды, чтобы выйти из панели.</span><span class="sxs-lookup"><span data-stu-id="8678f-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="8678f-118">Проверьте созданные строки проводки.</span><span class="sxs-lookup"><span data-stu-id="8678f-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="8678f-119">Только основные средства, для которых заданы параметры даты приобретения и цены приобретения в книге, будут включены в предложение по приобретению.</span><span class="sxs-lookup"><span data-stu-id="8678f-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="8678f-120">На странице выберите вкладку **Книги**.</span><span class="sxs-lookup"><span data-stu-id="8678f-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="8678f-121">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="8678f-121">Select **Post**.</span></span>

