---
title: "Время розничной торговли и посещаемость"
description: "В этом разделе описываются сценарии, поддерживаемые для управления временем и посещаемостью в Microsoft Dynamics 365 for Operations - Retail."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: eac0b85a17df33c860333c5c19d4fb58f160930f
ms.lasthandoff: 03/31/2017


---

# <a name="retail-time-and-attendance"></a>Время розничной торговли и посещаемость

[!include[banner](includes/banner.md)]


В этом разделе описываются сценарии, поддерживаемые для управления временем и посещаемостью в Microsoft Dynamics 365 for Operations - Retail. 

<a name="manage-worker-setup-and-scheduling"></a>Настройка и планирование управления работниками
----------------------------------

### <a name="initial-configuration"></a>Начальная конфигурация

-   Запустите мастер конфигурации.
-   Зарегистрируйте работников как работников с регистрацией времени.

### <a name="plan-worker-schedules"></a>Планирование расписаний работника

-   Примените профили, воспользовавшись планировщиком работы. Дополнительные сведения см. в разделе <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Сведения об этапах настройки см. в разделе <https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>Конфигурация для розничной торговли

-   Включите профиль функциональности "Таймер" для работников, для который нужно включить регистрацию времени. Щелкните **Профили функциональности POS** &gt; **Функции** &gt; **Регистрации времени POS** &gt; **Включить регистрации времени**.
-   Настройте группы разрешений POS, чтобы включить разрешение "Просмотр записей таймера". Это разрешение позволяет пользователю просматривать регистрации времени других работников магазина (и из любого другого магазина, с которым связан пользователь, через адресную книгу). Это разрешение имеет смысл включить для менеджера, например, но не для кассира. Щелкните **Группы разрешений POS** &gt; **Просмотр записей таймера**.

## <a name="register-time"></a>Зарегистрировать время
### <a name="cashier-and-non-cashier-time-registrations"></a>Регистрация времени кассира и других сотрудников

-   В POS:
    -   Операции прихода:
        -   выполните вход с помощью операции, не связанной с денежным ящиком, или начните новую смену.
        -   Выберите операцию "Таймер".
        -   Выберите нужную операцию:
            -   Время прихода
            -   Перерыв в работе
            -   Перерыв на обед
            -   Время ухода

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Текущий статус</th>
    <th>Доступные операции</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Время прихода</td>
    <td><ul>
    <li>Перерыв в работе</li>
    <li>Перерыв на обед</li>
    <li>Время ухода</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Перерыв в работе</td>
    <td>Время прихода</td>
    </tr>
    <tr class="odd">
    <td>Перерыв на обед</td>
    <td>Время прихода</td>
    </tr>
    <tr class="even">
    <td>Время ухода</td>
    <td>Время прихода</td>
    </tr>
    </tbody>
    </table>

    [![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)
-   Просмотрите сообщение конфигурации и убедитесь, что время текущего действия указано верно.
-   Регистрационный журнал:
    -   Щелкните **Регистрационный журнал**, чтобы просмотреть деятельность таймера.
    -   Используйте временные фильтры, чтобы выбрать другие периоды.
    -   Если вы работаете в нескольких магазинах, вы увидите свои регистрации времени изо всех магазинов, где вы фиксировали время. Можно использовать фильтр магазина для просмотра регистраций времени в выбранном магазине.

<!-- -->

-   Другие часовые пояса:
    -   если вы просматриваете время из другого расположения (для регистрационного журнала кассира или с помощью команды **Просмотр записей таймера** в случае менеджера) и это расположение находится в другом часовом поясе, отображаемые записи времени переводятся в ваш локальный часовой пояс. Например, вы менеджер в двух магазинах: один — в Аризоне, а другой — в Неваде. Кассир регистрирует приход в 09:00 в Аризоне. В Неваде в это время 08:00. Поэтому если вы в магазине в Неваде смотрите записи регистрации времени, время регистрации отмечено как 08:00.

## <a name="view-worker-time-registrations"></a>Просмотр регистраций времени работников
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Просмотрите регистрации времени работников и отфильтруйте их по магазину или типу деятельности

В POS:

-   Выберите **Просмотр записей таймера**.
-   Вы увидите действия по регистрации таймера для всех работников, назначенных тем же магазинам, что и вы.
-   Можно использовать фильтры по типу деятельности и магазину, чтобы отфильтровать регистрации времени.

## <a name="process-and-manage-time-registrations"></a>Обработка регистраций времени и управление ими
Пользователь Dynamics 365 for Operations - Retail выполняет workflow-процесс, чтобы вычислить, утвердить и перенеси регистрации времени в зарплату.

### <a name="primary-operations"></a>Основные операции

-   Рассчитать
-   Утвердить
-   Отправить на зарплату

### <a name="other-common-operations"></a>Прочие распространенные операции

-   Массовый уход
-   Регистрация отсутствия

Дополнительные сведения об обработке регистраций времени и посещаемости см. в разделе <https://technet.microsoft.com/en-us/library/aa573180.aspx>.



