---
title: Настройка глобальной адресной книги
description: Эта процедура используется для настройки значений по умолчанию и политик безопасности для глобальной адресной книги.
author: msftbrking
manager: AnnBe
ms.date: 07/23/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirParameters
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ebe68f926848c86843be04977f58d89e7a54509b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143897"
---
# <a name="configure-the-global-address-book"></a><span data-ttu-id="1ec4e-103">Настройка глобальной адресной книги</span><span class="sxs-lookup"><span data-stu-id="1ec4e-103">Configure the global address book</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1ec4e-104">Эта процедура используется для настройки значений по умолчанию и политик безопасности для глобальной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-104">Use this procedure to set the default values and security policies for the global address book.</span></span> 

<span data-ttu-id="1ec4e-105">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="1ec4e-106">Эта задача назначена для группы планирования и конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-106">This task is intended for the Planning and configuration team.</span></span>

1. <span data-ttu-id="1ec4e-107">В области переходов перейдите в раздел **Модули > Администрирование организации > Глобальная адресная книга > Параметры глобальной адресной книги**.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-107">In the Navigation pane, go to **Modules > Organization administration > Global address book > Global address book parameters**.</span></span>
2. <span data-ttu-id="1ec4e-108">В поле **Последовательность имя/фамилия** выберите способ отображения имен и фамилий.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-108">In the **Name sequence** field, select how names should be shown.</span></span>
3. <span data-ttu-id="1ec4e-109">В поле **Удалить субъекты без ролей** выберите, требуется ли удалять субъектов, которым не была назначена никакая роль.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-109">In **Delete parties with no roles**, select whether to delete parties with that have not been assigned a role.</span></span>
4. <span data-ttu-id="1ec4e-110">В поле **Использовать проверку на дубликаты** выберите, требуется ли проверять наличие дубликатов записей.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-110">In **Use duplicate check**, select whether to check for duplicate records.</span></span>
5. <span data-ttu-id="1ec4e-111">В поле **Отображать DUNS-номер в адресах** выберите, отображать ли номер DUNS в адресах.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-111">In **Display DUNS number on addresses**, select whether to display the DUNS number on addresses.</span></span>
6. <span data-ttu-id="1ec4e-112">В поле **Проверка уникальности номера DUNS** выберите, требуется ли проверять уникальность номеров DUNS.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-112">In **Check for unique DUNS number**, select whether to check for unique DUNS numbers.</span></span>
7. <span data-ttu-id="1ec4e-113">В поле **Субъект** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-113">In the **Party** field, select an option.</span></span>
8. <span data-ttu-id="1ec4e-114">В поле **Клиент** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-114">In the **Customer** field, select an option.</span></span>
9. <span data-ttu-id="1ec4e-115">В поле **Поставщик** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-115">In the **Vendor** field, select an option.</span></span>
10. <span data-ttu-id="1ec4e-116">В поле **Перспективный клиент** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-116">In the **Prospect** field, select an option.</span></span>
11. <span data-ttu-id="1ec4e-117">В поле **Конкурент** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-117">In the **Competitor** field, select an option.</span></span>
12. <span data-ttu-id="1ec4e-118">Перейдите на вкладку **Безопасность частного местоположения**.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-118">Click the **Private location security** tab.</span></span>
13. <span data-ttu-id="1ec4e-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="1ec4e-120">Нажмите клавишу SHIFT, чтобы выбрать несколько ролей для добавления в область **Выбранные роли**, а затем щелкните стрелку, чтобы добавить из к выбранным ролям.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-120">Press the Shift key to select multiple roles to add to the **Selected roles** pane and then click the arrow to add the selected roles.</span></span>  
14. <span data-ttu-id="1ec4e-121">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1ec4e-121">Click **Save**.</span></span>

