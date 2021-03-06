---
title: Настройка параметров Human Resources
description: В этой теме описывается, как настроить параметры модуля, относящиеся к конкретной компании, в Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c4c93e3d2644a380e3d5d2247961a8b6fb34568
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052417"
---
# <a name="configure-human-resources-parameters"></a>Настройка параметров Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Настройки некоторых параметров управления персоналом используются совместно несколькими компаниями, в то время как настройки других параметров относятся только к конкретной компании. В этой теме описывается, как настроить параметры управления персоналом, относящиеся к конкретной компании.

Для задания параметров управления персоналом используются две страницы. Для параметров, которые являются общими для различных компаний, используется страница **Совместно используемые параметры управления персоналом**. Для параметров конкретной компании (иными словами, параметров, относящихся к одной компании) используется страница **Параметры Управления персоналом**.

![Перейдите к параметрам управления персоналом](./media/hr-employee-self-service-human-resources-parameters.png)

На странице **Параметры Управления персоналом** страницы разделены на шесть вкладок:

- **Общие сведения**
- **Набор сотрудников** (эта вкладка не входит в Dynamics 365 Human Resources)
- **Компенсация**
- **Номерные серии**
- **FMLA**
- **Портал самообслуживания сотрудников**
- **Портал самообслуживания менеджеров**
- **Управление льготами**
- **Отпуск и отсутствие**
- **Способы оплаты**

Каждая вкладка содержит информацию, относящуюся к одной компании.

## <a name="general"></a>Общие сведения

Настройки на вкладке **Общее** определяют внешний вид информации об отсутствия, травмах и заболеваниях, а также новых работниках. Настройки на этой вкладке также определяют некоторые значения по умолчанию, предлагаемые вам в ходе работы. В частности, эта вкладка позволяет:

- Выбрать цвет, который будет применяться к открытым проводкам отсутствия
- Задать таблицу стилей для использования в отчетах
- Включить интеграцию между курсами обучения и регистрацией отсутствия
- Выбрать код отсутствия, который используется для управления этой интеграцией.
- Указать длительность хранения случаев травм и заболеваний.
- Задавать идентификационный номер по умолчанию, отображаемый при найме нового работника.

![Вкладка "Общие"](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a>Набор сотрудников

Настройки на вкладке **Набор сотрудников** определяют типы документов, используемые для корреспонденции, автоматически отправляемой кандидатам. Можно также указать проект по набору сотрудников, используемый для незапрошенных заявлений.

Период, заданный для распределения по срокам проектов по набору сотрудников, определяет, какие проекты по набору сотрудников включаются на плитку **Распределение по срокам проектов** в рабочей области **Управление набором сотрудников**. Период, заданный для предупреждения о крайнем сроке подачи заявлений, используется для отображения проектов по набору сотрудников, которые приближаются к крайнему сроку, на плитке **Приближается крайний срок подачи заявления** в рабочей области **Набор сотрудников**.

Дополнительные сведения о наборе сотрудников см. в разделе [Наем кандидатов на должность](hr-personnel-recruit.md).

## <a name="compensation"></a>Компенсация

В Dynamics 365 Finance настройки на вкладке **Компенсация** определяют, должны ли пользователи подтверждать, что они хотят сохранить информацию для плана фиксированной или переменной компенсации. Если выбрать **Включить сохранение подтверждения**, когда пользователь закрывает связанную с компенсациями страницу, он будет получать сообщение с вопросом о том, хочет ли он сохранить запись. Некоторые страницы управления компенсациями не позволяют пользователям удалять информацию. Предлагая пользователям подтвердить, что они хотят сохранить информацию, вы сможете ограничить объем информации, которая сохраняется, но впоследствии не может быть удалена. Если удалить **Включить сохранение подтверждения**, записи сохраняются сразу же, возможно, когда пользователь к этому еще не готов. Если вы используете управление производительностью, вкладка **Компенсация** также позволяет выбрать модель рейтинга для использования вместо модели, назначаемой планам компенсационных выплат при оценке производительности.

В управлении персоналом можно использовать вкладку **Компенсация**, чтобы ограничить доступ к планам компенсаций и задать валюту по умолчанию.

Дополнительные сведения о планах компенсации см. в разделе [Обзор планов компенсационных выплат](hr-compensation-overview.md).

![Вкладка "Компенсация"](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a>Номерные серии

Настройки на вкладке **Номерные серии** определяют последовательности, используемые для автоматического присвоения кодов номенклатурам в управлении персоналом, например:

- Приложения
- Регистрация отсутствия
- Результаты процесса компенсации
- Номера вариантов
- Курсы
- Планы курса

Для ведения ссылок и кодов номерных серий используется страница списка **Номерные серии** (выберите **Управление организацией > Номерные серии > Номерные серии**).

Дополнительные сведения см. в разделе [Обзор номерных серий](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

> [!NOTE]
> Количество отработанных часов не может превышать 1250, а длительность трудоустройства не может превышать 12 месяцев. Эти максимальные значения соответствуют федеральному законодательству США.

![Вкладка "Номерные серии"](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a>FMLA

На вкладке FMLA настройте требования к доступности FMLA и трудозатраты FMLA. Дополнительные сведения см. в разделе [Настройка параметров отпусков и отгулов](hr-leave-and-absence-parameters.md).

![Вкладка FMLA](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a>Самообслуживание сотрудника

Настройки на вкладке **Самообслуживание сотрудника** влияют на то, как cамообслуживание сотрудника отображается для сотрудников. На этой вкладке можно выполнить следующие действия:

- Введите имя рабочей области самообслуживания сотрудников
- Выбор сведений, которые руководитель может ввести для сотрудников
- Добавление полезных ссылок для сотрудников
- Ограничение сотрудникам добавления или изменения сведений о бизнес-контактах. Дополнительные сведения см. в разделе [Ограничение редактирования личных данных](hr-employee-self-service-restrict-editing.md).

Дополнительные сведения о настройке самообслуживания сотрудников см. в разделе [Обзор самообслуживания сотрудников и менеджеров](hr-employee-manager-self-service-overview.md).

![Вкладка самообслуживания сотрудников](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a>Портал самообслуживания менеджеров

Настройки на вкладке **Самообслуживание менеджеров** влияют на то, что видят менеджеры в самообслуживании менеджеров. На этой вкладке можно настроить следующие параметры:

- Диапазон записей с истекающим сроком действия
- Менеджеры по информационным данным могут просматривать записи с истекающим сроком действия
- Могут ли менеджеры просматривать открытые должности для расширенных отчетов
- Представления существующих работников
- Полезные ссылки для менеджеров

Дополнительные сведения о настройке самообслуживания менеджеров см. в разделе [Обзор самообслуживания сотрудников и менеджеров](hr-employee-manager-self-service-overview.md).

![Вкладка самообслуживания менеджеров](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a>Управление льготами

На вкладке управления льготами можно настроить параметры электронной почты для управления льготами. Дополнительные сведения о настройке и использовании управления льготами см. в разделе [Обзор управления льготами](hr-benefits-management-overview.md).

![Вкладка управления льготами](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a>Отпуск и отсутствие

Дополнительные сведения о настройке и использовании отпусков и отгулов см. в разделе [Обзор отпусков и отгулов](hr-leave-and-absence-overview.md).

## <a name="payment-methods"></a>Способы оплаты

На вкладке **Методы оплаты** можно выбрать методы оплаты, поддерживаемые вашей организацией. Дополнительные сведения о настройке компенсации см. в разделе [Обзор планов компенсационных выплат](hr-compensation-overview.md).

![Вкладка методов оплаты](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]