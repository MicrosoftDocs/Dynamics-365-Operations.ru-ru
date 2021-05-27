---
title: Параметры реверсирования в журналах и строках
description: В этом разделе описывается, почему запись реверсирования, которая была введена в общем журнале, может быть не включена в разнесенную проводку.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028582"
---
# <a name="reverse-settings-on-journals-and-lines"></a><span data-ttu-id="1eda1-103">Параметры реверсирования в журналах и строках</span><span class="sxs-lookup"><span data-stu-id="1eda1-103">Reverse settings on journals and lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1eda1-104">В этом разделе описывается, почему запись реверсирования, которая была введена в общем журнале, может быть не включена в разнесенную проводку.</span><span class="sxs-lookup"><span data-stu-id="1eda1-104">This topic addresses why a reversing entry that was entered on a general journal might not be included on the posted transaction.</span></span>  

## <a name="symptom"></a><span data-ttu-id="1eda1-105">Симптом</span><span class="sxs-lookup"><span data-stu-id="1eda1-105">Symptom</span></span>

<span data-ttu-id="1eda1-106">Общий журнал включает запись реверсирования и дату реверсирования в журнале.</span><span class="sxs-lookup"><span data-stu-id="1eda1-106">A general journal includes a reversing entry and reversing date on the journal.</span></span> <span data-ttu-id="1eda1-107">При разноске журнала ни один из ваучеров не реверсируется.</span><span class="sxs-lookup"><span data-stu-id="1eda1-107">When you post the journal, none of the vouchers are reversed.</span></span> <span data-ttu-id="1eda1-108">Почему это происходит?</span><span class="sxs-lookup"><span data-stu-id="1eda1-108">Why does this happen?</span></span>

## <a name="resolution"></a><span data-ttu-id="1eda1-109">Решение</span><span class="sxs-lookup"><span data-stu-id="1eda1-109">Resolution</span></span>

<span data-ttu-id="1eda1-110">При разноске журнала в процессе реверсирования рассматриваются только параметры **Запись реверсирования** и **Дата реверсирования** в разделе **Строки** ваучера.</span><span class="sxs-lookup"><span data-stu-id="1eda1-110">When the journal is posted, the reversing process looks only at the **Revering entry** and **Reversing date** settings on the **Lines** section of the voucher.</span></span> <span data-ttu-id="1eda1-111">Такой подход позволяет включить в журнал некоторые ваучеры, которые помечены для реверсирования, и другие ваучеры, которые не помечены для реверсирования.</span><span class="sxs-lookup"><span data-stu-id="1eda1-111">This approach allows a journal to include some vouchers that are marked for reversing, and others that are not.</span></span>

<span data-ttu-id="1eda1-112">Значения из журнала используются только в качестве значений по умолчанию при добавлении *новых* строк.</span><span class="sxs-lookup"><span data-stu-id="1eda1-112">The values from the journal are only used as defaults when adding *new* lines.</span></span> <span data-ttu-id="1eda1-113">Изменение значений в журнале не влияет на существующие строки.</span><span class="sxs-lookup"><span data-stu-id="1eda1-113">Changing the values on the journal doesn’t affect existing lines.</span></span> <span data-ttu-id="1eda1-114">В этом примере сначала были введены строки ваучеров.</span><span class="sxs-lookup"><span data-stu-id="1eda1-114">In this example, the voucher lines were entered first.</span></span> <span data-ttu-id="1eda1-115">При вводе сведений о строке перед назначением журнала как реверсированного, назначение в качестве записи и даты реверсирования не будет применено к существующим строкам.</span><span class="sxs-lookup"><span data-stu-id="1eda1-115">When you enter the line detail before designating the journal as reversing, the designation as a reversing entry and date won't be applied to any existing lines.</span></span>

<span data-ttu-id="1eda1-116">Изменение записи реверсирования или даты реверсирования в существующей строке распространяет это изменение на другие строки в том же ваучере.</span><span class="sxs-lookup"><span data-stu-id="1eda1-116">Changing the reversing entry or reversing date on an existing line propagates that change to other lines in the same voucher.</span></span> <span data-ttu-id="1eda1-117">Для оптимизации производительности сетка не обновляется после распространения изменений на другие строки.</span><span class="sxs-lookup"><span data-stu-id="1eda1-117">To optimize performance, the grid is not refreshed after propagating changes to other Lines.</span></span> <span data-ttu-id="1eda1-118">Вы можете отобразить обновленные значения, обновив сетку.</span><span class="sxs-lookup"><span data-stu-id="1eda1-118">You can display the updated values by refreshing the grid.</span></span>


