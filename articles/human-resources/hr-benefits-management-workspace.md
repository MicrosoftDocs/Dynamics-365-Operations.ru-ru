---
title: Рабочая область управления льготами
description: В этой теме описывается рабочее пространство "Управление льготами" в Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9b8dcad04e85a4beb2fe68e9d6fad4ec794e3ade
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805834"
---
# <a name="benefits-management-workspace"></a>Рабочая область управления льготами

[!include [applies to](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

В этой теме описывается рабочее пространство **Управление льготами** в Dynamics 365 Human Resources.

> [!NOTE]
> Для просмотра рабочей области **Управление льготами** необходимо сначала включить **(Предварительная версия) Рабочая область управления льготами** в управлении функциями. Дополнительные сведения о включении предварительных версий функций см. в разделе [Управление функциями](../hr-admin-manage-features.md).<br><br>![Включение рабочей области управления льготами](./media/hr-benefits-management-workspace-enable.png)

Рабочая область **Управление льготами** позволяет быстро просматривать льготы, требующие вашего внимания. На этой странице показано:

- Итоги для номенклатур, ожидающих действия
- Работники с неподтвержденным выбором
- Работники, недавно зарегистрированные в льготах
- Работники с будущими жизненными событиями
- Новые сотрудники, которые не были зарегистрированы
- Работники с активными жизненными событиями
- Работники с открытыми регистрациями, которые не выбрали планы

![Рабочая область управления льготами](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a>Просмотр элементов действия

Можно просмотреть элементы действий, выбирая плитку или вкладку. При выборе вкладки можно просматривать и выбирать сотрудников прямо на странице рабочей области.

![Элементы действия](./media/hr-benefits-management-workspace-action-items.png)

Если выбрать плитку, вы перейдете на страницу этой области. Например, при выборе любой из этих плиток отображается страница **Планы льгот работника**, отфильтрованная для сотрудников, по которым необходимо предпринять действие:

- **Неподтвержденные выбранные параметры**
- **Открытые регистрации без извлеченных планов**
- **Зарегистрированные для льгот**
- **Новый сотрудник не зарегистрирован**

![Планы льгот работника](./media/hr-benefits-management-workspace-plans.png)

При выборе плиток **Активных жизненные события** или **Будущие жизненные события** открывается список активных или будущих жизненных событий.

![Жизненные события](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a>Обрабатывается

Для обработки допустимости регистрации, жизненных событий или обновления изменения ставки выберите соответствующий элемент на панели навигации.

![Обрабатывается](./media/hr-benefits-management-workspace-processing.png)

Чтобы просмотреть результаты процесса, выберите **Результаты обработки** на странице.

![Результаты обработки](./media/hr-benefits-management-workspace-process-results.png)

Дополнительные сведения об обработке льгот см. в:

- [Обработка приемлемости регистрации](hr-benefits-process-enrollment-eligibility.md)
- [Обработка изменений событий в жизни](hr-benefits-process-life-event-changes.md)
- [Обработка допустимости событий в жизни](hr-benefits-process-life-event-eligibility.md)
- [Обработка событий в жизни](hr-benefits-process-life-events.md)
- [Обработка изменений рейтинга](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a>Изменить период

Для просмотра других льготных периодов выберите его из раскрывающегося списка **Период**.

![Изменить период](./media/hr-benefits-management-workspace-period.png)

## <a name="view-more-options"></a>Просмотр дополнительных параметров

Чтобы просмотреть дополнительные сведения и действия, которые можно выполнить, выберите **Ссылки**.

![Ссылки](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a>См. также

[Обзор управления льготами](hr-benefits-management-overview.md)