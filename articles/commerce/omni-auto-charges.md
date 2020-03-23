---
title: Омниканальные расширенные автоматические накладные расходы
description: В этом разделе описываются возможности для управления дополнительными расходами заказа по заказам канала Commerce с помощью функций расширенных автоматических накладных расходов.
author: hhaines
manager: annbe
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10
ms.openlocfilehash: fd02a81f35b40e5075ccfe5c9a617d7de4e8250d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023870"
---
# <a name="omni-channel-advanced-auto-charges"></a>Омниканальные расширенные автоматические накладные расходы

[!include [banner](includes/banner.md)]

В этом разделе приводятся сведения о конфигурации и развертывания функции расширенных автоматических накладных расходов, которая доступна в Dynamics 365 for Retail версии 10.0.

При включении функции расширенных автоматических накладных расходов заказы, созданные в любом поддерживаемом канале Commerce (POS, центр обработки вызовов и интернет-магазин), могут использовать конфигурации [автоматических расходов](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services), определенные в приложении электронной отчетности для накладных расходов уровня заголовка и уровня строк.

В версиях до Retail версии 10.0 конфигурации [автоматического расхода](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) доступны только заказам, созданным в каналах электронной коммерции и центра обработки вызовов. В версии 10.0 или более поздних заказы, созданные в POS, могут использовать конфигурации автоматических накладных расходов. Таким образом, дополнительные накладные расходы могут быть систематически добавлены в проводки по продажам.

При использовании версий, предшествующих версии 10.0, пользователю POS предлагается вручную ввести стоимость доставки при создании в POS проводок "Отгрузить все" или "Отгрузить выбранное". В то время как возможности дополнительных накладных расходов в приложении используются в отношении того, как накладные расходы записываются в заказ, систематическое вычисление не предоставляется — расчет основывается на введенных пользователем данных, чтобы определить сумму расходов. Накладные расходы могут быть добавлены только в качестве одного кода накладных расходов, связанных с "отгрузкой", и их невозможно легко изменить в POS после их создания.

Использование ручных подсказок, чтобы добавить накладные расходы на отгрузку, по-прежнему доступны в версии 10.0 и более поздних версиях. Если организация не включает параметр **Расширенные автоматические затраты**, приглашения POS с запросом ручного ввода накладных расходов не изменяется.

С функцией расширенных автоматических накладных расходов пользователи POS могут иметь систематические расчеты для любых определенных накладных расходов на основе таблиц настройки автоматических начислений. Кроме того, пользователи будут иметь возможность добавить или изменить неограниченное количество дополнительных расходов и сборов в проводке продаж через POS на уровне заголовка или уровне строки (для продаж типа "оплатил и забрал" или для заказа клиента).

## <a name="enabling-advanced-auto-charges"></a>Включение расширенных автоматических затрат

На странице **Retail и Commerce \> Настройка центрального офиса \> Параметры \> Параметры Commerce** откройте вкладку **Заказы клиентов**. На экспресс-вкладке **Расходы** задайте для параметра **Использовать расширенные автоматические затраты** значение **Да**.

![Параметр расширенных автоматических затрат](media/advancedchargesparameter.png)

При включении расширенных автоматических затрат пользователям больше не предлагается ввести накладные расходы на доставку в POS-терминал вручную при создании заказа клиента с доставкой всех или выбранных позиций. Накладные расходы по заказу POS систематически рассчитываются и добавляется к проводке POS (в случае обнаружения соответствующей таблицы автоматических затрат, которая совпадает с критерием создаваемого заказа). Пользователи могут также добавлять или вести расходы уровня заголовка или строки вручную с помощью только что добавленных операций POS, которые могут быть добавлены в макет экрана POS.

Когда расширенные автоматические затраты включены, существующие **Параметры Commerce** для настроек **Код расходов на поставку** и **Возмещение расходов на поставку** больше не используются. Эти параметры применяются только в случае, если для параметра **Использовать расширенные автоматические затраты** установлено значение **Нет**.

