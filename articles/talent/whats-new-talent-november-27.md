---
title: Что нового и что изменилось в Dynamics 365 for Talent Core HR (27 ноября 2018 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6bd049bfe4639136276ab2f14e6310e45d1254f2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "305903"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-27-2018"></a>Что нового и что изменилось в Dynamics 365 for Talent Core HR (27 ноября 2018 г.)

[!include [banner](includes/banner.md)]

**Сборка 8.1.2064**

В этой теме описываются новые и измененные компоненты Core HR.


## <a name="changes"></a>Изменения

### <a name="unable-to-create-a-note-in-case-management"></a>Не удается создать примечание в управлении обращениями

Было сделано изменение для проблемы при попытке изменить или создать примечание в журнале обращений управления обращениями.

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a>Неправильно написанное слово на вкладке аналитики в рабочей области компенсации 

Изменение сделано для исправления орфографии слов "Этническое происхождение" в диаграмме аналитики компенсации в рабочей области компенсации.

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a>Рабочая область самообслуживания сотрудников не отображается, когда пользователь не назначен работнику 

Внесено изменение, когда рабочая область **Самообслуживание сотрудников** выбрана в качестве начальной страницы при запуске для пользователя, которому не назначен работник. В этом случае будет отображена панель мониторинга по умолчанию.

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a>Ошибка отпусков и отсутствия: ссылка на объект не указывает на экземпляр объекта

Были внесены изменения в модуль отпусков и отсутствия для исправления этой ошибки после утверждения записей отпусков и отсутствия в списке **Рабочие элементы, назначенные мне**.

### <a name="unable-to-recall-an-image-workflow"></a>Не удается вызвать workflow-процесс изображения

После отзыва workflow-процесса изображения workflow-процесс будет задано значение "отменен" и существующий запрос может быть удален из рабочей области самообслуживания сотрудников.

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a>Повторно принятые на работу сотрудники или подрядчики отображаются несколько раз после увольнения 

С этим обновлением уволенные сотрудники, которые были повторно приняты на работу, будут отображаться только один раз в списке уволенных. 

## <a name="known-issue"></a>Известная проблема

- **Проблема**: при добавлении нового вложения для работника кнопки **Создать** и **Изменить** неактивны. 
- **Временное решение:** перед открытием страницы вложения убедитесь, что информационные панели на странице **Рабочий** закрыты. Если информационные панели закрыты при загрузке страницы **Работник**, кнопки вложений будут активны. (Эта проблема будет исправлена в следующем обновлении платформы.)
