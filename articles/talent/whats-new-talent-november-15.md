---
title: Что нового и что изменилось в Dynamics 365 Talent - Core HR (15 ноября 2018 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a7598db1dc4c11864cf5f5a73d00672ceb66e8c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462346"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-15-2018"></a>Что нового и что изменилось в Dynamics 365 Talent - Core HR (15 ноября 2018 г.)

**Сборка 8.1.2045**

В этой теме описываются новые и измененные компоненты Core HR.

## <a name="other-changesfixes"></a>Другие изменения/исправления

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a>Не удается изменить текущую должность сотрудника на будущую открытую должность

Изменение было сделано для обеспечения переносов должностей, когда должность будет доступна только в будущем. 

### <a name="position-does-not-display-when-creating-a-new-employee"></a>Должность не отображается при создании нового сотрудника

Внесено изменение для отображения всех открытых вакансий, которые доступны для назначения при приеме на работу новых сотрудников в Talent. Это включает исторические должности или должности с будущей датой. Должности теперь будут появляться правильно в зависимости от даты начала работы. 

### <a name="termination-date-is-displaying-based-on-user-settings"></a>Дату увольнения отображается на основе параметров пользователя

Внесено изменение в список прошлых сотрудников для учета любые смещений часового пояса для предпочтительного часового пояса сотрудников при просмотре даты увольнения.

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a>Ссылки на рабочие элементы, назначенные мне, не отображают правильную информацию

С этим изменением переход к подробным сведениям отдельных рабочих элементов в списке будет отображаться правильная информация для выбранного элемента. Эта проблема возникает только с расширенными параметрами безопасности.


## <a name="known-issue"></a>Известная проблема

- **Проблема**: при добавлении нового вложения для работника кнопки **Создать** и **Изменить** неактивны. 
- **Временное решение:** перед открытием страницы вложения убедитесь, что информационные панели на странице **Рабочий** закрыты. Если информационные панели закрыты при загрузке страницы **Работник**, кнопки вложений будут активны. (Эта проблема будет исправлена в следующем обновлении платформы.)
