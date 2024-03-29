---
title: Смешивание аналитик продуктов в местонахождении
description: В этой статье содержится информация о смешивании аналитик продуктов в местонахождении. Эта функция профиля местонахождения помогает улучшить управление местоположением при использовании вариантов продуктов или продуктов, имеющих аналитики, например, в индустрии моды. Она позволяет определить, могут ли быть смешаны конфигурации, цвета, стили и размеры для конкретного профиля местоположения, или же можно поместить только одну из этих аналитик или их комбинацию в одно и то же местонахождение.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 9daf6061d56ef004753114aaffa8eb580cea1186
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885735"
---
# <a name="location-product-dimension-mixing"></a>Смешивание аналитик продуктов в местонахождении

[!include [banner](../includes/banner.md)]

Смешивание аналитик продуктов в местонахождении — это функция профиля местонахождения, которая помогает улучшить управление местоположением при использовании вариантов продуктов или продуктов, имеющих аналитики, например, в индустрии моды. Она позволяет определить, могут ли быть смешаны конфигурации, цвета, стили и размеры для конкретного профиля местоположения, или же можно поместить только одну из этих аналитик или их комбинацию в одно и то же местонахождение.

## <a name="turn-the-location-product-dimension-mixing-feature-on-or-off"></a>Включение или отключение функции смешивания аналитики продуктов в местонахождении

