---
title: Создание каталогов Commerce для сайтов B2B
description: В этой статье описывается, как создавать каталоги Commerce для сайтов бизнес-бизнес (B2B) Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 7d4ed3e2a76924c2c3c0ba55e21ba648e8da7b76
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136835"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>Создание каталогов Commerce для сайтов B2B

[!include [banner](includes/banner.md)]

В этой статье описывается, как создавать каталоги продуктов Commerce для сайтов бизнес-бизнес (B2B) Microsoft Dynamics 365 Commerce. Ответы на часто задаваемые вопросы о каталогах Commerce для сайтов B2B см. в разделе [Вопросы и ответы по каталогам Commerce для B2B](catalogs-b2b-sites-FAQ.md).

> [!NOTE]
> Эта статья применима в Dynamics 365 Commerce версии 10.0.27 и более поздних версий.

Каталоги Commerce используются для определения продуктов, которые вы хотите предложить в ваших интернет-магазинах B2B. При создании каталога указывается интернет-магазины, в которых продукты предлагаются, добавляются продукты, которые нужно включить, и улучшаются предложения продукта путем добавления сбытовых сведений. Можно создать несколько каталогов для каждого интернет-магазина B2B, как показано на следующем рисунке.

![Предварительная версия каталогов продуктов Commerce.](./media/Commerce_Catalogs.png)

Каталоги продуктов Commerce позволяют определить следующие сведения:

- **Тип каталога** — настройте значение как **B2B**. Для каталога можно определить свойства, связанные с каталогом B2B, такие как иерархия навигации, иерархия клиентов и метаданные атрибутов. 
- **Иерархия навигации, относящаяся к каталогу** — организации могут создавать отдельную структуру категорий для их определенного каталога.
- **Метаданные атрибутов, связанные с каталогом** — атрибуты содержат сведения о продукте. Назначая атрибуты категории навигационной иерархии, можно определить значения этих атрибутов на уровне продуктов, назначенных этой категории. Организации могут затем выполнять следующие задачи:

    - Определение значений атрибутов, относящихся к каталогу.
    - Контроль видимости атрибутов на уровне каталога.
    - Выберите уточнения, которые относятся к отдельному каталогу.

