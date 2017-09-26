---
title: "Настройка программы лояльности клиентов"
description: "В этой статье описывается, как настроить программу лояльности. Программы лояльности могут повысить лояльность постоянного клиента благодаря тому, что клиент получает поощрения, приобретая продукты в магазинах розничной торговли. В Microsoft Dynamics 365 for Retail можно настроить простые или сложные программы лояльности, которые применяются ко всем юридическим лицам в любом канале розничной торговли."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16201
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 710f8ae3a6a2b5072f37879aad066dc699ede8f0
ms.contentlocale: ru-ru
ms.lasthandoff: 06/20/2017

---

# <a name="set-up-a-customer-loyalty-program"></a>Настройка программы лояльности клиентов

[!include[banner](includes/banner.md)]


В этой статье описывается, как настроить программу лояльности. Программы лояльности могут повысить лояльность постоянного клиента благодаря тому, что клиент получает поощрения, приобретая продукты в магазинах розничной торговли. В Microsoft Dynamics 365 for Retail можно настроить простые или сложные программы лояльности, которые применяются ко всем юридическим лицам в любом канале розничной торговли.

<a name="loyalty-features"></a>Характеристики лояльности
----------------

Вы можете настроить вашу программу лояльности, чтобы она включала следующие варианты:

-   Настройка нескольких типов поощрений, которые предлагаются в программах лояльности, и отслеживание участия в программах лояльности.
-   Настройка программ лояльности, которая представляет различные поощрения, предлагаемые компанией. Можно создать уровни программы лояльности для предложения более значимых поощрений и вознаграждений клиентам, которые совершают покупки чаще или тратят больше денег в магазинах.
-   Настройка правил начисления для определения действий, которые должен выполнить клиент, чтобы заработать поощрения. Можно также определить правила списания, чтобы указать, когда и как клиент может списывать поощрения.
-   Выпуск карточек постоянного клиента в любом канале розничной торговли, который участвует в программах лояльности, и привязка карточек постоянного клиента к одной или нескольким программам лояльности, в которых может участвовать клиент. Можно также связать запись клиента с карточкой постоянного клиента для предоставления клиенту возможности использовать баллы по программе лояльности на нескольких карточках и списывать их.
-   Настройка карточек постоянного клиента вручную или перенос баланса поощрений лояльности с одной карточки на другую, чтобы выполнить требования клиента или поощрить его.

## <a name="setting-up-loyalty-programs"></a>Настройка программ лояльности
Необходимо настроить несколько компонентов, чтобы включить функцию лояльности в Dynamics 365 for Retail. На следующей схеме показаны компоненты лояльности и то, как они связаны друг с другом. ![Последовательность операций при настройке лояльности](./media/loyaltyprocess.gif)

## <a name="loyalty-components"></a>Компоненты лояльности
В следующей таблице приводится описание каждого компонента и указывается, где он используется при настройке лояльности.

