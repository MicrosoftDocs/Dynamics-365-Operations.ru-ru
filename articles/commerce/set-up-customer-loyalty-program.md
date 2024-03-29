---
title: Обзор лояльности
description: В этой статье описываются возможности программы лояльности в Dynamics 365 Commerce и соответствующие шаги настройки, помогающие предприятиям розничной торговли легко приступить к работе со своими программами лояльности.
author: josaw1
ms.date: 11/16/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.custom: 16201, "intro-internal"
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.form: RetailLoyaltyPrograms, RetailPriceDiscGroup
ms.openlocfilehash: 17742bb5c0091804fc6f43bb2aabb7af73229890
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2022
ms.locfileid: "9784973"
---
# <a name="loyalty-overview"></a>Общие сведения о программе лояльности

[!include [banner](includes/banner.md)]

Программы лояльности могут повысить лояльность постоянного клиента благодаря тому, что клиент получает поощрения за покупки в магазинах розничной торговли данного бренда. В Dynamics 365 Commerce можно настроить простые или сложные программы лояльности, которые применяются ко всем юридическим лицам в любом коммерческом канале. В этой статье описываются возможности программы лояльности в Commerce и соответствующие шаги настройки, помогающие предприятиям розничной торговли легко приступить к работе со своими программами лояльности.

Вы можете настроить вашу программу лояльности, чтобы она включала следующие варианты.

- Настройка нескольких типов поощрений, которые предлагаются в программах лояльности, и отслеживание участия в программах лояльности.
- Настройка программ лояльности, которая представляет различные поощрения, предлагаемые компанией. Можно создать уровни программы лояльности для предложения более значимых поощрений и вознаграждений клиентам, которые совершают покупки чаще или тратят больше денег в магазинах.
- Настройка правил начисления для определения действий, которые должен выполнить клиент, чтобы заработать поощрения. Можно также определить правила списания, чтобы указать, когда и как клиент может списывать поощрения.
- Выпуск карточек постоянного клиента в любом канале, который участвует в программах лояльности, и привязка карточек постоянного клиента к одной или нескольким программам лояльности, в которых может участвовать клиент. Можно также связать запись клиента с карточкой постоянного клиента для предоставления клиенту возможности использовать баллы по программе лояльности на нескольких карточках и списывать их.
- Настройка карточек постоянного клиента вручную или перенос баланса поощрений лояльности с одной карточки на другую, чтобы выполнить требования клиента или поощрить его.

Следующий видеоролик содержит обзор и демонстрацию возможностей программы лояльности в Dynamics 365 Commerce.


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5c2wW]

## <a name="setting-up-loyalty-programs"></a>Настройка программ лояльности

Необходимо настроить несколько компонентов, чтобы включить функцию лояльности в Commerce. На следующей схеме показаны компоненты лояльности и то, как они связаны друг с другом.

![Последовательность операций при настройке лояльности.](./media/loyaltyprocess.gif "Компоненты программы лояльности и их связь друг с другом")

## <a name="loyalty-components"></a>Компоненты лояльности

В следующей таблице приводится описание каждого компонента и указывается, где он используется при настройке лояльности.

