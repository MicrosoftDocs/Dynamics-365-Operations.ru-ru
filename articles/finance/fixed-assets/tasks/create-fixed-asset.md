---
title: Создание основного средства
description: В этой теме объясняется, как создать новую запись основного средства на странице списка основных средств.
author: moaamer
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 770390092342e2db496dde850a75b2f7736bd4c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817109"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="fb083-103">Создание основного средства</span><span class="sxs-lookup"><span data-stu-id="fb083-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fb083-104">В этой теме объясняется, как создать новую запись основного средства на странице списка **Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="fb083-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="fb083-105">Номер актива назначается системой на основе номерной серии, назначенной группе основных средств.</span><span class="sxs-lookup"><span data-stu-id="fb083-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="fb083-106">При использовании шаблона основных средств для импорта активов через надстройку Microsoft Excel или при использовании другого задания импорта система автоматически создает записи основных средств и увеличивает номер актива.</span><span class="sxs-lookup"><span data-stu-id="fb083-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="fb083-107">Чтобы вручную создать запись актива, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fb083-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="fb083-108">Выберите **Область перехода \> Модули \> Основные средства \> Основные средства \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="fb083-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="fb083-109">В области **Панель операций** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="fb083-109">On the **Action pane**, select **New**.</span></span>
3. <span data-ttu-id="fb083-110">В поле **Группа ОС** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="fb083-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="fb083-111">Для поля **Номер** будет использоваться значение по умолчанию, если активирована функция **Автонумерация ОС** в разделах **Параметры основных средств** и **Группа ОС**.</span><span class="sxs-lookup"><span data-stu-id="fb083-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="fb083-112">В противном случае необходимо ввести уникальный номер для определения основного средства.</span><span class="sxs-lookup"><span data-stu-id="fb083-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="fb083-113">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="fb083-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="fb083-114">Введите дополнительные сведения, необходимые вашему предприятию для данного основного средства.</span><span class="sxs-lookup"><span data-stu-id="fb083-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="fb083-115">На **панели операций** выберите **Книги**.</span><span class="sxs-lookup"><span data-stu-id="fb083-115">On the **Action pane**, select **Books**.</span></span>
6. <span data-ttu-id="fb083-116">В поле **Дата приобретения** введите дату.</span><span class="sxs-lookup"><span data-stu-id="fb083-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="fb083-117">В поле **Цена приобретения** введите число.</span><span class="sxs-lookup"><span data-stu-id="fb083-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="fb083-118">Введите дополнительные сведения, необходимые вашему предприятию для данной книги.</span><span class="sxs-lookup"><span data-stu-id="fb083-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="fb083-119">Введите дополнительные сведения, необходимые вашему предприятию для оставшихся книг.</span><span class="sxs-lookup"><span data-stu-id="fb083-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="fb083-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="fb083-120">Close the page.</span></span>

<span data-ttu-id="fb083-121">Основные средства также можно импортировать с помощью надстройки Excel или путем запуска задания импорта из рабочей области **Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="fb083-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="fb083-122">Перед выполнением импорта введите значения для обязательных полей в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="fb083-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="fb083-123">Если номер основного средства не определен в шаблоне надстройки Excel или в модуле управления данными, система создает номер основного средства для каждого импортируемого актива и автоматически увеличивает номерную серию для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="fb083-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="fb083-124">Однако, если импортировать активы и определить номера основных средств в шаблоне, система **не** будет автоматически увеличивать номерную серию.</span><span class="sxs-lookup"><span data-stu-id="fb083-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="fb083-125">В этом случае администратору может потребоваться вручную обновить номерную серию.</span><span class="sxs-lookup"><span data-stu-id="fb083-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="fb083-126">Если вы определили номер основного средства в шаблоне надстройки Excel, система использует определенный номер основного средства и увеличивает номерную серию.</span><span class="sxs-lookup"><span data-stu-id="fb083-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="fb083-127">После разноски амортизации поля **Помещенный на обслуживание** и **Дата выполнения амортизации** будут заблокированы на странице **Книга**.</span><span class="sxs-lookup"><span data-stu-id="fb083-127">After posting the depreciation, the **Placed in service** and **Depreciation run date** fields will be locked on the **Book** page.</span></span> <span data-ttu-id="fb083-128">Кроме того, из объекта данных не будет обновлено ни одно поле.</span><span class="sxs-lookup"><span data-stu-id="fb083-128">Also, both neither field will be updated from the data entity.</span></span>

> [!WARNING]
> <span data-ttu-id="fb083-129">Запись основного средства не будет удалена, если проводки были разнесены в соответствующий журнал, или если только что созданное основное средство введено в строку журнала, но не разнесено.</span><span class="sxs-lookup"><span data-stu-id="fb083-129">The fixed asset record won't be deleted if transactions were posted to the associated book, or if the newly created fixed asset is entered on a journal line but not posted.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]