| Компонент                                        | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Использование                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Настройка скидок (необходимое условие)                  | Настройка скидок, предлагаемых постоянным клиентам. Например, вы можете предложить скидку 5 процентов на всю повседневную одежду.                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Чтобы можно было включить скидки в программу лояльности, их необходимо добавить в ценовые группы. Ценовые группы назначаются программам лояльности и уровням лояльности.                                                                                                                                                                                                                      |
| Настройка ценовых групп (необходимое условие)               | Ценовые группы используются для создания цен и скидок для розничных продуктов и управления ими. Настройте ценовые группы, включающие скидки, которые применяются к программам лояльности.                                                                                                                                                                                                                                                                                                                                                                                                             | Ценовые группы назначаются программам лояльности и уровням программ лояльности.                                                                                                                                                                                                                                                                                                        |
| Настройка каналов (необходимое условие)                   | Каналы розничной торговли — это магазины, участвующие в программах лояльности, такие как физические магазины, интернет-магазины или центры обработки вызовов. Необходимо настроить каналы розничной торговли перед назначением им программ лояльности.                                                                                                                                                                                                                                                                                                                                                      | Каналы розничной торговли назначаются программе лояльности, если канал розничной торговли участвует в программе лояльности.                                                                                                                                                                                                                                                                  |
| Настройка способа оплаты по программе лояльности (необходимое условие) | Прежде чем карточку постоянного клиента можно будет использовать на кассе, а баллы по программе лояльности можно будет применять в рамках программы лояльности, необходимо настроить способ оплаты. Кроме того, необходимо добавить способ оплаты по программе лояльности в канал розничной торговли, прежде чем клиенты получать возможность использовать баллы по программе лояльности для оплаты продуктов.                                                                                                                                                                                                                                                                                           | Настройте способ оплаты типа программы лояльности, а затем назначьте способ оплаты по программе лояльности каналам розничной торговли, участвующим в программе лояльности.                                                                                                                                                                                                                          |
| Настройка интервалов дат                            | Интервалы дат позволяют гибко настраивать период времени для уровней лояльности. Используйте интервалы дат для того, чтобы определить, сколько времени клиент может оставаться на уровне или сколько времени имеет клиент на то, чтобы выполнить действие, необходимое для квалификации на уровень.                                                                                                                                                                                                                                                                                                                                            | Интервалы дат применяются, только если в программах лояльности используются уровни. Можно выбрать интервал дат, который применяется к уровням программы, а также интервалы дат, которые применяются к правилам уровней программы.                                                                                                                                                                                  |
| Настройка баллов поощрения                             | Баллы поощрения — это типы поощрения, предлагаемые клиентам. Баллы поощрения могут иметь или не иметь возможность списания. Баллы поощрения с возможностью списания можно обменять на продукты. Баллы поощрения без возможности списания используются для отслеживания сведений о клиенте или перевода клиента на следующий уровень программы лояльности.                                                                                                                                                                                                                                                                          | Баллы поощрения определяются в правилах уровней и используются для перевода клиента на определенный уровень. Баллы поощрения также определяются в схемах лояльности в правилах начисления и списания. В правилах начисления определяются поощрения, которые клиент может получить, выполнив определенные действия. В правилах списания определяются поощрения, которые клиент может списать.                  |
| Настройка программ лояльности                          | Программы лояльности — это основной объект лояльности, предлагаемый компанией. Каждая программа лояльности может иметь уровни лояльности. Скидки и ценовые группы назначаются программам лояльности на уровне программы или на уровне уровня.                                                                                                                                                                                                                                                                                                                                             | Для программ лояльности можно создать схемы лояльности. Программам лояльности можно назначить карточки постоянного клиента, а карточки постоянного клиента можно назначить клиенту. Каналы розничной торговли участвуют в программах лояльности, назначенных схемам лояльности. Любой клиент, имеющий карточку постоянного клиента, может участвовать в программах лояльности, назначенных карточке.            |
| Настройка уровней лояльности и правил уровней              | Уровни лояльности — это дополнительные уровни, которые можно определить для программ лояльности. Можно настроить базовые скидки и поощрения для всех клиентов, участвующих в программе лояльности, а также дополнительные скидки и поощрения для клиентов, которые находятся на разных уровнях программы. Для каждого определяемого уровня лояльности можно настроить правила перевода клиента на данный уровень. Можно также указать период времени, в течение которого клиенты могут оставаться на данном уровне после перехода на него.                                                                                  | Уровни лояльности и правила уровней лояльности определяются в программах лояльности. Если не определить уровни лояльности, все клиенты, участвующие в программе лояльности, имеют право на скидки, назначенные в ценовой группе программы лояльности. Если определить уровни лояльности, можно настроить правила начисления и правила списания для уровней лояльности в схеме лояльности. |
| Настройка схем программы лояльности                           | В схемах лояльности указываются правила начисления и правила списания, которые применяются к выбранной программе лояльности. Каналы розничной торговли назначаются схеме лояльности для указания того, какая программа лояльности, правила начисления и правила списания применяются к магазину розничной торговли.                                                                                                                                                                                                                                                                                                                                  | Схема лояльности назначается программе лояльности и каналам розничной торговли. Можно назначить несколько схем лояльности одной программе лояльности и можно назначить несколько схем лояльности множеству каналов розничной торговли.                                                                                                                                                                        |
| Настройка карточек постоянного клиента                             | Карточка постоянного клиента дает владельцу карточки право участвовать в программах лояльности, назначенных карточке. Карточки постоянного клиента можно выпускать анонимно, или они могут назначаться определенному клиенту. Можно просмотреть проводки по программе лояльности для определенной карточки, а также просмотреть сводку баллов по программе лояльности, накопленных на карточке. Карточки постоянного клиента можно выпускать в любом канале розничной торговли. Можно также вручную скорректировать карточку постоянного клиента, чтобы перевести клиента на другой уровень, добавить баллы или перенести сальдо баллов по программе лояльности с одной карточки на другую. | Программы лояльности назначаются карточке постоянного клиента.                                                                                                                                                                                                                                                                                                                                  |

## <a name="loyalty-processes"></a>Процессы лояльности
Следующая таблица описывает процессы, которые необходимо запустить для отправки конфигураций и данных лояльности в ваши магазины, а также для извлечения проводок лояльности из ваших магазинов.

| Наименование процесса                         | Описание                                                                                                                                                                                                                                                                                                                                                                                                    | Имя страницы                            |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| 1050 (сведения по программе лояльности)           | Выполните этот процесс, чтобы отправить данные конфигурации лояльности из Dynamics 365 for Retail в магазины розничной торговли. Рекомендуется запланировать частое выполнение этого процесса, чтобы данные лояльности передавались во все магазины.                                                                                                                                                                                               | График распределения                |
| Обработать схемы программы лояльности              | Выполните этот процесс, чтобы связать схемы лояльности с каналами розничной торговли, которым назначена схема лояльности. Этот процесс можно запланировать для запуска в виде процесса пакетной обработки. Вы должны запустить этот процесс, если вы изменяете данные конфигурации лояльности, такие как схемы лояльности, программы лояльность или баллы вознаграждения по программе лояльности.                                                                                               | Обработать схемы программы лояльности              |
| Обработать автономные проводки лояльности | Выполните эту процедуру, чтобы обновить карточки постоянного клиента, чтобы они включали проводки, обработанные в автономном режиме. Этот процесс применяется только в том случае, если установлен флажок **Заработок в автономном режиме** на странице **Общие параметры розничной торговли**, чтобы баллы вознаграждения можно было зарабатывать в автономном режиме.                                                                                                                                               | Обработать автономные проводки лояльности |
| Обновить классы карточки постоянного клиента            | Выполните этот процесс, чтобы оценить достаточно ли клиент заработал баллов, чтобы остаться на данном уровне программы лояльности, и чтобы обновить статус уровня клиента. Этот процесс необходим, только если правила уровней в программах лояльности были изменены и требуется обновить правила задним числом для применения к карточкам постоянного клиента, которые уже были выданы. Этот процесс можно выполнить как процесс пакетной обработки или для отдельных карт. | Обновить классы карточки постоянного клиента            |





