---
title: Управление розничной ценой продажи
description: В этой статье описываются принципы создания цен продажи и управления ими в Dynamics 365 Commerce.
author: ShalabhjainMSFT
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16c948e6e14309f4e340bf622fac42b14e6ee591
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887018"
---
# <a name="retail-sales-price-management"></a>Управление розничной ценой продажи

[!include [banner](includes/banner.md)]

В этой статье предоставлена информация о процессе создания цен продажи и управления ими в Dynamics 365 Commerce. Основное внимание уделяется понятиям, участвующим в этом процессе, и на влияние различных параметров конфигурации для цен продажи.

## <a name="terminology"></a>Терминология

В этой статье используются следующие термины.

| Срок | Определение, использование и примечания |
|---|---|
| Цена | Сумма одной единицы измерения, в которой продается продукт, в POS-клиенте или в заказе на продажу. В этой статье термин *цена* всегда означает цену продажи, а не цену запасов или себестоимость. |
| Базовая цена | Цена, устанавливаемая в поле **Цена** выпущенного продукта. |
| Цена по коммерческому соглашению | Цена, устанавливаемая на продукта или вариант с помощью коммерческого соглашения типа **Цена (продажи)**. |
| Лучшая цена | Когда несколько цен или скидок могут применяться к продукту, минимальная сумма цены и/или наибольшая сумма скидки, которая создает минимальную возможную чистую сумму, которую должен заплатить клиент. В этой статье понятие наилучшей цены всегда называется "лучшая цена". Эта лучшая цена отличается от значения перечисления **Лучшая цена** для конкурентного режима скидок и их не следует путать. |

## <a name="price-groups"></a>Группы цен

Ценовые группы являются основой управления ценами и скидками в Commerce. Ценовые группы используются, чтобы назначать цены и скидки сущностям Commerce (то есть, каналам, каталогам, назначениям и программам лояльности). Так как ценовые группы используются для всех цен и скидок, очень важно планировать способ использования их перед началом.

Сама по себе ценовая группа содержит просто имя, описание и, при необходимости, приоритет ценообразования. Главное, что нужно помнить о ценовых группах — они используются для управления отношениями "многие ко многим", которые скидки и цены имеют с сущностями Commerce.

На следующем рисунке показано, как используются ценовые группы. На этом рисунке обратите внимание, что "Ценовая группа" находится буквально в центре управления ценами и скидками. Сущности Commerce, которые можно использовать для управления дифференцированными ценами и скидками, находятся в левой части, а фактические записи цен и скидок находятся в правой стороне.

![Группы цен.](./media/PriceGroups.png "Группы цен")

При создании ценовых групп не следует использовать одну ценовую группу для различных типов сущностей Commerce. В противном случае может быть трудно определить, почему конкретная цена или скидка применяется к транзакции.

Как показывает красная пунктирная строки на рисунке, Commerce не поддерживает базовую функциональность ценовой группы Microsoft Dynamics 365, которая устанавливается непосредственно для клиента. Однако в этом случае вы получаете только цену продажи по коммерческим соглашениям. Если вы хотите применить цены для конкретных клиентов, рекомендуется не устанавливать ценовые группы непосредственно для клиента. Вместо этого следует использовать назначения. 

Обратите внимание, что если ценовая группа настроена для клиента, эта ценовая группа связывается с заголовком заказа на продажу для заказов, созданных для этого клиента. Если пользователь изменяет ценовую группу в заголовке заказа, старая ценовая группа заменяется новой ценовой группой только для текущего заказа. Например, старая ценовая группа не повлияет на текущий заказ, но она все равно будет связана с клиентом для будущих заказов.

В следующих разделах приведены дополнительные сведения о сущностях Commerce, которые можно использовать для настройки различных цен при использовании ценовых групп. Конфигурация цен и скидок для всех этих объектов осуществляется в два этапа. Эти шаги могут выполнять в любом порядке. Тем не менее логическим порядком является сначала задать ценовые группы для объектов, поскольку этот шаг, вероятно, сводится к однократной настройке, которая выполняется во время реализации. Затем, при создании цен и скидок, можно задать ценовые группы для этих цен и скидок индивидуально.

### <a name="channels"></a>Каналы

В сфере коммерции часто имеются разные цены в разных каналах. Основные два фактора, влияющие на специфические для каналов цены, это затраты и условия на местном рынке.

