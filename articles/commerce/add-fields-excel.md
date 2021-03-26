---
title: Добавление полей в книгу Excel для редактирования проводок розничной торговли
description: В этой теме описывается, как добавить поля в книгу Microsoft Excel, чтобы можно было редактировать проводки розничной торговли в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: fb0435a617585689a87caa76f80e9774182576cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206327"
---
# <a name="add-fields-to-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="e761d-103">Добавление полей в книгу Excel для редактирования проводок розничной торговли</span><span class="sxs-lookup"><span data-stu-id="e761d-103">Add fields to an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e761d-104">В этой теме описывается, как добавить поля в книгу Microsoft Excel, чтобы можно было редактировать проводки розничной торговли в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e761d-104">This topic describes how to add fields to a Microsoft Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e761d-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="e761d-105">Overview</span></span>

<span data-ttu-id="e761d-106">При создании файла Excel для редактирования проводок розничной торговли файл заполняется данными из некоторых полей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e761d-106">When you generate an Excel file so that you can edit retail transactions, the file is filled with some default fields.</span></span> <span data-ttu-id="e761d-107">Если поле, которое должно быть обновлено, не отображается по умолчанию в созданном файле Excel, его можно добавить.</span><span class="sxs-lookup"><span data-stu-id="e761d-107">If a field that must be updated isn't visible by default in the generated Excel file, you can add it.</span></span>

## <a name="add-fields-to-a-worksheet-in-an-excel-workbook"></a><span data-ttu-id="e761d-108">Добавление полей в лист в книге Excel</span><span class="sxs-lookup"><span data-stu-id="e761d-108">Add fields to a worksheet in an Excel workbook</span></span>

<span data-ttu-id="e761d-109">Чтобы добавить поля в книгу Excel для редактирования проводок розничной торговли, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e761d-109">To add fields to an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="e761d-110">Загрузите и откройте файл Excel на странице **Журналы операций**, странице **Проводки розничной торговли** или плитке **Ошибки проверки проводок** в рабочей области **Финансовая информация магазина**.</span><span class="sxs-lookup"><span data-stu-id="e761d-110">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="e761d-111">Выберите **Разработка**.</span><span class="sxs-lookup"><span data-stu-id="e761d-111">Select **Design**.</span></span>
1. <span data-ttu-id="e761d-112">Выберите символ карандаша для нужной таблицы, затем в списке доступных полей найдите и выберите поле, которое требуется добавить.</span><span class="sxs-lookup"><span data-stu-id="e761d-112">Select the pencil symbol for the desired table, and then, in the list of available fields, find and select the field that you want to add.</span></span>
1. <span data-ttu-id="e761d-113">Выберите **Добавить** и нажмите **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="e761d-113">Select **Add**, and then select **Update**.</span></span> <span data-ttu-id="e761d-114">Можно изменить порядок полей.</span><span class="sxs-lookup"><span data-stu-id="e761d-114">You can reorder fields.</span></span>
1. <span data-ttu-id="e761d-115">По завершении обновления выберите **Обновить**, чтобы получить данные для нового столбца.</span><span class="sxs-lookup"><span data-stu-id="e761d-115">After the update is completed, select **Refresh** to fetch the data for the new column.</span></span>

<span data-ttu-id="e761d-116">Теперь новое поле и данные для него должны быть доступны для редактирования в Excel.</span><span class="sxs-lookup"><span data-stu-id="e761d-116">The new field and data for it should now be available for editing in Excel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e761d-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e761d-117">Additional resources</span></span>

[<span data-ttu-id="e761d-118">Редактирование и аудит кассовых проводок и проводок управления кассами</span><span class="sxs-lookup"><span data-stu-id="e761d-118">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="e761d-119">Редактирование и аудит проводок интернет-заказов и асинхронных проводок заказов клиентов</span><span class="sxs-lookup"><span data-stu-id="e761d-119">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="e761d-120">Изменение финансовых аналитик для проводок розничной торговли</span><span class="sxs-lookup"><span data-stu-id="e761d-120">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="e761d-121">Создание книги Excel для редактирования проводок розничной торговли</span><span class="sxs-lookup"><span data-stu-id="e761d-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]