| Компонент                                        | описание | Использование |
|--------------------------------------------------|-------------|-----------------|
| Настройка скидок (необходимое условие)                  | Настройка скидок, предлагаемых постоянным клиентам. Например, вы можете предложить скидку 5 процентов на всю повседневную одежду. | Чтобы можно было включить скидки в программу лояльности, их необходимо добавить в ценовые группы. Ценовые группы назначаются программам лояльности и уровням лояльности. |
| Настройка ценовых групп (необходимое условие)               | Ценовые группы используются для создания цен и скидок для продуктов и управления ими. Настройте ценовые группы, включающие скидки, которые применяются к программам лояльности. | Ценовые группы назначаются программам лояльности и уровням программ лояльности. |
| Настройка каналов (необходимое условие)                   | Каналы Commerce — это магазины, участвующие в программах лояльности, такие как физические магазины, интернет-магазины или центры обработки вызовов. Необходимо настроить каналы перед назначением им программ лояльности. | Каналы назначаются программе лояльности, если канал участвует в программе лояльности. |
| Настройка способа оплаты по программе лояльности (необходимое условие) | Чтобы гарантировать, что баллы программы лояльности могут быть погашены в любом канале, например в физических магазинах, в интернет-магазины или центрах обработки звонков, необходимо настроить диапазон ячеек постоянного клиента на странице **Номера карт**. | Настройте способ оплаты типа программы лояльности, а затем назначьте способ оплаты по программе лояльности каналам, участвующим в программе лояльности. |
| Настройка интервалов дат                            | Интервалы дат позволяют гибко настраивать период времени для уровней лояльности. Используйте интервалы дат для того, чтобы определить, сколько времени клиент может оставаться на уровне или сколько времени имеет клиент на то, чтобы выполнить действие, необходимое для квалификации на уровень. | Интервалы дат применяются, только если в программах лояльности используются уровни. Можно выбрать интервал дат, который применяется к уровням программы, а также интервалы дат, которые применяются к правилам уровней программы. |
| Настройка баллов поощрения                             | Баллы поощрения — это типы поощрения, предлагаемые клиентам. Баллы поощрения могут иметь или не иметь возможность списания. Баллы поощрения с возможностью списания можно обменять на продукты. Баллы поощрения без возможности списания используются для отслеживания сведений о клиенте или перевода клиента на следующий уровень программы лояльности. | Баллы поощрения определяются в правилах уровней и используются для перевода клиента на определенный уровень. Баллы поощрения также определяются в схемах лояльности в правилах начисления и списания. В правилах начисления определяются поощрения, которые клиент может получить, выполнив определенные действия. В правилах списания определяются поощрения, которые клиент может списать. |
| Настройка программ лояльности                          | Программы лояльности — это основной объект лояльности, предлагаемый компанией. Каждая программа лояльности может иметь уровни лояльности. Скидки и ценовые группы назначаются программам лояльности на уровне программы или на уровне уровня. | Для программ лояльности можно создать схемы лояльности. Программам лояльности можно назначить карточки постоянного клиента, а карточки постоянного клиента можно назначить клиенту. Каналы участвуют в программах лояльности, назначенных схемам лояльности. Любой клиент, имеющий карточку постоянного клиента, может участвовать в программах лояльности, назначенных карточке. |
| Настройка уровней лояльности и правил уровней              | Уровни лояльности — это дополнительные уровни, которые можно определить для программ лояльности. Можно настроить базовые скидки и поощрения для всех клиентов, участвующих в программе лояльности, а также дополнительные скидки и поощрения для клиентов, которые находятся на разных уровнях программы. Для каждого определяемого уровня лояльности можно настроить правила перевода клиента на данный уровень. Можно также указать период времени, в течение которого клиенты могут оставаться на данном уровне после перехода на него. | Уровни лояльности и правила уровней лояльности определяются в программах лояльности. Если не определить уровни лояльности, все клиенты, участвующие в программе лояльности, имеют право на скидки, назначенные в ценовой группе программы лояльности. Если определить уровни лояльности, можно настроить правила начисления и правила списания для уровней лояльности в схеме лояльности. |
| Настройка схем программы лояльности                           | В схемах лояльности указываются правила начисления и правила списания, которые применяются к выбранной программе лояльности. Каналы назначаются схеме лояльности для указания того, какая программа лояльности, правила начисления и правила списания применяются к магазину. | Схема лояльности назначается программе лояльности и каналам. Можно назначить несколько схем лояльности одной программе лояльности и можно назначить несколько схем лояльности множеству каналов. |
| Настройка карточек постоянного клиента                             | Карточка постоянного клиента дает владельцу карточки право участвовать в программах лояльности, назначенных карточке. Карточки постоянного клиента можно выпускать анонимно, или они могут назначаться определенному клиенту. Можно просмотреть проводки по программе лояльности для определенной карточки, а также просмотреть сводку баллов по программе лояльности, накопленных на карточке. Карточки постоянного клиента можно выпускать в любом канале. Можно также вручную скорректировать карточку постоянного клиента, чтобы перевести клиента на другой уровень, добавить баллы или перенести сальдо баллов по программе лояльности с одной карточки на другую. | Программы лояльности назначаются карточке постоянного клиента. |

