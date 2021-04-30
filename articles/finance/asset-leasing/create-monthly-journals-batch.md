---
title: Создание ежемесячных записей в журнале в пакетном режиме
description: В этой теме объясняется, как создавать записи журнала в пакетном режиме для повышения эффективности при записи ежемесячных арендных расходов.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ca84e56569ea5ddbb4d5335d0944a6bd8a50a1b1
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881212"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="0b972-103">Создание ежемесячных записей в журнале в пакетном режиме</span><span class="sxs-lookup"><span data-stu-id="0b972-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b972-104">В этой теме объясняется, как создавать записи журнала в пакетном режиме для повышения эффективности при записи ежемесячных арендных расходов.</span><span class="sxs-lookup"><span data-stu-id="0b972-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="0b972-105">Пакетная обработка может использоваться для создания записей журнала из нескольких расписаний.</span><span class="sxs-lookup"><span data-stu-id="0b972-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="0b972-106">Эти записи журнала могут включать арендные платежи, амортизацию обязательств, амортизацию активов в форме права пользования (ФПП) и расходы на затраты по осуществлению аренды.</span><span class="sxs-lookup"><span data-stu-id="0b972-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="0b972-107">Можно также использовать пакетную обработку для первоначального признания нескольких аренд в одно и то же время, либо для одновременного создания корректировок перехода для нескольких аренд.</span><span class="sxs-lookup"><span data-stu-id="0b972-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="0b972-108">Чтобы настроить пакетное задание или обработать накладные платежей, амортизацию или проценты для нескольких аренд, перейдите в раздел **Аренда активов \> Периодические задачи \> Создание журнала пакетных заданий**.</span><span class="sxs-lookup"><span data-stu-id="0b972-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="0b972-109">В появившемся диалоговом окне можно выбрать график, из которого должны создаваться записи журнала.</span><span class="sxs-lookup"><span data-stu-id="0b972-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="0b972-110">Можно также указать, следует ли выполнять пакетный процесс для конкретных сущностей, групп аренды или книг аренды.</span><span class="sxs-lookup"><span data-stu-id="0b972-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="0b972-111">Последующие проводки, такие как графики амортизации обязательств, платежи, амортизация и расходы, будут разнесены только после разноски исходного признания для соответствующих аренд.</span><span class="sxs-lookup"><span data-stu-id="0b972-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="0b972-112">Записи журнала создаются, но не разносятся, до тех пор, пока не будет выбрана команда **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="0b972-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
