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
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839913"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="51690-103">Предложение по приобретению ОС</span><span class="sxs-lookup"><span data-stu-id="51690-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51690-104">Этот раздел описывает, как приобрести основное средство с помощью предложения по приобретению в журнале основных средств.</span><span class="sxs-lookup"><span data-stu-id="51690-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="51690-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="51690-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="51690-106">В области перехода, перейдите к **Модули > Основные средства > Записи журнала > Журнал основных средств**.</span><span class="sxs-lookup"><span data-stu-id="51690-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="51690-107">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="51690-107">Select **New**.</span></span>
3. <span data-ttu-id="51690-108">В поле **Имя** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="51690-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="51690-109">На панели операций выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="51690-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="51690-110">Выберите **Предложения**.</span><span class="sxs-lookup"><span data-stu-id="51690-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="51690-111">Выберите в **Предложение по вводу в эксплуатацию**.</span><span class="sxs-lookup"><span data-stu-id="51690-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="51690-112">Выберите **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="51690-112">Select **Filter**.</span></span> <span data-ttu-id="51690-113">Выберите **Сброс**, чтобы сбросить вне предыдущие значения.</span><span class="sxs-lookup"><span data-stu-id="51690-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="51690-114">Выберите строку **Инв. номер ОС**.</span><span class="sxs-lookup"><span data-stu-id="51690-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="51690-115">В поле **Критерии** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="51690-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="51690-116">Настройте оставшиеся критерии для основных средств, которые необходимо приобрести с этим предложением.</span><span class="sxs-lookup"><span data-stu-id="51690-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="51690-117">Выберите **OK** дважды, чтобы выйти из панели.</span><span class="sxs-lookup"><span data-stu-id="51690-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="51690-118">Проверьте созданные строки проводки.</span><span class="sxs-lookup"><span data-stu-id="51690-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="51690-119">Только основные средства, для которых заданы параметры даты приобретения и цены приобретения в книге, будут включены в предложение по приобретению.</span><span class="sxs-lookup"><span data-stu-id="51690-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="51690-120">На странице выберите вкладку **Книги**.</span><span class="sxs-lookup"><span data-stu-id="51690-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="51690-121">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="51690-121">Select **Post**.</span></span>