## <a name="loyalty-processes"></a>Процессы лояльности

Следующая таблица описывает процессы, которые необходимо запустить для отправки конфигураций и данных лояльности в ваши магазины, а также для извлечения проводок лояльности из ваших магазинов.

| Наименование процесса                         | Описание | Имя страницы |
|--------------------------------------|-------------|-----------|
| 1050 (сведения по программе лояльности)           | Выполните этот процесс, чтобы отправить данные конфигурации лояльности из Commerce в магазины. Рекомендуется запланировать частое выполнение этого процесса, чтобы данные лояльности передавались во все магазины. | График распределения |
| Обработать схемы программы лояльности              | Выполните этот процесс, чтобы связать схемы лояльности с каналами, которым назначена схема лояльности. Этот процесс можно запланировать для запуска в виде процесса пакетной обработки. Вы должны запустить этот процесс, если вы изменяете данные конфигурации лояльности, такие как схемы лояльности, программы лояльность или баллы вознаграждения по программе лояльности. | Обработать схемы программы лояльности |
| Разнести начисленные баллы программы лояльности в пакетах | Выполните эту процедуру, чтобы обновить карточки постоянного клиента, чтобы они включали проводки, обработанные в автономном режиме. Этот процесс применяется только в том случае, если установлен флажок **Разнести начисленные баллы в пакетах** на странице **Общие параметры Commerce**, чтобы баллы вознаграждения можно было зарабатывать в автономном режиме. | Разнести начисленные баллы программы лояльности в пакетах |
| Обновить классы карточки постоянного клиента            | Выполните этот процесс, чтобы оценить достаточно ли клиент заработал баллов, чтобы остаться на данном уровне программы лояльности, и чтобы обновить статус уровня клиента. Этот процесс необходим, только если правила уровней в программах лояльности были изменены и требуется обновить правила задним числом для применения к карточкам постоянного клиента, которые уже были выданы. Этот процесс можно выполнить как процесс пакетной обработки или для отдельных карт. | Обновить классы карточки постоянного клиента |

## <a name="loyalty-capabilities"></a>Возможности программы лояльности

- Используя ценовые группы, связанные с программой лояльности и уровнями лояльности, розничные магазины могут легко создавать специальные цены и скидки для участников программы лояльности.

- В рамках схемы программы лояльности предприятия розничной торговли могут создать различные правила начисления и погашения с уровнями, чтобы отличать вознаграждения для клиентов на различных уровнях. Предприятия розничной торговли также могут включить "принадлежности" как часть правил начисления и погашения, чтобы определенные группы клиентов может быть частью существующих уровней, но получать вознаграждение по-разному. Это исключает необходимость создавать дополнительные уровни.
    
    > [!NOTE]
    > Правила начисления в рамках схемы программы лояльности являются дополнительными. Например если вы создаете правило, согласно которому члену золотого уровня начисляются 10 баллов для каждого доллара США, можно также создать правило для клиента с назначением «ветеран», чтобы начислять 5 баллов за каждый доллар США; тогда ветеран, который также является членом золотого уровня, будет накапливать 15 баллов за каждый 1 доллар США, так как он входит в обе строки. Тем не менее, если клиент-ветеран не является членом золотого уровня, клиент будет накапливать 5 баллов за каждый доллар. Чтобы отразить изменения в каналах, запустите задания **Обработать схемы программы лояльности** и **1050** (сведения о программе лояльности).
    
    ![Начисления на основе принадлежности.](./media/Affiliation-based-earning.png "Начисления на основе принадлежности")

