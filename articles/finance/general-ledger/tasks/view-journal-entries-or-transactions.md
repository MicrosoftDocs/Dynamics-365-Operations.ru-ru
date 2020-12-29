---
title: Просмотр записей или проводок в журнале
description: В этой процедуре показано, как использовать запрос проводок по ваучеру для поиска записей журнала или проводок.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, LedgerTransVoucher, LedgerTransBase, Originaldocuments
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f463b7764288918609cba364acf342eed28ad929
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447083"
---
# <a name="view-journal-entries-or-transactions"></a><span data-ttu-id="17731-103">Просмотр записей или проводок в журнале</span><span class="sxs-lookup"><span data-stu-id="17731-103">View journal entries or transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17731-104">В этой процедуре показано, как использовать запрос проводок по ваучеру для поиска записей журнала или проводок.</span><span class="sxs-lookup"><span data-stu-id="17731-104">This procedure shows how to use the Voucher transactions inquiry to search for journal entries or transactions.</span></span>

1. <span data-ttu-id="17731-105">Выберите **Область перехода > Модули > Главная книга > Запросы и отчеты > Проводки по ваучеру**.</span><span class="sxs-lookup"><span data-stu-id="17731-105">Go to **Navigation pane > Modules > General ledger > Inquiries and reports > Voucher transactions**.</span></span>
2. <span data-ttu-id="17731-106">Выберите поле для которого требуется определить критерии фильтра.</span><span class="sxs-lookup"><span data-stu-id="17731-106">Select the field for which you want to define a filter criteria.</span></span>
3. <span data-ttu-id="17731-107">Введите свои критерии фильтра для выбранного поля.</span><span class="sxs-lookup"><span data-stu-id="17731-107">Enter your filter critieria for the selected field.</span></span> <span data-ttu-id="17731-108">Можно фильтровать по одному значению или по диапазону.</span><span class="sxs-lookup"><span data-stu-id="17731-108">You could filter on a single value or a range.</span></span> <span data-ttu-id="17731-109">При определении диапазона убедитесь, что используется правильный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="17731-109">When defining a range, make sure the correct syntax is used.</span></span> <span data-ttu-id="17731-110">Значения должны быть разделены двумя точками (..).</span><span class="sxs-lookup"><span data-stu-id="17731-110">The values should be separated by a double period (..).</span></span>  
4. <span data-ttu-id="17731-111">Щелкните вкладку **Соединения** для добавления дополнительных таблиц, из которых будет выполняться фильтрация.</span><span class="sxs-lookup"><span data-stu-id="17731-111">Click the **Joins** tab to add additional tables from which to filter.</span></span>
5. <span data-ttu-id="17731-112">В дереве выберите **Таблицы/Запись в общем журнале**.</span><span class="sxs-lookup"><span data-stu-id="17731-112">In the tree, select **Tables/General journal entry**.</span></span>
6. <span data-ttu-id="17731-113">Щелкните **Добавить соединение таблицы**.</span><span class="sxs-lookup"><span data-stu-id="17731-113">Click **Add table join**.</span></span>
7. <span data-ttu-id="17731-114">Нажмите кнопку **Отмена**, если вы решили не добавлять дополнительную таблицу.</span><span class="sxs-lookup"><span data-stu-id="17731-114">Click **Cancel** if you decide not to add an additional table.</span></span>
8. <span data-ttu-id="17731-115">Перейдите на вкладку **Диапазон**.</span><span class="sxs-lookup"><span data-stu-id="17731-115">Click the **Range** tab.</span></span>
9. <span data-ttu-id="17731-116">Для выполнения запроса нажмите кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="17731-116">Click **OK** to run the query.</span></span>
10. <span data-ttu-id="17731-117">На панели операций щелкните **Источник проводки**.</span><span class="sxs-lookup"><span data-stu-id="17731-117">On the Action pane, click **Transaction origin**.</span></span> <span data-ttu-id="17731-118">Различные кнопки рядом с сеткой можно использовать, чтобы исследовать дополнительные сведения о выбранной записи ваучера.</span><span class="sxs-lookup"><span data-stu-id="17731-118">Various buttons about the grid can be used to research additional information about the selected record of the voucher.</span></span> <span data-ttu-id="17731-119">Некоторые кнопки могут быть недоступны в зависимости от типа проводки и свойств проводки.</span><span class="sxs-lookup"><span data-stu-id="17731-119">Some buttons may not be available, depending on the type of transaction and characteristics of the transaction.</span></span>
11. <span data-ttu-id="17731-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="17731-120">Close the page.</span></span>
12. <span data-ttu-id="17731-121">На панели операций щелкните **Исходный документ**.</span><span class="sxs-lookup"><span data-stu-id="17731-121">On the Action pane, Click **Original document**.</span></span>
13. <span data-ttu-id="17731-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="17731-122">Close the page.</span></span>