Прежде чем включить эту функцию, убедитесь в наличии проверенных и обученных сотрудников, так как это приведет к изменению потока бизнес-процессов расчета расходов на доставку и других расходов и их добавления их к заказам на продажу в POS. Убедитесь, что вы понимаете влияние этой последовательности операций на создания проводок из POS. Для заказов через центр обработки вызовов и электронную коммерцию влияние включения расширенных автоматических затрат минимально. Приложения центра обработки вызовов и электронной коммерции будут иметь то же поведение, которое они имели ранее в связи с таблицами автоматических затрат для расчета дополнительных сборов за заказ. Пользователи канала центра вызовов будут по-прежнему иметь возможность вручную изменить любых автоматически рассчитанные системой затраты на уровне заголовка или строки или вручную добавлять различные накладные расходы на уровне заголовка или строки.

## <a name="additional-pos-operations"></a>Дополнительные операции POS

Для правильной работы расширенных автоматических затрат в среде приложения POS были добавлены новые операции POS. Эти операции должны быть добавлены в ваши [макеты экрана POS](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) и развернуты на устройствах POS при развертывании расширенных автоматических накладных расходов. Если эти операции не добавляются, пользователи не смогут управлять или вести накладные расходы в проводках POS и не будут иметь никакого способа настройки или изменения значений накладных расходов, которые систематически рассчитаны на основе конфигураций автоматических начислений. Как минимум, рекомендуется развертывать операцию **Управление накладными расходами** в макет POS.

Это следующие новые операции.

- **142 — Управление накладными расходами** — эту операцию можно использовать, чтобы разрешить пользователям POS просматривать и редактировать накладные расходы для проводок POS, которые были добавлены вручную или систематически с помощью вычисления автоматических начислений.
- **141 — Добавить накладные расходы в заголовке** — эту операцию можно использовать для предоставления пользователю возможности вручную добавлять накладные расходы уровня заголовка в любую проводку по продаже через POS-терминал (и выбрать код накладных расходов для использования).
- **140 — Добавить накладные расходы по строке** — эту операцию можно использовать для предоставления пользователю возможности вручную добавлять накладные расходы уровня строки в любую строку проводки по продаже через POS-терминал (и выбрать код накладных расходов для использования).
- **143 — Пересчитать накладные расходы** — эту операцию можно использовать для выполнения полного повторного вычисления накладных расходов для проводки продажи. Любые ранее перезаписанные пользователем автоматические расходы будут пересчитаны на основе текущей конфигурации корзины для покупок.

Как и со всеми операциями POS, можно сделать конфигурации безопасности, чтобы требовать утверждения менеджера для выполнения операции.

Важно отметить, что перечисленные выше операции POS можно также добавить в макет POS, даже если параметр **Использовать расширенные автоматические затраты** отключен. В этом случае организации будут по-прежнему получать дополнительные преимущества за счет возможности просмотра вручную добавленных расходов и редактирования их с помощью операции **Управление накладными расходами**. Пользователи могут также использовать операции **Добавить расходы в заголовке** и **Добавить расходы по строке** для проводок POS, даже если параметр **Использовать расширенные автоматические затраты** отключен. Операция **Пересчитать накладные расходы** имеет более ограниченную функциональность, если используется, когда параметр **Использовать расширенные автоматические затраты** отключен. В этой случае ничего не будет пересчитано, и любые расходы, вручную добавленные в проводку, будут просто сброшены на $0,00.

## <a name="use-case-examples"></a>Примеры использования

В этом разделе представлены примеры использования, которые помогают понять особенности настройки и использования автоматических затрат и накладных расходов в контексте заказов канала. Эти примеры иллюстрируют поведение приложения, когда был включен параметр **Использовать расширенные автоматические затраты**.

### <a name="auto-charges-header-charges-example"></a>Пример автоматического начисления затрат на уровне заголовка

#### <a name="use-case-scenario"></a>Сценарий использования

Предприятие розничной торговли хочет автоматически добавлять расходы на фрахт при создании проводок в любом канале Commerce, который требует отгрузки продуктов клиенту. Предприятие розничной торговли предлагает 2 способа поставки: наземным транспортом и воздушным транспортом. Если клиент выбирает доставку наземным транспортом и сумма заказа меньше 100 долларов США, предприятие розничной торговли хочет начислять клиенту расходы на фрахт в размере 10,00 долларов США. Если сумма заказа превышает 100 долларов США и клиент выбирает доставку наземным транспортом, клиенту не будут начисляться никакие дополнительные сборы за фрахт. Если клиент выбирает метод поставки воздушным транспортом для всех заказов, независимо от их общей суммы, будет начислять плата за фрахт в размере 20,00 долларов США.

