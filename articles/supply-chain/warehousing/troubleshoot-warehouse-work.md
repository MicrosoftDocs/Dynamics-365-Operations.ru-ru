---
title: Устранение неполадок работы склада
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с работой склада в Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 3015ec777953cedb5a5d8eea873ed1043cac04cb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970251"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="9a755-103">Устранение неполадок работы склада</span><span class="sxs-lookup"><span data-stu-id="9a755-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a755-104">В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с работой склада в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9a755-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="9a755-105">Не удается переместить грузоместа с серийными номерами номенклатуры, если для группы аналитик отслеживания разрешены пустой расход и пустой приход.</span><span class="sxs-lookup"><span data-stu-id="9a755-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9a755-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="9a755-106">Issue description</span></span>

<span data-ttu-id="9a755-107">Нельзя переместить грузоместо, используя пункт меню **Перемещение**, если серийный номер имеет настройки *Пропуск для расходов* и *Пропуск для приходов* в группе аналитик отслеживания, и если в одном местоположении имеется несколько грузомест, некоторые из которых имеют серийные номера, а другие — не имеют.</span><span class="sxs-lookup"><span data-stu-id="9a755-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9a755-108">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="9a755-108">Issue resolution</span></span>

<span data-ttu-id="9a755-109">Эта проблема будет устранена изменениями, которые разворачиваются в [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span><span class="sxs-lookup"><span data-stu-id="9a755-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="9a755-110">Эти изменения сделают поле **Серийный номер** необязательным, если разрешены пустой прием и пустой расход.</span><span class="sxs-lookup"><span data-stu-id="9a755-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="9a755-111">При обработке перемещений в приложении склада выводится следующее сообщение об ошибке: "Владелец запасов %1не разрешен в этом процессе."</span><span class="sxs-lookup"><span data-stu-id="9a755-111">I receive the following error message in the warehouse app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9a755-112">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="9a755-112">Issue description</span></span>

<span data-ttu-id="9a755-113">Аналитика отслеживания **Владелец** отсутствует, если приложение склада используется для выполнения перемещений.</span><span class="sxs-lookup"><span data-stu-id="9a755-113">The **Owner** tracking dimension is missing when the warehouse app is used to make movements.</span></span> <span data-ttu-id="9a755-114">Обычный журнал перемещения запасов из клиента Supply Chain Management будет работать правильно и может быть разнесен только в том случае, если заполнена аналитика **Владелец**.</span><span class="sxs-lookup"><span data-stu-id="9a755-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9a755-115">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="9a755-115">Issue resolution</span></span>

<span data-ttu-id="9a755-116">Корпорация Майкрософт проверила эту проблему и определила, что она является ограничением функции.</span><span class="sxs-lookup"><span data-stu-id="9a755-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="9a755-117">В настоящее время процессы управления складом поддерживают только запасы, которыми владеет юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="9a755-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>
