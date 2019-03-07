---
title: Импорт и ведение проводок по кредитным картам
description: В этой теме поясняется, как импортировать и вести связанные с расходами проводки по кредитным картам. Эти проводки можно настроить так, чтобы они автоматически импортировались по графику, или импортировать их вручную, когда они необходимы.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 9674cf495b7fdd40d8672580b9d10e9ebe626bb0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "322659"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="ac285-104">Импорт и ведение проводок по кредитным картам</span><span class="sxs-lookup"><span data-stu-id="ac285-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac285-105">Связанные с расходами проводки по кредитным картам можно настроить так, чтобы они автоматически импортировались по графику.</span><span class="sxs-lookup"><span data-stu-id="ac285-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="ac285-106">Кроме того, проводки можно импортировать вручную по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="ac285-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="ac285-107">Проводки по кредитным картам импортируются посредством информационного объекта "Проводки кредитной карты".</span><span class="sxs-lookup"><span data-stu-id="ac285-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="ac285-108">Более подробную информацию об информационных объектах см. в теме [Информационные объекты](../../dev-itpro/data-entities/data-entities.md).</span><span class="sxs-lookup"><span data-stu-id="ac285-108">For more information about data entities, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="ac285-109">Импорт проводок по кредитной карте</span><span class="sxs-lookup"><span data-stu-id="ac285-109">Import credit card transactions</span></span>

1. <span data-ttu-id="ac285-110">На странице **Проводки кредитной карты** выберите **Импорт транзакций**.</span><span class="sxs-lookup"><span data-stu-id="ac285-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="ac285-111">Если вы впервые открываете управление данными, система должна будет обновить список информационных объектов, прежде чем вы сможете продолжить.</span><span class="sxs-lookup"><span data-stu-id="ac285-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="ac285-112">В поле **Имя** введите уникальное описание задания импорта.</span><span class="sxs-lookup"><span data-stu-id="ac285-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="ac285-113">В поле **Формат исходных данных** выберите формат файла, который содержит проводки по кредитным картам для импорта.</span><span class="sxs-lookup"><span data-stu-id="ac285-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="ac285-114">Выберите **Отправить**, а затем найдите и выберите файл для импорта.</span><span class="sxs-lookup"><span data-stu-id="ac285-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="ac285-115">После отправки файла проверьте сопоставление файла проводок по кредитным картам и столбцов информационного объекта "Проводки кредитной карты", выбрав ссылку **Просмотр карты** на плитке.</span><span class="sxs-lookup"><span data-stu-id="ac285-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="ac285-116">При наличии ошибок сопоставления или если сопоставление необходимо изменить, внесите изменения в сопоставление на вкладке **Визуализация сопоставления** или **Сведения о сопоставлении**.</span><span class="sxs-lookup"><span data-stu-id="ac285-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="ac285-117">Чтобы автоматизировать проводки по кредитным картам, выберите **Создать повторяющееся задание данных**.</span><span class="sxs-lookup"><span data-stu-id="ac285-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="ac285-118">После этого вы можете настроить повторение, которое определяет, как часто должны импортироваться проводки по кредитным картам.</span><span class="sxs-lookup"><span data-stu-id="ac285-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="ac285-119">Закончив, выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac285-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="ac285-120">Чтобы импортировать выбранный файл прямо сейчас, выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="ac285-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="ac285-121">При возникновении ошибок во время импорта можно просмотреть журнал выполнения или промежуточные данные, чтобы увидеть ошибки, которые необходимо исправить для того, чтобы импорт прошел успешно.</span><span class="sxs-lookup"><span data-stu-id="ac285-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="ac285-122">Если необходимо импортировать файлы нескольких форматов, необходимо создать отдельные задания импорта для каждого формата.</span><span class="sxs-lookup"><span data-stu-id="ac285-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="ac285-123">Переназначение проводок по кредитным картам для уволенных сотрудников</span><span class="sxs-lookup"><span data-stu-id="ac285-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="ac285-124">После прекращения действия записи сотрудника учетная запись сотрудника в доменных службах Active Directory (AD DS) отключается.</span><span class="sxs-lookup"><span data-stu-id="ac285-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="ac285-125">Однако при этом могут быть активные проводки по кредитной карте, которые все равно нужно учесть как расходы и возместить.</span><span class="sxs-lookup"><span data-stu-id="ac285-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="ac285-126">На странице **Проводки кредитной карты** можно переназначить сотрудника для любой проводки по кредитной карте, когда связанный сотрудник был уволен.</span><span class="sxs-lookup"><span data-stu-id="ac285-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="ac285-127">Выберите одну или несколько проводок по кредитной карте, а затем выберите **Переназначить проводки**.</span><span class="sxs-lookup"><span data-stu-id="ac285-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="ac285-128">После этого можно выбрать другого сотрудника для назначения ему проводок по кредитной карте.</span><span class="sxs-lookup"><span data-stu-id="ac285-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="ac285-129">После переназначения проводок по кредитной карте эти проводки можно выбрать для отчета о расходах и оплатить посредством обычного процесса возмещения отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="ac285-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
