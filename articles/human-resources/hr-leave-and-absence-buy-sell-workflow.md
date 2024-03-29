---
title: Создание рабочего процесса запросов покупки и продажи отпуска
description: Создание рабочего процесса запросов покупки и продажи отпуска для постоянного управления запросами покупки и продажи отпуска в Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fabe2333bbf76edf31b77c0d5fce044273333de2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869817"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>Создание рабочего процесса запросов покупки и продажи отпуска


>[!Important]
>Функции, перечисленные в этой статье, в настоящее время доступны для клиентов в отдельной версии Dynamics 365 Human Resources. Некоторые или все функции будут доступны в составе будущего выпуска в инфраструктуре Finance после выпуска Finance 10.0.26.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Рабочий процесс можно создать в Dynamics 365 Human Resources для постоянного управления запросами покупки и продажи отпуска. Рабочий процесс **Покупка и продажа отпуска** позволяет:

- Определение задач
- Определите, кто должен выполнять задачи
- Укажите, кто может утверждать или отклонять запросы

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>Создание рабочего процесса запросов покупки и продажи отпуска

1. На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.

2. В **Настройка** выберите **Workflow-процессы управления персоналом**.

3. Выберите **Создать**, затем выберите **Запрос покупки и продажи отпуска**. 

4. Когда появляется окно сообщения **Открыть этот файл?**, выберите **Открыть** и войдите в систему с учетными данными компании.

5. С помощью редактора workflow-процессов создайте workflow-процесс для своих запросов на отпуск. Дополнительные сведения о работе с workflow-процессами см. в разделе [Обзор создания workflow-процессов](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Элементы данных workflow-процесса запросов отпуска и отсутствия

Следующие элементы данных можно использовать для создания условного или автоматического утверждения в рабочих процессах для запросов покупки и продажи отпусков:

- **Сумма, руб.**
- **Политика покупки и продажи отпусков**
- **Организация**
- **Создан**
- **Дата и время создания**
- **Конечная дата**
- **Тип отпуска**
- **Изменено**
- **Дата и время изменения**
- **Код запроса**
- **Начальная дата**
- **Состояние** 
- **Дата отправки**
- **Кем отправлено:**
- **Отправлено отделом по управлению персоналом**
- **Отправлено менеджером**
- **Отправлено от имени**
- **Рабочий**

## <a name="workflow-examples"></a>Примеры рабочего процесса

В этих примерах показано, как можно создать различные типы условий workflow-процесса, используя эти элементы данных:

- Используйте **Отправлено отделом по управлению персоналом** и **Отправлено менеджером** в автоматическом действии для автоматического утверждения запросов покупки и продажи отпуска, которые эти роли отправляют от имени сотрудников. Дополнительные сведения об автоматических действиях см. в разделе [Настройка процессов утверждения в workflow-процессе](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- **Тип отпуска** используется в условных выражениях или автоматических действиях для управления перенаправление запросов с определенными типами отпусков.

## <a name="see-also"></a>См. также

[Обзор отпусков и отсутствия на работе](hr-leave-and-absence-overview.md)<br>
[Управление политиками покупки и продажи отпусков](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)<br>
[Покупка и продажа отпуска](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
