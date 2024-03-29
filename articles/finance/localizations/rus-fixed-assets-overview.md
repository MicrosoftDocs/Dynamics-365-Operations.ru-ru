---
title: Обзор основных средств
description: В этой статье содержится информация о модуле "Основные средства" для России.
author: AdamTrukawka
ms.date: 12/02/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: atrukawk
ms.search.validFrom: 2019-01-04
ms.dyn365.ops.version: 10.0.1
ms.search.form: ''
ms.openlocfilehash: 1a9223e140312b73316b2cb3b0e5bee2cf107d41
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280637"
---
# <a name="fixed-assets-overview"></a>Обзор основных средств

[!include [banner](../includes/banner.md)]

Модуль **Основные средства (Россия)** обеспечивает автоматизированный учет основных средств, нематериальных активов, а также спецодежды, спецоснастки и основные средства, которые не считаются ценными, с момента их ввода в эксплуатацию и размещения на соответствующих счетах до тех пор, пока они не будут утилизированы.

Требования к учету основных активов в законодательстве Российской Федерации различаются в зависимости от того, используется ли счет для целей бухгалтерского учета или налогообложения. Поэтому для соответствия требованиям законодательства Российской Федерации для записей учета основных средств следует использовать не менее двух моделей бухгалтерского учета — финансового и налогового. Как правило, может быть неограниченное количество моделей стоимости. Кроме того, можно добавлять модели для внутренних бизнес-счетов и счетов, основанных на международных стандартах бухгалтерского учета.

Все транзакции по основным средствам и нематериальным активам могут быть рассчитаны одновременно на основе неограниченных моделей стоимости для одной компании. Для каждой модели стоимости можно определить коды валюты, профиля разноски и финансовой аналитики.

Амортизирующие активы делятся на группы амортизации в модели стоимости. Таким образом, настройка начисления амортизации для различных подгрупп основных средств в модели стоимости является гибкой. Амортизационные группы используются для организации бухгалтерского и налогового учета.

Транзакции основных средств могут быть распределены по различным кодам аналитик так же, как они распределяются по всей системе бухгалтерского учета. Центры затрат, подразделения и коды расходов для налога на прибыль могут использоваться в качестве кодов аналитики.

Помимо учета основных средств модуль **Основные средства (Россия)** имеет и другие функциональные возможности. Далее приводятся некоторые примеры.

