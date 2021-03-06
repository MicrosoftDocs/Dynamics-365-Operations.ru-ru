---
title: Создание workflow-процесса запросов на отпуск
description: Создание workflow-процесса запросов отпуска и отсутствия для постоянного управления запросами отпуска в Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5580b4b07b2d335ad9444a064c726bc4aca1db6a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056548"
---
# <a name="create-a-leave-request-workflow"></a>Создание workflow-процесса запросов на отпуск

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Workflow-процесс можно создать в Dynamics 365 Human Resources для постоянного управления запросами отпуска и отсутствия. Workflow-процесс **Отпуск и отсутствие** позволяет:

- Определение задач
- Определите, кто должен выполнять задачи
- Укажите, кто может утверждать или отклонять запросы

## <a name="create-a-leave-and-absence-request-workflow"></a>Создание workflow-процесса запросов отпуска и отсутствия

1. На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.

2. В **Настройка** выберите **Workflow-процессы управления персоналом**.

3. Выберите **Создать**, а затем выберите **Запрос отпуска и отсутствия**. 

4. Когда появляется окно сообщения **Открыть этот файл?**, выберите **Открыть** и войдите в систему с учетными данными компании.

5. С помощью редактора workflow-процессов создайте workflow-процесс для своих запросов на отпуск. Дополнительные сведения о работе с workflow-процессами см. в разделе [Обзор создания workflow-процессов](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Элементы данных workflow-процесса запросов отпуска и отсутствия

Следующие элементы данных можно использовать для создания условного или автоматического утверждения в workflow-процессах для запросов отпусков и отсутствия:

- **Сумма, руб.**
- **Комментарий**
- **Организация**
- **Создан**
- **Дата и время создания**
- **Конечная дата**
- **Тип отпуска**
- **Кто изменил**
- **Дата и время изменения**
- **Код основания**
- **Код запроса**
- **Начальная дата**
- **Состояние** 
- **Дата отправки**
- **Кем отправлено:**
- **Отправлено отделом по управлению персоналом**
- **Отправлено менеджером**
- **Отправлено от имени**
- **Рабочий**
- **Тип работника**

В этих примерах показано, как можно создать различные типы условий workflow-процесса, используя эти элементы данных:

- **Код основания** используется в условном выражении для направления запросов на отпуск по болезни с кодом основания **Хирургическая операций** для утверждения отделом управления персоналом, в то время как все остальные коды основания перенаправляются менеджеру. Дополнительные сведения об условных выражениях см в разделе [Настройка условных решений в workflow-процессе](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md). 

- Используйте **Отправлено отделом по управлению персоналом** и **Отправлено менеджером** в автоматическом действии для автоматического утверждения запросов на отпуск, которые эти роли отправляют от имени сотрудников. Дополнительные сведения об автоматических действиях см. в разделе [Настройка процессов утверждения в workflow-процессе](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- **Тип отпуска** используется в условных выражениях или автоматических действиях для управления перенаправление запросов с определенными типами отпусков.

## <a name="see-also"></a>См. также

- [Обзор отпусков и отсутствия на работе](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]