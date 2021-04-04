---
title: Ограничение редактирования личных данных
description: Ограничение сотрудникам изменения сведений о контактах в Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d4785232dbb21c5f8a800497fb0cfd3c64dea2d8
ms.sourcegitcommit: 45d10d0c25b3ec585323709bb97ba1895b500429
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "5503044"
---
# <a name="restrict-editing-of-personal-information"></a><span data-ttu-id="b7867-103">Ограничение редактирования личных данных</span><span class="sxs-lookup"><span data-stu-id="b7867-103">Restrict editing of personal information</span></span>

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="b7867-104">В этом разделе описывается, как запретить сотрудникам изменять сведения о контактах в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b7867-104">This topic describes how to restrict employees from editing contact details in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b7867-105">Может возникнуть необходимость запретить внесение сотрудниками каких-либо дополнительных сведений о контакте, таких как местоположение компании или адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="b7867-105">You might want to prevent employees from editing certain contact details, such as their business location or email address.</span></span>

> [!NOTE]
> <span data-ttu-id="b7867-106">Чтобы использовать эту функцию, необходимо сначала включить **(Предварительная версия) Запретить сотрудникам добавлять или редактировать адрес и контактную информацию для целей выбора** в управлении функциями.</span><span class="sxs-lookup"><span data-stu-id="b7867-106">To use this feature, you must first enable **(Preview) Restrict employees from adding or editing address and contact information for select purposes** in Feature management.</span></span> <span data-ttu-id="b7867-107">Дополнительные сведения о включении предварительных версий функций см. в разделе [Управление функциями](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="b7867-107">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="b7867-108">![Включить предварительную версию функции](./media/hr-employee-self-service-restrict-enable.png)</span><span class="sxs-lookup"><span data-stu-id="b7867-108">![Enable preview feature](./media/hr-employee-self-service-restrict-enable.png)</span></span>

## <a name="choose-the-information-an-employee-can-add-or-edit"></a><span data-ttu-id="b7867-109">Выберите сведения, которые сотрудник может добавить или изменить</span><span class="sxs-lookup"><span data-stu-id="b7867-109">Choose the information an employee can add or edit</span></span>

1. <span data-ttu-id="b7867-110">В модуле Human Resources выберите **Управление персоналом**, выберите **Ссылки**, затем выберите **Параметры Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="b7867-110">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

   ![Перейдите к параметрам управления персоналом](./media/hr-employee-self-service-human-resources-parameters.png)

2. <span data-ttu-id="b7867-112">На странице **Параметры управления персоналом** выберите вкладку **Самообслуживание сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="b7867-112">On the **Human resources parameters** page, select the **Employee self service** tab.</span></span>

   ![Выберите самообслуживание сотрудников](./media/hr-employee-self-service-tab.png)

3. <span data-ttu-id="b7867-114">На вкладке **Самообслуживание сотрудников** снимите отметки всех сведения в разделе **Адрес и контактная информация**, которые сотрудники не должны добавлять или изменять.</span><span class="sxs-lookup"><span data-stu-id="b7867-114">On the **Employee self service** tab, uncheck all information in the **Address and contact information** section that you don't want employees to add or edit.</span></span> <span data-ttu-id="b7867-115">В этом примере сняты отметки для контактных данных **Бизнес**.</span><span class="sxs-lookup"><span data-stu-id="b7867-115">In this example, we've unchecked **Business** contact information.</span></span>

   ![Запрет редактирования сведений бизнес-контактов](./media/hr-employee-self-service-restrict-business.png)

4. <span data-ttu-id="b7867-117">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b7867-117">Select **Save**.</span></span>

   ![Сохранить изменения](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a><span data-ttu-id="b7867-119">Взаимодействие с сотрудниками</span><span class="sxs-lookup"><span data-stu-id="b7867-119">Employee experience</span></span>

<span data-ttu-id="b7867-120">После того как сотрудникам запрещено добавление или изменение контактных данных, они могут просматривать сведения, но не могут изменять их.</span><span class="sxs-lookup"><span data-stu-id="b7867-120">After you've restricted employees from adding or editing contact details, they can see the information, but can't change it.</span></span>

<span data-ttu-id="b7867-121">В этом примере сотрудникам запрещено редактировать сведения о контактах **Бизнес**, они по-прежнему могут просматривать сведения в самообслуживании сотрудников:</span><span class="sxs-lookup"><span data-stu-id="b7867-121">In this example, where employees are restricted from editing **Business** contact details, they can still see the information in Employee self service:</span></span>

![Просмотр сведений о бизнес-контактах](./media/hr-employee-self-service-restrict-view.png)

<span data-ttu-id="b7867-123">Однако при выборе сведений о бизнес-контактах область **Изменить адрес** отображается как доступная только для чтения и нельзя изменять никакое поля.</span><span class="sxs-lookup"><span data-stu-id="b7867-123">However, when they select the business contact details, the **Edit address** pane appears as read-only, and they can't change any of the fields.</span></span>

![Сведения бизнес-контакта отображаются только для чтения](./media/hr-employee-self-service-restrict-read-only.png)

<span data-ttu-id="b7867-125">Кроме того, если выбрать **Добавить** для добавления нового адреса, они не смогут выбрать **Бизнес** в раскрывающемся списке **Цель**.</span><span class="sxs-lookup"><span data-stu-id="b7867-125">In addition, if they select **Add** to add a new address, they can't select **Business** from the **Purpose** dropdown box.</span></span>

![Сотрудник не может добавить бизнес-адрес](./media/hr-employee-self-service-restrict-add.png)

<span data-ttu-id="b7867-127">Для сотрудников реализовано одинаковое взаимодействие при выборе **Контактная информация** на странице **Личные данные** и добавлении нового адреса.</span><span class="sxs-lookup"><span data-stu-id="b7867-127">Employees get the same experience when they select **Contact details** on the **Personal information** page and add a new address.</span></span> <span data-ttu-id="b7867-128">В раскрывающемся списке **Цель** отображаются только типы сведений, которые они могут добавлять.</span><span class="sxs-lookup"><span data-stu-id="b7867-128">The **Purpose** dropdown box only displays the types of information they can add.</span></span> 

![Сотрудник не может выбрать "Бизнес" в раскрывающемся списке целей](./media/hr-employee-self-service-restrict-purpose.png)

<span data-ttu-id="b7867-130">В **Контактная информация** будет показана **Цель** в сетке.</span><span class="sxs-lookup"><span data-stu-id="b7867-130">**Contact details** now shows **Purpose** in the grid.</span></span>

![Цель отображается в сетке сведений о контакте](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a><span data-ttu-id="b7867-132">См. также</span><span class="sxs-lookup"><span data-stu-id="b7867-132">See also</span></span>

[<span data-ttu-id="b7867-133">Обзор самообслуживания сотрудников и менеджеров</span><span class="sxs-lookup"><span data-stu-id="b7867-133">Employee and Manager self service overview</span></span>](hr-employee-manager-self-service-overview.md)<br>
[<span data-ttu-id="b7867-134">Настройка параметров Human Resources</span><span class="sxs-lookup"><span data-stu-id="b7867-134">Configure Human resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="b7867-135">Изменить личные сведения</span><span class="sxs-lookup"><span data-stu-id="b7867-135">Edit personal information</span></span>](hr-employee-manager-self-service-edit-personal-information.md)