- **Затраты** — чем дальше канал от источника продукта, тем больше издержки на создание запасов продукта. Например, свежие продукты имеет ограниченный срок хранения и особые производственные требования (например, сезон выращивания). Во время зимнего сезона свежий салат, вероятно, требуется больших затрат в северном климате, чем в южном. Если вы задаете цены для каналов в большой географической области, возможно, требуется настроить разные цены в разных каналах.
- **Условия на местном рынке** — магазина, который имеет прямого конкурента по соседству, будет гораздо более чувствителен к ценам, чем магазин, который не имеет прямого конкурента рядом.

### <a name="affiliations"></a>Назначения

Общее определение назначения — это связь или ассоциация с группой. В Commerce назначения представляют собой группы клиентов. Назначения — это гораздо более гибкий инструмент для ценообразования и скидок для клиентов, чем базовая концепция групп клиентов и групп скидок в Microsoft Dynamics 365. Во-первых, назначения можно использовать как для цен, так и для скидок, в то время как нерозничное ценообразование имеет разные группы для каждого типа скидок и цен. Далее, клиент может принадлежать нескольким назначениям, но может принадлежать только к одной нерозничной группе ценообразования каждого типа. Наконец, хотя назначения можно настроить таким образом, чтобы они были связаны с клиентом, но это не обязательно. Можно использовать специальное назначение для анонимных клиентов на POS-терминале. Типичным примером анонимной скидки назначения является скидка для пожилых людей или студентов, когда клиент может получить скидку, просто показав удостоверение о принадлежности к группе.

Хотя назначения чаще всего связаны со скидками, их можно также использовать для дифференцированного ценообразования. Например, когда предприятие розничной торговли продает сотруднику, оно может захотеть изменить цену продажи вместо применения скидки к стандартной цене. Другой пример — предприятие розничной торговли, осуществляющее продажи как розничным, так и оптовым клиентам, может предлагать оптовым клиентам более низкие цены в зависимости от объема закупок. Назначения позволяют реализовать оба этих сценария.

### <a name="loyalty-programs"></a>Программы лояльности

В отношении цен и скидок программы лояльности в основе являются просто назначением, которое имеет специальное название. Можно настроить как цены, так и скидки для программы лояльности, так же, как они могут быть настроены для назначения. Однако способ, которым клиенты получают цены по программе поддержки постоянных клиентов во время транзакции или заказа, отличается от того, как они получают ценообразование от назначений. Клиенты могут получить ценообразование постоянного клиента только в том случае, если в транзакцию добавляется карточка постоянного клиента. При добавлении в транзакции карточки постоянного клиента также добавляется программа лояльности. Программа лояльности затем включает специальные цены и скидки.

Программы лояльности могут иметь несколько уровней, и скидки могут различаться для различных уровней. Таким образом предприятия розничной торговли могут предоставлять частым клиентам более крупные бонусы без необходимости вручную помещать этих клиентов в специальную группу.

Программы лояльности обладают дополнительной функциональной возможностью, помимо цен и скидок. Однако с точки зрения цен и скидок они совпадают с назначениями.

### <a name="catalogs"></a>Каталоги

Некоторые предприятия розничной торговли используют физические или виртуальные каталоги для рекламы продуктов и задания цен на них для конкретных групп клиентов. Как часть своей бизнес-модели для целевого маркетинга через каталог, эти предприятия розничной торговли могут задавать дифференцированные цены в своих различных каталогах. Microsoft Dynamics 365 поддерживает такую возможность, позволяя определить скидки и цены, специфические для каталога, так же как можно определить конкретные скидки, зависящие от канала или назначения. При внесении изменений в каталог можно связать ценовые группы с каталогом, точно также как можно связать их с каналом, назначением или программой лояльности.

### <a name="best-practices-for-price-groups"></a>Рекомендации для ценовых групп

Не используйте ценовую группу для нескольких типов объектов. Вместо этого используйте один набор ценовых групп для каналов, другой набор ценовых групп для назначений или программ лояльности и так далее. Префикс или суффикс имени ценовой группы позволяет визуально группировать различные типы ценовых групп, которые вы используете.

Избегайте установки ценовых групп непосредственно для клиента. Вместо этого используйте назначения. Таким образом можно назначить все типы цен и скидок клиентам, а не просто коммерческим соглашениям по цене продажи.

