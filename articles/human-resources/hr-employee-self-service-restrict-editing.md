---
title: Ограничение редактирования личных данных
description: Ограничение сотрудникам изменения сведений о контактах в Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e43b9127b247fa618558b725837d12bf290662f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052033"
---
# <a name="restrict-editing-of-personal-information"></a>Ограничение редактирования личных данных

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

В этом разделе описывается, как запретить сотрудникам изменять сведения о контактах в Dynamics 365 Human Resources. Может возникнуть необходимость запретить внесение сотрудниками каких-либо дополнительных сведений о контакте, таких как местоположение компании или адрес электронной почты.

> [!NOTE]
> Чтобы использовать эту функцию, необходимо сначала включить **(Предварительная версия) Запретить сотрудникам добавлять или редактировать адрес и контактную информацию для целей выбора** в управлении функциями. Дополнительные сведения о включении предварительных версий функций см. в разделе [Управление функциями](hr-admin-manage-features.md).<br><br>![Включить предварительную версию функции](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>Выберите сведения, которые сотрудник может добавить или изменить

1. В модуле Human Resources выберите **Управление персоналом**, выберите **Ссылки**, затем выберите **Параметры Human Resources**.

   ![Перейдите к параметрам управления персоналом](./media/hr-employee-self-service-human-resources-parameters.png)

2. На странице **Параметры управления персоналом** выберите вкладку **Самообслуживание сотрудников**.

   ![Выберите самообслуживание сотрудников](./media/hr-employee-self-service-tab.png)

3. На вкладке **Самообслуживание сотрудников** снимите отметки всех сведения в разделе **Адрес и контактная информация**, которые сотрудники не должны добавлять или изменять. В этом примере сняты отметки для контактных данных **Бизнес**.

   ![Запрет редактирования сведений бизнес-контактов](./media/hr-employee-self-service-restrict-business.png)

4. Нажмите **Сохранить**.

   ![Сохранить изменения](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>Взаимодействие с сотрудниками

После того как сотрудникам запрещено добавление или изменение контактных данных, они могут просматривать сведения, но не могут изменять их.

В этом примере сотрудникам запрещено редактировать сведения о контактах **Бизнес**, они по-прежнему могут просматривать сведения в самообслуживании сотрудников:

![Просмотр сведений о бизнес-контактах](./media/hr-employee-self-service-restrict-view.png)

Однако при выборе сведений о бизнес-контактах область **Изменить адрес** отображается как доступная только для чтения и нельзя изменять никакое поля.

![Сведения бизнес-контакта отображаются только для чтения](./media/hr-employee-self-service-restrict-read-only.png)

Кроме того, если выбрать **Добавить** для добавления нового адреса, они не смогут выбрать **Бизнес** в раскрывающемся списке **Цель**.

![Сотрудник не может добавить бизнес-адрес](./media/hr-employee-self-service-restrict-add.png)

Для сотрудников реализовано одинаковое взаимодействие при выборе **Контактная информация** на странице **Личные данные** и добавлении нового адреса. В раскрывающемся списке **Цель** отображаются только типы сведений, которые они могут добавлять. 

![Сотрудник не может выбрать "Бизнес" в раскрывающемся списке целей](./media/hr-employee-self-service-restrict-purpose.png)

В **Контактная информация** будет показана **Цель** в сетке.

![Цель отображается в сетке сведений о контакте](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>См. также

[Обзор самообслуживания сотрудников и менеджеров](hr-employee-manager-self-service-overview.md)<br>
[Настройка параметров Human Resources](hr-setup-parameters.md)<br>
[Изменить личные сведения](hr-employee-manager-self-service-edit-personal-information.md)