- **Каналы** — организации могут связывать более одного интернет-канала B2B с каталогом. Сквозная поддержка для каталогов в настоящее время доступна только для интернет-магазинов B2B.
- **Иерархии клиентов** — для определенного канала B2B организации могут сделать конкретный каталог доступным для выбранных B2B-партнерам путем связывания иерархий клиентов с этим каталогом.
- **Ценовые группы** — можно настроить цены и рекламные акции, которые относятся к конкретному каталогу. Эта возможность является основной причиной определения каталога для канала B2B. Ценовые группы для каталогов позволяют организация делать продукты доступными для предполагаемых организаций B2B и применять их предпочтительные цены и скидки. Клиенты B2B, которые заказывают из настроенного каталога, могут получить преимущества от специальных цен и рекламных акций после того, как они выполнять вход на сайт Commerce B2B. Чтобы настроить конкретные цены каталога, выберите **Ценовые группы** на вкладке **Каталоги** для связывания одной или нескольких ценовых групп в каталоге. Все торговые соглашения, журналы корректировки цены и дополнительные скидки, которые были связаны с одной и той же ценовой группой, будут применены, когда клиент сделает заказ по этому каталогу. (Расширенные скидки включают в себя пороговые скидки, скидки на количество и скидки за комплект.) Дополнительные сведения о ценовых группах см. в разделе [Ценовые группы](price-management.md#price-groups).

> [!NOTE]
> Эта функция доступна начиная с выпуска Dynamics 365 Commerce версии 10.0.27. Чтобы настроить зависящие от каталога конфигурации, такие как иерархия навигации и иерархия клиентов, в Commerce headquarters перейдите в рабочую область **Управление функциями** (**Администрирование системы \> Рабочие области \> Управление функциями**), включите функцию **Включите использование нескольких каталогов в каналах розничной торговли**, затем запустите задание **1110 CDX**. Если эта функция включена, все существующие каталоги, которые используются для магазинов POS или центра обработки вызовов, будут помечены как **Типа каталога = B2C** на странице **Каталоги**. Только существующие и новые каталоги, помеченные как **Тип каталога = B2C**, применимы к магазинам POS и центру обработки звонков. 

## <a name="b2b-catalog-process-flow"></a>Последовательность операций для каталога B2B

Процесс создания и обработки каталога имеет четыре общих шага. Подробное описание каждого шага приведено в следующем разделе.

> [!NOTE]
> Прежде чем продолжить, убедитесь, что каталог помечен как **Тип каталога = B2B**.

1. **[Конфигурация](#configure-the-catalog)**

    - Свяжите иерархию навигации.
    - Укажите даты вступления в силу и истечения срока годности, если они применимы.
    - Добавьте продукты и задайте их категории.
    - Свяжите ценовые группы.
    - Свяжите иерархию клиентов, относящуюся к вашим организациям B2B. 
    - Свяжите группу атрибутов измерения по умолчанию для уточнений, таких как размер, стиль и цвет.
    - Задайте метаданные атрибутов.

1. **[Проверка](#validate-the-catalog)** — на этом этапе выполняются правила проверки, обеспечивающие специфическое поведение. Далее приводятся некоторые примеры.

    - Убедитесь в отсутствии продуктов без категории.
    - Убедитесь, что все номенклатуры, которые включаются в каждый канал, связаны с каталогом.

1. **[Утверждение](#approve-the-catalog)**
1. **[Публикация](#publish-the-catalog)**

## <a name="set-up-the-catalog"></a>Настройка каталога

Используйте сведения из этого раздела, чтобы настроить каталог.

### <a name="configure-the-catalog"></a>Настройка каталога

В Commerce headquarters перейдите к пункту **Розница и коммерция \> Каталоги и ассортименты \> Все каталоги**, чтобы настроить каталог.

При создании нового каталога необходимо сначала связать его с одним или несколькими каналами. Только номенклатуры, связанные с выбранными вами [ассортиментами](/dynamics365/unified-operations/retail/assortments) каналов, могут использоваться при создании каталога. Чтобы связать каталог с одним или несколькими каналами, выберите **Добавить** на экспресс-вкладке **Каналы Commerce** страницы **Настройка каталога**. Убедитесь, что каталог помечен как **Тип каталога = B2B**.

#### <a name="associate-the-navigation-hierarchy"></a>Связывание иерархии навигации

Чтобы добавить продукты в каталог, необходимо выбрать иерархию навигации. Иерархия навигации поддерживает структуру категорий для каталога. Необходимо выбрать одну из иерархий навигации, связанных с каналами, выбранными на экспресс-вкладке **Каналы Commerce** на странице **Настройка каталога**. Чтобы связать навигационную иерархию по умолчанию с каждым из ваших каналов, перейдите в раздел **Розница и коммерция \> Настройка каналов \> Категории каналов и атрибуты продуктов**.

#### <a name="specify-time-effective-and-expiration-dates"></a>Указание дат вступления в силу и окончания срока действия

Чтобы указать даты вступления в силу и истечения срока действия для каталога, выберите верхний узел иерархии каталогов, чтобы вернуться в главное представление заголовка каталога. Затем на экспресс-вкладке **Общие** задайте требуемые даты вступления в силу и истечения срока действия.

#### <a name="add-and-categorize-products"></a>Добавление продуктов и задание их категорий

Чтобы настроить продукты для добавления в каталог, в Commerce headquarters перейдите к пункту **Розница и коммерция \> Каталоги и ассортименты \> Все каталоги**. Затем на вкладке **Каталоги** выберите **Добавить продукты**.

Или выберите узел в иерархии навигации. После этого можно будет добавлять продукты непосредственно в категорию в каталоге.

#### <a name="associate-price-groups"></a>Связывание ценовых групп

Чтобы настроить продукты для добавления в каталог, в Commerce headquarters перейдите к пункту **Розница и коммерция \> Каталоги и ассортименты \> Все каталоги**. Затем на вкладке **Каталоги** выберите **Добавить продукты**. 

Продукты, добавленные в каталог из корневого узла иерархии навигации путем выбора пункта **Добавление продуктов** на панели действий, наследуют свои категории, если исходная иерархия навигации также связана с каталогом. Изменения категорий, сделанные в исходной иерархии навигации, немедленно отражаются в каталогах. Необходимо повторно опубликовать каталоги, чтобы обновить каналы.

В качестве альтернативы можно выбрать узел в иерархии навигации и добавить продукты непосредственно в выбранную категорию в каталоге. 

При добавлении продуктов будет доступен параметр **Автоматически включать все варианты, если выбран только шаблон продукта**. Чтобы не допустить включения всех вариантов, выберите по крайней мере один вариант для шаблона продукта. 

> [!NOTE]
> Если выбрать автоматическое включение всех вариантов в большой выбор шаблонов продуктов, время обработки может быть дольше. Для больших объемов выбора рекомендуется выбрать **Включить все варианты** на панели действий на странице каталогов, чтобы выполнить операцию в пакетном режиме. Если включен только шаблон продукта в каталог и не включены никакие варианты, средство выбора вариантов может оказаться недоступным при переходе на страницу сведений о продукте. 

Чтобы настроить цены, связанные с каталогом, необходимо связать одну или несколько ценовых групп с каталогом. Чтобы связать ценовые группы с каталогом, в Commerce headquarters перейдите к пункту **Розница и коммерция \> Каталоги и ассортименты \> Все каталоги**. Затем на вкладке **Каталоги** в области **Цены** выберите **Ценовые группы**. Все торговые соглашения, журналы корректировки цены и дополнительные скидки (по пороговому значению, по количеству, скидки за комплект), которые были связаны с одной и той же ценовой группой, будут применены, когда клиент сделает заказ по этому каталогу.

Дополнительные сведения о ценовых группах см. в разделе [Ценовые группы](price-management.md#price-groups).

> [!NOTE]
> Вы не можете создать новую ценовую группу со страницы **Все каталоги**. Вместо этого ее необходимо создать на странице **Все ценовые группы**. Затем необходимо связать ее с каталогом на странице **Все каталоги**.

#### <a name="associate-a-customer-hierarchy"></a>Связывание иерархии клиентов

Чтобы связать иерархии клиентов, в Commerce headquarters перейдите к пункту **Розница и коммерция \> Каталоги и ассортименты \> Все каталоги**. Затем на вкладке **Каталоги** в области **Иерархия клиентов** выберите **Назначить иерархии**, чтобы связать одну или несколько иерархий клиентов с каталогом.

> [!NOTE]
> Вы не можете создать новую иерархию клиентов со страницы **Все каталоги**. Вместо этого ее необходимо создать на странице **Иерархии клиентов**. Затем необходимо связать ее с каталогом на странице **Все каталоги**.

#### <a name="associate-default-dimension-attribute-group-for-refiners-such-as-size-style-and-color"></a>Связывание группы атрибутов измерения по умолчанию для уточнений, таких как размер, стиль и цвет

Чтобы связать группу атрибутов измерения по умолчанию для уточнений, таких как размер, стиль и цвет, в Commerce headquarters перейдите к пункту **Розница и коммерция \> Каталоги и ассортименты \> Все каталоги**. Затем на вкладке **Каталоги** в области **Атрибуты** выберите **Группы атрибутов**.

#### <a name="set-attribute-metadata"></a>Задать метаданные атрибута

Чтобы настроить метаданные атрибутов, в Commerce headquarters перейдите к пункту **Розница и коммерция \> Каталоги и ассортименты \> Все каталоги**. Затем на вкладке **Каталоги** в области **Атрибуты** выберите **Задать метаданные атрибута**. Чтобы выбрать атрибуты, которые должны быть доступны для просмотра или уточнения, выберите категорию в связанной иерархии навигации для каталога, затем в разделе **Атрибуты продукта каталога** выберите атрибут. Затем выберите **Показать атрибут для канала**. По умолчанию все видимые атрибуты также доступны для поиска. Чтобы дополнительно сделать атрибуты уточняемым, выберите **Возможно уточнение**.

### <a name="validate-the-catalog"></a>Проверка каталога

Прежде чем новый каталог будет доступен для использования, он должен быть проверен и опубликован.

Чтобы проверить каталог, выполните следующие действия.

1. На вкладке **Каталоги** на странице **Все каталоги** в области **Проверка** выберите **Проверить каталог** для выполнения проверки. Это обязательный шаг. Он проверит, что требуемые настройки верны.
1. Выберите **Просмотр результатов**, чтобы просмотреть подробные сведения о проверке. В случае обнаружения ошибок необходимо исправить данные, затем выполнить проверку еще раз, до тех пор пока она не будет пройдена.

> [!NOTE]
> Если **Тип каталога = B2B**, проверка завершится с ошибкой, если были добавлены магазины POS или центр обработки звонков в каталог. С каталогами B2B должны быть связаны только интернет-каналы B2B. Если иерархия клиентов не связана с каталогом B2B, проверка также приведет к сбою. 

### <a name="approve-the-catalog"></a>Утвердить каталог

После проверки каталога его необходимо утвердить.

Чтобы запустить рабочий поток утверждения каталога, выполните следующие действия.

1. На панели действий страницы **Все каталоги** выберите **Рабочий процесс \> Отправить**.
1. Перейдите к пункту **Розница и коммерция \> Настройка Headquarters \> Рабочие процессы Commerce**, чтобы настроить шаги и авторизованных пользователей для рабочего процесса. Рабочий процесс определит шаги, необходимые для перевода каталога в состояние **Утвержден**.

### <a name="publish-the-catalog"></a>Публикация каталога

После того как каталог перейдет в состояние **Утвержден**, его можно опубликовать, выбрав команду **Опубликовать** в меню **Каталоги**. После того как каталог перейдет в состояние **Опубликован**, он может использоваться для ввода заказов центра обработки вызовов и отправки процессов каталогов. Можно опубликовать каталог вручную или с помощью процесса пакетной обработки. Дату вступления в силу, определенная для каталога определяет, когда продукты доступны в интернете-магазине. Определенная вами дата окончания срока действия определяет, когда продукты удаляются из интернет-магазина.

> [!NOTE]
> Можно опубликовать каталог, содержащий продукты с предупреждениями. Однако эти продукты не отображаются в интернет-магазине.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Влияние расширяемости каталогов Commerce на настройки B2B](catalogs-b2b-sites-dev.md)

[Вопросы и ответы по каталогам Commerce для B2B](catalogs-b2b-sites-FAQ.md)

[Модуль выбора каталога](catalog-picker.md)