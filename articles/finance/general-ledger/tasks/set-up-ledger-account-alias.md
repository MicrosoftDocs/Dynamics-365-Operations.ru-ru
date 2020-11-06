---
title: Настройка псевдонима счета ГК
description: Ниже описан порядок создания псевдонима счета, который обеспечивает ярлык для ввода номера счета.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccountAlias
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1764f31c98039e9ea6f665dcb04a1cfd23c31dc
ms.sourcegitcommit: 3feccc9facb33e3dee18f04e202f7b20785df0a8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998856"
---
# <a name="set-up-a-ledger-account-alias"></a><span data-ttu-id="8740b-103">Настройка псевдонима счета ГК</span><span class="sxs-lookup"><span data-stu-id="8740b-103">Set up a ledger account alias</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8740b-104">Ниже описан порядок создания псевдонима счета, который обеспечивает ярлык для ввода номера счета.</span><span class="sxs-lookup"><span data-stu-id="8740b-104">This procedure shows how to create an account alias that provides a shortcut for entering an account number.</span></span> <span data-ttu-id="8740b-105">В этой процедуре используется компания с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="8740b-105">This procedure uses demo data company USMF.</span></span>

1. <span data-ttu-id="8740b-106">Перейдите в раздел "Главная книга" > "План счетов" > "Счета" > "Псевдоним счета учета".</span><span class="sxs-lookup"><span data-stu-id="8740b-106">Go to General ledger > Chart of accounts > Accounts > Ledger account alias.</span></span>
2. <span data-ttu-id="8740b-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8740b-107">Click New.</span></span>
3. <span data-ttu-id="8740b-108">В поле "Псевдоним счета учета" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8740b-108">In the Ledger account alias field, type a value.</span></span>
4. <span data-ttu-id="8740b-109">В поле "Структура счета" выберите структуру, которой принадлежат счет и аналитики.</span><span class="sxs-lookup"><span data-stu-id="8740b-109">In the Account structure field, select the structure the account and dimensions belong to.</span></span>
5. <span data-ttu-id="8740b-110">В поле "Компания" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8740b-110">In the Company field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="8740b-111">В списке найдите и выберите компанию, к которой применяется псевдоним.</span><span class="sxs-lookup"><span data-stu-id="8740b-111">In the list, find and select the company that the alias applies to.</span></span>
7. <span data-ttu-id="8740b-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8740b-112">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="8740b-113">В поле "Определение псевдонима счета учета" укажите счет и аналитики.</span><span class="sxs-lookup"><span data-stu-id="8740b-113">In the Ledger account alias definition field, specify the account and dimensions.</span></span>
    * <span data-ttu-id="8740b-114">Счет и аналитики будут заполнены при использовании ярлыка.</span><span class="sxs-lookup"><span data-stu-id="8740b-114">The account and dimensions will be populated when using the shortcut.</span></span>  
9. <span data-ttu-id="8740b-115">В поле "Первоначальное фокусирование" выберите аналитику, которая будет фокусироваться, где будет использоваться псевдоним.</span><span class="sxs-lookup"><span data-stu-id="8740b-115">In the Initial focus field, select the dimension that will have focus when the alias is used.</span></span>
    * <span data-ttu-id="8740b-116">После ввода ярлыка и заполнения счета и аналитик поле "Первоначальное фокусирование" находится там, где курсор, или куда перемещается фокус.</span><span class="sxs-lookup"><span data-stu-id="8740b-116">After you type the shortcut, and the account and dimensions are populated, the Initial focus field is where the cursor or focus will move to.</span></span>  