#### <a name="setup-and-configuration"></a>Настройка и конфигурация

Этот сценарий требует настройки двух таблиц автоматических начислений.

Перейдите в раздел **Расчеты с клиентами \> Настройка накладных расходов \> Автоматические затраты**.

Настройте два различных автоматических начисления уровня заголовка. Настройте один для режима доставки "Наземным транспортом", и второй для доставки "Воздушным транспортом". В этом сценарии настройте их для использования для "Все клиенты".

За расходов на доставку наземным транспортом, в разделе строк страницы **Автоматические затраты** определите расходы, которые будут применяться для заказов с суммой от 0,01 до 100 долларов США, как 10,00 долларов США. Создайте новую строку расходов, чтобы указать, что для заказов с суммой более 100,01 долларов США накладные расходы не начисляются.

![Пример автоматического расчета накладных расходов](media/headerchargesexample.png)

За расходов на доставку воздушным транспортом, в разделе строк формы автоматических затрат определите расходы в 20,00 долларов США, которые будут применяться ко всем заказам (с суммой от 0,01 до 9 999 999 долларов США).

Отправьте изменения в базу данных Commerce Scale Unit/Channel DB, чтобы POS могли использовать их, запустив задание **график распределения 1040**.

#### <a name="sales-processing-for-this-scenario"></a>Обработка продаж в этом сценарии

После выполнения описанных выше шагов настройки и применения этих изменений к базе данных канала любые заказы клиентов или проводки продажи, созданные на POS, в центре обработке вызовов или по каналам электронной коммерции, в которых способ доставки наземным транспортом или воздушным транспортом задан на уровне заголовка, будут использовать эти расходы и автоматически применять их к продаже.

В этот момент накладные расходы будут применяться ко всем проводкам продаж, созданным в рамках юридического лица, которое использует эти режимы доставки, так как нет возможности указать, что конфигурация автоматического начисления накладных расходов будет применяться только к конкретному каналу продаж.

Для сценариев POS и электронной коммерции, поскольку эти заказы не имеют четко определенного "заголовка", расходы на уровне заголовка применяется только в том случае, если все строки продажи в проводке заданы для точно одинакового способа поставки. Если имеются "смешанные режимы" выполнения проводок, созданных в POS или канале электронной коммерции, только автоматические расходы уровня строк будут учитываться и применяться.

В случаев центра обработки звонков у пользователя есть контроль над заданием режима доставки в заголовке заказа, поэтому расходы на уровне заголовка будут применяться для этих заказов, даже если некоторые из строк продаж были настроены для использования другого режима доставки. Расходы уровня заголовка расходов по заказам центра обработки вызовов всегда основаны на способе доставки, который определен на уровне заголовка заказа на продажу.

### <a name="auto-charges-line-charges-example"></a>Пример автоматического начисления затрат на уровне строк

#### <a name="use-case-scenario"></a>Сценарий использования 

Предприятие розничной торговли хочет добавить дополнительную плату клиенту для сборов за настройку, когда клиент приобретает конкретную модель компьютера. Этот компьютер требует дополнительных обязательных действий по настройке, которую розничный продавец будет выполнять для клиента. Предприятие розничной торговли проинформировало клиентов, что будет дополнительная плата за эту настройку. Предприятие розничной торговли предпочитает управлять расходами, связанными с этой платой, отдельно от цены продажи продукта для целей финансовой отчетности. Плата за настройку в 19,99 долларов США будет начисляться клиенту при приобретении конкретного компьютера в любом канале.

#### <a name="setup-and-configuration"></a>Настройка и конфигурация

Этот сценарий требует настройки одной таблицы автоматических начислений на уровне строки.

Перейдите в раздел **Расчеты с клиентами \> Настройка накладных расходов \> Автоматические затраты**.

Задайте в раскрывающемся меню **Уровень** значение **Строка**и создайте новую запись автоматических затрат для всех клиентов и для конкретного продукта или группы продуктов, для которых будет начисляться плата за настройку.

![Пример автоматического расчета накладных расходов](media/linechargesexample.png)