- Предприятия розничной торговли часто имеют специальные цены для группы клиентов, которые не хотят входить в программы лояльности. Например, оптовых клиенты или сотрудники, которые получают специальные цены, но не получают баллы по программе лояльности. Часто «принадлежности» используются для предоставления специальных цен для таких групп клиентов. Чтобы запретить определенным группам клиентов получать баллы по программе лояльности, предприятие розничной торговли может указать одну или несколько принадлежностей в разделе **Исключенные назначения** схемы программы лояльности. Таким образом, когда клиенты, входящие в исключенные группы принадлежности, являются действующими членами программы лояльности клиентов, они не смогут накапливать баллы по программе лояльности за свои покупки. Чтобы отразить изменения в каналах, запустите задания **Обработать схемы программы лояльности** и **1050** (сведения о программе лояльности).

    ![Исключенные назначения.](./media/Excluded-affiliations.png "Запрет группам принадлежности получать баллы по программе лояльности")
    
- POS-терминал гибко позволяет предприятиям розничной торговли использовать физические карты постоянного клиента или автоматически создавать уникальный номер карточки постоянного клиента. Чтобы включить автоматическое создание карточек постоянного клиента в магазинах, включите параметр **Создать номер карты лояльности** в профиле функциональности, связанном с магазином. Для каналов продаж через Интернет предприятия розничной торговли могут использовать API IssueLoyaltyCard для выпуска карточек программы лояльности для клиентов. Предприятия розничной торговли могут предоставить данному API номер, который будет использоваться для создания карты постоянного клиента, или система будет использовать номерную серию карт постоянного клиента, заданную в Commerce. Тем не менее, если номерная серия не существует и при вызове API предприятие розничной торговли не указало номер карточки постоянного клиента, выводится сообщение об ошибке.

    ![Создать карту лояльности.](./media/Generate-loyalty-card.png "Автоматическое создание номера карточки постоянного клиента")

- Начисленные и погашенные баллы по программе лояльности, теперь могут сохраняться для каждой проводки и заказов на продажу для строки продажи, чтобы та же сумма могла быть возвращена или аннулирована в случае полного или частичного возврата. Более того, наличие видимости для баллов на уровне строки продажи обеспечивает возможность для пользователей центра обработки вызовов отвечать на вопросы клиентов о том, сколько баллов было начислено или погашено для каждой строки. До этого изменения начисленные баллы всегда пересчитывались при возврате, что приводило к сумме, отличной от исходной, если правила начисления или погашение были изменены; кроме того, пользователи центра обработки вызовов не видели разбивку баллов. Баллы могут просматриваться в форме **Проводки по карте** для каждой карты постоянного клиента. Чтобы включить эту функцию, включите конфигурацию **Разнести баллы программы лояльности по строке продажи** на вкладке **Общие параметры Commerce** \> **Общие**.

    > [!NOTE]
    > Настоятельно рекомендуется включение этой функции, чтобы обеспечить, что в случае возврата правильное количество баллов будет возвращено клиенту или изъято у него.

- Предприятия розничной торговли теперь могут определять период ввода в действие для каждого начисленного балла. Конфигурации периода ввода в действие определяет время с даты начисления, после которого начисленные баллы становятся доступными для клиентов. Неначисленные баллы можно просмотреть в столбце **Неначисленные баллы** на странице **Карты лояльности**. Когда клиенты возвращают некоторые номенклатуры, для которых были получены баллы по программе лояльности, по умолчанию система вычитает неначисленные баллы, а затем вычитает все сальдо из доступных баллов. Однако можно настроить, чтобы вычитать доступные баллы только вместо вычитания из неначисленных баллов.

