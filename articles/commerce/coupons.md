---
title: Купоны
description: Эта статья содержит обзор возможностей, связанных с купонами, в Microsoft Dynamics 365 Commerce.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-30
ms.openlocfilehash: 20427a04a552ddec013daa6576ec64ab7046e95f
ms.sourcegitcommit: 87e75aa6af2c3280316d7d73eafa14a52353a5e4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2022
ms.locfileid: "9709768"
---
# <a name="coupons"></a>Купоны

[!include [banner](../includes/banner.md)]

Эта статья содержит обзор возможностей, связанных с купонами, в Microsoft Dynamics 365 Commerce.

Купоны — это коды и штрих-коды, используемые для добавления скидок к проводкам. Розничные продавцы распределяют купоны среди потенциальных или существующих клиентов, чтобы помочь улучшить свое распознавание торговой марки, улучшить конверсию, сохранить базу клиентов, увеличить объем продаж и, в конечном итоге, увеличить выручку. Купоны стали одним из самых популярных маркетинговых инструментов и являются новой нормой продаж в электронной коммерции.

В Dynamics 365 Commerce купоны связаны со скидками и рассматриваются как дополнительная проверка после скидок. Каждый купон связан с одной скидкой, а связанная скидка определяет набор продуктов, для которых действует купон.

Ценовые группы, связанные со скидкой, определяют подходящие условия, для которых можно использовать купон. Эти условия включают группы клиентов и каналы продаж. Купоны также предоставляют свойства **Лимит использования** и **Требуется клиент**, которые могут использоваться для настройки необязательных ограничений по использованию.

У каждого купона может быть несколько кодов купона и штрих-кодов купона, и у каждого кода может быть своя собственный диапазон дат действия и статус. Если статус кода имеет значение **Неактивный**, этот код нельзя использовать ни в одном канале.

## <a name="set-up-a-coupon"></a>Настройка купона

Прежде чем настраивать купоны, необходимо настроить штрих-код купона и две номерные серии купонов.

Для настройки купона в Commerce headquarters выполните следующие действия.

1. Перейдите в раздел **Retail и Commerce \> Управление запасами \> Штрих-коды и метки \> Символы маски**.
1. Выберите **Добавить** для создания символа маски типа **Код купона**. В поле **Символ** можно выбрать любой неиспользуемый символ.
1. Перейдите в раздел **Retail и Commerce \> Управление запасами \> Штрих-коды и метки \> Настройка маски штрих-кода**.
1. Выберите **Создать** для создания маски штрих-кода типа **Купон**.
1. Перейдите в раздел **Retail и Commerce \> Управление запасами \> Штрих-коды и метки \> Настройка штрих-кода**.
1. Выберите **Создать**, чтобы создать штрих-код, который использует созданную вами маску штрих-кода.
1. Перейдите в раздел **Управление организацией \> Номерные серии**.
1. Создайте две номерные серии:

    1. Одна последовательность для ссылки **Номер купона**. Эта последовательность определяет уникальный идентификатор купона.
    1. Одна последовательность для ссылки **Идентификатор кода купона**. Эта последовательность определяет уникальный идентификатор каждого кода купона для купона.

    Для обеих номерных серий необходимо установить в поле **Область действия** значение **Компания**. В большинстве случаев оба порядковых номера должны генерироваться автоматически.

1. Перейдите в раздел **Параметры Commerce \> Цены и скидки \> Купоны**.
1. В поле **Маска штрих-кода купона** задайте ранее созданный штрих-код.
1. Перейдите в раздел **Параметры Commerce \> Номерные серии**.
1. Выберите номерную серию, созданную ранее для ссылок **Номер купона** и **Идентификатор кода купона**.

Для настройки купона необходимо создать скидку и купон отдельно, а затем связать их путем выбора скидки в поле **Скидка** в конфигурации купона. После связывания купона со скидкой поля **Статус**, **Дата начала действия** и **Дата окончания срока действия** связанной скидки становятся доступны только для чтения, поскольку эти значения определяются статусом купона и сроком его действия. Если статус купона имеет значение **Активный**, статус связанной скидки автоматически обновляется на **Включено**. Аналогично, если статус купона изменяется на **Неактивный**, статус связанной скидки автоматически обновляется на **Выключено**.

## <a name="use-a-coupon"></a>Использование купона

Чтобы добавить купон в проводку продаж в POS-терминале Commerce, можно использовать код купона или штрих-код купона. Для использования кода купона выберите операцию **Добавить код купона**, затем введите код. Чтобы использовать штрих-код купона, можно или выполнить сканирование штрих-кода с помощью устройства сканирования, или ввести штрих-код, используя цифровую клавиатуру на экране **Проводка**.

Предприятиям розничной торговли иногда требуется, чтобы кассиры могли давать скидки по фиксированной сумме клиентам в целях успокоения или по причине дефектов продукта, но они не хотят печатать коды купонов и распределять их по кассирам. В этом случае можно задать для параметра купона **Применить без кода купона** значение **Да**. Затем кассиры на POS-терминале могут использовать функцию **Применить купон** в операции **Просмотр доступных скидок** для добавления купона в проводку без ввода этого кода вручную. Если для купона существует несколько кодов купона, система автоматически выбирает первый активный код и применяется его к проводке.

Чтобы добавить купон в заказ на продажу из центра обработки вызовов, пользователь центра обработки вызовов должен выбрать **Купоны** на вкладке **Управление** панели операций на странице заказа на продажу.

Чтобы добавить купон в заказ электронной коммерции, покупатель может ввести код купона в поле **промо-код** в корзине для покупок.

После добавления купона в заказ на продажу механизм ценообразования сразу инициирует пересчет для всего заказа, независимо от того, активирован ли отложенный расчет.

> [!NOTE]
> В Commerce версии 10.0.30 и более ранних после того, как пользователи центра обработки вызовов добавляют купона в заказ на продажу центра обработки вызовов, они должны выбрать **Пересчитать** в группе **Рассчитать** на вкладке **Продажа** на панели операций, чтобы применить скидку, связанную с этим купоном.

## <a name="coupon-usage-limit"></a>Лимит использования купона

Купоны можно настроить как купоны с ограниченным использованием. Лимит использования можно задать по клиенту, по каналу или глобально. Лимит использования применяется к коду купона на купоне. Например, купон однократного использования, имеющий два кода купона, можно использовать два раза, по одному разу для каждого кода купона.

Купоны могут использоваться в разных каналах продаж. Однако для центра вызова купоны с ограничением по использованию могут применяться только в том случае, если включен параметр **Включить заполнение заказа** для канала центра обработки вызовов. Если параметр **Включить заполнение заказа** отключен, могут быть применены только купоны без лимитов на использование.

[!INCLUDE[footer-include](../includes/footer-banner.md)]