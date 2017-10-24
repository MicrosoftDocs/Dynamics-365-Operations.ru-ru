--- 
title: "Настройка кодов налоговой отчетности"
description: "Эти коды налоговой отчетности ссылаются на номер поля в налоговом отчете."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fa32a12e49b6578c41ceb8991237a19ae3f77e17
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="66f6f-103">Настройка кодов налоговой отчетности</span><span class="sxs-lookup"><span data-stu-id="66f6f-103">Set up sales tax reporting codes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="66f6f-104">Эти коды налоговой отчетности ссылаются на номер поля в налоговом отчете.</span><span class="sxs-lookup"><span data-stu-id="66f6f-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="66f6f-105">Они используются в макетах отчетов для определенной страны и в отчете "Налоговые платежи по коду" для печати сумм налогов на период сопоставления, суммированных по коду отчетности.</span><span class="sxs-lookup"><span data-stu-id="66f6f-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="66f6f-106">После создания кодов налоговой отчетности на них можно ссылаться на экспресс-вкладке "Настройка отчетов" на странице "Налоговый код".</span><span class="sxs-lookup"><span data-stu-id="66f6f-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="66f6f-107">В данной записи используется демонстрационная компания DEMF.</span><span class="sxs-lookup"><span data-stu-id="66f6f-107">This recording uses the DEMF demo company.</span></span>



1. <span data-ttu-id="66f6f-108">Перейдите в раздел "Налог" > "Настройка" > "Налог" > "Коды налоговой отчетности".</span><span class="sxs-lookup"><span data-stu-id="66f6f-108">Go to Tax > Setup > Sales tax > Sales tax reporting codes.</span></span>
2. <span data-ttu-id="66f6f-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="66f6f-109">Click New.</span></span>
3. <span data-ttu-id="66f6f-110">Выберите макет отчета, к которому принадлежит код отчетности.</span><span class="sxs-lookup"><span data-stu-id="66f6f-110">Select the report layout that the reporting code belongs to.</span></span>
    * <span data-ttu-id="66f6f-111">Этот макет используется для фильтрации доступных кодов отчетности для налогового кода.</span><span class="sxs-lookup"><span data-stu-id="66f6f-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="66f6f-112">Каждый налоговый код принадлежит к периоду сопоставления, который принадлежит к налоговому органу, использующему макета отчета.</span><span class="sxs-lookup"><span data-stu-id="66f6f-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="66f6f-113">Введите номер, который ссылается на поле в налоговом отчете.</span><span class="sxs-lookup"><span data-stu-id="66f6f-113">Enter a number that refers to a field on a sales tax report.</span></span>
5. <span data-ttu-id="66f6f-114">В поле "Текст отчета" введите описание для отображения в отчетах.</span><span class="sxs-lookup"><span data-stu-id="66f6f-114">In the Report text field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="66f6f-115">В поле "Краткое описание" введите описание для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="66f6f-115">In the Brief description field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="66f6f-116">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="66f6f-116">Click Save.</span></span>