Кроме того, предприятия розничной торговли могут определить максимальное количество начисляемых баллов для каждой карты постоянного клиента. Это поле может использоваться для уменьшения воздействия мошенничества с программами лояльности. При достижении максимального количества начисленных баллов пользователь на может получить дополнительные баллы. Предприятия розничной торговли могут решить блокировать такие карты, пока они проверили на наличие потенциального мошенничества. Если предприятие розничной торговли определяет мошенничество, он может блокировать карточку постоянного клиента и пометить клиента как заблокированного. Чтобы это сделать, задайте для свойства **Заблокировать регистрацию в программе лояльности для клиента** значение **Да** в разделе **Все клиенты** на экспресс-вкладке **Commerce**. Заблокированные клиенты не смогут получить карточку постоянного клиента ни по одному из каналов.

   ![Начисление и максимальное количество баллов.](./media/Vesting-and-maximum-reward-points.png "Определение начисления и максимального количества баллов")

- Назначения используются для предоставления специальных цен и скидок, но также существуют некоторые назначения, которые предприятия розничной торговли не хотят показывать клиентам. Например, назначение под названием "Клиент с большим объемом покупок" может быть плохо воспринято некоторыми клиентами. Кроме того, существуют некоторые назначения, которые не должны управляться в магазине, например, сотрудники, так как вы не хотите, чтобы кассиры могли решать, кто является сотрудником, и таким образом обеспечивать скидки как для сотрудников. Предприятия розничной торговли теперь могут выбрать назначения, которые должны быть скрыты в каналах. Назначения, помеченные как **Скрыть в каналах**, нельзя просматривать, добавлять или удалять в POS. Тем не менее цены и скидки, связанные с этими назначениями, будут применяться к продуктам.

    ![Скрыть назначения.](./media/Hide-affiliations.png "Скрыть назначения в каналах")
    
- Пользователям центра обработки вызовов теперь легче искать клиентов с помощью информации о карте постоянного клиента и переходить на страницы карты постоянного клиента или проводки по карте постоянного клиента со страницы **Обслуживание клиентов**.

    ![Обслуживание клиентов.](./media/Customer-service.png "Поиск сведений по программе лояльности для клиента")
    
- Если безопасность карты постоянного клиента была нарушена, необходимо создать новую карты на замену и перенести существующие баллы на новую карту. Процесс замены карты в данном выпуске упрощен. Кроме того, клиенты могут дарить часть или все свои баллы по программе лояльности друзьям и членам семьи. При перемещении баллов для каждой карты постоянного клиента создаются записи корректировки баллов. Функция замены карт и переноса сальдо доступны со страницы **Карты лояльности**.

    ![Замена и перенос баллов.](./media/Replace-and-transfer-points.png "Замена карты локальности или перенос сальдо")
    
- Предприятиям розничной торговли может потребоваться оценить эффективность определенного канала для регистрации клиентов в программе лояльности. Источник подачи заявок для карт постоянного клиента теперь сохраняется, чтобы предприятия розничной торговли могли выполнять отчеты для этих данных. Источник регистрации автоматически регистрируется для всех выпущенных карт постоянного клиента из каналов MPOS/CPOS или электронной коммерции. Для карт постоянного клиента, выданных из приложения бэк-офиса, пользователь центра обработки вызовов может выбрать соответствующий канал.
- В предыдущих выпусках предприятия розничной торговли могли использовать MPOS/CPOS для погашения баллов по программе лояльности для клиентов в магазине. Тем не менее в этих выпусках, потому что сальдо по программе лояльности отображается в баллах по программе лояльности, кассир не может видеть сумму в валюте, которая может быть применена к текущей проводке. Кассир должен был сделать преобразование баллов в валюту перед оплатой баллами по программе лояльности. В текущем выпуске после добавления строк в проводку кассир может просмотреть сумму, которую можно оплатить баллами по программе лояльности для текущей проводки, что упрощает применение некоторых или всех баллов по программе лояльности к проводке. Кроме того, кассир может увидеть все баллы, срок действия которых истекает за следующие 30 дней, поэтому они могут предложить более дорогой продукт или перекрестные продажи, чтобы мотивировать клиента потратить баллы с истекающим сроком действия в этой транзакции.

    ![Баллы, покрываемые сальдо по программе лояльности.](./media/Points-covered-by-loyalty-balance.png "Показать баланс, покрываемый баллами по программе лояльности")

    ![Баллы с истекающим сроком действия.](./media/Expiring-points.png "Просмотр баллов с истекающим сроком действия")