## <a name="pricing-priority"></a>Приоритет ценообразования

Сам по себе приоритет ценообразования является просто номером и описанием. Приоритеты ценообразования могут применяться к ценовым группам или могут применяться непосредственно к скидкам. При использовании приоритетов ценообразования они позволяют предприятию розничной торговли переопределить принцип наилучшей цены, контролируя порядок, в котором цены и скидки применяются к продуктам. Большее значение номера приоритета ценообразования вычисляется до меньшего значения приоритета ценообразования. Кроме того, если цена или скидка найдена в каком-либо номере приоритета, все цены или скидки, которые имеют более низкий номер приоритета, игнорируются.

Цена и скидка могут поступать из двух различных приоритетов ценообразования, поскольку приоритеты ценообразования применяются к ценам и скидкам независимо друг от друга.

Чтобы использовать приоритет ценообразования для цен, необходимо назначить приоритет ценообразования ценовой группе, а затем создать коммерческое соглашение по цене продажи для этой ценовой группы.

Функция приоритета ценообразования была введена для поддержки сценария, где предприятию розничной торговли требуется применить более высокие цены в определенной группе магазинов. Например, предприятие розничной торговли определило региональные цены по восточному побережью США, но хочет установить более высокие цены на некоторые продукты в магазинах Нью-Йорка, поскольку затраты на продажу некоторых продуктов в городе выше и/или поскольку местный рынок готов к более высокой цене.

Как было описано в пункте "Лучшая цена" в этой статье, механизм ценообразования обычно выбирает меньшую из двух цен. Таким образом, предприятие розничной торговли обычно не может использовать более высокую из двух цен в магазине, который имеет как ценовую группу восточного побережья, так и ценовую группу Нью-Йорка. Чтобы решить эту проблему до введения функции приоритета ценообразования предприятие розничной торговли должно было определить цены для каждого продукта дважды и не назначать обе ценовые группы. Кроме того, предприятию розничной торговли приходилось создавать лишние ценовые группы для изоляции продуктов, чтобы отделить продукты, которые имеют более высокие цены, от продуктов с обычными, более низкими ценами.

Однако функция приоритета ценообразования позволяет предприятию розничной торговли создать приоритет ценообразования для цен в магазине, которые будет выше приоритета ценообразования для региональных цен. Кроме того, предприятие розничной торговли может создать приоритет ценообразования только для цен в магазине и оставить региональных цены с приоритетом ценообразования по умолчанию, который равен 0 (нулю). Обе настройки помогают гарантировать, что цены магазина будет всегда использоваться до региональных цен.

### <a name="pricing-priority-example"></a>Пример приоритета ценообразования

Рассмотрим пример, когда цены в магазине переопределяют другие цены.

Национальное предприятие розничной торговли задает большинство цен по областям и имеет четыре области: Северо-восток, Юго-восток, Средний запад и Запад. Оно определило несколько рынков с высокими затратами, которые могут поддерживать более высокие цены. Эти рынки находятся в Нью-Йорке, Чикаго и районе залива Сан Франциско.

В данном примере мы детально рассмотрим область "Северо-восток". Магазин 1-находится в Бостоне, а магазин 2 — на Манхэттене. Для магазина в Бостоне две ценовые группы связаны с каналом: "Северо-восток" и "Магазин 1". Для магазина на Манхэттене три ценовые группы связаны с каналом: "Северо-восток", "Нью-Йорк" и "Магазин 2".

Предприятие розничной торговли устанавливает два приоритета ценообразования: "Высокие затраты" имеет номер приоритета 5, а "Цены в магазине" имеет номер приоритета 10. (Помните, что по умолчанию приоритет ценообразования равен 0 \[ноль\], и цены или скидки, которые имеет более высокий номер приоритета, используются до цен или скидок, которые имеет меньший номер приоритета.) Для ценовой группы "Северо-восток" для приоритета ценообразования сохранено значение по умолчанию **0** (ноль). Если ценовой группы "Нью-Йорк" приоритет ценообразования равен **5**, поскольку Нью-Йорк — это рынок с высокими затратами. Для ценовых групп "Магазин 1" и "Магазин 2" для приоритета ценообразования задано значение **10**.

Двумя продуктами, продаваемыми предприятием розничной торговли, являются продукт 1, футболка, и товар 2, модные джинсы определенного бренда.

