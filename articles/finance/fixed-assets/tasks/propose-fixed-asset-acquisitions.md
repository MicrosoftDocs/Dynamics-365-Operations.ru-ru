---
title: Предложение по приобретению ОС
description: Этот раздел описывает, как приобрести основное средство с помощью предложения по приобретению в журнале основных средств.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817180"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="3e3c9-103">Предложение по приобретению ОС</span><span class="sxs-lookup"><span data-stu-id="3e3c9-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e3c9-104">Этот раздел описывает, как приобрести основное средство с помощью предложения по приобретению в журнале основных средств.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="3e3c9-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="3e3c9-106">Чтобы получить основные средства с помощью журнала предложений по основным средствам, необходимо сначала создать запись ОС, а затем определить цену приобретения в журнале активов.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

## <a name="create-an-asset-acquisition-proposal"></a><span data-ttu-id="3e3c9-107">Создание предложения по приобретению актива</span><span class="sxs-lookup"><span data-stu-id="3e3c9-107">Create an asset acquisition proposal</span></span>

<span data-ttu-id="3e3c9-108">Выполните следующие действия, чтобы создать предложение по приобретению актива.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-108">Complete the following steps to create an asset acquisition proposal.</span></span> 

1. <span data-ttu-id="3e3c9-109">В области перехода, перейдите к **Модули > Основные средства > Записи журнала > Журнал основных средств**.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-109">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="3e3c9-110">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-110">Select **New**.</span></span>
3. <span data-ttu-id="3e3c9-111">В поле **Имя** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="3e3c9-112">На панели действий выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-112">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="3e3c9-113">Выберите **Предложения**.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-113">Select **Proposals**.</span></span>
6. <span data-ttu-id="3e3c9-114">Выберите в **Предложение по вводу в эксплуатацию**.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-114">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="3e3c9-115">Выберите **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-115">Select **Filter**.</span></span> <span data-ttu-id="3e3c9-116">Выберите **Сброс**, чтобы сбросить предыдущие значения.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-116">Select **Reset** to clear previous values.</span></span>
8. <span data-ttu-id="3e3c9-117">Выберите строку **Инв. номер ОС**.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-117">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="3e3c9-118">В поле **Критерии** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-118">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="3e3c9-119">Настройте оставшиеся критерии для основных средств, которые необходимо приобрести с этим предложением.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-119">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="3e3c9-120">Выберите **OK** дважды, чтобы выйти из панели.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-120">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="3e3c9-121">Проверьте, что строки проводки созданы.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-121">Verify that the transaction lines are created.</span></span>  
- <span data-ttu-id="3e3c9-122">Только основные средства, для которых заданы параметры даты приобретения и цены приобретения в книге, будут включены в предложение по приобретению.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-122">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="3e3c9-123">На странице выберите вкладку **Книги**.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-123">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="3e3c9-124">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-124">Select **Post**.</span></span>

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a><span data-ttu-id="3e3c9-125">Включение финансовых аналитик по умолчанию в предложение по приобретению</span><span class="sxs-lookup"><span data-stu-id="3e3c9-125">Include default financial dimensions in an acquisition proposal</span></span>

<span data-ttu-id="3e3c9-126">Проводка приобретения может быть создана с помощью надстроек Excel путем перехода к пункту **Основные средства > Записи журнала > Журнал основных средств**.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-126">The acquisition transaction can be created using Excel add-ins, by going to **Fixed assets > Journal entries > Fixed asset journal**.</span></span> <span data-ttu-id="3e3c9-127">Создайте новый журнал и перейдите в раздел **Строки** на странице и выберите значок Microsoft Excel, затем выберите строку журнала основных средств.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-127">Create a new journal and move to the **Lines** section on the page and select the Excel icon, and then select a Fixed asset journal line.</span></span> <span data-ttu-id="3e3c9-128">В системе будет создан и открыт шаблон Excel, представляющий строки журнала.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-128">The system will create and open an Excel template representing journal lines.</span></span> <span data-ttu-id="3e3c9-129">Можно добавить данные для строк журнала, добавляемых в шаблон, затем опубликуйте эту информацию обратно в системе.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-129">You can add data for the journal lines you're adding into the template, and then publish that information back into the system.</span></span> 

<span data-ttu-id="3e3c9-130">Если аналитики по умолчанию были настроены для выбранной книги активов и соответствующие основные средства, введенные в шаблон Excel, финансовые аналитики по умолчанию будут вызываться из основных данных журнала активов, когда журнал публикуется из Excel в системе.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-130">If default dimensions have been set up for the selected asset book and the corresponding fixed assets that were entered in the Excel template, the default financial dimensions will be called from the asset book master data when the journal is published from the Excel to the system.</span></span> <span data-ttu-id="3e3c9-131">Для автоматического включения финансовых аналитик в журнал активов при публикации журнала основных средств из надстройки Excel необходимо заранее настроить аналитики по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3e3c9-131">To include financial dimensions on an asset book automatically while publishing the fixed asset journal from the Excel add-in, the default dimensions must be set up in advance.</span></span>  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
