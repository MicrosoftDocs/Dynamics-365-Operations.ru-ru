---
title: "Обновление способа отображения сумм в отчетах и документах"
description: "В этом разделе представлена информация о том, как обновить способ отображения сумм в отчетах и других документах для Эстонии, Латвии, Литвы, Польши, Чехии, Венгрии и России."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264254
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a9e63af61b42ef3f5ef1d05a659cbec572e04a4f
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a><span data-ttu-id="05d0b-103">Обновление способа отображения сумм в отчетах и документах</span><span class="sxs-lookup"><span data-stu-id="05d0b-103">Update how amounts are displayed on reports and documents</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="05d0b-104">В этом разделе представлена информация о том, как обновить способ отображения сумм в отчетах и других документах для Эстонии, Латвии, Литвы, Польши, Чехии, Венгрии и России.</span><span class="sxs-lookup"><span data-stu-id="05d0b-104">This topic provides information about how to update how amounts are displayed on reports and other documents for Estonia, Latvia, Lithuania, Poland, Czech Republic, Hungary, and Russia.</span></span>

<span data-ttu-id="05d0b-105">Для юридических лиц в Эстонии, Латвии, Литве, Польше, Чехии, Венгрии и России можно настроить полные имена и краткие имена денежных единиц и субединиц.</span><span class="sxs-lookup"><span data-stu-id="05d0b-105">For legal entities in Estonia, Latvia, Lithuania, Poland, Czech Republic, Hungary, and Russia, you can set up full names and short names for currency units and subunits.</span></span> <span data-ttu-id="05d0b-106">Эти имена можно использовать для преобразования представления сумм в документах и отчетах.</span><span class="sxs-lookup"><span data-stu-id="05d0b-106">These names can be used to transform how amounts are represented on documents and reports.</span></span> <span data-ttu-id="05d0b-107">Например: сумма **100,20 литов** может отображаться как **100 литов 20 центов**.</span><span class="sxs-lookup"><span data-stu-id="05d0b-107">For example: The amount **LTL 100.20** can be displayed as **100 Litas 20 Centas**.</span></span>

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a><span data-ttu-id="05d0b-108">Настройка полных и кратких имен для денежных единиц и субединиц</span><span class="sxs-lookup"><span data-stu-id="05d0b-108">Set up full and short names for currency units and subunits</span></span>
<span data-ttu-id="05d0b-109">Чтобы настроить полные и краткие имена денежных единиц и субединиц для языка, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="05d0b-109">To set up full and short names for currency units and subunits for a language, complete the following steps:</span></span>