| Продукт | Цена "Северо-восток" | Цена "Нью-Йорк" | Цена магазина |
|---|---|---|---|
| Футболка | $15 | Не установлено | Не установлено |
| Модные джинсы | $50 | $70 | Не установлено |

Футболка продается по одной цене (то есть, $15) в магазинах в Бостоне и на Манхэттене, поскольку только одна цена задана в ценовой группе "Северо-восток", которая связана с обеими каналами. Модные джинсы продаются по $50 в магазине в Бостоне, так как это единственная цена, доступна в этом магазине. Однако в магазине на Манхэттене доступны две цены: $50 и $70. Так как приоритет ценообразования для ценовой группы "Нью-Йорк" выше, чем приоритет ценообразования 0 (ноль) для ценовой группы "Северо-восток", в системе POS цена будет определена как $70.

> [!NOTE]
> Для каждого приоритета ценообразования требуется полный проход через логику механизма розничного ценообразования. Таким образом, чтобы поддерживать эффективность расчета цен и скидок, следует использовать приоритеты ценообразования только в случае необходимости.

## <a name="types-of-prices"></a>Типы цен

В Microsoft Dynamics 365 можно задать цену продукта в трех местах:

- Непосредственно для продукта (базовая цена)
- В коммерческом соглашении о цене продажи
- В корректировке цены

Базовая цена и цена коммерческого соглашения являются частью ядра Dynamics 365, и они доступны, даже если не используется Commerce. Функция корректировки цены доступна только в Commerce. Следующий раздел содержит дополнительные сведения о каждом из этих параметров для задания цен, и в нем объясняется, как работают параметры совместно.

## <a name="setting-prices"></a>Настройка цен

### <a name="base-price"></a>Базовая цена

Простейший способ — это задать цену продукта непосредственно в продукте. Значение, настроенное напрямую в продукте, часто называется базовой ценой для продукта. Базовая цена задаются в поле **Цена** на вкладке **Продажа** страницы **Сведения о выпущенном продукте**. Значение вводится в валюте компании. По умолчанию цена назначается за количество, равное 1 единице измерения (ЕИ), которая устанавливается в поле **Ед. изм.** на вкладке **Продажа**. Фактическая цена за единицу продукта основывается на единице измерения, цене за количество и валюте.

Если у продукта имеются одна цена для всех, базовая цена предлагает наиболее эффективный способ управления ценой этого продукта. Даже при использовании коммерческих соглашений для настройки цен можно также установить базовую цену на продукт. Затем, если вы не используете коммерческое соглашение **Все**, у вас имеется резервная цена, которая используется, когда не применяется коммерческое соглашение.

Если валюта канала отличается от валюты компании, базовая цена в этом канале определяется с помощью преобразования валют для цены, установленной на продукт.

Несмотря на то, что единица измерения цены не является распространенным сценарием, механизм ценообразования поддерживает его. Если для единицы измерения цены задано значение, отличное от **0** (ноль), цена за единицу равна Цена ÷ Единица измерения цены. Например, если цена продукта составляет $10,00, а единица измерения цены равняется 50, цена для количества 1 равна $0,20 (= $10,00 ÷ 50).

### <a name="sales-price-trade-agreement"></a>Коммерческое соглашение о цене продажи

С помощью журнала коммерческих соглашений можно создать торговые соглашений о цене продажи для каждого продукта. В Microsoft Dynamics 365 имеются три области клиента для торговых соглашений по ценам продажи: **Таблица**, **Группа** и **Все**. Область клиентов определяет клиентов, к которому применяется данное коммерческое соглашение о цене продажи.

Коммерческое соглашение о цене продажи **Таблица** предназначено для одного клиента, который задается непосредственно в коммерческом соглашении. Этот сценарий не является типичным сценарием "бизнес-потребитель" (B2C). Однако если он имеет место, механизм ценообразования использует коммерческие соглашения **Таблица**, когда определяет цену.

Коммерческое соглашение о цене продажи **Группа** является типом, который чаще всего используется. За пределами Commerce коммерческие соглашения о цене продажи типа **Группа** предназначены для простой группы клиентов. Однако в Commerce понятие группы клиентов было расширено, чтобы оно стал более общей ценовой группой. Ценовую группу можно связать с каналом, назначением, программой лояльности или каталогом. Подробные сведения о ценовых группах см. в пункте "Ценовые группы" ранее в этой статье.