- В выпуске 8.1.3 включен параметр "Оплата по карте лояльности" в канале центра обработки вызовов. Чтобы включить этот параметр, создайте тип платежного средства "карта лояльности" и свяжите его с центром обработки вызовов. 

    > [!NOTE]
    > Поскольку платежей картой постоянного клиента настраиваются как платежи картой, необходимо выбрать карту на странице **Настройка карты**. 

    ![Настройка карточки постоянного клиента.](./media/LoyaltyCardSetup.png "Настройка карточки постоянного клиента")

    После этой настройки клиенты могут использовать свои баллы по программе лояльности в центре обработки вызовов. Кроме того, мы дополнительно улучшаем работу пользователей, чтобы показывая значение "Сумма, покрываемая баллами лояльности", чтобы пользователям центра обработки вызовов не приходилось переходить на другой экран для просмотра сальдо по программе лояльности.

- Многие предприятия розничной торговли начисляют баллы по программе лояльности только на основе проводок продаж, но некоторые более ориентированные на клиента предприятия розничной торговли хотят иметь возможность поощрять клиентов за любые действия, связанные с их брендом. Например, они хотят предоставлять начисления баллов за прохождение интернет-опроса, посещение магазина, лайки для предприятий розничной торговли в Facebook, написание отзывов о предприятии розничной торговли в Twitter и т. д. Чтобы это сделать, предприятие розничной торговли может определить любое количество "Других типов мероприятий" и определить соответствующие правила начисления баллов для этих действий. Существует также предоставляемый API-интерфейс Commerce Scale Unit "PostNonTransactionalActivityLoyaltyPoints", который может быть вызван, когда действие определено, которое должно начислять баллы по программе лояльности клиенту. Этот API-интерфейс ожидает код карточки постоянного клиента, код канала и другие идентификаторы типов деятельности, чтобы клиента, которому должно быть начислено вознаграждение, можно было найти и можно было определить правило начисления для мероприятия. 

    Баллы вознаграждении для мероприятий без проводок обычно имеют два основных действия:

    - Обнаружение реализации действия, которое должно быть вознаграждено.
    - Начисление соответствующих баллов.

    Первый шаг является внешним по отношению к Commerce, например написание отзыва о товарном знаке в Twitter или нажатие кнопки "Мне нравится" в Facebook. После распознавания этого действия предприятия розничной торговли могут вызвать вышеупомянутый API-интерфейс Commerce Scale Unit и начислить баллы вознаграждения в режиме реального времени. В подобных случаях нет необходимости для этапа проверки, так как действие произошло и соответствующие баллы должны быть начислены. Однако существуют сценарии, в которых предприятию розничной торговли может понадобиться проверить записи перед начислением баллов вознаграждения. Например, предприятие розничной торговли настроило семинар в магазине, на который клиенты подписываются на веб-сайте электронной коммерции или в любом другом приложении регистрации на событие. Тем не менее, только клиенты, посетившие мероприятие, должны получить баллы по программе лояльности. Для таких сценариев в версии 10.0 мы представили информационный объект с именем **Строки действий другого типа для программы лояльности предприятия розничной торговли**. Этот информационный объект позволяет предприятиям розничной торговли использовать платформу импорта и экспорта данных (DIXF) или API-интерфейс OData для регистрации действий, за которые клиенты должны получать баллы лояльности. Информационный объект сохраняет мероприятия в журнале с именем **Строки программы лояльности для других действий**, который может использоваться для просмотра и изменения. После проверки данных ИТ-пользователь может затем вручную выполнить разноску строк мероприятия или выполнить задание с именем **Обработка мероприятий другого типа для строк программы лояльности**, которое выполнит разноску всех неразнесенных строк мероприятий и произведет начисление баллов клиентам на основе правил начисления. В приведенном выше примере приложение регистрации событий могло бы вызвать API-интерфейс OData, чтобы отправить сведения о клиентах в Commerce. Тем не менее, ИТ-пользователь может выполнить разноску строк мероприятия только для пользователей, которые посетили семинар и удалить строки мероприятия для других клиентов. 

    > [!NOTE]
    > В настоящее время система принудительно требует от пользователей настроить номерную серию для "других типов мероприятия", но это не будет обязательным шагом в будущих выпусках. Чтобы настроить номерную серию, откройте **Общие параметры Commerce** \> **Номерные серии** и выберите номерную серию для **Идентификатор типа других мероприятий лояльности**.