Отправьте изменения в базу данных Commerce Scale Unit/Channel DB, чтобы POS могли использовать их, запустив задание **график распределения 1040**.

#### <a name="sales-processing-for-this-scenario"></a>Обработка продаж в этом сценарии

После выполнения описанных выше шагов конфигурации и применения этих изменений к базе данных канала любые заказы клиентов или проводки продажи, созданные на POS, в центре обработке вызовов или по каналам электронной коммерции, в заказе которых имеется эта номенклатура, будут запускать систематическое добавление расходов уровня строки в итоговую сумму заказа.

В этот момент накладные расходы будут применяться к любой строке продажи, которая соответствует конфигурации автоматического начисления накладных расходов на уровне строки в рамках юридического лица, так как нет возможности указать, что конфигурация автоматического начисления накладных расходов на уровне строки будет применяться только к конкретному каналу.

### <a name="manual-header-charges-example"></a>Пример ручного ввода накладных расходов уровня заголовка

#### <a name="use-case-scenario-description"></a>Описание сценария использования

Предприятие розничной торговли делает исключение из типовых процессов, предлагая специальную доставку на дом продуктов, которые клиенты заказывают в магазине. Предприятие розничной торговли и клиент договорились, что клиент оплачивает дополнительно 25 долларов США за эту услугу. Принимающий заказы должен добавить эту дополнительную плату в проводку. Поскольку этот сбор является общим сбором, который не связан с каким-либо отдельным продуктом по заказу, будут использоваться расходы заголовка.

#### <a name="setup-and-configuration"></a>Настройка и конфигурация

Убедитесь, что правильно настроен код накладных расходов, который будет использоваться в этом сценарии, для чего откройте **Расчеты с клиентами \> Настройка накладных расходов \> Накладные расходы** для определения кода расходов, соответствующих сценарию.

![Пример накладных расходов](media/chargesexample.png)

Если накладные расходы должны учитываться как накладные расходы, связанные с "доставкой" для целей скидок или рекламы, связанных с доставкой, задайте для параметра **Расходы на поставку** для кода накладных расходов значение **Да**. Если для этих накладных расходов также разрешено систематическое возмещение во время обработки проводки возврата в приложении POS, задайте для параметра **Возмещаемый** значение **Да**. Флаг **Возмещаемый** применяется только тогда, когда для параметра **Использовать расширенные автоматические затраты** установлено значение **Да**.

Отправьте изменения в базу данных Commerce Scale Unit/Channel DB, чтобы POS могли использовать их, запустив задание **график распределения 1040**.

Операция **Добавить накладные расходы в заголовке** должна быть настроена в вашем [макете экрана POS](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts), чтобы кнопка, доступная пользователю на POS, могла вызывать эту операцию (операция 141). Изменения макета экрана необходимо распределить по каналу, а также через функцию графика распределения.

#### <a name="sales-processing-of-manual-header-charges"></a>Обработка продаж для заданных вручную накладных расходов уровня заголовка

Для выполнения сценария в приложении POS пользователь POS создаст транзакции продажи как обычно, добавляя к продаже продукты и любые прочие конфигурации. Перед сбором платежей пользователь должен выполнить операцию **Добавить накладные расходы в заголовке**, которая будет предлагать пользователю выбрать код накладных расходов и ввести значение накладных расходов. После того как пользователь завершит этот процесс, накладные расходы будут добавлены к заказу на продажу как расходы уровня заголовка.

Этот процесс может применяться в центре обработки вызовов, используя существующую функцию **Накладные расходы**, имеющиеся на вкладке **Продажа** на панели инструментов. На странице **Ведение накладных расходов** пользователь может добавить новую строку накладных расходов в заголовок заказа.

### <a name="manual-line-charges-example"></a>Пример вводимых вручную накладных расходов уровня строки

#### <a name="use-case-scenario"></a>Сценарий использования

Клиент запросил, чтобы 2 из 5 номенклатур были завернуты в подарочную упаковку. Предприятие розничной торговли предлагает эту дополнительную услугу по цене 2,00 доллара США за штуку. Принимающий заказ сотрудник должен добавить эти сборы к определенным номенклатурам, которые должны быть завернуты в подарочную упаковку.

#### <a name="setup-and-configuration"></a>Настройка и конфигурация