> [!NOTE]
> Цена коммерческого соглашения всегда используется до базовой цены.

### <a name="price-adjustment"></a>Ценовая коррекция

Как подразумевает названия, корректировка цены используется для изменения цены, которая была либо задана непосредственно в продукте, либо задана с помощью коммерческого соглашения. Корректировка цены может использовать только чтобы снизить цену, но не повысить. Корректировка цены представляет собой рекомендуемый способ для предприятий розничной торговли для создания, отслеживания и управления снижением цен на продукты с течением времени.

Существует три типа корректировки цены: скидка в процентам, сумма скидки и цена. Корректировка цены в виде скидки в процентах или суммы скидки всегда применяется к транзакции продажи. Однако корректировка цены типа "цена" применяется только в том случае, если скорректированная цена меньше цены, которая была установлена с помощью базовой цены или цены коммерческого соглашения. Таким образом, если цена, установленная в корректировке цены, больше нескорректированной цены, корректировка цены не используется.

## <a name="determining-price-for-a-product-in-a-transaction"></a>Определение цены для продукта в проводке

Расчет цены и скидки в проводке использует принцип поиска лучшей цены для клиента. В соответствии с этим принципом при обнаружении нескольких цен используется меньшая цена. Кроме того, используется сочетание скидок, дающее самую крупную сумму скидки для всей транзакции. В некоторых случаях меньшую скидку необходимо использовать для одного продукта, чтобы дополнительные скидки могли применяться к другим продуктам в проводке.

Единственным исключением из принципа поиска лучшей цены для клиента является возможность использовать скидки, когда скидка дается на самую дешевую номенклатуру в комплекте. Этот вариант дает возможность использовать скидки типа "наиболее дешевый", что выгодно для предприятия розничной торговли, когда продукты выбраны и сгруппированы. Таким образом, когда проводка включает больше продуктов, чем это необходимо для получения скидки на наименее дорогой продукт, механизм ценообразования выбирает продукты, образующие минимальную возможную сумму скидки для клиента.

Механизм ценообразования возвращает три цены для каждого продукта: базовая цена, цена из коммерческого соглашения и активная цена.

Базовая цена — это просто свойство в продукте и одинаково для всех и везде.

В коммерческом соглашении по цене продажи если для параметра **Найти далее** установлено значение **Да**, самая низкая цена, найденная для действующих коммерческих соглашений по цене продажи, используется как цена из коммерческого соглашения. Коммерческие соглашения можно найти с помощью ценовых групп или кода счета **Все**. Кроме того, коммерческие соглашения могут назначаться непосредственно клиенту. Если для параметра **Найти далее** задано значение **Нет**, используется цена из первого найденного коммерческого соглашения. Если коммерческие соглашения по цене продажи не найдены, цена из коммерческого соглашения устанавливается равной базовой цене.

Активная цена рассчитывается путем взятия цены из коммерческого соглашения и применения наибольшей корректировки цены, относящейся к продукту. Если корректировки цены не найдены или если рассчитанная активная цена больше, чем цена из коммерческого соглашения, активная цена устанавливается равной цене из коммерческого соглашения. Помните, что нельзя увеличить цену продукта с помощью корректировки цены. Применимые корректировки цены можно найти только с помощью ценовых групп, которые назначены каналу, каталогу, назначению или программе лояльности.

## <a name="category-price-rules"></a>Правила цены категории

Функция правил цены категории в Commerce предоставляет простой способ создания новых коммерческих соглашений для всех продуктов в категории. Эта функция также позволяет автоматически найти существующие торговые соглашения для продуктов в категории и задать их как с истекшим сроком действия.

При выборе параметра завершения срока действия существующих коммерческих соглашений система создается новый журнал коммерческих соглашений для продуктов в категории, которые имеют активные коммерческие соглашения. Однако этот журнал должен разноситься вручную. Кроме того, правила цены категории может найти существующие коммерческие соглашения, только если используется тоже правило цены (то есть, если вы создаете новое правило цены, использующее ту же категорию, что и раньше). Если вы не используете тоже правило цены, срок действия существующих коммерческих соглашений не завершается.

Цены могут быть увеличены или уменьшены с помощью полей **Правило цены** и **Основа для цен** правил цены категории.

