---
title: Настройка карты задания для устройств
description: В этой статье описываются различные параметры настройки устройства карты задания.
author: johanhoffmann
ms.date: 05/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch, JmgRegistrationTouchUserConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: c3024ca2e3b7eb24ac9a171def4a72cde7493a7a
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708626"
---
# <a name="configure-job-card-for-devices"></a>Настроить карту заданий для устройств

[!include [banner](../includes/banner.md)]

Устройство карты задания используется сотрудниками производственного цеха для регистрации своей ежедневной работы, например времени начала заданий, обратной связи по заданиям, регистрации дополнительных мероприятий и регистрации отсутствия. Эти регистрации являются основой для отслеживания хода выполнения работ и затрат на производственные заказы и для расчета базиса для оплаты работников. В этой статье описываются различные параметры настройки устройств карты задания.

## <a name="enable-new-features-in-feature-management"></a>Включение новых функций в управлении функциями

Некоторые параметры, описанные в этой статье, должны быть включены в системе, прежде чем они будут доступны для использования. На странице [управления функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) можно включить необходимые функции.

### <a name="generate-license-plate"></a>Создать грузоместо

Чтобы эта функция была доступна, включите следующие функции в [управлении функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (в указанном порядке):

1. *Грузоместо для приемки добавлено в устройство карты задания*<br>(В Supply Chain Management версии 10.0.21 эта функция включена по умолчанию. В Supply Chain Management версии 10.0.25 эта функция обязательна.)
1. *Включение автоматического создания номерного знака при приемке на устройстве карты задания*<br>(В Supply Chain Management версии 10.0.25 эта функция обязательна.)

### <a name="print-label"></a>Печать этикетки

Чтобы эта функция была доступна, включите следующие функции в [управлении функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (в указанном порядке):

1. *Грузоместо для приемки добавлено в устройство карты задания*<br>(В Supply Chain Management версии 10.0.21 эта функция включена по умолчанию. В Supply Chain Management версии 10.0.25 эта функция обязательна.)
1. *Печать этикетки с устройства карты задания*<br>(В Supply Chain Management версии 10.0.25 эта функция обязательна.)

### <a name="allow-locking-of-touch-screen"></a>Разрешить блокировку сенсорного экрана

В Supply Chain Management версии 10.0.21 эта функция включена по умолчанию. В Supply Chain Management 10.0.25 эта функция обязательна и не может быть отключена. При работе с версией, более ранней, чем 10.0.25, администраторы могут включать или выключать эту функцию путем поиска функции *Функция для блокировки устройства карты задания и терминала карты задания для дезинфекции* в рабочей области [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="manage-your-device-configurations"></a>Управление конфигурациями устройств

Для настройки конфигураций устройств перейдите **Управление производством > Настройка > Управление производством > Настроить карту заданий для устройств**. Откроется страница **Настроить карту заданий для устройств**, на которой отображается список существующих конфигураций. Здесь можно выполнить следующие необязательные действия. 

- Выберите любую конфигурацию устройства, указанную в левом столбце, для просмотра и редактирования.
- Выберите **Создать** на панели операций, чтобы добавить в список новую конфигурацию устройства. Затем введите имя в поле **Конфигурация**, чтобы идентифицировать новую конфигурацию. Введенное здесь значение должно быть уникальным для всех конфигураций устройств, и его нельзя изменить позже.

В следующих разделах приведены подробные сведения о каждом из параметров настройки устройств карты задания.

## <a name="general-settings"></a>Общие параметры

На Экспресс-вкладка **Общие** можно настраивать различные параметры, доступные для выбранной конфигурации устройства. Доступны следующие параметры:

- **Сообщать о количестве на время ухода** — установите значение **Да**, чтобы сотрудникам выдавалось напоминание об указании обратной связи по выполняемым заданиям при регистрации времени ухода с работы. Если указано значение **Нет**, работники не будут получать запрос.
- **Блокировать сотрудника** — когда для этого параметра установлено значение **Нет**, для каждого работника будет выполнен выход сразу после регистрации (например, нового задания), а затем устройство вернется на страницу входа в систему. Если этот параметр задан как **Да**, каждый работник останется в системе на устройстве карты задания. Однако работник по-прежнему может выйти из системы вручную, чтобы разрешить другому работнику войти в систему, пока устройство карты задания остается в системе под той же учетной записью пользователя. Для получения дополнительных сведений о учетных записей см. [Назначенные пользователи](#assigned-users).
- **Сканер штрих-кодов** — установите значение **Да**, чтобы задать параметр на устройстве карты задания, который позволяет сотрудникам регистрировать начало нового задания путем сканирования штрих-кода.
- **Использовать реальное время регистрации** — установите значение **Да**, чтобы задать время для каждой новой регистрации, равное точному времени, когда работнику была отправлена регистрация. При значении **Нет** вместо этого будет использоваться время входа. Обычно это значение устанавливается равным **Да**, если включен параметр **Блокировать сотрудника** и/или **Один сотрудник**, когда работники часто остаются в системе в течение длительных периодов.
- **Один сотрудник** — установите для этого параметра значение **Да**, если только один работник использует каждое устройство карты задания, в котором активна данная конфигурация. Если этот параметр установлен, параметр **Блокировать сотрудника** автоматически задается как **Да**. Кроме того, этот параметр позволяет удалить требование (и возможность) для входа работника в систему с использованием кода значка работника (или аналогичного). Вместо этого работник выполняет вход в Supply Chain Management с использованием учетной записи пользователя системы, связанной с *работником с зарегистрированным временем* (из таблицы *Работники*), и входит в устройство карты задания в качестве этого сотрудника в это же время.  Для получения дополнительных сведений о учетных записей см. [Назначенные пользователи](#assigned-users).
- **Разрешить работникам задавать личные фильтры** — установите этот параметр как **Да**, чтобы разрешить сотрудникам фильтровать задания, показанные им на устройстве. Работник может изменять значения для любого из трех критериев фильтрации: **Производственное подразделение**, **Группа ресурсов** и **Ресурс**. На устройстве будут отображаться только задания, запланированные для ресурсов, соответствующих выбранному критерию фильтрации. Можно также назначить значения по умолчанию для определенных критериев и выбрать, какие из них будут применяться, даже если этот параметр не выбран.
- **Разрешить блокировку сенсорного экрана** — установите этот параметр как **Да**, чтобы разрешить работникам блокировать сенсорный экран устройства карты задания для санитарной обработки. Если этот параметр включен, на страницу входа в устройство добавляется кнопка **Блокировать экран для санитарной обработки**. Когда работник нажимает эту кнопку, сенсорный экран временно блокируется, чтобы исключить непредусмотренный ввод данных и показывает таймер обратного отсчета. После этого работник может спокойно очистить устройство и экран. После завершения обратного отсчета сенсорный экран автоматически разблокируется.
- **Длительность блокировки экрана** — когда включен параметр **Разрешить блокировку сенсорного экрана**, используйте этот параметр, чтобы задать количество секунд, в течение которого сенсорный экран должен блокироваться для санитарной обработки. Длительность должна быть в интервале от 5 до 120 секунд.
- **Производственное подразделение** — выберите производственное подразделение, которое будет использоваться как критерий фильтра по умолчанию для списка заданий, отображаемых для каждого сотрудника. Только задания, запланированные для ресурсов, сгруппированных для выбранного производственного подразделения, первоначально отображаются устройством. Если включено **Разрешить работникам задавать личные фильтры**, работники смогут изменять это значение; в противном случае этот фильтр будет применяться всегда, когда конфигурация устройства активна.
- **Группа ресурсов** — выберите группу ресурсов, которое будет использоваться как критерий фильтра по умолчанию для списка заданий, отображаемых для каждого сотрудника. Только задания, запланированные для ресурсов, сгруппированных для выбранной группы ресурсов, первоначально отображаются устройством. Если включено **Разрешить работникам задавать личные фильтры**, работники смогут изменять это значение; в противном случае этот фильтр будет применяться всегда, когда конфигурация устройства активна.
- **Ресурс** — выберите ресурс, который будет использоваться как критерий фильтра по умолчанию для списка заданий, отображаемых для каждого сотрудника. Только задания, запланированные для выбранного ресурса, первоначально отображаются устройством. Если включено **Разрешить работникам задавать личные фильтры**, работники смогут изменять это значение; в противном случае этот фильтр будет применяться всегда, когда конфигурация устройства активна.
- **Создать грузоместо** — установите этот параметр как **Да**, чтобы создать новое грузоместо каждый раз, когда сотрудник использует устройство карты задания для приемки. Номерной знак создается на основе номерной серии, настроенной на странице **Параметры управления складом**. Если значение задано как **Нет**, работники должны указать существующее грузоместо при приемке.
- **Печать этикетки** — установите этот параметр как **Да**, чтобы печатать этикетку грузоместа, когда работник использует устройство карты задания для приемки. Конфигурация метки настраивается в маршрутизации документа, как описано в разделе [Макеты этикеток маршрутизации документов](../warehousing/document-routing-layout-for-license-plates.md).

<a name="assigned-users"></a>

## <a name="assigned-users"></a>Назначенные пользователи

На экспресс-вкладке **Назначенные пользователи** можно связать одного или нескольких пользователей с текущей конфигурацией устройства. Каждому пользователю системы может быть назначена только одна конфигурация устройства задания.

При настройке устройства ИТ-сотрудник обычно входит в Supply Chain Management с использованием учетной записи пользователя системы. Таким образом, конфигурация устройства задания, связанная с этим пользователем, будет применяться только в том случае, пока пользователь остается в системе. Этим учетным записям пользователей обычно ограничен доступ только страницей устройства карты задания, а не к какой-либо другой частью Supply Chain Management.

После того как пользователь войдет в систему и загружена конфигурация устройства задания, работники могут затем войти в устройство карты задания, используя учетную запись *работником с зарегистрированным временем* (например, путем сканирования штрих-кода на своем значке работника), чтобы они могли начать новые задания и выполнить другие виды регистраций. Различные работники могут входить в систему и выходить из нее в течение дня, в то время как конфигурация устройства действует на компьютере, потому что пользователь остается в Supply Chain Management в течение всего дня.

Однако, как упоминалось ранее, при использовании конфигурации устройства с параметром **Один работник** сами работники обычно выполняют вход в Supply Chain Management, используя учетную запись пользователя, связанную с собственной учетной записью *работника с зарегистрированным временем*, поэтому они загружают конфигурацию устройства и выполняют вход в качестве сотрудника на устройстве карты задания в это же время.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Приемка с устройства карты задания](report-finished-job-device.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]