Убедитесь, что правильно настроен код накладных расходов, который будет использоваться в этом сценарии, для чего откройте **Расчеты с клиентами \> Настройка накладных расходов \> Накладные расходы** для определения кода расходов, соответствующих сценарию.

Если накладные расходы должны учитываться как накладные расходы, связанные с "доставкой" для целей скидок или рекламы, связанных с доставкой, задайте для параметра **Расходы на поставку** для кода накладных расходов значение **Да**. Если для этих накладных расходов также разрешено систематическое возмещение во время обработки проводки возврата в приложении POS, задайте для параметра **Возмещаемый** значение **Да**. Флаг **Возмещаемый** применяется только тогда, когда для параметра **Использовать расширенные автоматические затраты** установлено значение **Да**.

Отправьте изменения в базу данных Commerce Scale Unit/Channel DB, чтобы POS могли использовать их, запустив задание **график распределения 1040**.

Операция **Добавить накладные расходы по строке** должна быть настроена в вашем [макете экрана POS](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts), чтобы кнопка, доступная пользователю на POS, могла вызывать эту операцию (операция 140). Изменения макета экрана необходимо распределить по каналу, а также через функцию графика распределения.

#### <a name="sales-processing-of-the-manual-line-charge"></a>Обработка продаж для заданных вручную накладных расходов уровня строки

Для выполнения сценария в приложении POS пользователь POS создаст транзакции продажи как обычно, добавляя к продаже продукты и любые прочие конфигурации. Перед тем как начать сбор оплаты, пользователь должен выбрать конкретную строку, в которой накладные расходы будут применяться, на экране списка номенклатур POS, затем выполнить операцию **Добавить накладные расходы по строке**. Пользователю будет предложено выбрать код накладных расходов и ввести значение накладных расходов. После того как пользователь завершит этот процесс, накладные расходы будут связаны со строкой и добавлены в общую сумму по заказу как расходы уровня строки. Пользователь может повторить процесс, чтобы добавить дополнительные накладные расходы строки к другим строкам номенклатуры по проводке, если это необходимо.

Такой же процесс может применяться в центре обработки вызовов с помощью функции "Ведение накладных расходов", которая находится в раскрывающемся меню **Финансы** в разделе **Строки заказа на продажу** на странице **Заказ на продажу**. При этом откроется страница **Ведение накладных расходов**, где пользователь может добавить в проводку новые накладных расходы для конкретной строки.

## <a name="additional-features"></a>Дополнительные функции

### <a name="editing-charges-on-a-pos-sales-transaction"></a>Изменение накладных расходов в проводке по продажам POS

Операция **Управление накладными расходами** (142) должна быть добавлена в [макет экрана POS](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts), чтобы пользователь мог просматривать и редактировать или переопределять любые рассчитанные системой или созданные вручную накладные расходы на уровне заголовка или строки. Если операция не добавлена, пользователи не смогут корректировать сумму накладных расходов по проводке POS, а также не смогут просматривать информацию о накладных расходы, такую как тип кода накладных расходов, привязанного с этими накладными расходами.

На странице **Управление накладными расходами** в POS пользователь может просмотреть сведения о накладных расходах как уровня заголовка, так и уровня строки. Пользователь может использовать функцию **Изменить**, доступную на этой странице, чтобы внести изменения в сумму, которая начислена на конкретную строку накладных расходов. После того как строка накладных расходов была перезаписана вручную, она не будет пересчитываться систематически, пока пользователь не запустит операцию **Пересчитать накладные расходы**.

Если **Код основания переопределения цены** был настроен на странице настройки **Параметры Commerce**, пользователю будет предложено указать код причины, когда накладные расходы были изменены в POS-приложении.

Если коды причины были записаны для переопределения накладных расходов, новый отчет также доступен для просмотра и аудита этих случаев переопределения. Отчет можно найти по пути **Retail и Commerce \> Запросы и отчеты \> Журнал переопределения расходов**.

### <a name="refunding-charges-on-a-pos-return-transaction"></a>Возмещение накладных расходов по проводке возврата на POS-терминале

