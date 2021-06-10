---
title: Работники без трудоустройства
description: Работники, не имеющие будущего, активного или исторического трудоустройства в вашей организацией, будут отображаться в форме сотрудники без занятости.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6fbada6feb55b8627b1aa1ddfe367177edb7a0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051721"
---
# <a name="workers-without-employment"></a><span data-ttu-id="7343f-103">Работники без трудоустройства</span><span class="sxs-lookup"><span data-stu-id="7343f-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7343f-104">Работники, не имеющие будущего, активного или исторического трудоустройства в вашей организацией, будут отображаться в форме **Сотрудники без занятости**.</span><span class="sxs-lookup"><span data-stu-id="7343f-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="7343f-105">Работники с этим статусом могут отображаться при импорте работников, не имеющих записи о приеме на работу, или при удалении занятости сотрудника через **Работники > История занятости**.</span><span class="sxs-lookup"><span data-stu-id="7343f-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="7343f-106">По умолчанию форма **Сотрудники без занятости** доступна для следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="7343f-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="7343f-107">Помощник Human Resources</span><span class="sxs-lookup"><span data-stu-id="7343f-107">Human Resources Assistant</span></span>
- <span data-ttu-id="7343f-108">Менеджер Human Resources</span><span class="sxs-lookup"><span data-stu-id="7343f-108">Human Resources Manager</span></span>
- <span data-ttu-id="7343f-109">Агентство по найму</span><span class="sxs-lookup"><span data-stu-id="7343f-109">Recruiter</span></span>
- <span data-ttu-id="7343f-110">Менеджер компенсаций и льгот</span><span class="sxs-lookup"><span data-stu-id="7343f-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="7343f-111">Администратор зарплаты</span><span class="sxs-lookup"><span data-stu-id="7343f-111">Payroll Administrator</span></span>
- <span data-ttu-id="7343f-112">Менеджер зарплаты</span><span class="sxs-lookup"><span data-stu-id="7343f-112">Payroll Manager</span></span>
- <span data-ttu-id="7343f-113">Менеджер по обучению</span><span class="sxs-lookup"><span data-stu-id="7343f-113">Training Manager</span></span>

<span data-ttu-id="7343f-114">В списке **Сотрудники без занятости** можно удалить перечисленные лица.</span><span class="sxs-lookup"><span data-stu-id="7343f-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="7343f-115">По умолчанию эта привилегия предоставляется роли помощника Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7343f-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="7343f-116">Вы можете предоставить эту привилегию другим ролям, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7343f-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="7343f-117">Выберите **Администрирование системы**, затем перейдите на вкладку **Конфигурация безопасности**.</span><span class="sxs-lookup"><span data-stu-id="7343f-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="7343f-118">На вкладке **Привилегии** отфильтруйте список **Привилегии** до **Ведение работников**.</span><span class="sxs-lookup"><span data-stu-id="7343f-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="7343f-119">[![Отфильтруйте список привилегий](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="7343f-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="7343f-120">В столбце **Ссылки** выберите **Пункты меню отображения**.</span><span class="sxs-lookup"><span data-stu-id="7343f-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="7343f-121">В **Пункты меню отображения** выберите **HcmWorkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="7343f-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="7343f-122">[![Выбрать форму](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="7343f-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="7343f-123">Установите разрешение **Удалить** как **Разрешить**.</span><span class="sxs-lookup"><span data-stu-id="7343f-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="7343f-124">Перейдите на вкладку **Неопубликованные объекты**.</span><span class="sxs-lookup"><span data-stu-id="7343f-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="7343f-125">Выберите **Опубликовать все**.</span><span class="sxs-lookup"><span data-stu-id="7343f-125">Select **Publish all**.</span></span>

   <span data-ttu-id="7343f-126">[![Публикация изменений](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="7343f-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]