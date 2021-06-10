---
title: Открытие шаблонов финансового журнала в Office
description: В этой теме описываются проблемы, которые могут возникнуть при создании настраиваемых финансовых журналов с помощью шаблона Microsoft Excel.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089465"
---
# <a name="open-financial-journal-templates-in-office"></a><span data-ttu-id="86a85-103">Открытие шаблонов финансового журнала в Office</span><span class="sxs-lookup"><span data-stu-id="86a85-103">Open financial journal templates in Office</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86a85-104">В этой теме описываются проблемы, которые могут возникнуть при создании настраиваемых финансовых журналов с помощью шаблона Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="86a85-104">This topic describes issues that might occur when you create custom financial journals by using a Microsoft Excel template.</span></span>

## <a name="symptom"></a><span data-ttu-id="86a85-105">Симптом</span><span class="sxs-lookup"><span data-stu-id="86a85-105">Symptom</span></span>

<span data-ttu-id="86a85-106">Создан пользовательский шаблон Excel для финансовых журналов, но он не отображается в меню **Открыть строки в Excel**.</span><span class="sxs-lookup"><span data-stu-id="86a85-106">You created a custom Excel template for financial journals, but it doesn't appear on the **Open lines in Excel** menu.</span></span> <span data-ttu-id="86a85-107">Либо он отображается в меню, но при его выборе открывается другой шаблон.</span><span class="sxs-lookup"><span data-stu-id="86a85-107">Alternatively, it does appear on the menu, a different template is opened but when you select it.</span></span>

## <a name="resolution"></a><span data-ttu-id="86a85-108">Решение</span><span class="sxs-lookup"><span data-stu-id="86a85-108">Resolution</span></span>

<span data-ttu-id="86a85-109">Функция "Открыть в Excel" по умолчанию использует корневой источник данных (таблицу) текущей страницы, чтобы определить, какие шаблоны или информационные объекты Office отображаются в виде параметров в меню **Открыть в Excel**.</span><span class="sxs-lookup"><span data-stu-id="86a85-109">The default Open in Excel functionality uses the root data source (table) of the current page to determine which Office templates or data entities appear as options on the **Open in Excel** menu.</span></span> <span data-ttu-id="86a85-110">Это не является идеальным поведением для финансовых журналов, поскольку финансовые журналы используют те же таблицы (LedgerJournalTable и LedgerJournalTrans), что и корневой источник данных многих других типов журналов.</span><span class="sxs-lookup"><span data-stu-id="86a85-110">This behavior isn't an ideal experience for financial journals, because financial journals use the same tables (LedgerJournalTable and LedgerJournalTrans) as the root data source of many other types of journals.</span></span>

<span data-ttu-id="86a85-111">Для финансовых журналов функция "Открыть строки в Excel" предназначена для отображения шаблонов, разработанных для журнала, в контексте которого в данный момент ведется работа, например общего журнала или журнала платежей.</span><span class="sxs-lookup"><span data-stu-id="86a85-111">For financial journals, the Open Lines in Excel functionality is intended to show templates that are designed for the journal that you're currently working in the context of, such as the general journal or a payment journal.</span></span> <span data-ttu-id="86a85-112">Например, шаблон, предназначенный для использования с журналом платежей поставщика, будет разработан таким образом, чтобы обязывать использовать основной счет в качестве счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="86a85-112">For example, a template that is intended to be used with a vendor payment journal will be designed to enforce your primary account as a vendor account.</span></span>

<span data-ttu-id="86a85-113">Если требуется повысить уровень шаблона, чтобы он был доступен в меню **Открыть строки в Excel** и **Открыть в Excel**, простым выходом будет реализовать интерфейс **LedgerIJournalExcelTemplate** и расширить класс **DocuTemplateRegistrationBase**.</span><span class="sxs-lookup"><span data-stu-id="86a85-113">If you want to promote a template so that it's available on the **Open lines in Excel** and **Open in Excel** menus, an easy developer experience is to implement the **LedgerIJournalExcelTemplate** interface and extend the **DocuTemplateRegistrationBase** class.</span></span> <span data-ttu-id="86a85-114">Многие примеры этого подхода реализованы в системе.</span><span class="sxs-lookup"><span data-stu-id="86a85-114">Many examples of this approach are implemented in the system.</span></span> <span data-ttu-id="86a85-115">Одним из примеров, который можно использовать для справки, является интерфейс **LedgerDailyJournalExcelTemplate**, который был создан для общего журнала (или ежедневного журнала).</span><span class="sxs-lookup"><span data-stu-id="86a85-115">One example that can be used for reference is the **LedgerDailyJournalExcelTemplate** interface that was created for the general journal (or daily journal).</span></span>

<span data-ttu-id="86a85-116">Если для шаблона реализован интерфейс **LedgerIJournalExcelTemplate**, в меню **Открыть строки в Excel** будут фильтроваться шаблоны по типу журнала и будут отображаться только шаблоны, доступные для этого журнала.</span><span class="sxs-lookup"><span data-stu-id="86a85-116">When the **LedgerIJournalExcelTemplate** interface is implemented for your template, the **Open Lines in Excel** menu will filter templates by the journal type of your journal and will show only the templates that are available for that journal.</span></span> <span data-ttu-id="86a85-117">Интерфейс также предоставляет метод проверки, гарантирующий, что шаблон невозможно открыть для журнала, если он не соответствует требованиям типа счета.</span><span class="sxs-lookup"><span data-stu-id="86a85-117">The interface also provides a validation method that ensures that a template can't be opened for a journal if it doesn't meet the account type requirements.</span></span> <span data-ttu-id="86a85-118">Например, можно указать, что типом счета должен быть **Поставщик** или **Книга учета**.</span><span class="sxs-lookup"><span data-stu-id="86a85-118">For example, you can specify that the account type must be of the **Vendor** or **Ledger** type.</span></span>

<span data-ttu-id="86a85-119">Дополнительные сведения об этих функциях см. в разделе [Добавление шаблонов в меню открытия строк в Excel](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span><span class="sxs-lookup"><span data-stu-id="86a85-119">For more information about this functionality, see [Add templates to the Open lines in Excel menu](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span></span>