- В поле **Правило цены** выберите требуемый тип изменения цены.

    - **Наценка** — процент базовой цены используется для расчета цены продажи. Например, наценка продукта, который стоит 10,00, а продается за 15,00, составляет 50 процентов.
    - **Маржа** — процент цены продажи, который используется для расчета суммы прибыли. Например, маржа продукта, который стоит 10,00, а продается за 15,00, составляет 33,3 процента.
    - **Фиксированная сумма** — сумма, которая добавляется к базовой цене, которая используется для расчета цены продажи. Например, фиксированная сумма продукта, который стоит 10,00, а продается за 15,00, составляет 5,00.

- В поле **Основа для цен** выберите тип цены для изменения.

    - **Базовая себестоимость** — сумма, которую предприятие розничной торговли выплатило поставщику.
    - **Базовая цена** — цена продажи до применения коммерческих соглашений и корректировок цен.
    - **Текущая цена** — цена продажи после применения коммерческих соглашений и корректировок цен.

Чтобы легко обновить цены различных продуктов из различных категорий продуктов, можно использовать категории дополнительного продукта вместе с правилами цены категории.

## <a name="best-practices"></a>Рекомендации

Microsoft SQL Server Express часто используется для базы данных канала из-за его стоимости (бесплатно). Имейте в виду, что SQL Server Express имеет ограничения на оборудование и ограничивает размер данных. Если вы ошиблись при планировании, можете быстро достичь ограничения на размер данных в SQL Server Express. Это относится не только к ценообразованию, но и к другим областям продукта. Ниже приведены несколько рекомендаций, которые помогут вам уменьшить объем данных.

- Если вы используете коммерческие соглашения, а ваши цены изменились, необходимо прекратить действие старых коммерческих соглашений, задав дату окончания. Со временем такой подход позволяет уменьшить количество коммерческих соглашений, которые будут храниться в базах данных канала. Он также помогает сократить объем данных, с которыми должен работать алгоритм расчета цены.
- Если цены зависят от варианта продукта, следует использовать базовую цену продукта как цену наиболее распространенного варианта. Затем используйте коммерческие соглашения только для цен вариантов, которые являются исключениями. Такой подход позволяет сократить число записей коммерческого соглашения. Поскольку импортировать данные в Microsoft Dynamics 365 очень легко, у вас может возникнуть желание импортировать коммерческие соглашения для каждого варианта каждого продукта. Однако такой подход может создавать много коммерческих соглашений, которые имеют одинаковое значение. Таким образом, он может без необходимости увеличить размер данных.
- Commerce обрабатывает цены вариантов в порядке от наиболее конкретных к наименее конкретным. Если аналитика продукта не влияет на цену, нет необходимости определять коммерческие соглашения для нее. Например, продукт доступен в трех цветах и четырех размерах, но цена зависит только от размера. Если определить коммерческое соглашение для каждого варианта, вы создадите 12 записей. Вместо этого можно определить коммерческое соглашение только для каждого размера и оставить аналитику "Цвет" пустой. В этом случае будет создано только четыре записи.

    Кроме того, если не каждое значения аналитики дает различные цены, можно определить одно коммерческое соглашение для шаблона продукта и оставить все аналитики продукта пустыми. Затем определите отдельное коммерческое соглашение только для каждого значения аналитики, которое создает другую цену. Например, если размер XXL имеет более высокую цену, а все другие размеры имеют одинаковую цену, требуется только два коммерческих соглашения: одно для шаблона продукта и второе для размера XXL.

## <a name="prices-that-include-tax-vs-prices-that-exclude-tax"></a>Цены, которые включают налог, и цены, которые не включают налог

При настройке цены продажи в Dynamics 365 вы не указываете, включает ли заданное значение цены налог или не включает. Значение является просто ценой. Тем не менее настройка **Цена включает налог** для каналов позволяет настраивать каналы так, чтобы они включали или не включали налог в цену. Этот параметр устанавливается для канала и может быть изменен даже в одной компании.

Если вы работаете как с ценами, включающими налог, так и с ценами, которые налог не включают, очень важно правильно установить цены, так как общая сумма, которую клиент оплачивает, изменяется при изменении настройки **Цена включает налог** для канала.

## <a name="differences-between-commerce-pricing-and-non-commerce-pricing"></a>Различия между ценообразованием Commerce и ценообразованием, отличным от Commerce

