---
title: Финансовые аналитики и счета ГК в языках с направлением письма справа налево
description: В этой теме описаны решения, которые требуется принимать при использовании языка с направлением письма справа налево и которые необходимо настроить в финансовых аналитиках и счетах ГК.
author: aprilolson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 508f4ed4de367770acddc77a6ff5e7e36fd20729
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748145"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a><span data-ttu-id="d164e-103">Финансовые аналитики и счета ГК в языках с направлением письма справа налево</span><span class="sxs-lookup"><span data-stu-id="d164e-103">Financial dimensions and main accounts in right-to-left languages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d164e-104">В этом разделе описаны некоторые решений реализации, которые следует учитывать при использовании языка с направлением письма справа налево и которые необходимо настроить в финансовых аналитик и счетах ГК.</span><span class="sxs-lookup"><span data-stu-id="d164e-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="d164e-105">Финансовые аналитики и счета ГК являются ключевыми компонентами этапа планирования для реализации.</span><span class="sxs-lookup"><span data-stu-id="d164e-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="d164e-106">После создания финансовых аналитик и счетов ГК в системе они используются на страницах **Настройка структур счета**, **Структуры дополнительных правил** и **Конфигурация финансовой аналитики для при интеграции приложений**.</span><span class="sxs-lookup"><span data-stu-id="d164e-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="d164e-107">Порядок, определенный на этих страницах, используется в системе для ввода данных и потребления.</span><span class="sxs-lookup"><span data-stu-id="d164e-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="d164e-108">В некоторых местах системы финансовые аналитики и счета ГК отображаются в отдельных полях.</span><span class="sxs-lookup"><span data-stu-id="d164e-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="d164e-109">В других местах, таких как журналы, финансовые аналитики и счета ГК отображаются как одна строка.</span><span class="sxs-lookup"><span data-stu-id="d164e-109">In other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="d164e-110">Рекомендации по настройке финансовых аналитик и счетов ГК в системе с направлением письма справа налево</span><span class="sxs-lookup"><span data-stu-id="d164e-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

- <span data-ttu-id="d164e-111">При выборе разделителя для планов счетов выберите один из вариантов двойных разделителей: два дефиса (`--`), две вертикальные черты (`||`), две точки (`..`) или два символа подчеркивания (`\\`).</span><span class="sxs-lookup"><span data-stu-id="d164e-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (`--`), double bar (`||`), double period (`..`), or double underscore (`\\`).</span></span>
- <span data-ttu-id="d164e-112">При создании значений финансовой аналитики и счета ГК используйте только цифры и символы языка с направлением письма справа налево.</span><span class="sxs-lookup"><span data-stu-id="d164e-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
- <span data-ttu-id="d164e-113">Не используйте выбранный разделить плана счетов в значениях финансовой аналитики и счета ГК.</span><span class="sxs-lookup"><span data-stu-id="d164e-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="d164e-114">Следуя этим рекомендациям, вы помогаете обеспечить согласованное представление определяемого пользователем порядка во всей системе.</span><span class="sxs-lookup"><span data-stu-id="d164e-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]