--- 
title: "Импорт конфигурации кредитового перевода ISO20022"
description: "Эта процедура показывает, как импортировать конфигурацию электронной отчетности по платежам поставщикам."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 71c0175178203006e297466c4a37cd3e6319b6ea
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="99c5d-103">Импорт конфигурации кредитового перевода ISO20022</span><span class="sxs-lookup"><span data-stu-id="99c5d-103">Import ISO20022 credit transfer configuration</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="99c5d-104">Эта процедура показывает, как импортировать конфигурацию электронной отчетности по платежам поставщикам.</span><span class="sxs-lookup"><span data-stu-id="99c5d-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="99c5d-105">Немецкий формат кредитного перевода ISO 20022 используется в качестве примера.</span><span class="sxs-lookup"><span data-stu-id="99c5d-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="99c5d-106">Эта процедура может использоваться для других доступных форматов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="99c5d-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="99c5d-107">Эта задача была создана с использованием демонстрационных данных компании DEMF, но можно использовать любую компанию с демонстрационными данными для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="99c5d-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="99c5d-108">Это первая из пяти задач, которые совместно иллюстрируют процесс платежа поставщикам с помощью конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="99c5d-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="99c5d-109">Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="99c5d-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="99c5d-110">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="99c5d-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="99c5d-111">В списке доступных поставщиков конфигурации выберите Microsoft.</span><span class="sxs-lookup"><span data-stu-id="99c5d-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="99c5d-112">Щелкните "Установить как активное".</span><span class="sxs-lookup"><span data-stu-id="99c5d-112">Click Set active.</span></span>
4. <span data-ttu-id="99c5d-113">Щелкните "Репозитории".</span><span class="sxs-lookup"><span data-stu-id="99c5d-113">Click Repositories.</span></span>
5. <span data-ttu-id="99c5d-114">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="99c5d-114">Click Open.</span></span>
6. <span data-ttu-id="99c5d-115">Щелкните "Показать фильтры".</span><span class="sxs-lookup"><span data-stu-id="99c5d-115">Click Show filters.</span></span>
7. <span data-ttu-id="99c5d-116">Примените следующие фильтры: введите значение фильтра "Перенос кредита ISO20022 (DE)" в поле "Имя конфигурации", используя оператор фильтра "начинается с".</span><span class="sxs-lookup"><span data-stu-id="99c5d-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="99c5d-117">Либо найдите конфигурацию в списке, выберите и переместите ее в задачу импорта.</span><span class="sxs-lookup"><span data-stu-id="99c5d-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="99c5d-118">Нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="99c5d-118">Click Import.</span></span>
    * <span data-ttu-id="99c5d-119">Если кнопка "Импорт" недоступна, это означает, что данная конфигурация уже была импортирована.</span><span class="sxs-lookup"><span data-stu-id="99c5d-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="99c5d-120">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="99c5d-120">Click Yes.</span></span>


