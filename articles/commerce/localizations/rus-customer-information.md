---
title: Управление информацией по клиентам для России
description: В этой теме описываются сценарии обработки информации о клиентах в POS-терминале Microsoft Dynamics 365 Commerce для России.
author: EvgenyPopovMBS
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailParameters
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Russia
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2021-8-2
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 4b266ad814aa283c648f72242b8abf47d809b5af
ms.sourcegitcommit: 47a3ad71210c7ac84d0c25e913c440b5ba205282
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2021
ms.locfileid: "7512905"
---
# <a name="customer-information-management-for-russia"></a>Управление информацией по клиентам для России

[!include [banner](../includes/banner.md)]

В этой теме описываются сценарии обработки информации о клиентах в POS-терминале Microsoft Dynamics 365 Commerce для России.

Dynamics 365 Commerce позволяет указать сведения о клиенте, такие как номер телефона или адрес электронной почты, при создании или редактировании основной записи клиента в POS-терминале. Можно также указать сведения о клиенте для проводки по продажам, скопировав сведения из клиента, указанного в проводке, или введя их вручную. Затем в финансовый чек могут быть включены сведения о клиенте. Сведения о создании и печати финансовых чеков см. в разделе [Пример интеграции финансового принтера для России](rus-fpi-sample.md).

> [!NOTE]
> Сведения о клиенте включаются в финансовый чек, который отправляется на финансовый принтер. Однако они не печатаются на образце финансового чека. Чтобы напечатать сведения о клиенте в финансовом чеке, необходимо настроить образец финансового чека.

## <a name="example-scenarios"></a>Пример сценариев

В следующих примерах сценариев показано, как работать с информацией о клиенте в Commerce POS для России.

### <a name="scenario-1-make-a-sale-to-an-anonymous-customer"></a>Сценарий 1. Выполнение продажи для анонимного клиента

1. Войдите в POS.
1. Добавьте номенклатуры в корзину.
1. Выберите **Добавить сведения о клиенте**, затем выберите **Ввести вручную**.
1. Выберите, будет ли указан номер телефона или адрес электронной почты.
1. Введите сведения о клиенте, затем выберите **ОК**.
1. Зарегистрируйте платежи для проводки, затем завершите проводку. Финансовый чек, который отправляется на финансовый принтер, включает сведения о клиенте.

### <a name="scenario-2-make-a-sale-to-a-new-named-customer"></a>Сценарий 2. Выполнение продажи новому именованному клиенту

1. Войдите в POS.
1. Добавьте номенклатуры в корзину.
1. Выберите **Добавить клиента** и нажмите **Создать**.
1. Задайте атрибуты нового клиента. Включены следующие атрибуты:

    - Основной адрес электронной почты и/или адрес электронной почты для отправки чеков
    - Основной номер телефона

1. Сохраните запись клиента и добавьте клиента в проводку.
1. Зарегистрируйте платежи для проводки, затем завершите проводку.
1. Поскольку запрос информации о клиенте активирован, но сведения о клиенте еще не добавлены в проводку, отображается диалоговое окно **Ввод сведений о клиенте**. Выберите **Да**, затем выберите **Копировать из клиента проводки**.
1. Выберите, следует ли копировать номер телефона или адрес электронной почты в сведения о клиенте.
1. Проверьте сведения о клиенте, затем выберите **ОК**. Финансовый чек, который отправляется на финансовый принтер, включает сведения о клиенте.

> [!NOTE]
> Чтобы указать для проводки другого клиента, необходимо сначала очистить информацию о клиенте, затем снова скопировать ее после добавления нового клиента.

### <a name="scenario-3-change-the-customer-information-for-a-sale-to-a-named-customer"></a>Сценарий 3. Изменение сведений о клиенте для продажи именованному клиенту

1. Войдите в POS.
1. Добавьте номенклатуры в корзину.
1. Выберите **Добавить клиента**, затем выберите учетную запись клиента для добавления в проводку.
1. Выберите **Добавить сведения о клиенте**, затем выберите **Копировать из клиента проводки**.
1. Выберите, следует ли копировать номер телефона или адрес электронной почты в сведения о клиенте.
1. Проверьте сведения о клиенте, затем выберите **ОК**.
1. Выберите **Добавить сведения о клиенте**, затем выберите **Очистить**, чтобы удалить сведения о клиенте из проводки.
1. Выберите **Добавить сведения о клиенте**, затем выберите **Ввести вручную**.
1. Выберите, будет ли указан номер телефона или адрес электронной почты.
1. Введите сведения о клиенте, затем выберите **ОК**.
1. Зарегистрируйте платежи для проводки, затем завершите проводку. Финансовый чек, который отправляется на финансовый принтер, включает сведения о клиенте.

## <a name="setup"></a>Настройка

Чтобы использовать функциональность сведений о клиенте, вы должны завершить следующие шаги настройки:

- [Добавьте операцию **Добавить сведения о клиенте** в макеты экрана](#add-the-add-customer-information-operation-to-screen-layouts).
- [Активируйте запрос для сведений о клиенте](#activate-the-inquiry-for-customer-information).
- [Настройте компоненты каналов](#configure-channel-components).

### <a name="add-the-add-customer-information-operation-to-screen-layouts"></a>Добавление операции "Добавить сведения о клиенте" в макеты экрана

Операция **Добавить сведения о клиенте** может использоваться для добавления в проводку продаж сведений о клиенте, таких как номер телефона или адрес электронной почты. Эти сведения могут быть скопированы из клиента, указанного для проводки, или они могут вводиться вручную.

Чтобы добавить операцию **Добавить сведения о клиенте** в макет экрана в Commerce POS для России, выполните следующие действия.

1. На странице **Сетки кнопок** выберите сетку кнопок, в которой должна появиться операция, затем откройте конструктор сетки кнопок.
1. Добавьте новую кнопку, затем в поле **Действие** выберите **Добавить сведения о клиенте**. 

Дополнительные сведения о работе с макетами экранов и сетками кнопок см. в разделе [Визуальные конфигурации пользовательского интерфейса POS](../pos-screen-layouts.md).

### <a name="activate-the-inquiry-for-customer-information"></a>Активация запроса для сведений о клиенте

Если сведения о клиенте не указаны для проводки по продаже, запрос на эту информацию может быть автоматически активирован после завершения проводки. Этот подход является альтернативой операции **Добавить сведения о клиенте**.

Чтобы активировать запрос информации о клиенте в модуле Commerce, выполните следующие действия.

1. Перейдите в раздел **Рабочие области \> Управление функциями**.
1. Включите функцию **(Россия) Управление сведениями о клиентах в Retail POS**.
1. Перейдите в раздел **Профили функциональности POS**.
1. На экспресс-вкладке **Функции** в разделе **Параметры налога** установите для параметра **Включить запрос сведений о клиенте в проводках по продажам** значение **Да**.

### <a name="configure-channel-components"></a>Настройка компонентов канала

Чтобы сделать функциональность, относящуюся к России, доступной, необходимо настроить расширения для компонентов каналов Commerce. Дополнительные сведения см. в разделе [Включение специфических для России компонентов Commerce](./rus-commerce-setup.md#enable-russia-specific-commerce-components).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Пример интеграции фискальных принтеров для России](rus-fpi-sample.md)

[Визуальные конфигурации пользовательского интерфейса POS](../pos-screen-layouts.md)

[Включение специфических для России компонентов Commerce](./rus-commerce-setup.md#enable-russia-specific-commerce-components)