- Для обеспечения качественного обслуживания клиентов и эффективного разрешения запросов клиентов, важно, чтобы кассиры имели доступ к полному профилю клиента. В выпуске 10.0 кассиры будут видеть сведения истории постоянного клиента вместе с информацией о связанной программе постоянного клиента и уровне на POS-терминале.
- Бесплатные покупки или покупки со скидкой — один из факторов высокой мотивации клиентов для покупок через Интернет. Чтобы позволить предприятиям розничной торговли настроить рекламные акции, в выпуске 10.0 введен новый тип рекламной акции с названием "Скидка по порогу отгрузки", в которой предприятие розничной торговли может определить пороговые значения, при выполнении которых клиентам будет доступна покупка со скидками или бесплатная доставка. Например, потратьте 35 долларов США для бесплатной "доставки в течение двух дней" или бесплатная "доставка в течение двух дней" для всех постоянных клиентов. Эта функция использует новую возможность расширенных автоматических накладных расходов. См. [документацию по расширенным автоматическим накладным расходам](/dynamics365/unified-operations/retail/omni-auto-charges). Эти расширенные автоматические накладные расходы должны быть включены, чтобы работали рекламные акции по доставке. Их можно включить на вкладке **Заказы клиентов** на странице **Параметры Commerce** и включены в конфигурации "Использовать расширенный автоматические затраты". Кроме того, поскольку предприятие розничной торговли может настроить несколько типов расходов, таких как обработка и установка, предприятие розничной торговли должно указать, какие расходы считается расходами на доставку. Скидки на доставку применяются только к расходам на доставку. Чтобы указать накладные расходы как расходы на доставку, перейдите к форме **Коды сборов** в пункте **Retail и Commerce** \> **ИТ Retail и Commerce** \> **Настройка канала** \> **Накладные расходы** и включите флажок "Расходы на доставку" для нужных расходов. Теперь можно перейти к форме **Скидка по порогу отгрузки** и настроить скидку.

    Как и скидка на продукты, эта скидка учитывает все существующие стандартные возможности скидок, например, позволяя предприятию розничной торговли ограничить эти скидки с помощью купонов, чтобы только клиенты с купонами могли получить эти скидки. Кроме того, эти скидки используют возможности ценовых групп для определения доступности таких скидок. Например, предприятие розничной торговли может проводить эти рекламные акции только в интернет-каналах и/или в нескольких каналах для определенных групп клиентов, таких как постоянные клиенты. После того как строки заказа с указанным способом доставки будут отвечать определенному пороговому значению, применяется скидка на доставку и уменьшаются расходы на доставку на основе настроенной скидки. 

    > [!NOTE]
    > В отличие от других периодических скидок, таких как количество, простая скидка, скидка на комплект и пороговые скидки, скидка на доставку не создает строки скидок, она изменяет расходы на доставку напрямую и добавляет название скидки к описанию накладных расходов.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