- Предоставьте подробную информацию об основных средствах компании.
- Печать следующих нормативных форм об операциях с основными средствами и создание реестра печатных форм:

    - Акт приемки (\#ОС-1 и \#ОС-1a)
    - Отчет о передаче (\#ОС-1 и \#ОС-1a)
    - Акт о приеме-передаче объекта основных средств (\#ОС-1 и \#ОС-1a)
    - Накладная на внутреннее перемещение (\#ОС-2)
    - Акт о приеме-сдаче (\#ОС-3)
    - Выписка по списанию ОС (\#ОС-4 и \#ОС-4a)
    - Инв.карточка (\#ОС-6)
    - Акт приемки оборудования (\#№ ОС-14)

- Ведение налогового учета для целей налога на прибыль. В рамках этого обслуживания можно создать отсрочки для списания убытков в налоговом учете.
- Ведение учета для малоценных основных средств (МОС): спецодежды и спецоснастки.
- Ведение различных периодических задач. Эти задачи включают создание штрих-кодов из инвентарных номеров основных средств, инициализации амортизационных премий и изменения метода амортизации.
- Ведение операций с основными средствами с помощью журнала ОС (например, ввод в эксплуатацию, амортизация и списание).
- Ведение операций ОС с помощью периодических журналов (учет, переоценка и списание).
- Ведение бюджетов ОС. 
- Рассчитать и создать налоговые декларации по начисленных налогам, транспортному налогу и земельному налогу.
- Создание различных отчетов.

## <a name="settings"></a>Настройки

Настройка модуля **Основные средства**, чтобы гарантировать точный расчет стоимости бухгалтерских транзакций и упростить процесс работы с основными средствами. Для получения дополнительной информации о том, как настроить модуль **Основные средства**, см. следующие темы:

- [Настройка основных средств (Россия)](rus-set-up-fixed-assets.md) — эта статья объясняет, как настроить основные средства для России. Она включает в себя информацию о том, как настроить модели стоимости основных средств, профили разноски, группы основных средств и параметры основных средств.
- [Настройка амортизации (Россия)](rus-depreciation-setup.md) — эта статья объясняет, как настроить амортизацию основных средств для России. Она включает в себя информацию о том, как настроить методы амортизации, коды анализа амортизации основных средств и группы амортизации, а также как обновить метод амортизации для налогового учета.
- [Методы амортизации (Россия)](rus-depreciation-methods.md) — в этой статье описываются различные методы амортизации ОС для России и реализация таких методов в приложении. Процесс расчета ежемесячной амортизации можно сделать несколькими способами. В учете и налоговом учете используются линейные и нелинейные методы расчета амортизации.
- [Амортизационные премии (Россия)](rus-bonus-depreciation.md) — эта статья объясняет, как настроить и рассчитать амортизационные премии. Премия амортизации — это дополнительная сумма амортизации, определяемая в течении первого года для некоторых типов производственных основных средств. Можно рассчитать амортизационную премию, уменьшив стоимость актива способом, отличным от обычной ставки амортизации. Можно применять суммы амортизационной премии в течение учетного периода после ввода актива в эксплуатацию или после крупного ремонта. Амортизационные премии всегда рассчитываются и применяются до других видов амортизации.
- [Настройка местоположений и нумерации основных средств (Россия)](rus-fixed-assets-locations-numbering.md) — эта статья объясняет, как настроить местоположения и нумерацию для основных средств. Местоположения определяется для основных средств и используются, чтобы рассчитывать начисления амортизации. В зависимости от местоположения ОС вычисленная сумма амортизации относится или на производственные затраты продукта, или на счет ГК.

## <a name="working-with-fixed-assets"></a>Работа с ОС

- [Основные средства](../fixed-assets/fixed-assets.md) — перед созданием проводок для любого основного средства или нематериального актива необходимо зарегистрировать запись средства и предоставить основную информацию. Эта статья включает описание страницы **Основные средства**, которая используется для регистрации и предоставляет обзор счетов ОС.
- [Регистрация приобретений основных средств (Россия)](rus-register-acquisition.md) — вы можете зарегистрировать приобретение основного средства, используя журнал накладных поставщиков или заказ на покупку. Как правило, журнал накладных поставщиков используется, если движение запасов основного средства не требуется отслеживать (например, если основное средство покупается и вводится в эксплуатацию в течение того же периода). Заказ на покупку может использоваться, если приобретено несколько идентичных основных средств или необходимо отслеживать движение запасов ОС. В этой статье объясняется, как зарегистрировать приобретение основного средства с помощью журнала накладных и заказа на покупку. В нем также объясняется, как сторнировать транзакцию по приобретению основного средства.
- [Приобретение ОС и их ввод в эксплуатацию (Россия)](rus-fixed-asset-acquisition.md) — следующие амортизированные имущественные активы могут быть приобретены и введены в эксплуатацию:

    - Купленные основные средства
    - Основные средства, получаемые в качестве вклада в уставный капитал
    - Основные средства, получаемые по договору дарения (т. е. получаемые без компенсации)
    - Основные средства, получаемые в обмен на другое имущество
    - Неучтенные основные средства, обнаруженные в ходе инвентаризации
    - Арендованные основные средства, возращаемые арендатором

    В сценариях, в которых фигурируют эти основные средства, используется кредитовый счет. Кредитный счет предоставляет несколько вариантов для создания корректирующих проводок в книге учета. Для указания счета создайте вручную проводку в журнале основных средств. Также можно на странице **Профили разноски** (**Основные средства (Россия)** \> **Настройка** \> **Профили разноски**) настроить профили разноски для проводок по различным типам основных средств.

    Стоимость приобретенного основного средства может отличаться от стоимости покупки. Например, стоимость может быть увеличена за счет накладных расходов на приобретение, например расходов на испытания и работы по вводу в эксплуатацию.

    В этой статье объясняется, как приобрести основное средство (то есть ввести его в эксплуатацию), создать стандартные формы печати, собрать ОС и реверсировать проводки по приобретению.

- [Расчет амортизации (Россия)](rus-depreciation-calculation.md) — эта статья объясняет, как рассчитывать амортизацию основных средств. Она включает в себя информацию о том, как рассчитать и сторнировать амортизацию с помощью нелинейного налогового метода амортизации.
- [Частичная разборка ОС (ликвидация) (Россия)](rus-fixed-assets-disassembly.md) — согласно законодательству Российской Федерации (ПБУ 6/01) частичная разборка (ликвидация) объектов основных средств может привести к изменению первоначальной стоимости основного средства. Снимаемые при разборке комплектующие могут учитываться как запасные части. Запасы, оставшиеся после выбытия основного средства, разносятся по своей фактической себестоимости. Эта себестоимость основывается на текущей рыночной стоимости запасов на дату разноски в учете.

    Эта статья содержит информацию о том, как настроить профили проводок и создать проводку частичной разборки основного средства. В ней также содержится информация о различных методах расчета цен.

- [Продажа, выбытие и списание ОС (Россия)](rus-sell-dispose-write-off-fixed-assets.md) — вы можете организовать выбытие ОС по любой из следующих причин:

    - Основные средства продаются другим юридическим лицам или физическим лицам.
    - Средства перемещается и используется как депозит в совместных работах или в качестве уставного капитала.
    - Средства подарены или используются как другой тип некомпенсированного перемещения.
    - Средства ликвидируются в результате аварии или природной катастрофы.
    - Основные средства обменяны по договору мены.

    Существует три способа создания проводки по выбытию: вывод (продажа), вывод (разборка) и списание ОС. В этой статье объясняется, как списать основное средство (ОС), настроить автоматическое создание счета расходов будущих периодов (РБП), создать заказ на продажу ОС и создать накладную с произвольным текстом для ОС.

- [Создание проводки по аренде и окончании аренды основных средств (Россия)](rus-fixed-asset-leasing.md) — эта статья объясняет, как передать в аренду основное средство и зарегистрировать возврат арендованного основного средства.
- [Ведение основных средств](rus-maintain-fixed-assets.md) — эта статья включает в себя описание крупного ремонта. Если основное средство неактивно в течение более чем трех месяцев, или если в течение более чем 12 месяцев производится его реконструкция, расчет амортизации приостанавливается. Он возобновится только после возврата основного средства в эксплуатацию. Например, основное средство может стать неактивным в случае капитальной модернизации. **Модификация оборудования** — это специальная категория активов, включающая капитальный ремонт, усовершенствование, технические обновления, достройки и приобретение дополнительного оборудования для ОС. При выполнении модификации оборудования рассчитанная амортизация не пересчитывается. Однако амортизированная стоимость и срок службы ОС меняются.
- [Инвентаризация ОС (Россия)](rus-fixed-assets-counting.md) — процедура инвентаризации основных средств регулируется законодательными актами и представляет собой одну из процедур, призванных обезопасить имущество компании. По сути в процессе инвентаризации основных средств производится сравнение фактического наличия ценностей (деньги, оборудование, здания и обязательства) с данными учета.
- [Переоценка ОС в иностранной валюте](rus-fixed-asset-currency-revaluation.md) — представители иностранных организаций имеют право вести учет основных средств в иностранной валюте. Учет основных средств (например, бухгалтерский учет и налоговый учет) может вестись в разных валютах. Если модель стоимости основных средств вводится в иностранной валюте, валюта учета указывается в записи основного средства. Суммы проводок по основным средствам указываются и в валюте учета, и в исходной валюте компании по курсу, который действовал на дату проводки. При изменении курса валюты вычисляется переоценка, после чего и для модуля **Основные средства**, и для проводок ГК создаются корректирующие проводки прибыли или убытка от курсовой разницы.
- [Переоценка стоимости основных средств и амортизация (Россия)](rus-fixed-assets-revaluation.md) — организация может самостоятельно изменить стоимость основного средства один раз в год, в конце отчетного года (обычно 31 декабря). Переоценка основных средств также может быть сделано в связи с решением правительства. Как правило, переоценка стоимости основных средств сопровождается переоценкой амортизации. Эта статья включает в себя описание двух методов, которые могут быть использованы для изменения стоимости основных средств: индексация и прямой перерасчет (или прямая оценка).
- [Создание и разноска журналов бюджета для приобретений ОС (Россия)](rus-post-budget-fixed-asset-acquisition.md) — вы можете создавать финансовые планы и текущие бюджеты в модуле **Основные средства (Россия)** с помощью бюджетных моделей. Модель бюджета представляет собой коллекцию планируемых оборотов для конкретных счетов и периодов. В этой статье объясняется, как настраивать бюджетные модели и создать журнал бюджета основных средств.

## <a name="setting-up-and-working-with-nvfas-working-clothes-and-special-rigging"></a>Настройка и работа с МОС, спецодежда и спецоснастка

- [Малоценные основные средства (МОС) для России](rus-not-valuable-assets.md) — малоценные номенклатуры с высоким износом, которые используются на рабочем месте, можно отслеживать и учитывать как особый тип основных средств. Эти ОС известны как малоценные основные средства (МОС). МОС — это номенклатуры, стоимость которых меньше определенного предела. Общая стоимость МОС должна списываться для амортизации в первом месяце использования. В процессе покупки основных средств система делит основные средства и МОС по цене, исходя из ценности параметра **Макс. стоимость МОС**.

    Эта статья включает описание настройки параметров основных средств (ОС), групп ОС, идентификации групп ОС, складской аналитики, номенклатур и должностных лиц для МОС.

- [Учет спецодежды и спецоснастки для России](rus-working-clothes-instruments-accounting.md) — организация должна отчитываться за создание записи по каждой единице спецодежды или спецоснастки, выдаваемой сотруднику. Можно создавать запросы для отображения всех активов, которые имеются в наличии для сотрудников, и можно напечатать **Ведомость выдачи спецодежды (МБ-7)**. Можно отменить выдачу спецодежды или спецоснастки или вернуть на склад и рассчитать остаточную стоимость и остаточный период износа.

    Активы спецодежды и спецоснастки регулируются сроком полезной службы. Этот период начинается, когда номенклатура списывается со склада и выдается сотруднику. Он заканчивается после определенного периода использования. Срок службы каждой номенклатуры задается в месяцах. Все данные, относящихся к определенной номенклатуре, связаны. В эти сведения входит код сотрудника, срок жизни номенклатуры, дата, когда номенклатура выдана сотруднику и дата окончания срока службы, рассчитанная на основе показателя номенклатуры. При приближении окончания срока службы номенклатура списывается, чтобы она больше не была назначена сотруднику.

    Во время срока службы стоимость этих активов необходимо амортизировать. Если срок службы превышает двенадцать месяцев, что является юридически определенным значением, используется линейный метод амортизации. Если срок менее двенадцати месяцев, стоимость списывается при выдаче номенклатуры сотруднику. Страницы **Спецодежда** и **Спецоснастка** напоминают страницу **Основные средства**, которая используется для учета всей выданной спецодежды и спецоснастки.

- [Формы печати](printing-forms-fixed-assets.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
