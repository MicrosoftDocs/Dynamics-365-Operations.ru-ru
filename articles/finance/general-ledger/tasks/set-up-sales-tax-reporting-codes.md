---
title: Настройка кодов налоговой отчетности
description: Эти коды налоговой отчетности ссылаются на номер поля в налоговом отчете.
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c18f4fb0db31a959647bb10d2b99d940646676e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976801"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="6c8de-103">Настройка кодов налоговой отчетности</span><span class="sxs-lookup"><span data-stu-id="6c8de-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c8de-104">Эти коды налоговой отчетности ссылаются на номер поля в налоговом отчете.</span><span class="sxs-lookup"><span data-stu-id="6c8de-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="6c8de-105">Они используются в макетах отчетов для определенной страны или региона и в отчете "Налоговые платежи по коду" для печати сумм налогов на период сопоставления, суммированных по коду отчетности.</span><span class="sxs-lookup"><span data-stu-id="6c8de-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="6c8de-106">После создания кодов налоговой отчетности на них можно ссылаться на экспресс-вкладке "Настройка отчетов" на странице "Налоговый код".</span><span class="sxs-lookup"><span data-stu-id="6c8de-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="6c8de-107">В данной записи используется демонстрационная компания DEMF.</span><span class="sxs-lookup"><span data-stu-id="6c8de-107">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="6c8de-108">В области **Область переходов** выберите **Налог > Настройка > Налог > Коды налоговой отчетности**.</span><span class="sxs-lookup"><span data-stu-id="6c8de-108">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="6c8de-109">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="6c8de-109">Click **New**.</span></span>
3. <span data-ttu-id="6c8de-110">Выберите макет отчета, к которому принадлежит код отчетности.</span><span class="sxs-lookup"><span data-stu-id="6c8de-110">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="6c8de-111">Этот макет используется для фильтрации доступных кодов отчетности для налогового кода.</span><span class="sxs-lookup"><span data-stu-id="6c8de-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="6c8de-112">Каждый налоговый код принадлежит к периоду сопоставления, который принадлежит к налоговому органу, использующему макета отчета.</span><span class="sxs-lookup"><span data-stu-id="6c8de-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="6c8de-113">В поле **Код отчетности** введите номер.</span><span class="sxs-lookup"><span data-stu-id="6c8de-113">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="6c8de-114">В поле **Текст отчета** введите описание для отображения в отчетах.</span><span class="sxs-lookup"><span data-stu-id="6c8de-114">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="6c8de-115">В поле **Краткое описание** введите описание для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="6c8de-115">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="6c8de-116">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="6c8de-116">Click **Save**.</span></span>

