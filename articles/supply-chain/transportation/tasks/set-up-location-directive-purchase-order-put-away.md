---
title: Настройка директивы местонахождения для размещения заказа на покупку
description: В этой статье описывается, как настроить простую директиву местонахождения.
author: Weijiesa
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25484efd7be026bfc3a209fb52822b87d6b76cc2
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065527"
---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Настройка директивы местонахождения для размещения заказа на покупку

[!include [banner](../../includes/banner.md)]

В этой статье описывается, как настроить простую директиву местонахождения. В этом примере создается директива места хранения, которая используется для определения того, куда поместить номенклатуры, полученные для заказа на продажу. Вы можете воспроизвести это руководство с указанными здесь данными, используя компанию с демонстрационными данными USMF. Предварительные условия: необходимо создать код метода обработки. В этой процедуре используется код метода обработки, который называется "Relabel" (переклейка этикеток). Если вы создаете директиву места хранения в своих собственных данных, необходимо настроить процессы управления складом (WMS) для вашего склада и номенклатур. Эта процедура предназначена для менеджера склада.

1. В области перехода выберите **Модули > Управление складом > Настройка > Волны > Директивы для мест хранения**.
2. В поле **Тип заказа на работу** выберите **Заказ на покупку**.

## <a name="create-a-location-directive-header"></a>Создание заголовка директивы места хранения
1. Выберите **Создать**.
2. В поле **Порядковый номер** введите число. Это последовательность, в которой обрабатывается директива места хранения для выбранного типа работы. При необходимости последовательность можно изменить.  
3. В поле **Имя** введите значение. Это уникальный идентификатор для данной директивы.  
4. В поле **Тип работы** выберите **Поместить**. Выберите тип работы для выполнения. Для директивы с типом заказа на работу "Заказ на покупку" вариант **Поместить** — единственное поддерживаемое значение.  
5. В поле **Сайт** введите значение.
6. В поле **Склад** введите значение. Оставьте код директивы пустым.  Коды директив используются для связывания строки заказа на выполнение работ типа "Поместить" с конкретной директивой. Для заказов на покупку местонахождение последней строки заказа на выполнение работ типа "Поместить" разрешается до определения шаблона работы. Поэтому связать последнюю строку шаблона работы с конкретной директивой невозможно.   
7. В поле **Код метода обработки** введите значение. Код метода обработки ограничивает использование директив места хранения, поэтому директива места хранения используется только в случае, если работник склада вводит это конкретное значение при регистрации номенклатуры с помощью мобильного устройства.  
8. Нажмите **Сохранить**.

## <a name="edit-the-query-for-directive"></a>Редактирование запроса для директивы
1. Выберите **Изменить запрос**. Использование этой директивы уже ограничено номенклатурами, зарегистрированными на указанном складе и с указанным кодом метода обработки. Можно добавить другие ограничения с помощью запроса.  
2. Нажмите **ОК**.

## <a name="add-directive-lines"></a>Добавление строк директивы
1. Выберите **Создать**. Это последовательность, в которой обрабатываются строки директивы места хранения для выбранного типа работы. При необходимости последовательность можно изменить.  
2. В поле **Количество "От"** введите число. Это минимальное количество, для которого действительна эта строка директивы.  
3. В поле **Количество "До"** введите число.
4. В поле **Единица измерения** введите значение. Единица измерения, в которое выражены количество "От" и количество "До". Если поле оставлено пустым, используется единица измерения складского учета номенклатуры.  
5. В поле **Найти количество** выберите один из вариантов.
    - "Нет" или "Количество по грузоместу": количество, зарегистрированное в каждом грузоместе.  
    - Классифицированное в единицах количество: все зарегистрированное количество.  
    - "Оставшееся количество": количество, которое еще предстоит зарегистрировать из строки заказа на покупку.  
    - "Ожидаемое количество": общее количество, указанное в строке заказа на покупку.  
6. Установите или снимите флажок **Ограничить по единице**. При выборе этого варианта и указании единицы на странице **Ограничить по единице** размещать в этом местонахождении можно будет только номенклатуры с этой единицей измерения. Например, если единицей измерения является палета, в указанном местонахождении можно размещать только номенклатуры в палетах.  
7. Установите или снимите флажок **Разрешить разделение**. Это позволяет директиве разделить количество на несколько местонахождений.  
8. Нажмите **Сохранить**.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Ограничение строки директивы определенной единицей измерения
1. Выберите **Ограничить по единице**. Эта кнопка доступна только при нажатии кнопки **Сохранить** после установки флажка **Ограничить по единице**.  
2. В поле **Единица измерения** введите значение.
3. Закройте страницу.

## <a name="add-a-location-directive-action-line"></a>Добавление строки действия директивы места хранения
1. Выберите **Создать**. Это последовательность, в которой обрабатываются строки действий директивы места хранения для выбранного типа работы. При необходимости последовательность можно изменить.  
2. В поле **Имя** введите значение. Это уникальный идентификатор для данного действия директивы.  
3. В поле **Использование фиксированного местонахождения** выберите один из вариантов.
    - Фиксированные и нефиксированные местонахождения: допустимы все нефиксированные местонахождения, а также собственное фиксированное местонахождение продукта, в пределах диапазона, заданного в запросе.  
    - "Только фиксированные местонахождения для продукта": допустимы фиксированные местонахождения для продукта, и для всех вариантов продукта используется один и тот же набор фиксированных местонахождений.  
    - "Только фиксированные местонахождения для варианта продукта": допустимы только фиксированные местонахождения, указанные для каждого варианта продукта.  
4. В поле **Стратегия** выберите один из вариантов. Заказы на работу типа "Заказ на покупку" поддерживают следующие стратегии: 
    - Нет: номенклатура помещается в первое найденное местоположение.  
    - "Консолидировать": номенклатура помещается в местонахождение, где уже есть аналогичные номенклатуры.  
    - Пустое местонахождение без входящих работ: номенклатура перемещается в первое пустое найденное местонахождение. Местонахождение считается пустым, если в нем нет физических запасов и ожидаемой входящей работы.  
5. Нажмите **Сохранить**.

## <a name="edit-the-query-for-directive-action-line"></a>Редактирование запроса для строки действия директивы
1. Выберите **Изменить запрос**.
2. Выберите **Добавить**.
3. В поле **Поле** введите `location profile ID`. В этом примере мы ограничим возможные местонахождения, используя код профиля местонахождения.  
4. В поле **Критерии** введите значение.
5. Нажмите **ОК**. Можно продолжать добавлять строки директивы и действия директивы, пока не будут охвачены все возможные сценарии на вашем складе.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]