---
title: Настройка устройства для запуска интерфейса выполнения производственного цеха
description: Интерфейс выполнения производственного цеха настраивается для каждого устройства в производственном цехе. Компании обычно настраивают каждое устройство по-разному, в зависимости от цели, обслуживаемой устройством. Например, у компании может быть одно устройство в области проходной, где работники регистрируют времени прихода на работу и ухода с работы, а другое — в цехе, где работники управляют заданиями.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution, HcmWorker, JmgProductionFloorExecutionDeviceConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0ae9ca901a7af8275db419e25a7297a77aab284e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857412"
---
# <a name="set-up-a-device-to-run-the-production-floor-execution-interface"></a>Настройка устройства для запуска интерфейса выполнения производственного цеха

[!include [banner](../includes/banner.md)]

Интерфейс выполнения производственного цеха настраивается для каждого устройства в производственном цехе. Компании обычно настраивают каждое устройство по-разному, в зависимости от цели, обслуживаемой устройством. Например, у компании может быть одно устройство в области проходной, где работники регистрируют времени прихода на работу и ухода с работы, а другое — в цехе, где работники управляют заданиями.

## <a name="set-the-configuration-and-filters-for-a-specific-device"></a>Настройка конфигурации и фильтров для конкретного устройства

Чтобы задать конфигурацию и фильтры заданий для устройства, выполните вход на страницу **Выполнение производственного цеха**, используя учетную запись, имеющую роль безопасности, включающую обязанность *Ведение контроля времени*. (Среди готовых ролей безопасности эта обязанность есть только у роли *Супервизор производственного цеха*.) Затем выполните следующие шаги.

1. Перейдите на устройство, которое необходимо настроить, и войдите в Microsoft Dynamics 365 Supply Chain Management в качестве супервизора производственного цеха. (Используйте учетную запись, которая включает обязанность *Ведение контроля времени*.)
1. Убедитесь, что конфигурация доступна для устройства, которую вы настраиваете. Если конфигурация уже не существует, используется конфигурация по умолчанию. Дополнительные сведения о настройке конфигурации см. в разделе [Настройка интерфейса выполнения производственного цеха](production-floor-execution-configure.md).
1. Перейдите в раздел **Управление производством \> Выполнение производства \> Выполнение производственного цеха**.

    Если интерфейс выполнения производственного цеха уже настроен по крайней мере один раз на текущем устройстве, отображается страница входа. В противном случае отображается страница приветствия.

1. На странице входа или на странице приветствия выберите **Настроить**.
1. Выберите конфигурацию в списке.
1. Выберите **Далее**.
1. Выберите один или несколько фильтров для применения к текущему устройству. Эти фильтры помогут гарантировать, что на устройстве будут отображаться только соответствующие задания. Чтобы задать фильтр, выберите тип фильтра, чтобы открыть список значений, а затем выберите значение для фильтра. Доступны следующие фильтры:

    - **Производственное подразделение** — этот фильтр является фильтром высшего уровня. Обычно это относится к большой рабочей области, в которой есть несколько групп ресурсов и отдельных ресурсов.
    - **Группа ресурсов** — этот фильтр является фильтром среднего уровня. Обычно это относится к набору взаимосвязанный ресурсов в ограниченной части рабочей области. Если сначала выбран фильтр **Производственное подразделение**, в списке групп ресурсов отображаются только группы из этого подразделения. В противном случае отображаются все доступные группы ресурсов.
    - **Ресурс** — этот фильтр является наиболее конкретным фильтром. Обычно он относится к конкретной машине или другому отдельному ресурсу. Если сначала выбран фильтр **Группа ресурсов** и/или **Производственное подразделение**, в списке ресурсов отображаются только ресурсы из этой группы и/или подразделения. В противном случае отображаются все доступные ресурсы.

1. Нажмите **ОК**.
1. Появится страница входа, и устройство готово к использованию.

## <a name="allow-a-worker-to-override-the-default-filters"></a>Разрешение работнику на переопределение фильтров по умолчанию

Можно предоставить отдельным сотрудникам разрешение на изменение настроек фильтра для любого устройства, которое они используют. Для сотрудников с данным разрешением в интерфейсе выполнения производственного цеха имеется кнопка **Фильтр** на страницах **Все задания** и **Активные задания**.

> [!NOTE]
> Если работник изменяет фильтр, новый фильтр применяется с этого момента для всех пользователей, вошедших в это устройство.

Чтобы разрешить работнику переопределить фильтры заданий по умолчанию, настроенные для устройства, выполните следующие действия.

1. Перейдите в раздел **Посещаемость и время присутствия \> Настройка \> Регистрация времени — работники**.
1. Выберите сотрудника в списке, чтобы открыть страницу **Регистрация времени - работники** этого работника.
1. На вкладке **Регистрация времени** установите для параметра **Установить фильтры** значение *Да*.

## <a name="run-the-interface-in-full-screen-mode"></a>Запуск интерфейса в полноэкранном режиме

Часто интерфейс выполнения производственного цеха будет запускаться на устройстве, которое используется исключительно для этой цели. Таким образом, может иметь смысл запускать интерфейс в полноэкранном режиме, не отображая никаких переходов и/или элементов браузера.

- Чтобы скрыть область переходов, которая отображается в Supply Chain Management, добавьте следующий текст в конец URL-адреса в адресной строке браузера: `\&limitednav=true`.
- Чтобы также скрыть адресную строку браузера, используйте собственный полноэкранный режим браузера. (Инструкции см. в документации по браузеру.)

В верхней части на следующем рисунке показано, как интерфейс выглядит по умолчанию. Нижняя часть показывает, как он отображается в полноэкранном режиме, когда область переходов скрыта.

![Обычный и полноэкранный интерфейсы.](media/pfei-full-screen.png "Обычный и полноэкранный интерфейсы")

## <a name="extend-the-session-past-12-hours"></a>Продление сеанса сверх 12 часов

По умолчанию выход из интерфейса выполнения производственного цеха производится автоматически, если никто не использует его в течение 12 часов. Пользователь Supply Chain Management должен снова войти в систему. Однако предельное время ожидания можно продлить до 90 дней.

Чтобы продлить предельный тайм-аут, войдите в Supply Chain Management и перейдите в раздел **Администрирование системы \> Пользователи \> Продления сеансов**. Укажите учетную запись пользователя Supply Chain Management, используемую для входа в устройство, и число часов, в течение которых сеанс должен оставаться активным.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