Единый механизм ценообразования используется для расчета цены во всех каналах: центр обработки вызовов, розничный магазин и интернет-магазины. Это помогает в обеспечении единых сценариев Commerce.

Ценообразование предназначено для работы с сущностями Commerce, а не с сущностями, отличными от Commerce. В частности, оно предназначено для установке цен по магазинам, а не по складам.

Механизм ценообразования Commerce **не поддерживает** следующие функции ценообразования:

- Настройка цен аналитиками хранения "сайт" или "сайт и склад" не поддерживается. Если вы укажете только аналитику "сайт" в коммерческих соглашениях, то механизм ценообразования проигнорирует сайт и применит коммерческое соглашение ко всем сайтам. Если вы указываете "сайт и склад", то поведение не определено/не проверено, поскольку ожидается, что розничные торговцы используют ценовые группы магазина для управления ценами для каждого магазина/склада.
- Ценообразование на основе атрибутов не поддерживается.
- Сквозная скидка поставщика не поддерживается.
- Функция универсальной валюты не поддерживается, т. е. даже если для коммерческого соглашения включено **Включать универсальную валюту**, это коммерческое соглашение по-прежнему будет считаться действительным только для валюты, определенной в коммерческом соглашении.
- Стандартный механизм ценообразования Supply Chain Management поддерживает расчет ценообразования на основе значения "Запрошенная дата отгрузки" и "Запрошенная дата поступления", а также текущей даты. Однако в настоящее время розничное ценообразование не поддерживает эти значения. Причина в том, что для сценариев B2C клиенты не ожидают, что запрошенная дата поставки повлияет на цену номенклатуры. В некоторых случаях у розничных продавцов есть и операции B2B, и B2C. В операциях B2B цены обычно изменяются на основе дат поставки. Эти розничные продавцы могут использовать ценообразование Supply Chain Management для своего бизнеса B2B и розничное ценообразование для своего бизнеса B2C. Розничное ценообразование используются только в том случае, если пользователь приложения добавлен в качестве пользователя центра обработки вызовов, поэтому розничные продавцы могут назначить определенных пользователей, которые будут работать с ценообразованием Supply Chain Management, назначить некоторых пользователей, которые будут работать с розничным ценообразованием, то есть эти пользователи должны быть добавлены в качестве пользователей центра обработки вызовов. Кроме того, свойство **Использовать текущую дату для расчета цен** в разделе **Параметры Commerce > Ценообразование и скидки > Прочее** должно быть включено. Таким образом, они могут по-прежнему использовать значение параметра расчетов с клиентами для запрошенной даты отгрузки или запрошенной даты поступления, но розничное ценообразование будет по-прежнему использовать текущую дату для расчета ценообразования.

Кроме того, **только** механизм ценообразования Commerce поддерживает следующие функции ценообразования:

- Цена основана на аналитиках продукта, в порядке от цены самого конкретного варианта до цены наименее конкретного варианта и до цены шаблона продукта. Цена, устанавливаемая с помощью двух аналитик продукта (например, цвет и размер) используется до цены, устанавливаемой с помощью только одной аналитики продукта (например, размер).
- Одна и та же ценовая группа может использоваться для управления ценообразованием и скидками.

## <a name="pricing-api-enhancements"></a>Расширения API ценообразования

Цена является одним из важнейших факторов, которые управляют решениями по покупке многих клиентов, и многие клиенты сравнивают цены на различных сайтах до того, как они совершают покупку. Для обеспечения того, что они предоставляют конкурентные цены, розничные продавцы внимательно следят за своими конкурентами и часто проводят рекламные акции. Чтобы помочь этим предприятиям розничной торговли привлечь клиентов, очень важно, чтобы поиск продуктов, функция просмотра, списки и страница сведений о продукте отображали наиболее точные цены.

Интерфейс прикладного программирования (API) **GetActivePrices** в Commerce возвращает цены, включающие простые скидки (например, однострочные скидки, которые не зависят от других номенклатур в корзине). Таким образом отображаемые цены будут ближе к фактической сумме, которую клиенты будут платить за товары. Этот интерфейс API включает все типы простых скидок: основанные на принадлежности, на основе постоянных клиентов, на основе каталогов и на основе каналов. Кроме того, интерфейс API возвращает имена и сведения о сроках действия для примененных скидок, чтобы розничные компании могли предоставить более подробное описание цены и создать ощущение срочности, если срок действия скидки скоро истечет.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