1.  <span data-ttu-id="05d0b-110">Откройте страницу **Валюты**.</span><span class="sxs-lookup"><span data-stu-id="05d0b-110">Open the **Currencies** page.</span></span>
2.  <span data-ttu-id="05d0b-111">Выбор валюты.</span><span class="sxs-lookup"><span data-stu-id="05d0b-111">Select a currency.</span></span>
3.  <span data-ttu-id="05d0b-112">В области действий щелкните **Склонение**.</span><span class="sxs-lookup"><span data-stu-id="05d0b-112">On the Action Pane, click **Declension**.</span></span>
4.  <span data-ttu-id="05d0b-113">Чтобы добавить полное имя и краткое имя для языка, щелкните **Создать** и заполните следующие поля.</span><span class="sxs-lookup"><span data-stu-id="05d0b-113">To add full name and short name for a language, click **New** and complete the following fields.</span></span>
    |                                                           |                                                                                                                                                                                                                    |
    |-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="05d0b-114">**Поле**</span><span class="sxs-lookup"><span data-stu-id="05d0b-114">**Field**</span></span>                                                 | <span data-ttu-id="05d0b-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="05d0b-115">**Description**</span></span>                                                                                                                                                                                                    |
    | <span data-ttu-id="05d0b-116">**Язык**</span><span class="sxs-lookup"><span data-stu-id="05d0b-116">**Language**</span></span>                                              | <span data-ttu-id="05d0b-117">Выбрать язык для текущего текста.</span><span class="sxs-lookup"><span data-stu-id="05d0b-117">Select the language for the current text.</span></span>                                                                                                                                                                          |
    | <span data-ttu-id="05d0b-118">**Именительный падеж единственное число (имя группы полей единиц)**</span><span class="sxs-lookup"><span data-stu-id="05d0b-118">**Singular nominative (Name of units field group)**</span></span>       | <span data-ttu-id="05d0b-119">Введите форму единственного числа для валюты.</span><span class="sxs-lookup"><span data-stu-id="05d0b-119">Enter the singular form of the currency.</span></span> <span data-ttu-id="05d0b-120">Например, форма единственного числа для литов — лит.</span><span class="sxs-lookup"><span data-stu-id="05d0b-120">For example, the singular form of Litas is Litas.</span></span>                                                                                                                         |
    | <span data-ttu-id="05d0b-121">**Именительный падеж множественное число (имя группы полей единиц)**</span><span class="sxs-lookup"><span data-stu-id="05d0b-121">**Plural nominative (Name of units field group)**</span></span>         | <span data-ttu-id="05d0b-122">Введите форму множественного числа для валюты.</span><span class="sxs-lookup"><span data-stu-id="05d0b-122">Enter the plural form of the currency.</span></span> <span data-ttu-id="05d0b-123">Например, введите "Литы".</span><span class="sxs-lookup"><span data-stu-id="05d0b-123">For example, enter Litai.</span></span> <span data-ttu-id="05d0b-124">**Примечание**. Поля **Родительный падеж единственное число** и **Родительный падеж множественное число** доступны в зависимости от языка, выбранного в поле **Язык**.</span><span class="sxs-lookup"><span data-stu-id="05d0b-124">**Note**: The **Singular genitive** and **Plural genitive** fields are available based on the language that you select in the **Language** field.</span></span> |
    | <span data-ttu-id="05d0b-125">**Поле именительного падежа единственного числа (имя группы полей частей)**</span><span class="sxs-lookup"><span data-stu-id="05d0b-125">**Singular nominative field (Name of parts field group)**</span></span> | <span data-ttu-id="05d0b-126">Введите форму единственного числа субединицы для валюты.</span><span class="sxs-lookup"><span data-stu-id="05d0b-126">Enter the singular form of the subunit of the currency.</span></span>                                                                                                                                                            |
    | <span data-ttu-id="05d0b-127">**Именительный падеж множественное число (имя группы полей частей)**</span><span class="sxs-lookup"><span data-stu-id="05d0b-127">**Plural nominative (Name of parts field group)**</span></span>         | <span data-ttu-id="05d0b-128">Введите форму множественного числа субединицы для валюты.</span><span class="sxs-lookup"><span data-stu-id="05d0b-128">Enter the plural form of the subunit of the currency.</span></span>                                                                                                                                                              |
    | <span data-ttu-id="05d0b-129">**Сокращенное наименование единиц (группа полей краткого имени)**</span><span class="sxs-lookup"><span data-stu-id="05d0b-129">**Shortcut name of units (Short name field group)**</span></span>       | <span data-ttu-id="05d0b-130">Введите код ISO для идентификации валюты.</span><span class="sxs-lookup"><span data-stu-id="05d0b-130">Enter the ISO code to identify the currency.</span></span> <span data-ttu-id="05d0b-131">Например, введите LTL для определения литовских литов.</span><span class="sxs-lookup"><span data-stu-id="05d0b-131">For example, enter LTL to identify Litas.</span></span>                                                                                                                             |
    | <span data-ttu-id="05d0b-132">**Сокращенное наименование частей (группа полей краткого имени)**</span><span class="sxs-lookup"><span data-stu-id="05d0b-132">**Shortcut name for parts (Short name field group)**</span></span>      | <span data-ttu-id="05d0b-133">Введите обозначение субединицы валюты.</span><span class="sxs-lookup"><span data-stu-id="05d0b-133">Enter the denomination of the currency subunit.</span></span> <span data-ttu-id="05d0b-134">Например, введите "Центы".</span><span class="sxs-lookup"><span data-stu-id="05d0b-134">For example, enter Centas.</span></span>                                                                                                                                         |
    | <span data-ttu-id="05d0b-135">**Соединительный союз "и" между единицами и частями**</span><span class="sxs-lookup"><span data-stu-id="05d0b-135">**Conjunction 'and' between units and parts**</span></span>             | <span data-ttu-id="05d0b-136">Установите этот флажок для печати союза «и» между единицами и частями валюты.</span><span class="sxs-lookup"><span data-stu-id="05d0b-136">Select to print the conjunction “and” between the currency units and unit parts.</span></span> <span data-ttu-id="05d0b-137">Например, в накладных или отчетах сумма 100,20 литов будет отображаться как «100 литов и 20 центов».</span><span class="sxs-lookup"><span data-stu-id="05d0b-137">For example, on invoices or reports, the amount for LTL 100.20 will be displayed as 100 Litas and 20 Centas.</span></span>                      |

5.  <span data-ttu-id="05d0b-138">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="05d0b-138">Click **Save**.</span></span>





