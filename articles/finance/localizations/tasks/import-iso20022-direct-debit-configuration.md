---
title: Импорт конфигурации безакцептного списания ISO20022
description: Эта процедура показывает, как импортировать конфигурацию электронной отчетности по платежам клиентов.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5d4256b155d3e06d63e425fab63b4025ef2577f
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140026"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="f5b65-103">Импорт конфигурации безакцептного списания ISO20022</span><span class="sxs-lookup"><span data-stu-id="f5b65-103">Import ISO20022 direct debit configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f5b65-104">Эта процедура показывает, как импортировать конфигурацию электронной отчетности по платежам клиентов.</span><span class="sxs-lookup"><span data-stu-id="f5b65-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="f5b65-105">Эта процедура использует формат прямого дебетования ISO 20022 в качестве примера.</span><span class="sxs-lookup"><span data-stu-id="f5b65-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="f5b65-106">Эта процедура была создана с использованием демонстрационных данных компании DEMF, но можно использовать любую компанию с демонстрационными данными для этих целей.</span><span class="sxs-lookup"><span data-stu-id="f5b65-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="f5b65-107">Это первая процедура из пяти, которые демонстрируют процесс платежа клиентов с помощью конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="f5b65-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="f5b65-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="f5b65-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f5b65-109">В списке доступных поставщиков конфигурации выберите Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f5b65-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="f5b65-110">Щелкните "Установить как активное".</span><span class="sxs-lookup"><span data-stu-id="f5b65-110">Click Set active.</span></span>
4. <span data-ttu-id="f5b65-111">Щелкните "Репозитории".</span><span class="sxs-lookup"><span data-stu-id="f5b65-111">Click Repositories.</span></span>
5. <span data-ttu-id="f5b65-112">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="f5b65-112">Click Open.</span></span>
6. <span data-ttu-id="f5b65-113">Щелкните "Показать фильтры".</span><span class="sxs-lookup"><span data-stu-id="f5b65-113">Click Show filters.</span></span>
7. <span data-ttu-id="f5b65-114">Примените следующие фильтры: введите значение фильтра "Прямое дебетование ISO20022 (DE)" в поле "Имя конфигурации", используя оператор фильтра "начинается с".</span><span class="sxs-lookup"><span data-stu-id="f5b65-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="f5b65-115">Если требуется, можно найти конфигурацию в списке, выбрать ее и пропустить этот шаг.</span><span class="sxs-lookup"><span data-stu-id="f5b65-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="f5b65-116">Нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="f5b65-116">Click Import.</span></span>
    * <span data-ttu-id="f5b65-117">Если кнопка "Импорт" недоступна, это означает, что данная конфигурация уже была импортирована.</span><span class="sxs-lookup"><span data-stu-id="f5b65-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="f5b65-118">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="f5b65-118">Click Yes.</span></span>

