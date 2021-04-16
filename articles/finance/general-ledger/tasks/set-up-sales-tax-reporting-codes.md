---
title: Настройка кодов налоговой отчетности
description: Эти коды налоговой отчетности ссылаются на номер поля, указанный в налоговом отчете.
author: twheeloc
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e040bac6ef9e950e8d7f97e3c136636acf1fe43
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813539"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="466f8-103">Настройка кодов налоговой отчетности</span><span class="sxs-lookup"><span data-stu-id="466f8-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="466f8-104">Эти коды налоговой отчетности ссылаются на номер поля, указанный в налоговом отчете.</span><span class="sxs-lookup"><span data-stu-id="466f8-104">The Sales tax reporting codes refer to a field number that's listed on a sales tax report.</span></span> <span data-ttu-id="466f8-105">Они используются в форматах отчетов для определенной страны или региона.</span><span class="sxs-lookup"><span data-stu-id="466f8-105">They are used on country-specific report layouts.</span></span> <span data-ttu-id="466f8-106">Они также используются в отчете о налоговых платежах по коду.</span><span class="sxs-lookup"><span data-stu-id="466f8-106">They're also used on the Sales tax payment by code report.</span></span> <span data-ttu-id="466f8-107">Этот отчет показывает суммы налогов для периода сопоставления, суммированные по каждому коду отчетности.</span><span class="sxs-lookup"><span data-stu-id="466f8-107">That report shows sales tax amounts for a settlement period summarized for each reporting code.</span></span> <span data-ttu-id="466f8-108">После создания кодов налоговой отчетности на эти коды можно ссылаться на экспресс-вкладке "Настройка отчетов", на которую можно перейти на странице **Налоговый код**.</span><span class="sxs-lookup"><span data-stu-id="466f8-108">After you create Sales tax reporting codes, you can refer to those codes on the Report setup FastTabs, which you can access from the **Sales tax code** page.</span></span> 

<span data-ttu-id="466f8-109">В данной записи используется демонстрационная компания DEMF.</span><span class="sxs-lookup"><span data-stu-id="466f8-109">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="466f8-110">В области **Область переходов** выберите **Налог > Настройка > Налог > Коды налоговой отчетности**.</span><span class="sxs-lookup"><span data-stu-id="466f8-110">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="466f8-111">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="466f8-111">Click **New**.</span></span>
3. <span data-ttu-id="466f8-112">Выберите макет отчета, к которому принадлежит код отчетности.</span><span class="sxs-lookup"><span data-stu-id="466f8-112">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="466f8-113">Этот макет используется для фильтрации доступных кодов отчетности для налогового кода.</span><span class="sxs-lookup"><span data-stu-id="466f8-113">This layout is used to filter the available reporting codes for a sales tax code.</span></span> <span data-ttu-id="466f8-114">Каждый налоговый код принадлежит к периоду сопоставления, который принадлежит к налоговому органу, использующему макета отчета.</span><span class="sxs-lookup"><span data-stu-id="466f8-114">Each sales tax code belongs to a settlement period, which belongs to a Sales tax authority, which uses a report layout.</span></span>  
4. <span data-ttu-id="466f8-115">В поле **Код отчетности** введите номер.</span><span class="sxs-lookup"><span data-stu-id="466f8-115">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="466f8-116">В поле **Текст отчета** введите описание для отображения в отчетах.</span><span class="sxs-lookup"><span data-stu-id="466f8-116">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="466f8-117">В поле **Краткое описание** введите описание для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="466f8-117">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="466f8-118">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="466f8-118">Click **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]