---
title: Изменение финансовых аналитик для проводок розничной торговли
description: В этой теме описывается, как изменить финансовые аналитики для проводок розничной торговли в Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4d4b7e383ca2089ee98e70d23ccd890d0e6a86c5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221806"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="d551b-103">Изменение финансовых аналитик для проводок розничной торговли</span><span class="sxs-lookup"><span data-stu-id="d551b-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d551b-104">В этой теме описывается, как изменить финансовые аналитики для проводок розничной торговли в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d551b-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="d551b-105">Изменение финансовых аналитик</span><span class="sxs-lookup"><span data-stu-id="d551b-105">Edit financial dimensions</span></span>

<span data-ttu-id="d551b-106">Чтобы изменить финансовые аналитики проводок розничной торговли в Commerce Headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d551b-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d551b-107">Откройте страницу **Конфигурация финансовых аналитик для интеграции приложений**.</span><span class="sxs-lookup"><span data-stu-id="d551b-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="d551b-108">Выберите активную запись **Интеграция аналитик по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="d551b-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="d551b-109">На экспресс-вкладке **Финансовые аналитики** проверьте, что все аналитики, которые требуется изменить на листе Excel, присутствуют в списке **Выбрано**.</span><span class="sxs-lookup"><span data-stu-id="d551b-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="d551b-110">Дополнительные сведения см. в разделе [Информационные объекты](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span><span class="sxs-lookup"><span data-stu-id="d551b-110">For more information, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span></span>
1. <span data-ttu-id="d551b-111">Загрузите и откройте файл Excel на странице **Журналы операций**, странице **Проводки розничной торговли** или плитке **Ошибки проверки проводок** в рабочей области **Финансовая информация магазина**.</span><span class="sxs-lookup"><span data-stu-id="d551b-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="d551b-112">Чтобы изменить финансовую аналитику проводки, выберите **Разработка**, а затем выберите символ карандаша рядом со строкой **Проводка (доступно для аудита)**.</span><span class="sxs-lookup"><span data-stu-id="d551b-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="d551b-113">Найдите и выберите поле **FinancialDimensionDisplayValue**, выберите ячейку в заголовке листа Excel и нажмите **Добавить метку**.</span><span class="sxs-lookup"><span data-stu-id="d551b-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="d551b-114">Выберите ячейку под ячейкой, выбранной на предыдущем шаге, нажмите **Добавить значение** и выберите **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="d551b-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="d551b-115">Финансовые аналитики будут добавлены на лист Excel, после чего их можно редактировать и публиковать.</span><span class="sxs-lookup"><span data-stu-id="d551b-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="d551b-116">Чтобы изменить аналитики в строках проводки, выберите строку **Проводки по продаже (доступно для аудита)**, выберите символ карандаша и повторите шаги 6 и 7.</span><span class="sxs-lookup"><span data-stu-id="d551b-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="d551b-117">Чтобы изменить аналитики в строках платежа, выберите строку **Проводки по оплате (доступно для аудита)**, выберите символ карандаша и повторите шаги 6 и 7.</span><span class="sxs-lookup"><span data-stu-id="d551b-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d551b-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d551b-118">Additional resources</span></span>

[<span data-ttu-id="d551b-119">Редактирование и аудит кассовых проводок и проводок управления кассами</span><span class="sxs-lookup"><span data-stu-id="d551b-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="d551b-120">Редактирование и аудит проводок интернет-заказов и асинхронных проводок заказов клиентов</span><span class="sxs-lookup"><span data-stu-id="d551b-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="d551b-121">Создание книги Excel для редактирования проводок розничной торговли</span><span class="sxs-lookup"><span data-stu-id="d551b-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="d551b-122">Добавление полей в книгу Excel для редактирования проводок розничной торговли</span><span class="sxs-lookup"><span data-stu-id="d551b-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]