Для использования описанных в этой статье функций в системе должна быть включена функция *Смешивание аналитик продуктов в местонахождении*. В Supply Chain Management 10.0.25 эта функция обязательна и не может быть отключена. При запуске версии, более старой, чем 10.0.25, администраторы могут включать или выключать эту функцию путем поиска функции *Смешивание аналитик продуктов в местонахождении* в рабочей области [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="setup"></a>Настройка

Каждое местоположение склада должно иметь связанный с ним профиль местоположения, описывающий свойства местоположения. Таким образом, все местоположения, использующие один и тот же профиль местоположения, смогут разрешать смешивание аналитики продуктов после ее настройки.

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a>Настройка профилей местоположений для разрешения смешивания аналитик продуктов

1. Перейдите в раздел **Управление складом \> Настройка \> Склад \> Профили местонахождения**.
1. В списке профилей местоположения выберите **НАВГРУЗ**.
1. На панели операций выберите **Правка**.
1. На экспресс-вкладке **Общие** установите для параметра **Включить смешивание аналитик продуктов в местонахождении** значение *Да*.

    > [!NOTE]
    > Можно установить для этого параметра значение *Да* только в том случае, если для параметра **Разрешить смешанные номенклатуры** установлено значение *Нет*.

1. На экспресс-вкладке **Разрешенное смешивание номенклатур продуктов** установите для параметра **Размер** значение *Да*. В сценарии, описанном в этой теме, смешивание может выполняться только для продуктов с различной аналитикой **Размер**. Однако также доступны и другие варианты.
1. Нажмите **Сохранить**.

### <a name="create-a-new-product-master-and-product-variants"></a>Создайте новый шаблон продукта и варианты продукта.

1. Перейдите в раздел **Управление сведениями о продукте \> Продукты \> Шаблоны продукта**.
1. На панели операций выберите **Создать** для создания шаблона продукта.
1. В диалоговом окне **Создать продукт** задайте следующие значения:

    - **Тип продукта:** *Номенклатура*
    - **Подтип продукта:** *Шаблон продукта*
    - **Номер продукта:** *B0001*
    - **Название продукта:** *Размер B0001*
    - **Группа аналитик продуктов:** *Размер*
    - **Метод конфигурации:** *Заранее определенный вариант*

1. Нажмите **ОК**.
1. На странице **Сведения о продукте** на экспресс-вкладке **Общие** задайте следующие значения.

    - **Автоматическое создание вариантов:** *Да*
    - **Группа размеров:** *CASUALDHIR*

1. Для просмотра предопределенных вариантов на панели операций выберите **Варианты продукта**.

    Отображается страница **Варианты продукта**, на которой отображается список вариантов из конфигурации группы размеров.

### <a name="release-products-to-the-usmf-company"></a>Выпустите продукты в компанию USMF

1. В области операций выберите **Использовать продукты**.
1. На странице **Выбор продуктов для выпуска** проверьте, что в списке указан номер продукта *B0001*, затем выберите **Далее**.
1. Выберите **Далее**, чтобы подтвердить варианты продукта для выпуска.
1. На странице **Выбор компаний для выпуска** выберите *USMF*, затем выберите **Далее**, чтобы подтвердить выбор.
1. На странице **Подтвердить выбор** выберите **Готово**, чтобы завершить выпуск.

    Вы получаете сообщение "Операция завершена".

### <a name="update-a-released-product-in-the-usmf-company"></a>Обновление выпущенного продукта в компании USMF

1. Убедитесь, что вы выполнили вход в компанию **USMF**.
1. Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**, чтобы завершить создание выпущенного продукта.
1. Найдите и выберите код номенклатуры *B0001*, чтобы открыть страницу **Сведения о выпущенном продукте**.
1. На панели операций выберите **Правка**.
1. На экспресс-вкладке **Общие** убедитесь, что в поле **Группа моделей номенклатуры** установлено значение *ФИФО*.
1. На панели операций на вкладке **Продукт** в группе **Настройка** выберите **Группы аналитики**.
1. Задайте следующие значения:

    - **Группа аналитик хранения:** *Товары*
    - **Группа аналитик отслеживания:** *Нет*

1. Нажмите **ОК**.
1. На панели операций на вкладке **Продукт** в группе **Настройка** выберите **Иерархия резервирования**.
1. Задайте для поля **Иерархия резервирования** значение *По умолчанию*, затем выберите **ОК**.
1. На экспресс-вкладке **Общие** в разделе **Администрирование** обратите внимание, что выбранные параметры были обновлены.
1. На экспресс-вкладке **Покупка** в поле **Цена** введите *10*.
1. На экспресс-вкладке **Управление затратами** в поле **Номенклатурная группа** введите *Аудио*.
1. На экспресс-вкладке **Покупка** в поле **Цена** введите *10*.
1. На экспресс-вкладке **Склад** в поле **Код группы упорядочения единиц** введите *шт.*
1. Нажмите **Сохранить**.

### <a name="create-a-location-directive"></a>Создание директивы местонахождения

1. Перейдите в раздел **Управление складом \> Настройка \> Директивы местонахождения**.
1. В левой области в поле **Тип заказа на работу** выберите *Заказ на покупку*.
1. В списке выберите директиву местонахождения с именем *24 Прямая по заказу на покупку*.
1. На экспресс-вкладке **Действия директивы местоположения** выберите **Создать**, чтобы добавить строку в сетку.
1. В новой строке установите следующие значения:

    - **Порядковый номер**: *1*

        Новая строка должна находиться перед предыдущей существующей строкой. Чтобы внести изменения, воспользуйтесь кнопками **Вверх** и **Вниз** на панели инструментов, либо измените значение в поле **Порядковый номер** существующей строки на *2*.

    - **Имя:** *Поместить в профиль местоположения НАВГРУЗ*
    - **Использование фиксированного местоположения:** *Фиксированные и нефиксированные местонахождения*
    - **Разрешить отрицательные запасы:** *Снять этот флажок (=Нет)*
    - **Пакетная обработка активирована:** *Снять этот флажок (=Нет)*
    - **Стратегия:** *Нет*

1. Пока новая строка остается выбранной, выберите **Изменить запрос** над сеткой.
1. В диалоговом окне запроса на вкладке **Диапазон** выберите **Добавить**, чтобы добавить строку в сетку.
1. В новой строке установите следующие значения:

    - **Таблица:** *Местонахождения*
    - **Производная таблица:** *Местонахождения*
    - **Поле:** *Код профиля местонахождения*
    - **Критерии:** *BULK*

1. Нажмите **ОК**.
1. На странице **Директивы местоположения** на панели действий выберите **Сохранить**.

> [!NOTE]
> В экспресс-вкладке **Действия директивы местоположения** в поле **Стратегия** если используется стратегия местоположения *Консолидация*, настройка экспресс-вкладки **Разрешенное смешивание номенклатур продуктов** в **Профили местоположения** будет переопределена, и номенклатуры будут помещены в то же местоположение даже в том случае, если это действие не разрешено данной настройкой.

### <a name="create-a-mobile-device-menu-item"></a>Создание элемента меню мобильного устройства

1. Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.
1. На панели операций выберите **Создать** для создания пункта меню для использования для сортировки.
1. В заголовке установите следующие значения:

    - **Название пункта меню:** *Получение строки заказа на покупку*
    - **Заголовок:** *Получение строки заказа на покупку*
    - **Режим:** *Работа*
    - **Использовать существующую работу:** *Нет*

1. На экспресс-вкладке **Общие** установите следующие значения.

    - **Процесс создания работы:** *Получение строки заказа на покупку и размещение*
    - **Создать грузоместо:** *Да*

1. Нажмите **Сохранить**.

### <a name="configure-the-mobile-device-menu"></a>Настройка меню мобильного устройства

1. Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Меню мобильного устройства**.
1. В списке меню выберите **Входящие**.
1. На панели операций выберите **Правка**.
1. В списке **Доступные меню и пункты меню** найдите и выберите пункт меню **Получение строки заказа на покупку**.
1. Нажмите кнопку со стрелкой вправо, чтобы переместить пункт меню **Получение строки заказа на покупку** в список **Структура меню**. Таким образом, вы добавляете новый пункт меню в выбранное меню.
1. Нажмите **Сохранить**.

## <a name="scenario"></a>Сценарий

В этом демонстрационном сценарии показано, как можно поместить два различных варианта продукта в одно и то же местонахождение, когда профиль местоположения не допускает смешанных номенклатур, но включена функция *Смешивание аналитик продуктов в местонахождении*. В этом случае в качестве критерия будет использоваться вариант **Размер**.

Прежде чем начать, убедитесь, что на складе *24* имеются пустые местонахождения, в которых используется профиль местоположения *НАВГРУЗ*.

### <a name="create-a-purchase-order"></a>Создание заказа на покупку

Будет создан заказ на покупку, имеющий три строки: две строки для одного и того же номера продукта, но разных вариантов **Размер**, и третью строку для другого продукта без вариантов.

1. Перейдите в раздел **Расчеты с поставщиками \> Заказы на покупку \> Все заказы на покупку**.
1. В области действий выберите **Создать**.
1. В диалоговом окне **Создание заказа на покупку** установите следующие значения:

    - **Счет поставщика:** *1001*
    - **Склад:** *24*

1. Нажмите **ОК**.
1. Создается заказ на покупку, и на экспресс-вкладке **Строки заказа на покупку** добавляется новая строка. Запишите номер заказа на покупку.
1. В новой строке установите следующие значения:

    - **Код номенклатуры:** *B0001*
    - **Размер** *L*
    - **Количество:** *2*

1. Выберите **Добавить строку** над сеткой, чтобы добавить вторую строку заказа на покупку, и установите следующие значения:

    - **Код номенклатуры:** *B0001*
    - **Размер** *XL*
    - **Количество:** *2*

1. Выберите **Добавить строку**, чтобы добавить третью строку заказа на покупку, и установите следующие значения:

    - **Код номенклатуры:** *A0001*
    - **Количество:** *1*

1. Выберите **Сохранить**.

### <a name="receive-purchase-order-lines-in-the-warehouse-management-mobile-app"></a>Получение строк заказа на покупку в мобильном приложении управления складом

1. Выполните вход в мобильное приложение управления складом в качестве пользователя, который имеет доступ к складу *24*.
1. Выберите меню **Входящий**.
1. Выберите **Получение строки заказа на покупку**.
1. Выберите поле **PONUM**, затем введите номер заказа на покупку.
1. Подтвердите запись, выбрав кнопку подтверждения (✔) в нижней части страницы.
1. Введите номер строки из принимаемого заказа на покупку. Выберите поле **LINENUM**, затем введите *1* с помощью числовой панели.
1. Подтвердите ввод.
1. Ввод количества для получения. Два раза выберите кнопку знак "плюс" (**+**), чтобы увеличить значение в поле **Кол-во** до значения *2*.
1. Зарегистрируйте запись, выбрав кнопку (✔) в нижней части страницы, затем подтвердите ввод, снова выбрав кнопку (✔).
1. Просмотрите информацию на странице **Заказы на покупку: размещение**. На этой странице отображается работа, которая была создана для размещения (Работа 1).

    Отображается местоположение, в котором будет размещаться полученная номенклатура, грузоместо, номенклатура, размер и количество задачи **Получение строки заказа на покупку**, которая только что была выполнено.

1. Подтвердите работу по размещению.
1. Повторите шаги с 4 по 11 для строки заказа на покупку 2. Однако на шаге 8 укажите количество *1*.

    Новая работа размещения (работа 2) создается для того же местоположения, что и работа 1.

1. Повторите шаги с 4 по 11 снова для строки заказа на покупку 2. На шаге 8 укажите оставшееся количество *1*.

    Новая работа размещения (работа 3) создается для того же местоположения, что и работа 1 и работа 2. Это поведение происходит из-за того, что используется стратегия директивы местоположения *Консолидировать*, а на экспресс-вкладке **Разрешенное смешивание номенклатур продуктов** в настройке *Сборные* **профили местонахождения** разрешается смешивание в местонахождении варианта **Размер**.

1. Повторите шаги с 4 по 11 для строки заказа на покупку 3. На шаге 8 укажите количество *1* для кода номенклатуры *A0001*.

    Новая работа размещения (работа 4) создается для другого местоположения, отличного от местоположения, используемого для строк заказа на покупку 1 и 2. Это происходит из-за того, что профиль местоположения не допускает использования смешанных продуктов, но он позволяет использовать смешанные аналитики для одного и того же шаблона продукта.

1. Выберите кнопку меню в верхней части страницы (иногда называется "гамбургер" или "кнопка-гамбургер"), затем выберите команду **Отмена**, чтобы выйти из пункта **Получение строки заказа на покупку**.

> [!TIP]
> Можно повторить этот сценарий, но на этот раз задать **Размер** - *Нет* на экспресс-вкладке **Разрешить смешивание номенклатур продуктов** в **профилях местоположения** *НАВГРУЗ*, чтобы ни одна из аналитик продуктов не могла быть смешанной. В этом случае при получении заказа на покупку каждый вариант продукта будет помещен в новое местоположение.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]