---
title: Предложение по приобретению ОС
description: Этот раздел описывает, как приобрести основное средство с помощью предложения по приобретению в журнале основных средств.
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
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
ms.openlocfilehash: 0997af638c141661afb677e2407a90a883168aed
ms.sourcegitcommit: a8201e0b9033c2afc2b1702b0337facaf7ad4b92
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/28/2020
ms.locfileid: "3628893"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="1d0fa-103">Предложение по приобретению ОС</span><span class="sxs-lookup"><span data-stu-id="1d0fa-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1d0fa-104">Этот раздел описывает, как приобрести основное средство с помощью предложения по приобретению в журнале основных средств.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="1d0fa-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="1d0fa-106">Чтобы получить основные средства с помощью журнала предложений по основным средствам, необходимо сначала создать запись ОС, а затем определить цену приобретения в журнале активов.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="1d0fa-107">В области перехода, перейдите к **Модули > Основные средства > Записи журнала > Журнал основных средств**.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="1d0fa-108">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-108">Select **New**.</span></span>
3. <span data-ttu-id="1d0fa-109">В поле **Имя** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="1d0fa-110">На панели операций выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="1d0fa-111">Выберите **Предложения**.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="1d0fa-112">Выберите в **Предложение по вводу в эксплуатацию**.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="1d0fa-113">Выберите **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-113">Select **Filter**.</span></span> <span data-ttu-id="1d0fa-114">Выберите **Сброс**, чтобы сбросить вне предыдущие значения.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="1d0fa-115">Выберите строку **Инв. номер ОС**.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="1d0fa-116">В поле **Критерии** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="1d0fa-117">Настройте оставшиеся критерии для основных средств, которые необходимо приобрести с этим предложением.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="1d0fa-118">Выберите **OK** дважды, чтобы выйти из панели.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="1d0fa-119">Проверьте созданные строки проводки.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="1d0fa-120">Только основные средства, для которых заданы параметры даты приобретения и цены приобретения в книге, будут включены в предложение по приобретению.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="1d0fa-121">На странице выберите вкладку **Книги**.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="1d0fa-122">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-122">Select **Post**.</span></span>
