---
title: Импорт конфигурации кредитового перевода ISO20022
description: Эта процедура показывает, как импортировать конфигурацию электронной отчетности по платежам поставщикам.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fbd2e39f488696ebe8db5579ed88595e246ce97
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573125"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="0ff89-103">Импорт конфигурации кредитового перевода ISO20022</span><span class="sxs-lookup"><span data-stu-id="0ff89-103">Import ISO20022 credit transfer configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0ff89-104">Эта процедура показывает, как импортировать конфигурацию электронной отчетности по платежам поставщикам.</span><span class="sxs-lookup"><span data-stu-id="0ff89-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="0ff89-105">Немецкий формат кредитного перевода ISO 20022 используется в качестве примера.</span><span class="sxs-lookup"><span data-stu-id="0ff89-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="0ff89-106">Эта процедура может использоваться для других доступных форматов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="0ff89-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="0ff89-107">Эта задача была создана с использованием демонстрационных данных компании DEMF, но можно использовать любую компанию с демонстрационными данными для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="0ff89-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="0ff89-108">Это первая из пяти задач, которые совместно иллюстрируют процесс платежа поставщикам с помощью конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="0ff89-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="0ff89-109">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="0ff89-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="0ff89-110">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="0ff89-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0ff89-111">В списке доступных поставщиков конфигурации выберите Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0ff89-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="0ff89-112">Щелкните "Установить как активное".</span><span class="sxs-lookup"><span data-stu-id="0ff89-112">Click Set active.</span></span>
4. <span data-ttu-id="0ff89-113">Щелкните "Репозитории".</span><span class="sxs-lookup"><span data-stu-id="0ff89-113">Click Repositories.</span></span>
5. <span data-ttu-id="0ff89-114">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="0ff89-114">Click Open.</span></span>
6. <span data-ttu-id="0ff89-115">Щелкните "Показать фильтры".</span><span class="sxs-lookup"><span data-stu-id="0ff89-115">Click Show filters.</span></span>
7. <span data-ttu-id="0ff89-116">Примените следующие фильтры: введите значение фильтра "Перенос кредита ISO20022 (DE)" в поле "Имя конфигурации", используя оператор фильтра "начинается с".</span><span class="sxs-lookup"><span data-stu-id="0ff89-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="0ff89-117">Либо найдите конфигурацию в списке, выберите и переместите ее в задачу импорта.</span><span class="sxs-lookup"><span data-stu-id="0ff89-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="0ff89-118">Нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="0ff89-118">Click Import.</span></span>
    * <span data-ttu-id="0ff89-119">Если кнопка "Импорт" недоступна, это означает, что данная конфигурация уже была импортирована.</span><span class="sxs-lookup"><span data-stu-id="0ff89-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="0ff89-120">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="0ff89-120">Click Yes.</span></span>