Если для параметра **Использовать расширенные автоматические затраты** установлено значение **Да**, существующий параметр Commerce **Возмещение расходов на поставку** больше не применяется. Чтобы указать, какие накладные расходы следует систематически возмещать клиенту при использовании расширенного автоматического начисления накладных расходов, убедитесь, что соответствующий код накладных расходов был настроен как **Возмещаемый** на странице настройки **Код накладных расходов**. Убедитесь, что параметры были синхронизированы с базами данных канала Commerce через обработку графика распределения.

### <a name="refunding-charges-on-a-return-order-transaction"></a>Возмещение накладных расходов по проводке заказа на возврат

Накладные расходы не возмещаются систематически для **Заказов на возврат**, созданных в Commerce. Пользователям требуется выбрать параметр **Копировать накладные расходы** при создании **Заказа на возврат**. Если параметр **Копировать накладные расходы** не выбран, накладные расходы из исходной проводки по продажам не будут подлежать возмещению автоматически. Если параметр **Копировать накладные расходы** выбран, все накладные расходы будут скопированы в заказ на возврат и пользователь может вручную изменить или удалить любые накладные расходы, которые не требуется возмещать. Процесс заказов на возврат через центр обработки вызовов в настоящее время не учитывает флаг **Возмещаемый** в настройке **Код накладных расходов**.

### <a name="configuring-pos-receipts-to-show-charges"></a>Настройка чеков POS для отображения накладных расходов

Следующие элементы чека были добавлены в строку и нижний колонтитул чека для поддержки функций расширенного автоматического начисления накладных расходов.

- **Накладные расходы на поставку по строке** — этот элемент уровня строки можно использовать для обзора кодов конкретных накладных расходов, которые были применены к строке продаж. Только коды накладных расходов, которые помечены как **Отгрузка** на странице **Код накладных расходов**, будут отображаться здесь.
- **Другие накладные расходы по строке** — этот элемент уровня строки можно использовать для обзора любых не связанных с доставкой кодов накладных расходов, которые были применены к строке продаж. Это коды накладных расходов, в которых флаг **Доставка** на странице **Код накладных расходов** не был включен.
- **Сведения о накладных расходах на поставку заказа** — данный элемент уровня нижнего колонтитула показывает описания кодов накладных расходов, примененных к заказу, которые были помеченных как накладные расходы **Доставка** на странице настройки **Код накладных расходов**.
- **Накладные расходы на поставку заказа** — этот элемент уровня нижнего колонтитула отображает значение накладных расходов по доставке в долларах.
- **Сведения о других накладных расходах по заказу** — данный элемент уровня нижнего колонтитула показывает описание кодов накладных расходов, примененных к заказу, которые не были помеченных как накладные расходы, связанные с доставкой.
- **Другие накладные расходы по заказу** — этот элемент уровня нижнего колонтитула отображает значение в долларах для других накладных расходов, которые не связаны с доставкой.

Рекомендуется, чтобы организация также добавила поля свободного текстового формата в нижний колонтитул чека, чтобы определить области, где будет приведена сводка накладных расходов.

### <a name="preventing-charges-from-being-calculated-until-the-pos-order-is-completed"></a>Предотвращение расчета накладных расходов до завершения заказа POS

Некоторые организации могут предпочитать дождаться завершения добавления всех строк продажи в проводку POS, прежде чем рассчитывать накладные расходы. Чтобы предотвратить расчет накладных расходов в процессе добавления номенклатур в проводку POS, включите параметр **Расчет накладных расходов вручную** в **Профиле функциональности**, который используется в магазине. Если этот параметр включен, пользователи POS-терминала должны использовать операцию **Рассчитать итоги** после завершения добавления продуктов к проводке в POS. Операция **Рассчитать итоги** затем запустит расчет всех автоматически добавляемых накладных расходов для заголовка или строк заказа, как это применимо.

### <a name="charges-override-reports"></a>Отчеты о переопределении накладных расходов

Если пользователи вручную переопределили вычисленные расходы или добавили вручную накладные расходы в проводку, эти данные будут доступны для аудита в отчете **Журнал переопределения расходов**. Отчет можно найти по пути **Retail и Commerce \> Запросы и отчеты \> Журнал переопределения расходов**. Важно отметить, что данные, необходимые для этого отчета, импортируются из базы данных канала в головной офис через задания планирования распределения "P". Таким образом, сведения о только что выполненных в POS переопределениях могут быть недоступны сразу в этом отчете, пока это задание не отправит данные проводок магазина в головной офис.