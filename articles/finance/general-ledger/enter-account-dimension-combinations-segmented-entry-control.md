---
title: Ввод комбинаций счета и аналитики (элемент управления сегментированным вводом)
description: В этой статье описывается порядок ввода сочетания накладной и аналитики или счетов ГК. Процедуру записи часто называют поделенное на сегменты управление записью.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: roschlom
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bed6a13a721269550fa72c495e7ecfddadf9d8b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260789"
---
# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="62d1f-104">Ввод комбинаций счета и аналитики (элемент управления сегментированным вводом)</span><span class="sxs-lookup"><span data-stu-id="62d1f-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62d1f-105">В этой статье описывается порядок ввода сочетания накладной и аналитики или счетов ГК.</span><span class="sxs-lookup"><span data-stu-id="62d1f-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="62d1f-106">Процедуру записи часто называют поделенное на сегменты управление записью.</span><span class="sxs-lookup"><span data-stu-id="62d1f-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="62d1f-107">Пользователи вводят комбинации счета и аналитики на различных страницах, таких как страницы для общих журналов, бюджетирования и определений разноски.</span><span class="sxs-lookup"><span data-stu-id="62d1f-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="62d1f-108">Действительные комбинации счета и аналитики зависят от структур счета, которые назначены ГК, и дополнительных правил, которые назначена структурам счета.</span><span class="sxs-lookup"><span data-stu-id="62d1f-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="62d1f-109">Когда пользователи вводят комбинацию, они могут вручную ввести значения или воспользоваться богатым опытом поиска.</span><span class="sxs-lookup"><span data-stu-id="62d1f-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="62d1f-110">При вводе в поле можно начать печатать, и будет выполнен поиск значения и описание.</span><span class="sxs-lookup"><span data-stu-id="62d1f-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="62d1f-111">Например, если ввести 180, будет выполнен поиск любого значения, которое начинается с этой комбинации цифр.</span><span class="sxs-lookup"><span data-stu-id="62d1f-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="62d1f-112">Или можно ввести "Касса", и будет выполнен поиск любого значения, которое имеет описание, начинающее со слова "Касса".</span><span class="sxs-lookup"><span data-stu-id="62d1f-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="62d1f-113">Также можно использовать подстановочные знаки, такие как \*Касса или \*180, для поиска, содержит ли значение или описание критерии поиска.</span><span class="sxs-lookup"><span data-stu-id="62d1f-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="62d1f-114">В следующей таблице описываются сочетания клавиш, которые можно использовать, если поиск закрыт.</span><span class="sxs-lookup"><span data-stu-id="62d1f-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62d1f-115">Сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="62d1f-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="62d1f-116">Действие</span><span class="sxs-lookup"><span data-stu-id="62d1f-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="62d1f-117">ALT + СТРЕЛКА ВНИЗ</span><span class="sxs-lookup"><span data-stu-id="62d1f-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="62d1f-118">Открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="62d1f-118">Open the lookup.</span></span> <span data-ttu-id="62d1f-119">Если нажать "ALT + СТРЕЛКА ВНИЗ" во второй раз, фокус переместится на сегменты в макете.</span><span class="sxs-lookup"><span data-stu-id="62d1f-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="62d1f-120">ВВОД и SHIFT + ВВОД</span><span class="sxs-lookup"><span data-stu-id="62d1f-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="62d1f-121">Разграничитель плана счетов</span><span class="sxs-lookup"><span data-stu-id="62d1f-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="62d1f-122">СТРЕЛКА ВПРАВО и СТРЕЛКА ВЛЕВО</span><span class="sxs-lookup"><span data-stu-id="62d1f-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="62d1f-123">Перейти к следующему или предыдущему сегменту.</span><span class="sxs-lookup"><span data-stu-id="62d1f-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62d1f-124">Табуляция</span><span class="sxs-lookup"><span data-stu-id="62d1f-124">Tab</span></span></td>
<td><span data-ttu-id="62d1f-125">Перейти к следующему полю в сетке.</span><span class="sxs-lookup"><span data-stu-id="62d1f-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="62d1f-126">В следующей таблице описываются сочетания клавиш, которые можно использовать, если поиск открыт.</span><span class="sxs-lookup"><span data-stu-id="62d1f-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62d1f-127">Сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="62d1f-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="62d1f-128">Действие</span><span class="sxs-lookup"><span data-stu-id="62d1f-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="62d1f-129">ESC</span><span class="sxs-lookup"><span data-stu-id="62d1f-129">Esc</span></span></td>
<td><span data-ttu-id="62d1f-130">Закрыть поиск.</span><span class="sxs-lookup"><span data-stu-id="62d1f-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="62d1f-131">СТРЕЛКА ВВЕРХ и СТРЕЛКА ВНИЗ</span><span class="sxs-lookup"><span data-stu-id="62d1f-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="62d1f-132">PAGE UP и PAGE DOWN</span><span class="sxs-lookup"><span data-stu-id="62d1f-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="62d1f-133">HOME и END</span><span class="sxs-lookup"><span data-stu-id="62d1f-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="62d1f-134">Перейти к предыдущему или следующему значению в списках, к предыдущей или следующей группе значений либо к первому или последнему элементу в поиске.</span><span class="sxs-lookup"><span data-stu-id="62d1f-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="62d1f-135">Разграничитель плана счетов</span><span class="sxs-lookup"><span data-stu-id="62d1f-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="62d1f-136">СТРЕЛКА ВПРАВО и СТРЕЛКА ВЛЕВО</span><span class="sxs-lookup"><span data-stu-id="62d1f-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="62d1f-137">Перейти к следующему или предыдущему сегменту.</span><span class="sxs-lookup"><span data-stu-id="62d1f-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62d1f-138">Вкладка</span><span class="sxs-lookup"><span data-stu-id="62d1f-138">Tab</span></span></td>
<td><span data-ttu-id="62d1f-139">Перейти к следующему полю в сетке.</span><span class="sxs-lookup"><span data-stu-id="62d1f-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62d1f-140">ALT + W</span><span class="sxs-lookup"><span data-stu-id="62d1f-140">Alt+W</span></span></td>
<td><span data-ttu-id="62d1f-141">Переключиться между режимами <strong>Показать все</strong> и <strong>Показать допустимый текст</strong>.</span><span class="sxs-lookup"><span data-stu-id="62d1f-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]