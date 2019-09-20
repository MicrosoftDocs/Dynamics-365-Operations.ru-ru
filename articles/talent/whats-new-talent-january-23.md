---
title: Что нового и что изменилось в Dynamics 365 for Talent Core HR (23 января 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4e492095d5269ec81c0c22145b7af356937c256b
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742524"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a>Что нового и что изменилось в Dynamics 365 for Talent Core HR (23 января 2019 г.)

[!include [banner](includes/banner.md)]

**Сборка 8.1.2121**

В этой теме описываются новые и измененные компоненты Core HR.

## <a name="changes"></a>Изменения

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a>Импорт фиксированной компенсации сотрудников не работает при создании новых записей фиксированной компенсации
Сделано изменение, чтобы сущность фиксированной компенсации сотрудников извлекала уровень компенсации при импорте. До этого выпуска отображалось сообщение, указывающее на то, что требовался уровень.

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a>Удалить поле минимального сальдо из диалогового окна запроса отгула
Поле **Минимальное сальдо** было удалено из диалогового окна **Запрос отгула**. Это изменение затрагивает все области, где можно запросить отгул.

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a>Обновление данных для уровней компенсации обновляется не во всех сценариях
Изменение сделано для обновления уровня компенсации в планах фиксированной компенсации. Это изменение приведет к заполнению уровня компенсации в фиксированных планах для должности, назначенной сотруднику.

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a>Информация о заработной плате на странице "Управление изменениями" доступна только при входе от имени системного администратора
Это изменение позволяет сотрудникам с ролью администратора заработной платы получать доступ к информации на странице **Временная шкала изменений > Управление изменениями** для должности.

### <a name="job-fields-default-to-positions"></a>Поля должности принимают значения по умолчанию для позиций
При изменении должности на позицию поля должности принимают значения по умолчанию для этой позиции. Оповещающее сообщение появится, давая возможность принять значения по умолчанию или сохранить текущие значения для этих полей.

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a>Период надзора и календарь не отображаются для будущих нанимаемых сотрудников.
После этого изменения поля **Период надзора** и **Календарь** были добавлены на страницу **Управление изменениями**, чтобы позволить вводить данные для будущих и прошлых сотрудников.

### <a name="platform-update-23"></a>Обновление платформы update 23
Исправления мелких ошибок были включены в состав обновления платформы 23. Дополнительные сведения см. в разделе [Что нового и что изменилось в Dynamics 365 for Finance and Operations, обновление платформы 23 (январь 2019 г.)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23). 
